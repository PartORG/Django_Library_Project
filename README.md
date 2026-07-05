# Django_Library_Project

A simple example of Django Framework for managing books and user authentication.

[![Python](https://img.shields.io/badge/python-3.10-blue.svg)] [![License](https://img.shields.io/badge/license-MIT-green.svg)] [![Package Manager](https://img.shields.io/badge/package-manager-pip-yellow.svg)] [![Framework](https://img.shields.io/badge/framework-Django-brightgreen.svg)] [![Testing](https://img.shields.io/badge/testing-None-red.svg)]

## Introduction

Django_Library_Project is a simple example of the Django Framework. It includes a catalog application for managing books and their instances, as well as user authentication features. The project uses SQLite as its database.

The primary workflow involves creating, updating, and deleting book records, managing user profiles, and handling user authentication. This project serves as an educational resource for understanding Django's architecture and best practices.

## Table of Contents

1. [Features](#features)
2. [How It Works](#how-it-works)
3. [Technology Stack](#technology-stack)
4. [Requirements](#requirements)
5. [Installation](#installation)
6. [Configuration](#configuration)
7. [Quick Start](#quick-start)
8. [Usage](#usage)
9. [Project Structure](#project-structure)
10. [Development](#development)
11. [Testing](#testing)
12. [Limitations](#limitations)
13. [License](#license)

## Features

### Book Management
- **What it does:** Allows users to add, update, and delete book records.
- **Why it exists:** To provide a centralized system for managing books in a library.
- **Why it is useful:** Facilitates easy access and management of book inventory.

### User Authentication
- **What it does:** Manages user registration, login, and profile management.
- **Why it exists:** Ensures secure access to the catalog application.
- **Why it is useful:** Protects sensitive data and provides a personalized experience for users.

## How It Works

Django_Library_Project follows a typical Django project structure. The main components include:

- `catalog`: Contains the logic for managing books and their instances.
- `library`: Contains the core settings, URLs, and WSGI configuration for the project.

The application uses Django's ORM to interact with the SQLite database. Views handle user requests, templates render HTML, and forms manage data input.

## Technology Stack

| Technology | Purpose |
|------------|---------|
| Python 3.10 | The programming language used for development. |
| Django 4.x | The web framework used for building the application. |
| SQLite | The database management system used to store book records. |

## Requirements

- Python 3.10
- Django 4.x
- SQLite (pre-installed with Django)

## Installation

To install and run Django_Library_Project, follow these steps:

```bash
# Clone the repository
git clone https://github.com/PartORG/Django_Library_Project.git

# Navigate to the project directory
cd Django_Library_Project

# Create a virtual environment (optional but recommended)
python -m venv venv

# Activate the virtual environment
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

# Install dependencies
pip install -r requirements.txt

# Run migrations
python manage.py migrate

# Start the development server
python manage.py runserver
```

## Configuration

The project uses environment variables for configuration. The following variables are observed:

- `SECRET_KEY`: A secret key used by Django for cryptographic signing.
- `DEBUG`: A boolean indicating whether debug mode is enabled.

These variables can be set in a `.env` file or directly in the operating system's environment.

## Quick Start

To quickly start using Django_Library_Project, follow these steps:

1. **Create a new book:**
    ```bash
    python manage.py createsuperuser
    ```

2. **Access the admin panel:**
    - Open your web browser and navigate to `http://127.0.0.1:8000/admin/`.
    - Log in using the superuser credentials.

3. **Add a new book instance:**
    - Navigate to `Books > Books` and add a new book.
    - Add instances of the book as needed.

## Usage

To interact with Django_Library_Project, use the following commands:

- **Run migrations:**
    ```bash
    python manage.py migrate
    ```

- **Start the development server:**
    ```bash
    python manage.py runserver
    ```

- **Create a superuser:**
    ```bash
    python manage.py createsuperuser
    ```

## Project Structure

```
Django_Library_Project/
├── catalog/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── migrations/
│   │   ├── 0001_initial.py
│   │   ├── 0002_bookinstance_borrower.py
│   │   └── __init__.py
│   ├── models.py
│   ├── templates/
│   │   └── catalog/
│   │       ├── book_detail.html
│   │       ├── book_form.html
│   │       ├── index.html
│   │       ├── my_view.html
│   │       └── profile.html
│   ├── tests.py
│   ├── urls.py
│   └── views.py
├── library/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── manage.py
└── requirements.txt
```

## Development

The development workflow involves:

1. **Creating a new feature branch:**
    ```bash
    git checkout -b feature/my-feature
    ```

2. **Making changes and committing them:**
    ```bash
    git add .
    git commit -m "Add my feature"
    ```

3. **Pushing the changes to the remote repository:**
    ```bash
    git push origin feature/my-feature
    ```

4. **Creating a pull request (PR) on GitHub.**

## Testing

This project does not include tests.

## Limitations

- The project uses SQLite, which may not be suitable for production environments.
- No automated testing is provided.

## License

Django_Library_Project is licensed under the MIT License.