# Lab Setup for Spring Course

You are welcome to use your own set of developer tools, deployment servers and IDE. In this class we assume you will use the following:
* Windows, MacOS or Linux environment (64-bit)
* Eclipse IDE for Java EE Developers
* Apache Tomcat
* HSQL database (using [hsqldb-runner] (https://github.com/javaclinic/hsqldb-runner) project)

## Requirements
* Downloaded and installed latest JDK, e.g. http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
> *NOTE**: If you are using your existing JDK, please make sure it is at least JDK7 (i.e. JDK 1.7.0_XX)
* Downloaded and installed latest Eclipse IDE for Java EE Developers, e.g. https://eclipse.org/downloads/packages/eclipse-ide-java-ee-developers/lunasr1
> *NOTE**: If you are using your existing Eclipse, please make sure it is "**Eclipse IDE for Java EE Developers**" and at least **Luna** edition.
* Downloaded latest Apache Tomcat 8.x, e.g. http://tomcat.apache.org/download-80.cgi (ZIP version)
> **NOTE**: You can also use Apache Tomcat 7.x version.

## Installation and Configuration - Windows

### JDK Installation
1. Make sure you have downloaded the latest JDK, e.g. `jdk-8u25-windows-x64.exe`
2. Double click on the `jdk-8u25-windows-x64.exe` file to start the JDK8 installation process.
3. Follow the installation steps:
![Step 1](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_01.png)
![Step 2](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_02.png)
![Step 3](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_03.png)
![Step 4](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_04.png)
![Step 5](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_05.png)
![Step 6](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_06.png)
![Step 7](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_07.png)

### JDK Configuration


### Eclipse Installation
1. Make sure you have downloaded the latest Eclipse IDE for Java EE Developers, e.g. `eclipse-jee-luna-SR1-win32-x86_64.zip`
2. Pick a folder where you want to install your Eclipse IDE, the shorter path, the better, e.g. `C:\training`
3. Unpack `eclipse-jee-luna-SR1-win32-x86_64.zip` into destination folder, e.g. `C:\training`
4. Make sure you know the path to the Eclipse binary, e.g. `C:\training\eclipse\eclipse.exe`
5. Create a shortcut on the desktop for this Eclipse binary.
6. That's it for **Eclipse Installation**

### Apache Tomcat Installation
1. Make sure you have downloaded the latest Apache Tomcat 8.x, e.g. `apache-tomcat-8.0.15.zip`
2. Pick a folder where you want to install your Apache Tomcat, e.g. `C:\training`
3. Unpack `apache-tomcat-8.0.15.zip` into destination folder, e.g. `C:\training`
4. Check the directory structure, e.g. 
```
C:\training\
C:\training\apache-tomcat-8.0.15\
C:\training\apache-tomcat-8.0.15\bin
C:\training\apache-tomcat-8.0.15\conf
C:\training\apache-tomcat-8.0.15\lib
C:\training\apache-tomcat-8.0.15\logs
C:\training\apache-tomcat-8.0.15\temp
C:\training\apache-tomcat-8.0.15\webapps
C:\training\apache-tomcat-8.0.15\work
```
5. That's it for **Apache Tomcat Installation**

### HSQL database Installation
Soon.

## Installation and Configuration - MacOS
Soon.

## Installation and Configuration - Linux
Soon.
