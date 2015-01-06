# Eclipse(STS) #
### optimization ###
	-Xverify:none
	-XX:+UseParallelGC
	-XX:+AggressiveOpts
	-XX:-UseConcMarkSweepGC
	-XX:PermSize=128M
	-XX:MaxPermSize=128M
	-XX:MaxNewSize=128M
	-XX:NewSize=128M
	-Xms1024M
	-Xmx1024M 
	
	Window > Perference > General - Show heap status opetion On
	Window > Prereces > General > Editors > Spellings - Encable spell checking Off
	Window > Preferences > Java > Editor > Save Actions - Organzize imports On
	Window > Preferences > Java > Editor > Content Assist - Enable auto activation off
	Window > Preferences > General > Appearance > Colors and Font > Basic > Text - Font Set
===================
#Maven
### Tomcat Deploy ###
#### "tomcat-users.xml" Add User, role ####
	<role rolename="manager-gui"/>
	<role rolename="manager-script"/>
	<user username="user1" password="pass1" roles="manager-gui,manager-script"/>
	
#### "pom.xml" Add "tomcat-maven plugin" ####
	<plugin>
	<groupId>org.apache.tomcat.maven</groupId>
	<artifactId>tomcat7-maven-plugin</artifactId>
	<version>2.2</version>
	<configuration>
	<path>/</path>
	<url>http://localhost:8080/manager/text</url>
	<username>user1</username>
	<password>pass1</password>
	</configuration>
	</plugin>
	
#### mvn Run ####
	mvn tomcat7:redeploy
	
### Pom Optimization ###
	mvn help:effective-pom
#Nginx
+ Tomcat Proxy
+ MP4 module

#Tomcat

#Git
+ public : GitHub
+ private : Bitbucket

#Vagrant
+ http://www.vagrantbox.es

#### INSTALL
1. Oracle VM Virtual Box install
2. vagrant init [Title] [URL or Path]
3. vagrant up

#SonarQube
+ http://www.sonarqube.org/

#Jenkins
+ http://jenkins-ci.org/
+ Install Tomcat, and Deploy
