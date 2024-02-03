---
title: "Json Dump(s) vs Load(s)"
date: 2023-11-17T20:00:52+05:30
draft: false
tags: ['python']
---

Do you often google the difference between json.dump(s) and json.loads(s) while working with json data in Python?

Well then, this will be your quick guide to distinguish these functions. 

## The difference

- Quite literally, json.load() and json.loads() loads json into your program, while 
- json.dump() and json.dumps() dump data in JSON.

#### Why the extra "s" though? 

- json.dumps() and json.loads() deal with JSON data in the form of a string.  

{{< callout type="info" >}}
  Remember: **s for string** 
{{< /callout >}}

- *Use load & dump when dealing with a file; loads and dumps when dealing with a string.*


## Examples


Assume you have a file named 'data.json' with the following:

```json
{
    "name": "Joe", 
    "age": 25, 
    "city": "Mumbai"
}
```

{{% steps %}}

### json.load() 

- load JSON data from a file.

```python
import json

with open('data.json', 'r') as file:
    data = json.load(file)

print(data)
```

Output:


```shell
{'name': 'Joe', 'age': 25, 'city': 'Mumbai'}
```

### json.loads() 

- load JSON data from a string.


```python
import json

json_str = '{"name": "Jane","age": 30, "city": "Bangalore"}'
data = json.loads(json_str)

print(data)
```


Output:

```shell
{'name': 'Jane', 'age': 30, 'city': 'Bangalore'}
```


### json.dump() 

- write JSON data to a file.


```python
import json

data = {"name": "Grace", "age": 23, "city": "Chennai"}

with open('output.json', 'w') as file:
    json.dump(data, file)
```

Output:

```shell
{"name": "Grace", "age": 23, "city": "Chennai"}
```

### json.dumps() 

- convert a Python object to a JSON-formatted string.


```python
import json

data = {"name": "Gary", "age": 28, "city": "Delhi"}
json_string = json.dumps(data)

print(json_string)
```

Output

```shell
{"name": "Gary", "age": 28, "city": "Delhi"}
```

{{% /steps %}}


### SUMMARY

- load - for reading JSON from a file.
- loads - for reading JSON from a string.
- dump - for writing JSON to a file.
- dumps - for converting a Python object to a JSON-formatted string.

