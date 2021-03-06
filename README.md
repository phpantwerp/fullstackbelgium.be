# fullstackbelgium.be

<a href="https://github.com/fullstackbelgium/fullstackbelgium.be?query=workflow%3ATests">
    <img src="https://github.com/fullstackbelgium/fullstackbelgium.be/workflows/Tests/badge.svg" alt="Tests">
</a>
<a href="https://github.styleci.io/repos/129402152">
    <img src="https://github.styleci.io/repos/129402152/shield?style=flat" alt="Code Style">
</a>

The source code of the Full Stack Belgium website.

Visit it at [https://fullstackbelgium.be](https://fullstackbelgium.be)

## Requirements

The following tools are required in order to start the installation.

- PHP >=8.0
- [Composer](https://getcomposer.org/download/)
- [NPM](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
- [A valid Laravel Nova license](https://nova.laravel.com)

## Installation

1. Clone this repository locally with `git clone git@github.com:fullstackbelgium/fullstackbelgium.be.git fullstackbelgium.be`
2. Setup a local database called `laravel`
3. Copy the `.env.example` file to `.env` and fill in the database credentials
4. Add [the `auth.json` file from below](#nova-license) to the root of the project
5. Install the PHP dependencies with `composer install` 
6. Generate a new app key with `php artisan key:generate`
7. Prepare the database by running `php artisan migrate --seed` 
8. Install and compile the front-end dependencies with `npm install && npm run dev`
9. Serve the website locally by running `php artisan serve`

You can now visit the app in your browser by visiting [http://127.0.0.1:8000](http://127.0.0.1:8000). You can login into the back-end at [http://127.0.0.1:8000/nova](http://127.0.0.1:8000/nova) with **`john@example.com`** & **`secret`**.

### Nova License

Your `auth.json` file at the root of the project should contain your Nova credentials:

```json
{
    "http-basic": {
        "nova.laravel.com": {
            "username": "Your Nova email address",
            "password": "Your Nova license key"
        }
    }
}
```

## Commands

Command | Description
--- | ---
**`vendor/bin/phpunit`** | Run the tests
`php artisan migrate:fresh --seed` | Reset the database
`npm run watch` | Watch for changes in CSS and JS files
