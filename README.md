📋 Table of Contents

Overview
Features
Tech Stack
Project Structure
Getting Started
Screenshots
Author


🎯 Overview

App Salón is a complete web solution for managing a barbershop or hair salon. Clients can browse available services, book appointments for specific dates and times, and receive confirmation. Admins can manage the service catalog, view daily appointments and manage their schedule. Built with a custom PHP MVC framework and a MySQL relational database.

✨ Features

ModuleDescription🔐 AuthClient registration, login, and session management📋 ServicesBrowse available services with name, price and duration📅 BookingSelect service + date + available time slot to book👤 Client dashboardView and cancel upcoming appointments🛠️ Admin panelManage services, view daily appointment list📧 Email confirmationAutomated appointment confirmation emails🗓️ AvailabilityTime-slot logic prevents double bookings

🛠️ Tech Stack

LayerTechnologyBackendPHP 8 (custom MVC — no framework)FrontendHTML5, CSS3, JavaScript (ES6+)StylingSASS / SCSS + Gulp build pipelineDatabaseMySQL (normalized relational schema)RoutingCustom PHP RouterDependency managerComposerBuild toolGulp 4

📁 Project Structure

App-Salon-/
├── classes/              # Core: Router, Email, helper classes
├── controllers/          # AppointmentController, AdminController, UserController
├── includes/             # Shared partials: header, footer, DB config
├── models/               # Model classes: Service, Appointment, User
├── public/               # Entry point (index.php) + public assets
│   └── build/            # Compiled CSS, JS
├── src/
│   └── scss/             # SASS source styles
├── views/                # PHP HTML templates
│   ├── auth/             # Register / login pages
│   ├── appointments/     # Booking flow views
│   └── admin/            # Admin panel views
├── appsalon_mvc_php.sql  # ✅ Database schema (ready to import)
├── Router.php            # Application router
├── gulpfile.js           # Gulp tasks
└── composer.json

🚀 Getting Started

Prerequisites

PHP 8.0+
MySQL 8+
Composer
Node.js + npm
Local server: Laragon, XAMPP or similar

Installation

bash# 1. Clone the repository
git clone https://github.com/LuisAOL2003/App-Salon-.git
cd App-Salon-

# 2. Install PHP dependencies
composer install

# 3. Install Node.js deps and compile SASS
npm install && npx gulp
Database Setup
bash# Create database and import the included schema:
mysql -u root -p -e "CREATE DATABASE appsalon_db;"
mysql -u root -p appsalon_db < appsalon_mvc_php.sql
Configure Database
Edit your database config (in includes/):
phpdefine('DB_HOST', 'localhost');
define('DB_USER', 'root');
define('DB_PASS', '');
define('DB_NAME', 'appsalon_db');
Run
Point your local server to the project and visit:
http://appsalon.test or http://localhost/App-Salon-/public

👤 Author
Luis Ojeda — Full Stack Developer

🌐 portafolio-luis-ojeda.vercel.app
💼 LinkedIn
🐙 GitHub @LuisAOL2003
