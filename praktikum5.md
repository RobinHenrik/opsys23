# Praktikum 5

Selles praktikumis tutvusin lähemalt failiõigustega Linuxis.
Lõin erinevaid kasutajaid erinevate õigustega ning erinevaid katalooge ja faile erinevate õigustega, et mõista kuidas õigused Linuxis töötavad.
### Ülesanne 5.1
a) Et lugeda faili kataloogis /tmp/kaust on vaja kataloogi õigusi u=rx ning faili õigus u=r  

b) Et kustutada faili kataloogis /tmp/kaust on vaja kataloogi õigusi u=wx ning failis u=w
### Ülesanne 5.2
Sest chmod a=x skriptifail määrab kõikidele kasutajatele, vaid skriptifaili käivitamisõiguse.
Skriptifaili käivitamiseks läheb lisaks käivitamisõigusele vaja ka lugemisõigust.
Enne skriptifaili käivitamist kontrollib operatsioonisüsteem selle sisu, et teada kuidas skripti täita. Ilma lugemisõiguseta saa sisu kontrollida.
### Ülesanne 5.3
Sest failidele ja kataloogidele määratakse vaikimisi õigused vastavalt kasutaja ja tema omanimelisele grupi õiguste järgi. Lisaks kui kasutajanimi ja grupi nimi on samad, siis on väga kerge tuvastada, mis kasutaja grupiga on tegu.
### Ülesanne 5.4
Minimaalsed õigused on g=r  

<img width="647" alt="ul4" src="https://github.com/RobinHenrik/opsys23/assets/144727763/f44e25d8-8ec5-4655-bbe6-b36d32576200">  

### Ülesanne 5.5
<img width="654" alt="ul5" src="https://github.com/RobinHenrik/opsys23/assets/144727763/6e3781c4-b0c6-446f-98d2-6f48d8767633">  

Setuid-õigused on kasulikud, kui on vaja teatud programmil või skriptil teha midagi, mille jaoks kasutajal endal õiguseid pole.  

### Ülesanne 5.6
Jah setuid kasutamine võib potensiaalselt vähendada süsteemi turvalisust. See võib näiteks anda administraatoriõigused programmile, millel neid olla ei tohiks. Programm saab tegutseda nagu administraator isegi, kui programmi käivitajal neid õigusi muidu ei oleks.  

### Ülesanne 5.7
Sticky-bit-õigustega yhiskaust-kataloogist saavad nüüd peeter-kasutaja loodud faile kustutada peeter-kasutaja ise, admin-kasutaja käsuga sudo ning root kasutaja.  

### Ülesanne 5.8
peeter@neem-U23:/home/opetaja/klass$ getfacl hinded.txt  

\# file: hinded.txt  

\# owner: opetaja  

\# group: opetaja  

user::rw-  

group::---  

group:direktor:rw-  

mask::rw-  

other::---  

### Ülesanne 5.9
chattr +i - parameetriga faili sisu ei saa keegi modifitseerida.
Käskudega "sudo chattr -i testfail-2" ja "sudo rm testfail-2" saab siiski faili kustutada.
