# salesforce-metadata-backup
## @Author: Bhoopender Pal Singh
## @License: GPL-3.0

###
### This utility backs up all the specified metadata from a Salesforce Org and generates a package.xml.
###

**What are the required Third Party Software?**
1. Oracle Java
2. Apache Ant
3. ant-salesforce.jar

	Place this jar in Ant's 'lib' directory. This jar is also checked-in with this project in 'ant-libs' directory.	
4. ant-contrib-1.0b3.jar

	Place this jar in Ant's 'lib' directory. This jar is also checked-in with this project in 'ant-libs' directory.
	
	
**How to Run?**
1. Open terminal (command prompt) and switch to your base directory of this project i.e. where you placed:

	build.xml
	
	build.properties
2. Configure build.properties

	Specify your preferences *e.g. Target Directory, SFDC API Version, Org Credentials, Desired Metadata to backup, Org Login URL*.
3. Execute

	Just type *ant* on the terminal and hit *ENTER* key.
4. This will download all specified metadata and create a *package.xml* in the specified target directory.


**What platforms/software versions this is tested on?**

This project has been tested on below versions but that doesn't mean just limited to run on these only:
1. Oracle Java

	java version "1.8.0_131"
	
	Java(TM) SE Runtime Environment (build 1.8.0_131-b11)
	
	Java HotSpot(TM) Client VM (build 25.131-b11, mixed mode, sharing)
2. Apache Ant

	Apache Ant(TM) version 1.9.7	
3. Operating System

	Windows 8.1 Pro
	
	***Note: This should run on other operating systems as well where Oracle Java is supported e.g. Linux, Ubuntu, Mac etc.***
