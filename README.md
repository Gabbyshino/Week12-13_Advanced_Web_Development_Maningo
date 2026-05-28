# Week12-13_Advanced_Web_Development_Maningo

# User Profile System with Pagination

---

## Features
- Add/Edit/Delete users with profile pictures
- 5 users per page pagination
- Search by name or email
- Image validation (JPEG, PNG, GIF, WEBP, max 2MB)

---

## Technologies
- PHP 8.2+ / CodeIgniter 4 / MySQL / Bootstrap 5

---

## Installation

```
bash
git clone https://github.com/YOUR_USERNAME/final-webdev.git
cd final-webdev
composer install

```

## Create database finalwebdev_db

```
CI_ENVIRONMENT = development
database.default.database = finalwebdev_db
database.default.username = root
database.default.password = 
```

```
mkdir public/uploads
php spark serve
```

### Open: http://localhost:8080/users

## Database
```
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(100) NOT NULL,
    email VARCHAR(255) UNIQUE NOT NULL,
    avatar VARCHAR(255),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

## Project Folder Structure
```
final-webdev/
├── app/
│   ├── Config/
│   │   ├── Routes.php
│   │   └── Pager.php
│   ├── Controllers/
│   │   └── UserController.php
│   ├── Models/
│   │   └── UserModel.php
│   └── Views/
│       ├── layout.php
│       ├── user_list.php
│       └── user_form.php
├── public/
│   └── uploads/
├── writable/
├── .env
└── spark
```
