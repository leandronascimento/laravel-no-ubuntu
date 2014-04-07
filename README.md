Laravel-no-Ubuntu
=================

Passos Instalação Laravel no Ubuntu


Preparando o ubuntu para receber as instalações

sudo apt-get update
sudo apt-get upgrade

Instalando o Apache, Php e o Mysql

sudo apt-get install apache2
sudo apt-get install php5
sudo apt-get install mysql-server
sudo apt-get install php5-mysql

Verificando as instalações

php -v
apache2 -v

Instalando as extensões necessarias

sudo apt-get install unzip
sudo apt-get install curl
sudo apt-get install openssl
sudo apt-get install php5-mcrypt


Instalando o git

$ apt-get install git

Gerando as chaves do git

ssh-keygen

Copiando a chave publica

cat ~/.ssh/id_rsa.pub


Instalando o composer

curl -sS https://getcomposer.org/installer | php
sudo mv composer.phar /usr/local/bin/composer


Ativando o mod_rewrite


sudo a2enmod rewrite

Reiniciando o apache

sudo service apache2 


Trabalhando com Vhost

Abra o arquivo de configução do Vhost

sudo nano /etc/apache2/sites-available/default

Agora, procure por "AllowOverride None" (que deverar aparecer DUAS vezes) e mude para "AllowOverride All". 

Procure por essas duas linhas

DocumentRoot /var/www
<Directory /var/www>

Altere para

DocumentRoot /var/www/public
<Directory /var/www/public>


Instalando o Laravel

git clone git@github.com:laravel/laravel.git
