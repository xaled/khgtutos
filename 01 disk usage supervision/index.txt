Intorduction
============

You will make a java web application that supervises the disk usage in the server.

Step 1: Build the environnemnt
==============================
1.1 Install JDK
---------------
The easiest way to install the JDK 7 is to do it with the Web Up8 Oracle Java OOS. However, it is believed that this PPA is sometimes out of date. Also note the dangers of using a PPA.

This installs JDK 7 (which includes Java JDK, JRE and the Java browser plugin):

    $ sudo apt-get install python-software-properties
    $ sudo add-apt-repository ppa:webupd8team/java
    $ sudo apt-get update
    $ sudo apt-get install oracle-java7-installer

1.2 Install Eclipse JEE
-----------------------
Download eclipse from: [http://www.eclipse.org/downloads/download.php?file=/technology/epp/downloads/release/mars/1/eclipse-jee-mars-1-linux-gtk-x86_64.tar.gz][1]

create your app dir in your home

    $ cd
    $ mkdir apps
    $ cd apps
    $ wget "http://mirror.ufs.ac.za/eclipse/technology/epp/downloads/release/mars/1/eclipse-jee-mars-1-linux-gtk-x86_64.tar.gz"
    $ tar -xvf eclipse-jee-mars-1-linux-gtk-x86_64.tar.gz

1.3 Install Apache Tomcat
-------------------------
From the apache tomcat download page, download the last stable version of tomcat7: http://tomcat.apache.org/download-70.cgi

     $ cd ~/apps 
     $ wget "http://www.us.apache.org/dist/tomcat/tomcat-7/v7.0.65/bin/apache-tomcat-7.0.65.tar.gz"
     $ tar -xvf apache-tomcat-7.0.65.tar.gz

Step2: Create Hello World project
=================================
2.1: Create project
-------------------
Open eclipse from `apps/eclipse-jee-mars-1-linux-gtk-x86_64/eclipse`.

