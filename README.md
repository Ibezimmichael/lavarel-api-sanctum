Laravel 8.0 Simple API Project for Products
This is a Laravel 8.0 API project that provides endpoints for managing products. It includes protected routes for logout, store, update, and delete operations, as well as public routes for register, login, and index operations.

Requirements
PHP 7.4 or higher
Composer
Laravel 8.0 or higher
Database (e.g., MySQL, PostgreSQL)
Installation
Clone the repository:

git clone https://github.com/your-username/laravel-api-project.git
Navigate to the project directory:

cd laravel-api-project
Install the dependencies:

composer install
Copy the .env.example file to .env:

cp .env.example .env
Generate an application key:

php artisan key:generate
Update the .env file with your database credentials.

Run the database migrations:


php artisan migrate
(Optional) Seed the database with sample data:

php artisan db:seed
Start the development server:

php artisan serve


Usage
Public Routes
Register
Endpoint: POST /api/register
Parameters:
name: The name of the user.
email: The email of the user.
password: The password of the user.
password_confirmation: Confirm the password.
Response: Returns the newly registered user and an access token.
Login
Endpoint: POST /api/login
Parameters:
email: The email of the user.
password: The password of the user.
Response: Returns the authenticated user and an access token.
Index
Endpoint: GET /api/products
Response: Returns a list of all products.
Protected Routes
The protected routes require an access token obtained through the login or register endpoints. The access token should be sent in the Authorization header as a Bearer token.

Logout
Endpoint: POST /api/logout
Response: Returns a message indicating successful logout.
Store
Endpoint: POST /api/products
Parameters:
name: The name of the product.
description: The description of the product.
price: The price of the product.
Response: Returns the created product.
Update
Endpoint: PUT /api/products/{id}
Parameters:
name (optional): The updated name of the product.
description (optional): The updated description of the product.
price (optional): The updated price of the product.
Response: Returns the updated product.
Delete
Endpoint: DELETE /api/products/{id}
Response: Returns a message indicating successful deletion.
Contributing
Contributions are welcome! If you have any suggestions, bug reports, or feature requests, please open an issue or submit a pull request.

License
This project is licensed under the MIT License.

Feel free to modify and customize this README to fit your project's specific details and requirements.





