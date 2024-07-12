# Django Messaging System with RabbitMQ/Celery

This project implements a Django application behind Nginx that interacts with RabbitMQ/Celery for email sending and logging functionalities.

## Setup Instructions

### Local Setup

1. **Install RabbitMQ and Celery:**
   - Follow installation instructions for RabbitMQ.
   ---I'm on Mac so I'm going to use brew
   ```zsh
   brew update
   brew install rabbitmq
   ```
   - Install Celery using pip.
   ```zsh
   pip install celery
   ```

2. **Setting up Django Project:**
   - Initialize Django and activate the virtual environment.
   -- Prepare virtual environment
   ```zsh
   python3 -m venv env
   ```
   - Activate vitual environment
   ```zsh
   source env/bin/activate
   ```
   --------------------------------------------
   - Install Django in the virtual environment
   ```zsh
   python -m pip install django
   ```
   - Create requirements.txt for version control
   ```zsh
   python -m pip freeze > requirements.txt
   ```
   - Create django project
   ```zsh
   django-admin startproject celerycourier .
   ```
   - Start django app
   ```zsh
   python manage.py startapp messaging 
   ```
--------------------------------------------------

### Endpoint Functionalities

#### `/?sendmail` Endpoint

- Description: Allows sending emails using SMTP and queues tasks with RabbitMQ/Celery.

#### `/?talktome` Endpoint

- Description: Logs the current time to `/var/log/messaging_system.log`.

#### `/logs` Endpoint

- Description: Access application logs.

### Nginx Configuration

- Configure Nginx to serve the Django application and route requests correctly.

### Testing

- Test functionality of `/?sendmail`, `/?talktome`, and `/logs` endpoints.
- Ensure Nginx is correctly routing requests.

## Screenshots and Video Walk-through

- Add screenshots of endpoint functionality.
- Embed a video walk-through demonstrating the setup and deployment process.

## Authors

- List team members who contributed to this project.

## License

- Mention the license under which the project is distributed.
