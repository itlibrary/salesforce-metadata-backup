# salesforce-metadata-backup
## @Author: Bhoopender Pal Singh
## @License: GPL-3.0

###
### This utility backs up all the specified metadata from a Salesforce Org and generates a package.xml.
###
	

**Have you ever encountered with any of below limitations while using Salesforce Ant migration tool?**
1. Backup entire Salesforce Org metadata in one go when not having package.xml already
2. Backup multiple specified Salesforce Org metadata in one go when not having package.xml already
3. Backup folder structure-based Salesforce Org metadata also i.e. Dashboard, Document, Email Templates and Reports without asking for any additional information

If yes, then relax, here is the way to do it locally i.e. on your own computer. You can now use this utility to address all above needs.

You can specify what metadata you want to backup including folder structure-based metadata as well, for example - Dashboard, Document, Email Templates and Reports. This can also be scheduled as needed through some batch file or any other supported script on your Operating System. The backup process also creates a package.xml which lists all metadata downloaded.


**How to Run?**
1. Open terminal (command prompt) and switch to your base directory of this project i.e. where you placed:

	build.xml
	
	build.properties
2. Configure build.properties

	Specify your preferences *e.g. Target Directory, SFDC API Version, Org Credentials, Desired Metadata to backup, Org Login URL*.
3. Execute

	Just type *ant* on the terminal and hit *ENTER* key.
4. This will download all specified metadata and create a *package.xml* in the specified target directory.

5. To watch the Demo, please click on below thumbnail

   <a href="http://www.youtube.com/watch?feature=player_embedded&v=akaVaOe3wLk" target="_blank"><img src="http://img.youtube.com/vi/akaVaOe3wLk/0.jpg" alt="Salesforce Metadata Backup" width="240" height="180" border="10" /></a>


**What are the required Third Party Software?**
1. Oracle Java
2. Apache Ant
3. ant-salesforce.jar

	Place this jar in Ant's 'lib' directory. This jar is also checked-in with this project in 'ant-libs' directory.	
4. ant-contrib-1.0b3.jar

	Place this jar in Ant's 'lib' directory. This jar is also checked-in with this project in 'ant-libs' directory.


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

**FAQ**
1. Can it download more than one type of metadata in one go?

	Yes, you can specify as many metadata types as you want in the build.properties file.

2. Can it download folder structure-based metadata also, for example - Dashboard, Document, Email Templates and Reports?

	Yes, you just have to specify the metadata type in the build.properties file.

3. Does downloading folder structure-based metadata, for example - Dashboard, Document, Email Templates and Reports - require to provide any additional information e.g. name or folder etc.?

	No, this utility requires no additional information to be specified.

4. Does it create a package.xml also?

	Yes.

5. Does it download packaged components as well?

	Yes.

6. Does this also work fine for Salesforce Org having huge number of components?

	Yes. The number of polling attempts to be performed before aborting can be fine tuned in build.properties file against ‘sf.maxPoll’ property. Currently this is set as 200 i.e. maximum 200 poll attempts will be made before aborting. Time interval between poll attempts is 10 seconds.
