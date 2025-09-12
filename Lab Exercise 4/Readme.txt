step 1 :

*Install tomcat
*Port 8081
*Start Server
*check "http://localhost:8081"

------------------------------------------------------------------------

step 2 :

*Edit environmental variable 
*Add Maven path
*Add Java Path
*Add Maven and Java bin files to path

------------------------------------------------------------------------

step 3 :

*Config Tomcat
*In tomcat folder -> conf -> tomcat-user.xml
*replace the below code in the file

<?xml version="1.0" encoding="UTF-8"?>

<tomcat-users xmlns="http://tomcat.apache.org/xml"
              xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
              xsi:schemaLocation="http://tomcat.apache.org/xml tomcat-users.xsd"
              version="1.0">

  <!-- Roles -->
  <role rolename="manager-gui"/>
  <role rolename="manager-script"/>
  <role rolename="manager-jmx"/>
  <role rolename="manager-status"/>

  <!-- Users -->
  <!-- User for Jenkins deployments -->
  <user username="deployer" password="deployer123" roles="manager-script"/>

  <!-- User for browser access to /manager/html -->
  <user username="admin" password="admin123" roles="manager-gui,manager-status"/>

</tomcat-users>

*Open Context.xml in tomcatfolder -> webapps -> Meta-inf -> Context.xml
*Remove the below line in the file 

<Valve className="org.apache.catalina.valves.RemoteAddrValve"
       allow="127\.\d+\.\d+\.\d+|::1|0:0:0:0:0:0:0:1" />

*Save and open browser enter "http://localhost:8081/manager/html"
*username : admin
*password : admin123
*Tomcat opens it means Success

------------------------------------------------------------------------

step 4 :

*create a new item in Jenkins
*project name -> Freestyle project
*save without any edit
*click build now
*On console output there is a workspace folder path
*on that folder paste all my program file given in rar file

------------------------------------------------------------------------

Step 5 :

*Open cmd as administrator
*Enter "mvn -v"
*It shows the version of maven in your system
*Then copy the program folder path and Paste in cmd like ( cd "C:\ProgramData\Jenkins\.jenkins\workspace\Sample_demo" )
*Then enter " mvn clean package "
*It will create a war file 

------------------------------------------------------------------------

step 6 :

*Go to Jenkins 
*Manage plugins -> Available plugins -> Deploy to container 
*Install the above plugin
*go to project configure settings
*look for Post-build Actions

------------------------------------------------------------------------

step 7 : 

*After providing all information 
*click build now 
*wait for console output
*if success open a new tab and enter "http://localhost:8081/Sample"
*The message will be displayed as "HTML deployed via Jenkins to Tomcat and Succesfully runned".

------------------------------------------------------------------------



