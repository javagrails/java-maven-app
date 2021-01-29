# Try Java application with tool maven*
## How to mavenize a simple java application

[Reference](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html)


![Resources](https://github.com/javagrails/java-maven-app/blob/develop/docs/java-maven-jar1.png)


### Necessary pre installed tools
```bash
1. Java/JDK any version 1.8 & above
2. Maven 3.x & above
3. Terminal to run maven/java commands
```

### Check Maven Installed or not
```bash
$ whereis mvn
mvn: /home/person/.sdkman/candidates/maven/3.5.0/bin/mvn /home/person/.sdkman/candidates/maven/3.5.0/bin/mvn.cmd
```

### Check Maven Version
```bash
$ mvn -version
Apache Maven 3.5.0 (ff8f5e7444045639af65f6095c62210b5713f426; 2017-04-04T01:39:06+06:00)
Maven home: /home/person/.sdkman/candidates/maven/current
Java version: 1.8.0_242, vendor: AdoptOpenJDK
Java home: /usr/lib/jvm/open-jdk1.8.0_242-linux-x64/jre
Default locale: en_US, platform encoding: UTF-8
OS name: "linux", version: "4.15.0-123-generic", arch: "amd64", family: "unix"
```

### Create Maven App With below Command

```bash
$ mvn archetype:generate -DgroupId=com.bk.app -DartifactId=java-maven-app -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false
```

### Tree View With target folder
```bash
$ tree java-maven-app
java-maven-app
├── info.txt
├── java-maven-app.iml
├── LICENSE
├── pom.xml
├── README.md
├── src
│   ├── main
│   │   └── java
│   │       └── com
│   │           └── bk
│   │               └── app
│   │                   └── App.java
│   └── test
│       └── java
│           └── com
│               └── bk
│                   └── app
│                       └── AppTest.java
└── target
    ├── classes
    │   └── com
    │       └── bk
    │           └── app
    │               └── App.class
    ├── generated-sources
    │   └── annotations
    ├── generated-test-sources
    │   └── test-annotations
    └── test-classes
        └── com
            └── bk
                └── app
                    └── AppTest.class

24 directories, 9 files
```

### Tree View Without target folder
```bash
$ tree java-maven-app
java-maven-app
├── info.txt
├── java-maven-app.iml
├── LICENSE
├── pom.xml
├── README.md
└── src
    ├── main
    │   └── java
    │       └── com
    │           └── bk
    │               └── app
    │                   └── App.java
    └── test
        └── java
            └── com
                └── bk
                    └── app
                        └── AppTest.java

11 directories, 7 files
```

### Project Compile (source code will compile in target folder)
```bash
$ mvn clean compile
OR
$ mvn compile
```

### Packaging JAR (.jar file will build in target folder)
```bash
$ mvn package
```

### Run JAR file as App
```bash
$ java -cp target/java-maven-app-1.0-SNAPSHOT.jar com.bk.app.App
Console Print : Java Maven App Created
```


# Bye Happy Coding - fork, star below
[**https://github.com/javagrails**](https://github.com/javagrails)
