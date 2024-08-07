# Django Rest Framework

To use django as API is necessary install some libraries running 

```
pip install djangorestframework markdown django-filter
```

After this installation, configure at `settings.py` in `django_project` 

```
...
INSTALLED_APPS = [
    ...

    'django_filters',
    'rest_framework',

    'django_app'
]
...

# DRF
REST_FRAMEWORK = {
    #Autenticação
    'DEFAULT_AUTHENTICATION_CLASSES': {
      #'rest_framework.authentication.TokenAuthentication',
      'rest_framework.authentication.SessionAuthentication',
    },
    #Autorização
    'DEFAULT_PERMISSION_CLASSES': {
      'rest_framework.permissions.IsAuthenticatedOrReadOnly',
    },
}
```

After this, is necessary to include the rest framework urls in project. So, at `django_project/urls.py` configure:

```
...
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('auth/', include('rest_framework.urls')),
]
```
