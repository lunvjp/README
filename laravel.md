## YouTalk API Server

# Development
If you guys get some issues, Follow some solution here.
- https://itsolutionstuff.com/post/laravel-5-clear-cache-from-route-view-config-and-all-cache-data-from-applicationexample.html

## Steps Set up
* Create new `.env` file by Copy texts from `.env.example` file
* Set up Database config inside new `.env` file.
* Run `php artisan key:generate`
* Run `php artisan migrate` to create Database Tables
> Run `php artisan passport:keys` to deploy Passport to your production servers for the first time (*Pass this step for now*)
* Set up Passport stuff.
    - Create `Encryption keys generated`
    - Create `Personal access client`
    - Create `Password grant client`
    ```
    php artisan passport:install
    ```
- Upload 2 Key files in `storage` folder to server with the same folder.
- Run `composer install && composer update`
- Run `php artisan migrate`
    - If you get some errors, Let's use this magic `composer dump-autoload`

## Database Set up.
- Create new Migration/Table/Model with `php artisan make:model {Your_Model_Name} --migration --controller --resource`
- Create new Controller inside `API` folder with `php artisan make:controller API/{Your_Model_Name}Controller --api`

## Production

### Client Key
- https://laravel.com/docs/5.8/passport#client-credentials-grant-tokens

### Optimization
[Docs here](https://laravel.com/docs/5.8/deployment)
##### Autoloader Optimization
- Run `composer dump-autoload`
- Run `composer install --optimize-autoloader --no-dev`
- Run `php artisan config:cache`

##### Optimizing Configuration Loading
- `php artisan config:cache`

##### Optimizing Route Loading
- `php artisan route:cache`

## Readme Template
- https://raw.githubusercontent.com/oblador/react-native-vector-icons/master/README.md

## Migrations
- MIGRATE: `php artisan migrate`
- MIGRATE (Refresh): `php artisan migrate:refresh`
- CREATE: `php artisan make:migration create_users_table`
- CREATE WITH TABLE: `php artisan make:migration create_users_table --create=users`
+ `php artisan make:migration add_votes_to_users_table --table=users`
+ `php artisan make:migration update_words_table --table=words`

- WITH MODEL: `php artisan make:model WordsTopics --migration`

* `php artisan make:model Todo -mcr`
-m, --migration Create a new migration file for the model.
-c, --controller Create a new controller for the model.
-r, --resource Indicates if the generated controller should be a resource controller

## Query with Relationship
- https://laravel-news.com/eloquent-eager-loading - AWESOME!

## Reset from master without any conflicts.
- https://ibb.co/fFmypmQ
https://stackoverflow.com/questions/9589814/how-do-i-force-git-pull-to-overwrite-everything-on-every-pull/9589927

## Set up Phpmyadmin in Production.
- `sudo ln -s /usr/share/phpmyadmin /var/www/public_html`
- `sudo ln -s /usr/share/phpmyadmin /var/www/public_html/public`

## Split websites.
- https://textfilesplitter.com/

FILE SYSTEM.
- `https://laravel.com/docs/5.8/filesystem#the-local-driver`