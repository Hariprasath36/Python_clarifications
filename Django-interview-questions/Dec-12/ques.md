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

# 11) How you can include and inherit files in your application?

Using the extends tag in Templates, we can inherit our files in Django, The extends tag is used to inherit these templates. The syntax for inheriting these templates is given as:

{% extends 'template_name.html' %} 

This syntax helps us to add all the elements of an HTML file into another without copy-pasting the entire code. Django templates not only allow us to pass variables from view to template, but they also provide some programming capabilities like loops, comments, and extensions.

# 12)  How do you connect your Django Project to the database?

We need to configure our database in the settings.py file. By default, SQLite is mentioned there, and we need to change this setting accordingly like Postgres, MongoDB, and MySql. 

# 13) Explain the caching strategies of Django. ?
Django has its own inbuilt caching system that allows us to store our dynamic pages. So that we don’t have to request them again when we need them. The advantage of the Django Cache framework is that it allows us to cache data such as templates or the entire site. Django provides four different types of caching options, they are:

*) per-site cache – It is the most straightforward to set up and caches your entire website.
*) per-view cache – Individual views can be cached using the per-view cache.
*) Template fragment caching allows you to cache only a portion of a template.
*) low-level cache API – It can manually set, retrieve, and maintain particular objects in the cache using the low-level cache API. 

# 14) Give the exception classes present in Django.

An exception is a rare occurrence that causes a program to fail. Django has its own exception classes to cope with this circumstance, and it also supports all fundamental Python exceptions. some of the exception classes are listed below:

*) MultipleObjectsReturned – If just one item is anticipated but many objects are returned, this error is thrown by the query.
*) ViewDoesNotExist – When a requested view does not exist, Django.URLs raise this exception.
*) PermissionDenied – It’s triggered when a user doesn’t have the necessary permissions to perform the requested activity.
*) SuspiciousOperation – The query throws this error if only one item is expected but several things are returned.
*) ValidationError – It’s triggered when data validation fails on a form or a model field.
*) FieldDoesNotExist – It raises when the requested field does not exist.
*) ObjectDoesNotExist – The base class for DoesNotExist exceptions.
*) AppRegistryNotReady – It is raised when attempting to use models before the app loading process.
*) EmptyResultSet – If a query does not return any result, this exception is raised.

# 15) What is No SQL and Does Django support NoSQL?

NoSql is also known as a non-relational database that stores data in a form of non-tabular, instead it stores data in the form of a storage model that is optimized for specific requirements of the type of data being stored. The types of NoSQL databases include pure documented databases, graph databases, wide column databases, and a key-value store. 
No, Django does not officially support no-SQL databases such as CouchDB, Redis, Neo4j, MongoDB, etc. 

# 16) What are the different model inheritance styles in Django?

Django supports 3 types of inheritance. They are

*) Abstract base classes
*) Multi-table Inheritance
*) Proxy models

# 17) What databases are supported by Django?

Databases that are supported by Django are SQLite(Inbuild), Oracle, PostgreSQL, and MySQL. Django also uses some third-party packages to handle databases including Microsoft SQL Server, IBM DB2, SAP SQL Anywhere, and Firebird. Django does not officially support no-SQL databases such as CouchDB, Redis, Neo4j, MongoDB, etc.

# 18) How would you query all the items in the database table?

XYZ.objects.all()
 Where XYZ is some class created in the model.

# 19) What is Django Rest Frameworkcont

The REST Framework is an HTTP-based standard for listing, generating, modifying, and deleting data on your server. The Django REST framework which is also known as DRF is a powerful and flexible toolkit built on top of the Django web framework that simplifies the creation of REST interfaces by reducing the amount of code required. there are different advantages of using REST Framework like:

*) Web browsable API that provides huge usability for developer
*) Authentication policy which includes packages for 0auth1 and auth2.
*) It supports both ORM and non-ORM data sources.
*) It has extensive documentation and great community support.

# 20) Explain the Django Response lifecycle.

The Django Response lifecycle is responsible for data interchange between clients and servers with the help of the HttpRequest object, whenever a request is made by the client to the server it passes information through the system using request and response objects. these request/response objects are transmitted over the web which contains request metadata such as images, HTML, CSS, and javascript. These data are then loaded and presented to the user by Django, which passes the HttpRequest as the first argument to the view method. It is the responsibility of each view to return a HttpResponse object.

