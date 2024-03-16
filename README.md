# Setup of basic gradle using cli:
```agsl
gradle init --use-defaults --type java-application
```

The above command will setup a basic gradle project

```agsl
./gradlew build
```

To prepare a jar which is executable, you need to setup manifest property in `build.gradle` to identify what is the main class to execute
```groovy
jar {
    manifest {
        attributes (
            'Main-Class': 'org.example.Main'
        )
    }
}

```


The above command can build your project

```agsl
./gradlew jar
```

The above command creates a new jar file in `build/libs` folder

```agsl
java -jar build/libs/filename.jar
```

The above command will execute your code


## Homework

- Try to build a jar and run it directly from cli and see if the okhttp code is working or not just like it is working by running directly from intellij
- instead of okhttp try to integrate retrofit library to make the same http call