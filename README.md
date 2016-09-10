# tomcat80-maven

this is an tomcat project build by maven ,base on TOMCAT_8_0_37
这个工程基于TOMCAT_8_0_37构建，是将tomcat完全转换为maven构建的方式，不再使用ant构建，也不是按照网上使用的用maven的聚合将ant的工程直接引入的。

use main class `org.apache.catalina.startup.Bootstrap` and add VM Options:
clone到本地之后，需要使用`org.apache.catalina.startup.Bootstrap`来运行，同时需要配置启动参数：

```
-Dcatalina.home=target/classes/ 
-Dcatalina.base=target/classes/ 
-Djava.endorsed.dirs=${catalina.base}endorsed 
-Djava.io.tmpdir=${catalina.base}temp 
-Djava.util.logging.manager=org.apache.juli.ClassLoaderLogManager 
-Djava.util.logging.config.file=${catalina.base}conf/logging.properties
```

注意，如果使用idea的话，需要将启动目录设置为core工程的目录，即Working directory设置为`$MODULE_DIR$`