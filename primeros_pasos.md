# PRIMEROS PASOS
bueno resulta que decidi probar otras distribuciones estoy usando manjaro minimal y tengo que instalar todo desde 0 asi que aca van los pasos

## PRIMERAS INSTALACIONES
instalamos php y composer tambien seria bueno instalar gedit es un editor de texto muy divertido de usar diria yo que es mas divertido que usar el nano o el vim 

Comandos para instalar:
sudo pacman -S php
sudo pacman -S composer
sudo pacman -S gedit

### CONFIGURACION DE php.ini
para ello usamos nuestro nuevo y divertido editor de texto yo usare mysql asi que busco *extension=pdo_mysql* y le quito el punto y coma delantero para habilitarlo si tu quieres usar otro y no el que yo estoy usando haces lo mismo 

Configuracion de php:
sudo gedit /etc/php/php.ini

## INSTALAR LARAVEL
ahora instalamos el laravel de esta manera:

composer global require laravel/installer

una vez este instalado

/home/chon/.config/composer/vendor/bin/laravel new web-php-laravel

### CONFIGURACION DEL PATH
bueno esto lo ponemos en nuestro .zshrc y .bashrc o si tu usas solo uno lo pones en uno de ellos yo uso los 2 porque soy genial tambien recuerda cambiar chon por tu usuario...
bueno cuando copiemos tenemos que descomentar... quitando el # que esta adelante de la linea de codigo

    -> *# export PATH="$HOME/.config/composer/vendor/bin:$PATH"* <-
    -> *# export PATH="$PATH:$HOME/.config/composer/vendor/bin"* <-
    -> *# export PATH="$PATH:/home/chon/.config/composer/vendor/bin"* <-

## Web_PHP_Laravel
tenemos que ir a Web_PHP_Laravel:

    -> *cd Web_PHP_Laravel* <-

Bueno con laravel 9 parece que las osas vienen preparadas por ejemplo APP_KEY ya viene preparada
pero para estar seguros en consola ponemos los siguientes comandos:

    -> *php artisan config:cache* <-
    -> *php artisan config:clear* <-
    -> *php artisan cache:clear* <-

Con este comando corremos la aplicacion
    -> *php artisan serve* <-

    npm i

    npm run dev

    Recordar:
    Configurar el .env , poner el usuario y el nombre de tu base de datos que estes usando

    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=nombre_de_DB
    DB_USERNAME=nombre_de_USER
    DB_PASSWORD=contraseña_de_BD