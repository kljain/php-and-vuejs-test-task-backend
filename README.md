# test Web Application with Laravel and Vue.js

## Overview

This is a simple web application with a PHP Laravel backend and a Vue.js frontend. The application includes basic login and registration functionalities with form validation and error handling.

we used Laravel v11.21.0 (PHP v8.2.4) 

## Backend Setup

1. **Install Laravel**

    composer create-project --prefer-dist laravel/laravel testProjectBackend

2. **Database Migration**

    Create and run the migration for the `users` table:

    php artisan make:model User -m
    php artisan migrate

3. **AuthController**

    Implements methods for user registration and login with validation.

4. **API Routes**

    Define routes for registration and login in `routes/api.php`.


## Frontend Setup

1. **Install Vue.js**

    Create a Vue.js project using Vite:
    npm create vite@latest frontend --template vue

2. **Install Axios**

    For making HTTP requests:
    npm install axios

3. **Create Components**

    - `Login.vue`: Handles user login.
    - `Register.vue`: Handles user registration.

4. **Main Vue Instance**
    Added the plugin for axios and use into App component
    Configures Axios and mounts the main `App` component.

## Running the Application

1. **Backend**

    Navigate to the `testProjectBackend` directory and run:

    php artisan serve

    The Laravel server will run on `http://localhost:8000`.

2. **Frontend**

    Navigate to the `frontend` directory and run:

    npm install
    npm run dev

    we need node -v for this greater the 16 
    in our project we used v20.17.0 for this project

    for update the node version use following commands 
    nvm install --lts
    nvm use --lts

## Database

    we used mysql database for this application
    migrated the default table of the laravel into the databse 
    Need to configure the Database details into the laravel env file 
    
    DB_HOST
    DB_DATABASE
    DB_USERNAME
    DB_PASSWORD