Marvel Installation Guide


1. Use PHP 8.2

Check your PHP version:

php -v


If you need to install PHP 8.2 (Ubuntu example):

sudo apt update
sudo apt install php8.2 php8.2-xml php8.2-mbstring php8.2-mysql php8.2-curl php8.2-zip

2. Clone the Marvel Project
git clone https://github.com/repo/marvel.git
cd marvel

3. Install Composer Dependencies
composer install

4. Create Environment File
cp .env.example .env
php artisan key:generate

5. Configure Database in .env

Open .env and update these lines:

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=marvel
DB_USERNAME=root
DB_PASSWORD=

6. Run Migrations and Seeders
php artisan migrate --seed

7. Start the Development Server
php artisan serve
