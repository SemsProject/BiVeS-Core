Build Bives-Core 
==================

When you've cloned the source code:

```sh
git clone https://github.com/SemsProject/BiVeS-Core
```

There are two supported options to build this project:

* [Build with Maven](#build-with-maven)
* [Build with Ant](#build-with-ant)


Build with Maven 
-----------------
[Maven](https://maven.apache.org/) is a build automation tool. We ship a `pom.xml`  together with the sources which tells maven about versions and dependencies. Thus, maven is able to resolve everything on its own and, in order to create the library, all you need to call is `mvn package`:

```sh
usr@srv $ mvn package

-------------------------------------------------------
 T E S T S
-------------------------------------------------------
Running de.unirostock.sems.bives.TestGraphs
Tests run: 2, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.113 sec
Running de.unirostock.sems.bives.TestCompare
Tests run: 2, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.086 sec
Running de.unirostock.sems.bives.TestSBO
Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.001 sec
Running de.unirostock.sems.bives.TestPatching
Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.048 sec

Results :

Tests run: 9, Failures: 0, Errors: 0, Skipped: 0
```

That done, you'll find the binaries in the `target` directory.

Build with Ant 
---------------

[Ant](https://ant.apache.org/) is an Apache tool for automating software build processes. There is a `build.xml` file included in the source code that tells ant what to do. Since ant is not able to resolve the dependencies you need to create a directory `lib` containing the following libraries:

* [xmlutils](http://sems.uni-rostock.de/trac/xmlutils/wiki) (download latest binary from [bin.sems.uni-rostock.de](http://bin.sems.uni-rostock.de) or see [sems.uni-rostock.de/trac/xmlutils/wiki//BuildXmlUtils](http://sems.uni-rostock.de/trac/xmlutils/wiki//BuildXmlUtils))
* [json-simple](https://code.google.com/p/json-simple/)

We defined multiple targets in the `build.xml`. They can be displayed by calling `ant -p`:

```sh
usr@srv $ ant -p
Buildfile: /path/to/BiVeS-Core/build.xml

        BiVeS - BioModel Version Control System
        This package provides core functionality
    
Main targets:

 clean    clean up
 compile  compile the source
 dist     generate the distribution
 init     initialize workspace
 sign     sign a dist
Default target: dist
```

* `clean up` will delete all compiled files and produced libraries
* `compile` compiles the source code
* `dist` bundles all compiled binaries into a jar library

For example, to create the jar library just run `ant dist`:

```sh
usr@srv $ ant dist
Buildfile: /path/to/BiVeS-Core/build.xml

init:
    [mkdir] Created dir: /path/to/BiVeS-Core/build
    [mkdir] Created dir: /path/to/BiVeS-Core/dist

compile:
    [javac] Compiling 53 source files to /path/to/BiVeS-Core/build

dist:
      [jar] Building jar: /path/to/BiVeS-Core/dist/BiVeS-Core-1.2.7.jar
      [jar] Building jar: /path/to/BiVeS-Core/dist/BiVeS-Core-1.2.7-fat.jar

BUILD SUCCESSFUL
Total time: 2 seconds
```
