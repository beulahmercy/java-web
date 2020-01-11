### Spring Boot + JDK 12 + Maven + Mongo DB

using https://start.spring.io to set up project
* Group
```java
 com.example
```
* Artifact
```java
 demo
```
* Dependencies
```java
 spring web, spring data mongodb
```
Download the project and unzip it. Then import it into your favorite IDE – Eclipse or IntelliJ IDEA.

#### Maven pom.xml
##### sprint-boot-starter-parent
The spring-boot-starter-parent project is a special starter project – that provides default configurations for our application and a complete dependency tree to quickly build our Spring Boot project.

It also provides default configuration for Maven plugins such as maven-failsafe-plugin, maven-jar-plugin, maven-surefire-plugin, maven-war-plugin.

```java
<parent>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-parent</artifactId>
	<version>2.3.0.BUILD-SNAPSHOT</version>
	<relativePath/> <!-- lookup parent from repository -->
</parent>
```
##### dependency for spring web and mongodb
```java

<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-data-mongodb-reactive</artifactId>
</dependency>
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-web</artifactId>
</dependency>

```
#### Build and Run

mvn package or mvn install
 install all the dependency defined in pom.xml
 package a jar based on the settings in pom.xml

#### Run Spring Boot app with java -jar command
```java
java -jar target/demo-0.0.1-SNAPSHOT.jar
```
build jar can be found in the following path of your project
```java
[INFO] --- maven-jar-plugin:3.2.0:jar (default-jar) @ demo ---
[INFO] Building jar: <PATH>\demo\target\demo-0.0.1-SNAPSHOT.jar
```
#### Run Spring Boot app using Maven
```java
mvn spring-boot:run
```
