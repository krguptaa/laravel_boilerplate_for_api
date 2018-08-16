## Inspired by Viral Solani

It is same as the below repo but some change we made in this git as per general requirement

`https://github.com/viralsolani/laravel-api-boilerplate-jwt.git`

## Laravel API Boilerplate (JWT Edition) for Laravel 5.6


# Getting started

## Introduction

Laravel API Boilerplate is a "starter kit" you can use to build your first API in seconds. As you can easily imagine, it is built on top of the awesome Laravel Framework. This version is built on Laravel 5.6!

## Installation

Please check the official laravel installation guide for server requirements before you start. [Official Documentation](https://laravel.com/docs/5.6/installation#installation)


Clone the repository

    git clone https://github.com/gupta-kamlesh-r/laravel_boilerplate_for_api.git

Switch to the repo folder

    cd laravel_boilerplate_for_api

Install all the dependencies using composer

    composer install

Copy the example env file and make the required configuration changes in the .env file

    cp .env.example .env
    
(**Set the database connection in .env file**)

Generate a new application key

    php artisan key:generate

Generate a new JWT authentication secret key

    php artisan jwt:generate

Run the database migrations (**Set the database connection in .env before migrating**)

    php artisan migrate

Run the Seeder 

    php artisan db:seed

Start the local development server

    php artisan serve

You can now access the server at http://localhost:8000

**TL;DR command list**

    git clone https://github.com/gupta-kamlesh-r/laravel_boilerplate_for_api.git
    cd laravel-api-boilerplate-jwt
    composer install
    cp .env.example .env
    php artisan key:generate
    php artisan jwt:generate

**Make sure you set the correct database connection information before running the migrations** [Environment variables](#environment-variables)

    php artisan migrate
    php artisan db:seed
    php artisan serve

## Environment variables

- `.env` - Environment variables can be set in this file


***Note*** : You can quickly set the database information and other variables in this file and have the application fully working.

# Authentication

This applications uses JSON Web Token (JWT) to handle authentication. The token is passed with each request using the `Authorization` header with `Token` scheme. The JWT authentication middleware handles the validation and authentication of the token. Please check the following sources to learn more about JWT.

- https://jwt.io/introduction/
- https://self-issued.info/docs/draft-ietf-oauth-json-web-token.html

## Simple Rest API Example 

# For login

    POST http://localhost:8000/api/v1/login 

**Request Parameter**
    email - admin@admin.com
    password - Admin@123

**Response**
    {
        "message": "Login Successfull.",
        "token": "adHRwOi8vd3d3LmdyYXZhdGFyLmNvbS9hdmF0YXIvNjRlMWI4ZDM0ZjQyNWQxOWUxZWUyZWE3MjM2ZDMwMjguanBnP3M9ODAmZD1tbSZyPWciLCJjb25maXJtZWQiOjEsInJlZ2lzdGVyZWRfYXQiOiIyMDE4LTA4LTE2VDA1OjU4OjM4KzAwOjAwIiwibGFzdF91cGRhdGVkX2F0IjoiMjAxOC0wOC0xNlQwNTo1ODozOCswMDowMCJ9.Cd6GA8_yenGW7y74auMxk3gPN6yO8EMA3qMVmkhghc0"
    }

## Issues

If you come across any issues please report them [here](https://github.com/gupta-kamlesh-r/laravel_boilerplate_for_api/issues).

## Contributing
Feel free to create any pull requests for the project. For propsing any new changes or features you want to add to the project, you can send us an email at webworldgk@gmail.com