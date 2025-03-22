# Dynamic Login and Register System

This project provides a dynamic login and registration system with OTP-based email verification and an account management feature. Users can create an account, verify their email, log in, and manage account details.

## Features
- User registration with OTP verification via email
- Secure password storage using `password_hash()`
- Login system with session management
- Account details management (add account, update balance, mark as favorite)
- Users can only see their own account details

## Technologies Used
- PHP (Backend)
- MySQL (Database)
- HTML, CSS, JavaScript (Frontend)
- PHPMailer (For sending OTP emails)
- Bootstrap (For styling)

## Installation

### Prerequisites
Make sure you have the following installed:
- XAMPP (or any local server with PHP and MySQL support)
- Composer (to install PHPMailer)
- Git (optional, for version control)

### Setup
1. **Clone the Repository**
   ```sh
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
   ```

2. **Setup Database**
   - Open **phpMyAdmin** and create a database named `bank_system`
   - Import the provided `database.sql` file into phpMyAdmin

3. **Configure Database Connection**
   - Open `db.php`
   - Update the following values:
     ```php
     $conn = new mysqli("localhost", "root", "", "bank_system");
     ```

4. **Install PHPMailer**
   Run the following command to install PHPMailer via Composer:
   ```sh
   composer require phpmailer/phpmailer
   ```

5. **Configure PHPMailer**
   - Open `register.php`
   - Update the following values with your Gmail credentials:
     ```php
     $mail->Username = 'your-email@gmail.com'; // Your email
     $mail->Password = 'your-app-password'; // Use an app password
     ```
   - Enable **Less Secure Apps** in your Google account (or use App Passwords)

6. **Run the Project**
   - Start **XAMPP** (Apache and MySQL)
   - Open your browser and go to:
     ```
     http://localhost/your-repo-name/frontend/register.php
     ```

## Usage

### Register
1. Enter your **username**, **phone number**, and **email**
2. Click "Send OTP"
3. Check your email (Spam folder if not in Inbox)
4. Enter the received OTP and verify
5. Set your **password** and complete the registration

### Login
1. Enter your **email** and **password**
2. Click "Login"
3. If successful, you will be redirected to the dashboard

### Account Details Management
- Add new account details with name and balance
- Increase balance using (+) button
- Mark accounts as favorites

## Future Enhancements
- Implement password reset via email
- Add user profile settings and avatars
- Enhance UI with better styling and animations

## Contributing
Feel free to fork this repository and contribute by submitting pull requests.

## License
This project is open-source under the [MIT License](LICENSE).

