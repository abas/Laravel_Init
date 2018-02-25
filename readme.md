# Laravel Fundamental
## install composer

1. download [composer](https://getcomposer.org/download/1.6.3/composer.phar)
2. copy **composer.phar** ke _/usr/share/bin__
``` bash
sudo cp -f ~/Download/composer.phar /urs/local/bin/
```
3. bikin alias 
``` bash
  nano ~/.bashrc
```
tambahkan line berikut :
```
alias composer="php /usr/local/bin/composer.phar"
```
4. kalo sudah save
```
ctrl+o -> [y] -> enter
ctrl+x -> enter
```
5. sourcing __.bashrc__
```
 source ~/.bashrc
```
6. coba cek composer, ketik command line
``` bash
 composer --version
```
7. done

## Installasi Project Laravel
### **Init project**
> composer create-project larevel/laravel {nama-project} {version}

``` bash
composer create-project larevel/laravel Abas "5.5.*"
cd Abas
code . || subl . || atom . 
```
!open with your text editor

### Configurasi Project
> bikin database baru

open __localhost/phpmyadmin__
buat database baru
ex : `laravel-fundamental`

> konfigurasi koneksi ke **database**

buka file `.env` dan ganti line berikut
```
...
DB_DATABASE={{nama_database}}
DB_USERNAME={{user_host}}
DB_PASSWORD={{password}}
...
```
konfigurasi database fungsinya itu buat menkoneksikan antara project dengan database

> migrasi table database

**membuat table** kas
```
php artisan make:model Kas --migration
```
command tersebut akan menggenerate 2 file yaitu:
`Kas.php` path : App/
`create-kas-table` path : database/migrations
