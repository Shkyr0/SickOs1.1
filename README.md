
# SickOs1.1

This is a Write up for the VM named SickOs 1.1  
[Link VM](https://www.vulnhub.com/entry/sickos-11,132/)  
SO 

## FIRST ONE  
do a  
```bash  
sudo netdiscover  
```  
![screen1](https://github.com/Shkyr0/SickOs1.1/blob/main/1.png)

you just find the IP (in this case 192.168.56.101)

## STEP 2  
```bash  
do nmap -Pn -A 192.168.56.101  
```  
![screen2](https://github.com/Shkyr0/SickOs1.1/blob/main/2.png)

Just after, you put the proxy in Firefox; you need it to access the site.

![screen3](https://github.com/Shkyr0/SickOs1.1/blob/main/3.png)  

## STEP 3  
so ***GO TO THE SITE***  

AND discover this 

![screen4](https://github.com/Shkyr0/SickOs1.1/blob/main/4.png)  

## STEP 3  
Now you can use fuzz or dirbuster, or be a robot and just try the most obvious page like  

[*http://192.168.56.10/robots.txt*](http://192.168.56.101/robots.txt)  

![screen5](https://github.com/Shkyr0/SickOs1.1/blob/main/5.png)  

so I go to wolfcms  

![screen3](https://github.com/Shkyr0/SickOs1.1/blob/main/6.png)  

and after finding this page, I look on exploit db if there is any exploit for this version of wolfcms

[exploit db link](https://www.exploit-db.com/exploits/38000)  

## STEP 4  
so go to http://192.168.56.101/wolfcms/?/admin/login  

![screen3](https://github.com/Shkyr0/SickOs1.1/blob/main/7.png)  

after this, go try admin admin (default log)  

![screen3](https://github.com/Shkyr0/SickOs1.1/blob/main/8.png)  

upload a reverse shell in PHP. I use one from pentestmonkey.  
The address to launch it is http://<IP-in-your-case>/wolfcms/public/shell.php  

![screen3](https://github.com/Shkyr0/SickOs1.1/blob/main/9.png)  

## STEP 5  
rummage through files  
found this  

![screen10](https://github.com/Shkyr0/SickOs1.1/blob/main/10.png)  

open the config.php  

![screen10](https://github.com/Shkyr0/SickOs1.1/blob/main/11.png)  

BUT when I try to connect as root, that doesn't work BECAUSE it's not the right name 😐  

![screen10](https://github.com/Shkyr0/SickOs1.1/blob/main/12.png)  

so when I just alt-tab the name of my VirtualBox window is SickOs, so I try it because I'm stupid 🙃  
and anyway that worked  

![screen10](https://github.com/Shkyr0/SickOs1.1/blob/main/13.png)  

## STEP 6  
go to  
```bash  
cd ~  
```  
and  
```bash  
ls  
```  
![screen10](https://github.com/Shkyr0/SickOs1.1/blob/main/14.png)  

and to finish, just do  
```bash  
cat a0216ea4d51874464078c618298b1367.txt  
```

# FINISH GG WP  
🥳🥳🥳
