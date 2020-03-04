Infinispan Server Test Driver Demo
==================================

This project is a demo for the Infinispan Server Test Driver.
It shows how to start a cluster of Infinispan Servers, each one running in its own container and then a number of
tests in which clients interact with the cluster.

First-off, you need to include the `org.infinispan:infinispan-server-testdriver-junit4` dependency to your project. For example, in Maven, add the following to your dependencies:

```xml
<dependency>
    <groupId>org.infinispan</groupId>
    <artifactId>infinispan-server-testdriver-junit4</artifactId>
    <version>${infinispan.version}</version>
</dependency>
```

By default, the tests will use the latest `infinispan/server` container image tagged for the major.minor version of the dependency above.
For example, if `infinispan.version` is `11.0.0.Final`, it will try to obtain `infinispan/server:11.0`. 
The image to use can be overridden by specifying an alternate one with the `org.infinispan.test.server.container.baseImageName` system property.
  
