This project is a fork based on the Java11-template that you can
find [here](https://github.com/openfaas/templates/tree/master/template/java11)

## Template: java17

The Java17 template uses gradle as a build system.

Gradle version: 8.0

The entrypoint library has been updated to use jetty as a server backend.
Both model and entrypoint has been upgraded to java17 and gradle 8
### Structure

There are three projects which make up a single gradle build:

- model - (Library) classes for parsing request/response
- function - (Library) your function code as a developer, you will only ever see this folder
- entrypoint - (App) HTTP server for re-using the JVM between requests

### Handler

The handler is written in the `./src/main/Handler.java` folder

Tests are supported with junit via files in `./src/test`

### External dependencies

External dependencies can be specified in ./build.gradle in the normal way using maven central, a local JAR or some other
remote repository.

