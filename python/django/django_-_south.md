# Django - South
@django 

Installing in a project
-----------------------


* ``pip install South``
* add 'south' to ~INSTALLED_APPS
* ``./manage.py syncdb``


Adding South to an existing project
-----------------------------------


* add 'south' to ~INSTALLED_APPS
* ``./manage.py syncdb``
* ``./manage.py convert_to_south myapp``


Initial migrate schema creation
-------------------------------



 ./manage.py schemamigration app --initial
 ./manage.py migrate app

Change schema
-------------



 ./manage.py schemamigration app --auto
 ./manage.py migrate app



