# gateway

This application was generated using JHipster 8.1.0, you can find documentation and help at [https://www.jhipster.tech/documentation-archive/v8.1.0](https://www.jhipster.tech/documentation-archive/v8.1.0).

This is a "gateway" application intended to be part of a microservice architecture, please refer to the [Doing microservices with JHipster][] page of the documentation for more information.
This application is configured for Service Discovery and Configuration with . On launch, it will refuse to start if it is not able to connect to .

## Project Structure
Using gateway as Authentication 
this Micro-service provide to create User with role (ADMIN, Users)
it s implemented inside gateway provider with mechanism to generate token with Spring security


## Run Project
./mvnw

## APi Create and authenticate 
 we need to generate from gateway to use betwwen other microservice .
for our case we will use hwt Token to validate Authority for Api called

* Creation user 
* the users already created ith liquibase when we start the microservice we can found the data here .../src/main/resources/config/liquibase/data
* we have two users to authenticate :
* 1/ {"username":"user",
  "password":"user"}
* 2/{"username":"admin",
  "password":"admin"}
* to generate token we need to call this api POST http://127.0.0.1:8080/api/authenticate
 we need save the token for the other APis
