# Phishing Awareness Project

This project is a phishing awareness tool that allows users to register, log in, and check if a URL is suspicious or not. The project is built using **HTML**, **PHP**, **MySQL**, and **JavaScript**.

## Features
- **User Registration**: Users can register using their details (username, email, password).
- **User Login**: Registered users can log in with their credentials.
- **URL Phishing Checker**: After logging in, users can enter a URL, and the tool checks if it is potentially phishing or not.
- **Database**: The project uses a MySQL database to store user data and track login attempts.

## Tech Stack
- **Frontend**: HTML, CSS, JavaScript
- **Backend**: PHP
- **Database**: MySQL (using phpMyAdmin for database management)
- **Hosting**: 000WebHost (or any free PHP hosting provider)

## Screenshots

### 1. Register Page
This is the registration page where users can create a new account by providing their username, email, and password.

![Image](https://github.com/user-attachments/assets/c1d935bf-ce1a-4c45-8d60-df627f7788d6)


### 2. Landing Page
After registration, users can log in using their credentials to access the phishing URL checker.

![Image](https://github.com/user-attachments/assets/0cabc28e-8127-456f-b3e2-8da77bc617d1)

### 3. Results Page
Once logged in, users can input a URL, and the results page will display whether the URL is suspicious or safe.

![Image](https://github.com/user-attachments/assets/374921e2-9ec0-47da-a43b-76716379bc59)

### 4. Database Structure
The project uses a MySQL database to store user information. Below is the structure of the `users` table:

![Image](https://github.com/user-attachments/assets/482af02a-5e77-4d6c-bd73-d39456ce0bea)

| Column   | Data Type        | Description                          |
|----------|------------------|--------------------------------------|
| `id`     | INT(11)          | Primary key, Auto Incremented        |
| `username` | VARCHAR(100)    | Username of the user                 |
| `email`    | VARCHAR(100)    | Email address of the user            |
| `password` | VARCHAR(255)    | Hashed password of the user          |

## Setup Instructions

To run this project locally, follow these steps:

### 1. Install XAMPP
Download and install XAMPP from [Apache Friends](https://www.apachefriends.org/index.html). XAMPP includes Apache (web server) and MySQL (database server), both of which are required to run this project.

### 2. Setup the Project Files
- Download or clone this repository to your local machine.
- Place the project files in the `htdocs` directory of your XAMPP installation. By default, this is located at `C:/xampp/htdocs/`.

### 3. Create a Database
- Open phpMyAdmin by navigating to `http://localhost/phpmyadmin` in your browser.
- Create a new database named `phishing_project`.
- Create a `users` table using the following SQL query:
  ```sql
  CREATE TABLE users (
      id INT(11) AUTO_INCREMENT PRIMARY KEY,
      username VARCHAR(100) NOT NULL,
      email VARCHAR(100) NOT NULL,
      password VARCHAR(255) NOT NULL
  );
