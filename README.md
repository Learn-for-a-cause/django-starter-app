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

### Session 1 - Models, Admin & Views
**Models:**
  > Models official documentation https://docs.djangoproject.com/en/3.0/topics/db/models/

  * Models define your database schema
  * Register your model in `admin.py`
  * Apply database migrations(changes) by running, 
  ```
  python manage.py makemigrations blog
  ```
  > Here `blog` is the example application name
  ```
  python manage.py migrate
  ```
  * Access the django shell for object creation and debugging 
  ```
  python manage.py shell
  ``` 
**Admin:**
  * Django provides by default admin site
  * Create a super user to login to admin site
  ```
  python manage.py createsuperuser
  ```
  * You can access admin portal in this url `http://127.0.0.1:8000/admin`
  * Create, update, delete model objects in admin portal

### Session 2 - Views & Templates
**Views**
  > Views official documentation https://docs.djangoproject.com/en/3.0/topics/http/views/
  
  * View present the data to the user by rendering HTML page
  * Add url route for your view under application `urls.py`
  * Also make sure your app url is added to main project `urls.py`

**Templates**
  * create a templates folder under the app for example create folder `blog/templates`
  * render the template by giving path to the template in the view `render(request, "blog/templates")`
  * Use `{% load static %}` in base html to load the static asserts in all the templates that inherit the base template 
  * Use template inheritance of django by adding extends tag in child template `{% extents "template/path %}`
  * Added the block of HTML content in the child template by enclosing the HTML tags with `{% block block_name %} <html tags here\> {% endblock %}`, use the same tags in base HTML page as well
  * use `{{ }}` for rendering django object
  * use `{% url url_name values %}` for getting the href link to the url
  * Check condition in template with if block `{% if condition %}<html tags here\>{% endif %}`
  * Iterating is done by for loop in templates `{% for p in posts %} <html tags here \> {% endfor %}`

### Session 3 - Todo app & Forms
  **Todo app requirements:**
  * List all the todo events in the home page
  * User should be able to add a new Todo task
  * User should be able to update the task description
  * User should be able to marks any task as resolved
  * User should be able to delete any task
