# django-starter-app

## Setup

**Requirements**
  * Install git
  * Install [Python 3.8](https://www.python.org/downloads/windows/)  
  * Make sure you have pip installed along with python, run this command for checking your pip version
  ```
  pip3 --version
  ```
  * Clone this git repository to your local
  ```
  git clone git@github.com:Learn-for-a-cause/django-starter-app.git
  ```
### Install virtual environment
Install virtualenv
  
```
pip3 install virtualenv
```
In your Command Prompt navigate to your project:
```
cd django-starter-project
```
Within your project run this command to create virtual environment
```
virtualenv myenv
```
Activate your virtualenv: on Windows, virtualenv creates a batch file
```
myenv/Scripts/activate.bat
```
To activate virtualenv on Windows, run the activate script in the command prompt
```
source ./myenv/Scripts/activate
```
To deactivate virtualenv just type `deactivate` into your command prompt. Install necessary requirements by running this
```
pip install -r requirements.txt 
```
To check the version of django
```
python -m django --version
```
### Create django project
> **Django Tutorial**: https://docs.djangoproject.com/en/2.2/intro/tutorial01/

To create your first django project run this in command prompt
```
django-admin.py startproject myproject
```
Run the django project and in the browser open `http://127.0.0.1:8000/`
```
cd myproject
python manage.py runserver
```
Create an app inside django project using this command
```
python manage.py startapp blog
```
