# Jetty on CloudBees

Jetty is a fast lightweight servlet engine for the JVM.

One of the best ways to deploy Jetty is to embed it in the app
- produce an executable app that is ready to go.

That is what this does (and also shows it running on CloudBees with just a JVM).
Use this as a starting point if you like, works with any version of Jetty you need.


# Running locally during development

    mvn clean compile exec:java

# Deploying by hand

    mvn clean compile assembly:single
    bees app:deploy -t java -R class=org.example.HelloWorld target/hello-world-0.1-SNAPSHOT-jar-with-dependencies.jar


# Executable jar

    mvn clean compile assembly:single
    java -jar target/hello-world-0.1-SNAPSHOT-jar-with-dependencies.jar

    (the jar is all you need)




