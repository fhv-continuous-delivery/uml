# UML
UML diagram which is used to generate the application. It uses [Eclipse Papyrus](https://www.eclipse.org/papyrus/) as the UML editor.

# Stereotypes
The following stereotypes are needed in order to generate the corresponding code:
* Endpoint: Generates a REST service endpoint, can be applied on UML classes only
    * Write: Generates a POST method, can be applied on methods only
      * path: URL which is used to reach this method
    * Read: Generates a GET method, can be applied on methods only
      * path: URL which is used to reach this method
* Handler: Generates a handler which contains the business logic of the application, can be applied on UML classes only
* Model: Generates a database model, can be applied on UML classes only

# Build
## Local build
Run the following maven command to build the artifact locally:

```
mvn org.eclipse.acceleo:org.eclipse.acceleo.maven.launcher:acceleo-launcher
```

## Remote build
Travis CI app is used to build the application. The build needs the following environment variables set in order to work:
* TRAVIS_GITHUB_TOKEN: This is the token used to push the generated code to the Github repository