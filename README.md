Develop_Tool-Server
===================

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
	
#Maven
+ Tomcat Deploy

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
