## Django Todo App

### Environment Prep

Preparing workspace:
```
mkdir django-todo-react
cd django-todo-react
pip3 install pipenv
```

Installing env:
```
pipenv shell
```

Installing Django:
```
pipenv install django
```

### Backend Setup

Creating backend project:
```
django-admin startproject backend
cd backend
python manage.py startapp todo
python manage.py migrate  # to create the sqlite database
python3 manage.py runserver  # should be running in localhost:8000
```

Registering applications:
In backend setting.py, ad todo under INSTALLED_APPS

Define your model under todo/models.py:
```
python3 manage.py makemigrations todo  # create the migration file
python3 manage.py migrate todo
```

Enable CRUD operations by registering your rodo model in admin.py:
```
python3 manage.py createsuperuser  # to create your admin user
python3 manage.py runserver  # and go to /admin to login
```

Configuring CORS:
```
pipenv install djangorestframework django-cors-headers
```

More about Django framework https://www.djangoproject.com/start/

### Frontend

For frontend development checkout README.md under frontend module.

### Testing

Deployed on heroku and using Heroku Postgres add-on.
https://calm-peak-56272.herokuapp.com/

The frontend is hosted on:
https://peaceful-citadel-47725.herokuapp.com/
