---
title: "Django Project Structure"
date: 2023-12-16T20:00:39+05:30
draft: false
tags: ['python', 'django']
---


I love the Python Programming Language, and its most popular Web Framework - Django. In fact I love it so much that it is reflected in my pseudonym. I am no expert django dev, however I understand the design. this blog post unravels the intricacies of Django's structural design.


## Design 

Django follows a Model-View-Template (MVT) architectural design pattern.

- __Model__: Defines the data structure of the application. Models are used to interact with the database.

- __View__: Handles user requests, processes data from the model, and renders templates. 

- __Template__: Handles how data is displayed. Typically written in HTML with Django template language. 


## Project & App

- __Project__: A Django project is the entire web application. 
- __App__: A module within a project that performs a specific function.


## Typical Project Structure

{{< filetree/container >}}
  {{< filetree/folder name="myproject" >}} 
  {{< filetree/file name="manage.py" >}}
  {{< filetree/folder name="myproject" >}} 
      {{< filetree/file name="\__init__\.py" >}}
      {{< filetree/file name="settings.py" >}}
      {{< filetree/file name="urls.py" >}}
      {{< filetree/file name="wsgi.py" >}}
  {{< /filetree/folder >}}

  
  {{< filetree/folder name="static" >}} 
   {{< /filetree/folder >}}
  {{< filetree/folder name="templates" >}} 
   {{< /filetree/folder >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}


-- __manage.py__: A command-line utility for interacting with the project, such as running development servers, creating database tables, creating superusers, making migrations, etc.

-- __myproject/__: Named after the core project. contains global urls, settings.

-- <b>\_\_init_\_\.py</b> - empty file that indicates that this directory should be treated as a Python Package.

-- __settings.py__: global configuration settings for the project, including database connections, static files, middleware, and more.

-- __urls.py__:  Defines the URL patterns for the project.

-- __wsgi.py__: configuration for the WSGI server, which is responsible for serving the web application.

-- __asgi.py__: similar to WSGI, but it performs some additional functions



## App Structure 


{{< filetree/container >}}
  {{< filetree/folder name="myproject" >}} 
    {{< filetree/file name="manage.py" >}}
    {{< filetree/folder name="my app" >}}  
      {{< filetree/folder name="migrations" >}}
      {{< /filetree/folder >}}
      {{< filetree/file name="__init__.py" >}}
      {{< filetree/file name="admin.py" >}}
      {{< filetree/file name="apps.py" >}}
      {{< filetree/file name="models.py" >}}
      {{< filetree/file name="tests.py" >}}
      {{< filetree/file name="views.py" >}}
    {{< /filetree/folder >}}
    {{< filetree/folder name="myproject" >}}
     {{< /filetree/folder >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}


─ __migrations/__: propagating changes you make to your models 

─ __admin.py__: file used to display the admin panel, connect models to the panel and make changes to admin interface.

─ __apps.py__: configures the Django app.

─ __models.py__: To create models so that we can query data.

─ __tests.py__: contains code for application testing.

─ __views.py__: Python functions that takes http requests and returns http response.


# Static

-- stores images, CSS, or JS files.


# Templates 

-- a HTML document or a Python string mark-up using the Django template language.

