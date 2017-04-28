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
  0. Navigate to [https://spring.io/guides/gs/intellij-idea/](https://spring.io/guides/gs/intellij-idea/) to learn to install and intialize Maven.
  1. After downloading the .zip file, I saved it at `C:\Program Files\Apache\apache-maven-3.5.0`.
  2. Then, I needed to set the path and envirnomental variables. You can refer to [this](https://www.mkyong.com/maven/how-to-install-maven-in-windows/).
  3. After the path is set, run `mvn -version` in Git Bash to verify the installation.


### Spring MVC
  0. Navigate to [https://spring.io/guides/gs/intellij-idea/](https://spring.io/guides/gs/intellij-idea/) to learn to set up Spring MVC with IntelliJ IDEA.