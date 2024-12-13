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


