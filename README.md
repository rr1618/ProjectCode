# ProjectCode
# Command for enviromnent setup

1. python3 -m venv env
2. source env/bin/activate  # On Windows use `env\Scripts\activate`

# Install Django and Django REST framework into the virtual environment
pip install django
pip install djangorestframework

# Set up a new project with a single application
django-admin startproject unified .  # Note the trailing '.' character
cd unified
django-admin startapp dataApp
cd ..

#Install all requirements
python3 -m pip install -r requirements.txt 

python manage.py migrate

python manage.py createsuperuser --email admin@example.com --username admin

python manage.py runserver