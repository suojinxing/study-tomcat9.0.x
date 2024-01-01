# README

源码学习，里面包含了一个servletDemo
启动后访问  http://localhost:8080/hello 即可看到DEMO

1. tomcat原本使用ant构建，改为使用maven构建
2. 修改Tomcat `org.apache.catalina.startup.ContextConfig` 类，

    ```java
    context.addServletContainerInitializer(new JasperInitializer(), null);
    ```

3. `org.apache.jasper.compiler.JDTCompiler` 常量报错

    把原有的超过1.8的常量去掉
