maven 3.9.8 :-
sudo apt remove maven
wget https://downloads.apache.org/maven/maven-3/3.9.8/binaries/apache-maven-3.9.8-bin.tar.gz --no-check-certificate
tar -xvzf apache-maven-3.9.8-bin.tar.gz
sudo mv apache-maven-3.9.8 /opt/maven
export MAVEN_HOME=/opt/maven
export PATH=$MAVEN_HOME/bin:$PATH
source ~/.bashrc
mvn -v
export MAVEN_HOME=/opt/maven
export PATH=$MAVEN_HOME/bin:$PATH
source ~/.bashrc


export JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64
export PATH=$JAVA_HOME/bin:$PATH


java 17:-
tanveer@tanveer-k8:~/cservice$ export PATH=$JAVA_HOME/bin:$PATH
tanveer@tanveer-k8:~/cservice$ java -version
openjdk version "17.0.12" 2024-07-16
OpenJDK Runtime Environment (build 17.0.12+7-Ubuntu-1ubuntu224.04)
OpenJDK 64-Bit Server VM (build 17.0.12+7-Ubuntu-1ubuntu224.04, mixed mode, sharing)
tanveer@tanveer-k8:~/cservice$ mvn -v
Apache Maven 3.9.8 (36645f6c9b5079805ea5009217e36f2cffd34256)
Maven home: /opt/maven
Java version: 17.0.12, vendor: Ubuntu, runtime: /usr/lib/jvm/java-17-openjdk-amd64
Default locale: en_US, platform encoding: UTF-8
OS name: "linux", version: "6.8.0-45-generic", arch: "amd64", family: "unix"




1. To build this project we had to install Java 17 and Maven 3.9.8
2. Also check the pom.xml files for both micro service
3. I created two repos in dockerhub 1.khatanve/course-service 2. khatanve/blog-service