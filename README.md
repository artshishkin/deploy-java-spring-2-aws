# Deploy Java Spring Apps Online to Amazon Cloud (AWS)

## Tutorial from Chád (shod) Darby (Udemy)

####  Section 2: Getting Started with Amazon Web Services

#####  12. Deploy HelloWorld JSP App - Demo: Create App and Upload WAR to Elastic Beanstalk

1.  Deploying WAR file into Tomcat container
    -  Beanstalk management console
    -  Create new application `Hello World App`
    -  Create a new Environment
        -  Platform: Tomcat
        -  Upload your code
        -  Configure more options: ensure single instance for dev environment
        -  Create environment
2.  Testing
    -  visit url: `http://helloworldapp.eu-north-1.elasticbeanstalk.com/` (will be changed)
    -  Update app:
        -  Applications: `Hello World App`
        -  Application versions
        -  Upload
        -  After upload:
            -  tick it
            -  Actions -> Deploy 

####  Section 3: Deploy Java Spring Apps to Amazon Cloud

-  Create new Application **OR** Update existing (I choose update)
-  Visit `http://helloworldapp.eu-north-1.elasticbeanstalk.com/`  