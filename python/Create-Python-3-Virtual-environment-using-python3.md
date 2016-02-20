# Create Python 3 Virtual environment using python3

this console command allows you to createa virtual environment for python 3
i cannot find how to do this using virtualenv, i found out it can be done using python 3 only
the example below uses python3.4 assumes requirements.txt contains dependencies for the project

```batch
>c:\python34\python.exe -m venv new_project
>cd new_project\Scripts
>activate.bat
>cd ..
>pip install -r requirements.txt
```