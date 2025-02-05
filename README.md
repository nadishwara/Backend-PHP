<h1>Login and Registration System</h1>
This is a simple login and registration system built using HTML, CSS, JavaScript, PHP, and MySQL. It allows users to register, log in, and access a home page. The system is designed for educational purposes and can be extended for more complex applications.

Features
User Registration:

Users can register by providing their email and password.

Passwords are securely hashed before being stored in the database.

User Login:

Registered users can log in using their email and password.

Passwords are verified using PHP's password_verify function.

Home Page:

After successful login, users are redirected to a home page.

Logout:

Users can log out, which destroys the session and redirects them to the login page.

Technologies Used
Frontend: HTML, CSS, JavaScript

Backend: PHP

Database: MySQL

Server: XAMPP (for local development)

Setup Instructions
1. Prerequisites
Install XAMPP or MAMP.

Ensure Apache and MySQL are running.

2. Database Setup
Open http://localhost/phpmyadmin in your browser.

Create a new database named user_auth.

Run the following SQL query to create the users table:

sql
Copy
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    email VARCHAR(255) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL
);
3. Project Setup
Clone or download this repository.

Place the project folder inside the htdocs directory of your XAMPP/MAMP installation.

Update the database credentials in register.php and login.php if necessary:

php
Copy
$host = "localhost";
$dbUsername = "root"; // Default XAMPP username
$dbPassword = ""; // Default XAMPP password
$dbName = "user_auth";
File Structure
Copy
htdocs/
│
├── registration.html       # Registration form
├── register.php            # Handles registration form submission
├── loginform.html          # Login form
├── login.php               # Handles login form submission
├── Home.html               # Home page after successful login
└── logout.php              # Logs out the user
Usage
1. Registration
Open http://localhost/registration.html in your browser.

Fill in the registration form with your email and password.

Click the "Register" button.

If successful, you will see a message prompting you to log in.

2. Login
Open http://localhost/loginform.html in your browser.

Enter your registered email and password.

Click the "Login" button.

If successful, you will be redirected to Home.html.

3. Logout
Click the "Logout" link on the home page.

You will be redirected to the login page.

Security Considerations
Password Hashing: Passwords are hashed using PHP's password_hash function.

SQL Injection: Use prepared statements or parameterized queries to prevent SQL injection.

Input Validation: Always validate and sanitize user input on both the client and server sides.

HTTPS: Use HTTPS in production to encrypt data transmitted between the client and server.

Future Improvements
Session Management: Implement sessions to track logged-in users.

Password Reset: Add a password reset feature.

Email Verification: Send a verification email to users after registration.

Frontend Styling: Use CSS frameworks like Bootstrap to improve the UI.

Contributing
Contributions are welcome! If you find any issues or have suggestions for improvement, please open an issue or submit a pull request.# Backend-PHP
