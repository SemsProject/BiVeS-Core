/ModelRetriever 
================
Some markup languages provide capabilities to import modules in a model. That means a model may point to a resource located on your disk or on a remote file server. /BiVeS uses the !FileRetriever provided by BFUtils to download/copy/read these files.

However, since the world is full of evil people guys may try to get access to sensible files on a web server running /BiVeS by encoding local imports pointing to e.g. *```/etc/passwd```*, or they may want to track your model usage by *"requiring" an empty model* from their web server.

Therefore, it might be clever to restrict the access to local or remote files:
```
#!java
// disallow reading of local files (e.g. for web servers, when there is nothing useful stored locally)
FileRetriever.FIND_LOCAL = false;
// disallow reading of remote files (e.g. to prevent tracking)
FileRetriever.FIND_REMOTE = false;
```
