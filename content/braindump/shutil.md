+++
title = 'shutil in python'
date = 2024-06-01T08:55:22+05:30
draft = false
tags = ['python']
+++


- module for high-level operations for copying, removing, moving files/directories.

{{% steps %}}

### Copy

```python
import shutil

# copies file located at source. If file already exists, it's overwritten
shutil.copy("main.py", "main2.py")

# copy2 is similar to copy except preserves metadata
shutil.copy2("main.py", "main2.py")

# copytree - copies full directory
shutil.copytree(".folder1", "myfolder")
```


### Move


```python
import shutil

shutil.move(".folder1/file.txt", "file.txt")  # moves file
```

### Delete

```python
import shutil

shutil.rmtree("folder1")  # deletes folder
```

{{% /steps %}}
