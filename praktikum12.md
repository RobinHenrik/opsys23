# Praktikum 12 

Selles praktikumis õppisin looma linuxi skripte.

### Ülesanne 3 
```
#!/bin/sh
echo "Sisesta oma nimi: "
read nimi
echo "Sisesta oma eriala: "
read eriala
echo "Sisesta enda matriklinumber"
read matriklinumber
echo "$nimi - $eriala - $matriklinumber"
```
<img width="491" alt="ül3" src="https://github.com/RobinHenrik/opsys23/assets/144727763/0d782d28-1795-485f-af78-f5739c60ed5a"> 

### Ülesanne 4 
```
#!/bin/bash
echo "Sisestage laiend, mida soovite asendada: "
read asendatav
echo "Sisestage laiend, millega soovite asendada: "
read asendus

for i in $(ls)
do
    if [ "${i##*.}" = "$asendatav" ]; then
        uus=$(echo "$i" | sed -e "s/.$asendatav/.$asendus/")
        mv "$i" "$uus"
    fi
done
```

<img width="410" alt="ül4" src="https://github.com/RobinHenrik/opsys23/assets/144727763/6cb4cbda-9e4a-44bb-949d-486464ff09fc"> 

### Ülesanne 5 
```
#!/bin/bash
IFS=$'\n'

echo "Sisestage protsessi nimi: "
read nimi



id=$(ps -A | grep "$nimi" | tr -s ' ' | cut -d ' ' -f2)

if [ -n "$id" ]
then
        echo "Protsessi-ID: $id"
        echo "Protsessi nimi: $nimi"
else
        echo "Protsessi ei leitud"
fi
```
<img width="408" alt="ül5" src="https://github.com/RobinHenrik/opsys23/assets/144727763/1f120b63-c15a-4bbc-83c4-7eb733a21a1f">  

### Ülesanne 6 
```
#!/bin/bash

astendus () {
  algne=$1
  uus=1
  aste=$2
  for ((i=1; i <= aste; i++))
  do
        uus=$((uus * algne))
  done
  echo $uus
}

a=$(astendus 9 5)
echo $a
```
<img width="410" alt="ül6" src="https://github.com/RobinHenrik/opsys23/assets/144727763/d8cbb4c0-297d-4880-9148-6ef4e7c9b30b"> 

 ### Ülesanne 7 
 
<img width="1920" alt="ül7" src="https://github.com/RobinHenrik/opsys23/assets/144727763/af314772-c20a-461e-bdc0-8003121ce5ae"> 
<img width="409" alt="image" src="https://github.com/RobinHenrik/opsys23/assets/144727763/9b39a614-492b-4bd6-8ce9-efddd8811ba4">

