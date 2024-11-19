Research Management System
A web-based application designed to manage research projects, users, and their data. This system allows users to log in, register, and manage their projects. The backend is powered by Django, and it uses MySQL as the database for data storage.

Features
User registration and authentication
Add, view, edit, and delete research projects
Clean and responsive UI using TailwindCSS
Secure authentication and session management
Admin interface for managing users and projects
Technologies Used
Backend: Django 5.1.2
Frontend: TailwindCSS
Database: MySQL
Authentication: Custom Django authentication
Version Control: Git
Web Server: Gunicorn (for production deployment)
Prerequisites
Before you begin, ensure that you have the following installed:

Python 3.8 or higher
Django 5.1.2
MySQL Database
Node.js (for frontend build tools)
Installing MySQL
Ensure you have MySQL installed on your machine. You can download it from MySQL's official website.

After installation, create a database for the project:

CREATE DATABASE research_management_system;
Setup
Follow these steps to set up the project locally:

1. Clone the repository
git clone https://github.com/BYUMVUHOREAimable/research-management-system.git
cd research-management-system
2. Set up a virtual environment
Create and activate a virtual environment:

python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
3. Install the dependencies
pip install -r requirements.txt
4. Configure Database Connection
Open settings.py in your Django project and configure the DATABASES setting to use MySQL:

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'research_management_system',
        'USER': 'your_mysql_username',
        'PASSWORD': 'your_mysql_password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
5. Apply migrations
Run the following command to apply the migrations to your MySQL database:

python manage.py migrate
6. Create a superuser
To access the Django admin interface, create a superuser:

python manage.py createsuperuser
Follow the prompts to create the superuser.

7.Run the development server
Now you can start the Django development server:

python manage.py runserver
Visit http://127.0.0.1:8000 to access the site.


pip install gunicorn
Start Gunicorn:

gunicorn --workers 3 research_management_system.wsgi:application
Contributing
We welcome contributions! If you'd like to contribute to the project, please fork the repository, make your changes, and create a pull request. For any issues or feature requests, feel free to open an issue in the GitHub repository.
