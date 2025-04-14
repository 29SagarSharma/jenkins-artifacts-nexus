Integrating jenkins with Nexus using jenkins-pipeline
Nexus= Nexus Repository Manager (by Sonatype) is a popular artifact repository manager, an artifact is any file generated as part of the build process that can be deployed or reused later.
![Uploading image.png…]()
![Uploading image.png…]() 

Frist, Setup the nexus on your system and launch it on port 8081/8082. Create a user and password then create a repository with maven(hosted 2) option because it is a java project. 
Second, on jenkins install the plugin name nexus-artifact-upoader then for create item choose pipeline in project, in pipleine option choose pipleine script from SCM provide the details and save. at last build it and artifacts will upload on nexus server.

Conclusion
Integrating Nexus with Jenkins Pipeline provides a streamlined approach to managing and deploying artifacts within a CI/CD workflow. By configuring Nexus as a repository for Jenkins, you can securely store and manage build artifacts, ensuring consistent deployment practices across environments.

This integration not only simplifies artifact management but also enhances the traceability and reliability of releases, making the development process more efficient and maintainable. Adopting Nexus in Jenkins Pipelines supports the automation and scalability essential for modern DevOps practices, contributing significantly to a robust, well-managed software delivery lifecycle.
