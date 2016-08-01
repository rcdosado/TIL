# Automate start up of application in windows

The script below starts a variety of applications asynchronously using batch scripts
this is obviously useful to automatically speed up launching your everyday projects.

instructions:

create batch file name it like go.bat in your home directory
and paste the following code inside it.

```Batch
@echo off
start chrome
start firefox
start "" "C:\dev\python\Django By Example\Django By Example.pdf"
start "" "C:\Program Files (x86)\Wing IDE 5.1\bin\wing.exe"
set run=python manage.py runserver
set scripts=c:\dev\python\projects\myenv\Scripts
cd %scripts% & activate.bat & cd.. & cd mysite & cls

```
### what it does:
 it asynchronously runs chrome, firefox , opens a pdf document, starts wing-ide (python IDE)
 and automatically goes to virtualenv environment and activates it, the virtual environment is a django project
 by the way.

 to minimize the navigation of directories, its best to save this to your home directory
 the reason is, it is the default location when you type win+r and cmd

 The script above starts assumes chrome and firefox is globally accessible (defined in PATH variable)

 if you remove start in the beginning of command, it waits for the application to close before returning (synchronous)

 the "" after start, is trick for applications who has spaces in its path. if you remove this, it will just create a new DOS instance.

 after it executes, ill just ` python manage.py runserver ` to run my django project.

