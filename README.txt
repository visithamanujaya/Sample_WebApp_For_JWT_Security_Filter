# Sample_WebApp_For_JWT_Security_Filter

This Web Application is a sample to demonstrate the sort of applications that can be filtered by JWT Security Filter. In this application there are three simple web pages called Admin page, HR page and Marketing page. And also we have defined four types of user roles to use this application, they are admin, hrOfficer, marketingOfficer and other. Admin users can use all three web pages, HR users are allowed only to use HR page like wise Marketing people are allowed to use only Marketing page.

Running sample WebApp in your system

Prerequisites 

1. maven 3.x.x
2. Tomcat 7 or above
3. Application Source code

How to configure

1. Go to your source code location where pom.xml is located by terminal and build the code using maven (mvn clean install). Then .War file will be crated inside the Target folder.

2. Next go to Tomcat_home / config / tomcat-users.xml and add these users and roles as follow.

	<user username="admin" password="admin" roles="manager-gui,admin gui,admin"/>
	<user username="hr" password="hr" roles="HROfficer"/>
	<user username="mkt" password="mkt" roles="MarketingOfficer"/>
	<user username="mktandhr" password="mktandhr" roles="HROfficer,MarketingOfficer"/>
	<user username="other" password="other" roles="other"/>

3. Then Start The Tomcat server and deploy the application.

4. Try to log in to different pages using give set of user names and passwords.
