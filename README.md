# Archetype for the accelerate-aqe framework

## Installation

To build and install your archetype, run:

```
mvn clean install
```


## Using the archetype

Once your archetype has been installed and the jar is available to maven, simply
change into the directory where you want to place the directory structure and
run:

```bash

mvn archetype:generate                           \
  -DarchetypeGroupId=com.liatrio.accelerate      \
  -DarchetypeArtifactId=accelerate-aqe-archetype \
  -DarchetypeVersion=1.0-SNAPSHOT                \
  -DgroupId=<my.groupid>                         \
  -DartifactId=<my-artifactId>

```

This will create the following directory structure in your current directory.

```
    <my-artifactId>
    ├── Jenkinsfile
    ├── README.md
    ├── pom.xml
    ├── quality_engineering
    │   ├── services
    │   │   ├── pom.xml
    │   │   └── src
    │   │       └── test
    │   │           └── java
    │   │               ├── examples
    │   │               │   ├── ExamplesTest.java
    │   │               │   └── users
    │   │               │       ├── UsersRunner.java
    │   │               │       └── users.feature
    │   │               ├── karate-config.js
    │   │               └── logback-test.xml
    │   └── ui
    │       ├── pom.xml
    │       └── src
    │           └── test
    │               ├── java
    │               │   └── stepDefintions
    │               │       ├── Hooks.java
    │               │       ├── RunCukeTest.java
    │               │       └── UserStepDefinitions.java
    │               └── resources
    │                   └── features
    │                       └── my_first.feature
    └── sonar-project.properties
```

### The archetype structure

Assets that are include int the template are stored in
`src/main/resources/archetype-resources`. Metadata about the archetype package
itself like variables and other qualities are kept in `META-INF/maven`.


## More on creating archetypes

Maven's documentation on archetypes

https://maven.apache.org/archetype/index.html

A brief quickstart guide to creating marven archetypes.
https://maven.apache.org/guides/mini/guide-creating-archetypes.html

Here is a link to the maven documentation for including and building archetype
artifcats.

https://maven.apache.org/archetype/archetype-models/archetype-descriptor/archetype-descriptor.html
