Selles praktikumis õppisin Windows Powershellis skriptimist.


Fail:
[tulemus.txt](https://github.com/RobinHenrik/opsys23/files/13708910/tulemus.txt)

Olulisemad käsud/käsu osad: 
<br>
<br>
function Valjasta:
<br>
Defineerib PowerShelli funktsiooni nimega Valjasta, millel on kolm parameetrit: $nr, $param, ja $sisu.
Kontrollib, kas $sisu on null, massiiv või muu tüüp ning genereerib vastavalt sellele väljundirea.

Start-Transcript -Path $failiTee -Append:
<br>
Alustab transkriptsiooni, salvestades kõik skripti väljundid tekstifaili.
Append valik tagab, et olemasolevat faili jätkatakse.

Stop-Transcript:
<br>
Lõpetab transkriptsiooni. 
<br>
Skript: 



```
#$nr:	küsimuse number
#$param: mis parameetriga tegemist (võimalikult lühidalt)
#$sisu:	väljastatav sisu
function Valjasta{
	param ($nr, $param, $sisu)
	$fail = ".\tulemus.txt"
	$aeg = Get-Date -Format "HH:mm:ss.fff"
	if($sisu -eq $null){
		$rida = "$nr.	$aeg	${param}:	NULL"
		Write-Output $rida
		$rida | Out-File -FilePath $fail -Append
	}elseif($sisu.GetType().Name -eq "Object[]"){
		$rida = "$nr.	$aeg	${param}:"
		Write-Output $rida $sisu
		$rida | Out-File -FilePath $fail -Append
		$sisu | Out-File -FilePath $fail -Append
	}else{
		$rida = "$nr.	$aeg	${param}:	$sisu"
		Write-Output $rida
		$rida | Out-File -FilePath $fail -Append
	}
}

$failiTee = "$env:USERPROFILE\tulemus.txt"
Start-Transcript -Path $failiTee -Append


[int]$aegA = (Get-Date).Millisecond
Valjasta 0 "ALGUS" ("Aeg: "+(Get-Date -Format "dddd MM/dd/yyyy HH:mm K")+" Teostaja: Robin")
Valjasta 1.1 "host" (hostname)
Valjasta 1.2 "Powershelli versioon" ($PSVersionTable.PSVersion)
Valjasta 1.3 "Windowsi versioon" (Get-CimInstance Win32_OperatingSystem).Version

Valjasta 2.1 "IP-aadress" (Get-NetIPAddress | Where-Object {$_.AddressFamily -eq 'IPv4'}).IPAddress
Valjasta 2.2 "Võrgumask" (Get-NetIPAddress | Where-Object {$_.AddressFamily -eq 'IPv4'}).PrefixLength
Valjasta 2.3 "Gateway" (Get-NetRoute | Where-Object {$_.DestinationPrefix -eq '0.0.0.0/0'}).NextHop
Valjasta 2.4 "DHCP olek" (Get-NetIPConfiguration | Select-Object -ExpandProperty NetIPv4Interface).Dhcp
Valjasta 2.5 "MAC-aadress" (Get-NetAdapter | Where-Object {$_.Status -eq 'Up'}).MacAddress

Valjasta 3.1 "Protsessor" (Get-CimInstance Win32_Processor).Caption
Valjasta 3.2 "Põhimälu (RAM)" "$([math]::Round((Get-CimInstance Win32_ComputerSystem).TotalPhysicalMemory / 1GB, 2)) GB"

Valjasta 4.1 "Graafikakaart" (Get-CimInstance Win32_VideoController).Caption
Valjasta 4.2 "Draiveri versioon" (Get-CimInstance Win32_VideoController).DriverVersion
Valjasta 4.3 "Draiveri kuupäev" (Get-CimInstance Win32_VideoController).DriverDate
Valjasta 4.4 "Ekraani lahutus" (Get-CimInstance Win32_VideoController).CurrentHorizontalResolution, "x", (Get-CimInstance Win32_VideoController).CurrentVerticalResolution

Valjasta 5.1 "Partitsioonitable" (Get-CimInstance Win32_DiskPartition | Select-Object -Property DeviceID, Size)
Valjasta 5.2 "Ketta maht" "$([math]::Round((Get-CimInstance Win32_DiskDrive | Select-Object -ExpandProperty Size) / 1GB, 2)) GB"
Valjasta 5.3 "C:-ketta vaba ruum" "$([math]::Round(((Get-WmiObject Win32_LogicalDisk | Where-Object { $_.DeviceID -eq 'C:' }).FreeSpace) / 1GB, 2)) GB"

Valjasta 6 "PCI seadmed" (Get-WmiObject –Class Win32_PnpSignedDriver | Where-Object {$_.DeviceID –like „PCI*“} | Select-Object Description, DriverVersion, Manufacturer | Sort-Object Description | Format-Table)

Valjasta 7 "Arvutis olevad kasutajad" (Get-WmiObject -Class Win32_UserAccount | Select-Object Name, Description, LocalAccount, Disabled | Sort-Object Name | Format-Table -AutoSize)

Valjasta 8 "Käimasolevate protsesside arv" ((Get-Process).Count)

Valjasta 9 "10 viimasena käivitatud protsessi" (Get-Process | Sort-Object StartTime -Descending | Select-Object -First 10 | Select-Object Name, Id, StartTime | Sort-Object StartTime)

Valjasta 10 "Arvuti kuupäev ja kellaaeg" (Get-Date)

[int]$aegL = (Get-Date).Millisecond
$ajakulu = ($aegL - $aegA)

Valjasta "*" "TEHTUD" "$ajakulu`n`n"

Stop-Transcript
```
