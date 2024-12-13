# 1) How do filter items in the Model?

To filters items present in our database we use a QuerySet. It is a database collection of data that is built up as a list of objects. QuerySet makes our work easy by allowing us to filter and organize the data, it is also easier to retrieve the information that we need with the help of QuerySet. we can filter our data with the help filter() method that allows us to return only the rows that match the search word.

# 2) What is the difference between CharField and TextField in Django?

*) TextField is a database field that is used to store big amounts of text. Paragraphs, data, and other items can be saved. CharField should be used to hold tiny text such as First name and Last name. Let’s make a new instance of the TextField we just made and see whether it works.
*) CharField is a string field, for small- to large-sized strings. It is generally used for storing small strings like first names, last names, etc. To store larger text TextField is used.

# 3) Give a brief about the settings.py file.

It’s the Django file’s main settings file, as the name says. Everything inside the Django project is saved in this file as a dictionary or list, including databases, middlewares, backend engines, templating engines, installed applications, static file URLs, main URL configurations, authorized hosts, servers, and security keys. When Django files are started, the settings.py file is first executed, followed by the loading of the appropriate databases and engines to swiftly serve the request.

# 4) What are Django cookies?

A cookie is a piece of information stored in the client’s browser. To set and fetch cookies, Django provides built-in methods to use the set_cookie() method for setting a cookie and the get() method for getting the cookie. we can also use the request.COOKIES[‘key’] array to get cookie values.

# 5) How to check the version of Django installed on your system?

Open the command prompt and enter the following command

py -m django --version

# 6) Why is Django called a loosely coupled framework?

Django is known as a loosely connected framework because of its MTV architecture. Django’s design is an MVC variant, and MTV is advantageous since it totally separates server code from the client’s hardware. The client machine has Models and Views, and templates are only returned to the client. All of the architectural elements make distinct from one another.

# 7) Explain Django Security.

The security of users’ data is an important aspect of any website design. Django provides adequate security against a number of common threats. Django’s security features are as follows:

*) Cross-site scripting (XSS) protection
*) SQL injection protection
*) Cross-site request forgery (CSRF) protection
*) Enforcing SSL/HTTPS
*) Session security
*) Clickjacking protection
*) Host header validation

# 8) Explain user authentication in Django

Django comes with an authentication system configured by default to handle objects like users, groups, permissions, and so on. The authentication system’s core is made up of user objects. It not only authenticates users but also authorizes them. Aside from using the default, we can employ a variety of web apps instead of using the default system to enable more user authentication. The default system objects are as follows:

*) Users
*) Permissions
*) Groups
*) Password Hashing System
*) Forms Validation
*) A pluggable backend system

# 9) What is the “Django.shortcuts.render” function?

We need the render function when a View function produces a web page as a HttpResponse instead of a basic string. Render is a shortcut for passing a template and a data dictionary. This function combines templates with a data dictionary using a templating engine. Finally, render() provides a HttpResponse containing the rendered text as well as the data from the models.

Syntax: render(request, template_name, context=None, content_type=None, status=None, using=None)

# 10) What is a context in Django?

In Django, a context is a dictionary in which the keys represent variable names and the values reflect the values of those variables. This dictionary or context is supplied to the template, which finally outputs the dynamic content using the variables. i.e. {var1: 11, var2: 12}, when you pass this context to the template render method, {{ var1 }} would be replaced with 11 and {{ var2 }} with 12 in your template.
