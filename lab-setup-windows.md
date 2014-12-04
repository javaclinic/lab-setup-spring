# Lab Setup Configuration for Windows Environment

The lab setup configuration has the following main steps:
* JDK Installation
* JDK Configuration
* Eclipse Installation
* Tomcat Installation
* Tomcat Configuration in Eclipse
* HSQL Database Installation

## JDK Installation
1. Make sure you have downloaded the latest JDK, e.g. `jdk-8u25-windows-x64.exe`
2. Double click on the `jdk-8u25-windows-x64.exe` file to start the JDK8 installation process. Follow the installation steps.
3. Click on `Next`.
![Step 1](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_01.png)
4. If you don't want to change default JDK installation directory, skip next two steps. If you prefer to change default location, click on `Change`.
![Step 2](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_02.png)
5. Update the installation directory, e.g. `C:\dev\java\jdk1.8.0_25`
![Step 3](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_03.png)
![Step 4](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_04.png)
6. Confirm the installation directory has been updated, click on `Next`.
![Step 5](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_05.png)
7. Wait for few moments/minutes for the installation process to finish.
![Step 6](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_06.png)
8. Confirm that installation was successful. Click on `Close`.
![Step 7](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_07.png)
9. That's it for **JDK Installation**.

## JDK Configuration
1. Let's configure JDK for all our programs, including Eclipse or command-line tools. Click on `Start`, right-click on `Computer`, click on `Properties`. Click on `Advanced system settings`.
![Step 1](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_config_01.png)
2. Click on `Environment Variables...`
![Step 2](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_config_02.png)
3. Under `System Variables`, click on `New`.
![Step 3](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_config_03.png)
4. Let's configure new variable with name `JAVA_HOME` and value `C:\dev\java\jdk1.8.0_25` (or wherever you installed your JDK) earlier. Click `OK`.
![Step 4](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_config_04.png)
5. Confirm that new system variable has been configured properly, e.g. `JAVA_HOME`.
![Step 5](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_config_05.png)
6. Let's update system variable with name `Path`. Add at the beginning of the variable the following `%JAVA_HOME%\bin;` (notice semicolon at the end)
![Step 6](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/java_config_06.png)
7. Click `OK`.
8. Click `OK`.
9. Open command prompt. Test if JDK has been properly installed, e.g. `java -version` and `javac -version`:
    ```
    Microsoft Windows [Version 6.1.7601]
    Copyright (c) 2009 Microsoft Corporation.  All rights reserved.
    
    C:\Users\Admin>java -version
    java version "1.8.0_25"
    Java(TM) SE Runtime Environment (build 1.8.0_25-b18)
    Java HotSpot(TM) 64-Bit Server VM (build 25.25-b02, mixed mode)
    
    C:\Users\Admin>javac -version
    javac 1.8.0_25
    
    C:\Users\Admin>
    ```
10. That's it for **JDK Configuration**.

## Eclipse Installation
1. Make sure you have downloaded the latest Eclipse IDE for Java EE Developers, e.g. `eclipse-jee-luna-SR1-win32-x86_64.zip`
2. Pick a folder where you want to install your Eclipse IDE, the shorter path, the better, e.g. `C:\training`
3. Unpack `eclipse-jee-luna-SR1-win32-x86_64.zip` into destination folder, e.g. `C:\training`
4. Make sure you know the path to the Eclipse binary, e.g. `C:\training\eclipse\eclipse.exe`
5. Create a shortcut on the desktop for this Eclipse binary.
6. That's it for **Eclipse Installation**.

## Tomcat Installation
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
5. That's it for **Tomcat Installation**.

## Tomcat Configuration in Eclipse
1. Click on the `Servers` tab and on the link `No servers available. Click this link to create a new server...`
  ![Step 1](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/eclipse_tomcat_configuration_01.png)
2. Under `Apache` select `Tomcat v8.0 Server`. Click `Next`.
  ![Step 2](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/eclipse_tomcat_configuration_02.png)
3. Type in the directory where you installed Tomcat in earlier steps, e.g. `C:\training\apache-tomcat-8.0.15`. Click `Next`.
  ![Step 3](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/eclipse_tomcat_configuration_03.png)
4. There are no applications to deploy at the moment. Click `Finish`.
  ![Step 4](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/eclipse_tomcat_configuration_04.png)
5. In the `Servers` tab, there should be a new server installed, e.g. `Tomcat v8.0 Server at localhost`. Double click on the server, server configuration options will open. Please update `Server Locations` and use "middle option", e.g. `Use Tomcat installation (takes control of Tomcat installation)`. Save the file, e.g. `CTRL+s`.
  ![Step 5](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/eclipse_tomcat_configuration_05.png)
6. Right click on the server and select `Start`.
    ![Step 6](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/eclipse_tomcat_configuration_06.png)
7. (Optional) Your windows firewall might pop up and ask to allow server process to bind to a listening port. Click `Allow access`.
  ![Step 7](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/eclipse_tomcat_configuration_07.png)
8. Notice the `Console` tab and observe the console output. You should see a message indicating your server is up and running.
  ![Step 8](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/eclipse_tomcat_configuration_08.png)
9. Open up browser view, and type in the address, e.g. `http://localhost:8080`
  ![Step 9](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/eclipse_tomcat_configuration_09.png)
10. That's it for **Tomcat Configuration in Eclipse**.


## HSQL database Installation
We will configure this at the beginning of the class.


