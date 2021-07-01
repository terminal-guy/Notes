# Creating Your Django Project

Pipenv package is so easy and more comfortable than using virtualenv or any other virutal enviroment creating package.

- **To Create a virtual enviroment And a install a package using**
	- ```pipenv install django ```
- **And use  ``pipenv shell `` to run it   **
- **To create a Django project**
	- `django-admin startproject projectname`

- **File and It's uses**
	- __init__.py = We don't touch that file that is for the project mangement for the directory's and some other stuffs.
	- asgi.py and wsgi.py = are for project deployment.
	- urls.py = For storing urls.
	- settings.py = for adding apps and set some settings.
	- manage.py = it's the core application of the project. It been used to run  our project and maintain admin stuff.


- We can expectily set the port number while running the server. If we having another application running on the same localhost server port it's may lead to errors. So if you have a another application use a port while running the server.


	

