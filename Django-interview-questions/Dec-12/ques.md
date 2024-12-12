# 1 Explain *args and **kwargs with example?

*) *args is used to pass a variable number of non-keyword arguments (positional arguments) to a function. It allows the function to accept any number of arguments (as a tuple).

*) **kwargs is used to pass a variable number of keyword arguments (named arguments) to a function. It allows the function to accept any number of arguments, which will be collected into a dictionary.

# 2 Difference between apps amd project in django?

*) Project
A Django project is the entire configuration and settings for a Django-powered website. It serves as the overall container for your web application.
A project contains configurations and settings that apply to the entire site.
It typically consists of:
A main directory containing the settings, URLs, WSGI/ASGI configurations, and other global files (e.g., settings.py, urls.py, wsgi.py, and manage.py).
It can include multiple apps, each with its own functionality.

 App

A Django app is a modular component of the project. It is designed to do a specific functionality (e.g., a blog, a user authentication system, or an e-commerce cart).
An app is reusable across projects (if designed modularly).
It typically contains:
models.py: Database models.
views.py: Business logic.
urls.py: URL routing for the app.
admin.py: Admin panel customization.
apps.py: App-specific settings.
migrations/: Database schema changes.

# 3) Difference between MVC and MVT design patterns?

*) Model and View are both driven by the controller in MVC, whereas Views in MVT are used to receive HTTP requests and return HTTP responses.
*) We must write all of the control-specific code in MVC whereas, We must write all of the control-specific code in the View and Template components in MVT.
*) MVC is Highly coupled whereas, MVT is loosely coupled.
*) In MVC, it is difficult to modify whereas, Modification is easy in MVT.
*) MVC is suitable for large applications, but MVT is suitable for both small and large applications.
*) MVC does not involve any URL mapping, whereas in MVT URL pattern mapping takes place.
*) Flow is clear and easy to understand, whereas MVT is sometimes harder to understand.

# 4) What is Django ORM?

ORM which is also known as the object relation model enables us to interact with our database. It allows us to add, delete, change, and query objects (Object Relational Mapper). Django uses a database abstraction API called ORM to interface Viewed with its database models, to use Django object relation Models, we must first have a project and an app running. Models can be created in app/models.py after an app has been started. The Django ORM may be accessed by running the following command in our project directory.

        python manage.py shell

This opens a Python console where we may add objects, retrieve objects, modify existing items, and delete objects. 

# 5) What is Superuser?

superuser is the most powerful user with permission to create, read, delete, and update on the admin page which includes model records and another user. Users of Django have access to an Admin Panel. Before using this feature, you must have to migrate your project; otherwise, the superuser database will not be created. To create a superuser,  first, reach the same directory, and run the following command

python manage.py createsuperuser

# 6)What is Jinja templating?

Jinja is also known as jinja2, which is the most recent version. It’s a template engine that allows you to make HTML, XML, and other markup types. Jinja2 is valuable since it features a templating tag syntax and because the project has been extracted as a standalone open-source project that may be utilized as a dependency by other code libraries. Some of its features are:

*) HTML Escaping – It provides automatic HTML Escaping as <, >, & characters have special values in templates and if using a regular text, these symbols can lead to XSS Attacks which Jinja deals with automatically.
*) Sandbox Execution – This is a framework for automating the testing process in a sandbox (or protected) environment.
*) Template Inheritance
*) Produces HTML templates far more quickly than the default engine.
*) When compared to the default engine, it is easier to debug.

# 7) What do you mean by the csrf_token?

Cross-Site Request Forgery (CSRF) is one of the most serious vulnerabilities, and it can be used to do everything from changing a user’s information without their knowledge to obtaining full control of their account. To prevent malicious attacks, Django provides a per cent token per cent tag {% csrf_token %} that is implemented within the form. When generating the page on the server, it generates a token and ensures that any requests coming back in are cross-checked against this token. The token is not included in the inbound requests, thus they are not executed.

# 8) Explain the use of Middlewares in Django.

Middleware is a lightweight plugin in Django that is used to keep the application secure during request and response processing. The application’s middleware is utilized to complete a task. Security, session, CSRF protection, and authentication are responsible for doing some specific functions. The application’s security is maintained by the usage of the middleware component, AuthenticationMiddleware which is associated with user requests using sessions.

# 9) What are ‘signals’?

Signals are used to take action in response to the modification or creation of a database entry. Its utilities help us to connect events with their action. we can create methods that will run a signal when it is called. For example, as soon as a new user instance is generated in the Database, one might want to create a profile instance. Generally, There are 3 types of signals.

*) pre_delete/post_delete: This signal is thrown before the remove() method is used to delete a model’s instance.
*) pre_init/post_init: This signal is thrown before/after instantiating a model (__init__() method)
*) pre_save/post_save: This signal works before/after the method save().

# 10) What is Media Root?

Media root is used to upload user-generated content. We can serve user-uploaded media files locally, using the MEDIA_ROOT and MEDIA_URL settings. User-upload these files are referred to as Media or Media Files in Django. The first step is to include the code below in the settings.py file.


MEDIA_ROOT = os.path.join(BASE_DIR, ‘media’)
MEDIA_URL = ‘/media/’


MEDIA_ROOT: It is for the server path to store files in the computer.
MEDIA_URL: It is the referring URL for the browser to access the files over HTTP.
