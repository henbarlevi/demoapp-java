# Maestrano Java DemoApp

This application shows examples of how to use the Maestrano Java API. A live version of this application is available at this address:

http://java-demoapp.maestrano.io

## Running the application locally

First build with:
```
mvn package
```
Then run it with (application uses embedded tomcat):

Linux
```
sh target/bin/webapp
```
Windows
```
target/bin/webapp.bat
```

If you need to use a special port
```
PORT=1238 sh target/bin/webapp

```