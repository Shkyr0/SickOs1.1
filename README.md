# SickOs1.1

This is a Write up for the VM named SickOs 1.1 
[Link VM]([https://www.example.com](https://www.vulnhub.com/entry/sickos-11,132/))
SO 

## FIRST ONE 
do a 
```bash
sudo netdiscover
```
![screen1](https://github.com/Shkyr0/SickOs1.1/blob/main/1.png)

you jsut find the IP ( in this case 192.168.56.101 )

## STEP 2 
```bash
do nmap -Pn -A 192.168.56.101
```
![screen2](https://github.com/Shkyr0/SickOs1.1/blob/main/2.png)

Juste after you put the proxy in fierfox u need it for access to the site 

![screen3](https://github.com/Shkyr0/SickOs1.1/blob/main/3.png)

so ***GO TOT THE SITE***

AND discover this shit

![screen4](https://github.com/Shkyr0/SickOs1.1/blob/main/4.png)

now you can use fuzz or dirbuster or being a robot guys and just try the most obvious page LIKE 

[*http://192.168.56.10/robots.txt*](http://192.168.56.101/robots.txt)

![screen5](https://github.com/Shkyr0/SickOs1.1/blob/main/5.png)

so i go to wolfcms

![screen3](https://github.com/Shkyr0/SickOs1.1/blob/main/6.png)

and after fine this page i look on exploit db if there is any exploit for this version of wolfcms

[exploit db link](https://www.exploit-db.com/exploits/38000)

so go to http://192.168.56.101/wolfcms/?/admin/login 

![screen3](https://github.com/Shkyr0/SickOs1.1/blob/main/7.png)

after this go try admin admin ( default log ) 

![screen3](https://github.com/Shkyr0/SickOs1.1/blob/main/8.png)

upload a revershell in PHP i use one from pentestmonkey 
the adrress to lunch-it is  http://<IP-in-your-case>/wolfcms/public/shell.php

![screen3](https://github.com/Shkyr0/SickOs1.1/blob/main/9.png)

rummage through files 
found this 

![screen10](https://github.com/Shkyr0/SickOs1.1/blob/main/10.png)

open the config.php

![screen10](https://github.com/Shkyr0/SickOs1.1/blob/main/11.png)

