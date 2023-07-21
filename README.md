# Snipe-IT-Open-Source-Asset-Management

- Easy Install Snipe-IT Asset Management on Windows 10 and 11
- Start...
- Requirements:
- webserver: with version PHP >= 7.4 and < v8.1.2
-Enable PHP Extensions: LDAP,...
-OK. Now, download the web server XAMPP for Windows
- use version: 8.1.12 / PHP 8.1.12
1. install Xampp server
waiting for Xampp install...
ok. xampp install finish.
2. install composer
ok. check version php, composer has installed yet.
Open command line
php -v
composer 
Press enter
OK.
3. Download and unzip Snipe-IT. After copy and paste into C:\xampp\htdocs
- rename folder snipe-it-6.0.14 to snipe-it
4. Configuration snipe-it
Copy and paste file .env.example in C:\xampp\htdocs\snipe-it. Rename to .env
Open file .env edit rows:
APP_URL=localhost
Save and close
- Open file php.ini and un-comment/delete; rows: C:\xampp\php
- extension=ldap
- extension=gd
- extension=sodium
-save and close.
5. Create a database for snipe-it with name snipeit
- start apache, MySQL service
- open browse http://localhost/phpmyadmin
-building laravel 
- open command prompt
- cd /
- C:\>cd xampp/htdocs/snipe-it
- composer install
- 6. Generate Your App Key
- open command promtp
- cd /
- C:\xampp\htdocs\snipe-it
- php artisan key: generate
- yes
7. Pre-Flight & Setup
- open file .env and edit rows:
- DB_DATABASE=snipeit
- DB_USERNAME=root
- Save and close
-Config DocumentRoot in Apache
- C:\xampp\apache\conf
- open file httpd.conf and add:
- DocumentRoot "/xampp/htdocs/snipe-it/public"
- <Directory "/xampp/htdocs/snipe-it/public">
- Save and close
- restart Apache service
- open browse input http://localhost
-Yeah!
- continue...
- Enter the information in the form:
+ Domain mail
+ First name:
+ Last name
+ Username...
OK.
GoodLuck!

