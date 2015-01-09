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
	mvn help:effective-pom -Doutput=out.txt
	
#Nginx
### Tomcat Proxy###
	upstream tomcat {
		server 127.0.0.1:38080;
	

	location / {
	         proxy_redirect     off;
	         proxy_set_header   Host             $host;
	         proxy_set_header   X-Real-IP        $remote_addr;
	         proxy_set_header   X-Forwarded-For  $remote_addr;
	         proxy_set_header   Proxy-Client-IP  $proxy_add_x_forwarded_for;
	         proxy_pass http://tomcat;
		index  index.jsp;
		}
### MP4 module###
	location /mp4/ {
          mp4;
          mp4_buffer_size 100M;
          mp4_max_buffer_size 2000M;
          alias   "G:/MP4/";
        }


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
 
#JConsole
+ JAVAHOME/bin/jconsole.exe
+ Session Monitor : MBeans/Catalina/Manager/Host/Attribute - activeSessions
###Tomcat add option###
	-Dcom.sun.management.jmxremote
	-Dcom.sun.management.jmxremote.port=8999
	-Dcom.sun.management.jmxremote.ssl=false
	-Dcom.sun.management.jmxremote.authenticate=false

#JvisualVM
+ JAVAHOME/bin/jvisualvm.exe
+ Real Process Status Monitoring


