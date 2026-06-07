# student_manage
# Student Management System - Authentication Module

## Overview

The Student Management System Authentication Module is a web-based application built using Django and PostgreSQL. It provides a secure authentication system that allows users to register, verify their accounts through Email OTP or Mobile OTP, log in, manage their profiles, and reset their passwords.

The project follows Django's MVT (Model-View-Template) architecture and uses server-rendered HTML templates for user interaction.

---

## Features

### User Registration

* Create a new account
* Register using email and mobile number
* Password validation and confirmation

### Email & Mobile Verification

* Email OTP verification
* Mobile OTP verification
* OTP expiration handling
* Resend OTP functionality

### Authentication

* Secure Login
* Logout
* Session-based Authentication

### Password Management

* Forgot Password
* OTP Verification
* Reset Password
* Password Change Success Notification

### User Profile

* View Profile
* Update Profile Information

### Security Features

* Password Hashing
* CSRF Protection
* Session Management
* Form Validation

---

## Technology Stack

| Technology             | Purpose                |
| ---------------------- | ---------------------- |
| Python                 | Programming Language   |
| Django                 | Web Framework          |
| PostgreSQL             | Database               |
| HTML5                  | Frontend Structure     |
| CSS3                   | Styling                |
| Bootstrap/Tailwind CSS | Responsive Design      |
| JavaScript             | Client-side Validation |
| SMTP                   | Email OTP Verification |

---

## Project Structure

```bash
student_management_system/
│
├── accounts/
│   ├── migrations/
│   ├── templates/accounts/
│   ├── models.py
│   ├── forms.py
│   ├── views.py
│   ├── urls.py
│   └── admin.py
│
├── dashboard/
│   ├── templates/dashboard/
│   ├── views.py
│   └── urls.py
│
├── static/
│   ├── css/
│   ├── js/
│   └── images/
│
├── templates/
│   ├── base.html
│   └── includes/
│
├── media/
│
├── student_management/
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
│
├── manage.py
├── requirements.txt
└── README.md
```

---

## Database Models

### User Model

Stores authentication and user information.

Fields:

* Full Name
* Email Address
* Mobile Number
* Password
* Email Verification Status
* Mobile Verification Status
* Created Date
* Updated Date

### OTP Verification Model

Stores OTP details for account verification and password reset.

Fields:

* User
* OTP
* OTP Type
* Verification Status
* Expiration Time
* Created Date

---

## Application Workflow

```text
Landing Page
      |
      v
Register Account
      |
      v
Email / Mobile OTP Verification
      |
      v
Verification Successful
      |
      v
Account Created Successfully
      |
      v
Login
      |
      v
Dashboard
      |
      +----------------+
      |                |
      v                v
Profile          Forgot Password
      |                |
      |                v
      |         Verify OTP
      |                |
      |                v
      |        Reset Password
      |                |
      |                v
      +---- Password Changed Successfully
```

---

## Available Pages

| Page                     | URL                        |
| ------------------------ | -------------------------- |
| Home                     | /                          |
| Register                 | /register/                 |
| Email Verification       | /verify-email/             |
| Mobile Verification      | /verify-mobile/            |
| Login                    | /login/                    |
| Logout                   | /logout/                   |
| Dashboard                | /dashboard/                |
| Profile                  | /profile/                  |
| Forgot Password          | /forgot-password/          |
| Verify OTP               | /verify-reset-otp/         |
| Reset Password           | /reset-password/           |
| Verification Success     | /verification-success/     |
| Account Created          | /account-created/          |
| Password Changed Success | /password-changed-success/ |

---

## Installation Guide

### Clone Repository

```bash
git clone https://github.com/your-username/student-management-system.git
```

### Navigate to Project Directory

```bash
cd student-management-system
```

### Create Virtual Environment

```bash
python -m venv env
```

### Activate Virtual Environment

Windows

```bash
env\Scripts\activate
```

Linux / Mac

```bash
source env/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Configure PostgreSQL Database

Update database settings inside `settings.py`

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'student_db',
        'USER': 'postgres',
        'PASSWORD': 'your_password',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

### Apply Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### Create Superuser

```bash
python manage.py createsuperuser
```

### Run Development Server

```bash
python manage.py runserver
```

Open browser:

```text
http://127.0.0.1:8000/
```

---

## Future Enhancements

* Student Management Module
* Attendance Management
* Parent Portal
* Course Management
* Fee Management
* Notification System
* Email Notifications
* SMS Notifications
* Role-Based Access Control (RBAC)
* Dashboard Analytics
* Docker Deployment
* Cloud Deployment

---

## Learning Outcomes

This project demonstrates:

* Django MVT Architecture
* Django Authentication System
* Custom User Models
* Form Handling
* Session Management
* PostgreSQL Integration
* OTP Verification Workflow
* Frontend Template Development
* User Authentication & Authorization
* Git & GitHub Workflow

---

## Author

**Kishor Shirke**

Python Developer | Django Developer | PostgreSQL | Web Application Development

---

## License

This project is licensed under the MIT License.

Feel free to use, modify, and distribute this project for learning and educational purposes.
