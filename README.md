### Chapter 1: Running Gradle for the first time:

Step1: Create a task in `build.gradle` file:

```groovy
task hello {
    doLast {
        println "Hello from Gradle"
    }
}
```

Step2: Run the newly created task
```bash
./gradlew hello 

> Task :hello
Hello from Gradle

BUILD SUCCESSFUL in 0s
1 actionable task: 1 executed
```

Step3: Apply Java plugin in `build.gradle` file to work with Java source code

`apply plugin: 'java'`

Step4. Create a simple Java class:

```java
public class MainClass {

  public static void main(String[] args) {
    System.out.println("Hello, Java from Gradle project!");
  }
}
```

Step4: Build the java class
```bash
 ./gradlew build

BUILD SUCCESSFUL in 0s
2 actionable tasks: 2 up-to-date
```

Step5: Run the Java class
```bash
$ java -cp build/classes/java/main MainClass
Hello, Java from Gradle project!
```

Some commands:

1. Get all tasks list
```bash
./gradlew tasks 
```

