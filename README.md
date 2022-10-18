### A simplest dynamic-template based JSON to JSON transformer with only one line of Java code.


```java
from("undertow:{{server}}/search?useStreaming=true").to("jslt:test.jslt").log("${body}");
```


- In the first part of this code we are using an undertow (jboss) to consume REST API.
- In the middle of this code we are passing rest JSON body into a JSLT template. 
- In the last part of this code we are logging the transformed JSON body.
