# Praktikum 6

Selles praktikumis tutvusin erinevate protsessidega ning nendega seotud käskudega. Õppisin kuidas muuta protsesside sisendit ja väljundit ning kuidas neid suunata failidesse.

### Ülesanne 6.1
![ül1](https://github.com/RobinHenrik/opsys23/assets/144727763/a906c3cd-396c-4948-98f8-b6cb71decbc5)

### Ülesanne 6.2
![ül2](https://github.com/RobinHenrik/opsys23/assets/144727763/fd8bbd55-a03a-4b39-a396-11da2ea65d2a)

### Ülesanne 6.3
ps -axu | grep daemon | sort | tr -s " " | cut -d " " -f11-

![ül3](https://github.com/RobinHenrik/opsys23/assets/144727763/1a03d56f-28af-41cc-9b49-eb9e0c5d4a54)

### Ülesanne 6.4
ip a | sort | tr -s " " | cut -d" " -f3 | tail -n+3 | head -1 | cut -d"/" -f1 

ip a | sort | tr -s " " | cut -d" " -f3 | tail -n+3 | head -1 | cut -d"/" -f1 >ipaddress.txt

![ül6](https://github.com/RobinHenrik/opsys23/assets/144727763/1fe95d95-8c66-4b9b-800f-ef74b0709abf)
