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

Instructions to run the application...




