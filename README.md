
We also encourage you to read the [Spring Boot User Guide](https://docs.spring.io/spring-boot/4.0.1-SNAPSHOT/reference/htmlsingle/)
We are building a web application using Spring Boot.
Version of Technology used : Java 21, spring boot 4.0.1-SNAPSHOT, Gradle 7.6.2

### Step 1. First time when we create the project we must include the following dependencies in build.gradle file.
1. Spring Boot DevTools
2. Spring Boot Web
3. Spring Boot Thymeleaf
4. Spring Boot Data JPA
5. Spring Boot Validation
6. MySQL Connector J


once we have done that we can run the application but it will not work because we have not configured the database.
so we need to configure the database in application.properties file.
But we are going to use the different different profiles to configure the database. Like for production and development and test..
so we will create different profiles for each environment. So to create different profiles we need to create different application.properties files. like for development we will create application-dev.properties file.for production we will create application-prod.properties file.for uat we will create application-uat.properties file.
and ensure that you are including the uat and prod profiles in git tracking because we want to exclude these files to other developers only the admin of the project can make the changes to these files and push it to the only master branch not to development.

Once we create these files then we need to define which configuration file we want to use in application.properties file. for that we need to add spring.profiles.active=dev in application.properties file.
So common property files we are going to use in application.properties file are application.properties, application-dev.properties, application-prod.properties, application-uat.properties. and development related properties we are goint to use in application-dev.properties file.and for uat related configuration we are going to use application-uat.properties file.and for production related configuration we are going to use application-prod.properties file.

Now when we created the file we have not added to git tracking we skiped now we will add uat and prod application.properties files  to gitignore file.

### Now we are ready to run the application.

### Step 2. Create a folder structure in this demo project.
In src/main/java/com/boolment/demowebapp inside it we are going to create all the packages and these 2 files should be outside of the project packages.

But here we are going to make this project as multiple functionlity so we will create a package for each functionlity inside it we are going to keep all the sub folder for entities, repositories, controllers, services, dtos.

