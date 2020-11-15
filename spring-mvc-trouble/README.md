Pivotal CF Workshop - Spring MVC
================================

Introduction
------------

This is the Spring MVC sample application for the Pivotal CF Workshop.
It is intended to demonstrate some of the basic functionality of Pivotal
CF:

 * Pivotal CF target, login, and push
 * Pivotal CF environment variables
 * Pivotal CF service variables
 * Scaling, router and load balancing
 * Health manager and application restart
 * RDBMS services and application auto-configuration

Building, Packaging, and Deploying
--------------------------------

###To get the source code and build the WAR file


    git clone https://github.com/bjimerson-pivotal/cf-workshop-spring-mvc

    mvn clean package

###To run the application

The application is set to use an embedded H2 database in non-PaaS environments,
to take advantage of Pivotal CF's auto-configuration for services.  No
additional configuration is necessary when running locally or in Pivotal CF.

In Pivotal CF, it is assumed that a postgres service will be used.  If another
service type, such as MySQL, is to be used, update the POM file and the manifest
before pushing.

Stack
-------
The application uses Spring 4, Spring Boot, Spring Data JPA, Spring Cloud, and Thymeleaf.  It can be packaged and run as either a JAR or a WAR, and it can run in cloud or non-cloud environments.
