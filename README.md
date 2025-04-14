Integrating jenkins with Nexus using jenkins-pipeline
Nexus= Nexus Repository Manager (by Sonatype) is a popular artifact repository manager, an artifact is any file generated as part of the build process that can be deployed or reused later.
![Uploading image.png…]()
![Uploading image.png…]() 

Frist, Setup the nexus on your system and launch it on port 8081/8082. Create a user and password then create a repository with maven(hosted 2) option because it is a java project. 
Second, on jenkins install the plugin name nexus-artifact-upoader then for create item choose pipeline in project, in pipleine option choose pipleine script from SCM provide the details and save. at last build it and artifacts will upload on nexus server.
