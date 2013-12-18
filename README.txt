Instructions File
*******************
1. Versioning
*******************

1.0. -Deployment instructions on Zendesk, Luis Oscar Mendoza Guzmán - 18122013

*******************
2. Virtual Education Platform
*******************

Package - efront_3.6.14_build18012_community

*******************
3. Deployment
*******************
For deployment on Zendesk server you have to make this

1. Create a new folder where you can copy the files
2. Open a CMD instance an execute the following instruction inside the new folder to create the structure
of the deployment

	zdpack.exe create learn

3. Go inside the "learn" Folder and edit the "deployment.xml" file
Set the following values like this ad

  <version>
      <release>1.0</release>
  </version>
  <directive>
	  <name>memory_limit</name>
	  <min>128M</min>
  </directive>

5. Go back in and execute the following command

	zdpack.exe validate c:\zendesk\learn\deployment.xml

6. Pack the application

	zdpack.exe pack learn

7. Deploy the application in the Zendesk Server

*******************

*******************
EOF