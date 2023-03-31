# simple-java-maven-app

This repository is for the
[Build a Java app with Maven](https://jenkins.io/doc/tutorials/build-a-java-app-with-maven/)
tutorial in the [Jenkins User Documentation](https://jenkins.io/doc/).

The repository contains a simple Java application which outputs the string
"Hello world!" and is accompanied by a couple of unit tests to check that the
main application works as expected. The results of these tests are saved to a
JUnit XML report.

The `jenkins` directory contains an example of the `Jenkinsfile` (i.e. Pipeline)
you'll be creating yourself during the tutorial and the `scripts` subdirectory
contains a shell script with commands that are executed when Jenkins processes
the "Deliver" stage of your Pipeline.

java-maven-junit-hello
===========================

A „Hello World!” sample written in Java using Maven for the build, that showcases a few very simple tests.

This example demonstrates:

* Unit tests written with [JUnit 4](http://junit.org/)
* Unit test using [PowerMockito](https://code.google.com/p/powermock/) to mock classes and test `System.exit()`
* Integration tests written with [JUnit 4](http://junit.org/)
* Integration test using [system-rules](http://www.stefan-birkner.de/system-rules/) to test `System.out`
* Code coverage reports via [Cobertura](http://cobertura.github.io/cobertura/)
* A Maven build that puts it all together

Running the tests
-----------------

* To run the unit tests, call `mvn test`
* To run the integration tests as well, call `mvn verify`
* To generate (unit test) code coverage reports, call `mvn cobertura:cobertura`, and point a browser at the output in `target/site/cobertura/`

Conventions
-----------

This example follows the following basic conventions:

 | unit test | integration test
--- | --- | ---
__resides in:__ | `src/test/java/*Test.java` | `src/test/java/*IT.java`
__executes in Maven phase:__ | test | verify
__handled by Maven plugin:__ | [surefire](http://maven.apache.org/surefire/maven-surefire-plugin/) | [failsafe](http://maven.apache.org/surefire/maven-failsafe-plugin/)
