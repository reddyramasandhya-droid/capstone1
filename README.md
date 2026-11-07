<img width="802" height="551" alt="Image" src="https://github.com/user-attachments/assets/c47cbc71-3402-4397-b623-ed9869e7501f" />
<img width="712" height="290" alt="Image" src="https://github.com/user-attachments/assets/2e609949-05f2-427f-9f2e-a7dee341bb6e" />
<img width="1143" height="490" alt="Image" src="https://github.com/user-attachments/assets/fe851ceb-a100-430f-b04e-a7ec5668fd5e" />
<img width="1913" height="1055" alt="Image" src="https://github.com/user-attachments/assets/ac87cbe5-a5fd-4dd9-b3c2-41e2acc6ff11" />
# Employee Database Management System

A Django web application for managing employee records, built as **Capstone Project-1**. Users can create an account, log in, browse all employees, view individual profiles, and add new employees through a validated form.

![Python](https://img.shields.io/badge/Python-3-blue)
![Django](https://img.shields.io/badge/Django-6.1-green)
![Database](https://img.shields.io/badge/Database-SQLite-lightgrey)

🔗 **Live Demo:** https://reddyramasandhya.pythonanywhere.com/

---

## About the Project

I built this project as part of my BTech in AIML at Presidency University, Bangalore. The goal was to understand how a real web application fits together: database models, forms, authentication, URL routing, templates, and deployment. It follows Django's MVT (Model-View-Template) pattern.

## Features

- User registration and login using Django's built-in authentication
- Protected home page that lists all employees (login required)
- Employee detail page
- Add-employee form with server-side validation
- Success confirmation page after saving a record
- Logout and Django admin panel for managing data

## Screenshots

### Employee List
![Employee list](screenshots/home.png)

### Add Employee
![Add employee form](screenshots/add.png)

### Login
![Login page](screenshots/login.png)

### Register
![Register page](screenshots/register.png)

## Tech Stack

| Layer | Technology |
|-------|------------|
| Language | Python 3 |
| Framework | Django 6.1 |
| Database | SQLite |
| Frontend | HTML, Bootstrap (Django templates) |
| Tools | Git, GitHub, VS Code, PythonAnywhere |

## Data Model

**Employee**

| Field | Type | Description |
|-------|------|-------------|
| `firstname` | CharField | First name |
| `last_name` | CharField | Last name |
| `photo` | CharField | Photo path or URL stored as text |
| `designation` | CharField | Job title |
| `email_address` | CharField | Email |
| `phone_number` | CharField | Phone number |

## URL Routes

| URL | View | Description |
|-----|------|-------------|
| `/` | `home` | Lists all employees (login required) |
| `/<id>/` | `detail` | Shows one employee's details |
| `/add/` | `add_employee` | Form to add a new employee |
| `/success/` | `success_view` | Confirmation after saving |
| `/register/` | `register` | Create a new account |
| `/login/` | `LoginView` | Log in |
| `/logout/` | `LogoutView` | Log out |
| `/admin/` | Django admin | Admin panel |

## Project Structure

```
capstone1/
├── app/
│   ├── templates/app/    # home, login, register, success, detail and add pages
│   ├── models.py         # Employee model
│   ├── forms.py          # EmployeeForm (ModelForm)
│   └── views.py          # Application logic
├── project10/
│   ├── settings.py       # Project configuration
│   └── urls.py           # URL routing
├── screenshots/          # Images used in this README
├── manage.py
├── requirements.txt
└── README.md
```

## Getting Started

### Prerequisites

- Python 3 and pip
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/reddyramasandhya-droid/capstone1.git
   cd capstone1
   ```

2. **Create and activate a virtual environment**
   ```bash
   python -m venv env
   source env/bin/activate      # Windows: env\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up the database**
   ```bash
   python manage.py migrate
   ```

5. **(Optional) Create an admin user**
   ```bash
   python manage.py createsuperuser
   ```

6. **Run the development server**
   ```bash
   python manage.py runserver
   ```

7. Open **http://127.0.0.1:8000/**, register an account, and log in.

## What I Learned

- Designing database models and generating migrations with the Django ORM
- Building forms with `ModelForm` and validating user input
- Implementing authentication with `UserCreationForm`, `LoginView`, `LogoutView` and `@login_required`
- Routing URLs to views and passing data to templates
- Managing dependencies with a virtual environment and `requirements.txt`
- Using Git and GitHub, including `.gitignore` to keep the repo clean
- Deploying a Django project on PythonAnywhere

## Future Improvements

- Edit and delete functionality to complete full CRUD
- Search and filter employees by name or designation
- Photo upload with `ImageField` instead of a text path
- Login protection on all employee pages
- Pagination for large employee lists
- Unit tests for views and forms
- Consistent styling across the login, register and add pages

## Author

**Somula Rama Sandhya**
BTech AIML, Presidency University, Bangalore (2024 to 2028)

GitHub: [@reddyramasandhya-droid](https://github.com/reddyramasandhya-droid)

---

If you found this project useful, feel free to star the repository.
