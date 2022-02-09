

## Creación de un CMS con Laravel

Siguiendo [este](https://webmobtuts.com/backend-development/building-a-simple-cms-with-laravel-breeze/) tutorial, dentro de la página de [webmobtuts](https://webmobtuts.com/).

Creamos un directorio dentro de nuestra carpeta de laragon/www mediante el siguiente comando:

1. ```
   composer create-project laravel/laravel lara-breeze-cms --prefer-dist
   ```

Instalamos el paquete de laravel breeze:

1. ```
   composer require laravel/breeze
   ```

2. ```
   php artisan breeze:install
   ```

Compilamos los activos que viene de base con laravel breeze usando npm:

3. ```
   npm install
   npm run dev
   ```

Creamos una BBDD llamada en mi caso 'lara_breeze_cms' y actualizamos el archivo env. con los datos pertienentes del nombre de la BBDD, el usuario empleado y su contraseña. Finalmente, migramos la BBDD:

4. ```
   php artisan migrate
   ```

Creamos dos módulos para el cms de categorias y artículos:

5. ```
   php artisan make:model Category -m
   php artisan make:model Post -m
   ```

El siguiente paso e poblar y actualizar una serie de directorios dentro de los directorios existentes de migrations, Models, Resources/views/admin, app/Http/Controllers/Admin. 

Después de continuar el tutorial añadiendo el código a cada fichero y corigiendo las líneas de código, la página resultado de todos los pasos da error. Aparece una tabla con los contenidos, pero muestra la siguiente página:

![image](https://user-images.githubusercontent.com/91055754/152993217-8b12e2d2-10f7-4dc6-851d-344b5d3b010a.png)

Al entrar a través del localhost/lara-breeze-cms/public/dashboard deja entrar a la pantalla de Login, en mi caso, me resgistré y luego entré. En el navegador, salían varias de las páginas:

![FireShot Capture 038 - Laravel - localhost](https://user-images.githubusercontent.com/91055754/152993486-2969728f-a0e9-4043-ac32-4cb817acbb66.png)
![FireShot Capture 042 - lara_breeze_cms - localhost](https://user-images.githubusercontent.com/91055754/152993652-155cc620-1392-42cb-89ba-f4f022113c51.png)
![FireShot Capture 043 - lara_breeze_cms - localhost](https://user-images.githubusercontent.com/91055754/152993711-9ed9f00a-9797-44ab-b73a-316701fdb71b.png)

<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>
