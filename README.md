# Hello Windows
Notes self on creating a developer environment for myself in Windows 10.

This is primarily for setting up a dev environment for Java, MySQL, MariaDB.

### git
  0. Navigate to [https://git-scm.com/download/win](https://git-scm.com/download/win) for the Windows version of Git.
  1. Launch the .exe file after download and select your preferences/install.
  2. Open Git Bash after the installation is complete. I also recommend pinning it to the taskbar.
  3. Set up your github credentials using:
    `git config --global user.name "Your Name" && git config --global user.email "you@example.com"`
  4. When pushing your first commit, you will be asked to enter your github credentials.


### Sublime Text
  0. Navigate to [https://www.sublimetext.com/3](https://www.sublimetext.com/3) to download Sublime Text 3


### Java
  0. Navigate to [Oracle Java SE Downloads](http://www.oracle.com/technetwork/java/javase/downloads/index.html) and find the Windows x64 (or x86) verison.
  1. Download the .exe file and run it to install.
  2. Leave the the "Development Kit" selected during download. This gives you the [JDK](http://stackoverflow.com/questions/11547458/what-is-the-difference-between-jvm-jdk-jre-openjdk) (Java Development Kit).
  3. Open up GitBash (or the regular command line) and run `java -version` to ensure the download was successful.


### IntelliJ IDEA
  0. Navigate to [JetBrains IDEA](https://www.jetbrains.com/idea/) and download the IntelliJ IDEA Community edition for windows.
  1. During installation, you can refer to [Team Treehouse](http://treehouse.github.io/installation-guides/windows/intellij-idea-win.html) for the options to be selected.
  2. Opening IntelliJ for the first time, you may need to point the Project SDK to your previously downloaded Java 8 JDK.
    Using the folder selector, your JDK should be located at `C:\Program Files\Java\[JDK VERSION]`.


### Maven
  0. Navigate to [https://spring.io/guides/gs/maven/](https://spring.io/guides/gs/maven/) to learn to install and initialize Maven.
  1. After downloading the .zip file, I saved it at `C:\Program Files\Apache\apache-maven-3.5.0`.
  2. Then, I needed to set the path and environmental variables. You can refer to [this guide](https://www.mkyong.com/maven/how-to-install-maven-in-windows/).
  3. After the path is set, run `mvn -version` in Git Bash to verify the installation.
  4. Below are some (optional steps) to run the Java .class and .jar files created in the how-to for the webpage above:
      - After running `mvn compile` and `mvn package`, in the `initial` folder of the project...
        - Run the .class file using `java -cp target/classes hello.HelloWorld`
        - Run the .jar file using `java -cp target/gs-maven-0.1.0.jar package.HelloWorld` 

### MySQL
  0. Navigate to this [tutorial](https://corlewsolutions.com/articles/article-21-how-to-install-mysql-server-5-6-on-windows-7-development-machine) for alot of information.
  1. Below are the steps I took to get set-up:
      - Download the MySQL Installer for Windows at [https://dev.mysql.com/downloads/installer/](https://dev.mysql.com/downloads/installer/).
      - Fire up the .exe file and select the Developer Default option. Note that everything (like Python or Visual Studio) may be excecuted. That is ok. You can always add those connectors later (i.e. if you install Python or Visual Studio)
      - You can click "Next" through the rest of the scenerios, leaving add default selections and adding a connection password.
        - If only using a localhost connection on your laptop a username and password of "root" is fine.
      - After installation, you can add `C:\Program Files\MySQL\MySQL Server 5.7\bin` to your Path variable.
  2. You can test that it worked in 2 ways:
      - From Command Line (Windows), run `mysql -u root -p` and enter the password.
      - From Git Bash, run `mysql -u root -proot` (assuming your password was "root").
        - As an aside, I noticed mysql commands work better in the Windows Command Line.


### MySQL Workbench
  0. Navigate to [https://dev.mysql.com/downloads/workbench/](https://dev.mysql.com/downloads/workbench/) for the download.
  1. Note that you may need to download the [prerequisites](https://dev.mysql.com/resources/wb52_prerequisites.html) for Windows.
  2. Once you're sure you have the prerequisites, fire up the .exe file
  3. Leave all the default setting to complete the installation.
  4. Open MySQL Workbench at the end of the installation and connect to the "localhost" connection with your password from the MySQL installation (above).


### MariaDB
  0. Navigate to this [webpage](https://mariadb.com/kb/en/mariadb/installing-mariadb-alongside-mysql/) to learn how to set up MariaDB in addition to MySQL
  1. Download the MariaDB installer for Windows from [https://mariadb.com/downloads](https://mariadb.com/downloads)
  2. Fire up the .exe file and proceed with all default option except that for TCP Port.
      - Change the TCP Port to 3307 (note that MySQL is already using 3306)
      - Again, you can use "root" for the username and password.
  3. After installation, you can add `C:\Program Files\MariaDB 10.1\bin` to your Path variable (optional).
      - Note that you can choose either MariaDB or MySQL for this. If you want to use MariaDB, you have to remove the `C:\Program Files\MySQL\MySQL Server 5.7\bin` you made before.
      - From Command Line (Windows), run `mysql -u root -p` and enter the password.
  4. Now you can add the MariaDB connection to MySQL Workbench.
      - Open MySQL Workbench and click the "+" icon above your localhost connection
      - Add in a Connection Name (i.e. "Local Instance MariaDB")
      - Change the Port to 3307
      - Click OK to finsh. And then connect into your new localhost instance for MariaDB.


### Spring MVC
  0. Navigate to [https://spring.io/guides/gs/intellij-idea/](https://spring.io/guides/gs/intellij-idea/) to learn to set up Spring MVC with IntelliJ IDEA.
      - Assuming you already installed Maven from above, no additional downloading/setup will be needed.
  1. Test your setup by making a [Hello World Webpage](https://spring.io/guides/gs/serving-web-content/).
      - Now that you are set up, a great series for learning Spring MVC can be found [here](https://www.gontu.org/spring-mvc-tutorials/).
