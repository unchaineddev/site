+++
title = 'Sphinx Setup Guide'
date = 2024-03-01T06:33:38+05:30
draft = false
+++

Sphinx is a powerful tool to create beautiful documentation by converting plain text source files into various output formats, like HTML, PDFs, LateX.

Sphinx uses the reStructuredText markup language by default, and can read MyST markdown via third-party extensions. Both of these are powerful and straightforward to use, 
and have functionality for complex documentation and publishing workflows. They both build upon Docutils to parse and write documents.


## Prerequisites

- Python 3.8 or later.


## Installation


1. Create a virtual environment.

```bash
$ python -m venv venv
```

2. Install Sphinx


```bash
pip install sphinx
```

3. Activate Environment in powershell/terminal

- Windows 

```powershell
.\venv\Scripts\activate
```

- Linux

```shell
source env/Scripts/activate
```

## Setup

{{% steps %}}

### **Create Docs Layout**

- With this command, all the documentation will be in the `docs` folder.


```bash
sphinx-quickstart docs
```


### **Inputs** 

- These inputs are required when you enter the command from step 1.

```
Separate source and build directories (y/n) [n]: y [Default is **y**]
project name: <enter your project name>
Author name(s): <your name>
Project release []: <release version>
Project language [en]: en 
```


### Build the project

```bash
sphinx-build -M html docs/source/ docs/build/
```

- To check the generated html, open the `index.html` file in the `build/html` folder.

{{% /steps %}}


## Adding extensions

1. go to `docs/source/conf.py`


```python
# Add any Sphinx extension module names here, as strings. They can be
# extensions coming with Sphinx (named 'sphinx.ext.*') or your custom
# ones.
extensions = [
    'sphinx.ext.duration',
]
```

Customize your Sphinx documentation effortlessly with these steps!

