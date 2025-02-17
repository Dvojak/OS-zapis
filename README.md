<h2>Zapis OS 17. 2. 2025</h2>
Importovat Ubuntu user server velky

log na server ssh na server:
```
ip add 
ssh student@192.168.10.30
``` 
```
sudo su -
```
Updatnout a stáhnout
```
Sudo apt update
Sudo apt install phpmyadmin
Sudo apt install dialog
dpkg-reconfigure tzdata
sudo apt install libapache2-php-mod
sudo apt install mariadb-server
```

Pokračujeme

Mysql
```
 mysql
 ### Vejdeme do mysql řádku ###
 show databases;
 create database wordpress;
 show databases;
 create user "student@localhost" identified by "student"
 use mysql
 show tables
 select * from user;
 flush privileges;
```
Vlezme do phpmyadmin pomocí server ip
```
### Pro me to bylo tohle ###
### Google ###
192.168.10.30/phpmyadmin/
### phpmyadmin ###
student@localhost
student
### dostali jsme se dovnitr ###
```
zpět do mysql
```
grant all privileges on wordpress.* to "student@localhost";
flush privileges;
quit
```
v terminalu
```
logout
### odešli jsme z roota ###
sudo apt install man-db
mysqldump -u student@localhost -pstudent wordpress  
mysqldump -u student@localhost -pstudent wordpress  > data.sql
 mcedit data.sql
 f10
 cat data.sql | mysql -u student@localhost -pstudent wordpress
 mc
```
mc
```
etc/apache2/sites-enable/@000-def...
(vůbec nevím jestli jsme v tom něco dělali)
```
Zpátky do terminal
```
sudo su -
cd /var/www/html/
ps axu | grep apache
```
Jít na wordpress stránky download 
vzít adresu download buttonu 
```
wget https://wordpress.org/latest.zip
unzip.zip
mv wordpress/* ./
chown www-data.www-data -R ./*
ls -l
rm index.html
```
V browseru jít na wordpress na ip toho serveru 
```
### Pokracuj v instalaci ###
database: wordpress
user: student@localhost
password: student
### Vyjede vec s konfigem nějakého wp-config.php ###
### upravte to nějak###
vim wp-config.php
```
Ve vimu
```
ctrl + shift + v
:wq
```
pak pokračovat na stránce 
Skončíš na  Information needed
```
Jakýkoli 
všechno si teď můžeš vymyslet
heslo si asi uprav
email si klidně vymysli
```
Jsme ve wordpressu 
Nainstalujeme antivir v pluginech
```
Wordfence
Wpvivid
Wp-optimize
Advanced database cleaner
```
https://developer.wordpress.org/themes/advanced-topics/child-themes/




Nejspíš to nebude vůbec k něčemu a možně chybné
--------------------------------------------------------------
Nespoléhejte se na to. Dělám to jenom abych dával pořádný pozor.											

