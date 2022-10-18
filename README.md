### Dynamic-template based JSON to JSON transformer

We need only one line of code for this -

```java
from("undertow:{{server}}/search?useStreaming=true").to("jslt:test.jslt").log("${body}");
```


- In the first part of this code we are using an undertow (jboss) to consume REST API.
- In the middle of this code we are passing rest JSON body into a JSLT template. 
- In the last part of this code we are logging the transformed JSON body.

### How to run this project 

This project is a Spring Boot Maven project and can be easily run using maven command

```
mvn spring-boot:run
```

or import this project in any IDE as a maven project.


