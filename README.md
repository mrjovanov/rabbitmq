# rabbitmq projekat za Univerzitet u Kragujevcu
- predmet: Integracija aplikacija preko sistema za prenos poruka
- autor: Milan Čabarkapa

Uputstvo:
---

~~~
cd rabbitmq/java
curl -O https://repo1.maven.org/maven2/com/rabbitmq/amqp-client/5.16.0/amqp-client-5.16.0.jar
curl -O https://repo1.maven.org/maven2/org/slf4j/slf4j-api/1.7.36/slf4j-api-1.7.36.jar
curl -O https://repo1.maven.org/maven2/org/slf4j/slf4j-simple/1.7.36/slf4j-simple-1.7.36.jar
~~~

Java okruženje (ako nije instalirano):
---
~~~
sudo apt install openjdk-17-jdk
~~

Kompilacija klijenta za slanje poruka:
---
~~~
export CP=.:amqp-client-5.16.0.jar:slf4j-api-1.7.36.jar:slf4j-simple-1.7.36.jar
javac -cp $CP Send.java
~~~
~~~
java -cp $CP Send
~~~

Kompilacija klijenta za prijem poruka:
---
~~~
export CP=.:amqp-client-5.16.0.jar:slf4j-api-1.7.36.jar:slf4j-simple-1.7.36.jar
javac -cp $CP Recv.java
~~~

~~~
java -cp $CP Recv
~~~