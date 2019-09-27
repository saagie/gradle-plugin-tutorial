# Gradle Plugin Demo

## V1 (Manager)
Code example available in `v1` folder.
### Configuration
After creating your job on Saagie using the manager UI, open the `saagie/build.gradle` file and fill in the correct properties :
* **saagie.server.url** = URL of your Saagie Platform (e.g. https://saagie-manager.prod.saagie.io/api/v1) 

Then for each environment, open the `saagie/gradle-<envname>.properties` and specify :

* **saagieEnvironment** =  ID of your environment (e.g. 1) 
* **saagieJob** =  uid of your job (e.g. 4041)

### Usage
Under the saagie directory : 

`gradlew packageCode -PenvironmentName=<envname>` to zip your Python code

`gradlew updateJob -PenvironmentName=<envname>` to update your job on Saagie (will first package your code)

`gradlew runJob -PenvironmentName=<envname>` to run your job on Saagie (will first update your job on Saagie)

## V2 (Project and job)
Code example available in `v2` folder.

### Configuration

After creating your job on Saagie using the P&J UI, open the `saagie/build.gradle` file and fill in the correct properties :
* **saagie.server.url** = URL of your Saagie Platform (e.g. https://saagie-beta.prod.saagie.io) 

Then for each environment, open the `saagie/gradle-<envname>.properties` and specify :

* **saagieEnvironment** =  ID of your environment (e.g. 1)
* **saagieProject** =  uid of your project (e.g. 051a99fb-6359-41dd-9b38-42c1ee1bfc75) 
* **saagieJob** =  uid of your job (e.g. 70488ff0-e562-471f-9af8-5d0feec34122)

### Usage

Under the saagie directory : 

`gradlew packageCode -PenvironmentName=<envname>` to zip your Python code

`gradlew projectsUpdateJob -PenvironmentName=<envname>` to update your job on Saagie (will first package your code)

`gradlew projectsRunJob -PenvironmentName=<envname>` to run your job on Saagie (will first update your job on Saagie)