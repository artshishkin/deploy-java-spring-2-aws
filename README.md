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

####  Section 4: Deploy MySQL Database in AWS with RDS

#####  18. Deploy MySQL Database in AWS with RDS - Demo - Create Instance

1.  Create DB in Paris (Free tier)
    -  MySQL
    -  Templates:  Free tier
    -  DB identifier: `springaws-db`
    -  Master username and password: `springstudent`
    -  Public access: **Yes**
    -  VPC security group: Create new `chad-spring-rds-sg`

#####  19. Configure Database 

1.  Modify Security Group to access from Anywhere (optional - may be modified later if our IP changes)
2.  Test database connection with MySQL Database
    -  copy Endpoint URL
    -  In MySQL Console Create new Connection
        -  `chad-spring-rds-aws`
        -  Endpoint (hostname): `springaws-db.cha39fdqzzb3.eu-west-3.rds.amazonaws.com`
        -  port: 3306
        -  Username: `springstudent`
        -  Password: `springstudent`
        -  Test connection: Successful
        -  Create (OK)            

#####  20. Create Table

-  Use `create-user.sql` and `customer-tracker.sql`  scripts
-  In Workbench:
    -  Open SQL script: `customer-tracker.sql`
    -  Execute SQL Script
    -  Schemas:  Refresh All
    -  View `web_customer_tracker`