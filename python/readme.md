# Start up commands for Django

Assuming you have installed python and virtualenv already
you can use this command to start a basic django project im using win7

```batch
virtualenv mysite
cd Scripts & activate.bat
pip install django
django-admin startproject mysite
python manage.py migrate
python manage.py createsuperuser
```