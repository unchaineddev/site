+++
title = 'MongoDB Setup'
date = 2024-04-16T18:19:29+05:30
draft = false
tags = ['technology']
+++

### Install 

- [Download](https://www.mongodb.com/try/download/community) the community version of MongoDB. 
- [Download](https://www.mongodb.com/docs/mongodb-shell/) Mongo Shell. 

### Set up Mongosh

- While you set up mongosh (Mongo Shell), you typically get the error below when you type `mongosh` on your terminal:


```text
mongosh : The term 'mongosh' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or
if a path was included, verify that the path is correct and try again.

At line:1 char:1
+ mongosh $Env:MDB_CONNECTION_STRING;
+ ~~~~~~~
    + CategoryInfo          : ObjectNotFound: (mongosh:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

### Solution

- To resolve this, you need to add Environment Variables. To do this: 

1. Go to "Edit System Environment Variables" 
2. Click on "Environment Variables" 
3. Under "System Variables", Edit "Path"
4. Add Two paths as follows:

- MongoDB bin path

`C:\Program Files\MongoDB\Server\7.0\bin`

- Depending on where you have downloaded mongosh:

`C:\Users\yusuf\Downloads\mongosh-2.2.3-win32-x64\mongosh-2.2.3-win32-x64\bin` 


{{< callout type="warning" >}}
 Important: Restart your editor. If it does not work, go to services and restart mongoDB.
{{< /callout >}}

