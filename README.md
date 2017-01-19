# Maestrano Java DemoApp

This application shows examples of how to use the Maestrano Java API. A live version of this application is available at this address: http://java-demoapp.maestrano.io 

That may be tested from our sandbox environment: https://sandbox.maestrano.com

Please follow the documentation described here: https://maestrano.atlassian.net/wiki/display/DEV/Integrate+your+app+on+partner%27s+marketplaces

## Running the application locally

### What you'll need
- JDK 1.7 or later
- Maven 3 or later

### Stack
- Spring Boot
- Java

### Guide

Go to https://developer.maestrano.com

Create a new Application, and a new Environment. Make sure your environment is associated to the Marketplace: Maestrano Singapore.

Retrieve your API Key and Secret

Set up the App endpoints:
- Host: http://localhost:1234j
- SSO Init Path: /maestrano/auth/saml/init/%{marketplace}
- SSO Consume Path: /maestrano/auth/saml/init/%{marketplace}

Then run it with (application uses [spring boot](https://projects.spring.io/spring-boot):

Linux
```
export MNO_DEVPL_ENV_NAME=<your environment name>
export MNO_DEVPL_ENV_KEY=<your environment key>
export MNO_DEVPL_ENV_SECRET=<your environment secret>
export SERVER_PORT=1234 
mvn spring-boot:run
```

Windows
```
set MNO_DEVPL_ENV_NAME=<your environment name>
set MNO_DEVPL_ENV_KEY=<your environment key>
set MNO_DEVPL_ENV_SECRET=<your environment secret>
set SERVER_PORT=1234
mvn spring-boot:run
```

Go to the platform sandbox:
https://sandbox.maestrano.com

Add your App from the marketplace

Start the application

## Deploy the application on heroku
```
heroku create
heroku config:set MNO_DEVPL_ENV_NAME=<your environment name> MNO_DEVPL_ENV_KEY=<your environment key> MNO_DEVPL_ENV_SECRET=<your environment secret>
git push heroku master

```
