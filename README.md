# tomcat80-maven
this is an tomcat project build by maven ,base on TOMCAT_8_0_37

use main class `org.apache.catalina.startup.Bootstrap` and add VM Options:

```
-Dcatalina.home=target/classes/ -Dcatalina.base=target/classes/ -Djava.endorsed.dirs=${catalina.base}endorsed -Djava.io.tmpdir=${catalina.base}temp -Djava.util.logging.manager=org.apache.juli.ClassLoaderLogManager -Djava.util.logging.config.file=${catalina.base}conf/logging.properties
```

