# steps for install java
```
1) goto below website and accept the licence for the agreement
https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
2)Download the below rpm in windows 
Linux x64	168.05 MB  	jdk-8u201-linux-x64.rpm
if u download the above rpm through wget it is not praperlly download and installed
3)Through scp we can transfer the file on /tmp folder
4)commands on linux
which java
java -version
rpm -e java
rpm -ivh jdk-8u201-linux-x64.rpm
cd /usr/java/jdk1.8.0_201-amd64
pwd
cd /root
vi .bash_profile
***************
JAVA_HOME=/usr/java/jdk1.8.0_201-amd64
PATH=$JAVA_HOME/bin:$PATH
***************
which java
java -version
echo $JAVA_HOME
source .bash_profile
echo $JAVA_HOME
which java
```
https://github.com/rajadevops26/jenkins/blob/master/jenkins_setup/rpmjava.jpg
*****************************************
# jenkins install steps
```
1)to know in which os, we are install the package 
cat /etc/os-release
2)os current state updation
yum update
```
```
3)Go to below website for adding jenkins repo to the yum repository and import key from jenkins through rpm,
then download and install jenkins on os
```
[jenkins](https://pkg.jenkins.io/redhat/)
```
wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat/jenkins.repo
yum update
rpm --import https://pkg.jenkins.io/redhat/jenkins.io.key
ls
yum update
wget https://pkg.jenkins.io/redhat-stable/jenkins-2.138.1-1.1.noarch.rpm
ls
rpm -ivh jenkins-2.138.1-1.1.noarch.rpm
(or)
yum install jenkins
service jenkins status
service jenkins stop
service jenkins start
```
