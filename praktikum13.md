Selles praktikumis õppisin Windows Powershellis skriptimist.
[tulemus.txt](https://github.com/RobinHenrik/opsys23/files/13708910/tulemus.txt)
**********************
Windows PowerShell transcript start
Start time: 20231218235445
Username: NEEM-W11\Robin
RunAs User: NEEM-W11\Robin
Configuration Name: 
Machine: NEEM-W11 (Microsoft Windows NT 10.0.22621.0)
Host Application: C:\Windows\system32\WindowsPowerShell\v1.0\PowerShell_ISE.exe
Process ID: 3856
PSVersion: 5.1.22621.2506
PSEdition: Desktop
PSCompatibleVersions: 1.0, 2.0, 3.0, 4.0, 5.0, 5.1.22621.2506
BuildVersion: 10.0.22621.2506
CLRVersion: 4.0.30319.42000
WSManStackVersion: 3.0
PSRemotingProtocolVersion: 2.3
SerializationVersion: 1.1.0.1
**********************
0.	23:54:45.006	ALGUS:	Aeg: esmaspäev 12.18.2023 23:54 +02:00 Teostaja: Robin
1.1.	23:54:45.034	host:	NEEM-W11
1.2.	23:54:45.038	Powershelli versioon:	5.1.22621.2506
1.3.	23:54:45.073	Windowsi versioon:	10.0.22621
2.1.	23:54:45.168	IP-aadress:
10.0.2.15
127.0.0.1
2.2.	23:54:45.203	Võrgumask:
24
8
2.3.	23:54:45.209	Gateway:	10.0.2.2
2.4.	23:54:45.515	DHCP olek:	Enabled
2.5.	23:54:45.550	MAC-aadress:	08-00-27-D1-08-47
3.1.	23:54:46.582	Protsessor:	Intel64 Family 6 Model 186 Stepping 3
3.2.	23:54:47.468	Põhimälu (RAM):	3.98 GB
4.1.	23:54:47.507	Graafikakaart:	VirtualBox Graphics Adapter (WDDM)
4.2.	23:54:47.524	Draiveri versioon:	7.0.10.8379
4.3.	23:54:47.556	Draiveri kuupäev:	07/12/2023 03:00:00
4.4.	23:54:47.622	Ekraani lahutus:
2322
x
1492
5.1.	23:54:47.684	Partitsioonitable:

DeviceID                     Size
--------                     ----
Disk #0, Partition #0   104857600
Disk #0, Partition #1 67886907392
Disk #0, Partition #2   707788800
5.2.	23:54:47.718	Ketta maht:	63.99 GB
5.3.	23:54:47.748	C:-ketta vaba ruum:	34.28 GB
6.	23:54:48.091	PCI seadmed:



Description                          DriverVersion   Manufacturer
-----------                          -------------   ------------
CPU to PCI Bridge                    10.0.22621.1    Intel
High Definition Audio Controller     10.0.22621.2506 Microsoft
Intel(R) PRO/1000 MT Desktop Adapter 8.4.13.0        Intel
PCI to ISA Bridge                    10.0.22621.1    Intel
Standard SATA AHCI Controller        10.0.22621.2506 Standard SATA AHCI Controller
USB xHCI Compliant Host Controller   10.0.22621.2506 Generic USB xHCI Host Controller
VirtualBox Graphics Adapter (WDDM)   7.0.10.8379     Oracle Corporation
VirtualBox Guest Device              7.0.10.8379     Oracle Corporation


7.	23:54:48.139	Arvutis olevad kasutajad:

Name               Description                                                                                     LocalAccount Disabled
----               -----------                                                                                     ------------ --------
Administrator      Built-in account for administering the computer/domain                                                  True     True
DefaultAccount     A user account managed by the system.                                                                   True     True
Guest              Built-in account for guest access to the computer/domain                                                True     True
Robin                                                                                                                      True    False
Robin-tava                                                                                                                 True    False
tootaja1                                                                                                                   True    False
tootaja2                                                                                                                   True    False
WDAGUtilityAccount A user account managed and used by the system for Windows Defender Application Guard scenarios.         True     True
ylemus                                                                                                                     True    False


8.	23:54:48.175	Käimasolevate protsesside arv:	138
Sort-Object : Exception getting "StartTime": "Access is denied"
At C:\Users\Robin\Desktop\kodutöö13.ps1:58 char:63
+ ... d protsessi" (Get-Process | Sort-Object StartTime -Descending | Selec ...
+                                 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidResult: (System.Diagnostics.Process (Idle):PSObject) [Sort-Object], GetValueInvocat
ionException
    + FullyQualifiedErrorId : ExpressionEvaluation,Microsoft.PowerShell.Commands.SortObjectCommand
Sort-Object : Exception getting "StartTime": "Access is denied"
At C:\Users\Robin\Desktop\kodutöö13.ps1:58 char:63
+ ... d protsessi" (Get-Process | Sort-Object StartTime -Descending | Selec ...
+                                 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidResult: (System.Diagnostics.Process (Idle):PSObject) [Sort-Object], GetValueInvocationException
    + FullyQualifiedErrorId : ExpressionEvaluation,Microsoft.PowerShell.Commands.SortObjectCommand

9.	23:54:48.252	10 viimasena käivitatud protsessi:

**********************
Windows PowerShell transcript end
End time: 20231218235448
**********************
