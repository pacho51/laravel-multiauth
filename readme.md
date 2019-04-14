## Laravel Application with Multiple Authentication
Laravel application with admin guard. You can use this application for your projects.

## Getting this app up and running

- Make sure you already have [xampp](https://www.apachefriends.org/index.html) installed (easy to use).

- [Clone](https://github.com/SagarMaheshwary/laravel-multiauth.git) this repository to your local machine or just download the zip from the above green button.

- Install [Composer](https://getcomposer.org/download) first, then run this command in your command-line (you should be inside your project directory). 
```bash
  composer install
```

- Rename .env.example to .env and add your database.

- Generate application key.

```bash
    php artisan key:generate
```

- Create tables.

```bash
    php artisan migrate
```

- Start the development server.

```bash
    php artisan serve
```

- Create a default admin.

```bash
    php artisan db:seed
```

#### Default Admin Credentials.
- Email: admin@admin.com
- password: password

## Usage
- Flash Messages: use **status** key for success messages and **error** key for error messages.
- Guards: **web** (default) and **admin** (custom).
- Auth middleware for admin guard: **auth:admin** for authenticated users using **admin** guard.
- Guest middleware for admin guard: **guest:admin** for unauthenticated users using **admin** guard.
- Don't use **@auth** or **@guest** directives for default guard, use **Auth::guard('web')->check()** with **@if** instead.
- Admin and Default routes are seperated and all the admin routes are prefixed by **admin**.