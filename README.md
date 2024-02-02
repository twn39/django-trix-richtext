## Trix editor for django framework


### Install

```shell
pip install django-trix-richtext
```

```py
INSTALLED_APPS = [
    'trixeditor.apps.TrixEditorConfig',  ## enable 
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
]
```

### Usage

```py
from django.db import models
from trixeditor.fields import TrixRichTextField


class Post(models.Model):
    title = models.CharField(max_length=255)
    content = TrixRichTextField()
    pub_date = models.DateTimeField('date published')

    def __str__(self):
        return self.title
```

### Screen

![django-trix](https://github.com/twn39/django-trix-richtext/assets/1572872/81133cd1-0a54-4953-91d4-56465e863014)
