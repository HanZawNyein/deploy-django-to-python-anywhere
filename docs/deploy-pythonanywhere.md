# Deploying to PythonAnywhere

Creating Account in Pythonanywhere - [pythonanywhere.com](https://www.pythonanywhere.com/)

Login To Pythonanywhere.

![Login to Pythonanywhere](https://github.com/HanZawNyein/deploy-django-to-python-anywhere/blob/main/images/login.png?raw=true){ align=left }

Go to MyDashboard

![Dashboard](https://github.com/HanZawNyein/deploy-django-to-python-anywhere/blob/main/images/dashboard.png?raw=true){align=left}

Create New Bash

check your `#!python pip` version

```bash
10:02 ~ $ pip3 -V
```

install `#!python pythonanywhere` package for deploy automation

```bash
10:02 ~ $ pip3 install --user pythonanywhere
```

Check `#!python pa_autoconfigure.py` file

```bash
10:02 ~ $ ls -a

pa_autoconfigure.py
```

Deploy Your Django Project

```bash
10:02 ~ $ pa_autoconfigure.py <your-github-repo>.git
```

if you want to replace it, use `#!python --nuke` options

master နေရာတွင် မိမိ clone ထားသော branch တစ်ခုခု ဖြစ်နိုင်ပါသည်။ username နေရာတွင် မိမိ၏ pythonanywhere acoount ရဲ့ username ဖြစ်နိုင်ပါသည်။

```bash
(username.pythonanywhere.com) 10:05 ~/username.pythonanywhere.com (master) $ ls

db.sqlite3 manage.py sub-app requirements.txt static templates root-app
```

admin အတွက် superuser အကောင့်ကို ဆက်လက်တည်ဆောက်ရပါမည်။

```bash
(username.pythonanywhere.com) 10:05 ~/username.pythonanywhere.com (master) $ python3 manage.py createsuperuser

Username (leave blank to use '<username>') :
Email Address :
Pasword :
Password (again):
```

Go to dashboard of Web and click Reload username.pythonanywhere.com button
![Dashboard of Web](https://github.com/HanZawNyein/deploy-django-to-python-anywhere/blob/main/images/reload_button.png?raw=true){align=left}


Now can see your site - username.pythonanywhere.com