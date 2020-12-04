##  Deploying Spring Boot JAR file with Thymeleaf on AWS

###  Deploy Spring Boot app on AWS

- AWS EBS expects for your apps to listen on port 5000
- Update your Spring Boot application.properties to use: server.port=5000
- Select Web App > Platform Java
- Upload the JAR file

#####  Test Spring Boot app locally

1.  Start with a simple REST app. Use any Spring Boot app
2.  Change port to 5000
3.  Open terminal window
4.  cd project directory
5.  mvn clean package
6.  Run your app
    -  `java -jar target/myapp.jar`      (or whatever name of your jar file)
7. Test it locally: `http://localhost:5000/api/v1/beer/0a818933-087d-47f2-ad83-2f986ed087eb/inventory`

#####  Deploy Spring Boot App to AWS

1.  Log into to AWS
2.  Navigate to Elastic Beanstalk
3.  Create a new application
4.  Select app type: Web Application
5.  Give it the name: simple-boot-demo
6.  Create a new environment
7.  For platform, select: Java
8.  Select option to Upload your JAR file.
    -  Note: the screen says only WAR and ZIP files, but it does in fact accept JAR files
9.  Upload your JAR file: target/myapp.jar
10.  Create the application
11.  Once the app is created, then visit the app URL.
    -  **actuator**: `http://deployjar-env.eba-x3pahtn7.eu-west-3.elasticbeanstalk.com/actuator`
    -  `http://deployjar-env.eba-x3pahtn7.eu-west-3.elasticbeanstalk.com/api/v1/beer/0a818933-087d-47f2-ad83-2f986ed087eb/inventory`

You will see your Spring Boot app up and running. :-)