# Maven (Basic Example)
## Overview
A basic example of a java project with maven to illustrate why maven is used. 

For smaller projects you can add dependcies manually (ie. a database connector .jar). Larger projects will require many more and adding them manually is a problem. 

For example - adding Spring. You *could* go to the site, download the .jar files etc. But that sucks. Maven solves this. It allows you to simply mention somewhere in your project "Hey I need *xyz library*" then goes and gets it for you.

***Why use Maven:*** dependency management

## Requirements
- JDK
- Maven
- Eclipse IDE 

## Steps:

1. Open Eclipse
    - *File > New > Maven Project* (use the *Internal* catalogue to narrow it down)
    - Choose the appropriate *Archetype* 
    - Group Id: com.demo.maven
    - Artifact Id: addDependencyExample
    - click *Finish* 

    NOTE: for this we'll be using [maven-archetype-quickstart](https://maven.apache.org/archetypes/maven-archetype-quickstart/) but you can chose whichever you need
    
    See [this maven intro](https://maven.apache.org/guides/introduction/introduction-to-archetypes.html) or [this video](https://www.youtube.com/watch?v=28fsqKNjxrc) for more info

1. Take a look around at the file structure, note the following:
    - src/main/java
    - src/test/java
    - pom.xml
    - Maven Dependencies folder 

    At this point the *Maven Dependencies* folder just contains a `j-unit-X.X.X.jar`

1. Add a dependency in the `pom.xml`
    - open up the `pom.xml`
    - go to the [Maven Repo](https://mvnrepository.com/) and search for a dependency you'd like to add (ie. MySQL connector)
    - copy the dependency tag and paste it into the pom.xml in the `<dependencies>` block

1. Save and it should rebuild automatically. Look in your *Maven Dependencies* folder and make sure it's there. 