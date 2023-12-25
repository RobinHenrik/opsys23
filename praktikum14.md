# Praktikum 14  
Selles praktikumis õppisin kasutama Azure vm-i. 

### Ülesanne 1 

![ül1](https://github.com/RobinHenrik/opsys23/assets/144727763/063e4b14-7358-4918-be40-84589000d0f2)

### Ülesanne 2 

![ül2_1](https://github.com/RobinHenrik/opsys23/assets/144727763/9080c7be-d619-46e2-9b50-8c1b0e981b01)
![ül2_2](https://github.com/RobinHenrik/opsys23/assets/144727763/c50dfc49-38b1-429b-b816-4d51246cf44e)

### Ülesanne 3 
![ül3](https://github.com/RobinHenrik/opsys23/assets/144727763/34fd1306-c84c-405a-a327-38d0baebaf00)

### Ülesanne 4 
![ül4_1](https://github.com/RobinHenrik/opsys23/assets/144727763/46174998-5890-4e4c-bbbf-b2665c13842c)
![ül4_2](https://github.com/RobinHenrik/opsys23/assets/144727763/5c0a6904-809b-4392-9aed-c57bfd585af1)


### Ülesanne 5 
![ül5](https://github.com/RobinHenrik/opsys23/assets/144727763/53659a12-9f09-4036-8a36-c008fac82fcd) 

### Ülesanne 6 


![ül6_oige](https://github.com/RobinHenrik/opsys23/assets/144727763/12d806d0-e0be-4580-b21d-bf46cd5a57c5)  

Skript: 



```
#!/bin/bash

kaust="accident"

failid=("$kaust"/*.md)

for fail in "${failid[@]}"; do
        if [ -f "$fail" ] && [ -s "$fail" ] && [ -r "$fail" ]; then

                echo "Fail: $fail"
                cat "$fail"
                echo "----------------------------------------------------"
        fi
done
```


