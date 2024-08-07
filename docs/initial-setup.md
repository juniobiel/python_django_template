# Django API Project

## Creating the virtual environment
To create virtual environment to setup project and install packages, is necessary the following steps
```
python3 -m venv .venv
```
venv is a library that creates the configurated virtual environment, and the ".venv" is the name of directory where the files for these configurated environment are installed.
After this initial setup, use `.venv/Scripts/Activate.ps1` to activate the virtual environment and setup the packages for the project.

## Installing the and Setup Django

To start, is necessary that to install the latest django
```
pip install django
```
After that, is possible to use **django-admin** cli to create and configure project

To configure the django project, use
```
django-admin startproject django_project
```
And to configure the django app, use
```
django-admin startapp django_app
```

After that, two directories are created. Is necessary some initial configurations at `django_project`.

```
...

INSTALLED_APPS = [ 
    ...
    'django_api',
    ...
]

...

LANGUAGE_CODE = 'pt_br'

TIME_ZONE = 'America/Sao_Paulo'

...

STATIC_URL = 'static/'
STATIC_ROOT = os.path.join(BASE_DIR, 'staticfiles')
MEDIA_URL = 'media/'
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')

...

```

