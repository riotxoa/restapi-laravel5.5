# restapi-laravel5.5

## `Step1` Release

Simple Rest API using **Laravel 5.5**.

This first pre-release (`Step1`) supports **basic CRUD** for `articles` database table (`title`, `body`):

- **Create** Article: `[POST] http://localhost:8000/api/articles/`
- **Retrieve all** Articles: `[GET] http://localhost:8000/api/articles/`
- **Retrieve single** Article: `[GET] http://localhost:8000/api/articles/{id}`
- **Update** an Article: `[PUT] http://localhost:8000/api/articles/{id}`
- **Delete** an Article: `[DELETE] http://localhost:8000/api/articles/{id}`

### For Developers

You can find a full tutorial explaining the code and how to build a Rest API using **Laravel 5.5** in these pages:

- **Basque**: https://www.netireki.com/laravel-rest-api-sortu-step-1/
- **Spanish**: https://www.netireki.com/crear-rest-api-con-laravel-step-1/

## `Step2`  Release

This second release (`Step2`) supports **API Authentication** for `Step1` release's operations**:

- **Register** User: `[POST] http://localhost:8080/api/register`
- **Login** User: `[POST] http://localhost:8000/api/login`
- **Logout** User: `[POST] http://localhost:8000/api/logout`

### For Developers

You can find a full tutorial explaining the code and how to build API Authentication using **Laravel 5.5** in these pages:

- **Basque**: https://www.netireki.com/laravel-rest-api-sortu-step-2/
- **Spanish**: https://www.netireki.com/crear-rest-api-con-laravel-step-2/

# Installation
Download `Step1` tagged version from this reposityory using the `git clone https://github.com/riotxoa/restapi-laravel5.5.git` command or downloading and uncompressing the ZIP file.

Once cloned or uncompressed, go ahead and install dependencies:

```
composer install
```

## Configuring database
You must edit or create `.env` file in project's root path (use `.env.example` as start point) and configure database connection parameters with your database's values:
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravelapi
DB_USERNAME=root
DB_PASSWORD=secret
```

Migrate data model:

```
$ php artisan migrate
```

## Database seeding
Database seeding is the process of filling up our database with dummy data that we can use to test it.

Run the seed command for Articles:
```
$ php artisan db:seed --class=ArticlesTableSeeder
```

And for Users:
```
$ php artisan db:seed --class=UsersTableSeeder
```

# Running the aplication
```
$ php artisan serve
```

Enjoy! =)
