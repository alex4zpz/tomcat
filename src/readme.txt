1、下载ant

官网首页：http://ant.apache.org/bindownload.cgi

2、设置ant环境变量；

3、下载tomcat源码；

官方直接下载地址：http://apache.fayea.com/tomcat/tomcat-6/v6.0.43/src/apache-tomcat-6.0.43-src.zip
官方首页：http://tomcat.apache.org/index.html

4、解压步骤3中下载的tomcat源码；

5、修改tomcat源码目录下的build.properties..default文件为build.properties

6、配置tomcat依赖包下载路径，修改build.properties文件的base.path，如图为我的配置

5、cmd进入进入tomcat源码解压后的路径后执行 ant  download,成功后如图：


6、成功后tomcat源码路径下会新生成一个文件夹


7、eclipse新建java工程，导入tomcat源码中的java和test目录文件，记住此处为导入file，然后将java和test两个文件夹加入到eclipse的编译路径下；

8、加入tomcat源码依赖的一些jar包，本次导入有如下包

ant.jar
ant-apache-log4j.jar
ant-commons-logging.jar
javax.wsdl_1.6.2.v201012040545.jar
jaxrpc.jar
junit-4.8.2.jar
org.eclipse.jdt.core_3.10.0.v20140902-0626.jar

9、启动类Bootstrap ，run configurations  -Dcatalina.home=编译后的源码路径\output\build