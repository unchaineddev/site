+++
title = 'Parsing Configuration files in Python'
date = 2024-03-27T20:49:21+05:30
draft = false
tags = ['python']
+++

### Introduction

configparser [^1] is a module that provides functionality for working with config files in a standardized format.

Although storing configurations in formats like JSON, Yaml/Toml, environment variables or a database
exists, configparser stands out to me as a pythonic approach, as it promotes
simplicity and reduces dependencies. 


### Quick Start

- #### Let’s take a very basic configuration file:

```
[DEFAULT]
; this is a comment
user_name = super-user
passwd = secure-pass

[DATABASE]
host = localhost
port = 5432
database = mydb

[Logging]
; Logging configuration
log_level = INFO
log_file = /var/log/my_python_app.log
```


- #### creating the same file programatically  


```python 

# importing module
import configparser
config = configparser.ConfigParser()

config['DEFAULT'] = {
        'user_name' : 'super_user',
        'passwd': 'secure-pass'
        }

config['DATABASE'] = {}
config['DATABASE']['host'] = 'localhost'
config['DATABASE']['port'] = '5432'
config['DATABASE']['database'] = 'mydb'


config['LOGGING'] = {
    'log_level': 'INFO',
    'log_file': '/var/log/my_python_app.log'
}


with open('config.ini', 'w') as configfile:
  config.write(configfile)
```

{{< callout type="info" >}} 
If you want to include a default section, you would typically add it to your
configuration file explicitly.
{{</callout >}}


### Accessing data

- Fetches sections, values. Note also that keys in sections are case-insensitive and stored in lowercase.

```python
import configparser

config = configparser.ConfigParser()
config.sections()

config.read('config.ini')

sections = config.sections()  # ['DATABASE', LOGGING']

user_name = config.get('DEFAULT', 'user_name' ) # super-user 
password = config.get('DEFAULT', 'passwd' ) # secure-pass

db_name = config['DATABASE']['database']  # mydb
```

- Config parsers do not guess datatypes of values in configuration files,
always storing them internally as strings. This means that if you need other
datatypes, you should convert on your own.

```python 
port_number = config['DATABASE']['port'] # <class 'str'>
PORT = int(port_number)  # 5432 
print(type(PORT)) # <class 'int'>
```


[^1]: https://docs.python.org/3/library/configparser.html
