# Django - taggit
@django 

Installing in a project
-----------------------


* ``pip install django-taggit``
* add 'taggit' to ~INSTALLED_APPS
* ``./manage.py syncdb``


```python
from django.db import models
from taggit.managers import TaggableManager

class Thing(models.Model):
# ... fields here

tags = TaggableManager()
```
