# Build tools

Multi module project with the following structure:

jar<--admin\

		|----services --- utils 

war<-- web/

## Prerequisites

Please ensure you have the following installed on your system:

- Java JDK 11 (or above)
- Apache Maven 3.8.3 (or above)
- Gradle 7.3 (or above)

## Building the project

### Building with Maven

Navigate to the directory containing the parent `pom.xml` file. Run the following command:

```bash
mvn clean install
```

This will compile the source code, execute tests, and package the resulting binaries in `.jar` (for `admin` module) and `.war` (for `web` module) files within the respective `target` directories.

### Building with Gradle

Navigate to the directory containing the parent `build.gradle` file. Run the following command:

```bash
gradle clean build
```

This will do similar steps as with Maven, but the built files will be located in the respective `build/libs` directories.

## Running the Application

After building the project, you should have the following artifact files available:

- A `*.jar` file in the target directory of the `admin` module.
- A `*.war` file in the target directory of the `web` module.

## Running the Admin Module

You can run the `admin` module by executing the following command:

```bash
java -jar admin/target/admin-1.0-SNAPSHOT.jar
```

## Running the Web Module
The war file generated after building the web module can be deployed to a Java servlet container. Here are brief instructions to do it with Apache Tomcat:

1. Download Apache Tomcat from the official page.
2. Extract the downloaded file to a location of choice. This location is referred to as CATALINA_HOME.
3. Copy the web.war file to the webapps directory located in CATALINA_HOME.
4. Run the startup script located in the bin folder (startup.sh or startup.bat depending on your operating system). For Unix-based systems, you might need to make the script executable by running chmod +x startup.sh.
Your application should be accessible at http://localhost:8080/web.
5. The port and context path could be different depending on your configuration



