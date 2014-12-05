# Lab Setup Configuration for MacOS Environment

The lab setup configuration has the following main steps:
* JDK Installation
* JDK Configuration
* Eclipse Installation
* Tomcat Installation
* Tomcat Configuration in Eclipse
* HSQL Database Installation


## JDK Installation
1. Make sure you have downloaded the latest JDK, e.g. `jdk-8u25-macosx-x64.dmg`

2. Open `jdk-8u25-macosx-x64.dmg` file to mount the image file.

3. Double click on `JDK 8 Update 25.pkg` file.

  ![Step 1](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/mac_java_01.png)

4. Follow the installation steps. Click on `Continue`.

  ![Step 2](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/mac_java_02.png)

5. Choose the installation destination. Click on `Continue`.

  ![Step 3](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/mac_java_03.png).

6. Confirm installation type, e.g. `Standard Install`. Click on `Install`.

  ![Step 4](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/mac_java_04.png).

7. Confirm your username (with admin privileges). Click on `Install Software`.

  ![Step 5](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/mac_java_05.png).

8. Wait for few moments/minutes for the installation process to finish.

  ![Step 6](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/mac_java_06.png)

9. Confirm that installation was successful. Click on `Close`.

  ![Step 7](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/mac_java_07.png)

10. That's it for **JDK Installation**.


## JDK Configuration
1. MacOS will take care of JDK installation and configuration.

2. Let's configure `$JAVA_HOME`  environment variable for all our programs. Edit `~/.bash_profile` file. Add a line:

    ```
    export JAVA_HOME="`/usr/libexec/java_home -v 1.8`"
    ```

3. Open new terminal window. Test if JDK has been properly installed, e.g. `java -version` and `javac -version`:

    ```
    user@localhost:~$ java -version
    java version "1.8.0_25"
    Java(TM) SE Runtime Environment (build 1.8.0_25-b17)
    Java HotSpot(TM) 64-Bit Server VM (build 25.25-b02, mixed mode)
    user@localhost:~$ javac -version
    javac 1.8.0_25
    ```

4. That's it for **JDK Configuration**.


## Eclipse Installation
1. Make sure you have downloaded the latest Eclipse IDE for Java EE Developers, e.g. `eclipse-jee-luna-SR1-macosx-cocoa-x86_64.tar.gz`

2. Pick (or create) a folder where you want to install your Eclipse IDE, the shorter path, the better, e.g.

    ```
    mkdir ~/training
    ```

3. Change directory into the destination folder, e.g.

    ```
    cd ~/training
    ```

4. Unpack `eclipse-jee-luna-SR1-macosx-cocoa-x86_64.tar.gz`, e.g.

    ```
    tar zxvf eclipse-jee-luna-SR1-macosx-cocoa-x86_64.tar.gz
    ```

5. (Optional) Link to your `/Applications` folder, e.g.

    ```
    ln -s ~/eclipse/Eclipse.app /Applications
    ```

6. (Optional) Link to your binary folder, e.g.

    ```
    sudo ln -s ~/eclipse/Eclipse.app/Contents/MacOS/eclipse /bin/eclipse
    ```

7. That's it for **Eclipse Installation**.


## Tomcat Installation
1. Make sure you have downloaded the latest Apache Tomcat 8.x, e.g. `apache-tomcat-8.0.15.zip`

2. Pick a folder where you want to install your Apache Tomcat, e.g. `~/training`

3. Change directory into the destination folder, e.g.

    ```
    cd ~/training
    ```

4. Unpack `apache-tomcat-8.0.15`, e.g.

    ```
    unzip apache-tomcat-8.0.15.zip
    ```

5. Check the directory structure, e.g. 

    ```
    ~/training/
    ~/training/apache-tomcat-8.0.15/
    ~/training/apache-tomcat-8.0.15/bin
    ~/training/apache-tomcat-8.0.15/conf
    ~/training/apache-tomcat-8.0.15/lib
    ~/training/apache-tomcat-8.0.15/logs
    ~/training/apache-tomcat-8.0.15/temp
    ~/training/apache-tomcat-8.0.15/webapps
    ~/training/apache-tomcat-8.0.15/work
    ```

6. That's it for **Tomcat Installation**.


## Tomcat Configuration in Eclipse
1. Click on the `Servers` tab and on the link `No servers available. Click this link to create a new server...`

  ![Step 1](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/mac_eclipse_tomcat_configuration_01.png)

2. Under `Apache` select `Tomcat v8.0 Server`. Click `Next`.

  ![Step 2](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/mac_eclipse_tomcat_configuration_02.png)

3. Type in the directory where you installed Tomcat in earlier steps, e.g. `~/training\apache-tomcat-8.0.15`. Click `Next`.

  ![Step 3](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/mac_eclipse_tomcat_configuration_03.png)

4. There are no applications to deploy at the moment. Click `Finish`.

  ![Step 4](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/mac_eclipse_tomcat_configuration_04.png)

5. In the `Servers` tab, there should be a new server installed, e.g. `Tomcat v8.0 Server at localhost`. Double click on the server, server configuration options will open. Please update `Server Locations` and use "middle option", e.g. `Use Tomcat installation (takes control of Tomcat installation)`. Save the file, e.g. `CTRL+s`.

  ![Step 5](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/mac_eclipse_tomcat_configuration_05.png)

6. Right click on the server and select `Start`.

  ![Step 6](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/mac_eclipse_tomcat_configuration_06.png)

7. (Optional) Your windows firewall might pop up and ask to allow server process to bind to a listening port. Click `Allow`.

  ![Step 7](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/mac_eclipse_tomcat_configuration_07.png)

8. Notice the `Console` tab and observe the console output. You should see a message indicating your server is up and running.

  ![Step 8](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/mac_eclipse_tomcat_configuration_08.png)

9. Open up browser view, and type in the address, e.g. `http://localhost:8080`

  ![Step 9](https://raw.github.com/javaclinic/lab-setup-spring/master/screenshots/mac_eclipse_tomcat_configuration_09.png)

10. That's it for **Tomcat Configuration in Eclipse**.


## HSQL database Installation
We will configure this at the beginning of the class.

