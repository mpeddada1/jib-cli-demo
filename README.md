# jib-cli-demo

## [Jib](https://github.com/GoogleContainerTools/jib)
Available as Maven and Gradle plugins
- Fast
- Reproducible
- Daemonless

## [Jib CLI](https://github.com/GoogleContainerTools/jib/tree/master/jib-cli)
 Command line interface for building optimized containers from file system content or JAR.

### Jib CLI JAR Command

1. We will be using the [Spring Petclinic](https://projects.spring.io/spring-petclinic/) JAR in this demo
```
 $ git clone https://github.com/spring-projects/spring-petclinic.git
 $ cd spring-petclinic
 $ ./mvnw package
```
2. Jib a JAR
```
$ jib jar --target=docker://cli-jar-quickstart target/spring-petclinic-*.jar
```
3. Run the image and open your browser http://localhost:8080
```
 $ docker run -p 8080:8080 cli-jar-quickstart
```

### Jib CLI Build Command

1. Get your script ready
2. Create build file 
3. Build to local docker daemon 

```
 $ jib build --target=docker://cli-build-demo
```
4. Run the container 

```
 docker run cli-build-demo
```
