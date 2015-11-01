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
Download eclipse from: http://www.eclipse.org/downloads/download.php?file=/technology/epp/downloads/release/mars/1/eclipse-jee-mars-1-linux-gtk-x86_64.tar.gz. (if this link doesn't work, search for the download link in http://www.eclipse.org)

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
2.1: Create Project in github.com
---------------------------------
Go to http://github.com, if you don't have an account sign up here: http://github.com/join.
On your github home page, create a new repository.

Name your repositorie `disk-usage-supervision`, and check `Initialize this repository with a README`.

Choose Java in `add .gitignore` and create the repository!

Now clone your github repositorie in your local machine:

    $ mkdir -p workspace
    $ cd workspace
    $ git clone "https://github.com/YOUR_ACCOUNT/disk-usage-supervision.git"

2.2: Create project in Eclipse
------------------------------
Open eclipse from `apps/eclipse-jee-mars-1-linux-gtk-x86_64/eclipse`.

From eclipse File menu click new project: `File > New > Project`.
Under Web choose *Dynamic Web Project*.
Specify the Project name: `disk-usage-supervision`.


2.3: Create new Servlet Helloworld1
-----------------------------------
`File > New > Servlet`

Return this html:
```html
<html>
   <body>
      <h1>Hello world</h1>
   </body>
</html>
```
2.4: Web.xml
------------
Web.xml vs Annoations

2.4: Create new Servlet Helloworld2
-----------------------------------
`File > New > Servlet`

`File > New > JSP`

Return this html:
```html
<html>
   <body>
      <h1>Hello $name</h1>
   </body>
</html>
```

Step3: Minimum Valuable Product
===============================
In order to check disk usage in our Linux server, we we use the command line df, and parse it output for the program
Example of df output:
```
$ df
Filesystem     1K-blocks     Used Available Use% Mounted on
/dev/sda1      953143188 49205136 855498144   6% /
none                   4        0         4   0% /sys/fs/cgroup
udev             4024112        4   4024108   1% /dev
tmpfs             807884     1456    806428   1% /run
none                5120        0      5120   0% /run/lock
none             4039408     2312   4037096   1% /run/shm
none              102400       16    102384   1% /run/user
```
3.1 The df output class:
-----------------------
output class has theses attributes: device, mount point, used, available, percent, and time of execution
```java
public class DFOutput{

   private String deviceName;
   private String mountPoint;

}
```

3.2 Disk usage supervision class
--------------------------------
Executes df and parse output, 1 static method that returns List<DFOutput>
```java
package com.example.supervision.model;
public class DFSupervisor{
   public static List<DFOutput> getDiskSpaceUsage(){

   }
}
```

3.3 Servlet
-----------
Output result html
```html
<html>
   <body>
      <h1>title<h1>
      <table> </table>
   </body>
</html>
```
3.4 Basic Logging & Exception Logging
-------------------------------------
check code return
raise exception
log error
log success
output error in case

Step4: Database
===============
4.1: Download sql-helper
------------------------
```
git clone "http..."
```

4.2: Generate classes from config file
--------------------------------------
config file
```
{}
```
4.3: Crontable
--------------
intro
each hour
```
0 * * * * java etc... or script
```

4.4: Generate fake data
-----------------------
fill data base with fake data

from d0 to today, for each hour, p = p0 + (ptoday-p0)/total_hours*hour

Step5: Bootstrap
================
what is bootstrap

download link

5.1 Download & create clean JSP page
------------------------------------
clean html with one menu entry: dashboard

5.2 JSP page with element
-------------------------
jsp page

servlet redirection

5.3 Charts
----------
servelt load all from database

convert to json

plot (jsp)

Step6: Docker
=============
what is docker

6.1: Setup database
-------------------
```
docker pull mysql
docker pull phpmyadmin
```
expose and volumes

6.2: Setup tomcat
-----------------
```
docker pull tomcat
mkdir diskusage-supervision-docker
gedit Dockerfile
...
```
build etc...
6.3 Github & dockerHub
----------------------

Step7: Extra features
=====================
