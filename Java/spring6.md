[[[[# Spring6

[![image-20221209110043449](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221209110043449.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221209110043449.png)

## [](https://blog.mohic.site/2024/05/18/spring6/#1%E3%80%81%E6%A6%82%E8%BF%B0 "1、概述")1、概述

### [](https://blog.mohic.site/2024/05/18/spring6/#1-1%E3%80%81Spring%E6%98%AF%E4%BB%80%E4%B9%88%EF%BC%9F "1.1、Spring是什么？")1.1、Spring是什么？

Spring 是一款主流的 Java EE 轻量级开源框架 ，Spring 由“Spring 之父”Rod Johnson 提出并创立，其目的是用于简化 Java 企业级应用的开发难度和开发周期。Spring的用途不仅限于服务器端的开发。从简单性、可测试性和松耦合的角度而言，任何Java应用都可以从Spring中受益。Spring 框架除了自己提供功能外，还提供整合其他技术和框架的能力。

Spring 自诞生以来备受青睐，一直被广大开发人员作为 Java 企业级应用程序开发的首选。时至今日，Spring 俨然成为了 Java EE 代名词，成为了构建 Java EE 应用的事实标准。

自 2004 年 4 月，Spring 1.0 版本正式发布以来，Spring 已经步入到了第 6 个大版本，也就是 Spring 6。本课程采用Spring当前最新发布的正式版本**6.0.2**。

[![image-20221216223135162](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221201102513199.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221201102513199.png)

### [](https://blog.mohic.site/2024/05/18/spring6/#1-2%E3%80%81Spring-%E7%9A%84%E7%8B%AD%E4%B9%89%E5%92%8C%E5%B9%BF%E4%B9%89 "1.2、Spring 的狭义和广义")1.2、Spring 的狭义和广义

在不同的语境中，Spring 所代表的含义是不同的。下面我们就分别从“广义”和“狭义”两个角度，对 Spring 进行介绍。

**广义的 Spring：Spring 技术栈**

广义上的 Spring 泛指以 Spring Framework 为核心的 Spring 技术栈。

经过十多年的发展，Spring 已经不再是一个单纯的应用框架，而是逐渐发展成为一个由多个不同子项目（模块）组成的成熟技术，例如 Spring Framework、Spring MVC、SpringBoot、Spring Cloud、Spring Data、Spring Security 等，其中 Spring Framework 是其他子项目的基础。

这些子项目涵盖了从企业级应用开发到云计算等各方面的内容，能够帮助开发人员解决软件发展过程中不断产生的各种实际问题，给开发人员带来了更好的开发体验。

**狭义的 Spring：Spring Framework**

狭义的 Spring 特指 Spring Framework，通常我们将它称为 Spring 框架。

Spring 框架是一个分层的、面向切面的 Java 应用程序的一站式轻量级解决方案，它是 Spring 技术栈的核心和基础，是为了解决企业级应用开发的复杂性而创建的。

Spring 有两个最核心模块： IoC 和 AOP。

**IoC**：Inverse of Control 的简写，译为“控制反转”，指把创建对象过程交给 Spring 进行管理。

**AOP**：Aspect Oriented Programming 的简写，译为“面向切面编程”。AOP 用来封装多个类的公共行为，将那些与业务无关，却为业务模块所共同调用的逻辑封装起来，减少系统的重复代码，降低模块间的耦合度。另外，AOP 还解决一些系统层面上的问题，比如日志、事务、权限等。

### [](https://blog.mohic.site/2024/05/18/spring6/#1-3%E3%80%81Spring-Framework%E7%89%B9%E7%82%B9 "1.3、Spring Framework特点")1.3、Spring Framework特点

- 非侵入式：使用 Spring Framework 开发应用程序时，Spring 对应用程序本身的结构影响非常小。对领域模型可以做到零污染；对功能性组件也只需要使用几个简单的注解进行标记，完全不会破坏原有结构，反而能将组件结构进一步简化。这就使得基于 Spring Framework 开发应用程序时结构清晰、简洁优雅。
    
- 控制反转：IoC——Inversion of Control，翻转资源获取方向。把自己创建资源、向环境索取资源变成环境将资源准备好，我们享受资源注入。
    
- 面向切面编程：AOP——Aspect Oriented Programming，在不修改源代码的基础上增强代码功能。
    
- 容器：Spring IoC 是一个容器，因为它包含并且管理组件对象的生命周期。组件享受到了容器化的管理，替程序员屏蔽了组件创建过程中的大量细节，极大的降低了使用门槛，大幅度提高了开发效率。
    
- 组件化：Spring 实现了使用简单的组件配置组合成一个复杂的应用。在 Spring 中可以使用 XML 和 Java 注解组合这些对象。这使得我们可以基于一个个功能明确、边界清晰的组件有条不紊的搭建超大型复杂应用系统。
    
- 一站式：在 IoC 和 AOP 的基础上可以整合各种企业应用的开源框架和优秀的第三方类库。而且 Spring 旗下的项目已经覆盖了广泛领域，很多方面的功能性需求可以在 Spring Framework 的基础上全部使用 Spring 来实现。
    

### [](https://blog.mohic.site/2024/05/18/spring6/#1-4%E3%80%81Spring%E6%A8%A1%E5%9D%97%E7%BB%84%E6%88%90 "1.4、Spring模块组成")1.4、Spring模块组成

官网地址：[https://spring.io/](https://spring.io/)

[![image-20221207142746771](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207142746771.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207142746771.png)

[![image-2097896352](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/2097896352.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/2097896352.png)

上图中包含了 Spring 框架的所有模块，这些模块可以满足一切企业级应用开发的需求，在开发过程中可以根据需求有选择性地使用所需要的模块。下面分别对这些模块的作用进行简单介绍。

**①Spring Core（核心容器）**

spring core提供了IOC,DI,Bean配置装载创建的核心实现。核心概念： Beans、BeanFactory、BeanDefinitions、ApplicationContext。

- spring-core ：IOC和DI的基本实现
    
- spring-beans：BeanFactory和Bean的装配管理(BeanFactory)
    
- spring-context：Spring context上下文，即IOC容器(AppliactionContext)
    
- spring-expression：spring表达式语言
    

**②Spring AOP**

- spring-aop：面向切面编程的应用模块，整合ASM，CGLib，JDK Proxy
- spring-aspects：集成AspectJ，AOP应用框架
- spring-instrument：动态Class Loading模块

**③Spring Data Access**

- spring-jdbc：spring对JDBC的封装，用于简化jdbc操作
- spring-orm：java对象与数据库数据的映射框架
- spring-oxm：对象与xml文件的映射框架
- spring-jms： Spring对Java Message Service(java消息服务)的封装，用于服务之间相互通信
- spring-tx：spring jdbc事务管理

**④Spring Web**

- spring-web：最基础的web支持，建立于spring-context之上，通过servlet或listener来初始化IOC容器
- spring-webmvc：实现web mvc
- spring-websocket：与前端的全双工通信协议
- spring-webflux：Spring 5.0提供的，用于取代传统java servlet，非阻塞式Reactive Web框架，异步，非阻塞，事件驱动的服务

**⑤Spring Message**

- Spring-messaging：spring 4.0提供的，为Spring集成一些基础的报文传送服务

**⑥Spring test**

- spring-test：集成测试支持，主要是对junit的封装

### [](https://blog.mohic.site/2024/05/18/spring6/#1-5%E3%80%81Spring6%E7%89%B9%E7%82%B9 "1.5、Spring6特点")1.5、Spring6特点

#### [](https://blog.mohic.site/2024/05/18/spring6/#1-5-1%E3%80%81%E7%89%88%E6%9C%AC%E8%A6%81%E6%B1%82 "1.5.1、版本要求")1.5.1、版本要求

**（1）Spring6要求JDK最低版本是JDK17**

[![image-20221201103138194](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221201103138194.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221201103138194.png)

#### [](https://blog.mohic.site/2024/05/18/spring6/#1-5-2%E3%80%81%E6%9C%AC%E8%AF%BE%E7%A8%8B%E8%BD%AF%E4%BB%B6%E7%89%88%E6%9C%AC "1.5.2、本课程软件版本")1.5.2、本课程软件版本

（1）IDEA开发工具：2022.1.2

（2）JDK：Java17**（Spring6要求JDK最低版本是Java17）**

（3）Spring：6.0.2

## [](https://blog.mohic.site/2024/05/18/spring6/#2%E3%80%81%E5%85%A5%E9%97%A8 "2、入门")2、入门

### [](https://blog.mohic.site/2024/05/18/spring6/#2-1%E3%80%81%E7%8E%AF%E5%A2%83%E8%A6%81%E6%B1%82 "2.1、环境要求")2.1、环境要求

- JDK：Java17+**（Spring6要求JDK最低版本是Java17）**
    
- Maven：3.6+
    
- Spring：6.0.2
    

### [](https://blog.mohic.site/2024/05/18/spring6/#2-2%E3%80%81%E6%9E%84%E5%BB%BA%E6%A8%A1%E5%9D%97 "2.2、构建模块")2.2、构建模块

**（1）构建父模块spring6**

在idea中，依次单击 File -> New -> Project -> New Project

[![image-20221205201741893](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221205201741893.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221205201741893.png)

点击“Create”

[![image-20221205202000198](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221205202000198.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221205202000198.png)

删除src目录

**（2）构建子模块spring6-first**

[![image-20221205202117383](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221205202117383.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221205202117383.png)

点击 Create 完成

[![image-20221205202154225](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221205202154225.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221205202154225.png)

### [](https://blog.mohic.site/2024/05/18/spring6/#2-3%E3%80%81%E7%A8%8B%E5%BA%8F%E5%BC%80%E5%8F%91 "2.3、程序开发")2.3、程序开发

#### [](https://blog.mohic.site/2024/05/18/spring6/#2-3-1%E3%80%81%E5%BC%95%E5%85%A5%E4%BE%9D%E8%B5%96 "2.3.1、引入依赖")2.3.1、引入依赖

[https://spring.io/projects/spring-framework#learn](https://spring.io/projects/spring-framework#learn)

**添加依赖：**

xml

```xml
<dependencies>  
    <!--spring context依赖-->  
    <!--当你引入Spring Context依赖之后，表示将Spring的基础依赖引入了-->  
    <dependency>  
        <groupId>org.springframework</groupId>  
        <artifactId>spring-context</artifactId>  
        <version>6.0.2</version>  
    </dependency>  
  
    <!--junit5测试-->  
    <dependency>  
        <groupId>org.junit.jupiter</groupId>  
        <artifactId>junit-jupiter-api</artifactId>  
        <version>5.3.1</version>  
    </dependency>  
</dependencies>
```
**查看依赖：**

[![image-20221201105416558](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221201105416558.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221201105416558.png)

#### [](https://blog.mohic.site/2024/05/18/spring6/#2-3-2%E3%80%81%E5%88%9B%E5%BB%BAjava%E7%B1%BB "2.3.2、创建java类")2.3.2、创建java类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8|package com.atguigu.spring6.bean;  <br>  <br>public class HelloWorld {  <br>      <br>    public void sayHello(){  <br>        System.out.println("helloworld");  <br>    }  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#2-3-3%E3%80%81%E5%88%9B%E5%BB%BA%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6 "2.3.3、创建配置文件")2.3.3、创建配置文件

在resources目录创建一个 Spring 配置文件 beans.xml（配置文件名称可随意命名，如：springs.xm）

[![img007](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img007.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img007.png)

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15|<?xml version="1.0" encoding="UTF-8"?>  <br><beans xmlns="http://www.springframework.org/schema/beans"  <br>       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  <br>       xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd">  <br>  <br>    <!--  <br>    配置HelloWorld所对应的bean，即将HelloWorld的对象交给Spring的IOC容器管理  <br>    通过bean标签配置IOC容器所管理的bean  <br>    属性：  <br>        id：设置bean的唯一标识  <br>        class：设置bean所对应类型的全类名  <br>	-->  <br>    <bean id="helloWorld" class="com.atguigu.spring6.bean.HelloWorld"></bean>  <br>      <br></beans>|

#### [](https://blog.mohic.site/2024/05/18/spring6/#2-3-4%E3%80%81%E5%88%9B%E5%BB%BA%E6%B5%8B%E8%AF%95%E7%B1%BB%E6%B5%8B%E8%AF%95 "2.3.4、创建测试类测试")2.3.4、创建测试类测试

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15|package com.atguigu.spring6.bean;  <br>  <br>import org.junit.jupiter.api.Test;  <br>import org.springframework.context.ApplicationContext;  <br>import org.springframework.context.support.ClassPathXmlApplicationContext;  <br>  <br>public class HelloWorldTest {  <br>  <br>    @Test  <br>    public void testHelloWorld(){  <br>        ApplicationContext ac = new ClassPathXmlApplicationContext("beans.xml");  <br>        HelloWorld helloworld = (HelloWorld) ac.getBean("helloWorld");  <br>        helloworld.sayHello();  <br>    }  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#2-3-5%E3%80%81%E8%BF%90%E8%A1%8C%E6%B5%8B%E8%AF%95%E7%A8%8B%E5%BA%8F "2.3.5、运行测试程序")2.3.5、运行测试程序

[![image-20221031172354535](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221031172354535.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221031172354535.png)

### [](https://blog.mohic.site/2024/05/18/spring6/#2-4%E3%80%81%E7%A8%8B%E5%BA%8F%E5%88%86%E6%9E%90 "2.4、程序分析")2.4、程序分析

**1. 底层是怎么创建对象的，是通过反射机制调用无参数构造方法吗？**

修改HelloWorld类：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12|package com.atguigu.spring6.bean;  <br>  <br>public class HelloWorld {  <br>  <br>    public HelloWorld() {  <br>        System.out.println("无参数构造方法执行");  <br>    }  <br>  <br>    public void sayHello(){  <br>        System.out.println("helloworld");  <br>    }  <br>}|

执行结果：

[![image-20221031181430720](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221031181430720.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221031181430720.png)

**测试得知：创建对象时确实调用了无参数构造方法。**

**2. Spring是如何创建对象的呢？原理是什么？**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5|// dom4j解析beans.xml文件，从中获取class属性值，类的全类名  <br> // 通过反射机制调用无参数构造方法创建对象  <br> Class clazz = Class.forName("com.atguigu.spring6.bean.HelloWorld");  <br> //Object obj = clazz.newInstance();  <br> Object object = clazz.getDeclaredConstructor().newInstance();|

**3. 把创建好的对象存储到一个什么样的数据结构当中了呢？**

bean对象最终存储在spring容器中，在spring源码底层就是一个map集合，存储bean的map在**DefaultListableBeanFactory**类中：

java

|   |   |
|---|---|
|1|private final Map<String, BeanDefinition> beanDefinitionMap = new ConcurrentHashMap<>(256);|

Spring容器加载到Bean类时 , 会把这个类的描述信息, 以包名加类名的方式存到beanDefinitionMap 中,  
Map<String,BeanDefinition> , 其中 String是Key , 默认是类名首字母小写 , BeanDefinition , 存的是类的定义(描述信息) , 我们通常叫BeanDefinition接口为 : bean的定义对象。

### [](https://blog.mohic.site/2024/05/18/spring6/#2-5%E3%80%81%E5%90%AF%E7%94%A8Log4j2%E6%97%A5%E5%BF%97%E6%A1%86%E6%9E%B6 "2.5、启用Log4j2日志框架")2.5、启用Log4j2日志框架

#### [](https://blog.mohic.site/2024/05/18/spring6/#2-5-1%E3%80%81Log4j2%E6%97%A5%E5%BF%97%E6%A6%82%E8%BF%B0 "2.5.1、Log4j2日志概述")2.5.1、Log4j2日志概述

在项目开发中，日志十分的重要，不管是记录运行情况还是定位线上问题，都离不开对日志的分析。日志记录了系统行为的时间、地点、状态等相关信息，能够帮助我们了解并监控系统状态，在发生错误或者接近某种危险状态时能够及时提醒我们处理，同时在系统产生问题时，能够帮助我们快速的定位、诊断并解决问题。

**Apache Log4j2**是一个开源的日志记录组件，使用非常的广泛。在工程中以易用方便代替了 System.out 等打印语句，它是JAVA下最流行的日志输入工具。

**Log4j2主要由几个重要的组件构成：**

**（1）日志信息的优先级**，日志信息的优先级从高到低有**TRACE < DEBUG < INFO < WARN < ERROR < FATAL**  
TRACE：追踪，是最低的日志级别，相当于追踪程序的执行  
DEBUG：调试，一般在开发中，都将其设置为最低的日志级别  
INFO：信息，输出重要的信息，使用较多  
WARN：警告，输出警告的信息  
ERROR：错误，输出错误信息  
FATAL：严重错误

这些级别分别用来指定这条日志信息的重要程度；级别高的会自动屏蔽级别低的日志，也就是说，设置了WARN的日志，则INFO、DEBUG的日志级别的日志不会显示

**（2）日志信息的输出目的地**，日志信息的输出目的地指定了日志将打印到**控制台**还是**文件中**；

**（3）日志信息的输出格式**，而输出格式则控制了日志信息的显示内容。

#### [](https://blog.mohic.site/2024/05/18/spring6/#2-5-2%E3%80%81%E5%BC%95%E5%85%A5Log4j2%E4%BE%9D%E8%B5%96 "2.5.2、引入Log4j2依赖")2.5.2、引入Log4j2依赖

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11|<!--log4j2的依赖-->  <br><dependency>  <br>    <groupId>org.apache.logging.log4j</groupId>  <br>    <artifactId>log4j-core</artifactId>  <br>    <version>2.19.0</version>  <br></dependency>  <br><dependency>  <br>    <groupId>org.apache.logging.log4j</groupId>  <br>    <artifactId>log4j-slf4j2-impl</artifactId>  <br>    <version>2.19.0</version>  <br></dependency>|

#### [](https://blog.mohic.site/2024/05/18/spring6/#2-5-3%E3%80%81%E5%8A%A0%E5%85%A5%E6%97%A5%E5%BF%97%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6 "2.5.3、加入日志配置文件")2.5.3、加入日志配置文件

在类的根路径下提供log4j2.xml配置文件（文件名固定为：log4j2.xml，文件必须放到类根路径下。）

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40  <br>41  <br>42  <br>43  <br>44  <br>45  <br>46|<?xml version="1.0" encoding="UTF-8"?>  <br><configuration>  <br>    <loggers>  <br>        <!--  <br>            level指定日志级别，从低到高的优先级：  <br>                TRACE < DEBUG < INFO < WARN < ERROR < FATAL  <br>                trace：追踪，是最低的日志级别，相当于追踪程序的执行  <br>                debug：调试，一般在开发中，都将其设置为最低的日志级别  <br>                info：信息，输出重要的信息，使用较多  <br>                warn：警告，输出警告的信息  <br>                error：错误，输出错误信息  <br>                fatal：严重错误  <br>        -->  <br>        <root level="DEBUG">  <br>            <appender-ref ref="spring6log"/>  <br>            <appender-ref ref="RollingFile"/>  <br>            <appender-ref ref="log"/>  <br>        </root>  <br>    </loggers>  <br>  <br>    <appenders>  <br>        <!--输出日志信息到控制台-->  <br>        <console name="spring6log" target="SYSTEM_OUT">  <br>            <!--控制日志输出的格式-->  <br>            <PatternLayout pattern="%d{yyyy-MM-dd HH:mm:ss SSS} [%t] %-3level %logger{1024} - %msg%n"/>  <br>        </console>  <br>  <br>        <!--文件会打印出所有信息，这个log每次运行程序会自动清空，由append属性决定，适合临时测试用-->  <br>        <File name="log" fileName="d:/spring6_log/test.log" append="false">  <br>            <PatternLayout pattern="%d{HH:mm:ss.SSS} %-5level %class{36} %L %M - %msg%xEx%n"/>  <br>        </File>  <br>  <br>        <!-- 这个会打印出所有的信息，  <br>            每次大小超过size，  <br>            则这size大小的日志会自动存入按年份-月份建立的文件夹下面并进行压缩，  <br>            作为存档-->  <br>        <RollingFile name="RollingFile" fileName="d:/spring6_log/app.log"  <br>                     filePattern="log/$${date:yyyy-MM}/app-%d{MM-dd-yyyy}-%i.log.gz">  <br>            <PatternLayout pattern="%d{yyyy-MM-dd 'at' HH:mm:ss z} %-5level %class{36} %L %M - %msg%xEx%n"/>  <br>            <SizeBasedTriggeringPolicy size="50MB"/>  <br>            <!-- DefaultRolloverStrategy属性如不设置，  <br>            则默认为最多同一文件夹下7个文件，这里设置了20 -->  <br>            <DefaultRolloverStrategy max="20"/>  <br>        </RollingFile>  <br>    </appenders>  <br></configuration>|

#### [](https://blog.mohic.site/2024/05/18/spring6/#2-5-4%E3%80%81%E6%B5%8B%E8%AF%95 "2.5.4、测试")2.5.4、测试

运行原测试程序

[![image-20221031214305224](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221031214305224.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221031214305224.png)

运行原测试程序，多了spring打印日志

#### [](https://blog.mohic.site/2024/05/18/spring6/#2-5-5%E3%80%81%E4%BD%BF%E7%94%A8%E6%97%A5%E5%BF%97 "2.5.5、使用日志")2.5.5、使用日志

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12|public class HelloWorldTest {  <br>  <br>    private Logger logger = LoggerFactory.getLogger(HelloWorldTest.class);  <br>  <br>    @Test  <br>    public void testHelloWorld(){  <br>        ApplicationContext ac = new ClassPathXmlApplicationContext("beans.xml");  <br>        HelloWorld helloworld = (HelloWorld) ac.getBean("helloWorld");  <br>        helloworld.sayHello();  <br>        logger.info("执行成功");  <br>    }  <br>}|

控制台：

[![image-20221031214547501](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221031214547501.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221031214547501.png)

## [](https://blog.mohic.site/2024/05/18/spring6/#3%E3%80%81%E5%AE%B9%E5%99%A8%EF%BC%9AIoC "3、容器：IoC")3、容器：IoC

IoC 是 Inversion of Control 的简写，译为“控制反转”，它不是一门技术，而是一种设计思想，是一个重要的面向对象编程法则，能够指导我们如何设计出松耦合、更优良的程序。

Spring 通过 IoC 容器来管理所有 Java 对象的实例化和初始化，控制对象与对象之间的依赖关系。我们将由 IoC 容器管理的 Java 对象称为 Spring Bean，它与使用关键字 new 创建的 Java 对象没有任何区别。

IoC 容器是 Spring 框架中最重要的核心组件之一，它贯穿了 Spring 从诞生到成长的整个过程。

### [](https://blog.mohic.site/2024/05/18/spring6/#3-1%E3%80%81IoC%E5%AE%B9%E5%99%A8 "3.1、IoC容器")3.1、IoC容器

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-1-1%E3%80%81%E6%8E%A7%E5%88%B6%E5%8F%8D%E8%BD%AC%EF%BC%88IoC%EF%BC%89 "3.1.1、控制反转（IoC）")3.1.1、控制反转（IoC）

- 控制反转是一种思想。
    
- 控制反转是为了降低程序耦合度，提高程序扩展力。
    
- 控制反转，反转的是什么？
    
- - 将对象的创建权利交出去，交给第三方容器负责。
    - 将对象和对象之间关系的维护权交出去，交给第三方容器负责。
- 控制反转这种思想如何实现呢？
    
- - DI（Dependency Injection）：依赖注入

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-1-2%E3%80%81%E4%BE%9D%E8%B5%96%E6%B3%A8%E5%85%A5 "3.1.2、依赖注入")3.1.2、依赖注入

DI（Dependency Injection）：依赖注入，依赖注入实现了控制反转的思想。

**依赖注入：**

- **指Spring创建对象的过程中，将对象依赖属性通过配置进行注入**

依赖注入常见的实现方式包括两种：

- 第一种：set注入
- 第二种：构造注入

所以结论是：IOC 就是一种控制反转的思想， 而 DI 是对IoC的一种具体实现。

**Bean管理说的是：Bean对象的创建，以及Bean对象中属性的赋值（或者叫做Bean对象之间关系的维护）。**

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-1-3%E3%80%81IoC%E5%AE%B9%E5%99%A8%E5%9C%A8Spring%E7%9A%84%E5%AE%9E%E7%8E%B0 "3.1.3、IoC容器在Spring的实现")3.1.3、IoC容器在Spring的实现

Spring 的 IoC 容器就是 IoC思想的一个落地的产品实现。IoC容器中管理的组件也叫做 bean。在创建 bean 之前，首先需要创建IoC 容器。Spring 提供了IoC 容器的两种实现方式：

**①BeanFactory**

这是 IoC 容器的基本实现，是 Spring 内部使用的接口。面向 Spring 本身，不提供给开发人员使用。

**②ApplicationContext**

BeanFactory 的子接口，提供了更多高级特性。面向 Spring 的使用者，几乎所有场合都使用 ApplicationContext 而不是底层的 BeanFactory。

**③ApplicationContext的主要实现类**

[![iamges](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img005.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img005.png)

|类型名|简介|
|---|---|
|ClassPathXmlApplicationContext|通过读取类路径下的 XML 格式的配置文件创建 IOC 容器对象|
|FileSystemXmlApplicationContext|通过文件系统路径读取 XML 格式的配置文件创建 IOC 容器对象|
|ConfigurableApplicationContext|ApplicationContext 的子接口，包含一些扩展方法 refresh() 和 close() ，让 ApplicationContext 具有启动、关闭和刷新上下文的能力。|
|WebApplicationContext|专门为 Web 应用准备，基于 Web 环境创建 IOC 容器对象，并将对象引入存入 ServletContext 域中。|

### [](https://blog.mohic.site/2024/05/18/spring6/#3-2%E3%80%81%E5%9F%BA%E4%BA%8EXML%E7%AE%A1%E7%90%86Bean "3.2、基于XML管理Bean")3.2、基于XML管理Bean

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-2-1%E3%80%81%E6%90%AD%E5%BB%BA%E5%AD%90%E6%A8%A1%E5%9D%97spring6-ioc-xml "3.2.1、搭建子模块spring6-ioc-xml")3.2.1、搭建子模块spring6-ioc-xml

**①搭建模块**

搭建方式如：spring-first

**②引入配置文件**

引入spring-first模块配置文件：beans.xml、log4j2.xml

**③添加依赖**

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28|<dependencies>  <br>    <!--spring context依赖-->  <br>    <!--当你引入Spring Context依赖之后，表示将Spring的基础依赖引入了-->  <br>    <dependency>  <br>        <groupId>org.springframework</groupId>  <br>        <artifactId>spring-context</artifactId>  <br>        <version>6.0.3</version>  <br>    </dependency>  <br>  <br>    <!--junit5测试-->  <br>    <dependency>  <br>        <groupId>org.junit.jupiter</groupId>  <br>        <artifactId>junit-jupiter-api</artifactId>  <br>        <version>5.3.1</version>  <br>    </dependency>  <br>  <br>    <!--log4j2的依赖-->  <br>    <dependency>  <br>        <groupId>org.apache.logging.log4j</groupId>  <br>        <artifactId>log4j-core</artifactId>  <br>        <version>2.19.0</version>  <br>    </dependency>  <br>    <dependency>  <br>        <groupId>org.apache.logging.log4j</groupId>  <br>        <artifactId>log4j-slf4j2-impl</artifactId>  <br>        <version>2.19.0</version>  <br>    </dependency>  <br></dependencies>|

**④引入java类**

引入spring-first模块java及test目录下实体类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13|package com.atguigu.spring6.bean;  <br>  <br>public class HelloWorld {  <br>  <br>    public HelloWorld() {  <br>        System.out.println("无参数构造方法执行");  <br>    }  <br>  <br>    public void sayHello(){  <br>        System.out.println("helloworld");  <br>    }  <br>}|

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17|package com.atguigu.spring6.bean;  <br>  <br>import org.junit.jupiter.api.Test;  <br>import org.slf4j.Logger;  <br>import org.slf4j.LoggerFactory;  <br>import org.springframework.context.ApplicationContext;  <br>import org.springframework.context.support.ClassPathXmlApplicationContext;  <br>  <br>public class HelloWorldTest {  <br>  <br>    private Logger logger = LoggerFactory.getLogger(HelloWorldTest.class);  <br>  <br>    @Test  <br>    public void testHelloWorld(){  <br>          <br>    }  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-2-2%E3%80%81%E5%AE%9E%E9%AA%8C%E4%B8%80%EF%BC%9A%E8%8E%B7%E5%8F%96bean "3.2.2、实验一：获取bean")3.2.2、实验一：获取bean

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A0%E6%96%B9%E5%BC%8F%E4%B8%80%EF%BC%9A%E6%A0%B9%E6%8D%AEid%E8%8E%B7%E5%8F%96 "①方式一：根据id获取")①方式一：根据id获取

由于 id 属性指定了 bean 的唯一标识，所以根据 bean 标签的 id 属性可以精确获取到一个组件对象。上个实验中我们使用的就是这种方式。

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A1%E6%96%B9%E5%BC%8F%E4%BA%8C%EF%BC%9A%E6%A0%B9%E6%8D%AE%E7%B1%BB%E5%9E%8B%E8%8E%B7%E5%8F%96 "②方式二：根据类型获取")②方式二：根据类型获取

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|@Test  <br>public void testHelloWorld1(){  <br>	ApplicationContext ac = new ClassPathXmlApplicationContext("beans.xml");  <br>    HelloWorld bean = ac.getBean(HelloWorld.class);  <br>    bean.sayHello();  <br>}|

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A2%E6%96%B9%E5%BC%8F%E4%B8%89%EF%BC%9A%E6%A0%B9%E6%8D%AEid%E5%92%8C%E7%B1%BB%E5%9E%8B "③方式三：根据id和类型")③方式三：根据id和类型

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|@Test  <br>public void testHelloWorld2(){  <br>	ApplicationContext ac = new ClassPathXmlApplicationContext("beans.xml");  <br>    HelloWorld bean = ac.getBean("helloworld", HelloWorld.class);  <br>    bean.sayHello();  <br>}|

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A3%E6%B3%A8%E6%84%8F%E7%9A%84%E5%9C%B0%E6%96%B9 "④注意的地方")④注意的地方

当根据类型获取bean时，要求IOC容器中指定类型的bean有且只能有一个

当IOC容器中一共配置了两个：

xml

|   |   |
|---|---|
|1  <br>2|<bean id="helloworldOne" class="com.atguigu.spring6.bean.HelloWorld"></bean>  <br><bean id="helloworldTwo" class="com.atguigu.spring6.bean.HelloWorld"></bean>|

根据类型获取时会抛出异常：

> org.springframework.beans.factory.NoUniqueBeanDefinitionException: No qualifying bean of type ‘com.atguigu.spring6.bean.HelloWorld’ available: expected single matching bean but found 2: helloworldOne,helloworldTwo

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A4%E6%89%A9%E5%B1%95%E7%9F%A5%E8%AF%86 "⑤扩展知识")⑤扩展知识

如果组件类实现了接口，根据接口类型可以获取 bean 吗？

> 可以，前提是bean唯一

如果一个接口有多个实现类，这些实现类都配置了 bean，根据接口类型可以获取 bean 吗？

> 不行，因为bean不唯一

**结论**

根据类型来获取bean时，在满足bean唯一性的前提下，其实只是看：『对象 **instanceof** 指定的类型』的返回结果，只要返回的是true就可以认定为和类型匹配，能够获取到。

java中，instanceof运算符用于判断前面的对象是否是后面的类，或其子类、实现类的实例。如果是返回true，否则返回false。也就是说：用instanceof关键字做判断时， instanceof 操作符的左右操作必须有继承或实现关系

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-2-3%E3%80%81%E5%AE%9E%E9%AA%8C%E4%BA%8C%EF%BC%9A%E4%BE%9D%E8%B5%96%E6%B3%A8%E5%85%A5%E4%B9%8Bsetter%E6%B3%A8%E5%85%A5 "3.2.3、实验二：依赖注入之setter注入")3.2.3、实验二：依赖注入之setter注入

**①创建学生类Student**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40  <br>41  <br>42  <br>43  <br>44  <br>45  <br>46  <br>47  <br>48  <br>49  <br>50  <br>51  <br>52  <br>53  <br>54  <br>55  <br>56  <br>57  <br>58|package com.atguigu.spring6.bean;  <br>  <br>public class Student {  <br>  <br>    private Integer id;  <br>  <br>    private String name;  <br>  <br>    private Integer age;  <br>  <br>    private String sex;  <br>  <br>    public Student() {  <br>    }  <br>  <br>    public Integer getId() {  <br>        return id;  <br>    }  <br>  <br>    public void setId(Integer id) {  <br>        this.id = id;  <br>    }  <br>  <br>    public String getName() {  <br>        return name;  <br>    }  <br>  <br>    public void setName(String name) {  <br>        this.name = name;  <br>    }  <br>  <br>    public Integer getAge() {  <br>        return age;  <br>    }  <br>  <br>    public void setAge(Integer age) {  <br>        this.age = age;  <br>    }  <br>  <br>    public String getSex() {  <br>        return sex;  <br>    }  <br>  <br>    public void setSex(String sex) {  <br>        this.sex = sex;  <br>    }  <br>  <br>    @Override  <br>    public String toString() {  <br>        return "Student{" +  <br>                "id=" + id +  <br>                ", name='" + name + '\'' +  <br>                ", age=" + age +  <br>                ", sex='" + sex + '\'' +  <br>                '}';  <br>    }  <br>  <br>}|

**②配置bean时为属性赋值**

spring-di.xml

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9|<bean id="studentOne" class="com.atguigu.spring6.bean.Student">  <br>    <!-- property标签：通过组件类的setXxx()方法给组件对象设置属性 -->  <br>    <!-- name属性：指定属性名（这个属性名是getXxx()、setXxx()方法定义的，和成员变量无关） -->  <br>    <!-- value属性：指定属性值 -->  <br>    <property name="id" value="1001"></property>  <br>    <property name="name" value="张三"></property>  <br>    <property name="age" value="23"></property>  <br>    <property name="sex" value="男"></property>  <br></bean>|

**③测试**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|@Test  <br>public void testDIBySet(){  <br>    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-di.xml");  <br>    Student studentOne = ac.getBean("studentOne", Student.class);  <br>    System.out.println(studentOne);  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-2-4%E3%80%81%E5%AE%9E%E9%AA%8C%E4%B8%89%EF%BC%9A%E4%BE%9D%E8%B5%96%E6%B3%A8%E5%85%A5%E4%B9%8B%E6%9E%84%E9%80%A0%E5%99%A8%E6%B3%A8%E5%85%A5 "3.2.4、实验三：依赖注入之构造器注入")3.2.4、实验三：依赖注入之构造器注入

**①在Student类中添加有参构造**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|public Student(Integer id, String name, Integer age, String sex) {  <br>    this.id = id;  <br>    this.name = name;  <br>    this.age = age;  <br>    this.sex = sex;  <br>}|

**②配置bean**

spring-di.xml

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|<bean id="studentTwo" class="com.atguigu.spring6.bean.Student">  <br>    <constructor-arg value="1002"></constructor-arg>  <br>    <constructor-arg value="李四"></constructor-arg>  <br>    <constructor-arg value="33"></constructor-arg>  <br>    <constructor-arg value="女"></constructor-arg>  <br></bean>|

> 注意：
> 
> constructor-arg标签还有两个属性可以进一步描述构造器参数：
> 
> - index属性：指定参数所在位置的索引（从0开始）
> - name属性：指定参数名

**③测试**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|@Test  <br>public void testDIByConstructor(){  <br>    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-di.xml");  <br>    Student studentOne = ac.getBean("studentTwo", Student.class);  <br>    System.out.println(studentOne);  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-2-5%E3%80%81%E5%AE%9E%E9%AA%8C%E5%9B%9B%EF%BC%9A%E7%89%B9%E6%AE%8A%E5%80%BC%E5%A4%84%E7%90%86 "3.2.5、实验四：特殊值处理")3.2.5、实验四：特殊值处理

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A0%E5%AD%97%E9%9D%A2%E9%87%8F%E8%B5%8B%E5%80%BC "①字面量赋值")①字面量赋值

> 什么是字面量？
> 
> int a = 10;
> 
> 声明一个变量a，初始化为10，此时a就不代表字母a了，而是作为一个变量的名字。当我们引用a的时候，我们实际上拿到的值是10。
> 
> 而如果a是带引号的：’a’，那么它现在不是一个变量，它就是代表a这个字母本身，这就是字面量。所以字面量没有引申含义，就是我们看到的这个数据本身。

xml

|   |   |
|---|---|
|1  <br>2|<!-- 使用value属性给bean的属性赋值时，Spring会把value属性的值看做字面量 -->  <br><property name="name" value="张三"/>|

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A1null%E5%80%BC "②null值")②null值

xml

|   |   |
|---|---|
|1  <br>2  <br>3|<property name="name">  <br>    <null />  <br></property>|

> 注意：
> 
> xml
> 
> |   |   |
> |---|---|
> |1|<property name="name" value="null"></property>|
> 
> 以上写法，为name所赋的值是字符串null

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A2xml%E5%AE%9E%E4%BD%93 "③xml实体")③xml实体

xml

|   |   |
|---|---|
|1  <br>2  <br>3|<!-- 小于号在XML文档中用来定义标签的开始，不能随便使用 -->  <br><!-- 解决方案一：使用XML实体来代替 -->  <br><property name="expression" value="a &lt; b"/>|

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A3CDATA%E8%8A%82 "④CDATA节")④CDATA节

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7|<property name="expression">  <br>    <!-- 解决方案二：使用CDATA节 -->  <br>    <!-- CDATA中的C代表Character，是文本、字符的含义，CDATA就表示纯文本数据 -->  <br>    <!-- XML解析器看到CDATA节就知道这里是纯文本，就不会当作XML标签或属性来解析 -->  <br>    <!-- 所以CDATA节中写什么符号都随意 -->  <br>    <value><![CDATA[a < b]]></value>  <br></property>|

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-2-6%E3%80%81%E5%AE%9E%E9%AA%8C%E4%BA%94%EF%BC%9A%E4%B8%BA%E5%AF%B9%E8%B1%A1%E7%B1%BB%E5%9E%8B%E5%B1%9E%E6%80%A7%E8%B5%8B%E5%80%BC "3.2.6、实验五：为对象类型属性赋值")3.2.6、实验五：为对象类型属性赋值

**①创建班级类Clazz**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40|package com.atguigu.spring6.bean  <br>      <br>public class Clazz {  <br>  <br>    private Integer clazzId;  <br>  <br>    private String clazzName;  <br>  <br>    public Integer getClazzId() {  <br>        return clazzId;  <br>    }  <br>  <br>    public void setClazzId(Integer clazzId) {  <br>        this.clazzId = clazzId;  <br>    }  <br>  <br>    public String getClazzName() {  <br>        return clazzName;  <br>    }  <br>  <br>    public void setClazzName(String clazzName) {  <br>        this.clazzName = clazzName;  <br>    }  <br>  <br>    @Override  <br>    public String toString() {  <br>        return "Clazz{" +  <br>                "clazzId=" + clazzId +  <br>                ", clazzName='" + clazzName + '\'' +  <br>                '}';  <br>    }  <br>  <br>    public Clazz() {  <br>    }  <br>  <br>    public Clazz(Integer clazzId, String clazzName) {  <br>        this.clazzId = clazzId;  <br>        this.clazzName = clazzName;  <br>    }  <br>}|

**②修改Student类**

在Student类中添加以下代码：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9|private Clazz clazz;  <br>  <br>public Clazz getClazz() {  <br>	return clazz;  <br>}  <br>  <br>public void setClazz(Clazz clazz) {  <br>	this.clazz = clazz;  <br>}|

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E6%96%B9%E5%BC%8F%E4%B8%80%EF%BC%9A%E5%BC%95%E7%94%A8%E5%A4%96%E9%83%A8bean "方式一：引用外部bean")方式一：引用外部bean

配置Clazz类型的bean：

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4|<bean id="clazzOne" class="com.atguigu.spring6.bean.Clazz">  <br>    <property name="clazzId" value="1111"></property>  <br>    <property name="clazzName" value="财源滚滚班"></property>  <br></bean>|

为Student中的clazz属性赋值：

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8|<bean id="studentFour" class="com.atguigu.spring6.bean.Student">  <br>    <property name="id" value="1004"></property>  <br>    <property name="name" value="赵六"></property>  <br>    <property name="age" value="26"></property>  <br>    <property name="sex" value="女"></property>  <br>    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->  <br>    <property name="clazz" ref="clazzOne"></property>  <br></bean>|

错误演示：

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7|<bean id="studentFour" class="com.atguigu.spring6.bean.Student">  <br>    <property name="id" value="1004"></property>  <br>    <property name="name" value="赵六"></property>  <br>    <property name="age" value="26"></property>  <br>    <property name="sex" value="女"></property>  <br>    <property name="clazz" value="clazzOne"></property>  <br></bean>|

> 如果错把ref属性写成了value属性，会抛出异常： Caused by: java.lang.IllegalStateException: Cannot convert value of type ‘java.lang.String’ to required type ‘com.atguigu.spring6.bean.Clazz’ for property ‘clazz’: no matching editors or conversion strategy found
> 
> 意思是不能把String类型转换成我们要的Clazz类型，说明我们使用value属性时，Spring只把这个属性看做一个普通的字符串，不会认为这是一个bean的id，更不会根据它去找到bean来赋值

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E6%96%B9%E5%BC%8F%E4%BA%8C%EF%BC%9A%E5%86%85%E9%83%A8bean "方式二：内部bean")方式二：内部bean

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14|<bean id="studentFour" class="com.atguigu.spring6.bean.Student">  <br>    <property name="id" value="1004"></property>  <br>    <property name="name" value="赵六"></property>  <br>    <property name="age" value="26"></property>  <br>    <property name="sex" value="女"></property>  <br>    <property name="clazz">  <br>        <!-- 在一个bean中再声明一个bean就是内部bean -->  <br>        <!-- 内部bean只能用于给属性赋值，不能在外部通过IOC容器获取，因此可以省略id属性 -->  <br>        <bean id="clazzInner" class="com.atguigu.spring6.bean.Clazz">  <br>            <property name="clazzId" value="2222"></property>  <br>            <property name="clazzName" value="远大前程班"></property>  <br>        </bean>  <br>    </property>  <br></bean>|

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E6%96%B9%E5%BC%8F%E4%B8%89%EF%BC%9A%E7%BA%A7%E8%81%94%E5%B1%9E%E6%80%A7%E8%B5%8B%E5%80%BC "方式三：级联属性赋值")方式三：级联属性赋值

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9|<bean id="studentFour" class="com.atguigu.spring6.bean.Student">  <br>    <property name="id" value="1004"></property>  <br>    <property name="name" value="赵六"></property>  <br>    <property name="age" value="26"></property>  <br>    <property name="sex" value="女"></property>  <br>    <property name="clazz" ref="clazzOne"></property>  <br>    <property name="clazz.clazzId" value="3333"></property>  <br>    <property name="clazz.clazzName" value="最强王者班"></property>  <br></bean>|

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-2-7%E3%80%81%E5%AE%9E%E9%AA%8C%E5%85%AD%EF%BC%9A%E4%B8%BA%E6%95%B0%E7%BB%84%E7%B1%BB%E5%9E%8B%E5%B1%9E%E6%80%A7%E8%B5%8B%E5%80%BC "3.2.7、实验六：为数组类型属性赋值")3.2.7、实验六：为数组类型属性赋值

**①修改Student类**

在Student类中添加以下代码：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9|private String[] hobbies;  <br>  <br>public String[] getHobbies() {  <br>    return hobbies;  <br>}  <br>  <br>public void setHobbies(String[] hobbies) {  <br>    this.hobbies = hobbies;  <br>}|

**②配置bean**

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15|<bean id="studentFour" class="com.atguigu.spring.bean6.Student">  <br>    <property name="id" value="1004"></property>  <br>    <property name="name" value="赵六"></property>  <br>    <property name="age" value="26"></property>  <br>    <property name="sex" value="女"></property>  <br>    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->  <br>    <property name="clazz" ref="clazzOne"></property>  <br>    <property name="hobbies">  <br>        <array>  <br>            <value>抽烟</value>  <br>            <value>喝酒</value>  <br>            <value>烫头</value>  <br>        </array>  <br>    </property>  <br></bean>|

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-2-8%E3%80%81%E5%AE%9E%E9%AA%8C%E4%B8%83%EF%BC%9A%E4%B8%BA%E9%9B%86%E5%90%88%E7%B1%BB%E5%9E%8B%E5%B1%9E%E6%80%A7%E8%B5%8B%E5%80%BC "3.2.8、实验七：为集合类型属性赋值")3.2.8、实验七：为集合类型属性赋值

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A0%E4%B8%BAList%E9%9B%86%E5%90%88%E7%B1%BB%E5%9E%8B%E5%B1%9E%E6%80%A7%E8%B5%8B%E5%80%BC "①为List集合类型属性赋值")①为List集合类型属性赋值

在Clazz类中添加以下代码：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9|private List<Student> students;  <br>  <br>public List<Student> getStudents() {  <br>    return students;  <br>}  <br>  <br>public void setStudents(List<Student> students) {  <br>    this.students = students;  <br>}|

配置bean：

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11|<bean id="clazzTwo" class="com.atguigu.spring6.bean.Clazz">  <br>    <property name="clazzId" value="4444"></property>  <br>    <property name="clazzName" value="Javaee0222"></property>  <br>    <property name="students">  <br>        <list>  <br>            <ref bean="studentOne"></ref>  <br>            <ref bean="studentTwo"></ref>  <br>            <ref bean="studentThree"></ref>  <br>        </list>  <br>    </property>  <br></bean>|

> 若为Set集合类型属性赋值，只需要将其中的list标签改为set标签即可

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A1%E4%B8%BAMap%E9%9B%86%E5%90%88%E7%B1%BB%E5%9E%8B%E5%B1%9E%E6%80%A7%E8%B5%8B%E5%80%BC "②为Map集合类型属性赋值")②为Map集合类型属性赋值

创建教师类Teacher：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40|package com.atguigu.spring6.bean;  <br>public class Teacher {  <br>  <br>    private Integer teacherId;  <br>  <br>    private String teacherName;  <br>  <br>    public Integer getTeacherId() {  <br>        return teacherId;  <br>    }  <br>  <br>    public void setTeacherId(Integer teacherId) {  <br>        this.teacherId = teacherId;  <br>    }  <br>  <br>    public String getTeacherName() {  <br>        return teacherName;  <br>    }  <br>  <br>    public void setTeacherName(String teacherName) {  <br>        this.teacherName = teacherName;  <br>    }  <br>  <br>    public Teacher(Integer teacherId, String teacherName) {  <br>        this.teacherId = teacherId;  <br>        this.teacherName = teacherName;  <br>    }  <br>  <br>    public Teacher() {  <br>  <br>    }  <br>      <br>    @Override  <br>    public String toString() {  <br>        return "Teacher{" +  <br>                "teacherId=" + teacherId +  <br>                ", teacherName='" + teacherName + '\'' +  <br>                '}';  <br>    }  <br>}|

在Student类中添加以下代码：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9|private Map<String, Teacher> teacherMap;  <br>  <br>public Map<String, Teacher> getTeacherMap() {  <br>    return teacherMap;  <br>}  <br>  <br>public void setTeacherMap(Map<String, Teacher> teacherMap) {  <br>    this.teacherMap = teacherMap;  <br>}|

配置bean：

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40  <br>41|<bean id="teacherOne" class="com.atguigu.spring6.bean.Teacher">  <br>    <property name="teacherId" value="10010"></property>  <br>    <property name="teacherName" value="大宝"></property>  <br></bean>  <br>  <br><bean id="teacherTwo" class="com.atguigu.spring6.bean.Teacher">  <br>    <property name="teacherId" value="10086"></property>  <br>    <property name="teacherName" value="二宝"></property>  <br></bean>  <br>  <br><bean id="studentFour" class="com.atguigu.spring6.bean.Student">  <br>    <property name="id" value="1004"></property>  <br>    <property name="name" value="赵六"></property>  <br>    <property name="age" value="26"></property>  <br>    <property name="sex" value="女"></property>  <br>    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->  <br>    <property name="clazz" ref="clazzOne"></property>  <br>    <property name="hobbies">  <br>        <array>  <br>            <value>抽烟</value>  <br>            <value>喝酒</value>  <br>            <value>烫头</value>  <br>        </array>  <br>    </property>  <br>    <property name="teacherMap">  <br>        <map>  <br>            <entry>  <br>                <key>  <br>                    <value>10010</value>  <br>                </key>  <br>                <ref bean="teacherOne"></ref>  <br>            </entry>  <br>            <entry>  <br>                <key>  <br>                    <value>10086</value>  <br>                </key>  <br>                <ref bean="teacherTwo"></ref>  <br>            </entry>  <br>        </map>  <br>    </property>  <br></bean>|

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A2%E5%BC%95%E7%94%A8%E9%9B%86%E5%90%88%E7%B1%BB%E5%9E%8B%E7%9A%84bean "③引用集合类型的bean")③引用集合类型的bean

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40  <br>41  <br>42|<!--list集合类型的bean-->  <br><util:list id="students">  <br>    <ref bean="studentOne"></ref>  <br>    <ref bean="studentTwo"></ref>  <br>    <ref bean="studentThree"></ref>  <br></util:list>  <br><!--map集合类型的bean-->  <br><util:map id="teacherMap">  <br>    <entry>  <br>        <key>  <br>            <value>10010</value>  <br>        </key>  <br>        <ref bean="teacherOne"></ref>  <br>    </entry>  <br>    <entry>  <br>        <key>  <br>            <value>10086</value>  <br>        </key>  <br>        <ref bean="teacherTwo"></ref>  <br>    </entry>  <br></util:map>  <br><bean id="clazzTwo" class="com.atguigu.spring6.bean.Clazz">  <br>    <property name="clazzId" value="4444"></property>  <br>    <property name="clazzName" value="Javaee0222"></property>  <br>    <property name="students" ref="students"></property>  <br></bean>  <br><bean id="studentFour" class="com.atguigu.spring6.bean.Student">  <br>    <property name="id" value="1004"></property>  <br>    <property name="name" value="赵六"></property>  <br>    <property name="age" value="26"></property>  <br>    <property name="sex" value="女"></property>  <br>    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->  <br>    <property name="clazz" ref="clazzOne"></property>  <br>    <property name="hobbies">  <br>        <array>  <br>            <value>抽烟</value>  <br>            <value>喝酒</value>  <br>            <value>烫头</value>  <br>        </array>  <br>    </property>  <br>    <property name="teacherMap" ref="teacherMap"></property>  <br></bean>|

> 使用util:list、util:map标签必须引入相应的命名空间
> 
> xml
> 
> |   |   |
> |---|---|
> |1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8|<?xml version="1.0" encoding="UTF-8"?>  <br><beans xmlns="http://www.springframework.org/schema/beans"  <br>       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  <br>       xmlns:util="http://www.springframework.org/schema/util"  <br>       xsi:schemaLocation="http://www.springframework.org/schema/util  <br>       http://www.springframework.org/schema/util/spring-util.xsd  <br>       http://www.springframework.org/schema/beans  <br>       http://www.springframework.org/schema/beans/spring-beans.xsd">|

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-2-9%E3%80%81%E5%AE%9E%E9%AA%8C%E5%85%AB%EF%BC%9Ap%E5%91%BD%E5%90%8D%E7%A9%BA%E9%97%B4 "3.2.9、实验八：p命名空间")3.2.9、实验八：p命名空间

引入p命名空间

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9|<?xml version="1.0" encoding="UTF-8"?>  <br><beans xmlns="http://www.springframework.org/schema/beans"  <br>       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  <br>       xmlns:util="http://www.springframework.org/schema/util"  <br>       xmlns:p="http://www.springframework.org/schema/p"  <br>       xsi:schemaLocation="http://www.springframework.org/schema/util  <br>       http://www.springframework.org/schema/util/spring-util.xsd  <br>       http://www.springframework.org/schema/beans  <br>       http://www.springframework.org/schema/beans/spring-beans.xsd">|

引入p命名空间后，可以通过以下方式为bean的各个属性赋值

xml

|   |   |
|---|---|
|1  <br>2|<bean id="studentSix" class="com.atguigu.spring6.bean.Student"  <br>    p:id="1006" p:name="小明" p:clazz-ref="clazzOne" p:teacherMap-ref="teacherMap"></bean>|

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-2-10%E3%80%81%E5%AE%9E%E9%AA%8C%E4%B9%9D%EF%BC%9A%E5%BC%95%E5%85%A5%E5%A4%96%E9%83%A8%E5%B1%9E%E6%80%A7%E6%96%87%E4%BB%B6 "3.2.10、实验九：引入外部属性文件")3.2.10、实验九：引入外部属性文件

**①加入依赖**

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13|<!-- MySQL驱动 -->  <br><dependency>  <br>    <groupId>mysql</groupId>  <br>    <artifactId>mysql-connector-java</artifactId>  <br>    <version>8.0.30</version>  <br></dependency>  <br>  <br><!-- 数据源 -->  <br><dependency>  <br>    <groupId>com.alibaba</groupId>  <br>    <artifactId>druid</artifactId>  <br>    <version>1.2.15</version>  <br></dependency>|

**②创建外部属性文件**

[![images](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img010.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img010.png)

properties

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4|jdbc.user=root  <br>jdbc.password=atguigu  <br>jdbc.url=jdbc:mysql://localhost:3306/ssm?serverTimezone=UTC  <br>jdbc.driver=com.mysql.cj.jdbc.Driver|

**③引入属性文件**

引入context 名称空间

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10|<?xml version="1.0" encoding="UTF-8"?>  <br><beans xmlns="http://www.springframework.org/schema/beans"  <br>       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  <br>       xmlns:context="http://www.springframework.org/schema/context"  <br>       xsi:schemaLocation="http://www.springframework.org/schema/beans  <br>       http://www.springframework.org/schema/beans/spring-beans.xsd  <br>       http://www.springframework.org/schema/context  <br>       http://www.springframework.org/schema/context/spring-context.xsd">  <br>  <br></beans>|

xml

|   |   |
|---|---|
|1  <br>2|<!-- 引入外部属性文件 -->  <br><context:property-placeholder location="classpath:jdbc.properties"/>|

注意：在使用 [context:property-placeholder](context:property-placeholder) 元素加载外包配置文件功能前，首先需要在 XML 配置的一级标签 中添加 context 相关的约束。

**④配置bean**

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|<bean id="druidDataSource" class="com.alibaba.druid.pool.DruidDataSource">  <br>    <property name="url" value="${jdbc.url}"/>  <br>    <property name="driverClassName" value="${jdbc.driver}"/>  <br>    <property name="username" value="${jdbc.user}"/>  <br>    <property name="password" value="${jdbc.password}"/>  <br></bean>|

**⑤测试**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7|@Test  <br>public void testDataSource() throws SQLException {  <br>    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-datasource.xml");  <br>    DataSource dataSource = ac.getBean(DataSource.class);  <br>    Connection connection = dataSource.getConnection();  <br>    System.out.println(connection);  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-2-11%E3%80%81%E5%AE%9E%E9%AA%8C%E5%8D%81%EF%BC%9Abean%E7%9A%84%E4%BD%9C%E7%94%A8%E5%9F%9F "3.2.11、实验十：bean的作用域")3.2.11、实验十：bean的作用域

**①概念**

在Spring中可以通过配置bean标签的scope属性来指定bean的作用域范围，各取值含义参加下表：

|取值|含义|创建对象的时机|
|---|---|---|
|singleton（默认）|在IOC容器中，这个bean的对象始终为单实例|IOC容器初始化时|
|prototype|这个bean在IOC容器中有多个实例|获取bean时|

如果是在WebApplicationContext环境下还会有另外几个作用域（但不常用）：

|取值|含义|
|---|---|
|request|在一个请求范围内有效|
|session|在一个会话范围内有效|

**②创建类User**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40  <br>41  <br>42  <br>43  <br>44  <br>45  <br>46  <br>47  <br>48  <br>49  <br>50  <br>51  <br>52  <br>53  <br>54  <br>55  <br>56  <br>57  <br>58  <br>59  <br>60  <br>61  <br>62  <br>63|package com.atguigu.spring6.bean;  <br>public class User {  <br>  <br>    private Integer id;  <br>  <br>    private String username;  <br>  <br>    private String password;  <br>  <br>    private Integer age;  <br>  <br>    public User() {  <br>    }  <br>  <br>    public User(Integer id, String username, String password, Integer age) {  <br>        this.id = id;  <br>        this.username = username;  <br>        this.password = password;  <br>        this.age = age;  <br>    }  <br>  <br>    public Integer getId() {  <br>        return id;  <br>    }  <br>  <br>    public void setId(Integer id) {  <br>        this.id = id;  <br>    }  <br>  <br>    public String getUsername() {  <br>        return username;  <br>    }  <br>  <br>    public void setUsername(String username) {  <br>        this.username = username;  <br>    }  <br>  <br>    public String getPassword() {  <br>        return password;  <br>    }  <br>  <br>    public void setPassword(String password) {  <br>        this.password = password;  <br>    }  <br>  <br>    public Integer getAge() {  <br>        return age;  <br>    }  <br>  <br>    public void setAge(Integer age) {  <br>        this.age = age;  <br>    }  <br>  <br>    @Override  <br>    public String toString() {  <br>        return "User{" +  <br>                "id=" + id +  <br>                ", username='" + username + '\'' +  <br>                ", password='" + password + '\'' +  <br>                ", age=" + age +  <br>                '}';  <br>    }  <br>}|

**③配置bean**

xml

|   |   |
|---|---|
|1  <br>2  <br>3|<!-- scope属性：取值singleton（默认值），bean在IOC容器中只有一个实例，IOC容器初始化时创建对象 -->  <br><!-- scope属性：取值prototype，bean在IOC容器中可以有多个实例，getBean()时创建对象 -->  <br><bean class="com.atguigu.spring6.bean.User" scope="prototype"></bean>|

**④测试**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7|@Test  <br>public void testBeanScope(){  <br>    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-scope.xml");  <br>    User user1 = ac.getBean(User.class);  <br>    User user2 = ac.getBean(User.class);  <br>    System.out.println(user1==user2);  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-2-12%E3%80%81%E5%AE%9E%E9%AA%8C%E5%8D%81%E4%B8%80%EF%BC%9Abean%E7%94%9F%E5%91%BD%E5%91%A8%E6%9C%9F "3.2.12、实验十一：bean生命周期")3.2.12、实验十一：bean生命周期

**①具体的生命周期过程**

- bean对象创建（调用无参构造器）
    
- 给bean对象设置属性
    
- bean的后置处理器（初始化之前）
    
- bean对象初始化（需在配置bean时指定初始化方法）
    
- bean的后置处理器（初始化之后）
    
- bean对象就绪可以使用
    
- bean对象销毁（需在配置bean时指定销毁方法）
    
- IOC容器关闭
    

**②修改类User**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40  <br>41  <br>42  <br>43  <br>44  <br>45  <br>46  <br>47  <br>48  <br>49  <br>50  <br>51  <br>52  <br>53  <br>54  <br>55  <br>56  <br>57  <br>58  <br>59  <br>60  <br>61  <br>62  <br>63  <br>64  <br>65  <br>66  <br>67  <br>68  <br>69  <br>70  <br>71  <br>72|public class User {  <br>  <br>    private Integer id;  <br>  <br>    private String username;  <br>  <br>    private String password;  <br>  <br>    private Integer age;  <br>  <br>    public User() {  <br>        System.out.println("生命周期：1、创建对象");  <br>    }  <br>  <br>    public User(Integer id, String username, String password, Integer age) {  <br>        this.id = id;  <br>        this.username = username;  <br>        this.password = password;  <br>        this.age = age;  <br>    }  <br>  <br>    public Integer getId() {  <br>        return id;  <br>    }  <br>  <br>    public void setId(Integer id) {  <br>        System.out.println("生命周期：2、依赖注入");  <br>        this.id = id;  <br>    }  <br>  <br>    public String getUsername() {  <br>        return username;  <br>    }  <br>  <br>    public void setUsername(String username) {  <br>        this.username = username;  <br>    }  <br>  <br>    public String getPassword() {  <br>        return password;  <br>    }  <br>  <br>    public void setPassword(String password) {  <br>        this.password = password;  <br>    }  <br>  <br>    public Integer getAge() {  <br>        return age;  <br>    }  <br>  <br>    public void setAge(Integer age) {  <br>        this.age = age;  <br>    }  <br>  <br>    public void initMethod(){  <br>        System.out.println("生命周期：3、初始化");  <br>    }  <br>  <br>    public void destroyMethod(){  <br>        System.out.println("生命周期：5、销毁");  <br>    }  <br>  <br>    @Override  <br>    public String toString() {  <br>        return "User{" +  <br>                "id=" + id +  <br>                ", username='" + username + '\'' +  <br>                ", password='" + password + '\'' +  <br>                ", age=" + age +  <br>                '}';  <br>    }  <br>}|

> 注意其中的initMethod()和destroyMethod()，可以通过配置bean指定为初始化和销毁的方法

**③配置bean**

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8|<!-- 使用init-method属性指定初始化方法 -->  <br><!-- 使用destroy-method属性指定销毁方法 -->  <br><bean class="com.atguigu.spring6.bean.User" scope="prototype" init-method="initMethod" destroy-method="destroyMethod">  <br>    <property name="id" value="1001"></property>  <br>    <property name="username" value="admin"></property>  <br>    <property name="password" value="123456"></property>  <br>    <property name="age" value="23"></property>  <br></bean>|

**④测试**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7|@Test  <br>public void testLife(){  <br>    ClassPathXmlApplicationContext ac = new ClassPathXmlApplicationContext("spring-lifecycle.xml");  <br>    User bean = ac.getBean(User.class);  <br>    System.out.println("生命周期：4、通过IOC容器获取bean并使用");  <br>    ac.close();  <br>}|

**⑤bean的后置处理器**

bean的后置处理器会在生命周期的初始化前后添加额外的操作，需要实现BeanPostProcessor接口，且配置到IOC容器中，需要注意的是，bean后置处理器不是单独针对某一个bean生效，而是针对IOC容器中所有bean都会执行

创建bean的后置处理器：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19|package com.atguigu.spring6.process;  <br>      <br>import org.springframework.beans.BeansException;  <br>import org.springframework.beans.factory.config.BeanPostProcessor;  <br>  <br>public class MyBeanProcessor implements BeanPostProcessor {  <br>      <br>    @Override  <br>    public Object postProcessBeforeInitialization(Object bean, String beanName) throws BeansException {  <br>        System.out.println("☆☆☆" + beanName + " = " + bean);  <br>        return bean;  <br>    }  <br>      <br>    @Override  <br>    public Object postProcessAfterInitialization(Object bean, String beanName) throws BeansException {  <br>        System.out.println("★★★" + beanName + " = " + bean);  <br>        return bean;  <br>    }  <br>}|

在IOC容器中配置后置处理器：

xml

|   |   |
|---|---|
|1  <br>2|<!-- bean的后置处理器要放入IOC容器才能生效 -->  <br><bean id="myBeanProcessor" class="com.atguigu.spring6.process.MyBeanProcessor"/>|

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-2-13%E3%80%81%E5%AE%9E%E9%AA%8C%E5%8D%81%E4%BA%8C%EF%BC%9AFactoryBean "3.2.13、实验十二：FactoryBean")3.2.13、实验十二：FactoryBean

**①简介**

FactoryBean是Spring提供的一种整合第三方框架的常用机制。和普通的bean不同，配置一个FactoryBean类型的bean，在获取bean的时候得到的并不是class属性中配置的这个类的对象，而是getObject()方法的返回值。通过这种机制，Spring可以帮我们把复杂组件创建的详细过程和繁琐细节都屏蔽起来，只把最简洁的使用界面展示给我们。

将来我们整合Mybatis时，Spring就是通过FactoryBean机制来帮我们创建SqlSessionFactory对象的。

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40  <br>41  <br>42  <br>43  <br>44  <br>45  <br>46  <br>47  <br>48  <br>49  <br>50  <br>51  <br>52  <br>53  <br>54  <br>55  <br>56  <br>57  <br>58  <br>59  <br>60  <br>61  <br>62  <br>63  <br>64  <br>65  <br>66  <br>67  <br>68  <br>69  <br>70  <br>71  <br>72  <br>73  <br>74  <br>75  <br>76  <br>77  <br>78  <br>79  <br>80  <br>81  <br>82  <br>83  <br>84  <br>85  <br>86  <br>87  <br>88  <br>89  <br>90  <br>91  <br>92  <br>93  <br>94  <br>95  <br>96  <br>97  <br>98  <br>99  <br>100  <br>101  <br>102  <br>103  <br>104  <br>105  <br>106  <br>107  <br>108  <br>109  <br>110  <br>111  <br>112  <br>113  <br>114  <br>115  <br>116  <br>117  <br>118  <br>119  <br>120  <br>121  <br>122  <br>123  <br>124  <br>125  <br>126  <br>127  <br>128  <br>129  <br>130  <br>131  <br>132  <br>133  <br>134  <br>135  <br>136  <br>137  <br>138  <br>139  <br>140  <br>141  <br>142  <br>143  <br>144  <br>145  <br>146|/*  <br> * Copyright 2002-2020 the original author or authors.  <br> *  <br> * Licensed under the Apache License, Version 2.0 (the "License");  <br> * you may not use this file except in compliance with the License.  <br> * You may obtain a copy of the License at  <br> *  <br> *      https://www.apache.org/licenses/LICENSE-2.0  <br> *  <br> * Unless required by applicable law or agreed to in writing, software  <br> * distributed under the License is distributed on an "AS IS" BASIS,  <br> * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  <br> * See the License for the specific language governing permissions and  <br> * limitations under the License.  <br> */  <br>package org.springframework.beans.factory;  <br>  <br>import org.springframework.lang.Nullable;  <br>  <br>/**  <br> * Interface to be implemented by objects used within a {@link BeanFactory} which  <br> * are themselves factories for individual objects. If a bean implements this  <br> * interface, it is used as a factory for an object to expose, not directly as a  <br> * bean instance that will be exposed itself.  <br> *  <br> * <p><b>NB: A bean that implements this interface cannot be used as a normal bean.</b>  <br> * A FactoryBean is defined in a bean style, but the object exposed for bean  <br> * references ({@link #getObject()}) is always the object that it creates.  <br> *  <br> * <p>FactoryBeans can support singletons and prototypes, and can either create  <br> * objects lazily on demand or eagerly on startup. The {@link SmartFactoryBean}  <br> * interface allows for exposing more fine-grained behavioral metadata.  <br> *  <br> * <p>This interface is heavily used within the framework itself, for example for  <br> * the AOP {@link org.springframework.aop.framework.ProxyFactoryBean} or the  <br> * {@link org.springframework.jndi.JndiObjectFactoryBean}. It can be used for  <br> * custom components as well; however, this is only common for infrastructure code.  <br> *  <br> * <p><b>{@code FactoryBean} is a programmatic contract. Implementations are not  <br> * supposed to rely on annotation-driven injection or other reflective facilities.</b>  <br> * {@link #getObjectType()} {@link #getObject()} invocations may arrive early in the  <br> * bootstrap process, even ahead of any post-processor setup. If you need access to  <br> * other beans, implement {@link BeanFactoryAware} and obtain them programmatically.  <br> *  <br> * <p><b>The container is only responsible for managing the lifecycle of the FactoryBean  <br> * instance, not the lifecycle of the objects created by the FactoryBean.</b> Therefore,  <br> * a destroy method on an exposed bean object (such as {@link java.io.Closeable#close()}  <br> * will <i>not</i> be called automatically. Instead, a FactoryBean should implement  <br> * {@link DisposableBean} and delegate any such close call to the underlying object.  <br> *  <br> * <p>Finally, FactoryBean objects participate in the containing BeanFactory's  <br> * synchronization of bean creation. There is usually no need for internal  <br> * synchronization other than for purposes of lazy initialization within the  <br> * FactoryBean itself (or the like).  <br> *  <br> * @author Rod Johnson  <br> * @author Juergen Hoeller  <br> * @since 08.03.2003  <br> * @param <T> the bean type  <br> * @see org.springframework.beans.factory.BeanFactory  <br> * @see org.springframework.aop.framework.ProxyFactoryBean  <br> * @see org.springframework.jndi.JndiObjectFactoryBean  <br> */  <br>public interface FactoryBean<T> {  <br>  <br>    /**  <br>     * The name of an attribute that can be  <br>     * {@link org.springframework.core.AttributeAccessor#setAttribute set} on a  <br>     * {@link org.springframework.beans.factory.config.BeanDefinition} so that  <br>     * factory beans can signal their object type when it can't be deduced from  <br>     * the factory bean class.  <br>     * @since 5.2  <br>     */  <br>    String OBJECT_TYPE_ATTRIBUTE = "factoryBeanObjectType";  <br>  <br>    /**  <br>     * Return an instance (possibly shared or independent) of the object  <br>     * managed by this factory.  <br>     * <p>As with a {@link BeanFactory}, this allows support for both the  <br>     * Singleton and Prototype design pattern.  <br>     * <p>If this FactoryBean is not fully initialized yet at the time of  <br>     * the call (for example because it is involved in a circular reference),  <br>     * throw a corresponding {@link FactoryBeanNotInitializedException}.  <br>     * <p>As of Spring 2.0, FactoryBeans are allowed to return {@code null}  <br>     * objects. The factory will consider this as normal value to be used; it  <br>     * will not throw a FactoryBeanNotInitializedException in this case anymore.  <br>     * FactoryBean implementations are encouraged to throw  <br>     * FactoryBeanNotInitializedException themselves now, as appropriate.  <br>     * @return an instance of the bean (can be {@code null})  <br>     * @throws Exception in case of creation errors  <br>     * @see FactoryBeanNotInitializedException  <br>     */  <br>    @Nullable  <br>    T getObject() throws Exception;  <br>  <br>    /**  <br>     * Return the type of object that this FactoryBean creates,  <br>     * or {@code null} if not known in advance.  <br>     * <p>This allows one to check for specific types of beans without  <br>     * instantiating objects, for example on autowiring.  <br>     * <p>In the case of implementations that are creating a singleton object,  <br>     * this method should try to avoid singleton creation as far as possible;  <br>     * it should rather estimate the type in advance.  <br>     * For prototypes, returning a meaningful type here is advisable too.  <br>     * <p>This method can be called <i>before</i> this FactoryBean has  <br>     * been fully initialized. It must not rely on state created during  <br>     * initialization; of course, it can still use such state if available.  <br>     * <p><b>NOTE:</b> Autowiring will simply ignore FactoryBeans that return  <br>     * {@code null} here. Therefore it is highly recommended to implement  <br>     * this method properly, using the current state of the FactoryBean.  <br>     * @return the type of object that this FactoryBean creates,  <br>     * or {@code null} if not known at the time of the call  <br>     * @see ListableBeanFactory#getBeansOfType  <br>     */  <br>    @Nullable  <br>    Class<?> getObjectType();  <br>  <br>    /**  <br>     * Is the object managed by this factory a singleton? That is,  <br>     * will {@link #getObject()} always return the same object  <br>     * (a reference that can be cached)?  <br>     * <p><b>NOTE:</b> If a FactoryBean indicates to hold a singleton object,  <br>     * the object returned from {@code getObject()} might get cached  <br>     * by the owning BeanFactory. Hence, do not return {@code true}  <br>     * unless the FactoryBean always exposes the same reference.  <br>     * <p>The singleton status of the FactoryBean itself will generally  <br>     * be provided by the owning BeanFactory; usually, it has to be  <br>     * defined as singleton there.  <br>     * <p><b>NOTE:</b> This method returning {@code false} does not  <br>     * necessarily indicate that returned objects are independent instances.  <br>     * An implementation of the extended {@link SmartFactoryBean} interface  <br>     * may explicitly indicate independent instances through its  <br>     * {@link SmartFactoryBean#isPrototype()} method. Plain {@link FactoryBean}  <br>     * implementations which do not implement this extended interface are  <br>     * simply assumed to always return independent instances if the  <br>     * {@code isSingleton()} implementation returns {@code false}.  <br>     * <p>The default implementation returns {@code true}, since a  <br>     * {@code FactoryBean} typically manages a singleton instance.  <br>     * @return whether the exposed object is a singleton  <br>     * @see #getObject()  <br>     * @see SmartFactoryBean#isPrototype()  <br>     */  <br>    default boolean isSingleton() {  <br>        return true;  <br>    }  <br>}|

**②创建类UserFactoryBean**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12|package com.atguigu.spring6.bean;  <br>public class UserFactoryBean implements FactoryBean<User> {  <br>    @Override  <br>    public User getObject() throws Exception {  <br>        return new User();  <br>    }  <br>  <br>    @Override  <br>    public Class<?> getObjectType() {  <br>        return User.class;  <br>    }  <br>}|

**③配置bean**

xml

|   |   |
|---|---|
|1|<bean id="user" class="com.atguigu.spring6.bean.UserFactoryBean"></bean>|

**④测试**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7|@Test  <br>public void testUserFactoryBean(){  <br>    //获取IOC容器  <br>    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-factorybean.xml");  <br>    User user = (User) ac.getBean("user");  <br>    System.out.println(user);  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-2-14%E3%80%81%E5%AE%9E%E9%AA%8C%E5%8D%81%E4%B8%89%EF%BC%9A%E5%9F%BA%E4%BA%8Exml%E8%87%AA%E5%8A%A8%E8%A3%85%E9%85%8D "3.2.14、实验十三：基于xml自动装配")3.2.14、实验十三：基于xml自动装配

> 自动装配：
> 
> 根据指定的策略，在IOC容器中匹配某一个bean，自动为指定的bean中所依赖的类类型或接口类型属性赋值

**①场景模拟**

创建类UserController

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14|package com.atguigu.spring6.autowire.controller  <br>public class UserController {  <br>  <br>    private UserService userService;  <br>  <br>    public void setUserService(UserService userService) {  <br>        this.userService = userService;  <br>    }  <br>  <br>    public void saveUser(){  <br>        userService.saveUser();  <br>    }  <br>  <br>}|

创建接口UserService

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|package com.atguigu.spring6.autowire.service  <br>public interface UserService {  <br>  <br>    void saveUser();  <br>  <br>}|

创建类UserServiceImpl实现接口UserService

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15|package com.atguigu.spring6.autowire.service.impl  <br>public class UserServiceImpl implements UserService {  <br>  <br>    private UserDao userDao;  <br>  <br>    public void setUserDao(UserDao userDao) {  <br>        this.userDao = userDao;  <br>    }  <br>  <br>    @Override  <br>    public void saveUser() {  <br>        userDao.saveUser();  <br>    }  <br>  <br>}|

创建接口UserDao

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|package com.atguigu.spring6.autowire.dao  <br>public interface UserDao {  <br>  <br>    void saveUser();  <br>  <br>}|

创建类UserDaoImpl实现接口UserDao

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9|package com.atguigu.spring6.autowire.dao.impl  <br>public class UserDaoImpl implements UserDao {  <br>  <br>    @Override  <br>    public void saveUser() {  <br>        System.out.println("保存成功");  <br>    }  <br>  <br>}|

**②配置bean**

> 使用bean标签的autowire属性设置自动装配效果
> 
> 自动装配方式：byType
> 
> byType：根据类型匹配IOC容器中的某个兼容类型的bean，为属性自动赋值
> 
> 若在IOC中，没有任何一个兼容类型的bean能够为属性赋值，则该属性不装配，即值为默认值null
> 
> 若在IOC中，有多个兼容类型的bean能够为属性赋值，则抛出异常NoUniqueBeanDefinitionException

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5|<bean id="userController" class="com.atguigu.spring6.autowire.controller.UserController" autowire="byType"></bean>  <br>  <br><bean id="userService" class="com.atguigu.spring6.autowire.service.impl.UserServiceImpl" autowire="byType"></bean>  <br>  <br><bean id="userDao" class="com.atguigu.spring6.autowire.dao.impl.UserDaoImpl"></bean>|

> 自动装配方式：byName
> 
> byName：将自动装配的属性的属性名，作为bean的id在IOC容器中匹配相对应的bean进行赋值

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7|<bean id="userController" class="com.atguigu.spring6.autowire.controller.UserController" autowire="byName"></bean>  <br>  <br><bean id="userService" class="com.atguigu.spring6.autowire.service.impl.UserServiceImpl" autowire="byName"></bean>  <br><bean id="userServiceImpl" class="com.atguigu.spring6.autowire.service.impl.UserServiceImpl" autowire="byName"></bean>  <br>  <br><bean id="userDao" class="com.atguigu.spring6.autowire.dao.impl.UserDaoImpl"></bean>  <br><bean id="userDaoImpl" class="com.atguigu.spring6.autowire.dao.impl.UserDaoImpl"></bean>|

**③测试**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|@Test  <br>public void testAutoWireByXML(){  <br>    ApplicationContext ac = new ClassPathXmlApplicationContext("autowire-xml.xml");  <br>    UserController userController = ac.getBean(UserController.class);  <br>    userController.saveUser();  <br>}|

### [](https://blog.mohic.site/2024/05/18/spring6/#3-3%E3%80%81%E5%9F%BA%E4%BA%8E%E6%B3%A8%E8%A7%A3%E7%AE%A1%E7%90%86Bean%EF%BC%88%E2%98%86%EF%BC%89 "3.3、基于注解管理Bean（☆）")3.3、基于注解管理Bean（☆）

从 Java 5 开始，Java 增加了对注解（Annotation）的支持，它是代码中的一种特殊标记，可以在编译、类加载和运行时被读取，执行相应的处理。开发人员可以通过注解在不改变原有代码和逻辑的情况下，在源代码中嵌入补充信息。

Spring 从 2.5 版本开始提供了对注解技术的全面支持，我们可以使用注解来实现自动装配，简化 Spring 的 XML 配置。

Spring 通过注解实现自动装配的步骤如下：

1. 引入依赖
2. 开启组件扫描
3. 使用注解定义 Bean
4. 依赖注入

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-3-1%E3%80%81%E6%90%AD%E5%BB%BA%E5%AD%90%E6%A8%A1%E5%9D%97spring6-ioc-annotation "3.3.1、搭建子模块spring6-ioc-annotation")3.3.1、搭建子模块spring6-ioc-annotation

**①搭建模块**

搭建方式如：spring6-ioc-xml

**②引入配置文件**

引入spring-ioc-xml模块日志log4j2.xml

**③添加依赖**

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27|<dependencies>  <br>    <!--spring context依赖-->  <br>    <!--当你引入Spring Context依赖之后，表示将Spring的基础依赖引入了-->  <br>    <dependency>  <br>        <groupId>org.springframework</groupId>  <br>        <artifactId>spring-context</artifactId>  <br>        <version>6.0.3</version>  <br>    </dependency>  <br>  <br>    <!--junit5测试-->  <br>    <dependency>  <br>        <groupId>org.junit.jupiter</groupId>  <br>        <artifactId>junit-jupiter-api</artifactId>  <br>    </dependency>  <br>  <br>    <!--log4j2的依赖-->  <br>    <dependency>  <br>        <groupId>org.apache.logging.log4j</groupId>  <br>        <artifactId>log4j-core</artifactId>  <br>        <version>2.19.0</version>  <br>    </dependency>  <br>    <dependency>  <br>        <groupId>org.apache.logging.log4j</groupId>  <br>        <artifactId>log4j-slf4j2-impl</artifactId>  <br>        <version>2.19.0</version>  <br>    </dependency>  <br></dependencies>|

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-3-2%E3%80%81%E5%BC%80%E5%90%AF%E7%BB%84%E4%BB%B6%E6%89%AB%E6%8F%8F "3.3.2、开启组件扫描")3.3.2、开启组件扫描

Spring 默认不使用注解装配 Bean，因此我们需要在 Spring 的 XML 配置中，通过 [context:component-scan](context:component-scan) 元素开启 Spring Beans的自动扫描功能。开启此功能后，Spring 会自动从扫描指定的包（base-package 属性设置）及其子包下的所有类，如果类上使用了 @Component 注解，就将该类装配到容器中。

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11|<?xml version="1.0" encoding="UTF-8"?>  <br><beans xmlns="http://www.springframework.org/schema/beans"  <br>       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  <br>       xmlns:context="http://www.springframework.org/schema/context"  <br>       xsi:schemaLocation="http://www.springframework.org/schema/beans  <br>    http://www.springframework.org/schema/beans/spring-beans-3.0.xsd  <br>    http://www.springframework.org/schema/context  <br>            http://www.springframework.org/schema/context/spring-context.xsd">  <br>    <!--开启组件扫描功能-->  <br>    <context:component-scan base-package="com.atguigu.spring6"></context:component-scan>  <br></beans>|

注意：在使用 [context:component-scan](context:component-scan) 元素开启自动扫描功能前，首先需要在 XML 配置的一级标签 中添加 context 相关的约束。

**情况一：最基本的扫描方式**

xml

|   |   |
|---|---|
|1  <br>2|<context:component-scan base-package="com.atguigu.spring6">  <br></context:component-scan>|

**情况二：指定要排除的组件**

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10|<context:component-scan base-package="com.atguigu.spring6">  <br>    <!-- context:exclude-filter标签：指定排除规则 -->  <br>    <!--   <br> 		type：设置排除或包含的依据  <br>		type="annotation"，根据注解排除，expression中设置要排除的注解的全类名  <br>		type="assignable"，根据类型排除，expression中设置要排除的类型的全类名  <br>	-->  <br>    <context:exclude-filter type="annotation" expression="org.springframework.stereotype.Controller"/>  <br>        <!--<context:exclude-filter type="assignable" expression="com.atguigu.spring6.controller.UserController"/>-->  <br></context:component-scan>|

**情况三：仅扫描指定组件**

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12|<context:component-scan base-package="com.atguigu" use-default-filters="false">  <br>    <!-- context:include-filter标签：指定在原有扫描规则的基础上追加的规则 -->  <br>    <!-- use-default-filters属性：取值false表示关闭默认扫描规则 -->  <br>    <!-- 此时必须设置use-default-filters="false"，因为默认规则即扫描指定包下所有类 -->  <br>    <!--   <br> 		type：设置排除或包含的依据  <br>		type="annotation"，根据注解排除，expression中设置要排除的注解的全类名  <br>		type="assignable"，根据类型排除，expression中设置要排除的类型的全类名  <br>	-->  <br>    <context:include-filter type="annotation" expression="org.springframework.stereotype.Controller"/>  <br>	<!--<context:include-filter type="assignable" expression="com.atguigu.spring6.controller.UserController"/>-->  <br></context:component-scan>|

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-3-3%E3%80%81%E4%BD%BF%E7%94%A8%E6%B3%A8%E8%A7%A3%E5%AE%9A%E4%B9%89-Bean "3.3.3、使用注解定义 Bean")3.3.3、使用注解定义 Bean

Spring 提供了以下多个注解，这些注解可以直接标注在 Java 类上，将它们定义成 Spring Bean。

|注解|说明|
|---|---|
|@Component|该注解用于描述 Spring 中的 Bean，它是一个泛化的概念，仅仅表示容器中的一个组件（Bean），并且可以作用在应用的任何层次，例如 Service 层、Dao 层等。 使用时只需将该注解标注在相应类上即可。|
|@Repository|该注解用于将数据访问层（Dao 层）的类标识为 Spring 中的 Bean，其功能与 @Component 相同。|
|@Service|该注解通常作用在业务层（Service 层），用于将业务层的类标识为 Spring 中的 Bean，其功能与 @Component 相同。|
|@Controller|该注解通常作用在控制层（如SpringMVC 的 Controller），用于将控制层的类标识为 Spring 中的 Bean，其功能与 @Component 相同。|

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-3-4%E3%80%81%E5%AE%9E%E9%AA%8C%E4%B8%80%EF%BC%9A-Autowired%E6%B3%A8%E5%85%A5 "3.3.4、实验一：@Autowired注入")3.3.4、实验一：@Autowired注入

单独使用@Autowired注解，**默认根据类型装配**。【默认是byType】

查看源码：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14|package org.springframework.beans.factory.annotation;  <br>  <br>import java.lang.annotation.Documented;  <br>import java.lang.annotation.ElementType;  <br>import java.lang.annotation.Retention;  <br>import java.lang.annotation.RetentionPolicy;  <br>import java.lang.annotation.Target;  <br>  <br>@Target({ElementType.CONSTRUCTOR, ElementType.METHOD, ElementType.PARAMETER, ElementType.FIELD, ElementType.ANNOTATION_TYPE})  <br>@Retention(RetentionPolicy.RUNTIME)  <br>@Documented  <br>public @interface Autowired {  <br>    boolean required() default true;  <br>}|

源码中有两处需要注意：

- 第一处：该注解可以标注在哪里？
    
- - 构造方法上
    - 方法上
    - 形参上
    - 属性上
    - 注解上
- 第二处：该注解有一个required属性，默认值是true，表示在注入的时候要求被注入的Bean必须是存在的，如果不存在则报错。如果required属性设置为false，表示注入的Bean存在或者不存在都没关系，存在的话就注入，不存在的话，也不报错。
    

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A0%E5%9C%BA%E6%99%AF%E4%B8%80%EF%BC%9A%E5%B1%9E%E6%80%A7%E6%B3%A8%E5%85%A5 "①场景一：属性注入")①场景一：属性注入

创建UserDao接口

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|package com.atguigu.spring6.dao;  <br>  <br>public interface UserDao {  <br>  <br>    public void print();  <br>}|

创建UserDaoImpl实现

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13|package com.atguigu.spring6.dao.impl;  <br>  <br>import com.atguigu.spring6.dao.UserDao;  <br>import org.springframework.stereotype.Repository;  <br>  <br>@Repository  <br>public class UserDaoImpl implements UserDao {  <br>  <br>    @Override  <br>    public void print() {  <br>        System.out.println("Dao层执行结束");  <br>    }  <br>}|

创建UserService接口

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|package com.atguigu.spring6.service;  <br>  <br>public interface UserService {  <br>  <br>    public void out();  <br>}|

创建UserServiceImpl实现类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19|package com.atguigu.spring6.service.impl;  <br>  <br>import com.atguigu.spring6.dao.UserDao;  <br>import com.atguigu.spring6.service.UserService;  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.stereotype.Service;  <br>  <br>@Service  <br>public class UserServiceImpl implements UserService {  <br>  <br>    @Autowired  <br>    private UserDao userDao;  <br>  <br>    @Override  <br>    public void out() {  <br>        userDao.print();  <br>        System.out.println("Service层执行结束");  <br>    }  <br>}|

创建UserController类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18|package com.atguigu.spring6.controller;  <br>  <br>import com.atguigu.spring6.service.UserService;  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.stereotype.Controller;  <br>  <br>@Controller  <br>public class UserController {  <br>  <br>    @Autowired  <br>    private UserService userService;  <br>  <br>    public void out() {  <br>        userService.out();  <br>        System.out.println("Controller层执行结束。");  <br>    }  <br>  <br>}|

**测试一**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23|package com.atguigu.spring6.bean;  <br>  <br>import com.atguigu.spring6.controller.UserController;  <br>import org.junit.jupiter.api.Test;  <br>import org.slf4j.Logger;  <br>import org.slf4j.LoggerFactory;  <br>import org.springframework.context.ApplicationContext;  <br>import org.springframework.context.support.ClassPathXmlApplicationContext;  <br>  <br>public class UserTest {  <br>  <br>    private Logger logger = LoggerFactory.getLogger(UserTest.class);  <br>  <br>    @Test  <br>    public void testAnnotation(){  <br>        ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");  <br>        UserController userController = context.getBean("userController", UserController.class);  <br>        userController.out();  <br>        logger.info("执行成功");  <br>    }  <br>  <br>  <br>}|

测试结果：

[![image-20221101153556681](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221101153556681.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221101153556681.png)

以上构造方法和setter方法都没有提供，经过测试，仍然可以注入成功。

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A1%E5%9C%BA%E6%99%AF%E4%BA%8C%EF%BC%9Aset%E6%B3%A8%E5%85%A5 "②场景二：set注入")②场景二：set注入

修改UserServiceImpl类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23|package com.atguigu.spring6.service.impl;  <br>  <br>import com.atguigu.spring6.dao.UserDao;  <br>import com.atguigu.spring6.service.UserService;  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.stereotype.Service;  <br>  <br>@Service  <br>public class UserServiceImpl implements UserService {  <br>  <br>    private UserDao userDao;  <br>  <br>    @Autowired  <br>    public void setUserDao(UserDao userDao) {  <br>        this.userDao = userDao;  <br>    }  <br>  <br>    @Override  <br>    public void out() {  <br>        userDao.print();  <br>        System.out.println("Service层执行结束");  <br>    }  <br>}|

修改UserController类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22|package com.atguigu.spring6.controller;  <br>  <br>import com.atguigu.spring6.service.UserService;  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.stereotype.Controller;  <br>  <br>@Controller  <br>public class UserController {  <br>  <br>    private UserService userService;  <br>  <br>    @Autowired  <br>    public void setUserService(UserService userService) {  <br>        this.userService = userService;  <br>    }  <br>  <br>    public void out() {  <br>        userService.out();  <br>        System.out.println("Controller层执行结束。");  <br>    }  <br>  <br>}|

测试：成功调用

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A2%E5%9C%BA%E6%99%AF%E4%B8%89%EF%BC%9A%E6%9E%84%E9%80%A0%E6%96%B9%E6%B3%95%E6%B3%A8%E5%85%A5 "③场景三：构造方法注入")③场景三：构造方法注入

修改UserServiceImpl类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23|package com.atguigu.spring6.service.impl;  <br>  <br>import com.atguigu.spring6.dao.UserDao;  <br>import com.atguigu.spring6.service.UserService;  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.stereotype.Service;  <br>  <br>@Service  <br>public class UserServiceImpl implements UserService {  <br>  <br>    private UserDao userDao;  <br>  <br>    @Autowired  <br>    public UserServiceImpl(UserDao userDao) {  <br>        this.userDao = userDao;  <br>    }  <br>  <br>    @Override  <br>    public void out() {  <br>        userDao.print();  <br>        System.out.println("Service层执行结束");  <br>    }  <br>}|

修改UserController类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22|package com.atguigu.spring6.controller;  <br>  <br>import com.atguigu.spring6.service.UserService;  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.stereotype.Controller;  <br>  <br>@Controller  <br>public class UserController {  <br>  <br>    private UserService userService;  <br>  <br>    @Autowired  <br>    public UserController(UserService userService) {  <br>        this.userService = userService;  <br>    }  <br>  <br>    public void out() {  <br>        userService.out();  <br>        System.out.println("Controller层执行结束。");  <br>    }  <br>  <br>}|

测试：成功调用

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A3%E5%9C%BA%E6%99%AF%E5%9B%9B%EF%BC%9A%E5%BD%A2%E5%8F%82%E4%B8%8A%E6%B3%A8%E5%85%A5 "④场景四：形参上注入")④场景四：形参上注入

修改UserServiceImpl类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22|package com.atguigu.spring6.service.impl;  <br>  <br>import com.atguigu.spring6.dao.UserDao;  <br>import com.atguigu.spring6.service.UserService;  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.stereotype.Service;  <br>  <br>@Service  <br>public class UserServiceImpl implements UserService {  <br>  <br>    private UserDao userDao;  <br>  <br>    public UserServiceImpl(@Autowired UserDao userDao) {  <br>        this.userDao = userDao;  <br>    }  <br>  <br>    @Override  <br>    public void out() {  <br>        userDao.print();  <br>        System.out.println("Service层执行结束");  <br>    }  <br>}|

修改UserController类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21|package com.atguigu.spring6.controller;  <br>  <br>import com.atguigu.spring6.service.UserService;  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.stereotype.Controller;  <br>  <br>@Controller  <br>public class UserController {  <br>  <br>    private UserService userService;  <br>  <br>    public UserController(@Autowired UserService userService) {  <br>        this.userService = userService;  <br>    }  <br>  <br>    public void out() {  <br>        userService.out();  <br>        System.out.println("Controller层执行结束。");  <br>    }  <br>  <br>}|

测试：成功调用

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A4%E5%9C%BA%E6%99%AF%E4%BA%94%EF%BC%9A%E5%8F%AA%E6%9C%89%E4%B8%80%E4%B8%AA%E6%9E%84%E9%80%A0%E5%87%BD%E6%95%B0%EF%BC%8C%E6%97%A0%E6%B3%A8%E8%A7%A3 "⑤场景五：只有一个构造函数，无注解")⑤场景五：只有一个构造函数，无注解

修改UserServiceImpl类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24|package com.atguigu.spring6.service.impl;  <br>  <br>import com.atguigu.spring6.dao.UserDao;  <br>import com.atguigu.spring6.service.UserService;  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.beans.factory.annotation.Qualifier;  <br>import org.springframework.stereotype.Service;  <br>  <br>@Service  <br>public class UserServiceImpl implements UserService {  <br>  <br>    @Autowired  <br>    private UserDao userDao;  <br>  <br>    public UserServiceImpl(UserDao userDao) {  <br>        this.userDao = userDao;  <br>    }  <br>  <br>    @Override  <br>    public void out() {  <br>        userDao.print();  <br>        System.out.println("Service层执行结束");  <br>    }  <br>}|

测试通过

**当有参数的构造方法只有一个时，@Autowired注解可以省略。**

说明：有多个构造方法时呢？大家可以测试（再添加一个无参构造函数），测试报错

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A5%E5%9C%BA%E6%99%AF%E5%85%AD%EF%BC%9A-Autowired%E6%B3%A8%E8%A7%A3%E5%92%8C-Qualifier%E6%B3%A8%E8%A7%A3%E8%81%94%E5%90%88 "⑥场景六：@Autowired注解和@Qualifier注解联合")⑥场景六：@Autowired注解和@Qualifier注解联合

添加dao层实现

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13|package com.atguigu.spring6.dao.impl;  <br>  <br>import com.atguigu.spring6.dao.UserDao;  <br>import org.springframework.stereotype.Repository;  <br>  <br>@Repository  <br>public class UserDaoRedisImpl implements UserDao {  <br>  <br>    @Override  <br>    public void print() {  <br>        System.out.println("Redis Dao层执行结束");  <br>    }  <br>}|

测试：测试异常

错误信息中说：不能装配，UserDao这个Bean的数量等于2

怎么解决这个问题呢？**当然要byName，根据名称进行装配了。**

修改UserServiceImpl类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20|package com.atguigu.spring6.service.impl;  <br>  <br>import com.atguigu.spring6.dao.UserDao;  <br>import com.atguigu.spring6.service.UserService;  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.stereotype.Service;  <br>  <br>@Service  <br>public class UserServiceImpl implements UserService {  <br>  <br>    @Autowired  <br>    @Qualifier("userDaoImpl") // 指定bean的名字  <br>    private UserDao userDao;  <br>  <br>    @Override  <br>    public void out() {  <br>        userDao.print();  <br>        System.out.println("Service层执行结束");  <br>    }  <br>}|

**总结**

- @Autowired注解可以出现在：属性上、构造方法上、构造方法的参数上、setter方法上。
- 当带参数的构造方法只有一个，@Autowired注解可以省略。（）
- @Autowired注解默认根据类型注入。如果要根据名称注入的话，需要配合@Qualifier注解一起使用。

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-3-5%E3%80%81%E5%AE%9E%E9%AA%8C%E4%BA%8C%EF%BC%9A-Resource%E6%B3%A8%E5%85%A5 "3.3.5、实验二：@Resource注入")3.3.5、实验二：@Resource注入

@Resource注解也可以完成属性注入。那它和@Autowired注解有什么区别？

- @Resource注解是JDK扩展包中的，也就是说属于JDK的一部分。所以该注解是标准注解，更加具有通用性。(JSR-250标准中制定的注解类型。JSR是Java规范提案。)
- @Autowired注解是Spring框架自己的。
- **@Resource注解默认根据名称装配byName，未指定name时，使用属性名作为name。通过name找不到的话会自动启动通过类型byType装配。**
- **@Autowired注解默认根据类型装配byType，如果想根据名称装配，需要配合@Qualifier注解一起用。**
- @Resource注解用在属性上、setter方法上。
- @Autowired注解用在属性上、setter方法上、构造方法上、构造方法参数上。

@Resource注解属于JDK扩展包，所以不在JDK当中，需要额外引入以下依赖：【**如果是JDK8的话不需要额外引入依赖。高于JDK11或低于JDK8需要引入以下依赖。**】

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5|<dependency>  <br>    <groupId>jakarta.annotation</groupId>  <br>    <artifactId>jakarta.annotation-api</artifactId>  <br>    <version>2.1.1</version>  <br></dependency>|

源码：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34|package jakarta.annotation;  <br>  <br>import java.lang.annotation.ElementType;  <br>import java.lang.annotation.Repeatable;  <br>import java.lang.annotation.Retention;  <br>import java.lang.annotation.RetentionPolicy;  <br>import java.lang.annotation.Target;  <br>  <br>@Target({ElementType.TYPE, ElementType.FIELD, ElementType.METHOD})  <br>@Retention(RetentionPolicy.RUNTIME)  <br>@Repeatable(Resources.class)  <br>public @interface Resource {  <br>    String name() default "";  <br>  <br>    String lookup() default "";  <br>  <br>    Class<?> type() default Object.class;  <br>  <br>    Resource.AuthenticationType authenticationType() default Resource.AuthenticationType.CONTAINER;  <br>  <br>    boolean shareable() default true;  <br>  <br>    String mappedName() default "";  <br>  <br>    String description() default "";  <br>  <br>    public static enum AuthenticationType {  <br>        CONTAINER,  <br>        APPLICATION;  <br>  <br>        private AuthenticationType() {  <br>        }  <br>    }  <br>}|

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A0%E5%9C%BA%E6%99%AF%E4%B8%80%EF%BC%9A%E6%A0%B9%E6%8D%AEname%E6%B3%A8%E5%85%A5 "①场景一：根据name注入")①场景一：根据name注入

修改UserDaoImpl类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13|package com.atguigu.spring6.dao.impl;  <br>  <br>import com.atguigu.spring6.dao.UserDao;  <br>import org.springframework.stereotype.Repository;  <br>  <br>@Repository("myUserDao")  <br>public class UserDaoImpl implements UserDao {  <br>  <br>    @Override  <br>    public void print() {  <br>        System.out.println("Dao层执行结束");  <br>    }  <br>}|

修改UserServiceImpl类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21|package com.atguigu.spring6.service.impl;  <br>  <br>import com.atguigu.spring6.dao.UserDao;  <br>import com.atguigu.spring6.service.UserService;  <br>import jakarta.annotation.Resource;  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.beans.factory.annotation.Qualifier;  <br>import org.springframework.stereotype.Service;  <br>  <br>@Service  <br>public class UserServiceImpl implements UserService {  <br>  <br>    @Resource(name = "myUserDao")  <br>    private UserDao myUserDao;  <br>  <br>    @Override  <br>    public void out() {  <br>        myUserDao.print();  <br>        System.out.println("Service层执行结束");  <br>    }  <br>}|

测试通过

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A1%E5%9C%BA%E6%99%AF%E4%BA%8C%EF%BC%9Aname%E6%9C%AA%E7%9F%A5%E6%B3%A8%E5%85%A5 "②场景二：name未知注入")②场景二：name未知注入

修改UserDaoImpl类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13|package com.atguigu.spring6.dao.impl;  <br>  <br>import com.atguigu.spring6.dao.UserDao;  <br>import org.springframework.stereotype.Repository;  <br>  <br>@Repository("myUserDao")  <br>public class UserDaoImpl implements UserDao {  <br>  <br>    @Override  <br>    public void print() {  <br>        System.out.println("Dao层执行结束");  <br>    }  <br>}|

修改UserServiceImpl类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21|package com.atguigu.spring6.service.impl;  <br>  <br>import com.atguigu.spring6.dao.UserDao;  <br>import com.atguigu.spring6.service.UserService;  <br>import jakarta.annotation.Resource;  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.beans.factory.annotation.Qualifier;  <br>import org.springframework.stereotype.Service;  <br>  <br>@Service  <br>public class UserServiceImpl implements UserService {  <br>  <br>    @Resource  <br>    private UserDao myUserDao;  <br>  <br>    @Override  <br>    public void out() {  <br>        myUserDao.print();  <br>        System.out.println("Service层执行结束");  <br>    }  <br>}|

测试通过

当@Resource注解使用时没有指定name的时候，还是根据name进行查找，这个name是属性名。

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A2%E5%9C%BA%E6%99%AF%E4%B8%89-%E5%85%B6%E4%BB%96%E6%83%85%E5%86%B5 "③场景三 其他情况")③场景三 其他情况

修改UserServiceImpl类，userDao1属性名不存在

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21|package com.atguigu.spring6.service.impl;  <br>  <br>import com.atguigu.spring6.dao.UserDao;  <br>import com.atguigu.spring6.service.UserService;  <br>import jakarta.annotation.Resource;  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.beans.factory.annotation.Qualifier;  <br>import org.springframework.stereotype.Service;  <br>  <br>@Service  <br>public class UserServiceImpl implements UserService {  <br>  <br>    @Resource  <br>    private UserDao userDao1;  <br>  <br>    @Override  <br>    public void out() {  <br>        userDao1.print();  <br>        System.out.println("Service层执行结束");  <br>    }  <br>}|

测试异常

根据异常信息得知：显然当通过name找不到的时候，自然会启动byType进行注入，以上的错误是因为UserDao接口下有两个实现类导致的。所以根据类型注入就会报错。

@Resource的set注入可以自行测试

**总结：**

@Resource注解：默认byName注入，没有指定name时把属性名当做name，根据name找不到时，才会byType注入。byType注入时，某种类型的Bean只能有一个

#### [](https://blog.mohic.site/2024/05/18/spring6/#3-3-6%E3%80%81Spring%E5%85%A8%E6%B3%A8%E8%A7%A3%E5%BC%80%E5%8F%91 "3.3.6、Spring全注解开发")3.3.6、Spring全注解开发

全注解开发就是不再使用spring配置文件了，写一个配置类来代替配置文件。

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10|package com.atguigu.spring6.config;  <br>  <br>import org.springframework.context.annotation.ComponentScan;  <br>import org.springframework.context.annotation.Configuration;  <br>  <br>@Configuration  <br>//@ComponentScan({"com.atguigu.spring6.controller", "com.atguigu.spring6.service","com.atguigu.spring6.dao"})  <br>@ComponentScan("com.atguigu.spring6")  <br>public class Spring6Config {  <br>}|

测试类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7|@Test  <br>public void testAllAnnotation(){  <br>    ApplicationContext context = new AnnotationConfigApplicationContext(Spring6Config.class);  <br>    UserController userController = context.getBean("userController", UserController.class);  <br>    userController.out();  <br>    logger.info("执行成功");  <br>}|

## [](https://blog.mohic.site/2024/05/18/spring6/#4%E3%80%81%E5%8E%9F%E7%90%86-%E6%89%8B%E5%86%99IoC "4、原理-手写IoC")4、原理-手写IoC

我们都知道，Spring框架的IOC是基于Java反射机制实现的，下面我们先回顾一下java反射。

### [](https://blog.mohic.site/2024/05/18/spring6/#4-1%E3%80%81%E5%9B%9E%E9%A1%BEJava%E5%8F%8D%E5%B0%84 "4.1、回顾Java反射")4.1、回顾Java反射

`Java`反射机制是在运行状态中，对于任意一个类，都能够知道这个类的所有属性和方法；对于任意一个对象，都能够调用它的任意方法和属性；这种动态获取信息以及动态调用对象方法的功能称为`Java`语言的反射机制。简单来说，反射机制指的是程序在运行时能够获取自身的信息。

要想解剖一个类，必须先要**获取到该类的Class对象**。而剖析一个类或用反射解决具体的问题就是使用相关API**（1）java.lang.Class（2）java.lang.reflect**，所以，**Class对象是反射的根源**。

**自定义类**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40  <br>41  <br>42  <br>43  <br>44  <br>45  <br>46  <br>47  <br>48  <br>49  <br>50  <br>51  <br>52  <br>53  <br>54|package com.atguigu.reflect;  <br>  <br>public class Car {  <br>  <br>    //属性  <br>    private String name;  <br>    private int age;  <br>    private String color;  <br>  <br>    //无参数构造  <br>    public Car() {  <br>    }  <br>  <br>    //有参数构造  <br>    public Car(String name, int age, String color) {  <br>        this.name = name;  <br>        this.age = age;  <br>        this.color = color;  <br>    }  <br>  <br>    //普通方法  <br>    private void run() {  <br>        System.out.println("私有方法-run.....");  <br>    }  <br>  <br>    //get和set方法  <br>    public String getName() {  <br>        return name;  <br>    }  <br>    public void setName(String name) {  <br>        this.name = name;  <br>    }  <br>    public int getAge() {  <br>        return age;  <br>    }  <br>    public void setAge(int age) {  <br>        this.age = age;  <br>    }  <br>    public String getColor() {  <br>        return color;  <br>    }  <br>    public void setColor(String color) {  <br>        this.color = color;  <br>    }  <br>  <br>    @Override  <br>    public String toString() {  <br>        return "Car{" +  <br>                "name='" + name + '\'' +  <br>                ", age=" + age +  <br>                ", color='" + color + '\'' +  <br>                '}';  <br>    }  <br>}|

**编写测试类**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40  <br>41  <br>42  <br>43  <br>44  <br>45  <br>46  <br>47  <br>48  <br>49  <br>50  <br>51  <br>52  <br>53  <br>54  <br>55  <br>56  <br>57  <br>58  <br>59  <br>60  <br>61  <br>62  <br>63  <br>64  <br>65  <br>66  <br>67  <br>68  <br>69  <br>70  <br>71  <br>72  <br>73  <br>74  <br>75  <br>76  <br>77  <br>78  <br>79  <br>80  <br>81  <br>82  <br>83  <br>84  <br>85  <br>86  <br>87  <br>88  <br>89  <br>90  <br>91  <br>92  <br>93  <br>94  <br>95  <br>96  <br>97  <br>98  <br>99|package com.atguigu.reflect;  <br>  <br>import org.junit.jupiter.api.Test;  <br>import java.lang.reflect.Constructor;  <br>import java.lang.reflect.Field;  <br>import java.lang.reflect.Method;  <br>  <br>public class TestCar {  <br>  <br>    //1、获取Class对象多种方式  <br>    @Test  <br>    public void test01() throws Exception {  <br>        //1 类名.class  <br>        Class clazz1 = Car.class;  <br>  <br>        //2 对象.getClass()  <br>        Class clazz2 = new Car().getClass();  <br>  <br>        //3 Class.forName("全路径")  <br>        Class clazz3 = Class.forName("com.atguigu.reflect.Car");  <br>  <br>        //实例化  <br>        Car car = (Car)clazz3.getConstructor().newInstance();  <br>        System.out.println(car);  <br>    }  <br>  <br>    //2、获取构造方法  <br>    @Test  <br>    public void test02() throws Exception {  <br>        Class clazz = Car.class;  <br>        //获取所有构造  <br>        // getConstructors()获取所有public的构造方法  <br>//        Constructor[] constructors = clazz.getConstructors();  <br>        // getDeclaredConstructors()获取所有的构造方法public  private  <br>        Constructor[] constructors = clazz.getDeclaredConstructors();  <br>        for (Constructor c:constructors) {  <br>            System.out.println("方法名称："+c.getName()+" 参数个数："+c.getParameterCount());  <br>        }  <br>  <br>        //指定有参数构造创建对象  <br>        //1 构造public  <br>//        Constructor c1 = clazz.getConstructor(String.class, int.class, String.class);  <br>//        Car car1 = (Car)c1.newInstance("夏利", 10, "红色");  <br>//        System.out.println(car1);  <br>          <br>        //2 构造private  <br>        Constructor c2 = clazz.getDeclaredConstructor(String.class, int.class, String.class);  <br>        c2.setAccessible(true);  <br>        Car car2 = (Car)c2.newInstance("捷达", 15, "白色");  <br>        System.out.println(car2);  <br>    }  <br>  <br>    //3、获取属性  <br>    @Test  <br>    public void test03() throws Exception {  <br>        Class clazz = Car.class;  <br>        Car car = (Car)clazz.getDeclaredConstructor().newInstance();  <br>        //获取所有public属性  <br>        //Field[] fields = clazz.getFields();  <br>        //获取所有属性（包含私有属性）  <br>        Field[] fields = clazz.getDeclaredFields();  <br>        for (Field field:fields) {  <br>            if(field.getName().equals("name")) {  <br>                //设置允许访问  <br>                field.setAccessible(true);  <br>                field.set(car,"五菱宏光");  <br>                System.out.println(car);  <br>            }  <br>            System.out.println(field.getName());  <br>        }  <br>    }  <br>  <br>    //4、获取方法  <br>    @Test  <br>    public void test04() throws Exception {  <br>        Car car = new Car("奔驰",10,"黑色");  <br>        Class clazz = car.getClass();  <br>        //1 public方法  <br>        Method[] methods = clazz.getMethods();  <br>        for (Method m1:methods) {  <br>            //System.out.println(m1.getName());  <br>            //执行方法 toString  <br>            if(m1.getName().equals("toString")) {  <br>                String invoke = (String)m1.invoke(car);  <br>                //System.out.println("toString执行了："+invoke);  <br>            }  <br>        }  <br>  <br>        //2 private方法  <br>        Method[] methodsAll = clazz.getDeclaredMethods();  <br>        for (Method m:methodsAll) {  <br>            //执行方法 run  <br>            if(m.getName().equals("run")) {  <br>                m.setAccessible(true);  <br>                m.invoke(car);  <br>            }  <br>        }  <br>    }  <br>}|

### [](https://blog.mohic.site/2024/05/18/spring6/#4-2%E3%80%81%E5%AE%9E%E7%8E%B0Spring%E7%9A%84IoC "4.2、实现Spring的IoC")4.2、实现Spring的IoC

我们知道，IoC（控制反转）和DI（依赖注入）是Spring里面核心的东西，那么，我们如何自己手写出这样的代码呢？下面我们就一步一步写出Spring框架最核心的部分。

**①搭建子模块**

搭建模块：guigu-spring，搭建方式如其他spring子模块

**②准备测试需要的bean**

添加依赖

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8|<dependencies>  <br>    <!--junit5测试-->  <br>    <dependency>  <br>        <groupId>org.junit.jupiter</groupId>  <br>        <artifactId>junit-jupiter-api</artifactId>  <br>        <version>5.3.1</version>  <br>    </dependency>  <br></dependencies>|

创建UserDao接口

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|package com.atguigu.spring6.test.dao;  <br>  <br>public interface UserDao {  <br>  <br>    public void print();  <br>}|

创建UserDaoImpl实现

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12|package com.atguigu.spring6.test.dao.impl;  <br>  <br>import com.atguigu.spring.dao.UserDao;  <br>  <br>public class UserDaoImpl implements UserDao {  <br>  <br>    @Override  <br>    public void print() {  <br>        System.out.println("Dao层执行结束");  <br>    }  <br>}|

创建UserService接口

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|package com.atguigu.spring6.test.service;  <br>  <br>public interface UserService {  <br>  <br>    public void out();  <br>}|

创建UserServiceImpl实现类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17|package com.atguigu.spring.test.service.impl;  <br>  <br>import com.atguigu.spring.core.annotation.Bean;  <br>import com.atguigu.spring.service.UserService;  <br>  <br>@Bean  <br>public class UserServiceImpl implements UserService {  <br>  <br>//    private UserDao userDao;  <br>  <br>    @Override  <br>    public void out() {  <br>        //userDao.print();  <br>        System.out.println("Service层执行结束");  <br>    }  <br>}|

**③定义注解**

我们通过注解的形式加载bean与实现依赖注入

bean注解

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11|package com.atguigu.spring.core.annotation;  <br>  <br>import java.lang.annotation.ElementType;  <br>import java.lang.annotation.Retention;  <br>import java.lang.annotation.RetentionPolicy;  <br>import java.lang.annotation.Target;  <br>  <br>@Target(ElementType.TYPE)  <br>@Retention(RetentionPolicy.RUNTIME)  <br>public @interface Bean {  <br>}|

依赖注入注解

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11|package com.atguigu.spring.core.annotation;  <br>  <br>import java.lang.annotation.ElementType;  <br>import java.lang.annotation.Retention;  <br>import java.lang.annotation.RetentionPolicy;  <br>import java.lang.annotation.Target;  <br>  <br>@Target({ElementType.FIELD})  <br>@Retention(RetentionPolicy.RUNTIME)  <br>public @interface Di {  <br>}|

说明：上面两个注解可以随意取名

**④定义bean容器接口**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|package com.atguigu.spring.core;  <br>  <br>public interface ApplicationContext {  <br>  <br>    Object getBean(Class clazz);  <br>}|

**⑤编写注解bean容器接口实现**

AnnotationApplicationContext基于注解扫描bean

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22|package com.atguigu.spring.core;  <br>  <br>import java.util.HashMap;  <br>  <br>public class AnnotationApplicationContext implements ApplicationContext {  <br>  <br>    //存储bean的容器  <br>    private HashMap<Class, Object> beanFactory = new HashMap<>();  <br>  <br>    @Override  <br>    public Object getBean(Class clazz) {  <br>        return beanFactory.get(clazz);  <br>    }  <br>  <br>    /**  <br>     * 根据包扫描加载bean  <br>     * @param basePackage  <br>     */  <br>    public AnnotationApplicationContext(String basePackage) {  <br>          <br>    }  <br>}|

**⑥编写扫描bean逻辑**

我们通过构造方法传入包的base路径，扫描被@Bean注解的java对象，完整代码如下：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40  <br>41  <br>42  <br>43  <br>44  <br>45  <br>46  <br>47  <br>48  <br>49  <br>50  <br>51  <br>52  <br>53  <br>54  <br>55  <br>56  <br>57  <br>58  <br>59  <br>60  <br>61  <br>62  <br>63  <br>64  <br>65  <br>66  <br>67  <br>68  <br>69  <br>70  <br>71  <br>72  <br>73  <br>74  <br>75  <br>76  <br>77  <br>78  <br>79  <br>80  <br>81  <br>82  <br>83  <br>84  <br>85|package com.atguigu.spring.core;  <br>  <br>import com.atguigu.spring.core.annotation.Bean;  <br>  <br>import java.io.File;  <br>import java.util.HashMap;  <br>  <br>public class AnnotationApplicationContext implements ApplicationContext {  <br>  <br>    //存储bean的容器  <br>    private HashMap<Class, Object> beanFactory = new HashMap<>();  <br>    private static String rootPath;  <br>  <br>    @Override  <br>    public Object getBean(Class clazz) {  <br>        return beanFactory.get(clazz);  <br>    }  <br>  <br>    /**  <br>     * 根据包扫描加载bean  <br>     * @param basePackage  <br>     */  <br>    public AnnotationApplicationContext(String basePackage) {  <br>       try {  <br>            String packageDirName = basePackage.replaceAll("\\.", "\\\\");  <br>            Enumeration<URL> dirs =Thread.currentThread().getContextClassLoader().getResources(packageDirName);  <br>            while (dirs.hasMoreElements()) {  <br>                URL url = dirs.nextElement();  <br>                String filePath = URLDecoder.decode(url.getFile(),"utf-8");  <br>                rootPath = filePath.substring(0, filePath.length()-packageDirName.length());  <br>                loadBean(new File(filePath));  <br>            }  <br>  <br>        } catch (Exception e) {  <br>            throw new RuntimeException(e);  <br>        }  <br>    }  <br>  <br>    private  void loadBean(File fileParent) {  <br>        if (fileParent.isDirectory()) {  <br>            File[] childrenFiles = fileParent.listFiles();  <br>            if(childrenFiles == null \| childrenFiles.length == 0){  <br>                return;  <br>            }  <br>            for (File child : childrenFiles) {  <br>                if (child.isDirectory()) {  <br>                    //如果是个文件夹就继续调用该方法,使用了递归  <br>                    loadBean(child);  <br>                } else {  <br>                    //通过文件路径转变成全类名,第一步把绝对路径部分去掉  <br>                    String pathWithClass = child.getAbsolutePath().substring(rootPath.length() - 1);  <br>                    //选中class文件  <br>                    if (pathWithClass.contains(".class")) {  <br>                        //    com.xinzhi.dao.UserDao  <br>                        //去掉.class后缀，并且把 \ 替换成 .  <br>                        String fullName = pathWithClass.replaceAll("\\\\", ".").replace(".class", "");  <br>                        try {  <br>                            Class<?> aClass = Class.forName(fullName);  <br>                            //把非接口的类实例化放在map中  <br>                            if(!aClass.isInterface()){  <br>                                Bean annotation = aClass.getAnnotation(Bean.class);  <br>                                if(annotation != null){  <br>                                    Object instance = aClass.newInstance();  <br>                                    //判断一下有没有接口  <br>                                    if(aClass.getInterfaces().length > 0) {  <br>                                        //如果有接口把接口的class当成key，实例对象当成value  <br>                                        System.out.println("正在加载【"+ aClass.getInterfaces()[0] +"】,实例对象是：" + instance.getClass().getName());  <br>                                        beanFactory.put(aClass.getInterfaces()[0], instance);  <br>                                    }else{  <br>                                        //如果有接口把自己的class当成key，实例对象当成value  <br>                                        System.out.println("正在加载【"+ aClass.getName() +"】,实例对象是：" + instance.getClass().getName());  <br>                                        beanFactory.put(aClass, instance);  <br>                                    }  <br>                                }  <br>                            }  <br>                        } catch (ClassNotFoundException \| IllegalAccessException \| InstantiationException e) {  <br>                            e.printStackTrace();  <br>                        }  <br>                    }  <br>                }  <br>            }  <br>        }  <br>    }  <br>  <br>}|

**⑦java类标识Bean注解**

java

|   |   |
|---|---|
|1  <br>2|@Bean  <br>public class UserServiceImpl implements UserService|

java

|   |   |
|---|---|
|1  <br>2|@Bean  <br>public class UserDaoImpl implements UserDao|

**⑧测试Bean加载**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17|package com.atguigu.spring;  <br>  <br>import com.atguigu.spring.core.AnnotationApplicationContext;  <br>import com.atguigu.spring.core.ApplicationContext;  <br>import com.atguigu.spring.test.service.UserService;  <br>import org.junit.jupiter.api.Test;  <br>  <br>public class SpringIocTest {  <br>  <br>    @Test  <br>    public void testIoc() {  <br>        ApplicationContext applicationContext = new AnnotationApplicationContext("com.atguigu.spring.test");  <br>        UserService userService = (UserService)applicationContext.getBean(UserService.class);  <br>        userService.out();  <br>        System.out.println("run success");  <br>    }  <br>}|

控制台打印测试

**⑨依赖注入**

只要userDao.print();调用成功，说明就注入成功

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19|package com.atguigu.spring.test.service.impl;  <br>  <br>import com.atguigu.spring.core.annotation.Bean;  <br>import com.atguigu.spring.core.annotation.Di;  <br>import com.atguigu.spring.dao.UserDao;  <br>import com.atguigu.spring.service.UserService;  <br>  <br>@Bean  <br>public class UserServiceImpl implements UserService {  <br>  <br>    @Di  <br>    private UserDao userDao;  <br>  <br>    @Override  <br>    public void out() {  <br>        userDao.print();  <br>        System.out.println("Service层执行结束");  <br>    }  <br>}|

执行第八步：报错了，说明当前userDao是个空对象

**⑩依赖注入实现**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40  <br>41  <br>42  <br>43  <br>44  <br>45  <br>46  <br>47  <br>48  <br>49  <br>50  <br>51  <br>52  <br>53  <br>54  <br>55  <br>56  <br>57  <br>58  <br>59  <br>60  <br>61  <br>62  <br>63  <br>64  <br>65  <br>66  <br>67  <br>68  <br>69  <br>70  <br>71  <br>72  <br>73  <br>74  <br>75  <br>76  <br>77  <br>78  <br>79  <br>80  <br>81  <br>82  <br>83  <br>84  <br>85  <br>86  <br>87  <br>88  <br>89  <br>90  <br>91  <br>92  <br>93  <br>94  <br>95  <br>96  <br>97  <br>98  <br>99  <br>100  <br>101  <br>102  <br>103  <br>104  <br>105  <br>106  <br>107  <br>108  <br>109  <br>110  <br>111  <br>112|package com.atguigu.spring.core;  <br>  <br>import com.atguigu.spring.core.annotation.Bean;  <br>import com.atguigu.spring.core.annotation.Di;  <br>  <br>import java.io.File;  <br>import java.lang.reflect.Field;  <br>import java.util.HashMap;  <br>import java.util.Map;  <br>  <br>public class AnnotationApplicationContext implements ApplicationContext {  <br>  <br>    //存储bean的容器  <br>    private HashMap<Class, Object> beanFactory = new HashMap<>();  <br>    private static String rootPath;  <br>  <br>    @Override  <br>    public Object getBean(Class clazz) {  <br>        return beanFactory.get(clazz);  <br>    }  <br>  <br>    /**  <br>     * 根据包扫描加载bean  <br>     * @param basePackage  <br>     */  <br>    public AnnotationApplicationContext(String basePackage) {  <br>        try {  <br>            String packageDirName = basePackage.replaceAll("\\.", "\\\\");  <br>            Enumeration<URL> dirs =Thread.currentThread().getContextClassLoader().getResources(packageDirName);  <br>            while (dirs.hasMoreElements()) {  <br>                URL url = dirs.nextElement();  <br>                String filePath = URLDecoder.decode(url.getFile(),"utf-8");  <br>                rootPath = filePath.substring(0, filePath.length()-packageDirName.length());  <br>                loadBean(new File(filePath));  <br>            }  <br>  <br>        } catch (Exception e) {  <br>            throw new RuntimeException(e);  <br>        }  <br>          <br>        //依赖注入  <br>        loadDi();  <br>    }  <br>      <br>    private  void loadBean(File fileParent) {  <br>        if (fileParent.isDirectory()) {  <br>            File[] childrenFiles = fileParent.listFiles();  <br>            if(childrenFiles == null \| childrenFiles.length == 0){  <br>                return;  <br>            }  <br>            for (File child : childrenFiles) {  <br>                if (child.isDirectory()) {  <br>                    //如果是个文件夹就继续调用该方法,使用了递归  <br>                    loadBean(child);  <br>                } else {  <br>                    //通过文件路径转变成全类名,第一步把绝对路径部分去掉  <br>                    String pathWithClass = child.getAbsolutePath().substring(rootPath.length() - 1);  <br>                    //选中class文件  <br>                    if (pathWithClass.contains(".class")) {  <br>                        //    com.xinzhi.dao.UserDao  <br>                        //去掉.class后缀，并且把 \ 替换成 .  <br>                        String fullName = pathWithClass.replaceAll("\\\\", ".").replace(".class", "");  <br>                        try {  <br>                            Class<?> aClass = Class.forName(fullName);  <br>                            //把非接口的类实例化放在map中  <br>                            if(!aClass.isInterface()){  <br>                                Bean annotation = aClass.getAnnotation(Bean.class);  <br>                                if(annotation != null){  <br>                                    Object instance = aClass.newInstance();  <br>                                    //判断一下有没有接口  <br>                                    if(aClass.getInterfaces().length > 0) {  <br>                                        //如果有接口把接口的class当成key，实例对象当成value  <br>                                        System.out.println("正在加载【"+ aClass.getInterfaces()[0] +"】,实例对象是：" + instance.getClass().getName());  <br>                                        beanFactory.put(aClass.getInterfaces()[0], instance);  <br>                                    }else{  <br>                                        //如果有接口把自己的class当成key，实例对象当成value  <br>                                        System.out.println("正在加载【"+ aClass.getName() +"】,实例对象是：" + instance.getClass().getName());  <br>                                        beanFactory.put(aClass, instance);  <br>                                    }  <br>                                }  <br>                            }  <br>                        } catch (ClassNotFoundException \| IllegalAccessException \| InstantiationException e) {  <br>                            e.printStackTrace();  <br>                        }  <br>                    }  <br>                }  <br>            }  <br>        }  <br>    }  <br>  <br>    private void loadDi() {  <br>        for(Map.Entry<Class,Object> entry : beanFactory.entrySet()){  <br>            //就是咱们放在容器的对象  <br>            Object obj = entry.getValue();  <br>            Class<?> aClass = obj.getClass();  <br>            Field[] declaredFields = aClass.getDeclaredFields();  <br>            for (Field field : declaredFields){  <br>                Di annotation = field.getAnnotation(Di.class);  <br>                if( annotation != null ){  <br>                    field.setAccessible(true);  <br>                    try {  <br>                        System.out.println("正在给【"+obj.getClass().getName()+"】属性【" + field.getName() + "】注入值【"+ beanFactory.get(field.getType()).getClass().getName() +"】");  <br>                        field.set(obj,beanFactory.get(field.getType()));  <br>                    } catch (IllegalAccessException e) {  <br>                        e.printStackTrace();  <br>                    }  <br>                }  <br>            }  <br>        }  <br>    }  <br>  <br>}|

执行第八步：执行成功，依赖注入成功

## [](https://blog.mohic.site/2024/05/18/spring6/#5%E3%80%81%E9%9D%A2%E5%90%91%E5%88%87%E9%9D%A2%EF%BC%9AAOP "5、面向切面：AOP")5、面向切面：AOP

### [](https://blog.mohic.site/2024/05/18/spring6/#5-1%E3%80%81%E5%9C%BA%E6%99%AF%E6%A8%A1%E6%8B%9F "5.1、场景模拟")5.1、场景模拟

**搭建子模块：spring6-aop**

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-1-1%E3%80%81%E5%A3%B0%E6%98%8E%E6%8E%A5%E5%8F%A3 "5.1.1、声明接口")5.1.1、声明接口

声明计算器接口Calculator，包含加减乘除的抽象方法

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11|public interface Calculator {  <br>      <br>    int add(int i, int j);  <br>      <br>    int sub(int i, int j);  <br>      <br>    int mul(int i, int j);  <br>      <br>    int div(int i, int j);  <br>      <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-1-2%E3%80%81%E5%88%9B%E5%BB%BA%E5%AE%9E%E7%8E%B0%E7%B1%BB "5.1.2、创建实现类")5.1.2、创建实现类

[![images](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img014.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img014.png)

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40  <br>41  <br>42|public class CalculatorImpl implements Calculator {  <br>      <br>    @Override  <br>    public int add(int i, int j) {  <br>      <br>        int result = i + j;  <br>      <br>        System.out.println("方法内部 result = " + result);  <br>      <br>        return result;  <br>    }  <br>      <br>    @Override  <br>    public int sub(int i, int j) {  <br>      <br>        int result = i - j;  <br>      <br>        System.out.println("方法内部 result = " + result);  <br>      <br>        return result;  <br>    }  <br>      <br>    @Override  <br>    public int mul(int i, int j) {  <br>      <br>        int result = i * j;  <br>      <br>        System.out.println("方法内部 result = " + result);  <br>      <br>        return result;  <br>    }  <br>      <br>    @Override  <br>    public int div(int i, int j) {  <br>      <br>        int result = i / j;  <br>      <br>        System.out.println("方法内部 result = " + result);  <br>      <br>        return result;  <br>    }  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-1-3%E3%80%81%E5%88%9B%E5%BB%BA%E5%B8%A6%E6%97%A5%E5%BF%97%E5%8A%9F%E8%83%BD%E7%9A%84%E5%AE%9E%E7%8E%B0%E7%B1%BB "5.1.3、创建带日志功能的实现类")5.1.3、创建带日志功能的实现类

[![images](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img015.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img015.png)

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40  <br>41  <br>42  <br>43  <br>44  <br>45  <br>46  <br>47  <br>48  <br>49  <br>50  <br>51  <br>52  <br>53  <br>54  <br>55  <br>56  <br>57  <br>58|public class CalculatorLogImpl implements Calculator {  <br>      <br>    @Override  <br>    public int add(int i, int j) {  <br>      <br>        System.out.println("[日志] add 方法开始了，参数是：" + i + "," + j);  <br>      <br>        int result = i + j;  <br>      <br>        System.out.println("方法内部 result = " + result);  <br>      <br>        System.out.println("[日志] add 方法结束了，结果是：" + result);  <br>      <br>        return result;  <br>    }  <br>      <br>    @Override  <br>    public int sub(int i, int j) {  <br>      <br>        System.out.println("[日志] sub 方法开始了，参数是：" + i + "," + j);  <br>      <br>        int result = i - j;  <br>      <br>        System.out.println("方法内部 result = " + result);  <br>      <br>        System.out.println("[日志] sub 方法结束了，结果是：" + result);  <br>      <br>        return result;  <br>    }  <br>      <br>    @Override  <br>    public int mul(int i, int j) {  <br>      <br>        System.out.println("[日志] mul 方法开始了，参数是：" + i + "," + j);  <br>      <br>        int result = i * j;  <br>      <br>        System.out.println("方法内部 result = " + result);  <br>      <br>        System.out.println("[日志] mul 方法结束了，结果是：" + result);  <br>      <br>        return result;  <br>    }  <br>      <br>    @Override  <br>    public int div(int i, int j) {  <br>      <br>        System.out.println("[日志] div 方法开始了，参数是：" + i + "," + j);  <br>      <br>        int result = i / j;  <br>      <br>        System.out.println("方法内部 result = " + result);  <br>      <br>        System.out.println("[日志] div 方法结束了，结果是：" + result);  <br>      <br>        return result;  <br>    }  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-1-4%E3%80%81%E6%8F%90%E5%87%BA%E9%97%AE%E9%A2%98 "5.1.4、提出问题")5.1.4、提出问题

**①现有代码缺陷**

针对带日志功能的实现类，我们发现有如下缺陷：

- 对核心业务功能有干扰，导致程序员在开发核心业务功能时分散了精力
- 附加功能分散在各个业务功能方法中，不利于统一维护

**②解决思路**

解决这两个问题，核心就是：解耦。我们需要把附加功能从业务功能代码中抽取出来。

**③困难**

解决问题的困难：要抽取的代码在方法内部，靠以前把子类中的重复代码抽取到父类的方式没法解决。所以需要引入新的技术。

### [](https://blog.mohic.site/2024/05/18/spring6/#5-2%E3%80%81%E4%BB%A3%E7%90%86%E6%A8%A1%E5%BC%8F "5.2、代理模式")5.2、代理模式

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-2-1%E3%80%81%E6%A6%82%E5%BF%B5 "5.2.1、概念")5.2.1、概念

**①介绍**

二十三种设计模式中的一种，属于结构型模式。它的作用就是通过提供一个代理类，让我们在调用目标方法的时候，不再是直接对目标方法进行调用，而是通过代理类**间接**调用。让不属于目标方法核心逻辑的代码从目标方法中剥离出来——**解耦**。调用目标方法时先调用代理对象的方法，减少对目标方法的调用和打扰，同时让附加功能能够集中在一起也有利于统一维护。

[![images](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img016.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img016.png)

使用代理后：

[![images](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img017.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img017.png)

**②生活中的代理**

- 广告商找大明星拍广告需要经过经纪人
- 合作伙伴找大老板谈合作要约见面时间需要经过秘书
- 房产中介是买卖双方的代理

**③相关术语**

- 代理：将非核心逻辑剥离出来以后，封装这些非核心逻辑的类、对象、方法。
- 目标：被代理“套用”了非核心逻辑代码的类、对象、方法。

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-2-2%E3%80%81%E9%9D%99%E6%80%81%E4%BB%A3%E7%90%86 "5.2.2、静态代理")5.2.2、静态代理

创建静态代理类：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23|public class CalculatorStaticProxy implements Calculator {  <br>      <br>    // 将被代理的目标对象声明为成员变量  <br>    private Calculator target;  <br>      <br>    public CalculatorStaticProxy(Calculator target) {  <br>        this.target = target;  <br>    }  <br>      <br>    @Override  <br>    public int add(int i, int j) {  <br>      <br>        // 附加功能由代理类中的代理方法来实现  <br>        System.out.println("[日志] add 方法开始了，参数是：" + i + "," + j);  <br>      <br>        // 通过目标对象来实现核心业务逻辑  <br>        int addResult = target.add(i, j);  <br>      <br>        System.out.println("[日志] add 方法结束了，结果是：" + addResult);  <br>      <br>        return addResult;  <br>    }  <br>}|

> 静态代理确实实现了解耦，但是由于代码都写死了，完全不具备任何的灵活性。就拿日志功能来说，将来其他地方也需要附加日志，那还得再声明更多个静态代理类，那就产生了大量重复的代码，日志功能还是分散的，没有统一管理。
> 
> 提出进一步的需求：将日志功能集中到一个代理类中，将来有任何日志需求，都通过这一个代理类来实现。这就需要使用动态代理技术了。

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-2-3%E3%80%81%E5%8A%A8%E6%80%81%E4%BB%A3%E7%90%86 "5.2.3、动态代理")5.2.3、动态代理

[![images](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img018.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img018.png)

生产代理对象的工厂类：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40  <br>41  <br>42  <br>43  <br>44  <br>45|public class ProxyFactory {  <br>  <br>    private Object target;  <br>  <br>    public ProxyFactory(Object target) {  <br>        this.target = target;  <br>    }  <br>  <br>    public Object getProxy(){  <br>  <br>        /**  <br>         * newProxyInstance()：创建一个代理实例  <br>         * 其中有三个参数：  <br>         * 1、classLoader：加载动态生成的代理类的类加载器  <br>         * 2、interfaces：目标对象实现的所有接口的class对象所组成的数组  <br>         * 3、invocationHandler：设置代理对象实现目标对象方法的过程，即代理类中如何重写接口中的抽象方法  <br>         */  <br>        ClassLoader classLoader = target.getClass().getClassLoader();  <br>        Class<?>[] interfaces = target.getClass().getInterfaces();  <br>        InvocationHandler invocationHandler = new InvocationHandler() {  <br>            @Override  <br>            public Object invoke(Object proxy, Method method, Object[] args) throws Throwable {  <br>                /**  <br>                 * proxy：代理对象  <br>                 * method：代理对象需要实现的方法，即其中需要重写的方法  <br>                 * args：method所对应方法的参数  <br>                 */  <br>                Object result = null;  <br>                try {  <br>                    System.out.println("[动态代理][日志] "+method.getName()+"，参数："+ Arrays.toString(args));  <br>                    result = method.invoke(target, args);  <br>                    System.out.println("[动态代理][日志] "+method.getName()+"，结果："+ result);  <br>                } catch (Exception e) {  <br>                    e.printStackTrace();  <br>                    System.out.println("[动态代理][日志] "+method.getName()+"，异常："+e.getMessage());  <br>                } finally {  <br>                    System.out.println("[动态代理][日志] "+method.getName()+"，方法执行完毕");  <br>                }  <br>                return result;  <br>            }  <br>        };  <br>  <br>        return Proxy.newProxyInstance(classLoader, interfaces, invocationHandler);  <br>    }  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-2-4%E3%80%81%E6%B5%8B%E8%AF%95 "5.2.4、测试")5.2.4、测试

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7|@Test  <br>public void testDynamicProxy(){  <br>    ProxyFactory factory = new ProxyFactory(new CalculatorLogImpl());  <br>    Calculator proxy = (Calculator) factory.getProxy();  <br>    proxy.div(1,0);  <br>    //proxy.div(1,1);  <br>}|

### [](https://blog.mohic.site/2024/05/18/spring6/#5-3%E3%80%81AOP%E6%A6%82%E5%BF%B5%E5%8F%8A%E7%9B%B8%E5%85%B3%E6%9C%AF%E8%AF%AD "5.3、AOP概念及相关术语")5.3、AOP概念及相关术语

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-3-1%E3%80%81%E6%A6%82%E8%BF%B0 "5.3.1、概述")5.3.1、概述

AOP（Aspect Oriented Programming）是一种设计思想，是软件设计领域中的面向切面编程，它是面向对象编程的一种补充和完善，它以通过预编译方式和运行期动态代理方式实现，在不修改源代码的情况下，给程序动态统一添加额外功能的一种技术。利用AOP可以对业务逻辑的各个部分进行隔离，从而使得业务逻辑各部分之间的耦合度降低，提高程序的可重用性，同时提高了开发的效率。

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-3-2%E3%80%81%E7%9B%B8%E5%85%B3%E6%9C%AF%E8%AF%AD "5.3.2、相关术语")5.3.2、相关术语

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A0%E6%A8%AA%E5%88%87%E5%85%B3%E6%B3%A8%E7%82%B9 "①横切关注点")①横切关注点

分散在每个各个模块中解决同一样的问题，如用户验证、日志管理、事务处理、数据缓存都属于横切关注点。

从每个方法中抽取出来的同一类非核心业务。在同一个项目中，我们可以使用多个横切关注点对相关方法进行多个不同方面的增强。

这个概念不是语法层面的，而是根据附加功能的逻辑上的需要：有十个附加功能，就有十个横切关注点。

[![images](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img019.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img019.png)

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A1%E9%80%9A%E7%9F%A5%EF%BC%88%E5%A2%9E%E5%BC%BA%EF%BC%89 "②通知（增强）")②通知（增强）

**增强，通俗说，就是你想要增强的功能，比如 安全，事务，日志等。**

每一个横切关注点上要做的事情都需要写一个方法来实现，这样的方法就叫通知方法。

- 前置通知：在被代理的目标方法**前**执行
- 返回通知：在被代理的目标方法**成功结束**后执行（**寿终正寝**）
- 异常通知：在被代理的目标方法**异常结束**后执行（**死于非命**）
- 后置通知：在被代理的目标方法**最终结束**后执行（**盖棺定论**）
- 环绕通知：使用try…catch…finally结构围绕**整个**被代理的目标方法，包括上面四种通知对应的所有位置

[![images](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img020.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img020.png)

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A2%E5%88%87%E9%9D%A2 "③切面")③切面

封装通知方法的类。

[![images](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img021.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img021.png)

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A3%E7%9B%AE%E6%A0%87 "④目标")④目标

被代理的目标对象。

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A4%E4%BB%A3%E7%90%86 "⑤代理")⑤代理

向目标对象应用通知之后创建的代理对象。

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A5%E8%BF%9E%E6%8E%A5%E7%82%B9 "⑥连接点")⑥连接点

这也是一个纯逻辑概念，不是语法定义的。

把方法排成一排，每一个横切位置看成x轴方向，把方法从上到下执行的顺序看成y轴，x轴和y轴的交叉点就是连接点。**通俗说，就是spring允许你使用通知的地方**

[![images](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img022.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img022.png)

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A6%E5%88%87%E5%85%A5%E7%82%B9 "⑦切入点")⑦切入点

定位连接点的方式。

每个类的方法中都包含多个连接点，所以连接点是类中客观存在的事物（从逻辑上来说）。

如果把连接点看作数据库中的记录，那么切入点就是查询记录的 SQL 语句。

**Spring 的 AOP 技术可以通过切入点定位到特定的连接点。通俗说，要实际去增强的方法**

切点通过 org.springframework.aop.Pointcut 接口进行描述，它使用类和方法作为连接点的查询条件。

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-3-3%E3%80%81%E4%BD%9C%E7%94%A8 "5.3.3、作用")5.3.3、作用

- 简化代码：把方法中固定位置的重复的代码**抽取**出来，让被抽取的方法更专注于自己的核心功能，提高内聚性。
    
- 代码增强：把特定的功能封装到切面类中，看哪里有需要，就往上套，被**套用**了切面逻辑的方法就被切面给增强了。
    

### [](https://blog.mohic.site/2024/05/18/spring6/#5-4%E3%80%81%E5%9F%BA%E4%BA%8E%E6%B3%A8%E8%A7%A3%E7%9A%84AOP "5.4、基于注解的AOP")5.4、基于注解的AOP

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-4-1%E3%80%81%E6%8A%80%E6%9C%AF%E8%AF%B4%E6%98%8E "5.4.1、技术说明")5.4.1、技术说明

[![images](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img023.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img023.png)

[![image-20221216132844066](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221216132844066.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221216132844066.png)

- 动态代理分为JDK动态代理和cglib动态代理
- 当目标类有接口的情况使用JDK动态代理和cglib动态代理，没有接口时只能使用cglib动态代理
- JDK动态代理动态生成的代理类会在com.sun.proxy包下，类名为$proxy1，和目标类实现相同的接口
- cglib动态代理动态生成的代理类会和目标在在相同的包下，会继承目标类
- 动态代理（InvocationHandler）：JDK原生的实现方式，需要被代理的目标类必须实现接口。因为这个技术要求**代理对象和目标对象实现同样的接口**（兄弟两个拜把子模式）。
- cglib：通过**继承被代理的目标类**（认干爹模式）实现代理，所以不需要目标类实现接口。
- AspectJ：是AOP思想的一种实现。本质上是静态代理，**将代理逻辑“织入”被代理的目标类编译得到的字节码文件**，所以最终效果是动态的。weaver就是织入器。Spring只是借用了AspectJ中的注解。

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-4-2%E3%80%81%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C "5.4.2、准备工作")5.4.2、准备工作

**①添加依赖**

在IOC所需依赖基础上再加入下面依赖即可：

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40  <br>41|<dependencies>  <br>    <!--spring context依赖-->  <br>    <!--当你引入Spring Context依赖之后，表示将Spring的基础依赖引入了-->  <br>    <dependency>  <br>        <groupId>org.springframework</groupId>  <br>        <artifactId>spring-context</artifactId>  <br>        <version>6.0.2</version>  <br>    </dependency>  <br>  <br>    <!--spring aop依赖-->  <br>    <dependency>  <br>        <groupId>org.springframework</groupId>  <br>        <artifactId>spring-aop</artifactId>  <br>        <version>6.0.2</version>  <br>    </dependency>  <br>    <!--spring aspects依赖-->  <br>    <dependency>  <br>        <groupId>org.springframework</groupId>  <br>        <artifactId>spring-aspects</artifactId>  <br>        <version>6.0.2</version>  <br>    </dependency>  <br>  <br>    <!--junit5测试-->  <br>    <dependency>  <br>        <groupId>org.junit.jupiter</groupId>  <br>        <artifactId>junit-jupiter-api</artifactId>  <br>        <version>5.3.1</version>  <br>    </dependency>  <br>  <br>    <!--log4j2的依赖-->  <br>    <dependency>  <br>        <groupId>org.apache.logging.log4j</groupId>  <br>        <artifactId>log4j-core</artifactId>  <br>        <version>2.19.0</version>  <br>    </dependency>  <br>    <dependency>  <br>        <groupId>org.apache.logging.log4j</groupId>  <br>        <artifactId>log4j-slf4j2-impl</artifactId>  <br>        <version>2.19.0</version>  <br>    </dependency>  <br></dependencies>|

**②准备被代理的目标资源**

接口：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11|public interface Calculator {  <br>      <br>    int add(int i, int j);  <br>      <br>    int sub(int i, int j);  <br>      <br>    int mul(int i, int j);  <br>      <br>    int div(int i, int j);  <br>      <br>}|

实现类：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40  <br>41  <br>42  <br>43|@Component  <br>public class CalculatorImpl implements Calculator {  <br>      <br>    @Override  <br>    public int add(int i, int j) {  <br>      <br>        int result = i + j;  <br>      <br>        System.out.println("方法内部 result = " + result);  <br>      <br>        return result;  <br>    }  <br>      <br>    @Override  <br>    public int sub(int i, int j) {  <br>      <br>        int result = i - j;  <br>      <br>        System.out.println("方法内部 result = " + result);  <br>      <br>        return result;  <br>    }  <br>      <br>    @Override  <br>    public int mul(int i, int j) {  <br>      <br>        int result = i * j;  <br>      <br>        System.out.println("方法内部 result = " + result);  <br>      <br>        return result;  <br>    }  <br>      <br>    @Override  <br>    public int div(int i, int j) {  <br>      <br>        int result = i / j;  <br>      <br>        System.out.println("方法内部 result = " + result);  <br>      <br>        return result;  <br>    }  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-4-3%E3%80%81%E5%88%9B%E5%BB%BA%E5%88%87%E9%9D%A2%E7%B1%BB%E5%B9%B6%E9%85%8D%E7%BD%AE "5.4.3、创建切面类并配置")5.4.3、创建切面类并配置

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40  <br>41  <br>42  <br>43  <br>44  <br>45  <br>46  <br>47  <br>48  <br>49  <br>50  <br>51|// @Aspect表示这个类是一个切面类  <br>@Aspect  <br>// @Component注解保证这个切面类能够放入IOC容器  <br>@Component  <br>public class LogAspect {  <br>      <br>    @Before("execution(public int com.atguigu.aop.annotation.CalculatorImpl.*(..))")  <br>    public void beforeMethod(JoinPoint joinPoint){  <br>        String methodName = joinPoint.getSignature().getName();  <br>        String args = Arrays.toString(joinPoint.getArgs());  <br>        System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);  <br>    }  <br>  <br>    @After("execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))")  <br>    public void afterMethod(JoinPoint joinPoint){  <br>        String methodName = joinPoint.getSignature().getName();  <br>        System.out.println("Logger-->后置通知，方法名："+methodName);  <br>    }  <br>  <br>    @AfterReturning(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", returning = "result")  <br>    public void afterReturningMethod(JoinPoint joinPoint, Object result){  <br>        String methodName = joinPoint.getSignature().getName();  <br>        System.out.println("Logger-->返回通知，方法名："+methodName+"，结果："+result);  <br>    }  <br>  <br>    @AfterThrowing(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", throwing = "ex")  <br>    public void afterThrowingMethod(JoinPoint joinPoint, Throwable ex){  <br>        String methodName = joinPoint.getSignature().getName();  <br>        System.out.println("Logger-->异常通知，方法名："+methodName+"，异常："+ex);  <br>    }  <br>      <br>    @Around("execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))")  <br>    public Object aroundMethod(ProceedingJoinPoint joinPoint){  <br>        String methodName = joinPoint.getSignature().getName();  <br>        String args = Arrays.toString(joinPoint.getArgs());  <br>        Object result = null;  <br>        try {  <br>            System.out.println("环绕通知-->目标对象方法执行之前");  <br>            //目标对象（连接点）方法的执行  <br>            result = joinPoint.proceed();  <br>            System.out.println("环绕通知-->目标对象方法返回值之后");  <br>        } catch (Throwable throwable) {  <br>            throwable.printStackTrace();  <br>            System.out.println("环绕通知-->目标对象方法出现异常时");  <br>        } finally {  <br>            System.out.println("环绕通知-->目标对象方法执行完毕");  <br>        }  <br>        return result;  <br>    }  <br>      <br>}|

在Spring的配置文件中配置：

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21|<?xml version="1.0" encoding="UTF-8"?>  <br><beans xmlns="http://www.springframework.org/schema/beans"  <br>       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  <br>       xmlns:context="http://www.springframework.org/schema/context"  <br>       xmlns:aop="http://www.springframework.org/schema/aop"  <br>       xsi:schemaLocation="http://www.springframework.org/schema/beans  <br>       http://www.springframework.org/schema/beans/spring-beans.xsd  <br>       http://www.springframework.org/schema/context  <br>       http://www.springframework.org/schema/context/spring-context.xsd  <br>       http://www.springframework.org/schema/aop  <br>       http://www.springframework.org/schema/aop/spring-aop.xsd">  <br>    <!--  <br>        基于注解的AOP的实现：  <br>        1、将目标对象和切面交给IOC容器管理（注解+扫描）  <br>        2、开启AspectJ的自动代理，为目标对象自动生成代理  <br>        3、将切面类通过注解@Aspect标识  <br>    -->  <br>    <context:component-scan base-package="com.atguigu.aop.annotation"></context:component-scan>  <br>  <br>    <aop:aspectj-autoproxy />  <br></beans>|

执行测试：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13|public class CalculatorTest {  <br>  <br>    private Logger logger = LoggerFactory.getLogger(CalculatorTest.class);  <br>  <br>    @Test  <br>    public void testAdd(){  <br>        ApplicationContext ac = new ClassPathXmlApplicationContext("beans.xml");  <br>        Calculator calculator = ac.getBean( Calculator.class);  <br>        int add = calculator.add(1, 1);  <br>        logger.info("执行成功:"+add);  <br>    }  <br>  <br>}|

执行结果：

[![image-20221102155523983](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221102155523983.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221102155523983.png)

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-4-4%E3%80%81%E5%90%84%E7%A7%8D%E9%80%9A%E7%9F%A5 "5.4.4、各种通知")5.4.4、各种通知

- 前置通知：使用@Before注解标识，在被代理的目标方法**前**执行
- 返回通知：使用@AfterReturning注解标识，在被代理的目标方法**成功结束**后执行（**寿终正寝**）
- 异常通知：使用@AfterThrowing注解标识，在被代理的目标方法**异常结束**后执行（**死于非命**）
- 后置通知：使用@After注解标识，在被代理的目标方法**最终结束**后执行（**盖棺定论**）
- 环绕通知：使用@Around注解标识，使用try…catch…finally结构围绕**整个**被代理的目标方法，包括上面四种通知对应的所有位置

> 各种通知的执行顺序：
> 
> - Spring版本5.3.x以前：
>     - 前置通知
>     - 目标操作
>     - 后置通知
>     - 返回通知或异常通知
> - Spring版本5.3.x以后：
>     - 前置通知
>     - 目标操作
>     - 返回通知或异常通知
>     - 后置通知

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-4-5%E3%80%81%E5%88%87%E5%85%A5%E7%82%B9%E8%A1%A8%E8%BE%BE%E5%BC%8F%E8%AF%AD%E6%B3%95 "5.4.5、切入点表达式语法")5.4.5、切入点表达式语法

**①作用**

[![images](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img024.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img024.png)

**②语法细节**

- 用*号代替“权限修饰符”和“返回值”部分表示“权限修饰符”和“返回值”不限
    
- 在包名的部分，一个“*”号只能代表包的层次结构中的一层，表示这一层是任意的。
    
    - 例如：*.Hello匹配com.Hello，不匹配com.atguigu.Hello
- 在包名的部分，使用“*..”表示包名任意、包的层次深度任意
    
- 在类名的部分，类名部分整体用*号代替，表示类名任意
    
- 在类名的部分，可以使用*号代替类名的一部分
    
    - 例如：*Service匹配所有名称以Service结尾的类或接口
- 在方法名部分，可以使用*号表示方法名任意
    
- 在方法名部分，可以使用*号代替方法名的一部分
    
    - 例如：*Operation匹配所有方法名以Operation结尾的方法
- 在方法参数列表部分，使用(..)表示参数列表任意
    
- 在方法参数列表部分，使用(int,..)表示参数列表以一个int类型的参数开头
    
- 在方法参数列表部分，基本数据类型和对应的包装类型是不一样的
    
    - 切入点表达式中使用 int 和实际方法中 Integer 是不匹配的
- 在方法返回值部分，如果想要明确指定一个返回值类型，那么必须同时写明权限修饰符
    
    - 例如：execution(public int _.._Service._(.., int)) 正确  
        例如：execution(_ int *.._Service._(.., int)) 错误

[![images](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img025.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img025.png)

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-4-6%E3%80%81%E9%87%8D%E7%94%A8%E5%88%87%E5%85%A5%E7%82%B9%E8%A1%A8%E8%BE%BE%E5%BC%8F "5.4.6、重用切入点表达式")5.4.6、重用切入点表达式

**①声明**

java

|   |   |
|---|---|
|1  <br>2|@Pointcut("execution(* com.atguigu.aop.annotation.*.*(..))")  <br>public void pointCut(){}|

**②在同一个切面中使用**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|@Before("pointCut()")  <br>public void beforeMethod(JoinPoint joinPoint){  <br>    String methodName = joinPoint.getSignature().getName();  <br>    String args = Arrays.toString(joinPoint.getArgs());  <br>    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);  <br>}|

**③在不同切面中使用**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|@Before("com.atguigu.aop.CommonPointCut.pointCut()")  <br>public void beforeMethod(JoinPoint joinPoint){  <br>    String methodName = joinPoint.getSignature().getName();  <br>    String args = Arrays.toString(joinPoint.getArgs());  <br>    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-4-7%E3%80%81%E8%8E%B7%E5%8F%96%E9%80%9A%E7%9F%A5%E7%9A%84%E7%9B%B8%E5%85%B3%E4%BF%A1%E6%81%AF "5.4.7、获取通知的相关信息")5.4.7、获取通知的相关信息

**①获取连接点信息**

获取连接点信息可以在通知方法的参数位置设置JoinPoint类型的形参

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8|@Before("execution(public int com.atguigu.aop.annotation.CalculatorImpl.*(..))")  <br>public void beforeMethod(JoinPoint joinPoint){  <br>    //获取连接点的签名信息  <br>    String methodName = joinPoint.getSignature().getName();  <br>    //获取目标方法到的实参信息  <br>    String args = Arrays.toString(joinPoint.getArgs());  <br>    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);  <br>}|

**②获取目标方法的返回值**

@AfterReturning中的属性returning，用来将通知方法的某个形参，接收目标方法的返回值

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5|@AfterReturning(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", returning = "result")  <br>public void afterReturningMethod(JoinPoint joinPoint, Object result){  <br>    String methodName = joinPoint.getSignature().getName();  <br>    System.out.println("Logger-->返回通知，方法名："+methodName+"，结果："+result);  <br>}|

**③获取目标方法的异常**

@AfterThrowing中的属性throwing，用来将通知方法的某个形参，接收目标方法的异常

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5|@AfterThrowing(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", throwing = "ex")  <br>public void afterThrowingMethod(JoinPoint joinPoint, Throwable ex){  <br>    String methodName = joinPoint.getSignature().getName();  <br>    System.out.println("Logger-->异常通知，方法名："+methodName+"，异常："+ex);  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-4-8%E3%80%81%E7%8E%AF%E7%BB%95%E9%80%9A%E7%9F%A5 "5.4.8、环绕通知")5.4.8、环绕通知

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18|@Around("execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))")  <br>public Object aroundMethod(ProceedingJoinPoint joinPoint){  <br>    String methodName = joinPoint.getSignature().getName();  <br>    String args = Arrays.toString(joinPoint.getArgs());  <br>    Object result = null;  <br>    try {  <br>        System.out.println("环绕通知-->目标对象方法执行之前");  <br>        //目标方法的执行，目标方法的返回值一定要返回给外界调用者  <br>        result = joinPoint.proceed();  <br>        System.out.println("环绕通知-->目标对象方法返回值之后");  <br>    } catch (Throwable throwable) {  <br>        throwable.printStackTrace();  <br>        System.out.println("环绕通知-->目标对象方法出现异常时");  <br>    } finally {  <br>        System.out.println("环绕通知-->目标对象方法执行完毕");  <br>    }  <br>    return result;  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-4-9%E3%80%81%E5%88%87%E9%9D%A2%E7%9A%84%E4%BC%98%E5%85%88%E7%BA%A7 "5.4.9、切面的优先级")5.4.9、切面的优先级

相同目标方法上同时存在多个切面时，切面的优先级控制切面的**内外嵌套**顺序。

- 优先级高的切面：外面
- 优先级低的切面：里面

使用@Order注解可以控制切面的优先级：

- @Order(较小的数)：优先级高
- @Order(较大的数)：优先级低

[![images](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img026.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/img026.png)

### [](https://blog.mohic.site/2024/05/18/spring6/#5-5%E3%80%81%E5%9F%BA%E4%BA%8EXML%E7%9A%84AOP "5.5、基于XML的AOP")5.5、基于XML的AOP

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-5-1%E3%80%81%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C "5.5.1、准备工作")5.5.1、准备工作

参考基于注解的AOP环境

#### [](https://blog.mohic.site/2024/05/18/spring6/#5-5-2%E3%80%81%E5%AE%9E%E7%8E%B0 "5.5.2、实现")5.5.2、实现

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14|<context:component-scan base-package="com.atguigu.aop.xml"></context:component-scan>  <br>  <br><aop:config>  <br>    <!--配置切面类-->  <br>    <aop:aspect ref="loggerAspect">  <br>        <aop:pointcut id="pointCut"   <br>                   expression="execution(* com.atguigu.aop.xml.CalculatorImpl.*(..))"/>  <br>        <aop:before method="beforeMethod" pointcut-ref="pointCut"></aop:before>  <br>        <aop:after method="afterMethod" pointcut-ref="pointCut"></aop:after>  <br>        <aop:after-returning method="afterReturningMethod" returning="result" pointcut-ref="pointCut"></aop:after-returning>  <br>        <aop:after-throwing method="afterThrowingMethod" throwing="ex" pointcut-ref="pointCut"></aop:after-throwing>  <br>        <aop:around method="aroundMethod" pointcut-ref="pointCut"></aop:around>  <br>    </aop:aspect>  <br></aop:config>|

## [](https://blog.mohic.site/2024/05/18/spring6/#6%E3%80%81%E5%8D%95%E5%85%83%E6%B5%8B%E8%AF%95%EF%BC%9AJUnit "6、单元测试：JUnit")6、单元测试：JUnit

在之前的测试方法中，几乎都能看到以下的两行代码：

java

|   |   |
|---|---|
|1  <br>2|ApplicationContext context = new ClassPathXmlApplicationContext("xxx.xml");  <br>Xxxx xxx = context.getBean(Xxxx.class);|

这两行代码的作用是创建Spring容器，最终获取到对象，但是每次测试都需要重复编写。针对上述问题，我们需要的是程序能自动帮我们创建容器。我们都知道JUnit无法知晓我们是否使用了 Spring 框架，更不用说帮我们创建 Spring 容器了。Spring提供了一个运行器，可以读取配置文件（或注解）来创建容器。我们只需要告诉它配置文件位置就可以了。这样一来，我们通过Spring整合JUnit可以使程序创建spring容器了

### [](https://blog.mohic.site/2024/05/18/spring6/#6-1%E3%80%81%E6%95%B4%E5%90%88JUnit5 "6.1、整合JUnit5")6.1、整合JUnit5

#### [](https://blog.mohic.site/2024/05/18/spring6/#6-1-1%E3%80%81%E6%90%AD%E5%BB%BA%E5%AD%90%E6%A8%A1%E5%9D%97 "6.1.1、搭建子模块")6.1.1、搭建子模块

搭建spring-junit模块

#### [](https://blog.mohic.site/2024/05/18/spring6/#6-1-2%E3%80%81%E5%BC%95%E5%85%A5%E4%BE%9D%E8%B5%96 "6.1.2、引入依赖")6.1.2、引入依赖

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35|<dependencies>  <br>    <!--spring context依赖-->  <br>    <!--当你引入Spring Context依赖之后，表示将Spring的基础依赖引入了-->  <br>    <dependency>  <br>        <groupId>org.springframework</groupId>  <br>        <artifactId>spring-context</artifactId>  <br>        <version>6.0.2</version>  <br>    </dependency>  <br>  <br>    <!--spring对junit的支持相关依赖-->  <br>    <dependency>  <br>        <groupId>org.springframework</groupId>  <br>        <artifactId>spring-test</artifactId>  <br>        <version>6.0.2</version>  <br>    </dependency>  <br>  <br>    <!--junit5测试-->  <br>    <dependency>  <br>        <groupId>org.junit.jupiter</groupId>  <br>        <artifactId>junit-jupiter-api</artifactId>  <br>        <version>5.9.0</version>  <br>    </dependency>  <br>  <br>    <!--log4j2的依赖-->  <br>    <dependency>  <br>        <groupId>org.apache.logging.log4j</groupId>  <br>        <artifactId>log4j-core</artifactId>  <br>        <version>2.19.0</version>  <br>    </dependency>  <br>    <dependency>  <br>        <groupId>org.apache.logging.log4j</groupId>  <br>        <artifactId>log4j-slf4j2-impl</artifactId>  <br>        <version>2.19.0</version>  <br>    </dependency>  <br></dependencies>|

#### [](https://blog.mohic.site/2024/05/18/spring6/#6-1-3%E3%80%81%E6%B7%BB%E5%8A%A0%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6 "6.1.3、添加配置文件")6.1.3、添加配置文件

beans.xml

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8|<?xml version="1.0" encoding="UTF-8"?>  <br><beans xmlns="http://www.springframework.org/schema/beans"  <br>       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  <br>       xmlns:context="http://www.springframework.org/schema/context"  <br>       xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd  <br>                           http://www.springframework.org/schema/context http://www.springframework.org/schema/context/spring-context.xsd">  <br>    <context:component-scan base-package="com.atguigu.spring6.bean"/>  <br></beans>|

copy日志文件：log4j2.xml

#### [](https://blog.mohic.site/2024/05/18/spring6/#6-1-4%E3%80%81%E6%B7%BB%E5%8A%A0java%E7%B1%BB "6.1.4、添加java类")6.1.4、添加java类

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11|package com.atguigu.spring6.bean;  <br>  <br>import org.springframework.stereotype.Component;  <br>  <br>@Component  <br>public class User {  <br>  <br>    public User() {  <br>        System.out.println("run user");  <br>    }  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#6-1-5%E3%80%81%E6%B5%8B%E8%AF%95 "6.1.5、测试")6.1.5、测试

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24|import com.atguigu.spring6.bean.User;  <br>import org.junit.jupiter.api.Test;  <br>import org.junit.jupiter.api.extension.ExtendWith;  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.test.context.ContextConfiguration;  <br>import org.springframework.test.context.junit.jupiter.SpringExtension;  <br>import org.springframework.test.context.junit.jupiter.SpringJUnitConfig;  <br>  <br>//两种方式均可  <br>//方式一  <br>//@ExtendWith(SpringExtension.class)  <br>//@ContextConfiguration("classpath:beans.xml")  <br>//方式二  <br>@SpringJUnitConfig(locations = "classpath:beans.xml")  <br>public class SpringJUnit5Test {  <br>  <br>    @Autowired  <br>    private User user;  <br>  <br>    @Test  <br>    public void testUser(){  <br>        System.out.println(user);  <br>    }  <br>}|

### [](https://blog.mohic.site/2024/05/18/spring6/#6-2%E3%80%81%E6%95%B4%E5%90%88JUnit4 "6.2、整合JUnit4")6.2、整合JUnit4

JUnit4在公司也会经常用到，在此也学习一下

#### [](https://blog.mohic.site/2024/05/18/spring6/#6-2-1%E3%80%81%E6%B7%BB%E5%8A%A0%E4%BE%9D%E8%B5%96 "6.2.1、添加依赖")6.2.1、添加依赖

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|<!-- junit测试 -->  <br><dependency>  <br>    <groupId>junit</groupId>  <br>    <artifactId>junit</artifactId>  <br>    <version>4.12</version>  <br></dependency>|

#### [](https://blog.mohic.site/2024/05/18/spring6/#6-2-2%E3%80%81%E6%B5%8B%E8%AF%95 "6.2.2、测试")6.2.2、测试

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19|import com.atguigu.spring6.bean.User;  <br>import org.junit.Test;  <br>import org.junit.runner.RunWith;  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.test.context.ContextConfiguration;  <br>import org.springframework.test.context.junit4.SpringJUnit4ClassRunner;  <br>  <br>@RunWith(SpringJUnit4ClassRunner.class)  <br>@ContextConfiguration("classpath:beans.xml")  <br>public class SpringJUnit4Test {  <br>  <br>    @Autowired  <br>    private User user;  <br>  <br>    @Test  <br>    public void testUser(){  <br>        System.out.println(user);  <br>    }  <br>}|

## [](https://blog.mohic.site/2024/05/18/spring6/#7%E3%80%81%E4%BA%8B%E5%8A%A1 "7、事务")7、事务

### [](https://blog.mohic.site/2024/05/18/spring6/#7-1%E3%80%81JdbcTemplate "7.1、JdbcTemplate")7.1、JdbcTemplate

#### [](https://blog.mohic.site/2024/05/18/spring6/#7-1-1%E3%80%81%E7%AE%80%E4%BB%8B "7.1.1、简介")7.1.1、简介

[![image-20221217115515670](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221217115515670.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221217115515670.png)

Spring 框架对 JDBC 进行封装，使用 JdbcTemplate 方便实现对数据库操作

#### [](https://blog.mohic.site/2024/05/18/spring6/#7-1-2%E3%80%81%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C "7.1.2、准备工作")7.1.2、准备工作

**①搭建子模块**

搭建子模块：spring-jdbc-tx

**②加入依赖**

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20|<dependencies>  <br>    <!--spring jdbc  Spring 持久化层支持jar包-->  <br>    <dependency>  <br>        <groupId>org.springframework</groupId>  <br>        <artifactId>spring-jdbc</artifactId>  <br>        <version>6.0.2</version>  <br>    </dependency>  <br>    <!-- MySQL驱动 -->  <br>    <dependency>  <br>        <groupId>mysql</groupId>  <br>        <artifactId>mysql-connector-java</artifactId>  <br>        <version>8.0.30</version>  <br>    </dependency>  <br>    <!-- 数据源 -->  <br>    <dependency>  <br>        <groupId>com.alibaba</groupId>  <br>        <artifactId>druid</artifactId>  <br>        <version>1.2.15</version>  <br>    </dependency>  <br></dependencies>|

**③创建jdbc.properties**

properties

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4|jdbc.user=root  <br>jdbc.password=root  <br>jdbc.url=jdbc:mysql://localhost:3306/spring?characterEncoding=utf8&useSSL=false  <br>jdbc.driver=com.mysql.cj.jdbc.Driver|

**④配置Spring的配置文件**

beans.xml

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27|<?xml version="1.0" encoding="UTF-8"?>  <br><beans xmlns="http://www.springframework.org/schema/beans"  <br>       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  <br>       xmlns:context="http://www.springframework.org/schema/context"  <br>       xsi:schemaLocation="http://www.springframework.org/schema/beans  <br>       http://www.springframework.org/schema/beans/spring-beans.xsd  <br>       http://www.springframework.org/schema/context  <br>       http://www.springframework.org/schema/context/spring-context.xsd">  <br>  <br>    <!-- 导入外部属性文件 -->  <br>    <context:property-placeholder location="classpath:jdbc.properties" />  <br>  <br>    <!-- 配置数据源 -->  <br>    <bean id="druidDataSource" class="com.alibaba.druid.pool.DruidDataSource">  <br>        <property name="url" value="${jdbc.url}"/>  <br>        <property name="driverClassName" value="${jdbc.driver}"/>  <br>        <property name="username" value="${jdbc.user}"/>  <br>        <property name="password" value="${jdbc.password}"/>  <br>    </bean>  <br>  <br>    <!-- 配置 JdbcTemplate -->  <br>    <bean id="jdbcTemplate" class="org.springframework.jdbc.core.JdbcTemplate">  <br>        <!-- 装配数据源 -->  <br>        <property name="dataSource" ref="druidDataSource"/>  <br>    </bean>  <br>  <br></beans>|

**⑤准备数据库与测试表**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11|CREATE DATABASE `spring`;  <br>  <br>use `spring`;  <br>  <br>CREATE TABLE `t_emp` (  <br>  `id` int(11) NOT NULL AUTO_INCREMENT,  <br>  `name` varchar(20) DEFAULT NULL COMMENT '姓名',  <br>  `age` int(11) DEFAULT NULL COMMENT '年龄',  <br>  `sex` varchar(2) DEFAULT NULL COMMENT '性别',  <br>  PRIMARY KEY (`id`)  <br>) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;|

#### [](https://blog.mohic.site/2024/05/18/spring6/#7-1-3%E3%80%81%E5%AE%9E%E7%8E%B0CURD "7.1.3、实现CURD")7.1.3、实现CURD

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A0%E8%A3%85%E9%85%8D-JdbcTemplate "①装配 JdbcTemplate")①装配 JdbcTemplate

**创建测试类，整合JUnit，注入JdbcTemplate**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13|package com.atguigu.spring6;  <br>  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.jdbc.core.JdbcTemplate;  <br>import org.springframework.test.context.junit.jupiter.SpringJUnitConfig;  <br>  <br>@SpringJUnitConfig(locations = "classpath:beans.xml")  <br>public class JDBCTemplateTest {  <br>  <br>    @Autowired  <br>    private JdbcTemplate jdbcTemplate;  <br>      <br>}|

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A1%E6%B5%8B%E8%AF%95%E5%A2%9E%E5%88%A0%E6%94%B9%E5%8A%9F%E8%83%BD "②测试增删改功能")②测试增删改功能

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15|@Test  <br>//测试增删改功能  <br>public void testUpdate(){  <br>    //添加功能  <br>	String sql = "insert into t_emp values(null,?,?,?)";  <br>	int result = jdbcTemplate.update(sql, "张三", 23, "男");  <br>      <br>    //修改功能  <br>	//String sql = "update t_emp set name=? where id=?";  <br>    //int result = jdbcTemplate.update(sql, "张三atguigu", 1);  <br>  <br>    //删除功能  <br>	//String sql = "delete from t_emp where id=?";  <br>	//int result = jdbcTemplate.update(sql, 1);  <br>}|

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A2%E6%9F%A5%E8%AF%A2%E6%95%B0%E6%8D%AE%E8%BF%94%E5%9B%9E%E5%AF%B9%E8%B1%A1 "③查询数据返回对象")③查询数据返回对象

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20|public class Emp {  <br>  <br>    private Integer id;  <br>    private String name;  <br>    private Integer age;  <br>    private String sex;  <br>  <br>    //生成get和set方法  <br>    //......  <br>  <br>    @Override  <br>    public String toString() {  <br>        return "Emp{" +  <br>                "id=" + id +  <br>                ", name='" + name + '\'' +  <br>                ", age=" + age +  <br>                ", sex='" + sex + '\'' +  <br>                '}';  <br>    }  <br>}|

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22|//查询：返回对象  <br>@Test  <br>public void testSelectObject() {  <br>    //写法一  <br>//        String sql = "select * from t_emp where id=?";  <br>//        Emp empResult = jdbcTemplate.queryForObject(sql,  <br>//                (rs, rowNum) -> {  <br>//                    Emp emp = new Emp();  <br>//                    emp.setId(rs.getInt("id"));  <br>//                    emp.setName(rs.getString("name"));  <br>//                    emp.setAge(rs.getInt("age"));  <br>//                    emp.setSex(rs.getString("sex"));  <br>//                    return emp;  <br>//                }, 1);  <br>//        System.out.println(empResult);  <br>  <br>    //写法二  <br>    String sql = "select * from t_emp where id=?";  <br>    Emp emp = jdbcTemplate.queryForObject(sql,  <br>                  new BeanPropertyRowMapper<>(Emp.class),1);  <br>    System.out.println(emp);  <br>}|

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A3%E6%9F%A5%E8%AF%A2%E6%95%B0%E6%8D%AE%E8%BF%94%E5%9B%9Elist%E9%9B%86%E5%90%88 "④查询数据返回list集合")④查询数据返回list集合

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7|@Test  <br>//查询多条数据为一个list集合  <br>public void testSelectList(){  <br>    String sql = "select * from t_emp";  <br>    List<Emp> list = jdbcTemplate.query(sql, new BeanPropertyRowMapper<>(Emp.class));  <br>    System.out.println(list);  <br>}|

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A4%E6%9F%A5%E8%AF%A2%E8%BF%94%E5%9B%9E%E5%8D%95%E4%B8%AA%E7%9A%84%E5%80%BC "⑤查询返回单个的值")⑤查询返回单个的值

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7|@Test  <br>//查询单行单列的值  <br>public void selectCount(){  <br>    String sql = "select count(id) from t_emp";  <br>    Integer count = jdbcTemplate.queryForObject(sql, Integer.class);  <br>    System.out.println(count);  <br>}|

### [](https://blog.mohic.site/2024/05/18/spring6/#7-2%E3%80%81%E5%A3%B0%E6%98%8E%E5%BC%8F%E4%BA%8B%E5%8A%A1%E6%A6%82%E5%BF%B5 "7.2、声明式事务概念")7.2、声明式事务概念

#### [](https://blog.mohic.site/2024/05/18/spring6/#7-2-1%E3%80%81%E4%BA%8B%E5%8A%A1%E5%9F%BA%E6%9C%AC%E6%A6%82%E5%BF%B5 "7.2.1、事务基本概念")7.2.1、事务基本概念

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A0%E4%BB%80%E4%B9%88%E6%98%AF%E4%BA%8B%E5%8A%A1 "①什么是事务")①什么是事务

数据库事务( transaction)是访问并可能操作各种数据项的一个数据库操作序列，这些操作要么全部执行,要么全部不执行，是一个不可分割的工作单位。事务由事务开始与事务结束之间执行的全部数据库操作组成。

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A1%E4%BA%8B%E5%8A%A1%E7%9A%84%E7%89%B9%E6%80%A7 "②事务的特性")②事务的特性

**A：原子性(Atomicity)**

一个事务(transaction)中的所有操作，要么全部完成，要么全部不完成，不会结束在中间某个环节。事务在执行过程中发生错误，会被回滚（Rollback）到事务开始前的状态，就像这个事务从来没有执行过一样。

**C：一致性(Consistency)**

事务的一致性指的是在一个事务执行之前和执行之后数据库都必须处于一致性状态。

如果事务成功地完成，那么系统中所有变化将正确地应用，系统处于有效状态。

如果在事务中出现错误，那么系统中的所有变化将自动地回滚，系统返回到原始状态。

**I：隔离性(Isolation)**

指的是在并发环境中，当不同的事务同时操纵相同的数据时，每个事务都有各自的完整数据空间。由并发事务所做的修改必须与任何其他并发事务所做的修改隔离。事务查看数据更新时，数据所处的状态要么是另一事务修改它之前的状态，要么是另一事务修改它之后的状态，事务不会查看到中间状态的数据。

**D：持久性(Durability)**

指的是只要事务成功结束，它对数据库所做的更新就必须保存下来。即使发生系统崩溃，重新启动数据库系统后，数据库还能恢复到事务成功结束时的状态。

#### [](https://blog.mohic.site/2024/05/18/spring6/#7-2-2%E3%80%81%E7%BC%96%E7%A8%8B%E5%BC%8F%E4%BA%8B%E5%8A%A1 "7.2.2、编程式事务")7.2.2、编程式事务

事务功能的相关操作全部通过自己编写代码来实现：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23|Connection conn = ...;  <br>      <br>try {  <br>      <br>    // 开启事务：关闭事务的自动提交  <br>    conn.setAutoCommit(false);  <br>      <br>    // 核心操作  <br>      <br>    // 提交事务  <br>    conn.commit();  <br>      <br>}catch(Exception e){  <br>      <br>    // 回滚事务  <br>    conn.rollBack();  <br>      <br>}finally{  <br>      <br>    // 释放数据库连接  <br>    conn.close();  <br>      <br>}|

编程式的实现方式存在缺陷：

- 细节没有被屏蔽：具体操作过程中，所有细节都需要程序员自己来完成，比较繁琐。
- 代码复用性不高：如果没有有效抽取出来，每次实现功能都需要自己编写代码，代码就没有得到复用。

#### [](https://blog.mohic.site/2024/05/18/spring6/#7-2-3%E3%80%81%E5%A3%B0%E6%98%8E%E5%BC%8F%E4%BA%8B%E5%8A%A1 "7.2.3、声明式事务")7.2.3、声明式事务

既然事务控制的代码有规律可循，代码的结构基本是确定的，所以框架就可以将固定模式的代码抽取出来，进行相关的封装。

封装起来后，我们只需要在配置文件中进行简单的配置即可完成操作。

- 好处1：提高开发效率
- 好处2：消除了冗余的代码
- 好处3：框架会综合考虑相关领域中在实际开发环境下有可能遇到的各种问题，进行了健壮性、性能等各个方面的优化

所以，我们可以总结下面两个概念：

- **编程式**：**自己写代码**实现功能
- **声明式**：通过**配置**让**框架**实现功能

### [](https://blog.mohic.site/2024/05/18/spring6/#7-3%E3%80%81%E5%9F%BA%E4%BA%8E%E6%B3%A8%E8%A7%A3%E7%9A%84%E5%A3%B0%E6%98%8E%E5%BC%8F%E4%BA%8B%E5%8A%A1 "7.3、基于注解的声明式事务")7.3、基于注解的声明式事务

#### [](https://blog.mohic.site/2024/05/18/spring6/#7-3-1%E3%80%81%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C "7.3.1、准备工作")7.3.1、准备工作

**①添加配置**

在beans.xml添加配置

xml

|   |   |
|---|---|
|1  <br>2|<!--扫描组件-->  <br><context:component-scan base-package="com.atguigu.spring6"></context:component-scan>|

**②创建表**

sql

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15|CREATE TABLE `t_book` (  <br>  `book_id` int(11) NOT NULL AUTO_INCREMENT COMMENT '主键',  <br>  `book_name` varchar(20) DEFAULT NULL COMMENT '图书名称',  <br>  `price` int(11) DEFAULT NULL COMMENT '价格',  <br>  `stock` int(10) unsigned DEFAULT NULL COMMENT '库存（无符号）',  <br>  PRIMARY KEY (`book_id`)  <br>) ENGINE=InnoDB AUTO_INCREMENT=3 DEFAULT CHARSET=utf8;  <br>insert  into `t_book`(`book_id`,`book_name`,`price`,`stock`) values (1,'斗破苍穹',80,100),(2,'斗罗大陆',50,100);  <br>CREATE TABLE `t_user` (  <br>  `user_id` int(11) NOT NULL AUTO_INCREMENT COMMENT '主键',  <br>  `username` varchar(20) DEFAULT NULL COMMENT '用户名',  <br>  `balance` int(10) unsigned DEFAULT NULL COMMENT '余额（无符号）',  <br>  PRIMARY KEY (`user_id`)  <br>) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8;  <br>insert  into `t_user`(`user_id`,`username`,`balance`) values (1,'admin',50);|

**③创建组件**

创建BookController：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12|package com.atguigu.spring6.controller;  <br>  <br>@Controller  <br>public class BookController {  <br>  <br>    @Autowired  <br>    private BookService bookService;  <br>  <br>    public void buyBook(Integer bookId, Integer userId){  <br>        bookService.buyBook(bookId, userId);  <br>    }  <br>}|

创建接口BookService：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4|package com.atguigu.spring6.service;  <br>public interface BookService {  <br>    void buyBook(Integer bookId, Integer userId);  <br>}|

创建实现类BookServiceImpl：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17|package com.atguigu.spring6.service.impl;  <br>@Service  <br>public class BookServiceImpl implements BookService {  <br>  <br>    @Autowired  <br>    private BookDao bookDao;  <br>  <br>    @Override  <br>    public void buyBook(Integer bookId, Integer userId) {  <br>        //查询图书的价格  <br>        Integer price = bookDao.getPriceByBookId(bookId);  <br>        //更新图书的库存  <br>        bookDao.updateStock(bookId);  <br>        //更新用户的余额  <br>        bookDao.updateBalance(userId, price);  <br>    }  <br>}|

创建接口BookDao：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8|package com.atguigu.spring6.dao;  <br>public interface BookDao {  <br>    Integer getPriceByBookId(Integer bookId);  <br>  <br>    void updateStock(Integer bookId);  <br>  <br>    void updateBalance(Integer userId, Integer price);  <br>}|

创建实现类BookDaoImpl：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25|package com.atguigu.spring6.dao.impl;  <br>@Repository  <br>public class BookDaoImpl implements BookDao {  <br>  <br>    @Autowired  <br>    private JdbcTemplate jdbcTemplate;  <br>  <br>    @Override  <br>    public Integer getPriceByBookId(Integer bookId) {  <br>        String sql = "select price from t_book where book_id = ?";  <br>        return jdbcTemplate.queryForObject(sql, Integer.class, bookId);  <br>    }  <br>  <br>    @Override  <br>    public void updateStock(Integer bookId) {  <br>        String sql = "update t_book set stock = stock - 1 where book_id = ?";  <br>        jdbcTemplate.update(sql, bookId);  <br>    }  <br>  <br>    @Override  <br>    public void updateBalance(Integer userId, Integer price) {  <br>        String sql = "update t_user set balance = balance - ? where user_id = ?";  <br>        jdbcTemplate.update(sql, price, userId);  <br>    }  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#7-3-2%E3%80%81%E6%B5%8B%E8%AF%95%E6%97%A0%E4%BA%8B%E5%8A%A1%E6%83%85%E5%86%B5 "7.3.2、测试无事务情况")7.3.2、测试无事务情况

**①创建测试类**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17|import org.junit.jupiter.api.Test;  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.jdbc.core.JdbcTemplate;  <br>import org.springframework.test.context.junit.jupiter.SpringJUnitConfig;  <br>  <br>@SpringJUnitConfig(locations = "classpath:beans.xml")  <br>public class TxByAnnotationTest {  <br>  <br>    @Autowired  <br>    private BookController bookController;  <br>  <br>    @Test  <br>    public void testBuyBook(){  <br>        bookController.buyBook(1, 1);  <br>    }  <br>  <br>}|

**②模拟场景**

用户购买图书，先查询图书的价格，再更新图书的库存和用户的余额

假设用户id为1的用户，购买id为1的图书

用户余额为50，而图书价格为80

购买图书之后，用户的余额为-30，数据库中余额字段设置了无符号，因此无法将-30插入到余额字段

此时执行sql语句会抛出SQLException

**③观察结果**

因为没有添加事务，图书的库存更新了，但是用户的余额没有更新

显然这样的结果是错误的，购买图书是一个完整的功能，更新库存和更新余额要么都成功要么都失败

#### [](https://blog.mohic.site/2024/05/18/spring6/#7-3-3%E3%80%81%E5%8A%A0%E5%85%A5%E4%BA%8B%E5%8A%A1 "7.3.3、加入事务")7.3.3、加入事务

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A0%E6%B7%BB%E5%8A%A0%E4%BA%8B%E5%8A%A1%E9%85%8D%E7%BD%AE "①添加事务配置")①添加事务配置

在spring配置文件中引入tx命名空间

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11|<?xml version="1.0" encoding="UTF-8"?>  <br><beans xmlns="http://www.springframework.org/schema/beans"  <br>       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  <br>       xmlns:context="http://www.springframework.org/schema/context"  <br>       xmlns:tx="http://www.springframework.org/schema/tx"  <br>       xsi:schemaLocation="http://www.springframework.org/schema/beans  <br>       http://www.springframework.org/schema/beans/spring-beans.xsd  <br>       http://www.springframework.org/schema/context  <br>       http://www.springframework.org/schema/context/spring-context.xsd  <br>       http://www.springframework.org/schema/tx  <br>       http://www.springframework.org/schema/tx/spring-tx.xsd">|

在Spring的配置文件中添加配置：

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10|<bean id="transactionManager" class="org.springframework.jdbc.datasource.DataSourceTransactionManager">  <br>    <property name="dataSource" ref="druidDataSource"></property>  <br></bean>  <br>  <br><!--  <br>    开启事务的注解驱动  <br>    通过注解@Transactional所标识的方法或标识的类中所有的方法，都会被事务管理器管理事务  <br>-->  <br><!-- transaction-manager属性的默认值是transactionManager，如果事务管理器bean的id正好就是这个默认值，则可以省略这个属性 -->  <br><tx:annotation-driven transaction-manager="transactionManager" />|

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A1%E6%B7%BB%E5%8A%A0%E4%BA%8B%E5%8A%A1%E6%B3%A8%E8%A7%A3 "②添加事务注解")②添加事务注解

因为service层表示业务逻辑层，一个方法表示一个完成的功能，因此处理事务一般在service层处理

**在BookServiceImpl的buybook()添加注解@Transactional**

##### [](https://blog.mohic.site/2024/05/18/spring6/#%E2%91%A2%E8%A7%82%E5%AF%9F%E7%BB%93%E6%9E%9C "③观察结果")③观察结果

由于使用了Spring的声明式事务，更新库存和更新余额都没有执行

#### [](https://blog.mohic.site/2024/05/18/spring6/#7-3-4%E3%80%81-Transactional%E6%B3%A8%E8%A7%A3%E6%A0%87%E8%AF%86%E7%9A%84%E4%BD%8D%E7%BD%AE "7.3.4、@Transactional注解标识的位置")7.3.4、@Transactional注解标识的位置

@Transactional标识在方法上，则只会影响该方法

@Transactional标识的类上，则会影响类中所有的方法

#### [](https://blog.mohic.site/2024/05/18/spring6/#7-3-5%E3%80%81%E4%BA%8B%E5%8A%A1%E5%B1%9E%E6%80%A7%EF%BC%9A%E5%8F%AA%E8%AF%BB "7.3.5、事务属性：只读")7.3.5、事务属性：只读

**①介绍**

对一个查询操作来说，如果我们把它设置成只读，就能够明确告诉数据库，这个操作不涉及写操作。这样数据库就能够针对查询操作来进行优化。

**②使用方式**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10|@Transactional(readOnly = true)  <br>public void buyBook(Integer bookId, Integer userId) {  <br>    //查询图书的价格  <br>    Integer price = bookDao.getPriceByBookId(bookId);  <br>    //更新图书的库存  <br>    bookDao.updateStock(bookId);  <br>    //更新用户的余额  <br>    bookDao.updateBalance(userId, price);  <br>    //System.out.println(1/0);  <br>}|

**③注意**

对增删改操作设置只读会抛出下面异常：

Caused by: java.sql.SQLException: Connection is read-only. Queries leading to data modification are not allowed

#### [](https://blog.mohic.site/2024/05/18/spring6/#7-3-6%E3%80%81%E4%BA%8B%E5%8A%A1%E5%B1%9E%E6%80%A7%EF%BC%9A%E8%B6%85%E6%97%B6 "7.3.6、事务属性：超时")7.3.6、事务属性：超时

**①介绍**

事务在执行过程中，有可能因为遇到某些问题，导致程序卡住，从而长时间占用数据库资源。而长时间占用资源，大概率是因为程序运行出现了问题（可能是Java程序或MySQL数据库或网络连接等等）。此时这个很可能出问题的程序应该被回滚，撤销它已做的操作，事务结束，把资源让出来，让其他正常程序可以执行。

概括来说就是一句话：超时回滚，释放资源。

**②使用方式**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16|//超时时间单位秒  <br>@Transactional(timeout = 3)  <br>public void buyBook(Integer bookId, Integer userId) {  <br>    try {  <br>        TimeUnit.SECONDS.sleep(5);  <br>    } catch (InterruptedException e) {  <br>        e.printStackTrace();  <br>    }  <br>    //查询图书的价格  <br>    Integer price = bookDao.getPriceByBookId(bookId);  <br>    //更新图书的库存  <br>    bookDao.updateStock(bookId);  <br>    //更新用户的余额  <br>    bookDao.updateBalance(userId, price);  <br>    //System.out.println(1/0);  <br>}|

**③观察结果**

执行过程中抛出异常：

org.springframework.transaction.**TransactionTimedOutException**: Transaction timed out: deadline was Fri Jun 04 16:25:39 CST 2022

#### [](https://blog.mohic.site/2024/05/18/spring6/#7-3-7%E3%80%81%E4%BA%8B%E5%8A%A1%E5%B1%9E%E6%80%A7%EF%BC%9A%E5%9B%9E%E6%BB%9A%E7%AD%96%E7%95%A5 "7.3.7、事务属性：回滚策略")7.3.7、事务属性：回滚策略

**①介绍**

声明式事务默认只针对运行时异常回滚，编译时异常不回滚。

可以通过@Transactional中相关属性设置回滚策略

- rollbackFor属性：需要设置一个Class类型的对象
    
- rollbackForClassName属性：需要设置一个字符串类型的全类名
    
- noRollbackFor属性：需要设置一个Class类型的对象
    
- rollbackFor属性：需要设置一个字符串类型的全类名
    

**②使用方式**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11|@Transactional(noRollbackFor = ArithmeticException.class)  <br>//@Transactional(noRollbackForClassName = "java.lang.ArithmeticException")  <br>public void buyBook(Integer bookId, Integer userId) {  <br>    //查询图书的价格  <br>    Integer price = bookDao.getPriceByBookId(bookId);  <br>    //更新图书的库存  <br>    bookDao.updateStock(bookId);  <br>    //更新用户的余额  <br>    bookDao.updateBalance(userId, price);  <br>    System.out.println(1/0);  <br>}|

**③观察结果**

虽然购买图书功能中出现了数学运算异常（ArithmeticException），但是我们设置的回滚策略是，当出现ArithmeticException不发生回滚，因此购买图书的操作正常执行

#### [](https://blog.mohic.site/2024/05/18/spring6/#7-3-8%E3%80%81%E4%BA%8B%E5%8A%A1%E5%B1%9E%E6%80%A7%EF%BC%9A%E9%9A%94%E7%A6%BB%E7%BA%A7%E5%88%AB "7.3.8、事务属性：隔离级别")7.3.8、事务属性：隔离级别

**①介绍**

数据库系统必须具有隔离并发运行各个事务的能力，使它们不会相互影响，避免各种并发问题。一个事务与其他事务隔离的程度称为隔离级别。SQL标准中规定了多种事务隔离级别，不同隔离级别对应不同的干扰程度，隔离级别越高，数据一致性就越好，但并发性越弱。

隔离级别一共有四种：

- 读未提交：READ UNCOMMITTED
    
    允许Transaction01读取Transaction02未提交的修改。
    
- 读已提交：READ COMMITTED、
    
    要求Transaction01只能读取Transaction02已提交的修改。
    
- 可重复读：REPEATABLE READ
    
    确保Transaction01可以多次从一个字段中读取到相同的值，即Transaction01执行期间禁止其它事务对这个字段进行更新。
    
- 串行化：SERIALIZABLE
    
    确保Transaction01可以多次从一个表中读取到相同的行，在Transaction01执行期间，禁止其它事务对这个表进行添加、更新、删除操作。可以避免任何并发问题，但性能十分低下。
    

各个隔离级别解决并发问题的能力见下表：

|隔离级别|脏读|不可重复读|幻读|
|---|---|---|---|
|READ UNCOMMITTED|有|有|有|
|READ COMMITTED|无|有|有|
|REPEATABLE READ|无|无|有|
|SERIALIZABLE|无|无|无|

各种数据库产品对事务隔离级别的支持程度：

|隔离级别|Oracle|MySQL|
|---|---|---|
|READ UNCOMMITTED|×|√|
|READ COMMITTED|√(默认)|√|
|REPEATABLE READ|×|√(默认)|
|SERIALIZABLE|√|√|

**②使用方式**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5|@Transactional(isolation = Isolation.DEFAULT)//使用数据库默认的隔离级别  <br>@Transactional(isolation = Isolation.READ_UNCOMMITTED)//读未提交  <br>@Transactional(isolation = Isolation.READ_COMMITTED)//读已提交  <br>@Transactional(isolation = Isolation.REPEATABLE_READ)//可重复读  <br>@Transactional(isolation = Isolation.SERIALIZABLE)//串行化|

#### [](https://blog.mohic.site/2024/05/18/spring6/#7-3-9%E3%80%81%E4%BA%8B%E5%8A%A1%E5%B1%9E%E6%80%A7%EF%BC%9A%E4%BC%A0%E6%92%AD%E8%A1%8C%E4%B8%BA "7.3.9、事务属性：传播行为")7.3.9、事务属性：传播行为

**①介绍**

什么是事务的传播行为？

在service类中有a()方法和b()方法，a()方法上有事务，b()方法上也有事务，当a()方法执行过程中调用了b()方法，事务是如何传递的？合并到一个事务里？还是开启一个新的事务？这就是事务传播行为。

一共有七种传播行为：

- REQUIRED：支持当前事务，如果不存在就新建一个(默认)**【没有就新建，有就加入】**
- SUPPORTS：支持当前事务，如果当前没有事务，就以非事务方式执行**【有就加入，没有就不管了】**
- MANDATORY：必须运行在一个事务中，如果当前没有事务正在发生，将抛出一个异常**【有就加入，没有就抛异常】**
- REQUIRES_NEW：开启一个新的事务，如果一个事务已经存在，则将这个存在的事务挂起**【不管有没有，直接开启一个新事务，开启的新事务和之前的事务不存在嵌套关系，之前事务被挂起】**
- NOT_SUPPORTED：以非事务方式运行，如果有事务存在，挂起当前事务**【不支持事务，存在就挂起】**
- NEVER：以非事务方式运行，如果有事务存在，抛出异常**【不支持事务，存在就抛异常】**
- NESTED：如果当前正有一个事务在进行中，则该方法应当运行在一个嵌套式事务中。被嵌套的事务可以独立于外层事务进行提交或回滚。如果外层事务不存在，行为就像REQUIRED一样。**【有事务的话，就在这个事务里再嵌套一个完全独立的事务，嵌套的事务可以独立的提交和回滚。没有事务就和REQUIRED一样。】**

**②测试**

创建接口CheckoutService：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5|package com.atguigu.spring6.service;  <br>  <br>public interface CheckoutService {  <br>    void checkout(Integer[] bookIds, Integer userId);  <br>}|

创建实现类CheckoutServiceImpl：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17|package com.atguigu.spring6.service.impl;  <br>  <br>@Service  <br>public class CheckoutServiceImpl implements CheckoutService {  <br>  <br>    @Autowired  <br>    private BookService bookService;  <br>  <br>    @Override  <br>    @Transactional  <br>    //一次购买多本图书  <br>    public void checkout(Integer[] bookIds, Integer userId) {  <br>        for (Integer bookId : bookIds) {  <br>            bookService.buyBook(bookId, userId);  <br>        }  <br>    }  <br>}|

在BookController中添加方法：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|@Autowired  <br>private CheckoutService checkoutService;  <br>  <br>public void checkout(Integer[] bookIds, Integer userId){  <br>    checkoutService.checkout(bookIds, userId);  <br>}|

在数据库中将用户的余额修改为100元

**③观察结果**

可以通过@Transactional中的propagation属性设置事务传播行为

修改BookServiceImpl中buyBook()上，注解@Transactional的propagation属性

@Transactional(propagation = Propagation.REQUIRED)，默认情况，表示如果当前线程上有已经开启的事务可用，那么就在这个事务中运行。经过观察，购买图书的方法buyBook()在checkout()中被调用，checkout()上有事务注解，因此在此事务中执行。所购买的两本图书的价格为80和50，而用户的余额为100，因此在购买第二本图书时余额不足失败，导致整个checkout()回滚，即只要有一本书买不了，就都买不了

@Transactional(propagation = Propagation.REQUIRES_NEW)，表示不管当前线程上是否有已经开启的事务，都要开启新事务。同样的场景，每次购买图书都是在buyBook()的事务中执行，因此第一本图书购买成功，事务结束，第二本图书购买失败，只在第二次的buyBook()中回滚，购买第一本图书不受影响，即能买几本就买几本。

#### [](https://blog.mohic.site/2024/05/18/spring6/#7-3-10%E3%80%81%E5%85%A8%E6%B3%A8%E8%A7%A3%E9%85%8D%E7%BD%AE%E4%BA%8B%E5%8A%A1 "7.3.10、全注解配置事务")7.3.10、全注解配置事务

**①添加配置类**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36  <br>37  <br>38  <br>39  <br>40|package com.atguigu.spring6.config;  <br>  <br>import com.alibaba.druid.pool.DruidDataSource;  <br>import org.springframework.context.annotation.Bean;  <br>import org.springframework.context.annotation.ComponentScan;  <br>import org.springframework.context.annotation.Configuration;  <br>import org.springframework.jdbc.core.JdbcTemplate;  <br>import org.springframework.jdbc.datasource.DataSourceTransactionManager;  <br>import org.springframework.transaction.annotation.EnableTransactionManagement;  <br>import javax.sql.DataSource;  <br>  <br>@Configuration  <br>@ComponentScan("com.atguigu.spring6")  <br>@EnableTransactionManagement  <br>public class SpringConfig {  <br>  <br>    @Bean  <br>    public DataSource getDataSource(){  <br>        DruidDataSource dataSource = new DruidDataSource();  <br>        dataSource.setDriverClassName("com.mysql.cj.jdbc.Driver");  <br>        dataSource.setUrl("jdbc:mysql://localhost:3306/spring?characterEncoding=utf8&useSSL=false");  <br>        dataSource.setUsername("root");  <br>        dataSource.setPassword("root");  <br>        return dataSource;  <br>    }  <br>  <br>    @Bean(name = "jdbcTemplate")  <br>    public JdbcTemplate getJdbcTemplate(DataSource dataSource){  <br>        JdbcTemplate jdbcTemplate = new JdbcTemplate();  <br>        jdbcTemplate.setDataSource(dataSource);  <br>        return jdbcTemplate;  <br>    }  <br>  <br>    @Bean  <br>    public DataSourceTransactionManager getDataSourceTransactionManager(DataSource dataSource){  <br>        DataSourceTransactionManager dataSourceTransactionManager = new DataSourceTransactionManager();  <br>        dataSourceTransactionManager.setDataSource(dataSource);  <br>        return dataSourceTransactionManager;  <br>    }  <br>}|

**②测试**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17|import com.atguigu.spring6.config.SpringConfig;  <br>import com.atguigu.spring6.controller.BookController;  <br>import org.junit.jupiter.api.Test;  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.context.ApplicationContext;  <br>import org.springframework.context.annotation.AnnotationConfigApplicationContext;  <br>import org.springframework.test.context.junit.jupiter.SpringJUnitConfig;  <br>  <br>public class TxByAllAnnotationTest {  <br>  <br>    @Test  <br>    public void testTxAllAnnotation(){  <br>        ApplicationContext applicationContext = new AnnotationConfigApplicationContext(SpringConfig.class);  <br>        BookController accountService = applicationContext.getBean("bookController", BookController.class);  <br>        accountService.buyBook(1, 1);  <br>    }  <br>}|

### [](https://blog.mohic.site/2024/05/18/spring6/#7-4%E3%80%81%E5%9F%BA%E4%BA%8EXML%E7%9A%84%E5%A3%B0%E6%98%8E%E5%BC%8F%E4%BA%8B%E5%8A%A1 "7.4、基于XML的声明式事务")7.4、基于XML的声明式事务

#### [](https://blog.mohic.site/2024/05/18/spring6/#7-3-1%E3%80%81%E5%9C%BA%E6%99%AF%E6%A8%A1%E6%8B%9F "7.3.1、场景模拟")7.3.1、场景模拟

参考基于注解的声明式事务

#### [](https://blog.mohic.site/2024/05/18/spring6/#7-3-2%E3%80%81%E4%BF%AE%E6%94%B9Spring%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6 "7.3.2、修改Spring配置文件")7.3.2、修改Spring配置文件

将Spring配置文件中去掉tx:annotation-driven 标签，并添加配置：

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26|<aop:config>  <br>    <!-- 配置事务通知和切入点表达式 -->  <br>    <aop:advisor advice-ref="txAdvice" pointcut="execution(* com.atguigu.spring.tx.xml.service.impl.*.*(..))"></aop:advisor>  <br></aop:config>  <br><!-- tx:advice标签：配置事务通知 -->  <br><!-- id属性：给事务通知标签设置唯一标识，便于引用 -->  <br><!-- transaction-manager属性：关联事务管理器 -->  <br><tx:advice id="txAdvice" transaction-manager="transactionManager">  <br>    <tx:attributes>  <br>        <!-- tx:method标签：配置具体的事务方法 -->  <br>        <!-- name属性：指定方法名，可以使用星号代表多个字符 -->  <br>        <tx:method name="get*" read-only="true"/>  <br>        <tx:method name="query*" read-only="true"/>  <br>        <tx:method name="find*" read-only="true"/>  <br>      <br>        <!-- read-only属性：设置只读属性 -->  <br>        <!-- rollback-for属性：设置回滚的异常 -->  <br>        <!-- no-rollback-for属性：设置不回滚的异常 -->  <br>        <!-- isolation属性：设置事务的隔离级别 -->  <br>        <!-- timeout属性：设置事务的超时属性 -->  <br>        <!-- propagation属性：设置事务的传播行为 -->  <br>        <tx:method name="save*" read-only="false" rollback-for="java.lang.Exception" propagation="REQUIRES_NEW"/>  <br>        <tx:method name="update*" read-only="false" rollback-for="java.lang.Exception" propagation="REQUIRES_NEW"/>  <br>        <tx:method name="delete*" read-only="false" rollback-for="java.lang.Exception" propagation="REQUIRES_NEW"/>  <br>    </tx:attributes>  <br></tx:advice>|

> 注意：基于xml实现的声明式事务，必须引入aspectJ的依赖
> 
> xml
> 
> |   |   |
> |---|---|
> |1  <br>2  <br>3  <br>4  <br>5|<dependency>  <br>     <groupId>org.springframework</groupId>  <br>     <artifactId>spring-aspects</artifactId>  <br>     <version>6.0.2</version>  <br></dependency>|

## [](https://blog.mohic.site/2024/05/18/spring6/#8%E3%80%81%E8%B5%84%E6%BA%90%E6%93%8D%E4%BD%9C%EF%BC%9AResources "8、资源操作：Resources")8、资源操作：Resources

### [](https://blog.mohic.site/2024/05/18/spring6/#8-1%E3%80%81Spring-Resources%E6%A6%82%E8%BF%B0 "8.1、Spring Resources概述")8.1、Spring Resources概述

[![image-20221218154945878](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221218154945878.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221218154945878.png)

[![image-20221206231535991](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221206231535991.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221206231535991.png)

Java的标准java.net.URL类和各种URL前缀的标准处理程序无法满足所有对low-level资源的访问，比如：没有标准化的 URL 实现可用于访问需要从类路径或相对于 ServletContext 获取的资源。并且缺少某些Spring所需要的功能，例如检测某资源是否存在等。**而Spring的Resource声明了访问low-level资源的能力。**

### [](https://blog.mohic.site/2024/05/18/spring6/#8-2%E3%80%81Resource%E6%8E%A5%E5%8F%A3 "8.2、Resource接口")8.2、Resource接口

Spring 的 Resource 接口位于 org.springframework.core.io 中。 旨在成为一个更强大的接口，用于抽象对低级资源的访问。以下显示了Resource接口定义的方法

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28|public interface Resource extends InputStreamSource {  <br>  <br>    boolean exists();  <br>  <br>    boolean isReadable();  <br>  <br>    boolean isOpen();  <br>  <br>    boolean isFile();  <br>  <br>    URL getURL() throws IOException;  <br>  <br>    URI getURI() throws IOException;  <br>  <br>    File getFile() throws IOException;  <br>  <br>    ReadableByteChannel readableChannel() throws IOException;  <br>  <br>    long contentLength() throws IOException;  <br>  <br>    long lastModified() throws IOException;  <br>  <br>    Resource createRelative(String relativePath) throws IOException;  <br>  <br>    String getFilename();  <br>  <br>    String getDescription();  <br>}|

Resource接口继承了InputStreamSource接口，提供了很多InputStreamSource所没有的方法。InputStreamSource接口，只有一个方法：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5|public interface InputStreamSource {  <br>  <br>    InputStream getInputStream() throws IOException;  <br>  <br>}|

**其中一些重要的方法：**

getInputStream(): 找到并打开资源，返回一个InputStream以从资源中读取。预计每次调用都会返回一个新的InputStream()，调用者有责任关闭每个流  
exists(): 返回一个布尔值，表明某个资源是否以物理形式存在  
isOpen: 返回一个布尔值，指示此资源是否具有开放流的句柄。如果为true，InputStream就不能够多次读取，只能够读取一次并且及时关闭以避免内存泄漏。对于所有常规资源实现，返回false，但是InputStreamResource除外。  
getDescription(): 返回资源的描述，用来输出错误的日志。这通常是完全限定的文件名或资源的实际URL。

**其他方法：**

isReadable(): 表明资源的目录读取是否通过getInputStream()进行读取。  
isFile(): 表明这个资源是否代表了一个文件系统的文件。  
getURL(): 返回一个URL句柄，如果资源不能够被解析为URL，将抛出IOException  
getURI(): 返回一个资源的URI句柄  
getFile(): 返回某个文件，如果资源不能够被解析称为绝对路径，将会抛出FileNotFoundException  
lastModified(): 资源最后一次修改的时间戳  
createRelative(): 创建此资源的相关资源  
getFilename(): 资源的文件名是什么 例如：最后一部分的文件名 myfile.txt

### [](https://blog.mohic.site/2024/05/18/spring6/#8-3%E3%80%81Resource%E7%9A%84%E5%AE%9E%E7%8E%B0%E7%B1%BB "8.3、Resource的实现类")8.3、Resource的实现类

Resource 接口是 Spring 资源访问策略的抽象，它本身并不提供任何资源访问实现，具体的资源访问由该接口的实现类完成——每个实现类代表一种资源访问策略。Resource一般包括这些实现类：UrlResource、ClassPathResource、FileSystemResource、ServletContextResource、InputStreamResource、ByteArrayResource

#### [](https://blog.mohic.site/2024/05/18/spring6/#8-3-1%E3%80%81UrlResource%E8%AE%BF%E9%97%AE%E7%BD%91%E7%BB%9C%E8%B5%84%E6%BA%90 "8.3.1、UrlResource访问网络资源")8.3.1、UrlResource访问网络资源

Resource的一个实现类，用来访问网络资源，它支持URL的绝对路径。

http:——该前缀用于访问基于HTTP协议的网络资源。

ftp:——该前缀用于访问基于FTP协议的网络资源

file: ——该前缀用于从文件系统中读取资源

**实验：访问基于HTTP协议的网络资源**

**创建一个maven子模块spring6-resources，配置Spring依赖（参考前面）**

[![image-20221207102315185](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207102315185.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207102315185.png)

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28|package com.atguigu.spring6.resources;  <br>  <br>import org.springframework.core.io.UrlResource;  <br>  <br>public class UrlResourceDemo {  <br>  <br>    public static void loadAndReadUrlResource(String path){  <br>        // 创建一个 Resource 对象  <br>        UrlResource url = null;  <br>        try {  <br>            url = new UrlResource(path);  <br>            // 获取资源名  <br>            System.out.println(url.getFilename());  <br>            System.out.println(url.getURI());  <br>            // 获取资源描述  <br>            System.out.println(url.getDescription());  <br>            //获取资源内容  <br>            System.out.println(url.getInputStream().read());  <br>        } catch (Exception e) {  <br>            throw new RuntimeException(e);  <br>        }  <br>    }  <br>      <br>    public static void main(String[] args) {  <br>        //访问网络资源  <br>        loadAndReadUrlResource("http://www.baidu.com");  <br>    }  <br>}|

**实验二：在项目根路径下创建文件，从文件系统中读取资源**

方法不变，修改调用传递路径

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7|public static void main(String[] args) {  <br>    //1 访问网络资源  <br>	//loadAndReadUrlResource("http://www.atguigu.com");  <br>      <br>    //2 访问文件系统资源  <br>    loadAndReadUrlResource("file:atguigu.txt");  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#8-3-2%E3%80%81ClassPathResource-%E8%AE%BF%E9%97%AE%E7%B1%BB%E8%B7%AF%E5%BE%84%E4%B8%8B%E8%B5%84%E6%BA%90 "8.3.2、ClassPathResource 访问类路径下资源")8.3.2、ClassPathResource 访问类路径下资源

ClassPathResource 用来访问类加载路径下的资源，相对于其他的 Resource 实现类，其主要优势是方便访问类加载路径里的资源，尤其对于 Web 应用，ClassPathResource 可自动搜索位于 classes 下的资源文件，无须使用绝对路径访问。

**实验：在类路径下创建文件atguigu.txt，使用ClassPathResource 访问**

[![image-20221207103020854](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207103020854.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207103020854.png)

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26|package com.atguigu.spring6.resources;  <br>  <br>import org.springframework.core.io.ClassPathResource;  <br>import java.io.InputStream;  <br>  <br>public class ClassPathResourceDemo {  <br>  <br>    public static void loadAndReadUrlResource(String path) throws Exception{  <br>        // 创建一个 Resource 对象  <br>        ClassPathResource resource = new ClassPathResource(path);  <br>        // 获取文件名  <br>        System.out.println("resource.getFileName = " + resource.getFilename());  <br>        // 获取文件描述  <br>        System.out.println("resource.getDescription = "+ resource.getDescription());  <br>        //获取文件内容  <br>        InputStream in = resource.getInputStream();  <br>        byte[] b = new byte[1024];  <br>        while(in.read(b)!=-1) {  <br>            System.out.println(new String(b));  <br>        }  <br>    }  <br>  <br>    public static void main(String[] args) throws Exception {  <br>        loadAndReadUrlResource("atguigu.txt");  <br>    }  <br>}|

ClassPathResource实例可使用ClassPathResource构造器显式地创建，但更多的时候它都是隐式地创建的。当执行Spring的某个方法时，该方法接受一个代表资源路径的字符串参数，当Spring识别该字符串参数中包含classpath:前缀后，系统会自动创建ClassPathResource对象。

#### [](https://blog.mohic.site/2024/05/18/spring6/#8-3-3%E3%80%81FileSystemResource-%E8%AE%BF%E9%97%AE%E6%96%87%E4%BB%B6%E7%B3%BB%E7%BB%9F%E8%B5%84%E6%BA%90 "8.3.3、FileSystemResource 访问文件系统资源")8.3.3、FileSystemResource 访问文件系统资源

Spring 提供的 FileSystemResource 类用于访问文件系统资源，使用 FileSystemResource 来访问文件系统资源并没有太大的优势，因为 Java 提供的 File 类也可用于访问文件系统资源。

**实验：使用FileSystemResource 访问文件系统资源**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29|package com.atguigu.spring6.resources;  <br>  <br>import org.springframework.core.io.FileSystemResource;  <br>  <br>import java.io.InputStream;  <br>  <br>public class FileSystemResourceDemo {  <br>  <br>    public static void loadAndReadUrlResource(String path) throws Exception{  <br>        //相对路径  <br>        FileSystemResource resource = new FileSystemResource("atguigu.txt");  <br>        //绝对路径  <br>        //FileSystemResource resource = new FileSystemResource("C:\\atguigu.txt");  <br>        // 获取文件名  <br>        System.out.println("resource.getFileName = " + resource.getFilename());  <br>        // 获取文件描述  <br>        System.out.println("resource.getDescription = "+ resource.getDescription());  <br>        //获取文件内容  <br>        InputStream in = resource.getInputStream();  <br>        byte[] b = new byte[1024];  <br>        while(in.read(b)!=-1) {  <br>            System.out.println(new String(b));  <br>        }  <br>    }  <br>  <br>    public static void main(String[] args) throws Exception {  <br>        loadAndReadUrlResource("atguigu.txt");  <br>    }  <br>}|

FileSystemResource实例可使用FileSystemResource构造器显示地创建，但更多的时候它都是隐式创建。执行Spring的某个方法时，该方法接受一个代表资源路径的字符串参数，当Spring识别该字符串参数中包含file:前缀后，系统将会自动创建FileSystemResource对象。

#### [](https://blog.mohic.site/2024/05/18/spring6/#8-3-4%E3%80%81ServletContextResource "8.3.4、ServletContextResource")8.3.4、ServletContextResource

这是ServletContext资源的Resource实现，它解释相关Web应用程序根目录中的相对路径。它始终支持流(stream)访问和URL访问，但只有在扩展Web应用程序存档且资源实际位于文件系统上时才允许java.io.File访问。无论它是在文件系统上扩展还是直接从JAR或其他地方（如数据库）访问，实际上都依赖于Servlet容器。

#### [](https://blog.mohic.site/2024/05/18/spring6/#8-3-5%E3%80%81InputStreamResource "8.3.5、InputStreamResource")8.3.5、InputStreamResource

InputStreamResource 是给定的输入流(InputStream)的Resource实现。它的使用场景在没有特定的资源实现的时候使用(感觉和@Component 的适用场景很相似)。与其他Resource实现相比，这是已打开资源的描述符。 因此，它的isOpen()方法返回true。如果需要将资源描述符保留在某处或者需要多次读取流，请不要使用它。

#### [](https://blog.mohic.site/2024/05/18/spring6/#8-3-6%E3%80%81ByteArrayResource "8.3.6、ByteArrayResource")8.3.6、ByteArrayResource

字节数组的Resource实现类。通过给定的数组创建了一个ByteArrayInputStream。它对于从任何给定的字节数组加载内容非常有用，而无需求助于单次使用的InputStreamResource。

### [](https://blog.mohic.site/2024/05/18/spring6/#8-4%E3%80%81Resource%E7%B1%BB%E5%9B%BE "8.4、Resource类图")8.4、Resource类图

上述Resource实现类与Resource顶级接口之间的关系可以用下面的UML关系模型来表示

[![image-20221206232920494](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221206232920494.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221206232920494.png)

### [](https://blog.mohic.site/2024/05/18/spring6/#8-5%E3%80%81ResourceLoader-%E6%8E%A5%E5%8F%A3 "8.5、ResourceLoader 接口")8.5、ResourceLoader 接口

#### [](https://blog.mohic.site/2024/05/18/spring6/#8-5-1%E3%80%81ResourceLoader-%E6%A6%82%E8%BF%B0 "8.5.1、ResourceLoader 概述")8.5.1、ResourceLoader 概述

Spring 提供如下两个标志性接口：

**（1）ResourceLoader ：** 该接口实现类的实例可以获得一个Resource实例。

**（2） ResourceLoaderAware ：** 该接口实现类的实例将获得一个ResourceLoader的引用。

在ResourceLoader接口里有如下方法：

（1）**Resource getResource（String location）** ： 该接口仅有这个方法，用于返回一个Resource实例。ApplicationContext实现类都实现ResourceLoader接口，因此ApplicationContext可直接获取Resource实例。

#### [](https://blog.mohic.site/2024/05/18/spring6/#8-5-2%E3%80%81%E4%BD%BF%E7%94%A8%E6%BC%94%E7%A4%BA "8.5.2、使用演示")8.5.2、使用演示

**实验一：ClassPathXmlApplicationContext获取Resource实例**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17|package com.atguigu.spring6.resouceloader;  <br>  <br>import org.springframework.context.ApplicationContext;  <br>import org.springframework.context.support.ClassPathXmlApplicationContext;  <br>import org.springframework.core.io.Resource;  <br>  <br>public class Demo1 {  <br>  <br>    public static void main(String[] args) {  <br>        ApplicationContext ctx = new ClassPathXmlApplicationContext();  <br>//        通过ApplicationContext访问资源  <br>//        ApplicationContext实例获取Resource实例时，  <br>//        默认采用与ApplicationContext相同的资源访问策略  <br>        Resource res = ctx.getResource("atguigu.txt");  <br>        System.out.println(res.getFilename());  <br>    }  <br>}|

**实验二：FileSystemApplicationContext获取Resource实例**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14|package com.atguigu.spring6.resouceloader;  <br>  <br>import org.springframework.context.ApplicationContext;  <br>import org.springframework.context.support.FileSystemXmlApplicationContext;  <br>import org.springframework.core.io.Resource;  <br>  <br>public class Demo2 {  <br>  <br>    public static void main(String[] args) {  <br>        ApplicationContext ctx = new FileSystemXmlApplicationContext();  <br>        Resource res = ctx.getResource("atguigu.txt");  <br>        System.out.println(res.getFilename());  <br>    }  <br>}|

#### [](https://blog.mohic.site/2024/05/18/spring6/#8-5-3%E3%80%81ResourceLoader-%E6%80%BB%E7%BB%93 "8.5.3、ResourceLoader 总结")8.5.3、ResourceLoader 总结

Spring将采用和ApplicationContext相同的策略来访问资源。也就是说，如果ApplicationContext是FileSystemXmlApplicationContext，res就是FileSystemResource实例；如果ApplicationContext是ClassPathXmlApplicationContext，res就是ClassPathResource实例

当Spring应用需要进行资源访问时，实际上并不需要直接使用Resource实现类，而是调用ResourceLoader实例的getResource()方法来获得资源，ReosurceLoader将会负责选择Reosurce实现类，也就是确定具体的资源访问策略，从而将应用程序和具体的资源访问策略分离开来

另外，使用ApplicationContext访问资源时，可通过不同前缀指定强制使用指定的ClassPathResource、FileSystemResource等实现类

java

|   |   |
|---|---|
|1  <br>2  <br>3|Resource res = ctx.getResource("calsspath:bean.xml");  <br>Resrouce res = ctx.getResource("file:bean.xml");  <br>Resource res = ctx.getResource("http://localhost:8080/beans.xml");|

### [](https://blog.mohic.site/2024/05/18/spring6/#8-6%E3%80%81ResourceLoaderAware-%E6%8E%A5%E5%8F%A3 "8.6、ResourceLoaderAware 接口")8.6、ResourceLoaderAware 接口

ResourceLoaderAware接口实现类的实例将获得一个ResourceLoader的引用，ResourceLoaderAware接口也提供了一个setResourceLoader()方法，该方法将由Spring容器负责调用，Spring容器会将一个ResourceLoader对象作为该方法的参数传入。

如果把实现ResourceLoaderAware接口的Bean类部署在Spring容器中，Spring容器会将自身当成ResourceLoader作为setResourceLoader()方法的参数传入。由于ApplicationContext的实现类都实现了ResourceLoader接口，Spring容器自身完全可作为ResorceLoader使用。

**实验：演示ResourceLoaderAware使用**

**第一步 创建类，实现ResourceLoaderAware接口**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22|package com.atguigu.spring6.resouceloader;  <br>  <br>import org.springframework.context.ResourceLoaderAware;  <br>import org.springframework.core.io.ResourceLoader;  <br>  <br>public class TestBean implements ResourceLoaderAware {  <br>  <br>    private ResourceLoader resourceLoader;  <br>  <br>    //实现ResourceLoaderAware接口必须实现的方法  <br>	//如果把该Bean部署在Spring容器中，该方法将会有Spring容器负责调用。  <br>	//SPring容器调用该方法时，Spring会将自身作为参数传给该方法。  <br>    public void setResourceLoader(ResourceLoader resourceLoader) {  <br>        this.resourceLoader = resourceLoader;  <br>    }  <br>  <br>    //返回ResourceLoader对象的应用  <br>    public ResourceLoader getResourceLoader(){  <br>        return this.resourceLoader;  <br>    }  <br>  <br>}|

**第二步 创建bean.xml文件，配置TestBean**

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7|<?xml version="1.0" encoding="UTF-8"?>  <br><beans xmlns="http://www.springframework.org/schema/beans"  <br>       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  <br>       xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd">  <br>  <br>    <bean id="testBean" class="com.atguigu.spring6.resouceloader.TestBean"></bean>  <br></beans>|

**第三步 测试**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22|package com.atguigu.spring6.resouceloader;  <br>  <br>import org.springframework.context.ApplicationContext;  <br>import org.springframework.context.support.ClassPathXmlApplicationContext;  <br>import org.springframework.core.io.Resource;  <br>import org.springframework.core.io.ResourceLoader;  <br>  <br>public class Demo3 {  <br>  <br>    public static void main(String[] args) {  <br>        //Spring容器会将一个ResourceLoader对象作为该方法的参数传入  <br>        ApplicationContext ctx = new ClassPathXmlApplicationContext("bean.xml");  <br>        TestBean testBean = ctx.getBean("testBean",TestBean.class);  <br>        //获取ResourceLoader对象  <br>        ResourceLoader resourceLoader = testBean.getResourceLoader();  <br>        System.out.println("Spring容器将自身注入到ResourceLoaderAware Bean 中 ？ ：" + (resourceLoader == ctx));  <br>        //加载其他资源  <br>        Resource resource = resourceLoader.getResource("atguigu.txt");  <br>        System.out.println(resource.getFilename());  <br>        System.out.println(resource.getDescription());  <br>    }  <br>}|

### [](https://blog.mohic.site/2024/05/18/spring6/#8-7%E3%80%81%E4%BD%BF%E7%94%A8Resource-%E4%BD%9C%E4%B8%BA%E5%B1%9E%E6%80%A7 "8.7、使用Resource 作为属性")8.7、使用Resource 作为属性

前面介绍了 Spring 提供的资源访问策略，但这些依赖访问策略要么需要使用 Resource 实现类，要么需要使用 ApplicationContext 来获取资源。实际上，当应用程序中的 Bean 实例需要访问资源时，Spring 有更好的解决方法：直接利用依赖注入。从这个意义上来看，Spring 框架不仅充分利用了策略模式来简化资源访问，而且还将策略模式和 IoC 进行充分地结合，最大程度地简化了 Spring 资源访问。

归纳起来，**如果 Bean 实例需要访问资源，有如下两种解决方案：**

- **代码中获取 Resource 实例。**
- **使用依赖注入。**

对于第一种方式，当程序获取 Resource 实例时，总需要提供 Resource 所在的位置，不管通过 FileSystemResource 创建实例，还是通过 ClassPathResource 创建实例，或者通过 ApplicationContext 的 getResource() 方法获取实例，都需要提供资源位置。这意味着：资源所在的物理位置将被耦合到代码中，如果资源位置发生改变，则必须改写程序。因此，通常建议采用第二种方法，让 Spring 为 Bean 实例**依赖注入**资源。

**实验：让Spring为Bean实例依赖注入资源**

**第一步 创建依赖注入类，定义属性和方法**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20|package com.atguigu.spring6.resouceloader;  <br>  <br>import org.springframework.core.io.Resource;  <br>  <br>public class ResourceBean {  <br>      <br>    private Resource res;  <br>      <br>    public void setRes(Resource res) {  <br>        this.res = res;  <br>    }  <br>    public Resource getRes() {  <br>        return res;  <br>    }  <br>      <br>    public void parse(){  <br>        System.out.println(res.getFilename());  <br>        System.out.println(res.getDescription());  <br>    }  <br>}|

**第二步 创建spring配置文件，配置依赖注入**

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11|<?xml version="1.0" encoding="UTF-8"?>  <br><beans xmlns="http://www.springframework.org/schema/beans"  <br>       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  <br>       xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd">  <br>  <br>    <bean id="resourceBean" class="com.atguigu.spring6.resouceloader.ResourceBean" >  <br>      <!-- 可以使用file:、http:、ftp:等前缀强制Spring采用对应的资源访问策略 -->  <br>      <!-- 如果不采用任何前缀，则Spring将采用与该ApplicationContext相同的资源访问策略来访问资源 -->  <br>        <property name="res" value="classpath:atguigu.txt"/>  <br>    </bean>  <br></beans>|

**第三步 测试**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14|package com.atguigu.spring6.resouceloader;  <br>  <br>import org.springframework.context.ApplicationContext;  <br>import org.springframework.context.support.ClassPathXmlApplicationContext;  <br>  <br>public class Demo4 {  <br>  <br>    public static void main(String[] args) {  <br>        ApplicationContext ctx =  <br>                new ClassPathXmlApplicationContext("bean.xml");  <br>        ResourceBean resourceBean = ctx.getBean("resourceBean",ResourceBean.class);  <br>        resourceBean.parse();  <br>    }  <br>}|

### [](https://blog.mohic.site/2024/05/18/spring6/#8-8%E3%80%81%E5%BA%94%E7%94%A8%E7%A8%8B%E5%BA%8F%E4%B8%8A%E4%B8%8B%E6%96%87%E5%92%8C%E8%B5%84%E6%BA%90%E8%B7%AF%E5%BE%84 "8.8、应用程序上下文和资源路径")8.8、应用程序上下文和资源路径

#### [](https://blog.mohic.site/2024/05/18/spring6/#8-8-1%E3%80%81%E6%A6%82%E8%BF%B0 "8.8.1、概述")8.8.1、概述

不管以怎样的方式创建ApplicationContext实例，都需要为ApplicationContext指定配置文件，Spring允许使用一份或多分XML配置文件。当程序创建ApplicationContext实例时，通常也是以Resource的方式来访问配置文件的，所以ApplicationContext完全支持ClassPathResource、FileSystemResource、ServletContextResource等资源访问方式。

**ApplicationContext确定资源访问策略通常有两种方法：**

**（1）使用ApplicationContext实现类指定访问策略。**

**（2）使用前缀指定访问策略。**

#### [](https://blog.mohic.site/2024/05/18/spring6/#8-8-2%E3%80%81ApplicationContext%E5%AE%9E%E7%8E%B0%E7%B1%BB%E6%8C%87%E5%AE%9A%E8%AE%BF%E9%97%AE%E7%AD%96%E7%95%A5 "8.8.2、ApplicationContext实现类指定访问策略")8.8.2、ApplicationContext实现类指定访问策略

创建ApplicationContext对象时，通常可以使用如下实现类：

（1） ClassPathXMLApplicationContext : 对应使用ClassPathResource进行资源访问。

（2）FileSystemXmlApplicationContext ： 对应使用FileSystemResource进行资源访问。

（3）XmlWebApplicationContext ： 对应使用ServletContextResource进行资源访问。

当使用ApplicationContext的不同实现类时，就意味着Spring使用响应的资源访问策略。

效果前面已经演示

#### [](https://blog.mohic.site/2024/05/18/spring6/#8-8-3%E3%80%81%E4%BD%BF%E7%94%A8%E5%89%8D%E7%BC%80%E6%8C%87%E5%AE%9A%E8%AE%BF%E9%97%AE%E7%AD%96%E7%95%A5 "8.8.3、使用前缀指定访问策略")8.8.3、使用前缀指定访问策略

**实验一：classpath前缀使用**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22|package com.atguigu.spring6.context;  <br>  <br>import org.springframework.context.ApplicationContext;  <br>import org.springframework.context.support.FileSystemXmlApplicationContext;  <br>import org.springframework.core.io.Resource;  <br>  <br>public class Demo1 {  <br>  <br>    public static void main(String[] args) {  <br>        /*  <br>         * 通过搜索文件系统路径下的xml文件创建ApplicationContext，  <br>         * 但通过指定classpath:前缀强制搜索类加载路径  <br>         * classpath:bean.xml  <br>         * */  <br>        ApplicationContext ctx =  <br>                new ClassPathXmlApplicationContext("classpath:bean.xml");  <br>        System.out.println(ctx);  <br>        Resource resource = ctx.getResource("atguigu.txt");  <br>        System.out.println(resource.getFilename());  <br>        System.out.println(resource.getDescription());  <br>    }  <br>}|

**实验二：classpath通配符使用**

classpath * :前缀提供了加载多个XML配置文件的能力，当使用classpath*:前缀来指定XML配置文件时，系统将搜索类加载路径，找到所有与文件名匹配的文件，分别加载文件中的配置定义，最后合并成一个ApplicationContext。

java

|   |   |
|---|---|
|1  <br>2|ApplicationContext ctx = new ClassPathXmlApplicationContext("classpath*:bean.xml");  <br>System.out.println(ctx);|

当使用classpath * :前缀时，Spring将会搜索类加载路径下所有满足该规则的配置文件。

如果不是采用classpath * :前缀，而是改为使用classpath:前缀，Spring则只加载第一个符合条件的XML文件

**注意 ：**

classpath * : 前缀仅对ApplicationContext有效。实际情况是，创建ApplicationContext时，分别访问多个配置文件(通过ClassLoader的getResource方法实现)。因此，classpath * :前缀不可用于Resource。

**使用三：通配符其他使用**

一次性加载多个配置文件的方式：指定配置文件时使用通配符

java

|   |   |
|---|---|
|1|ApplicationContext ctx = new ClassPathXmlApplicationContext("classpath:bean*.xml");|

Spring允许将classpath*:前缀和通配符结合使用：

java

|   |   |
|---|---|
|1|ApplicationContext ctx = new ClassPathXmlApplicationContext("classpath*:bean*.xml");|

## [](https://blog.mohic.site/2024/05/18/spring6/#9%E3%80%81%E5%9B%BD%E9%99%85%E5%8C%96%EF%BC%9Ai18n "9、国际化：i18n")9、国际化：i18n

[![image-20221218154728062](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221218154728062.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221218154728062.png)

### [](https://blog.mohic.site/2024/05/18/spring6/#9-1%E3%80%81i18n%E6%A6%82%E8%BF%B0 "9.1、i18n概述")9.1、i18n概述

国际化也称作i18n，其来源是英文单词 internationalization的首末字符i和n，18为中间的字符数。由于软件发行可能面向多个国家，对于不同国家的用户，软件显示不同语言的过程就是国际化。通常来讲，软件中的国际化是通过配置文件来实现的，假设要支撑两种语言，那么就需要两个版本的配置文件。

### [](https://blog.mohic.site/2024/05/18/spring6/#9-2%E3%80%81Java%E5%9B%BD%E9%99%85%E5%8C%96 "9.2、Java国际化")9.2、Java国际化

（1）Java自身是支持国际化的，java.util.Locale用于指定当前用户所属的语言环境等信息，java.util.ResourceBundle用于查找绑定对应的资源文件。Locale包含了language信息和country信息，Locale创建默认locale对象时使用的静态方法：

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8|/**  <br> * This method must be called only for creating the Locale.*  <br> * constants due to making shortcuts.  <br> */  <br>private static Locale createConstant(String lang, String country) {  <br>    BaseLocale base = BaseLocale.createInstance(lang, country);  <br>    return getInstance(base, null);  <br>}|

（2）配置文件命名规则：  
**basename_language_country.properties**  
必须遵循以上的命名规则，java才会识别。其中，basename是必须的，语言和国家是可选的。这里存在一个优先级概念，如果同时提供了messages.properties和messages_zh_CN.propertes两个配置文件，如果提供的locale符合en_CN，那么优先查找messages_en_CN.propertes配置文件，如果没查找到，再查找messages.properties配置文件。最后，提示下，所有的配置文件必须放在classpath中，一般放在resources目录下

**（3）实验：演示Java国际化**

**第一步 创建子模块spring6-i18n，引入spring依赖**

[![image-20221207122500801](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207122500801.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207122500801.png)

**第二步 在resource目录下创建两个配置文件：messages_zh_CN.propertes和messages_en_GB.propertes**

[![image-20221207124839565](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207124839565.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207124839565.png)

**第三步 测试**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16|package com.atguigu.spring6.javai18n;  <br>  <br>import java.nio.charset.StandardCharsets;  <br>import java.util.Locale;  <br>import java.util.ResourceBundle;  <br>  <br>public class Demo1 {  <br>  <br>    public static void main(String[] args) {  <br>        System.out.println(ResourceBundle.getBundle("messages",  <br>                new Locale("en","GB")).getString("test"));  <br>  <br>        System.out.println(ResourceBundle.getBundle("messages",  <br>                new Locale("zh","CN")).getString("test"));  <br>    }  <br>}|

### [](https://blog.mohic.site/2024/05/18/spring6/#9-3%E3%80%81Spring6%E5%9B%BD%E9%99%85%E5%8C%96 "9.3、Spring6国际化")9.3、Spring6国际化

#### [](https://blog.mohic.site/2024/05/18/spring6/#9-3-1%E3%80%81MessageSource%E6%8E%A5%E5%8F%A3 "9.3.1、MessageSource接口")9.3.1、MessageSource接口

spring中国际化是通过MessageSource这个接口来支持的

**常见实现类**

**ResourceBundleMessageSource**

这个是基于Java的ResourceBundle基础类实现，允许仅通过资源名加载国际化资源

**ReloadableResourceBundleMessageSource**

这个功能和第一个类的功能类似，多了定时刷新功能，允许在不重启系统的情况下，更新资源的信息

**StaticMessageSource**

它允许通过编程的方式提供国际化信息，一会我们可以通过这个来实现db中存储国际化信息的功能。

#### [](https://blog.mohic.site/2024/05/18/spring6/#9-3-2%E3%80%81%E4%BD%BF%E7%94%A8Spring6%E5%9B%BD%E9%99%85%E5%8C%96 "9.3.2、使用Spring6国际化")9.3.2、使用Spring6国际化

**第一步 创建资源文件**

**国际化文件命名格式：基本名称 _ 语言 _ 国家.properties**

**{0},{1}这样内容，就是动态参数**

[![image-20221207140024056](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207140024056.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207140024056.png)

**（1）创建atguigu_en_US.properties**

properties

|   |   |
|---|---|
|1|www.atguigu.com=welcome {0},时间:{1}|

**（2）创建atguigu_zh_CN.properties**

properties

|   |   |
|---|---|
|1|www.atguigu.com=欢迎 {0},时间:{1}|

**第二步 创建spring配置文件，配置MessageSource**

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17|<?xml version="1.0" encoding="UTF-8"?>  <br><beans xmlns="http://www.springframework.org/schema/beans"  <br>       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  <br>       xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd">  <br>  <br>    <bean id="messageSource"  <br>          class="org.springframework.context.support.ResourceBundleMessageSource">  <br>        <property name="basenames">  <br>            <list>  <br>                <value>atguigu</value>  <br>            </list>  <br>        </property>  <br>        <property name="defaultEncoding">  <br>            <value>utf-8</value>  <br>        </property>  <br>    </bean>  <br></beans>|

**第三步 创建测试类**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23|package com.atguigu.spring6.javai18n;  <br>  <br>import org.springframework.context.ApplicationContext;  <br>import org.springframework.context.annotation.AnnotationConfigApplicationContext;  <br>import org.springframework.context.support.ClassPathXmlApplicationContext;  <br>import java.util.Date;  <br>import java.util.Locale;  <br>  <br>public class Demo2 {  <br>  <br>    public static void main(String[] args) {  <br>          <br>        ApplicationContext context = new ClassPathXmlApplicationContext("beans.xml");  <br>          <br>        //传递动态参数，使用数组形式对应{0} {1}顺序  <br>        Object[] objs = new Object[]{"atguigu",new Date().toString()};  <br>  <br>        //www.atguigu.com为资源文件的key值,  <br>        //objs为资源文件value值所需要的参数,Local.CHINA为国际化为语言  <br>        String str=context.getMessage("www.atguigu.com", objs, Locale.CHINA);  <br>        System.out.println(str);  <br>    }  <br>}|

## [](https://blog.mohic.site/2024/05/18/spring6/#10%E3%80%81%E6%95%B0%E6%8D%AE%E6%A0%A1%E9%AA%8C%EF%BC%9AValidation "10、数据校验：Validation")10、数据校验：Validation

[![image-20221218154808754](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221218154808754.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221218154808754.png)

### [](https://blog.mohic.site/2024/05/18/spring6/#10-1%E3%80%81Spring-Validation%E6%A6%82%E8%BF%B0 "10.1、Spring Validation概述")10.1、Spring Validation概述

[![image-20221206220207266](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221206220207266.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221206220207266.png)

在开发中，我们经常遇到参数校验的需求，比如用户注册的时候，要校验用户名不能为空、用户名长度不超过20个字符、手机号是合法的手机号格式等等。如果使用普通方式，我们会把校验的代码和真正的业务处理逻辑耦合在一起，而且如果未来要新增一种校验逻辑也需要在修改多个地方。而spring validation允许通过注解的方式来定义对象校验规则，把校验和业务逻辑分离开，让代码编写更加方便。Spring Validation其实就是对Hibernate Validator进一步的封装，方便在Spring中使用。

在Spring中有多种校验的方式

**第一种是通过实现org.springframework.validation.Validator接口，然后在代码中调用这个类**

**第二种是按照Bean Validation方式来进行校验，即通过注解的方式。**

**第三种是基于方法实现校验**

**除此之外，还可以实现自定义校验**

### [](https://blog.mohic.site/2024/05/18/spring6/#10-2%E3%80%81%E5%AE%9E%E9%AA%8C%E4%B8%80%EF%BC%9A%E9%80%9A%E8%BF%87Validator%E6%8E%A5%E5%8F%A3%E5%AE%9E%E7%8E%B0 "10.2、实验一：通过Validator接口实现")10.2、实验一：通过Validator接口实现

**第一步 创建子模块 spring6-validator**

[![image-20221206221002615](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221206221002615.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221206221002615.png)

**第二步 引入相关依赖**

xml

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13|<dependencies>  <br>    <dependency>  <br>        <groupId>org.hibernate.validator</groupId>  <br>        <artifactId>hibernate-validator</artifactId>  <br>        <version>7.0.5.Final</version>  <br>    </dependency>  <br>  <br>    <dependency>  <br>        <groupId>org.glassfish</groupId>  <br>        <artifactId>jakarta.el</artifactId>  <br>        <version>4.0.1</version>  <br>    </dependency>  <br></dependencies>|

**第三步 创建实体类，定义属性和方法**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19|package com.atguigu.spring6.validation.method1;  <br>  <br>public class Person {  <br>    private String name;  <br>    private int age;  <br>  <br>    public String getName() {  <br>        return name;  <br>    }  <br>    public void setName(String name) {  <br>        this.name = name;  <br>    }  <br>    public int getAge() {  <br>        return age;  <br>    }  <br>    public void setAge(int age) {  <br>        this.age = age;  <br>    }  <br>}|

**第四步 创建类实现Validator接口，实现接口方法指定校验规则**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24|package com.atguigu.spring6.validation.method1;  <br>  <br>import org.springframework.validation.Errors;  <br>import org.springframework.validation.ValidationUtils;  <br>import org.springframework.validation.Validator;  <br>  <br>public class PersonValidator implements Validator {  <br>  <br>    @Override  <br>    public boolean supports(Class<?> clazz) {  <br>        return Person.class.equals(clazz);  <br>    }  <br>  <br>    @Override  <br>    public void validate(Object object, Errors errors) {  <br>        ValidationUtils.rejectIfEmpty(errors, "name", "name.empty");  <br>        Person p = (Person) object;  <br>        if (p.getAge() < 0) {  <br>            errors.rejectValue("age", "error value < 0");  <br>        } else if (p.getAge() > 110) {  <br>            errors.rejectValue("age", "error value too old");  <br>        }  <br>    }  <br>}|

上面定义的类，其实就是实现接口中对应的方法，

supports方法用来表示此校验用在哪个类型上，

validate是设置校验逻辑的地点，其中ValidationUtils，是Spring封装的校验工具类，帮助快速实现校验。

**第五步 使用上述Validator进行测试**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27|package com.atguigu.spring6.validation.method1;  <br>  <br>import org.springframework.validation.BindingResult;  <br>import org.springframework.validation.DataBinder;  <br>  <br>public class TestMethod1 {  <br>  <br>    public static void main(String[] args) {  <br>        //创建person对象  <br>        Person person = new Person();  <br>        person.setName("lucy");  <br>        person.setAge(-1);  <br>          <br>        // 创建Person对应的DataBinder  <br>        DataBinder binder = new DataBinder(person);  <br>  <br>        // 设置校验  <br>        binder.setValidator(new PersonValidator());  <br>  <br>        // 由于Person对象中的属性为空，所以校验不通过  <br>        binder.validate();  <br>  <br>        //输出结果  <br>        BindingResult results = binder.getBindingResult();  <br>        System.out.println(results.getAllErrors());  <br>    }  <br>}|

### [](https://blog.mohic.site/2024/05/18/spring6/#10-3%E3%80%81%E5%AE%9E%E9%AA%8C%E4%BA%8C%EF%BC%9ABean-Validation%E6%B3%A8%E8%A7%A3%E5%AE%9E%E7%8E%B0 "10.3、实验二：Bean Validation注解实现")10.3、实验二：Bean Validation注解实现

使用Bean Validation校验方式，就是如何将Bean Validation需要使用的javax.validation.ValidatorFactory 和javax.validation.Validator注入到容器中。spring默认有一个实现类LocalValidatorFactoryBean，它实现了上面Bean Validation中的接口，并且也实现了org.springframework.validation.Validator接口。

**第一步 创建配置类，配置LocalValidatorFactoryBean**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9|@Configuration  <br>@ComponentScan("com.atguigu.spring6.validation.method2")  <br>public class ValidationConfig {  <br>  <br>    @Bean  <br>    public LocalValidatorFactoryBean validator() {  <br>        return new LocalValidatorFactoryBean();  <br>    }  <br>}|

**第二步 创建实体类，使用注解定义校验规则**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28|package com.atguigu.spring6.validation.method2;  <br>  <br>import jakarta.validation.constraints.Max;  <br>import jakarta.validation.constraints.Min;  <br>import jakarta.validation.constraints.NotNull;  <br>  <br>public class User {  <br>  <br>    @NotNull  <br>    private String name;  <br>  <br>    @Min(0)  <br>    @Max(120)  <br>    private int age;  <br>  <br>    public String getName() {  <br>        return name;  <br>    }  <br>    public void setName(String name) {  <br>        this.name = name;  <br>    }  <br>    public int getAge() {  <br>        return age;  <br>    }  <br>    public void setAge(int age) {  <br>        this.age = age;  <br>    }  <br>}|

**常用注解说明**  
@NotNull 限制必须不为null  
@NotEmpty 只作用于字符串类型，字符串不为空，并且长度不为0  
@NotBlank 只作用于字符串类型，字符串不为空，并且trim()后不为空串  
@DecimalMax(value) 限制必须为一个不大于指定值的数字  
@DecimalMin(value) 限制必须为一个不小于指定值的数字  
@Max(value) 限制必须为一个不大于指定值的数字  
@Min(value) 限制必须为一个不小于指定值的数字  
@Pattern(value) 限制必须符合指定的正则表达式  
@Size(max,min) 限制字符长度必须在min到max之间  
@Email 验证注解的元素值是Email，也可以通过正则表达式和flag指定自定义的email格式

**第三步 使用两种不同的校验器实现**

**（1）使用jakarta.validation.Validator校验**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20|package com.atguigu.spring6.validation.method2;  <br>  <br>import jakarta.validation.ConstraintViolation;  <br>import jakarta.validation.Validator;  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.stereotype.Service;  <br>import java.util.Set;  <br>  <br>@Service  <br>public class MyService1 {  <br>  <br>    @Autowired  <br>    private Validator validator;  <br>  <br>    public  boolean validator(User user){  <br>        Set<ConstraintViolation<User>> sets =  validator.validate(user);  <br>        return sets.isEmpty();  <br>    }  <br>  <br>}|

**（2）使用org.springframework.validation.Validator校验**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19|package com.atguigu.spring6.validation.method2;  <br>  <br>import org.springframework.beans.factory.annotation.Autowired;  <br>import org.springframework.stereotype.Service;  <br>import org.springframework.validation.BindException;  <br>import org.springframework.validation.Validator;  <br>  <br>@Service  <br>public class MyService2 {  <br>  <br>    @Autowired  <br>    private Validator validator;  <br>  <br>    public boolean validaPersonByValidator(User user) {  <br>        BindException bindException = new BindException(user, user.getName());  <br>        validator.validate(user, bindException);  <br>        return bindException.hasErrors();  <br>    }  <br>}|

**第四步 测试**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30|package com.atguigu.spring6.validation.method2;  <br>  <br>import org.junit.jupiter.api.Test;  <br>import org.springframework.context.ApplicationContext;  <br>import org.springframework.context.annotation.AnnotationConfigApplicationContext;  <br>  <br>public class TestMethod2 {  <br>  <br>    @Test  <br>    public void testMyService1() {  <br>        ApplicationContext context = new AnnotationConfigApplicationContext(ValidationConfig.class);  <br>        MyService1 myService = context.getBean(MyService1.class);  <br>        User user = new User();  <br>        user.setAge(-1);  <br>        boolean validator = myService.validator(user);  <br>        System.out.println(validator);  <br>    }  <br>  <br>    @Test  <br>    public void testMyService2() {  <br>        ApplicationContext context = new AnnotationConfigApplicationContext(ValidationConfig.class);  <br>        MyService2 myService = context.getBean(MyService2.class);  <br>        User user = new User();  <br>        user.setName("lucy");  <br>        user.setAge(130);  <br>        user.setAge(-1);  <br>        boolean validator = myService.validaPersonByValidator(user);  <br>        System.out.println(validator);  <br>    }  <br>}|

### [](https://blog.mohic.site/2024/05/18/spring6/#10-4%E3%80%81%E5%AE%9E%E9%AA%8C%E4%B8%89%EF%BC%9A%E5%9F%BA%E4%BA%8E%E6%96%B9%E6%B3%95%E5%AE%9E%E7%8E%B0%E6%A0%A1%E9%AA%8C "10.4、实验三：基于方法实现校验")10.4、实验三：基于方法实现校验

**第一步 创建配置类，配置MethodValidationPostProcessor**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17|package com.atguigu.spring6.validation.method3;  <br>  <br>import org.springframework.context.annotation.Bean;  <br>import org.springframework.context.annotation.ComponentScan;  <br>import org.springframework.context.annotation.Configuration;  <br>import org.springframework.validation.beanvalidation.LocalValidatorFactoryBean;  <br>import org.springframework.validation.beanvalidation.MethodValidationPostProcessor;  <br>  <br>@Configuration  <br>@ComponentScan("com.atguigu.spring6.validation.method3")  <br>public class ValidationConfig {  <br>  <br>    @Bean  <br>    public MethodValidationPostProcessor validationPostProcessor() {  <br>        return new MethodValidationPostProcessor();  <br>    }  <br>}|

**第二步 创建实体类，使用注解设置校验规则**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28  <br>29  <br>30  <br>31  <br>32  <br>33  <br>34  <br>35  <br>36|package com.atguigu.spring6.validation.method3;  <br>  <br>import jakarta.validation.constraints.*;  <br>  <br>public class User {  <br>  <br>    @NotNull  <br>    private String name;  <br>  <br>    @Min(0)  <br>    @Max(120)  <br>    private int age;  <br>  <br>    @Pattern(regexp = "^1(3\|4\|5\|7\|8)\\d{9}$",message = "手机号码格式错误")  <br>    @NotBlank(message = "手机号码不能为空")  <br>    private String phone;  <br>  <br>    public String getName() {  <br>        return name;  <br>    }  <br>    public void setName(String name) {  <br>        this.name = name;  <br>    }  <br>    public int getAge() {  <br>        return age;  <br>    }  <br>    public void setAge(int age) {  <br>        this.age = age;  <br>    }  <br>    public String getPhone() {  <br>        return phone;  <br>    }  <br>    public void setPhone(String phone) {  <br>        this.phone = phone;  <br>    }  <br>}|

**第三步 定义Service类，通过注解操作对象**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16|package com.atguigu.spring6.validation.method3;  <br>  <br>import jakarta.validation.Valid;  <br>import jakarta.validation.constraints.NotNull;  <br>import org.springframework.stereotype.Service;  <br>import org.springframework.validation.annotation.Validated;  <br>  <br>@Service  <br>@Validated  <br>public class MyService {  <br>      <br>    public String testParams(@NotNull @Valid User user) {  <br>        return user.toString();  <br>    }  <br>  <br>}|

**第四步 测试**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17|package com.atguigu.spring6.validation.method3;  <br>  <br>import org.junit.jupiter.api.Test;  <br>import org.springframework.context.ApplicationContext;  <br>import org.springframework.context.annotation.AnnotationConfigApplicationContext;  <br>  <br>public class TestMethod3 {  <br>  <br>    @Test  <br>    public void testMyService1() {  <br>        ApplicationContext context = new AnnotationConfigApplicationContext(ValidationConfig.class);  <br>        MyService myService = context.getBean(MyService.class);  <br>        User user = new User();  <br>        user.setAge(-1);  <br>        myService.testParams(user);  <br>    }  <br>}|

### [](https://blog.mohic.site/2024/05/18/spring6/#10-5%E3%80%81%E5%AE%9E%E9%AA%8C%E5%9B%9B%EF%BC%9A%E5%AE%9E%E7%8E%B0%E8%87%AA%E5%AE%9A%E4%B9%89%E6%A0%A1%E9%AA%8C "10.5、实验四：实现自定义校验")10.5、实验四：实现自定义校验

**第一步 自定义校验注解**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27  <br>28|package com.atguigu.spring6.validation.method4;  <br>  <br>import jakarta.validation.Constraint;  <br>import jakarta.validation.Payload;  <br>import java.lang.annotation.*;  <br>  <br>@Target({ElementType.METHOD, ElementType.FIELD, ElementType.ANNOTATION_TYPE, ElementType.CONSTRUCTOR, ElementType.PARAMETER})  <br>@Retention(RetentionPolicy.RUNTIME)  <br>@Documented  <br>@Constraint(validatedBy = {CannotBlankValidator.class})  <br>public @interface CannotBlank {  <br>    //默认错误消息  <br>    String message() default "不能包含空格";  <br>  <br>    //分组  <br>    Class<?>[] groups() default {};  <br>  <br>    //负载  <br>    Class<? extends Payload>[] payload() default {};  <br>  <br>    //指定多个时使用  <br>    @Target({ElementType.METHOD, ElementType.FIELD, ElementType.ANNOTATION_TYPE, ElementType.CONSTRUCTOR, ElementType.PARAMETER, ElementType.TYPE_USE})  <br>    @Retention(RetentionPolicy.RUNTIME)  <br>    @Documented  <br>    @interface List {  <br>        CannotBlank[] value();  <br>    }  <br>}|

**第二步 编写真正的校验类**

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6  <br>7  <br>8  <br>9  <br>10  <br>11  <br>12  <br>13  <br>14  <br>15  <br>16  <br>17  <br>18  <br>19  <br>20  <br>21  <br>22  <br>23  <br>24  <br>25  <br>26  <br>27|package com.atguigu.spring6.validation.method4;  <br>  <br>import jakarta.validation.ConstraintValidator;  <br>import jakarta.validation.ConstraintValidatorContext;  <br>  <br>public class CannotBlankValidator implements ConstraintValidator<CannotBlank, String> {  <br>  <br>        @Override  <br>        public void initialize(CannotBlank constraintAnnotation) {  <br>        }  <br>  <br>        @Override  <br>        public boolean isValid(String value, ConstraintValidatorContext context) {  <br>                //null时不进行校验  <br>                if (value != null && value.contains(" ")) {  <br>                        //获取默认提示信息  <br>                        String defaultConstraintMessageTemplate = context.getDefaultConstraintMessageTemplate();  <br>                        System.out.println("default message :" + defaultConstraintMessageTemplate);  <br>                        //禁用默认提示信息  <br>                        context.disableDefaultConstraintViolation();  <br>                        //设置提示语  <br>                        context.buildConstraintViolationWithTemplate("can not contains blank").addConstraintViolation();  <br>                        return false;  <br>                }  <br>                return true;  <br>        }  <br>}|

## [](https://blog.mohic.site/2024/05/18/spring6/#11%E3%80%81%E6%8F%90%E5%89%8D%E7%BC%96%E8%AF%91%EF%BC%9AAOT "11、提前编译：AOT")11、提前编译：AOT

[![image-20221218154841001](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221218154841001.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221218154841001.png)

### [](https://blog.mohic.site/2024/05/18/spring6/#11-1%E3%80%81AOT%E6%A6%82%E8%BF%B0 "11.1、AOT概述")11.1、AOT概述

#### [](https://blog.mohic.site/2024/05/18/spring6/#11-1-1%E3%80%81JIT%E4%B8%8EAOT%E7%9A%84%E5%8C%BA%E5%88%AB "11.1.1、JIT与AOT的区别")11.1.1、JIT与AOT的区别

JIT和AOT 这个名词是指两种不同的编译方式，这两种编译方式的主要区别在于是否在“运行时”进行编译

**（1）JIT， Just-in-time,动态(即时)编译，边运行边编译；**

在程序运行时，根据算法计算出热点代码，然后进行 JIT 实时编译，这种方式吞吐量高，有运行时性能加成，可以跑得更快，并可以做到动态生成代码等，但是相对启动速度较慢，并需要一定时间和调用频率才能触发 JIT 的分层机制。JIT 缺点就是编译需要占用运行时资源，会导致进程卡顿。

**（2）AOT，Ahead Of Time，指运行前编译，预先编译。**

AOT 编译能直接将源代码转化为机器码，内存占用低，启动速度快，可以无需 runtime 运行，直接将 runtime 静态链接至最终的程序中，但是无运行时性能加成，不能根据程序运行情况做进一步的优化，AOT 缺点就是在程序运行前编译会使程序安装的时间增加。

**简单来讲：**JIT即时编译指的是在程序的运行过程中，将字节码转换为可在硬件上直接运行的机器码，并部署至托管环境中的过程。而 AOT 编译指的则是，在程序运行之前，便将字节码转换为机器码的过程。

plaintext

|   |   |
|---|---|
|1|.java -> .class -> (使用jaotc编译工具) -> .so（程序函数库,即编译好的可以供其他程序使用的代码和数据）|

[![image-20221207113544080](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207113544080.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207113544080.png)

**（3）AOT的优点**

**简单来讲，**Java 虚拟机加载已经预编译成二进制库，可以直接执行。不必等待及时编译器的预热，减少 Java 应用给人带来“第一次运行慢” 的不良体验。

在程序运行前编译，可以避免在运行时的编译性能消耗和内存消耗  
可以在程序运行初期就达到最高性能，程序启动速度快  
运行产物只有机器码，打包体积小

**AOT的缺点**

由于是静态提前编译，不能根据硬件情况或程序运行情况择优选择机器指令序列，理论峰值性能不如JIT  
没有动态能力，同一份产物不能跨平台运行

第一种即时编译 (JIT) 是默认模式，Java Hotspot 虚拟机使用它在运行时将字节码转换为机器码。后者提前编译 (AOT)由新颖的 GraalVM 编译器支持，并允许在构建时将字节码直接静态编译为机器码。

现在正处于云原生，降本增效的时代，Java 相比于 Go、Rust 等其他编程语言非常大的弊端就是启动编译和启动进程非常慢，这对于根据实时计算资源，弹性扩缩容的云原生技术相冲突，Spring6 借助 AOT 技术在运行时内存占用低，启动速度快，逐渐的来满足 Java 在云原生时代的需求，对于大规模使用 Java 应用的商业公司可以考虑尽早调研使用 JDK17，通过云原生技术为公司实现降本增效。

#### [](https://blog.mohic.site/2024/05/18/spring6/#11-1-2%E3%80%81Graalvm "11.1.2、Graalvm")11.1.2、Graalvm

Spring6 支持的 AOT 技术，这个 GraalVM 就是底层的支持，Spring 也对 GraalVM 本机映像提供了一流的支持。GraalVM 是一种高性能 JDK，旨在加速用 Java 和其他 JVM 语言编写的应用程序的执行，同时还为 JavaScript、Python 和许多其他流行语言提供运行时。 GraalVM 提供两种运行 Java 应用程序的方法：在 HotSpot JVM 上使用 Graal 即时 (JIT) 编译器或作为提前 (AOT) 编译的本机可执行文件。 GraalVM 的多语言能力使得在单个应用程序中混合多种编程语言成为可能，同时消除了外语调用成本。GraalVM 向 HotSpot Java 虚拟机添加了一个用 Java 编写的高级即时 (JIT) 优化编译器。

GraalVM 具有以下特性：

（1）一种高级优化编译器，它生成更快、更精简的代码，需要更少的计算资源

（2）AOT 本机图像编译提前将 Java 应用程序编译为本机二进制文件，立即启动，无需预热即可实现最高性能

（3）Polyglot 编程在单个应用程序中利用流行语言的最佳功能和库，无需额外开销

（4）高级工具在 Java 和多种语言中调试、监视、分析和优化资源消耗

总的来说对云原生的要求不算高短期内可以继续使用 2.7.X 的版本和 JDK8，不过 Spring 官方已经对 Spring6 进行了正式版发布。

#### [](https://blog.mohic.site/2024/05/18/spring6/#11-1-3%E3%80%81Native-Image "11.1.3、Native Image")11.1.3、Native Image

目前业界除了这种在JVM中进行AOT的方案，还有另外一种实现Java AOT的思路，那就是直接摒弃JVM，和C/C++一样通过编译器直接将代码编译成机器代码，然后运行。这无疑是一种直接颠覆Java语言设计的思路，那就是GraalVM Native Image。它通过C语言实现了一个超微缩的运行时组件 —— Substrate VM，基本实现了JVM的各种特性，但足够轻量、可以被轻松内嵌，这就让Java语言和工程摆脱JVM的限制，能够真正意义上实现和C/C++一样的AOT编译。这一方案在经过长时间的优化和积累后，已经拥有非常不错的效果，基本上成为Oracle官方首推的Java AOT解决方案。  
Native Image 是一项创新技术，可将 Java 代码编译成独立的本机可执行文件或本机共享库。在构建本机可执行文件期间处理的 Java 字节码包括所有应用程序类、依赖项、第三方依赖库和任何所需的 JDK 类。生成的自包含本机可执行文件特定于不需要 JVM 的每个单独的操作系统和机器体系结构。

### [](https://blog.mohic.site/2024/05/18/spring6/#11-2%E3%80%81%E6%BC%94%E7%A4%BANative-Image%E6%9E%84%E5%BB%BA%E8%BF%87%E7%A8%8B "11.2、演示Native Image构建过程")11.2、演示Native Image构建过程

#### [](https://blog.mohic.site/2024/05/18/spring6/#11-2-1%E3%80%81GraalVM%E5%AE%89%E8%A3%85 "11.2.1、GraalVM安装")11.2.1、GraalVM安装

##### [](https://blog.mohic.site/2024/05/18/spring6/#%EF%BC%881%EF%BC%89%E4%B8%8B%E8%BD%BDGraalVM "（1）下载GraalVM")（1）下载GraalVM

进入官网下载：[https://www.graalvm.org/downloads/](https://www.graalvm.org/downloads/)

[![image-20221207153944132](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207153944132.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207153944132.png)

[![image-20221207152841304](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207152841304.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207152841304.png)

##### [](https://blog.mohic.site/2024/05/18/spring6/#%EF%BC%882%EF%BC%89%E9%85%8D%E7%BD%AE%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F "（2）配置环境变量")（2）配置环境变量

**添加GRAALVM_HOME**

[![image-20221207110539954](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207110539954.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207110539954.png)

**把JAVA_HOME修改为graalvm的位置**

[![image-20221207153724340](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207153724340.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207153724340.png)

**把Path修改位graalvm的bin位置**

[![image-20221207153755732](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207153755732.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207153755732.png)

**使用命令查看是否安装成功**

[![image-20221207153642253](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207153642253.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207153642253.png)

##### [](https://blog.mohic.site/2024/05/18/spring6/#%EF%BC%883%EF%BC%89%E5%AE%89%E8%A3%85native-image%E6%8F%92%E4%BB%B6 "（3）安装native-image插件")（3）安装native-image插件

**使用命令 gu install native-image下载安装**

[![image-20221207155009832](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207155009832.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207155009832.png)

#### [](https://blog.mohic.site/2024/05/18/spring6/#11-2-2%E3%80%81%E5%AE%89%E8%A3%85C-%E7%9A%84%E7%BC%96%E8%AF%91%E7%8E%AF%E5%A2%83 "11.2.2、安装C++的编译环境")11.2.2、安装C++的编译环境

##### [](https://blog.mohic.site/2024/05/18/spring6/#%EF%BC%881%EF%BC%89%E4%B8%8B%E8%BD%BDVisual-Studio%E5%AE%89%E8%A3%85%E8%BD%AF%E4%BB%B6 "（1）下载Visual Studio安装软件")（1）下载Visual Studio安装软件

[https://visualstudio.microsoft.com/zh-hans/downloads/](https://visualstudio.microsoft.com/zh-hans/downloads/)

[![image-20221219112426052](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221219112426052.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221219112426052.png)

##### [](https://blog.mohic.site/2024/05/18/spring6/#%EF%BC%882%EF%BC%89%E5%AE%89%E8%A3%85Visual-Studio "（2）安装Visual Studio")（2）安装Visual Studio

[![image-20221207155726572](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207155726572.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207155726572.png)

[![image-20221207155756512](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207155756512.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207155756512.png)

##### [](https://blog.mohic.site/2024/05/18/spring6/#%EF%BC%883%EF%BC%89%E6%B7%BB%E5%8A%A0Visual-Studio%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F "（3）添加Visual Studio环境变量")（3）添加Visual Studio环境变量

配置INCLUDE、LIB和Path

[![image-20221207110947997](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207110947997.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207110947997.png)

[![image-20221207111012582](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207111012582.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207111012582.png)

[![image-20221207111105569](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207111105569.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207111105569.png)

##### [](https://blog.mohic.site/2024/05/18/spring6/#%EF%BC%884%EF%BC%89%E6%89%93%E5%BC%80%E5%B7%A5%E5%85%B7%EF%BC%8C%E5%9C%A8%E5%B7%A5%E5%85%B7%E4%B8%AD%E6%93%8D%E4%BD%9C "（4）打开工具，在工具中操作")（4）打开工具，在工具中操作

[![image-20221207111206279](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207111206279.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207111206279.png)

#### [](https://blog.mohic.site/2024/05/18/spring6/#11-2-3%E3%80%81%E7%BC%96%E5%86%99%E4%BB%A3%E7%A0%81%EF%BC%8C%E6%9E%84%E5%BB%BANative-Image "11.2.3、编写代码，构建Native Image")11.2.3、编写代码，构建Native Image

##### [](https://blog.mohic.site/2024/05/18/spring6/#%EF%BC%881%EF%BC%89%E7%BC%96%E5%86%99Java%E4%BB%A3%E7%A0%81 "（1）编写Java代码")（1）编写Java代码

java

|   |   |
|---|---|
|1  <br>2  <br>3  <br>4  <br>5  <br>6|public class Hello {  <br>  <br>    public static void main(String[] args) {  <br>        System.out.println("hello world");  <br>    }  <br>}|

##### [](https://blog.mohic.site/2024/05/18/spring6/#%EF%BC%882%EF%BC%89%E5%A4%8D%E5%88%B6%E6%96%87%E4%BB%B6%E5%88%B0%E7%9B%AE%E5%BD%95%EF%BC%8C%E6%89%A7%E8%A1%8C%E7%BC%96%E8%AF%91 "（2）复制文件到目录，执行编译")（2）复制文件到目录，执行编译

[![image-20221207111420056](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207111420056.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207111420056.png)

##### [](https://blog.mohic.site/2024/05/18/spring6/#%EF%BC%883%EF%BC%89Native-Image-%E8%BF%9B%E8%A1%8C%E6%9E%84%E5%BB%BA "（3）Native Image 进行构建")（3）Native Image 进行构建

[![image-20221207111509837](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207111509837.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207111509837.png)

[![image-20221207111609878](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207111609878.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207111609878.png)

##### [](https://blog.mohic.site/2024/05/18/spring6/#%EF%BC%884%EF%BC%89%E6%9F%A5%E7%9C%8B%E6%9E%84%E5%BB%BA%E7%9A%84%E6%96%87%E4%BB%B6 "（4）查看构建的文件")（4）查看构建的文件

[![image-20221207111644950](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207111644950.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207111644950.png)

##### [](https://blog.mohic.site/2024/05/18/spring6/#%EF%BC%885%EF%BC%89%E6%89%A7%E8%A1%8C%E6%9E%84%E5%BB%BA%E7%9A%84%E6%96%87%E4%BB%B6 "（5）执行构建的文件")（5）执行构建的文件

[![image-20221207111731150](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207111731150.png)](https://ghproxy.588854.xyz/mohicai/File/main/Qexo/img/Spring6/image-20221207111731150.png)

可以看到这个Hello最终打包产出的二进制文件大小为11M，这是包含了SVM和JDK各种库后的大小，虽然相比C/C++的二进制文件来说体积偏大，但是对比完整JVM来说，可以说是已经是非常小了。

相比于使用JVM运行，Native Image的速度要快上不少，cpu占用也更低一些，从官方提供的各类实验数据也可以看出Native Image对于启动速度和内存占用带来的提升是非常显著的：](<文章目录
1.概述
1.1定义
1.2作用
1.3简介
1.4狭义和广义
1.5模块组成
1.5.1Spring Core（核心容器）
1.5.2Spring AOP（面向切面编程）
1.5.3Spring Data Access（数据访问）
1.5.4Spring Web（应用程序）
1.5.5Spring Message（消息传递）
1.5.6Spring test（测试）
1.6Spring Framework（框架）
1.6.1概述
1.6.2作用
1.6.3特点
1.7 特点
2.基本用例-Spring框架基本使用
3.原理
4.启用日志框架
4.1概述
4.2组成
4.3基本用例-Log4j2基本使用
5.容器：IoC（重点）
5.1概述
5.1.1定义
5.1.2简介
5.1.3作用
5.1.4依赖注入
5.1.4.1定义
5.1.4.2作用
5.1.4.3实现方式
5.1.5实现
5.2基于XML管理Bean（了解）
5.2.1获取Bean的方式
5.2.1.1根据ID获取Bean
5.2.1.2根据类型获取Bean
5.2.1.3根据Id和类型获取Bean
5.2.2依赖注入
5.2.2.1根据setter注入
5.2.2.2根据构造器注入
5.2.3特殊值处理
5.2.3.1字面量赋值
5.2.3.2null值
5.2.3.3xml实体
5.2.3.4CDATA节
5.2.4注入对象类型属性值
5.2.4.1引用外部Bean
5.2.4.2引用内部Bean
5.2.4.3级联属性赋值
5.2.5注入数组类型属性值
5.2.6注入集合类型属性值
5.2.6.1注入List集合类型属性值
5.2.6.2注入Map集合类型属性值
5.2.6.2注入引用集合类型属性值
5.2.7引入P命名空间属性值
5.2.8引入外部属性文件
5.2.9引入Bean的作用域
5.2.10Bean的生命周期
5.2.11引入FactoryBean属性值
5.2.12引入xml自动装配
5.3基于注解管理Bean（重点）
5.3.1概述
5.3.1.1简介
5.3.1.2步骤
5.3.1.3使用注解
5.3.2开启组件扫描
5.3.2.1概述
5.3.2.2基本用例-实现组件扫描
5.3.2.3指定要排除的组件
5.3.2.4仅扫描指定组件
5.3.2使用注解定义Bean
5.3.3使用@Autowired注入
5.3.3.1概述
5.3.3.2属性注入
5.3.3.3set注入
5.3.3.4构造方法注入
5.3.3.5形参注入
5.3.3.6无注解注入
5.3.3.7联合@Qualifier注解注入
5.3.4使用@Resource注入
5.3.4.1概述
5.3.4.2Name注入
5.3.4.3未知Name注入
5.3.4.4类型注入
5.3.5全注解开发
5.3.5.1概述
5.3.5.2基本用例-全注解开发实现
5.4原理
6.面向切面：AOP (重点)
6.1概述
6.1.1定义
6.1.2作用
6.1.3横切关注点
6.1.4通知（增强）
6.1.5切面
6.1.6目标
6.1.7代理
6.1.8连接点
6.1.9切入点
6.2代理模式
6.2.1概述
6.2.2静态代理
6.2.3动态代理
6.2.3.1概述
6.2.3.1.1定义
6.2.3.1.2分类
6.2.3.2基本用例-实现动态代理
6.3切入点表达式
6.4基于注解的AOP
6.4.1概述
6.4.2基本用例-注解实现AOP
6.4.3通知方式
6.4.3.1前置通知
6.4.3.2异常通知
6.4.3.3返回通知
6.4.3.4后置通知
6.4.3.5环绕通知
6.4.4获取通知信息
6.4.4.1获取连接点信息
6.4.4.2获取目标方法的返回值
6.4.4.3获取目标方法的异常
6.4.5重用切入点表达式
6.4.5.1声明
6.4.5.2同切面使用
6.4.5.3不同切面使用
6.5基于XML的AOP（了解）
知识加油站
1.自动装配和依赖注入的区别与联系
2.依赖注入的两种方式
1.概述
笔记小结：

含义：Spring 是一款主流的 Java EE 轻量级开源框架，包含Spring MVC、Spring Boot、Spring Cloud等
作用：简化 Java 企业级应用的开发难度和开发周期，提供了整合其他技术和框架的能力
简介：核心功能是控制反转(IoC)和面向切面(AOP)
组成：
Spring Core（核心容器）
Spring AOP（面向切面编程）
Spring **Data Access（**数据访问）
Spring Web（应用程序）
Spring Message（消息传递）
Spring test（测试）
Spring Framework（框架）
概述：Spring Framework是Spring项目的核心框架
作用：Spring Framework实现IOC容器和AOP技术的功能模块
特点：
非侵入式
控制反转
面向切面编程
容器
组件化
特点：
轻：框架轻量级，不依赖其余Spring的对象
控制反转（IOC）：实现了对象之间的松耦合
面向切面（AOP）：分离应用的业务逻辑与系统级服务
容器：Spring包含并管理应用对象的配置和生命周期
1.1定义
​ Spring 是一款主流的 Java EE 轻量级开源框架 ，由于其轻便、易用和高效，被广泛应用于企业级Java应用开发中。

​ Spring包含了很多子框架和扩展，如Spring MVC、Spring Boot、Spring Cloud等。

​ Spring的主要特点是IOC容器和AOP技术，它们使得Java应用的开发和管理更加简单和高效。

1.2作用
​ Spring 目的是用于简化 Java 企业级应用的开发难度和开发周期。Spring 框架除了自己提供功能外，还提供整合其他技术和框架的能力

1.3简介
​ 自 2004 年 4 月，Spring 1.0 版本正式发布以来，Spring 已经步入到了第 6 个大版本，也就是 Spring 6。



说明：

​ 参考链接：Spring Framework

Spring是一个轻量级的控制反转(IoC)和面向切面(AOP)的容器框架。
Spring最初的出现是为了解决EJB臃肿的设计，以及难以测试等问题。
Spring为简化开发而生，让程序员只需关注核心业务的实现，尽可能的不再关注非业务逻辑代码（事务控制，安全日志等）。
1.4狭义和广义
广义的 Spring：Spring 技术栈
​ 广义上的 Spring 泛指以 Spring Framework 为核心的 Spring 技术栈。

​ 经过十多年的发展，Spring 已经不再是一个单纯的应用框架，而是逐渐发展成为一个由多个不同子项目（模块）组成的成熟技术，例如 Spring Framework、Spring MVC、SpringBoot、Spring Cloud、Spring Data、Spring Security 等，其中 Spring Framework 是其他子项目的基础。

​ 这些子项目涵盖了从企业级应用开发到云计算等各方面的内容，能够帮助开发人员解决软件发展过程中不断产生的各种实际问题，给开发人员带来了更好的开发体验。

狭义的 Spring：Spring Framework
​ 狭义的 Spring 特指 Spring Framework，通常我们将它称为 Spring 框架。

​ Spring 框架是一个分层的、面向切面的 Java 应用程序的一站式轻量级解决方案，它是 Spring 技术栈的核心和基础，是为了解决企业级应用开发的复杂性而创建的。

Spring 有两个最核心模块： IoC 和 AOP。

IoC：Inverse of Control 的简写，译为“控制反转”，指把创建对象过程交给 Spring 进行管理。
AOP：Aspect Oriented Programming 的简写，译为“面向切面编程”。AOP 用来封装多个类的公共行为，将那些与业务无关，却为业务模块所共同调用的逻辑封装起来，减少系统的重复代码，降低模块间的耦合度。另外，AOP 还解决一些系统层面上的问题，比如日志、事务、权限等。
1.5模块组成


说明：

​ 上图中包含了 Spring 框架的所有模块，这些模块可以满足一切企业级应用开发的需求，在开发过程中可以根据需求有选择性地使用所需要的模块。下面分别对这些模块的作用进行简单介绍。

1.5.1Spring Core（核心容器）
​ spring core提供了IOC,DI,Bean配置装载创建的核心实现。核心概念： Beans、BeanFactory、BeanDefinitions、ApplicationContext。

spring-core ：IOC和DI的基本实现

spring-beans：BeanFactory和Bean的装配管理(BeanFactory)

spring-context：Spring context上下文，即IOC容器(AppliactionContext)

spring-expression：spring表达式语言

1.5.2Spring AOP（面向切面编程）
spring-aop：面向切面编程的应用模块，整合ASM，CGLib，JDK Proxy
spring-aspects：集成AspectJ，AOP应用框架
spring-instrument：动态Class Loading模块
1.5.3Spring Data Access（数据访问）
spring-jdbc：spring对JDBC的封装，用于简化jdbc操作
spring-orm：java对象与数据库数据的映射框架
spring-oxm：对象与xml文件的映射框架
spring-jms： Spring对Java Message Service(java消息服务)的封装，用于服务之间相互通信
spring-tx：spring jdbc事务管理
1.5.4Spring Web（应用程序）
spring-web：最基础的web支持，建立于spring-context之上，通过servlet或listener来初始化IOC容器
spring-webmvc：实现web mvc
spring-websocket：与前端的全双工通信协议
spring-webflux：Spring 5.0提供的，用于取代传统java servlet，非阻塞式Reactive Web框架，异步，非阻塞，事件驱动的服务
1.5.5Spring Message（消息传递）
Spring-messaging：spring 4.0提供的，为Spring集成一些基础的报文传送服务
1.5.6Spring test（测试）
spring-test：集成测试支持，主要是对junit的封装
1.6Spring Framework（框架）
1.6.1概述
​ Spring Framework是Spring项目的核心框架，而Spring是整个Spring项目的总称，包括了Spring Framework和其他相关的子项目和扩展



1.6.2作用
​ Spring Framework实现IOC容器和AOP技术的功能模块

​ Spring Framework包含了许多模块，如Core模块、Beans模块、Context模块、AOP模块、Web模块等，每个模块都提供了不同的功能，可以灵活地选择使用。Spring Framework的目标是为了简化企业级Java开发，提高开发效率和质量。

1.6.3特点
非侵入式：使用 Spring Framework 开发应用程序时，Spring 对应用程序本身的结构影响非常小。对领域模型可以做到零污染；对功能性组件也只需要使用几个简单的注解进行标记，完全不会破坏原有结构，反而能将组件结构进一步简化。这就使得基于 Spring Framework 开发应用程序时结构清晰、简洁优雅。

控制反转：IoC——Inversion of Control，翻转资源获取方向。把自己创建资源、向环境索取资源变成环境将资源准备好，我们享受资源注入。

面向切面编程：AOP——Aspect Oriented Programming，在不修改源代码的基础上增强代码功能。

容器：Spring IoC 是一个容器，因为它包含并且管理组件对象的生命周期。组件享受到了容器化的管理，替程序员屏蔽了组件创建过程中的大量细节，极大的降低了使用门槛，大幅度提高了开发效率。

组件化：Spring 实现了使用简单的组件配置组合成一个复杂的应用。在 Spring 中可以使用 XML 和 Java 注解组合这些对象。这使得我们可以基于一个个功能明确、边界清晰的组件有条不紊的搭建超大型复杂应用系统。

一站式：在 IoC 和 AOP 的基础上可以整合各种企业应用的开源框架和优秀的第三方类库。而且 Spring 旗下的项目已经覆盖了广泛领域，很多方面的功能性需求可以在 Spring Framework 的基础上全部使用 Spring 来实现。

1.7 特点
轻
从大小与开销两方面而言Spring都是轻量的。完整的Spring框架可以在一个大小只有1MB多的JAR文件里发布。并且Spring所需的处理开销也是微不足道的。
Spring是非侵入式的：Spring应用中的对象不依赖于Spring的特定类。
控制反转
Spring通过一种称作控制反转（IoC）的技术促进了松耦合。当应用了IoC，一个对象依赖的其它对象会通过被动的方式传递进来，而不是这个对象自己创建或者查找依赖对象。你可以认为IoC与JNDI相反——不是对象从容器中查找依赖，而是容器在对象初始化时不等对象请求就主动将依赖传递给它。
面向切面
Spring提供了面向切面编程的丰富支持，允许通过分离应用的业务逻辑与系统级服务（例如审计（auditing）和事务（transaction）管理）进行内聚性的开发。应用对象只实现它们应该做的——完成业务逻辑——仅此而已。它们并不负责（甚至是意识）其它的系统级关注点，例如日志或事务支持。
容器
Spring包含并管理应用对象的配置和生命周期，在这个意义上它是一种容器，你可以配置你的每个bean如何被创建——基于一个可配置原型（prototype），你的bean可以创建一个单独的实例或者每次需要时都生成一个新的实例——以及它们是如何相互关联的。然而，Spring不应该被混同于传统的重量级的EJB容器，它们经常是庞大与笨重的，难以使用。
框架
Spring可以将简单的组件配置、组合成为复杂的应用。在Spring中，应用对象被声明式地组合，典型地是在一个XML文件里。Spring也提供了很多基础功能（事务管理、持久化框架集成等等），将应用逻辑的开发留给了你。
说明：

​ 所有Spring的这些特征使你能够编写更干净、更可管理、并且更易于测试的代码。它们也为Spring中的各种模块提供了基础支持。

Spring6要求JDK最低版本是JDK17


2.基本用例-Spring框架基本使用
说明：

​ 本基本用例演示，通过XML方式，实现Bean的自动注入

补充：环境

JDK：Java17+（Spring6要求JDK最低版本是Java17）

Maven：3.6+

Spring：6.0.2

步骤一：构建模块

通过Idea开发工具，创建空项目后创建子模块


说明：

​ 在空项目中，创建子模块

步骤二：导入依赖

修改模块的pom.xml文件
%3Cdependencies%3E
    <!--spring context依赖-->
    <!--当你引入Spring Context依赖之后，表示将Spring的基础依赖引入了-->
    <dependency>
        <groupId>org.springframework</groupId>
        <artifactId>spring-context</artifactId>
        <version>6.0.2</version>
    </dependency>

    <!--junit5测试-->
    <!--此依赖可选，主要便于junit进行测试使用-->
    <dependency>
        <groupId>org.junit.jupiter</groupId>
        <artifactId>junit-jupiter-api</artifactId>
        <version>5.3.1</version>
    </dependency>
</dependencies>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
说明：

​ 在pom.xml文件中，添加如上依赖

补充：

添加完成后，可在IDEA工具中的最右侧点击Maven进行查看


步骤三：创建实体

package org.example.entity;

public class User {
    public void add() {
        System.out.println("add……");
    }
}

1
2
3
4
5
6
7
8
说明：

​ 在org.example.entity包下，创建User实体

步骤四：创建配置文件

在模块的resources目录下，创建beans.xml文件
说明：

​ 创建beans.xml文件，是为了完成通过xml的方式实现依赖的自动注入

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd">

    <!--id是该bean的唯一标识符，在整个应用程序上下文中用于获取该bean实例-->
    <!--class是该bean所属的Java类的全限定名（包括包名），它告诉Spring需要实例化哪个类-->
    <bean id="user" class="org.example.entity.User"/>
</beans>
1
2
3
4
5
6
7
8
9
说明：

在beans,xml文件中，有bean标签
在beans,xml文件中，bean标签有Id属性，与class属性
步骤五：演示

在模块中的test.java包下，创建UserTest类
public class UserTest {
    @Test
    void newTest() {
        ApplicationContext applicationContext = new ClassPathXmlApplicationContext("beans.xml");
        User user = (User) applicationContext.getBean("user");
        user.add(); // add……
    }
}
1
2
3
4
5
6
7
8
补充：

@Test 是 JUnit 框架中的一个注解，表示该方法是一个测试方法，会被 JUnit 框架执行。

3.原理
笔记小结：通过XML方式，实现Bean的自动注入的基本用例原理

创建对象时，会调用无参构造方法
Spring 是通过反射机制调用无参构造方法创建对象
Spring 创建的对象（Bean对象），最终存储在Spring容器中
1.创建对象时，会调用无参构造方法

public class HelloWorld {
    public HelloWorld() {
        System.out.println("无参数构造方法执行");
    }
    public void sayHello(){
        System.out.println("helloworld");
    }
}
1
2
3
4
5
6
7
8
说明：



2.Spring 是通过反射机制调用无参构造方法创建对象

// dom4j解析beans.xml文件，从中获取class属性值，类的全类名
// 通过反射机制调用无参数构造方法创建对象
Class clazz = Class.forName("com.atguigu.spring6.bean.HelloWorld");
//Object obj = clazz.newInstance();
Object object = clazz.getDeclaredConstructor().newInstance();
1
2
3
4
5
3.Spring 创建的对象（Bean对象），最终存储在Spring容器中

private final Map<String, BeanDefinition> beanDefinitionMap = new ConcurrentHashMap<>(256);
1
说明：

Spring容器底层就是一个map集合
存储bean的map在DefaultListableBeanFactory类中
Spring容器加载到Bean类时 , 会把这个类的描述信息, 以包名加类名的方式存到beanDefinitionMap 中
Map<String,BeanDefinition> , 其中 String是Key , 默认是类名首字母小写 。BeanDefinition , 存的是类的定义(描述信息) , 我们通常叫BeanDefinition接口为 : bean的定义对象。
4.启用日志框架
笔记小结：

概述：Log4j2是一个开源的Java日志框架，帮助Java开发人员在应用程序中实现灵活和可配置的日志记录

组成：

日志信息的优先级：TRACE < DEBUG < INFO < WARN < ERROR < FATAL
日志信息的输出目的地：控制台或者本地文件
日志信息的输出格式：日志信息的显示内容
基本用例：

导入依赖：
<!--log4j2的依赖-->
<dependency>
  <groupId>org.apache.logging.log4j</groupId>
  <artifactId>log4j-core</artifactId>
  <version>2.19.0</version>
</dependency>
<dependency>
  <groupId>org.apache.logging.log4j</groupId>
  <artifactId>log4j-slf4j2-impl</artifactId>
  <version>2.19.0</version>
</dependency>
1
2
3
4
5
6
7
8
9
10
11
创建日志配置文件：建议复制根据需求修改

使用日志

private Logger logger = LoggerFactory.getLogger(HelloWorldTest.class);
……
logger.info("执行成功");
1
2
3
结果：



4.1概述
​ Log4j2是一个开源的Java日志框架，是Log4j的升级版。它可以帮助Java开发人员在应用程序中实现灵活和可配置的日志记录，支持异步日志记录、多线程安全等特性

4.2组成
日志信息的优先级，日志信息的优先级从高到低有TRACE < DEBUG < INFO < WARN < ERROR < FATAL

说明：

TRACE：追踪，是最低的日志级别，相当于追踪程序的执行
DEBUG：调试，一般在开发中，都将其设置为最低的日志级别
INFO：信息，输出重要的信息，使用较多
WARN：警告，输出警告的信息
ERROR：错误，输出错误信息
FATAL：严重错误
日志信息的输出目的地，日志信息的输出目的地指定了日志将打印到控制台还是文件中；

日志信息的输出格式，而输出格式则控制了日志信息的显示内容。

4.3基本用例-Log4j2基本使用
步骤一：引入Log4j2依赖

修改模块中的pom.xml文件
<!--log4j2的依赖-->
<dependency>
    <groupId>org.apache.logging.log4j</groupId>
    <artifactId>log4j-core</artifactId>
    <version>2.19.0</version>
</dependency>
<dependency>
    <groupId>org.apache.logging.log4j</groupId>
    <artifactId>log4j-slf4j2-impl</artifactId>
    <version>2.19.0</version>
</dependency>
1
2
3
4
5
6
7
8
9
10
11
说明：

​ log4j的Maven使用光有核心core依赖不够，还需要有实现impl依赖

步骤二：创建日志配置文件

在模块文件路径在resource的根路径下，配置文件名为log4j2.xml
<?xml version="1.0" encoding="UTF-8"?>
<configuration>
    <loggers>
        <!--
            level指定日志级别，从低到高的优先级：
                TRACE < DEBUG < INFO < WARN < ERROR < FATAL
                trace：追踪，是最低的日志级别，相当于追踪程序的执行
                debug：调试，一般在开发中，都将其设置为最低的日志级别
                info：信息，输出重要的信息，使用较多
                warn：警告，输出警告的信息
                error：错误，输出错误信息
                fatal：严重错误
        -->
        <root level="DEBUG">
            <appender-ref ref="spring6log"/>
            <appender-ref ref="RollingFile"/>
            <appender-ref ref="log"/>
        </root>
    </loggers>

    <appenders>
        <!--输出日志信息到控制台-->
        <console name="spring6log" target="SYSTEM_OUT">
            <!--控制日志输出的格式-->
            <PatternLayout pattern="%d{yyyy-MM-dd HH:mm:ss SSS} [%t] %-3level %logger{1024} - %msg%n"/>
        </console>

        <!--文件会打印出所有信息，这个log每次运行程序会自动清空，由append属性决定，适合临时测试用-->
        <File name="log" fileName="d:/spring6_log/test.log" append="false">
            <PatternLayout pattern="%d{HH:mm:ss.SSS} %-5level %class{36} %L %M - %msg%xEx%n"/>
        </File>

        <!-- 这个会打印出所有的信息，
            每次大小超过size，
            则这size大小的日志会自动存入按年份-月份建立的文件夹下面并进行压缩，
            作为存档-->
        <RollingFile name="RollingFile" fileName="d:/spring6_log/app.log"
                     filePattern="log/$${date:yyyy-MM}/app-%d{MM-dd-yyyy}-%i.log.gz">
            <PatternLayout pattern="%d{yyyy-MM-dd 'at' HH:mm:ss z} %-5level %class{36} %L %M - %msg%xEx%n"/>
            <SizeBasedTriggeringPolicy size="50MB"/>
            <!-- DefaultRolloverStrategy属性如不设置，
            则默认为最多同一文件夹下7个文件，这里设置了20 -->
            <DefaultRolloverStrategy max="20"/>
        </RollingFile>
    </appenders>
</configuration>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
步骤三：日常使用

在日常中，只用log4j2，此处创建HelloWorldTest使用
public class HelloWorldTest {

    // 1.通过日志工程获取日志对象记录器
    private Logger logger = LoggerFactory.getLogger(HelloWorldTest.class);
 
    @Test
    public void testHelloWorld(){
        ApplicationContext ac = new ClassPathXmlApplicationContext("beans.xml");
        HelloWorld helloworld = (HelloWorld) ac.getBean("helloWorld");
        helloworld.sayHello();
        // 2.记录日志
        logger.info("执行成功");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
说明：

​ 创建日志记录器

步骤四：演示



说明：

​ 当完成以上步骤后，运行，日志就会输出在控制台

5.容器：IoC（重点）
笔记小结：见各个小节

5.1概述
笔记小结：

定义：IoC (Inversion of Control)，即控制反转，是一种设计模式或者说设计思想
简介：Spring 通过 IoC 容器来管理所有 Java 对象的实例化和初始化，控制对象与对象之间的依赖关系
作用：通过容器来管理对象的创建、销毁、依赖注入等操作，而应用程序本身只需要使用这些对象即可
依赖注入:
含义：以解耦对象之间的依赖关系
作用：Spring通过依赖注入的方式来完成Bean管理的。换句话说，依赖注入，依赖注入实现了控制反转的思想
实现方式（重点）：
setter注入
构造注入
实现接口以及常用类：
BeanFactory接口：面向 Spring 本身，不提供给开发人员使用
ApplicationContext接口：面向 Spring 的使用者，几乎所有场合（创建、管理Bean实例，支持国际化、资源访问、消息传递）都适用
常用类：
FileSystemXmlApplicationContext：通过文件系统路径读取 XML 格式的配置文件创建 IOC 容器对象
ClassPathXmlApplicationContext：通过读取类路径下的 XML 格式的配置文件创建 IOC 容器对象
5.1.1定义
​ IoC (Inversion of Control)，即控制反转，是一种设计模式或者说设计思想，它是面向对象编程中的一种概念，用来描述对象之间的依赖关系，指导我们如何设计出松耦合、更优良的程序。

5.1.2简介
​ Spring 通过 IoC 容器来管理所有 Java 对象的实例化和初始化，控制对象与对象之间的依赖关系。我们将由 IoC 容器管理的 Java 对象称为 Spring Bean，它与使用关键字 new 创建的 Java 对象没有任何区别。

5.1.3作用
​ 在 IoC 模式中，控制权从程序代码中转移到了容器中，即通过容器来管理对象的创建、销毁、依赖注入等操作，而应用程序本身只需要使用这些对象即可。这样，应用程序就不需要自己管理对象之间的依赖关系，而是由容器来管理，从而实现了代码的解耦和更好的可维护性，提高程序扩展力。

说明：

将对象的创建权利交出去，交给第三方容器负责
将对象和对象之间关系的维护权交出去，交给第三方容器负责
5.1.4依赖注入
5.1.4.1定义
​ 依赖注入（Dependency Injection，DI）是一种设计模式，其主要思想是在程序运行的过程中，通过外部容器（如Spring容器）动态地将依赖对象注入到程序中，以解耦对象之间的依赖关系，从而提高程序的灵活性、可维护性和可测试性。

5.1.4.2作用
​ **Spring通过依赖注入的方式来完成Bean管理的。**换句话说，依赖注入，依赖注入实现了控制反转的思想。依赖指的是对象和对象之间的关联关系。注入指的是一种数据传递行为，通过注入行为来让对象和对象产生关系。

补充：

​ Bean管理说的是：Bean对象的创建，以及Bean对象中属性的赋值（或者叫做Bean对象之间关系的维护）。

5.1.4.3实现方式
第一种：set注入
第二种：构造注入
5.1.5实现
​ Spring 的框架中，IoC 容器是通过 BeanFactory 和 ApplicationContext 接口实现的。BeanFactory 接口是 Spring 框架最底层的接口，提供了基本的 IoC 功能；ApplicationContext 接口是 BeanFactory 接口的子接口，提供了更高级的特性和功能，如 AOP、国际化、事件驱动等。其中BeanFactory 接口，最重要的方法是getBean()方法，用于从容器中获取对象。

​ Spring 的 IoC 容器就是 IoC思想的一个落地的产品实现。IoC容器中管理的组件也叫做 bean。在创建 bean 之前，首先需要创建IoC 容器。Spring 提供了IoC 容器的两种实现方式：

BeanFactory：这是 IoC 容器的基本实现，是 Spring 内部使用的接口。面向 Spring 本身，不提供给开发人员使用。
ApplicationContext：BeanFactory 的子接口，提供了更多高级特性。面向 Spring 的使用者，几乎所有场合都使用 ApplicationContext 而不是底层的 BeanFactory
ApplicationContext的主要实现类:

类型名	简介
ClassPathXmlApplicationContext	通过读取类路径下的 XML 格式的配置文件创建 IOC 容器对象
FileSystemXmlApplicationContext	通过文件系统路径读取 XML 格式的配置文件创建 IOC 容器对象
ConfigurableApplicationContext	ApplicationContext 的子接口，包含一些扩展方法 refresh() 和 close() ，让 ApplicationContext 具有启动、关闭和刷新上下文的能力。
WebApplicationContext	专门为 Web 应用准备，基于 Web 环境创建 IOC 容器对象，并将对象引入存入 ServletContext 域中。


说明：

​ ApplicationContext有众多的实现类，其中最常用的就是ClassPathXmlApplicationContext与FileSystemXmlApplicationContext实现类

5.2基于XML管理Bean（了解）
笔记小结：

获取Bean的方式：

根据ID：

User user = (User) applicationContext.getBean("user");
1
根据类型：

 User user = (User) applicationContext.getBean(User.class);
1
根据Id和类型:

User user = (User) applicationContext.getBean("user", User.class);
1
依赖注入

根据Setter注入：<property/>
根据构造器注入：<constructor-arg/>
特殊值处理

字面量赋值<property>
Null值<null>
Xml实体：属性值value="a &lt; b"
CDATA节：标签内容<![CDATA[a < b]]>
注入对象类型属性值

引用外部Bean：属性ref
引用内部Bean：bean嵌套
级联属性赋值：引入对象后，级联赋值name="clazz.clazzId"
注入数组类型属性值：<array></array>

注入集合类型属性值：

注入List集合类型属性值： <list> </list>
注入Map集合类型属性值：<map><entry><<key>/key><value></value></entry></map>
注入引用集合类型属性值：<util></util>
注意：使用前，需要引入util命名空间
引入P命名空间属性值：属性p:

注意：使用前，需要引入p命名空间
引入外部属性文件：<context:property-placeholder location="classpath:jdbc.properties"/>

引入Bean的作用域：属性scope属性值prototype（多例）、singleton（单例）

Bean的生命周期：

bean对象创建（调用无参构造器）

bean对象设置属性

bean的后置处理器（初始化之前）

bean对象初始化（需在配置bean时指定初始化方法）

bean的后置处理器（初始化之后）

bean对象就绪可以使用

bean对象销毁（需在配置bean时指定销毁方法）

IOC容器关闭

引入FactoryBean属性值：实现FactoryBean<T>接口

引入自动装配：属性值autowire属性值byType、byName

5.2.1获取Bean的方式
5.2.1.1根据ID获取Bean
public class UserTest {
    @Test
    void newTest() {
        ApplicationContext applicationContext = new ClassPathXmlApplicationContext("beans.xml");
        User user = (User) applicationContext.getBean("user");
        user.add(); // add……
    }
}
1
2
3
4
5
6
7
8
说明：

​ 此获取方式，需要基于第2.基本用例进行查看

5.2.1.2根据类型获取Bean
public class UserTest {
    @Test
    void newTest() {
        ApplicationContext applicationContext = new ClassPathXmlApplicationContext("beans.xml");
        User user = (User) applicationContext.getBean(User.class);
        user.add(); // add……
    }
}
1
2
3
4
5
6
7
8
注意：

当根据类型获取bean时，要求IOC容器中指定类型的bean有且只能有一个

org.springframework.beans.factory.NoUniqueBeanDefinitionException: No qualifying bean of type 'com.atguigu.spring6.bean.HelloWorld' available: expected single matching bean but found 2: helloworldOne,helloworldTwo
1
说明：

​ 此获取方式，需要基于第2.基本用例进行查看

5.2.1.3根据Id和类型获取Bean
public class UserTest {
    @Test
    void newTest() {
        ApplicationContext applicationContext = new ClassPathXmlApplicationContext("beans.xml");
        User user = (User) applicationContext.getBean("user", User.class);
        user.add(); // add……
    }
}
1
2
3
4
5
6
7
8
补充：

​ 如果组件类实现了接口，可以根据接口类型获取Bean，但前提是Bean唯一

说明：

​ 此获取方式，需要基于第2.基本用例进行查看

5.2.2依赖注入
5.2.2.1根据setter注入
步骤一：创建学生类Student

package com.atguigu.spring6.bean;

public class Student {

    private Integer id;

    private String name;

    private Integer age;

    private String sex;

    public Student() {
    }

    public Integer getId() {
        return id;
    }

    public void setId(Integer id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public Integer getAge() {
        return age;
    }

    public void setAge(Integer age) {
        this.age = age;
    }

    public String getSex() {
        return sex;
    }

    public void setSex(String sex) {
        this.sex = sex;
    }

    @Override
    public String toString() {
        return "Student{" +
                "id=" + id +
                ", name='" + name + '\'' +
                ", age=" + age +
                ", sex='" + sex + '\'' +
                '}';
    }

}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
步骤二：配置bean时为属性赋值

<bean id="studentOne" class="com.atguigu.spring6.bean.Student">
    <!-- property标签：通过组件类的setXxx()方法给组件对象设置属性 -->
    <!-- name属性：指定属性名（这个属性名是getXxx()、setXxx()方法定义的，和成员变量无关） -->
    <!-- value属性：指定属性值 -->
    <property name="id" value="1001"></property>
    <property name="name" value="张三"></property>
    <property name="age" value="23"></property>
    <property name="sex" value="男"></property>
</bean>
1
2
3
4
5
6
7
8
9
说明：

​ 当使用标签标签完成对象的属性创建时，name需要跟对象中的成员变量同名

步骤三：演示

@Test
public void testDIBySet(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-di.xml");
    Student studentOne = ac.getBean("studentOne", Student.class);
    System.out.println(studentOne);
}
1
2
3
4
5
6
说明：

​ 当打印输出是，由于基于XML根据Setter注入方式进行对象的创建，此时输出可获得成员方法tostring的内容

5.2.2.2根据构造器注入
步骤一：在基于根据setter注入的基础上，在Student类中添加有参构造

public Student(Integer id, String name, Integer age, String sex) {
    this.id = id;
    this.name = name;
    this.age = age;
    this.sex = sex;
}
1
2
3
4
5
6
步骤二：配置bean

<bean id="studentTwo" class="com.atguigu.spring6.bean.Student">
    <constructor-arg name="id" value="1002"></constructor-arg>
    <constructor-arg name="name" value="李四"></constructor-arg>
    <constructor-arg name="age"value="33"></constructor-arg>
    <constructor-arg name="sex" value="女"></constructor-arg>
</bean>
1
2
3
4
5
6
说明：

constructor-arg标签属性描述构造器参数：
index属性：指定参数所在位置的索引（从0开始）
name属性：指定参数名，name需要跟对象中的成员变量同名
步骤三：演示

@Test
public void testDIByConstructor(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-di.xml");
    Student studentOne = ac.getBean("studentTwo", Student.class);
    System.out.println(studentOne);
}
1
2
3
4
5
6
说明：

​ 当打印输出是，由于基于XML根据构造器注入方式进行对象的创建，此时输出可获得成员方法tostring的内容

5.2.3特殊值处理
5.2.3.1字面量赋值
<!-- 使用value属性给bean的属性赋值时，Spring会把value属性的值看做字面量 -->
<property name="name" value="张三"/>
1
2
5.2.3.2null值
<property name="name">
    <null />
</property>
1
2
3
细节：

<property name="name" value="null"></property>
1
以上写法，为name所赋值为字符串null

5.2.3.3xml实体
<!-- 解决方案一：使用XML实体来代替 -->
<property name="expression" value="a &lt; b"/>
1
2
说明：

​ 小于号在XML文档中用来定义标签的开始，不能随便使用

5.2.3.4CDATA节
<property name="expression">
    <!-- 解决方案二：使用CDATA节 -->
    <value><![CDATA[a < b]]></value>
</property>
1
2
3
4
说明：

CDATA中的C代表Character，是文本、字符的含义，CDATA就表示纯文本数据
ML解析器看到CDATA节就知道这里是纯文本，就不会当作XML标签或属性来解析
所以CDATA节中写什么符号都随意
5.2.4注入对象类型属性值
5.2.4.1引用外部Bean
步骤一：配置Clazz类型的bean

<bean id="clazzOne" class="com.atguigu.spring6.bean.Clazz">
    <property name="clazzId" value="1111"></property>
    <property name="clazzName" value="财源滚滚班"></property>
</bean>
1
2
3
4
步骤二：为Student中的clazz属性赋值

<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->
    <property name="clazz" ref="clazzOne"></property>
</bean>
1
2
3
4
5
6
7
8
说明：

​ 当引用外部对象时，需要将ref属性变为Value属性。ref属性，值表示引用对象、value属性，值表示字符串

5.2.4.2引用内部Bean
步骤一：在引用外部Bean的基础上

<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <property name="clazz">
        <!-- 在一个bean中再声明一个bean就是内部bean -->
        <!-- 内部bean只能用于给属性赋值，不能在外部通过IOC容器获取，因此可以省略id属性 -->
        <bean id="clazzInner" class="com.atguigu.spring6.bean.Clazz">
            <property name="clazzId" value="2222"></property>
            <property name="clazzName" value="远大前程班"></property>
        </bean>
    </property>
</bean>
1
2
3
4
5
6
7
8
9
10
11
12
13
14
说明：

​ 将Bean写于属性标签内，即为引用内部Bean

5.2.4.3级联属性赋值
步骤一：在引用内部Bean的基础上

<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <property name="clazz" ref="clazzOne"></property>
    <property name="clazz.clazzId" value="3333"></property>
    <property name="clazz.clazzName" value="最强王者班"></property>
</bean>
1
2
3
4
5
6
7
8
9
5.2.5注入数组类型属性值
步骤一：在Student类中中添加成员变量数组和getter于setter方法

private String[] hobbies;

public String[] getHobbies() {
    return hobbies;
}

public void setHobbies(String[] hobbies) {
    this.hobbies = hobbies;
}
1
2
3
4
5
6
7
8
9
步骤二：配置Bean

<bean id="studentFour" class="com.atguigu.spring.bean6.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->
    <property name="clazz" ref="clazzOne"></property>
    <property name="hobbies">
        <array>
            <value>抽烟</value>
            <value>喝酒</value>
            <value>烫头</value>
        </array>
    </property>
</bean>
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
说明：

​ 当注入数组类型数据时，需要使用标签

5.2.6注入集合类型属性值
5.2.6.1注入List集合类型属性值
步骤一：在Clazz类中添加添加成员变量集合和getter于setter方法

private List<Student> students;

public List<Student> getStudents() {
    return students;
}

public void setStudents(List<Student> students) {
    this.students = students;
}
1
2
3
4
5
6
7
8
9
步骤二：配置Bean

<bean id="clazzTwo" class="com.atguigu.spring6.bean.Clazz">
    <property name="clazzId" value="4444"></property>
    <property name="clazzName" value="Javaee0222"></property>
    <property name="students">
        <list>
            <ref bean="studentOne"></ref>
            <ref bean="studentTwo"></ref>
            <ref bean="studentThree"></ref>
        </list>
    </property>
</bean>
1
2
3
4
5
6
7
8
9
10
11
说明：

​ 当注入List集合类型数据时，需要使用标签

细节：

​ 因为List students，List集合中引用的是Student对象，因此注入时需要使用标签，进行引用对象

5.2.6.2注入Map集合类型属性值
步骤一：创建Student类

package com.atguigu.spring6.bean;
public class Teacher {

    private Integer teacherId;

    private String teacherName;

    public Integer getTeacherId() {
        return teacherId;
    }

    public void setTeacherId(Integer teacherId) {
        this.teacherId = teacherId;
    }

    public String getTeacherName() {
        return teacherName;
    }

    public void setTeacherName(String teacherName) {
        this.teacherName = teacherName;
    }

    public Teacher(Integer teacherId, String teacherName) {
        this.teacherId = teacherId;
        this.teacherName = teacherName;
    }

    public Teacher() {

    }
    
    @Override
    public String toString() {
        return "Teacher{" +
                "teacherId=" + teacherId +
                ", teacherName='" + teacherName + '\'' +
                '}';
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
步骤二：在Student类中添加添加成员变量集合和getter于setter方法

private Map<String, Teacher> teacherMap;

public Map<String, Teacher> getTeacherMap() {
    return teacherMap;
}

public void setTeacherMap(Map<String, Teacher> teacherMap) {
    this.teacherMap = teacherMap;
}
1
2
3
4
5
6
7
8
9
步骤三：配置bean

<bean id="teacherOne" class="com.atguigu.spring6.bean.Teacher">
    <property name="teacherId" value="10010"></property>
    <property name="teacherName" value="大宝"></property>
</bean>

<bean id="teacherTwo" class="com.atguigu.spring6.bean.Teacher">
    <property name="teacherId" value="10086"></property>
    <property name="teacherName" value="二宝"></property>
</bean>

<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->
    <property name="clazz" ref="clazzOne"></property>
    <property name="hobbies">
        <array>
            <value>抽烟</value>
            <value>喝酒</value>
            <value>烫头</value>
        </array>
    </property>
    <property name="teacherMap">
        <map>
            <entry>
                <key>
                    <value>10010</value>
                </key>
                <ref bean="teacherOne"></ref>
            </entry>
            <entry>
                <key>
                    <value>10086</value>
                </key>
                <ref bean="teacherTwo"></ref>
            </entry>
        </map>
    </property>
</bean>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
说明：

当注入Map集合类型数据时，需要使用标签
需要使用表示键值对
需要使用表示键
细节：

​ 因为Map<String, Teacher> teacherMap，Map集合中引用的是Teacher对象，因此注入时需要使用标签，进行引用对象

5.2.6.2注入引用集合类型属性值
步骤一：配置对应的命名空间

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns:util="http://www.springframework.org/schema/util"
    xsi:schemaLocation="http://www.springframework.org/schema/util
    http://www.springframework.org/schema/util/spring-util.xsd
    http://www.springframework.org/schema/beans
    http://www.springframework.org/schema/beans/spring-beans.xsd">
1
2
3
4
5
6
7
8
步骤二：配置Bean

<!--list集合类型的bean-->
<util:list id="students">
    <ref bean="studentOne"></ref>
    <ref bean="studentTwo"></ref>
    <ref bean="studentThree"></ref>
</util:list>
<!--map集合类型的bean-->
<util:map id="teacherMap">
    <entry>
        <key>
            <value>10010</value>
        </key>
        <ref bean="teacherOne"></ref>
    </entry>
    <entry>
        <key>
            <value>10086</value>
        </key>
        <ref bean="teacherTwo"></ref>
    </entry>
</util:map>
<bean id="clazzTwo" class="com.atguigu.spring6.bean.Clazz">
    <property name="clazzId" value="4444"></property>
    <property name="clazzName" value="Javaee0222"></property>
    <property name="students" ref="students"></property>
</bean>
<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->
    <property name="clazz" ref="clazzOne"></property>
    <property name="hobbies">
        <array>
            <value>抽烟</value>
            <value>喝酒</value>
            <value>烫头</value>
        </array>
    </property>
    <property name="teacherMap" ref="teacherMap"></property>
</bean>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
说明：

使用标签，可以将List集合或者Map集合的属性注入变为引用的方式
在使用util标签时，需要引入相应的命名空间
5.2.7引入P命名空间属性值
步骤一：引入P命名空间

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:util="http://www.springframework.org/schema/util"
       xmlns:p="http://www.springframework.org/schema/p"
       xsi:schemaLocation="http://www.springframework.org/schema/util
       http://www.springframework.org/schema/util/spring-util.xsd
       http://www.springframework.org/schema/beans
       http://www.springframework.org/schema/beans/spring-beans.xsd">
1
2
3
4
5
6
7
8
9
步骤二：通过p命名空间方式为bean的各个属性赋值

<bean id="studentSix" class="com.atguigu.spring6.bean.Student"
    p:id="1006" p:name="小明" p:clazz-ref="clazzOne" p:teacherMap-ref="teacherMap"></bean>
1
2
说明：

​ 通过p:成员属性，即可完成各个属性的赋值.

5.2.8引入外部属性文件
步骤一：添加依赖

 <!-- MySQL驱动 -->
<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <version>8.0.30</version>
</dependency>

<!-- 数据源 -->
<dependency>
    <groupId>com.alibaba</groupId>
    <artifactId>druid</artifactId>
    <version>1.2.15</version>
</dependency>
1
2
3
4
5
6
7
8
9
10
11
12
13
步骤二：创建外部属性文件

jdbc.user=root
jdbc.password=atguigu
jdbc.url=jdbc:mysql://localhost:3306/ssm?serverTimezone=UTC
jdbc.driver=com.mysql.cj.jdbc.Driver
1
2
3
4
说明：

​ 在resources文件下创建jdbc.properties文件

步骤三：引入属性文件

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:context="http://www.springframework.org/schema/context"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
                           http://www.springframework.org/schema/beans/spring-beans.xsd
                           http://www.springframework.org/schema/context
                           http://www.springframework.org/schema/context/spring-context.xsd">
    <!-- 引入外部属性文件 -->
    <context:property-placeholder location="classpath:jdbc.properties"/>
</beans>
1
2
3
4
5
6
7
8
9
10
11
注意：

​ 在使用 <context:property-placeholder> 元素加载外包配置文件功能前，首先需要在 XML 配置的一级标签 中添加 context 相关的约束。

步骤四：配置Bean

<!--完成数据库信息注入-->
<bean id="druidDataSource" class="com.alibaba.druid.pool.DruidDataSource">
    <property name="url" value="${jdbc.url}"/>
    <property name="driverClassName" value="${jdbc.driver}"/>
    <property name="username" value="${jdbc.user}"/>
    <property name="password" value="${jdbc.password}"/>
</bean>
1
2
3
4
5
6
7
说明：

​ 取外部文件中的值时，需要根据外部文件中属性的名字，可以把相应值取得

步骤五：演示

@Test
public void testDataSource() throws SQLException {
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-datasource.xml");
    DataSource dataSource = ac.getBean(DruidDataSource.class);
    Connection connection = dataSource.getConnection();
    System.out.println(connection);
}
1
2
3
4
5
6
7
5.2.9引入Bean的作用域
步骤一：创建类User

package com.atguigu.spring6.bean;
public class User {

    private Integer id;

    private String username;

    private String password;

    private Integer age;

    public User() {
    }

    public User(Integer id, String username, String password, Integer age) {
        this.id = id;
        this.username = username;
        this.password = password;
        this.age = age;
    }

    public Integer getId() {
        return id;
    }

    public void setId(Integer id) {
        this.id = id;
    }

    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public String getPassword() {
        return password;
    }

    public void setPassword(String password) {
        this.password = password;
    }

    public Integer getAge() {
        return age;
    }

    public void setAge(Integer age) {
        this.age = age;
    }

    @Override
    public String toString() {
        return "User{" +
                "id=" + id +
                ", username='" + username + '\'' +
                ", password='" + password + '\'' +
                ", age=" + age +
                '}';
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
步骤二：配置bean

<!-- scope属性：取值singleton（默认值），bean在IOC容器中只有一个实例，IOC容器初始化时创建对象 -->
<!-- scope属性：取值prototype，bean在IOC容器中可以有多个实例，getBean()时创建对象 -->
<bean class="com.atguigu.spring6.bean.User" scope="prototype"></bean>
1
2
3
说明：

属性值：
singleton（默认），在IOC容器中，这个bean的对象始终为单实例，当IOC容器初始化时即可创建对象
prototype，在IOC容器中，这个bean在IOC容器中有多个实例，当 获取bean时可创建对象
步骤三：演示

@Test
public void testBeanScope(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-scope.xml");
    User user1 = ac.getBean(User.class);
    User user2 = ac.getBean(User.class);
    System.out.println(user1==user2);
}
1
2
3
4
5
6
7
5.2.10Bean的生命周期
流程

bean对象创建（调用无参构造器）

bean对象设置属性

bean的后置处理器（初始化之前）

bean对象初始化（需在配置bean时指定初始化方法）

bean的后置处理器（初始化之后）

bean对象就绪可以使用

bean对象销毁（需在配置bean时指定销毁方法）

IOC容器关闭

步骤一：修改User类

public class User {

    private Integer id;

    private String username;

    private String password;

    private Integer age;

    public User() {
        System.out.println("生命周期：1、创建对象");
    }

    public User(Integer id, String username, String password, Integer age) {
        this.id = id;
        this.username = username;
        this.password = password;
        this.age = age;
    }

    public Integer getId() {
        return id;
    }

    public void setId(Integer id) {
        System.out.println("生命周期：2、依赖注入");
        this.id = id;
    }

    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public String getPassword() {
        return password;
    }

    public void setPassword(String password) {
        this.password = password;
    }

    public Integer getAge() {
        return age;
    }

    public void setAge(Integer age) {
        this.age = age;
    }

    public void initMethod(){
        System.out.println("生命周期：3、初始化");
    }

    public void destroyMethod(){
        System.out.println("生命周期：5、销毁");
    }

    @Override
    public String toString() {
        return "User{" +
                "id=" + id +
                ", username='" + username + '\'' +
                ", password='" + password + '\'' +
                ", age=" + age +
                '}';
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
64
65
66
67
68
69
70
71
72
说明：

​ 其中的initMethod()和destroyMethod()，可以通过配置Bean指定为初始化和销毁的方法

步骤二：创建Bean 的后置处理器

package com.atguigu.spring6.process;
    
import org.springframework.beans.BeansException;
import org.springframework.beans.factory.config.BeanPostProcessor;

public class MyBeanProcessor implements BeanPostProcessor {
    
    @Override
    public Object postProcessBeforeInitialization(Object bean, String beanName) throws BeansException {
        System.out.println("☆☆☆" + beanName + " = " + bean);
        return bean;
    }
    
    @Override
    public Object postProcessAfterInitialization(Object bean, String beanName) throws BeansException {
        System.out.println("★★★" + beanName + " = " + bean);
        return bean;
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
注意：

​ bean的后置处理器会在生命周期的初始化前后添加额外的操作，需要实现BeanPostProcessor接口，且配置到IOC容器中，需要注意的是，bean后置处理器不是单独针对某一个bean生效，而是针对IOC容器中所有bean都会执行

步骤三：配置Bean

<!-- 使用init-method属性指定初始化方法 -->
<!-- 使用destroy-method属性指定销毁方法 -->
<bean class="com.atguigu.spring6.bean.User" scope="prototype" init-method="initMethod" destroy-method="destroyMethod">
    <property name="id" value="1001"></property>
    <property name="username" value="admin"></property>
    <property name="password" value="123456"></property>
    <property name="age" value="23"></property>
</bean>
<!-- bean的后置处理器要放入IOC容器才能生效 -->
<bean id="myBeanProcessor" class="com.atguigu.spring6.process.MyBeanProcessor"/>
1
2
3
4
5
6
7
8
9
10
说明：

在配置Bean时，需要使用init-method属性和destroy-method属性进行配置Bean的初始化方法与销毁的方法
在配置Bean时，需要将Bean的后置处理器放入IOC容器才能生效
步骤四：演示

@Test
public void testLife(){
    ClassPathXmlApplicationContext ac = new ClassPathXmlApplicationContext("spring-lifecycle.xml");
    User bean = ac.getBean(User.class);
    System.out.println("生命周期：4、通过IOC容器获取bean并使用");
    ac.close();
}
1
2
3
4
5
6
7
5.2.11引入FactoryBean属性值


说明：

​ FactoryBean是Spring提供的一种整合第三方框架的常用机制。和普通的bean不同，配置一个FactoryBean类型的bean，在获取bean的时候得到的并不是class属性中配置的这个类的对象，而是getObject()方法的返回值。通过这种机制，Spring可以帮我们把复杂组件创建的详细过程和繁琐细节都屏蔽起来，只把最简洁的使用界面展示给我们。

步骤一 ：创建类UserFactoryBean

package com.atguigu.spring6.bean;
public class UserFactoryBean implements FactoryBean<User> {
    @Override
    public User getObject() throws Exception {
        return new User();
    }

    @Override
    public Class<?> getObjectType() {
        return User.class;
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
步骤二：配置bean

<bean id="user" class="com.atguigu.spring6.bean.UserFactoryBean"></bean>
1
步骤三：演示

@Test
public void testUserFactoryBean(){
    //获取IOC容器
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-factorybean.xml");
    User user = (User) ac.getBean("user");
    System.out.println(user);
}
1
2
3
4
5
6
7
说明：

​ 此时获取到的容器对象，并不是UserFactoryBean，而是User

5.2.12引入xml自动装配
步骤一：环境准备

1.创建UserController类

package com.atguigu.spring6.autowire.controller
public class UserController {

    private UserService userService;

    public void setUserService(UserService userService) {
        this.userService = userService;
    }

    public void saveUser(){
        userService.saveUser();
    }

}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
2.创建UserService接口

package com.atguigu.spring6.autowire.service
public interface UserService {

    void saveUser();

}
1
2
3
4
5
6
3.创建UserServiceImpl类实现UserService接口

package com.atguigu.spring6.autowire.service.impl
public class UserServiceImpl implements UserService {

    private UserDao userDao;

    public void setUserDao(UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void saveUser() {
        userDao.saveUser();
    }

}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
4.创建UserDao接口

package com.atguigu.spring6.autowire.dao
public interface UserDao {

    void saveUser();

}
1
2
3
4
5
6
5.创建UserDaoImpl类实现UserDao接口

package com.atguigu.spring6.autowire.dao.impl
public class UserDaoImpl implements UserDao {

    @Override
    public void saveUser() {
        System.out.println("保存成功");
    }

}
1
2
3
4
5
6
7
8
9
步骤二：配置bean

<bean id="userController" class="com.atguigu.spring6.autowire.controller.UserController" autowire="byType"></bean>

<bean id="userService" class="com.atguigu.spring6.autowire.service.impl.UserServiceImpl" autowire="byType"></bean>

<bean id="userDao" class="com.atguigu.spring6.autowire.dao.impl.UserDaoImpl"></bean>
1
2
3
4
5
说明：

当使用Bean标签的autowire属性是，通过byType的方式进行自动装配
byType：根据类型匹配IOC容器中的某个兼容类型的bean，为属性自动赋值
若在IOC中，没有任何一个兼容类型的bean能够为属性赋值，则该属性不装配，即值为默认值null
若在IOC中，有多个兼容类型的bean能够为属性赋值，则抛出异常NoUniqueBeanDefinitionException
byName：将自动装配的属性的属性名，作为bean的id在IOC容器中匹配相对应的bean进行赋值
步骤三：演示

@Test
public void testAutoWireByXML(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("autowire-xml.xml");
    UserController userController = ac.getBean(UserController.class);
    userController.saveUser();
}
1
2
3
4
5
6
说明：

​ 当使用标签中的属性时，使用Autowire属性使用byType的方式即可实现属性的自动注入

5.3基于注解管理Bean（重点）
笔记小结：

概述：

简介：Java 增加了对注解（Annotation）的支持，它是代码中的一种特殊标记，可以在编译、类加载和运行时被读取，执行相应的处理。
使用注解：
@Component：表示泛化组件
@Repository：表示数据访问层组件
@Service：表示业务层组件
@Controller：：表示控制层组件
开启组件扫描

概述：通过 <context:component-scan> 元素开启 Spring Beans的自动扫描功能。Spring 会自动从扫描指定的包（base-package 属性设置）及其子包下的所有类，如果类上使用了 @Component 注解，就将该类装配到容器中
基本用例：使用标签<context:component-scan></context:component-scan>
添加conentt约束
开启扫描方式
指定要排除的组件： <context:exclude-filter></context:exclude-filter>
仅扫描指定组件： <context:include-filter></context:include-filter
使用注解定义Bean

使用@Autowired注入：

属性注入

@Autowired
private UserDao userDao;
1
2
setter注入

private UserDao userDao;
@Autowired
public void setUserDao(UserDao userDao) {
    this.userDao = userDao;
}
1
2
3
4
5
构造方法注入

private UserDao userDao;
@Autowired
public UserServiceImpl(UserDao userDao) {
	this.userDao = userDao;
}
1
2
3
4
5
形参注入

private UserDao userDao;
public UserServiceImpl(@Autowired UserDao userDao) {
    this.userDao = userDao;
}
1
2
3
4
无注解注入：当构造函数仅有一个需要注入的构造参数时，@Autowired可以省略

private UserDao userDao;
public UserServiceImpl(UserDao userDao) {
    this.userDao = userDao;
}
1
2
3
4
联合**@Qualifier注解注入：适用于一个接口多个实现类的注解区别**

@Autowired
@Qualifier("userDaoImpl") // 指定bean的名字
private UserDao userDao;
1
2
3
使用@Resource注入：

Name注入：在使用注解时，配置name属性

@Resource(name = "myUserDao")
1
未知Name注入：不配置name属性，注入属性的成员变量但需要与Bean 的名称同名

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {
    ……
@Resource
private UserDao myUserDao;
1
2
3
4
5
类型注入：不配置name属性，名称都不同时，注入属性的成员类型会根据Bean实现的接口类型进行匹配

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {
    ……
@Resource
private UserDao userDao1;
1
2
3
4
5
全注解开发：不再使用spring配置文件了，写一个配置类来代替配置文件

@Configuration
//@ComponentScan({"com.atguigu.spring6.controller", "com.atguigu.spring6.service","com.atguigu.spring6.dao"})
@ComponentScan("com.atguigu.spring6") //开启包扫描
public class Spring6Config {
}
1
2
3
4
5
说明：用全注解开发方式时，需要指定包扫描所属的范围，便于Spring框架确定扫描而注入Bean的范围

5.3.1概述
5.3.1.1简介
​ 从 Java 5 开始，Java 增加了对注解（Annotation）的支持，它是代码中的一种特殊标记，可以在编译、类加载和运行时被读取，执行相应的处理。开发人员可以通过注解在不改变原有代码和逻辑的情况下，在源代码中嵌入补充信息。

​ Spring 从 2.5 版本开始提供了对注解技术的全面支持，我们可以使用注解来实现自动装配，简化 Spring 的 XML 配置。

5.3.1.2步骤
引入依赖
开启组件扫描
使用注解定义 Bean
依赖注入
5.3.1.3使用注解
​ Spring 提供了以下多个注解，这些注解可以直接标注在 Java 类上，将它们定义成 Spring Bean

注解	说明
@Component	该注解用于描述 Spring 中的 Bean，它是一个泛化的概念，仅仅表示容器中的一个组件（Bean），并且可以作用在应用的任何层次，例如 Service 层、Dao 层等。 使用时只需将该注解标注在相应类上即可。
@Repository	该注解用于将数据访问层（Dao 层）的类标识为 Spring 中的 Bean，其功能与 @Component 相同。
@Service	该注解通常作用在业务层（Service 层），用于将业务层的类标识为 Spring 中的 Bean，其功能与 @Component 相同。
@Controller	该注解通常作用在控制层（如SpringMVC 的 Controller），用于将控制层的类标识为 Spring 中的 Bean，其功能与 @Component 相同。
5.3.2开启组件扫描
5.3.2.1概述
​ Spring 默认不使用注解装配 Bean，因此我们需要在 Spring 的 XML 配置中，通过 <context:component-scan> 元素开启 Spring Beans的自动扫描功能。开启此功能后，Spring 会自动从扫描指定的包（base-package 属性设置）及其子包下的所有类，如果类上使用了 @Component 注解，就将该类装配到容器中。

5.3.2.2基本用例-实现组件扫描
步骤一：添加约束

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:context="http://www.springframework.org/schema/context"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
    http://www.springframework.org/schema/beans/spring-beans-3.0.xsd
    http://www.springframework.org/schema/context
            http://www.springframework.org/schema/context/spring-context.xsd">
</beans>
1
2
3
4
5
6
7
8
9
说明：

​ 在 XML 配置的一级标签 中添加 context 相关的约束

步骤二：开启扫描方式

<context:component-scan base-package="com.atguigu.spring6">
</context:component-scan>
1
2
说明：

​ 在Beans.xml文件中，设置开启扫描方式即可

5.3.2.3指定要排除的组件
<context:component-scan base-package="com.atguigu.spring6">
    <!-- context:exclude-filter标签：指定排除规则 -->
    <!-- 
 		type：设置排除或包含的依据
		type="annotation"，根据注解排除，expression中设置要排除的注解的全类名
		type="assignable"，根据类型排除，expression中设置要排除的类型的全类名
	-->
    <context:exclude-filter type="annotation" expression="org.springframework.stereotype.Controller"/>
        <!--<context:exclude-filter type="assignable" expression="com.atguigu.spring6.controller.UserController"/>-->
</context:component-scan>
1
2
3
4
5
6
7
8
9
10
说明：

<context:exclude-filter></context:exclude-filter>标签，指定排除规则
type属性：设置排除或包含的依据
属性值：annotation，根据注解排除
属性值：assignable，根据类型排除
expression属性：设置要排除的注解或类型的全类名
5.3.2.4仅扫描指定组件
<context:component-scan base-package="com.atguigu" use-default-filters="false">
    <!-- context:include-filter标签：指定在原有扫描规则的基础上追加的规则 -->
    <!-- use-default-filters属性：取值false表示关闭默认扫描规则 -->
    <!-- 此时必须设置use-default-filters="false"，因为默认规则即扫描指定包下所有类 -->
    <context:include-filter type="annotation" expression="org.springframework.stereotype.Controller"/>
    <!--<context:include-filter type="assignable" expression="com.atguigu.spring6.controller.UserController"/>-->
</context:component-scan>
1
2
3
4
5
6
7
说明：

use-default-filters="false"，表示关闭默认扫描规则
<context:include-filter></context:include-filter>，表示指定的过滤条件来确定哪些类应该被包含在组件扫描中
5.3.2使用注解定义Bean
5.3.3使用@Autowired注入
5.3.3.1概述


说明：

@Autowired注解可以标注在：构造方法上、方法上、形参上、属性上、注解上
@Autowired注解的required属性，
属性值为True：表示注入的时候要求被注入的Bean必须是存在的，如果不存在则报错
属性值为False：：表示注入的时候要求被注入的Bean不一定是存在的，如果存在的话就注入，不存在的话，也不报错
细节：

单独使用@Autowired注解时，默认是根据类型装配，默认是"byType"，例如基于XML管理Bean
<bean id="userService" class="com.atguigu.spring6.autowire.service.impl.UserServiceImpl" autowire="byType"></bean>
1
5.3.3.2属性注入
步骤一：搭建环境

1.创建UserDao接口

package com.atguigu.spring6.dao;

public interface UserDao {

    public void print();
}
1
2
3
4
5
6
2.创建UserDaoImpl实现

package com.atguigu.spring6.dao.impl;

import com.atguigu.spring6.dao.UserDao;
import org.springframework.stereotype.Repository;

@Repository
public class UserDaoImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
3.创建UserService接口

package com.atguigu.spring6.service;

public interface UserService {

    public void out();
}
1
2
3
4
5
6
4.创建UserServiceImpl实现类

package com.atguigu.spring6.service.impl;

import com.atguigu.spring6.dao.UserDao;
import com.atguigu.spring6.service.UserService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;

@Service
public class UserServiceImpl implements UserService {

    @Autowired
    private UserDao userDao;

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
5.创建UserController类

package com.atguigu.spring6.controller;

import com.atguigu.spring6.service.UserService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Controller;

@Controller
public class UserController {

    @Autowired
    private UserService userService;

    public void out() {
        userService.out();
        System.out.println("Controller层执行结束。");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

当使用@Autowired注解注入时，可不提供构造方法喝Setter方法，也可以注入成功
结果：
5.3.3.3set注入
步骤一：搭建环境

1.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    private UserDao userDao;

    @Autowired
    public void setUserDao(UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
2.修改UserController类

@Controller
public class UserController {

    private UserService userService;

    @Autowired
    public void setUserService(UserService userService) {
        this.userService = userService;
    }

    public void out() {
        userService.out();
        System.out.println("Controller层执行结束。");
    }

}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

​ 通过在需要注入的setter方法上进行添加@Autowired注解

5.3.3.4构造方法注入
步骤一：搭建环境

1.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    private UserDao userDao;

    @Autowired
    public UserServiceImpl(UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
2.修改UserController类

@Controller
public class UserController {

    private UserService userService;

    @Autowired
    public UserController(UserService userService) {
        this.userService = userService;
    }

    public void out() {
        userService.out();
        System.out.println("Controller层执行结束。");
    }

}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

​ 通过在需要注入的构造器方法上进行添加@Autowired注解

5.3.3.5形参注入
步骤一：搭建环境

1.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    private UserDao userDao;

    public UserServiceImpl(@Autowired UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
2.修改UserController类

@Controller
public class UserController {

    private UserService userService;

    public UserController(@Autowired UserService userService) {
        this.userService = userService;
    }

    public void out() {
        userService.out();
        System.out.println("Controller层执行结束。");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

​ 通过在需要注入的形参上进行添加@Autowired注解

5.3.3.6无注解注入
步骤一：搭建环境

1.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

 
    private UserDao userDao;

    public UserServiceImpl(UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

​ 当有参数的构造方法只有一个时，@Autowired注解可以省略

5.3.3.7联合@Qualifier注解注入
步骤一：搭建环境

1.添加UserDaoRedisImpl类

@Repository
public class UserDaoRedisImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Redis Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
说明：

此时，添加实现UserDao接口类，已经造成一个接口对应两个实现类
此时，程序错误，信息中说：不能装配，UserDao这个Bean的数量等于2
步骤二：修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    @Autowired
    @Qualifier("userDaoImpl") // 指定bean的名字
    private UserDao userDao;

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
说明：

​ 当需要注入的接口有多个实现类时，可以联合使用@Qualifier(“userDaoImpl”) 注解，并指定实现类的名字，即可完成属性注入

5.3.4使用@Resource注入
5.3.4.1概述
​ @Resource注解是通过名称匹配的方式来实现注入的，默认按照名称进行匹配，如果找不到匹配的名称，则会尝试按照类型匹配。

​ @Resource注解是JDK扩展包中的，也就是说属于JDK的一部分。所以该注解是标准注解，更加具有通用性。(JSR-250标准中制定的注解类型。JSR是Java规范提案。)



说明：

如果是JDK8的话不需要额外引入依赖。高于JDK11或低于JDK8需要引入以下依赖
<dependency>
    <groupId>jakarta.annotation</groupId>
    <artifactId>jakarta.annotation-api</artifactId>
    <version>2.1.1</version>
</dependency>
1
2
3
4
5
5.3.4.2Name注入
步骤一：搭建环境

1.修改UserDaoImpl类

package com.atguigu.spring6.dao.impl;

import com.atguigu.spring6.dao.UserDao;
import org.springframework.stereotype.Repository;

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
说明：

​ 当使用注解时，在小括号内写上属性名称表示为此Bean定义别名

2.修改UserServiceImpl类

package com.atguigu.spring6.service.impl;

import com.atguigu.spring6.dao.UserDao;
import com.atguigu.spring6.service.UserService;
import jakarta.annotation.Resource;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.beans.factory.annotation.Qualifier;
import org.springframework.stereotype.Service;

@Service
public class UserServiceImpl implements UserService {

    @Resource(name = "myUserDao")
    private UserDao myUserDao;

    @Override
    public void out() {
        myUserDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
说明：

​ 当使用@Resource注解时，可以使用name属性指定属性注入的别名

步骤二：演示

5.3.4.3未知Name注入
步骤一：搭建环境

1.修改UserDaoImpl类

package com.atguigu.spring6.dao.impl;

import com.atguigu.spring6.dao.UserDao;
import org.springframework.stereotype.Repository;

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
2.修改UserServiceImpl类

package com.atguigu.spring6.service.impl;

import com.atguigu.spring6.dao.UserDao;
import com.atguigu.spring6.service.UserService;
import jakarta.annotation.Resource;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.beans.factory.annotation.Qualifier;
import org.springframework.stereotype.Service;

@Service
public class UserServiceImpl implements UserService {

    @Resource
    private UserDao myUserDao;

    @Override
    public void out() {
        myUserDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
说明：

​ 当使用@Resource注解时，在name属性未知的情况下，将属性注入的成员属性变量名定义为与Bean同名，即可完成注入

步骤二：演示

5.3.4.4类型注入
步骤一：搭建环境

1.原UserDaoImpl类

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
2.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    @Resource
    private UserDao userDao1;

    @Override
    public void out() {
        userDao1.print();
        System.out.println("Service层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
说明：

​ 当使用@Resource注解时，现在userDao1属性名不存在，但仍然可以注入成功。因为，UserDao他们的类型名相同

5.3.5全注解开发
5.3.5.1概述
​ 全注解开发就是不再使用spring配置文件了，写一个配置类来代替配置文件

5.3.5.2基本用例-全注解开发实现
步骤一：创建配置类

@Configuration
//@ComponentScan({"com.atguigu.spring6.controller", "com.atguigu.spring6.service","com.atguigu.spring6.dao"})
@ComponentScan("com.atguigu.spring6")
public class Spring6Config {
}
1
2
3
4
5
说明：

​ 使用@ComponentScan注解，进行组件扫描，从而替代了原有在xml文件中的配置

步骤二：演示

@Test
public void testAllAnnotation(){
    ApplicationContext context = new AnnotationConfigApplicationContext(Spring6Config.class);
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
    logger.info("执行成功");
}
1
2
3
4
5
6
7
说明：

​ 需要使用AnnotationConfigApplicationContext类来获取Spring6Config的字节码文件

5.4原理
笔记小结：

扫描指定的包，获取所有需要管理的类的类名。
实例化需要管理的类，通过反射机制调用构造器来实现。
通过反射机制调用setter方法或者构造器注入属性值。
维护对象之间的依赖关系，实现对象之间的解耦。
将实例化好的对象注册到IOC容器中，便于后续使用。
说明：



步骤一：环境搭建

1.创建注解

创建Bean注解

// 此注解用于定义容器对象，类似于@Componet、@Service、@Controller注解等作用
@Target(ElementType.TYPE)
@Retention(RetentionPolicy.RUNTIME)
public @interface Bean {
}
1
2
3
4
5
创建依赖注入注解

// 此注解用于完成成员属性的依赖注入，类似于@Autoware、@Resource注解等作用
@Target({ElementType.FIELD})
@Retention(RetentionPolicy.RUNTIME)
public @interface Di {
}
1
2
3
4
5
2.创建IOC核心逻辑

定义bean容器接口

package com.atguigu.spring.core;

public interface ApplicationContext {

    Object getBean(Class clazz);
}
1
2
3
4
5
6
编写注解bean容器接口实现

public class AnnotationApplicationContext implements ApplicationContext {

    // 存储Bean的容器
    private HashMap<Class, Object> beanFactory = new HashMap<>();

    // 根据字节码文件获取Bean容器中的对象
    @Override
    public Object getBean(Class clazz) {
        return beanFactory.get(clazz);
    }

    /**
     * 根据包扫描加载bean
     * @param basePackage
     */
    public AnnotationApplicationContext(String basePackage) {
        try {
            String packageDirName = basePackage.replaceAll("\\.", "\\\\");
            Enumeration<URL> dirs =Thread.currentThread().getContextClassLoader().getResources(packageDirName);
            while (dirs.hasMoreElements()) {
                URL url = dirs.nextElement();
                String filePath = URLDecoder.decode(url.getFile(),"utf-8");
                rootPath = filePath.substring(0, filePath.length()-packageDirName.length());
                // 扫描包下的Bean
                loadBean(new File(filePath));
            }

        } catch (Exception e) {
            throw new RuntimeException(e);
        }
        //依赖注入
        loadDi();
    }


    private  void loadBean(File fileParent) {
        if (fileParent.isDirectory()) {
            File[] childrenFiles = fileParent.listFiles();
            if(childrenFiles == null || childrenFiles.length == 0){
                return;
            }
            for (File child : childrenFiles) {
                if (child.isDirectory()) {
                    //如果是个文件夹就继续调用该方法,使用了递归
                    loadBean(child);
                } else {
                    //通过文件路径转变成全类名,第一步把绝对路径部分去掉
                    String pathWithClass = child.getAbsolutePath().substring(rootPath.length() - 1);
                    //选中class文件
                    if (pathWithClass.contains(".class")) {
                        //    com.xinzhi.dao.UserDao
                        //去掉.class后缀，并且把 \ 替换成 .
                        String fullName = pathWithClass.replaceAll("\\\\", ".").replace(".class", "");
                        try {
                            Class<?> aClass = Class.forName(fullName);
                            //把非接口的类实例化放在map中
                            if(!aClass.isInterface()){
                                Bean annotation = aClass.getAnnotation(Bean.class);
                                if(annotation != null){
                                    Object instance = aClass.newInstance();
                                    //判断一下有没有接口
                                    if(aClass.getInterfaces().length > 0) {
                                        //如果有接口把接口的class当成key，实例对象当成value
                                        System.out.println("正在加载【"+ aClass.getInterfaces()[0] +"】,实例对象是：" + instance.getClass().getName());
                                        beanFactory.put(aClass.getInterfaces()[0], instance);
                                    }else{
                                        //如果有接口把自己的class当成key，实例对象当成value
                                        System.out.println("正在加载【"+ aClass.getName() +"】,实例对象是：" + instance.getClass().getName());
                                        beanFactory.put(aClass, instance);
                                    }
                                }
                            }
                        } catch (ClassNotFoundException | IllegalAccessException | InstantiationException e) {
                            e.printStackTrace();
                        }
                    }
                }
            }
        }
    }

    private void loadDi() {
        for(Map.Entry<Class,Object> entry : beanFactory.entrySet()){
            //就是咱们放在容器的对象
            Object obj = entry.getValue();
            Class<?> aClass = obj.getClass();
            Field[] declaredFields = aClass.getDeclaredFields();
            for (Field field : declaredFields){
                Di annotation = field.getAnnotation(Di.class);
                if( annotation != null ){
                    field.setAccessible(true);
                    try {
                        System.out.println("正在给【"+obj.getClass().getName()+"】属性【" + field.getName() + "】注入值【"+ beanFactory.get(field.getType()).getClass().getName() +"】");
                        field.set(obj,beanFactory.get(field.getType()));
                    } catch (IllegalAccessException e) {
                        e.printStackTrace();
                    }
                }
            }
        }
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
64
65
66
67
68
69
70
71
72
73
74
75
76
77
78
79
80
81
82
83
84
85
86
87
88
89
90
91
92
93
94
95
96
97
98
99
100
101
102
说明：

可将此代码复制到IDEA中查看逻辑更详细

3.创建Dao层

创建UserDao接口
public interface UserDao {

    public void print();
}
1
2
3
4
创建UserDaoImpl实现
@Bean
public class UserDaoImpl implements UserDao {
    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}

1
2
3
4
5
6
7
8
说明：

当此类实现了UserDao这个接口时，会将UserDao这个接口作为容器的Key值，来获取UserDaoImpl这个实现类

这也就是为什么一个接口不能对应多个实现类，因为HashMap的Key值不能重复

// 参数解释，参数1：实现类上实现的第一个接口或者实现类的字节码文件；参数2：实现类实例
beanFactory.put(aClass.getInterfaces()[0], instance);
// 此处，参数1：接口为UserDao；参数2，实现类实例为UserDaoImpl
1
2
3
4.创建Service层

创建UserService接口

public interface UserService {
    public void out();
}
1
2
3
创建UserServiceImpl实现类

@Bean
public class UserServiceImpl implements UserService {

    @DI
    private UserDao userDao;

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
说明：

当此类里包含了依赖注入这个接口时，会将UserServiceImpl这个实现类实例作为依赖注入的Key值，并且根据依赖注入的变量名确定所需要依赖注入的实现类实例

// 参数解释，参数1：设置字段值的对象实例；参数2：需要设置的字段值
field.set(obj, beanFactory.get(field.getType()));
//此处，参数1：实现类实例UserServiceImpl；参数2：实现类实例UserDaoImpl
1
2
3
步骤二：演示

ApplicationContext applicationContext = new AnnotationApplicationContext("org.example");
UserService bean = (UserService) applicationContext.getBean(UserService.class);
bean.out();
1
2
3
6.面向切面：AOP (重点)
笔记小结：

概述：

含义：AOP（Aspect Oriented Programming）是一种设计思想，是软件设计领域中的面向切面编程
作用：
简化开发：分离关注点，让各个一些通用的行为（日志、事务、安全）实现重用
降低代码耦合度：将不同的关注点分离开来，提高代码可复用性和可维护性
横切关注点：横切关注点是指跨越应用程序多个模块的功能或行为。例如日志记录、安全性等与业务逻辑无关的功能
通知：通知（增强）是指在 AOP 中定义的一种特殊类型的方法，它包含要在连接点（join point）执行的一些行为。例如在某个方法执行前、中、后需要加上一些输出日志等这样的逻辑
切面：切面指的是横切关注点和通知的组合，简单的说，切面就是封装通知方法的类
目标：目标（Target）是指被通知的对象或者被切面所影响的对象。例如类、接口、方法这类元素
代理：代理是指控制对目标对象的访问，并在访问过程中插入额外的逻辑。简单的说，代理就是向目标对象应用通知之后创建的代理对象
连接点：连接点（Join Point）表示在程序执行过程中能够插入一个切面的点。简单的说，连接点就是代理对象中的执行逻辑
切入点：切入点（Pointcut）表示在目标对象中定义的一个或多个特定的方法或方法执行位置，它表示在何处应该插入切面的逻辑
代理模式：代理模式是一种结构型设计模式，它使得代理对象可以代表另一个对象进行访问

静态代理：静态代理是用代码的方式实现方法之前或之后执行一些附加操作
动态代理：它允许在运行时动态地创建代理对象，并将切面逻辑织入到目标对象的方法中
分类：基于接口的代理（有接口情况）、基于类的代理（无接口情况）
切入点表达式：用于匹配目标对象中的方法，并提供切入点的精确定义



基于注解的AOP：各个小结模块，请查看此小结（重点）

基于XML的AOP：通过XML 的方式来实现切面的定义和应用（了解）

6.1概述
6.1.1定义
​ AOP（Aspect Oriented Programming）是一种设计思想，是软件设计领域中的面向切面编程，它是面向对象编程的一种补充和完善，它以通过预编译方式和运行期动态代理方式实现，在不修改源代码的情况下，给程序动态统一添加额外功能的一种技术。利用AOP可以对业务逻辑的各个部分进行隔离，从而使得业务逻辑各部分之间的耦合度降低，提高程序的可重用性，同时提高了开发的效率

6.1.2作用
代码重用和模块化：AOP可以将一些通用的行为（例如日志记录、安全控制、事务管理等）抽象出来，形成可重用的模块，避免在每个业务逻辑中都重复编写这些代码。

分离关注点：AOP将不同的关注点分离开来，使得各个模块间职责更加清晰明确，代码的可读性和可维护性也更强。

简化开发：AOP可以帮助开发人员将关注点从业务逻辑中分离出来，使得开发更加简单明了。

提高系统的可扩展性：在系统需求变化时，只需要修改AOP模块而不是修改业务逻辑，这可以使得系统更加易于扩展和维护。

降低代码耦合度：AOP的作用是将不同的关注点分离开来，这可以避免代码之间的紧耦合，提高代码的可复用性和可维护性。

6.1.3横切关注点
​ 在 AOP 中，横切关注点指的是在应用程序中影响多个类或对象的横切性质的行为，比如日志记录、性能监控、事务处理等等。这些行为可能分散在整个应用程序中的不同类和方法中，而不是与应用程序的核心业务逻辑紧密相关。

​ 使用 AOP 技术，可以将这些横切关注点从应用程序的核心业务逻辑中分离出来，并将它们模块化为可重用的模块，从而实现更好的代码结构和更好的可维护性。



6.1.4通知（增强）
​ 通知（advice）也被称为增强（advice），是指在 AOP 中定义的一种特殊类型的方法，它包含要在连接点（join point）执行的一些行为。通知可以在目标方法执行之前、之后或异常时被执行，也可以在目标方法返回一个结果后被执行。通知的目的是在不修改目标对象的情况下，将增强（如日志、事务管理等）应用于应用程序的特定方法或切入点。通知是实现 AOP 的核心组件之一，通过将通知应用于特定的连接点（join point）来实现面向切面编程

简单来说：通知就是你想要增强的功能，比如 安全，事务，日志等

通知分类：

前置通知：在被代理的目标方法前执行
返回通知：在被代理的目标方法成功结束后执行（寿终正寝）
异常通知：在被代理的目标方法异常结束后执行（死于非命）
后置通知：在被代理的目标方法最终结束后执行（盖棺定论）
环绕通知：使用try…catch…finally结构围绕整个被代理的目标方法，包括上面四种通知对应的所有位置


6.1.5切面
​ 在AOP中，切面指的是横切关注点和通知的组合，它是一个模块化的横向分割，可以理解为一个横向的切片。切面是对横切关注点和通知的封装，它包含了一组切点和通知，用于描述在何处、何时、以及如何执行横切逻辑。切面可以在不修改原代码的情况下，对原有的代码进行功能的增强或改变。通常，切面是以一个类的形式存在的，它包含了一个或多个通知和一个或多个切点。

简单来说：切面就是封装通知方法的类



6.1.6目标
​ 在AOP（Aspect-Oriented Programming）中，目标（Target）是指被通知的对象或者被切面所影响的对象。它是应用程序中的一个具体元素，可以是类、接口、方法或者字段等。简单点说，目标就是被代理的目标对象

6.1.7代理
​ 在AOP（Aspect-Oriented Programming）中，代理（Proxy）是一种设计模式，用于控制对目标对象的访问，并在访问过程中插入额外的逻辑。简单点说，代理就是向目标对象应用通知之后创建的代理对象

6.1.8连接点
​ 在 AOP 中，连接点（Join Point）表示在程序执行过程中能够插入一个切面的点，例如方法调用、异常处理、字段访问等。连接点定义了在程序中的哪个位置可以应用切面。切面可以在连接点前后增加额外的处理逻辑，从而影响程序的行为。通俗地讲，连接点就是在程序执行中可以被拦截的地方



说明：

​ 把方法排成一排，每一个横切位置看成x轴方向，把方法从上到下执行的顺序看成y轴，x轴和y轴的交叉点就是连接点。通俗说，就是spring允许你使用通知的地方

6.1.9切入点
​ 在 AOP 中，切入点（Join Point）是指程序执行过程中明确的点，通常是方法调用的时候，也可以是异常处理程序的处理过程。切入点定义了哪些方法是需要被拦截或增强的，是 AOP 中最重要的概念之一。切入点通常以方法的形式被定义，比如某个类的所有方法、某个包下的所有方法等等。在 AOP 中，通常会使用表达式语言定义切入点，如使用 Spring AOP 中的 @Pointcut 注解定义。

6.2代理模式
6.2.1概述
​ 代理模式是一种结构型设计模式，它使得代理对象可以代表另一个对象进行访问。它是二十三种设计模式中的一种，属于结构型模式。它的作用就是通过提供一个代理类，让我们在调用目标方法的时候，不再是直接对目标方法进行调用，而是通过代理类间接调用。让不属于目标方法核心逻辑的代码从目标方法中剥离出来——解耦。调用目标方法时先调用代理对象的方法，减少对目标方法的调用和打扰，同时让附加功能能够集中在一起也有利于统一维护。



​

代理：将非核心逻辑剥离出来以后，封装这些非核心逻辑的类、对象、方法

6.2.2静态代理
​ 在静态代理中，代理类是在编译时期创建的，代理类和委托类实现相同的接口或继承相同的类，并在代理类中实现委托类中的方法，在调用委托类的方法之前或之后执行一些附加操作

public class CalculatorStaticProxy implements Calculator {
    
    // 将被代理的目标对象声明为成员变量
    private Calculator target;
    
    public CalculatorStaticProxy(Calculator target) {
        this.target = target;
    }
    
    @Override
    public int add(int i, int j) {
    
        // 附加功能由代理类中的代理方法来实现
        System.out.println("[日志] add 方法开始了，参数是：" + i + "," + j);
    
        // 通过目标对象来实现核心业务逻辑
        int addResult = target.add(i, j);
    
        System.out.println("[日志] add 方法结束了，结果是：" + addResult);
    
        return addResult;
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
说明：

​ 静态代理确实实现了解耦，但是由于代码都写死了，完全不具备任何的灵活性

6.2.3动态代理
6.2.3.1概述
6.2.3.1.1定义
​ 在动态代理中，代理类是在运行时期动态创建的。它不需要事先知道委托类的接口或实现类，而是在运行时期通过 Java 反射机制动态生成代理类



6.2.3.1.2分类
动态代理分类

基于接口的代理（有接口情况）
基于类的代理（无接口情况）


说明：

​ AspectJ：是AOP思想的一种实现。本质上是静态代理，将代理逻辑“织入”被代理的目标类编译得到的字节码文件，所以最终效果是动态的。weaver就是织入器。Spring只是借用了AspectJ中的注解。



说明：

当动态代理是基于接口的代理情况时，此种方式是JDK原生的实现方式。需要被代理的目标类必须**实现接口。因为这个技术要求代理对象和目标对象实现同样的接口**
当动态代理是基于类的代理情况时，通过**继承被代理的目标类**实现代理。因此不需要目标类实现接口
补充：

JDK动态代理动态生成的代理类会在com.sun.proxy包下，类名为$proxy1，和目标类实现相同的接口
cglib动态代理动态生成的代理类会和目标在在相同的包下，会继承目标类
6.2.3.2基本用例-实现动态代理
步骤一：创建ProxyFactory类

public class ProxyFactory {

    private Object target;

    public ProxyFactory(Object target) {
        this.target = target;
    }

    public Object getProxy(){
        /**
         * newProxyInstance()：创建一个代理实例
         * 其中有三个参数：
         * 1、classLoader：加载动态生成的代理类的类加载器
         * 2、interfaces：目标对象实现的所有接口的class对象所组成的数组
         * 3、invocationHandler：设置代理对象实现目标对象方法的过程，即代理类中如何重写接口中的抽象方法
         */
        ClassLoader classLoader = target.getClass().getClassLoader();
        Class<?>[] interfaces = target.getClass().getInterfaces();
        InvocationHandler invocationHandler = new InvocationHandler() {
            @Override
            public Object invoke(Object proxy, Method method, Object[] args) throws Throwable {
                /**
                 * proxy：代理对象
                 * method：代理对象需要实现的方法，即其中需要重写的方法
                 * args：method所对应方法的参数
                 */
                Object result = null;
                try {
                    System.out.println("[动态代理][日志] "+method.getName()+"，参数："+ Arrays.toString(args));
                    result = method.invoke(target, args);
                    System.out.println("[动态代理][日志] "+method.getName()+"，结果："+ result);
                } catch (Exception e) {
                    e.printStackTrace();
                    System.out.println("[动态代理][日志] "+method.getName()+"，异常："+e.getMessage());
                } finally {
                    System.out.println("[动态代理][日志] "+method.getName()+"，方法执行完毕");
                }
                return result;
            }
        };

        return Proxy.newProxyInstance(classLoader, interfaces, invocationHandler);
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
说明：

动态代理需要使用Proxy.newProxyInstance()方法
需要设置代理对象实现目标对象的方法过程
步骤二：演示

@Test
public void testDynamicProxy(){
    ProxyFactory factory = new ProxyFactory(new CalculatorLogImpl());
    Calculator proxy = (Calculator) factory.getProxy();
    proxy.div(1,0);
    //proxy.div(1,1);
}
1
2
3
4
5
6
7
6.3切入点表达式
​ 在 AOP 中，切入点表达式指定了哪些方法需要被织入增强逻辑。它是一个表达式，用于匹配目标对象中的方法，并提供切入点的精确定义



说明：

​ 在切入点表达式语法中，用*号代替“权限修饰符”和“返回值”部分表示“权限修饰符”和“返回值”不限

6.4基于注解的AOP
笔记小结：

概述：在Java类、方法、参数等上添加注解的方式来实现切面的定义和应用

基本用例：

步骤一：导入依赖

步骤二：创建切面类（需要选择通知方式）

步骤三：添加xml配置文件

通知方式：

前置通知：@Before
异常通知：@AfterThrowing
返回通知：@AfterReturning
后置通知：@After
环绕通知：@Around
获取通知信息

获取连接点：在方法中使用JoinPoint即可获取连接点信息

public void beforeMethod(JoinPoint joinPoint)
1
获取目标对象的返回值：在目标对象的返回通知上添加returning属性

@AfterReturning(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", returning = "result")
public void afterReturningMethod(JoinPoint joinPoint, Object result)
1
2
获取目标对象的异常：在目标对象的异常通知上添加throwing属性

@AfterThrowing(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", throwing = "ex")
public void afterThrowingMethod(JoinPoint joinPoint, Throwable ex)
1
2
重用切入点表达式

声明：在空参、空方法体、空返回值的方法上使用**@Pointcut**注解

@Pointcut("execution(* com.atguigu.aop.annotation.*.*(..))")
public void pointCut(){}
1
2
同切面使用：在同一切面中直接引用即可

@Before("pointCut()")
1
不同切面使用：在不同切面中

@Before("com.atguigu.aop.CommonPointCut.pointCut()")
1
6.4.1概述
​ 基于注解的AOP是一种AOP的实现方式，它通过在Java类、方法、参数等上添加注解的方式来实现切面的定义和应用，相比于传统的XML配置方式更加便捷和灵活

6.4.2基本用例-注解实现AOP
步骤一：导入依赖

 <!--spring aop依赖-->
    <dependency>
        <groupId>org.springframework</groupId>
        <artifactId>spring-aop</artifactId>
        <version>6.0.2</version>
    </dependency>
    <!--spring aspects依赖-->
    <dependency>
        <groupId>org.springframework</groupId>
        <artifactId>spring-aspects</artifactId>
        <version>6.0.2</version>
    </dependency>
1
2
3
4
5
6
7
8
9
10
11
12
步骤二：创建接口以及实现类

1.接口

public interface Calculator {
    int add(int i, int j); 
}
1
2
3
2.实现类

@Component
public class CalculatorImpl implements Calculator {

    @Override
    public int add(int i, int j) {
        int result = i + j;
        System.out.println("方法内部 result = " + result);
        return result;
    }
}
1
2
3
4
5
6
7
8
9
10
说明：

​ 此实现类，也需要添加@Component注解，便于Spring容器进行管理

步骤三：创建切面类

@Aspect
@Component
public class LogAspect {
    // 前置通知
    // 异常通知
    // 返回通知
    // 后置通知
    // 环绕通知
    ……
}
1
2
3
4
5
6
7
8
9
10
注意：

​ 此处需要配置切面类的通知方式！

说明：

@Aspect表示这个类是一个切面类
@Component注解保证这个切面类能够放入IOC容器
步骤四：配置Spring配置文件

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:context="http://www.springframework.org/schema/context"
       xmlns:aop="http://www.springframework.org/schema/aop"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
       http://www.springframework.org/schema/beans/spring-beans.xsd
       http://www.springframework.org/schema/context
       http://www.springframework.org/schema/context/spring-context.xsd
       http://www.springframework.org/schema/aop
       http://www.springframework.org/schema/aop/spring-aop.xsd">
    <!--
        基于注解的AOP的实现：
        1、将目标对象和切面交给IOC容器管理（注解+扫描）
        2、开启AspectJ的自动代理，为目标对象自动生成代理
        3、将切面类通过注解@Aspect标识
    -->
    <context:component-scan base-package="com.atguigu.aop.annotation"></context:component-scan>

    <aop:aspectj-autoproxy />
</beans>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
补充：

​ 当学习了SpringBoot后，通过SpringBoot来实现AOP，可省略此文件。因为SpringBoot以实现包扫描和切面标识

步骤五：演示

@Test
public void testAdd(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("beans.xml");
    Calculator calculator = ac.getBean( Calculator.class);
    int add = calculator.add(1, 1);
}
1
2
3
4
5
6
说明：

​

6.4.3通知方式
6.4.3.1前置通知
使用@Before注解标识，在被代理的目标方法前执行

@Before("execution(public int com.atguigu.aop.annotation.CalculatorImpl.*(..))")
public void beforeMethod(JoinPoint joinPoint){
    // getSignature（）获取连接点签名，getName（）获取连接点名称
    String methodName = joinPoint.getSignature().getName();
    String args = Arrays.toString(joinPoint.getArgs());
    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);
}
1
2
3
4
5
6
7
说明：

@Before注解内为切入点表达式
JoinPoint 是指程序执行过程中明确的点，比如方法的调用或异常的处理。JoinPoint 提供了一个可供切面通知获取方法的关键信息的方式
6.4.3.2异常通知
使用@AfterThrowing注解标识，在被代理的目标方法异常结束后执行

@AfterThrowing(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", throwing = "ex")
public void afterThrowingMethod(JoinPoint joinPoint, Throwable ex){
    String methodName = joinPoint.getSignature().getName();
    System.out.println("Logger-->异常通知，方法名："+methodName+"，异常："+ex);
}

1
2
3
4
5
6
说明：

​ @AfterThrowing注解内为切入点表达式

6.4.3.3返回通知
使用@AfterReturning注解标识，在被代理的目标方法成功结束后执行

@AfterReturning(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", returning = "result")
public void afterReturningMethod(JoinPoint joinPoint, Object result){
    String methodName = joinPoint.getSignature().getName();
    System.out.println("Logger-->返回通知，方法名："+methodName+"，结果："+result);
}

1
2
3
4
5
6
说明：

​ @AfterReturning注解内为切入点表达式

6.4.3.4后置通知
使用@After注解标识，在被代理的目标方法最终结束后执行

  @After("execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))")
    public void afterMethod(JoinPoint joinPoint){
        String methodName = joinPoint.getSignature().getName();
        System.out.println("Logger-->后置通知，方法名："+methodName);
    }

1
2
3
4
5
6
说明：

​ @After注解内为切入点表达式

6.4.3.5环绕通知
使用@Around注解标识，使用try…catch…finally结构围绕整个被代理的目标方法，包括上面四种通知对应的所有位置

@Around("execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))")
public Object aroundMethod(ProceedingJoinPoint joinPoint){
    String methodName = joinPoint.getSignature().getName();
    String args = Arrays.toString(joinPoint.getArgs());
    Object result = null;
    try {
        System.out.println("环绕通知-->目标对象方法执行之前");
        //目标对象（连接点）方法的执行
        result = joinPoint.proceed();
        System.out.println("环绕通知-->目标对象方法返回值之后");
    } catch (Throwable throwable) {
        throwable.printStackTrace();
        System.out.println("环绕通知-->目标对象方法出现异常时");
    } finally {
        System.out.println("环绕通知-->目标对象方法执行完毕");
    }
    return result;
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
说明：

@Around注解内为切入点表达式
ProceedingJoinPoint 继承自 JoinPoint 接口，是用于环绕通知的特殊类型的 JoinPoint，它可以用于在通知中控制目标方法的执行。在环绕通知中，ProceedingJoinPoint 提供了一个 proceed() 方法，该方法会执行目标方法，并返回其结果。
6.4.4获取通知信息
6.4.4.1获取连接点信息
在任何通知方式中，获取连接点信息可以在通知方法的参数位置设置JoinPoint类型的形参

@Before("execution(public int com.atguigu.aop.annotation.CalculatorImpl.*(..))")
public void beforeMethod(JoinPoint joinPoint){
    //获取连接点的签名信息
    String methodName = joinPoint.getSignature().getName();
    //获取目标方法到的实参信息
    String args = Arrays.toString(joinPoint.getArgs());
    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);
}
1
2
3
4
5
6
7
8
6.4.4.2获取目标方法的返回值
@AfterReturning中的属性returning，用来将通知方法的某个形参，接收目标方法的返回值

@AfterReturning(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", returning = "result")
public void afterReturningMethod(JoinPoint joinPoint, Object result){
    String methodName = joinPoint.getSignature().getName();
    System.out.println("Logger-->返回通知，方法名："+methodName+"，结果："+result);
}
1
2
3
4
5
6.4.4.3获取目标方法的异常
@AfterThrowing中的属性throwing，用来将通知方法的某个形参，接收目标方法的异常

@AfterThrowing(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", throwing = "ex")
public void afterThrowingMethod(JoinPoint joinPoint, Throwable ex){
    String methodName = joinPoint.getSignature().getName();
    System.out.println("Logger-->异常通知，方法名："+methodName+"，异常："+ex);
}
1
2
3
4
5
6.4.5重用切入点表达式
说明：

​ 切入点表达式可参考本节面向切面：AOP中的概述部分

简化切入点的书写

6.4.5.1声明
@Pointcut("execution(* com.atguigu.aop.annotation.*.*(..))")
public void pointCut(){}
1
2
6.4.5.2同切面使用
@Before("pointCut()")
public void beforeMethod(JoinPoint joinPoint){
    String methodName = joinPoint.getSignature().getName();
    String args = Arrays.toString(joinPoint.getArgs());
    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);
}
1
2
3
4
5
6
6.4.5.3不同切面使用
@Before("com.atguigu.aop.CommonPointCut.pointCut()")
public void beforeMethod(JoinPoint joinPoint){
    String methodName = joinPoint.getSignature().getName();
    String args = Arrays.toString(joinPoint.getArgs());
    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);
}
1
2
3
4
5
6
6.5基于XML的AOP（了解）
<context:component-scan base-package="com.atguigu.aop.xml"></context:component-scan>

<aop:config>
    <!--配置切面类-->
    <aop:aspect ref="loggerAspect">
        <aop:pointcut id="pointCut" 
                   expression="execution(* com.atguigu.aop.xml.CalculatorImpl.*(..))"/>
        <aop:before method="beforeMethod" pointcut-ref="pointCut"></aop:before>
        <aop:after method="afterMethod" pointcut-ref="pointCut"></aop:after>
        <aop:after-returning method="afterReturningMethod" returning="result" pointcut-ref="pointCut"></aop:after-returning>
        <aop:after-throwing method="afterThrowingMethod" throwing="ex" pointcut-ref="pointCut"></aop:after-throwing>
        <aop:around method="aroundMethod" pointcut-ref="pointCut"></aop:around>
    </aop:aspect>
</aop:config>
1
2
3
4
5
6
7
8
9
10
11
12
13
14
知识加油站
1.自动装配和依赖注入的区别与联系
​ 依赖注入（Dependency Injection） 是一种设计模式，旨在通过将依赖关系从一个对象传递给另一个对象，来实现对象之间的解耦。在Spring中，依赖注入通过容器来管理和传递对象之间的依赖关系，而不是由对象自身来创建或管理它们的依赖。这可以通过构造函数注入、Setter方法注入或字段注入等方式来实现

​ 自动装配（Autowired） 是Spring Framework提供的一种依赖注入的方式，用于自动将合适的依赖注入到相应的位置，无需手动指定每个依赖的注入方式。通过使用@Autowired注解，Spring会自动在容器中查找匹配的依赖，并将其注入到需要的位置

总结：

自动装配是Spring框架的特性，用于自动连接应用程序中的组件。
依赖注入是自动装配的一种具体实现方式，使用**@Autowired注解来标识需要自动注入**的属性、构造函数或方法参数。
2.依赖注入的两种方式
依赖注入（Dependency Injection）有两种常见的方式：

构造函数注入（Constructor Injection）：通过构造函数来注入依赖对象。在目标类的构造函数中声明参数，并在创建目标对象时通过构造函数传入依赖对象。这种方式可以保证依赖对象在目标对象创建时就被传入，从而确保了目标对象的完整性和一致性。
Setter方法注入（Setter Injection）：通过Setter方法来注入依赖对象。在目标类中定义对应的Setter方法，并在方法中接收依赖对象作为参数，通过调用Setter方法来注入依赖对象。这种方式可以在目标对象创建后动态地设置依赖对象，灵活性较高。
————————————————

                            版权声明：本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。
                        
原文链接：https://blog.csdn.net/D_boj/article/details/132286492>)](<文章目录
1.概述
1.1定义
1.2作用
1.3简介
1.4狭义和广义
1.5模块组成
1.5.1Spring Core（核心容器）
1.5.2Spring AOP（面向切面编程）
1.5.3Spring Data Access（数据访问）
1.5.4Spring Web（应用程序）
1.5.5Spring Message（消息传递）
1.5.6Spring test（测试）
1.6Spring Framework（框架）
1.6.1概述
1.6.2作用
1.6.3特点
1.7 特点
2.基本用例-Spring框架基本使用
3.原理
4.启用日志框架
4.1概述
4.2组成
4.3基本用例-Log4j2基本使用
5.容器：IoC（重点）
5.1概述
5.1.1定义
5.1.2简介
5.1.3作用
5.1.4依赖注入
5.1.4.1定义
5.1.4.2作用
5.1.4.3实现方式
5.1.5实现
5.2基于XML管理Bean（了解）
5.2.1获取Bean的方式
5.2.1.1根据ID获取Bean
5.2.1.2根据类型获取Bean
5.2.1.3根据Id和类型获取Bean
5.2.2依赖注入
5.2.2.1根据setter注入
5.2.2.2根据构造器注入
5.2.3特殊值处理
5.2.3.1字面量赋值
5.2.3.2null值
5.2.3.3xml实体
5.2.3.4CDATA节
5.2.4注入对象类型属性值
5.2.4.1引用外部Bean
5.2.4.2引用内部Bean
5.2.4.3级联属性赋值
5.2.5注入数组类型属性值
5.2.6注入集合类型属性值
5.2.6.1注入List集合类型属性值
5.2.6.2注入Map集合类型属性值
5.2.6.2注入引用集合类型属性值
5.2.7引入P命名空间属性值
5.2.8引入外部属性文件
5.2.9引入Bean的作用域
5.2.10Bean的生命周期
5.2.11引入FactoryBean属性值
5.2.12引入xml自动装配
5.3基于注解管理Bean（重点）
5.3.1概述
5.3.1.1简介
5.3.1.2步骤
5.3.1.3使用注解
5.3.2开启组件扫描
5.3.2.1概述
5.3.2.2基本用例-实现组件扫描
5.3.2.3指定要排除的组件
5.3.2.4仅扫描指定组件
5.3.2使用注解定义Bean
5.3.3使用@Autowired注入
5.3.3.1概述
5.3.3.2属性注入
5.3.3.3set注入
5.3.3.4构造方法注入
5.3.3.5形参注入
5.3.3.6无注解注入
5.3.3.7联合@Qualifier注解注入
5.3.4使用@Resource注入
5.3.4.1概述
5.3.4.2Name注入
5.3.4.3未知Name注入
5.3.4.4类型注入
5.3.5全注解开发
5.3.5.1概述
5.3.5.2基本用例-全注解开发实现
5.4原理
6.面向切面：AOP (重点)
6.1概述
6.1.1定义
6.1.2作用
6.1.3横切关注点
6.1.4通知（增强）
6.1.5切面
6.1.6目标
6.1.7代理
6.1.8连接点
6.1.9切入点
6.2代理模式
6.2.1概述
6.2.2静态代理
6.2.3动态代理
6.2.3.1概述
6.2.3.1.1定义
6.2.3.1.2分类
6.2.3.2基本用例-实现动态代理
6.3切入点表达式
6.4基于注解的AOP
6.4.1概述
6.4.2基本用例-注解实现AOP
6.4.3通知方式
6.4.3.1前置通知
6.4.3.2异常通知
6.4.3.3返回通知
6.4.3.4后置通知
6.4.3.5环绕通知
6.4.4获取通知信息
6.4.4.1获取连接点信息
6.4.4.2获取目标方法的返回值
6.4.4.3获取目标方法的异常
6.4.5重用切入点表达式
6.4.5.1声明
6.4.5.2同切面使用
6.4.5.3不同切面使用
6.5基于XML的AOP（了解）
知识加油站
1.自动装配和依赖注入的区别与联系
2.依赖注入的两种方式
1.概述
笔记小结：

含义：Spring 是一款主流的 Java EE 轻量级开源框架，包含Spring MVC、Spring Boot、Spring Cloud等
作用：简化 Java 企业级应用的开发难度和开发周期，提供了整合其他技术和框架的能力
简介：核心功能是控制反转(IoC)和面向切面(AOP)
组成：
Spring Core（核心容器）
Spring AOP（面向切面编程）
Spring **Data Access（**数据访问）
Spring Web（应用程序）
Spring Message（消息传递）
Spring test（测试）
Spring Framework（框架）
概述：Spring Framework是Spring项目的核心框架
作用：Spring Framework实现IOC容器和AOP技术的功能模块
特点：
非侵入式
控制反转
面向切面编程
容器
组件化
特点：
轻：框架轻量级，不依赖其余Spring的对象
控制反转（IOC）：实现了对象之间的松耦合
面向切面（AOP）：分离应用的业务逻辑与系统级服务
容器：Spring包含并管理应用对象的配置和生命周期
1.1定义
​ Spring 是一款主流的 Java EE 轻量级开源框架 ，由于其轻便、易用和高效，被广泛应用于企业级Java应用开发中。

​ Spring包含了很多子框架和扩展，如Spring MVC、Spring Boot、Spring Cloud等。

​ Spring的主要特点是IOC容器和AOP技术，它们使得Java应用的开发和管理更加简单和高效。

1.2作用
​ Spring 目的是用于简化 Java 企业级应用的开发难度和开发周期。Spring 框架除了自己提供功能外，还提供整合其他技术和框架的能力

1.3简介
​ 自 2004 年 4 月，Spring 1.0 版本正式发布以来，Spring 已经步入到了第 6 个大版本，也就是 Spring 6。



说明：

​ 参考链接：Spring Framework

Spring是一个轻量级的控制反转(IoC)和面向切面(AOP)的容器框架。
Spring最初的出现是为了解决EJB臃肿的设计，以及难以测试等问题。
Spring为简化开发而生，让程序员只需关注核心业务的实现，尽可能的不再关注非业务逻辑代码（事务控制，安全日志等）。
1.4狭义和广义
广义的 Spring：Spring 技术栈
​ 广义上的 Spring 泛指以 Spring Framework 为核心的 Spring 技术栈。

​ 经过十多年的发展，Spring 已经不再是一个单纯的应用框架，而是逐渐发展成为一个由多个不同子项目（模块）组成的成熟技术，例如 Spring Framework、Spring MVC、SpringBoot、Spring Cloud、Spring Data、Spring Security 等，其中 Spring Framework 是其他子项目的基础。

​ 这些子项目涵盖了从企业级应用开发到云计算等各方面的内容，能够帮助开发人员解决软件发展过程中不断产生的各种实际问题，给开发人员带来了更好的开发体验。

狭义的 Spring：Spring Framework
​ 狭义的 Spring 特指 Spring Framework，通常我们将它称为 Spring 框架。

​ Spring 框架是一个分层的、面向切面的 Java 应用程序的一站式轻量级解决方案，它是 Spring 技术栈的核心和基础，是为了解决企业级应用开发的复杂性而创建的。

Spring 有两个最核心模块： IoC 和 AOP。

IoC：Inverse of Control 的简写，译为“控制反转”，指把创建对象过程交给 Spring 进行管理。
AOP：Aspect Oriented Programming 的简写，译为“面向切面编程”。AOP 用来封装多个类的公共行为，将那些与业务无关，却为业务模块所共同调用的逻辑封装起来，减少系统的重复代码，降低模块间的耦合度。另外，AOP 还解决一些系统层面上的问题，比如日志、事务、权限等。
1.5模块组成


说明：

​ 上图中包含了 Spring 框架的所有模块，这些模块可以满足一切企业级应用开发的需求，在开发过程中可以根据需求有选择性地使用所需要的模块。下面分别对这些模块的作用进行简单介绍。

1.5.1Spring Core（核心容器）
​ spring core提供了IOC,DI,Bean配置装载创建的核心实现。核心概念： Beans、BeanFactory、BeanDefinitions、ApplicationContext。

spring-core ：IOC和DI的基本实现

spring-beans：BeanFactory和Bean的装配管理(BeanFactory)

spring-context：Spring context上下文，即IOC容器(AppliactionContext)

spring-expression：spring表达式语言

1.5.2Spring AOP（面向切面编程）
spring-aop：面向切面编程的应用模块，整合ASM，CGLib，JDK Proxy
spring-aspects：集成AspectJ，AOP应用框架
spring-instrument：动态Class Loading模块
1.5.3Spring Data Access（数据访问）
spring-jdbc：spring对JDBC的封装，用于简化jdbc操作
spring-orm：java对象与数据库数据的映射框架
spring-oxm：对象与xml文件的映射框架
spring-jms： Spring对Java Message Service(java消息服务)的封装，用于服务之间相互通信
spring-tx：spring jdbc事务管理
1.5.4Spring Web（应用程序）
spring-web：最基础的web支持，建立于spring-context之上，通过servlet或listener来初始化IOC容器
spring-webmvc：实现web mvc
spring-websocket：与前端的全双工通信协议
spring-webflux：Spring 5.0提供的，用于取代传统java servlet，非阻塞式Reactive Web框架，异步，非阻塞，事件驱动的服务
1.5.5Spring Message（消息传递）
Spring-messaging：spring 4.0提供的，为Spring集成一些基础的报文传送服务
1.5.6Spring test（测试）
spring-test：集成测试支持，主要是对junit的封装
1.6Spring Framework（框架）
1.6.1概述
​ Spring Framework是Spring项目的核心框架，而Spring是整个Spring项目的总称，包括了Spring Framework和其他相关的子项目和扩展



1.6.2作用
​ Spring Framework实现IOC容器和AOP技术的功能模块

​ Spring Framework包含了许多模块，如Core模块、Beans模块、Context模块、AOP模块、Web模块等，每个模块都提供了不同的功能，可以灵活地选择使用。Spring Framework的目标是为了简化企业级Java开发，提高开发效率和质量。

1.6.3特点
非侵入式：使用 Spring Framework 开发应用程序时，Spring 对应用程序本身的结构影响非常小。对领域模型可以做到零污染；对功能性组件也只需要使用几个简单的注解进行标记，完全不会破坏原有结构，反而能将组件结构进一步简化。这就使得基于 Spring Framework 开发应用程序时结构清晰、简洁优雅。

控制反转：IoC——Inversion of Control，翻转资源获取方向。把自己创建资源、向环境索取资源变成环境将资源准备好，我们享受资源注入。

面向切面编程：AOP——Aspect Oriented Programming，在不修改源代码的基础上增强代码功能。

容器：Spring IoC 是一个容器，因为它包含并且管理组件对象的生命周期。组件享受到了容器化的管理，替程序员屏蔽了组件创建过程中的大量细节，极大的降低了使用门槛，大幅度提高了开发效率。

组件化：Spring 实现了使用简单的组件配置组合成一个复杂的应用。在 Spring 中可以使用 XML 和 Java 注解组合这些对象。这使得我们可以基于一个个功能明确、边界清晰的组件有条不紊的搭建超大型复杂应用系统。

一站式：在 IoC 和 AOP 的基础上可以整合各种企业应用的开源框架和优秀的第三方类库。而且 Spring 旗下的项目已经覆盖了广泛领域，很多方面的功能性需求可以在 Spring Framework 的基础上全部使用 Spring 来实现。

1.7 特点
轻
从大小与开销两方面而言Spring都是轻量的。完整的Spring框架可以在一个大小只有1MB多的JAR文件里发布。并且Spring所需的处理开销也是微不足道的。
Spring是非侵入式的：Spring应用中的对象不依赖于Spring的特定类。
控制反转
Spring通过一种称作控制反转（IoC）的技术促进了松耦合。当应用了IoC，一个对象依赖的其它对象会通过被动的方式传递进来，而不是这个对象自己创建或者查找依赖对象。你可以认为IoC与JNDI相反——不是对象从容器中查找依赖，而是容器在对象初始化时不等对象请求就主动将依赖传递给它。
面向切面
Spring提供了面向切面编程的丰富支持，允许通过分离应用的业务逻辑与系统级服务（例如审计（auditing）和事务（transaction）管理）进行内聚性的开发。应用对象只实现它们应该做的——完成业务逻辑——仅此而已。它们并不负责（甚至是意识）其它的系统级关注点，例如日志或事务支持。
容器
Spring包含并管理应用对象的配置和生命周期，在这个意义上它是一种容器，你可以配置你的每个bean如何被创建——基于一个可配置原型（prototype），你的bean可以创建一个单独的实例或者每次需要时都生成一个新的实例——以及它们是如何相互关联的。然而，Spring不应该被混同于传统的重量级的EJB容器，它们经常是庞大与笨重的，难以使用。
框架
Spring可以将简单的组件配置、组合成为复杂的应用。在Spring中，应用对象被声明式地组合，典型地是在一个XML文件里。Spring也提供了很多基础功能（事务管理、持久化框架集成等等），将应用逻辑的开发留给了你。
说明：

​ 所有Spring的这些特征使你能够编写更干净、更可管理、并且更易于测试的代码。它们也为Spring中的各种模块提供了基础支持。

Spring6要求JDK最低版本是JDK17


2.基本用例-Spring框架基本使用
说明：

​ 本基本用例演示，通过XML方式，实现Bean的自动注入

补充：环境

JDK：Java17+（Spring6要求JDK最低版本是Java17）

Maven：3.6+

Spring：6.0.2

步骤一：构建模块

通过Idea开发工具，创建空项目后创建子模块


说明：

​ 在空项目中，创建子模块

步骤二：导入依赖

修改模块的pom.xml文件
%3Cdependencies%3E
    <!--spring context依赖-->
    <!--当你引入Spring Context依赖之后，表示将Spring的基础依赖引入了-->
    <dependency>
        <groupId>org.springframework</groupId>
        <artifactId>spring-context</artifactId>
        <version>6.0.2</version>
    </dependency>

    <!--junit5测试-->
    <!--此依赖可选，主要便于junit进行测试使用-->
    <dependency>
        <groupId>org.junit.jupiter</groupId>
        <artifactId>junit-jupiter-api</artifactId>
        <version>5.3.1</version>
    </dependency>
</dependencies>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
说明：

​ 在pom.xml文件中，添加如上依赖

补充：

添加完成后，可在IDEA工具中的最右侧点击Maven进行查看


步骤三：创建实体

package org.example.entity;

public class User {
    public void add() {
        System.out.println("add……");
    }
}

1
2
3
4
5
6
7
8
说明：

​ 在org.example.entity包下，创建User实体

步骤四：创建配置文件

在模块的resources目录下，创建beans.xml文件
说明：

​ 创建beans.xml文件，是为了完成通过xml的方式实现依赖的自动注入

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd">

    <!--id是该bean的唯一标识符，在整个应用程序上下文中用于获取该bean实例-->
    <!--class是该bean所属的Java类的全限定名（包括包名），它告诉Spring需要实例化哪个类-->
    <bean id="user" class="org.example.entity.User"/>
</beans>
1
2
3
4
5
6
7
8
9
说明：

在beans,xml文件中，有bean标签
在beans,xml文件中，bean标签有Id属性，与class属性
步骤五：演示

在模块中的test.java包下，创建UserTest类
public class UserTest {
    @Test
    void newTest() {
        ApplicationContext applicationContext = new ClassPathXmlApplicationContext("beans.xml");
        User user = (User) applicationContext.getBean("user");
        user.add(); // add……
    }
}
1
2
3
4
5
6
7
8
补充：

@Test 是 JUnit 框架中的一个注解，表示该方法是一个测试方法，会被 JUnit 框架执行。

3.原理
笔记小结：通过XML方式，实现Bean的自动注入的基本用例原理

创建对象时，会调用无参构造方法
Spring 是通过反射机制调用无参构造方法创建对象
Spring 创建的对象（Bean对象），最终存储在Spring容器中
1.创建对象时，会调用无参构造方法

public class HelloWorld {
    public HelloWorld() {
        System.out.println("无参数构造方法执行");
    }
    public void sayHello(){
        System.out.println("helloworld");
    }
}
1
2
3
4
5
6
7
8
说明：



2.Spring 是通过反射机制调用无参构造方法创建对象

// dom4j解析beans.xml文件，从中获取class属性值，类的全类名
// 通过反射机制调用无参数构造方法创建对象
Class clazz = Class.forName("com.atguigu.spring6.bean.HelloWorld");
//Object obj = clazz.newInstance();
Object object = clazz.getDeclaredConstructor().newInstance();
1
2
3
4
5
3.Spring 创建的对象（Bean对象），最终存储在Spring容器中

private final Map<String, BeanDefinition> beanDefinitionMap = new ConcurrentHashMap<>(256);
1
说明：

Spring容器底层就是一个map集合
存储bean的map在DefaultListableBeanFactory类中
Spring容器加载到Bean类时 , 会把这个类的描述信息, 以包名加类名的方式存到beanDefinitionMap 中
Map<String,BeanDefinition> , 其中 String是Key , 默认是类名首字母小写 。BeanDefinition , 存的是类的定义(描述信息) , 我们通常叫BeanDefinition接口为 : bean的定义对象。
4.启用日志框架
笔记小结：

概述：Log4j2是一个开源的Java日志框架，帮助Java开发人员在应用程序中实现灵活和可配置的日志记录

组成：

日志信息的优先级：TRACE < DEBUG < INFO < WARN < ERROR < FATAL
日志信息的输出目的地：控制台或者本地文件
日志信息的输出格式：日志信息的显示内容
基本用例：

导入依赖：
<!--log4j2的依赖-->
<dependency>
  <groupId>org.apache.logging.log4j</groupId>
  <artifactId>log4j-core</artifactId>
  <version>2.19.0</version>
</dependency>
<dependency>
  <groupId>org.apache.logging.log4j</groupId>
  <artifactId>log4j-slf4j2-impl</artifactId>
  <version>2.19.0</version>
</dependency>
1
2
3
4
5
6
7
8
9
10
11
创建日志配置文件：建议复制根据需求修改

使用日志

private Logger logger = LoggerFactory.getLogger(HelloWorldTest.class);
……
logger.info("执行成功");
1
2
3
结果：



4.1概述
​ Log4j2是一个开源的Java日志框架，是Log4j的升级版。它可以帮助Java开发人员在应用程序中实现灵活和可配置的日志记录，支持异步日志记录、多线程安全等特性

4.2组成
日志信息的优先级，日志信息的优先级从高到低有TRACE < DEBUG < INFO < WARN < ERROR < FATAL

说明：

TRACE：追踪，是最低的日志级别，相当于追踪程序的执行
DEBUG：调试，一般在开发中，都将其设置为最低的日志级别
INFO：信息，输出重要的信息，使用较多
WARN：警告，输出警告的信息
ERROR：错误，输出错误信息
FATAL：严重错误
日志信息的输出目的地，日志信息的输出目的地指定了日志将打印到控制台还是文件中；

日志信息的输出格式，而输出格式则控制了日志信息的显示内容。

4.3基本用例-Log4j2基本使用
步骤一：引入Log4j2依赖

修改模块中的pom.xml文件
<!--log4j2的依赖-->
<dependency>
    <groupId>org.apache.logging.log4j</groupId>
    <artifactId>log4j-core</artifactId>
    <version>2.19.0</version>
</dependency>
<dependency>
    <groupId>org.apache.logging.log4j</groupId>
    <artifactId>log4j-slf4j2-impl</artifactId>
    <version>2.19.0</version>
</dependency>
1
2
3
4
5
6
7
8
9
10
11
说明：

​ log4j的Maven使用光有核心core依赖不够，还需要有实现impl依赖

步骤二：创建日志配置文件

在模块文件路径在resource的根路径下，配置文件名为log4j2.xml
<?xml version="1.0" encoding="UTF-8"?>
<configuration>
    <loggers>
        <!--
            level指定日志级别，从低到高的优先级：
                TRACE < DEBUG < INFO < WARN < ERROR < FATAL
                trace：追踪，是最低的日志级别，相当于追踪程序的执行
                debug：调试，一般在开发中，都将其设置为最低的日志级别
                info：信息，输出重要的信息，使用较多
                warn：警告，输出警告的信息
                error：错误，输出错误信息
                fatal：严重错误
        -->
        <root level="DEBUG">
            <appender-ref ref="spring6log"/>
            <appender-ref ref="RollingFile"/>
            <appender-ref ref="log"/>
        </root>
    </loggers>

    <appenders>
        <!--输出日志信息到控制台-->
        <console name="spring6log" target="SYSTEM_OUT">
            <!--控制日志输出的格式-->
            <PatternLayout pattern="%d{yyyy-MM-dd HH:mm:ss SSS} [%t] %-3level %logger{1024} - %msg%n"/>
        </console>

        <!--文件会打印出所有信息，这个log每次运行程序会自动清空，由append属性决定，适合临时测试用-->
        <File name="log" fileName="d:/spring6_log/test.log" append="false">
            <PatternLayout pattern="%d{HH:mm:ss.SSS} %-5level %class{36} %L %M - %msg%xEx%n"/>
        </File>

        <!-- 这个会打印出所有的信息，
            每次大小超过size，
            则这size大小的日志会自动存入按年份-月份建立的文件夹下面并进行压缩，
            作为存档-->
        <RollingFile name="RollingFile" fileName="d:/spring6_log/app.log"
                     filePattern="log/$${date:yyyy-MM}/app-%d{MM-dd-yyyy}-%i.log.gz">
            <PatternLayout pattern="%d{yyyy-MM-dd 'at' HH:mm:ss z} %-5level %class{36} %L %M - %msg%xEx%n"/>
            <SizeBasedTriggeringPolicy size="50MB"/>
            <!-- DefaultRolloverStrategy属性如不设置，
            则默认为最多同一文件夹下7个文件，这里设置了20 -->
            <DefaultRolloverStrategy max="20"/>
        </RollingFile>
    </appenders>
</configuration>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
步骤三：日常使用

在日常中，只用log4j2，此处创建HelloWorldTest使用
public class HelloWorldTest {

    // 1.通过日志工程获取日志对象记录器
    private Logger logger = LoggerFactory.getLogger(HelloWorldTest.class);
 
    @Test
    public void testHelloWorld(){
        ApplicationContext ac = new ClassPathXmlApplicationContext("beans.xml");
        HelloWorld helloworld = (HelloWorld) ac.getBean("helloWorld");
        helloworld.sayHello();
        // 2.记录日志
        logger.info("执行成功");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
说明：

​ 创建日志记录器

步骤四：演示



说明：

​ 当完成以上步骤后，运行，日志就会输出在控制台

5.容器：IoC（重点）
笔记小结：见各个小节

5.1概述
笔记小结：

定义：IoC (Inversion of Control)，即控制反转，是一种设计模式或者说设计思想
简介：Spring 通过 IoC 容器来管理所有 Java 对象的实例化和初始化，控制对象与对象之间的依赖关系
作用：通过容器来管理对象的创建、销毁、依赖注入等操作，而应用程序本身只需要使用这些对象即可
依赖注入:
含义：以解耦对象之间的依赖关系
作用：Spring通过依赖注入的方式来完成Bean管理的。换句话说，依赖注入，依赖注入实现了控制反转的思想
实现方式（重点）：
setter注入
构造注入
实现接口以及常用类：
BeanFactory接口：面向 Spring 本身，不提供给开发人员使用
ApplicationContext接口：面向 Spring 的使用者，几乎所有场合（创建、管理Bean实例，支持国际化、资源访问、消息传递）都适用
常用类：
FileSystemXmlApplicationContext：通过文件系统路径读取 XML 格式的配置文件创建 IOC 容器对象
ClassPathXmlApplicationContext：通过读取类路径下的 XML 格式的配置文件创建 IOC 容器对象
5.1.1定义
​ IoC (Inversion of Control)，即控制反转，是一种设计模式或者说设计思想，它是面向对象编程中的一种概念，用来描述对象之间的依赖关系，指导我们如何设计出松耦合、更优良的程序。

5.1.2简介
​ Spring 通过 IoC 容器来管理所有 Java 对象的实例化和初始化，控制对象与对象之间的依赖关系。我们将由 IoC 容器管理的 Java 对象称为 Spring Bean，它与使用关键字 new 创建的 Java 对象没有任何区别。

5.1.3作用
​ 在 IoC 模式中，控制权从程序代码中转移到了容器中，即通过容器来管理对象的创建、销毁、依赖注入等操作，而应用程序本身只需要使用这些对象即可。这样，应用程序就不需要自己管理对象之间的依赖关系，而是由容器来管理，从而实现了代码的解耦和更好的可维护性，提高程序扩展力。

说明：

将对象的创建权利交出去，交给第三方容器负责
将对象和对象之间关系的维护权交出去，交给第三方容器负责
5.1.4依赖注入
5.1.4.1定义
​ 依赖注入（Dependency Injection，DI）是一种设计模式，其主要思想是在程序运行的过程中，通过外部容器（如Spring容器）动态地将依赖对象注入到程序中，以解耦对象之间的依赖关系，从而提高程序的灵活性、可维护性和可测试性。

5.1.4.2作用
​ **Spring通过依赖注入的方式来完成Bean管理的。**换句话说，依赖注入，依赖注入实现了控制反转的思想。依赖指的是对象和对象之间的关联关系。注入指的是一种数据传递行为，通过注入行为来让对象和对象产生关系。

补充：

​ Bean管理说的是：Bean对象的创建，以及Bean对象中属性的赋值（或者叫做Bean对象之间关系的维护）。

5.1.4.3实现方式
第一种：set注入
第二种：构造注入
5.1.5实现
​ Spring 的框架中，IoC 容器是通过 BeanFactory 和 ApplicationContext 接口实现的。BeanFactory 接口是 Spring 框架最底层的接口，提供了基本的 IoC 功能；ApplicationContext 接口是 BeanFactory 接口的子接口，提供了更高级的特性和功能，如 AOP、国际化、事件驱动等。其中BeanFactory 接口，最重要的方法是getBean()方法，用于从容器中获取对象。

​ Spring 的 IoC 容器就是 IoC思想的一个落地的产品实现。IoC容器中管理的组件也叫做 bean。在创建 bean 之前，首先需要创建IoC 容器。Spring 提供了IoC 容器的两种实现方式：

BeanFactory：这是 IoC 容器的基本实现，是 Spring 内部使用的接口。面向 Spring 本身，不提供给开发人员使用。
ApplicationContext：BeanFactory 的子接口，提供了更多高级特性。面向 Spring 的使用者，几乎所有场合都使用 ApplicationContext 而不是底层的 BeanFactory
ApplicationContext的主要实现类:

类型名	简介
ClassPathXmlApplicationContext	通过读取类路径下的 XML 格式的配置文件创建 IOC 容器对象
FileSystemXmlApplicationContext	通过文件系统路径读取 XML 格式的配置文件创建 IOC 容器对象
ConfigurableApplicationContext	ApplicationContext 的子接口，包含一些扩展方法 refresh() 和 close() ，让 ApplicationContext 具有启动、关闭和刷新上下文的能力。
WebApplicationContext	专门为 Web 应用准备，基于 Web 环境创建 IOC 容器对象，并将对象引入存入 ServletContext 域中。


说明：

​ ApplicationContext有众多的实现类，其中最常用的就是ClassPathXmlApplicationContext与FileSystemXmlApplicationContext实现类

5.2基于XML管理Bean（了解）
笔记小结：

获取Bean的方式：

根据ID：

User user = (User) applicationContext.getBean("user");
1
根据类型：

 User user = (User) applicationContext.getBean(User.class);
1
根据Id和类型:

User user = (User) applicationContext.getBean("user", User.class);
1
依赖注入

根据Setter注入：<property/>
根据构造器注入：<constructor-arg/>
特殊值处理

字面量赋值<property>
Null值<null>
Xml实体：属性值value="a &lt; b"
CDATA节：标签内容<![CDATA[a < b]]>
注入对象类型属性值

引用外部Bean：属性ref
引用内部Bean：bean嵌套
级联属性赋值：引入对象后，级联赋值name="clazz.clazzId"
注入数组类型属性值：<array></array>

注入集合类型属性值：

注入List集合类型属性值： <list> </list>
注入Map集合类型属性值：<map><entry><<key>/key><value></value></entry></map>
注入引用集合类型属性值：<util></util>
注意：使用前，需要引入util命名空间
引入P命名空间属性值：属性p:

注意：使用前，需要引入p命名空间
引入外部属性文件：<context:property-placeholder location="classpath:jdbc.properties"/>

引入Bean的作用域：属性scope属性值prototype（多例）、singleton（单例）

Bean的生命周期：

bean对象创建（调用无参构造器）

bean对象设置属性

bean的后置处理器（初始化之前）

bean对象初始化（需在配置bean时指定初始化方法）

bean的后置处理器（初始化之后）

bean对象就绪可以使用

bean对象销毁（需在配置bean时指定销毁方法）

IOC容器关闭

引入FactoryBean属性值：实现FactoryBean<T>接口

引入自动装配：属性值autowire属性值byType、byName

5.2.1获取Bean的方式
5.2.1.1根据ID获取Bean
public class UserTest {
    @Test
    void newTest() {
        ApplicationContext applicationContext = new ClassPathXmlApplicationContext("beans.xml");
        User user = (User) applicationContext.getBean("user");
        user.add(); // add……
    }
}
1
2
3
4
5
6
7
8
说明：

​ 此获取方式，需要基于第2.基本用例进行查看

5.2.1.2根据类型获取Bean
public class UserTest {
    @Test
    void newTest() {
        ApplicationContext applicationContext = new ClassPathXmlApplicationContext("beans.xml");
        User user = (User) applicationContext.getBean(User.class);
        user.add(); // add……
    }
}
1
2
3
4
5
6
7
8
注意：

当根据类型获取bean时，要求IOC容器中指定类型的bean有且只能有一个

org.springframework.beans.factory.NoUniqueBeanDefinitionException: No qualifying bean of type 'com.atguigu.spring6.bean.HelloWorld' available: expected single matching bean but found 2: helloworldOne,helloworldTwo
1
说明：

​ 此获取方式，需要基于第2.基本用例进行查看

5.2.1.3根据Id和类型获取Bean
public class UserTest {
    @Test
    void newTest() {
        ApplicationContext applicationContext = new ClassPathXmlApplicationContext("beans.xml");
        User user = (User) applicationContext.getBean("user", User.class);
        user.add(); // add……
    }
}
1
2
3
4
5
6
7
8
补充：

​ 如果组件类实现了接口，可以根据接口类型获取Bean，但前提是Bean唯一

说明：

​ 此获取方式，需要基于第2.基本用例进行查看

5.2.2依赖注入
5.2.2.1根据setter注入
步骤一：创建学生类Student

package com.atguigu.spring6.bean;

public class Student {

    private Integer id;

    private String name;

    private Integer age;

    private String sex;

    public Student() {
    }

    public Integer getId() {
        return id;
    }

    public void setId(Integer id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public Integer getAge() {
        return age;
    }

    public void setAge(Integer age) {
        this.age = age;
    }

    public String getSex() {
        return sex;
    }

    public void setSex(String sex) {
        this.sex = sex;
    }

    @Override
    public String toString() {
        return "Student{" +
                "id=" + id +
                ", name='" + name + '\'' +
                ", age=" + age +
                ", sex='" + sex + '\'' +
                '}';
    }

}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
步骤二：配置bean时为属性赋值

<bean id="studentOne" class="com.atguigu.spring6.bean.Student">
    <!-- property标签：通过组件类的setXxx()方法给组件对象设置属性 -->
    <!-- name属性：指定属性名（这个属性名是getXxx()、setXxx()方法定义的，和成员变量无关） -->
    <!-- value属性：指定属性值 -->
    <property name="id" value="1001"></property>
    <property name="name" value="张三"></property>
    <property name="age" value="23"></property>
    <property name="sex" value="男"></property>
</bean>
1
2
3
4
5
6
7
8
9
说明：

​ 当使用标签标签完成对象的属性创建时，name需要跟对象中的成员变量同名

步骤三：演示

@Test
public void testDIBySet(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-di.xml");
    Student studentOne = ac.getBean("studentOne", Student.class);
    System.out.println(studentOne);
}
1
2
3
4
5
6
说明：

​ 当打印输出是，由于基于XML根据Setter注入方式进行对象的创建，此时输出可获得成员方法tostring的内容

5.2.2.2根据构造器注入
步骤一：在基于根据setter注入的基础上，在Student类中添加有参构造

public Student(Integer id, String name, Integer age, String sex) {
    this.id = id;
    this.name = name;
    this.age = age;
    this.sex = sex;
}
1
2
3
4
5
6
步骤二：配置bean

<bean id="studentTwo" class="com.atguigu.spring6.bean.Student">
    <constructor-arg name="id" value="1002"></constructor-arg>
    <constructor-arg name="name" value="李四"></constructor-arg>
    <constructor-arg name="age"value="33"></constructor-arg>
    <constructor-arg name="sex" value="女"></constructor-arg>
</bean>
1
2
3
4
5
6
说明：

constructor-arg标签属性描述构造器参数：
index属性：指定参数所在位置的索引（从0开始）
name属性：指定参数名，name需要跟对象中的成员变量同名
步骤三：演示

@Test
public void testDIByConstructor(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-di.xml");
    Student studentOne = ac.getBean("studentTwo", Student.class);
    System.out.println(studentOne);
}
1
2
3
4
5
6
说明：

​ 当打印输出是，由于基于XML根据构造器注入方式进行对象的创建，此时输出可获得成员方法tostring的内容

5.2.3特殊值处理
5.2.3.1字面量赋值
<!-- 使用value属性给bean的属性赋值时，Spring会把value属性的值看做字面量 -->
<property name="name" value="张三"/>
1
2
5.2.3.2null值
<property name="name">
    <null />
</property>
1
2
3
细节：

<property name="name" value="null"></property>
1
以上写法，为name所赋值为字符串null

5.2.3.3xml实体
<!-- 解决方案一：使用XML实体来代替 -->
<property name="expression" value="a &lt; b"/>
1
2
说明：

​ 小于号在XML文档中用来定义标签的开始，不能随便使用

5.2.3.4CDATA节
<property name="expression">
    <!-- 解决方案二：使用CDATA节 -->
    <value><![CDATA[a < b]]></value>
</property>
1
2
3
4
说明：

CDATA中的C代表Character，是文本、字符的含义，CDATA就表示纯文本数据
ML解析器看到CDATA节就知道这里是纯文本，就不会当作XML标签或属性来解析
所以CDATA节中写什么符号都随意
5.2.4注入对象类型属性值
5.2.4.1引用外部Bean
步骤一：配置Clazz类型的bean

<bean id="clazzOne" class="com.atguigu.spring6.bean.Clazz">
    <property name="clazzId" value="1111"></property>
    <property name="clazzName" value="财源滚滚班"></property>
</bean>
1
2
3
4
步骤二：为Student中的clazz属性赋值

<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->
    <property name="clazz" ref="clazzOne"></property>
</bean>
1
2
3
4
5
6
7
8
说明：

​ 当引用外部对象时，需要将ref属性变为Value属性。ref属性，值表示引用对象、value属性，值表示字符串

5.2.4.2引用内部Bean
步骤一：在引用外部Bean的基础上

<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <property name="clazz">
        <!-- 在一个bean中再声明一个bean就是内部bean -->
        <!-- 内部bean只能用于给属性赋值，不能在外部通过IOC容器获取，因此可以省略id属性 -->
        <bean id="clazzInner" class="com.atguigu.spring6.bean.Clazz">
            <property name="clazzId" value="2222"></property>
            <property name="clazzName" value="远大前程班"></property>
        </bean>
    </property>
</bean>
1
2
3
4
5
6
7
8
9
10
11
12
13
14
说明：

​ 将Bean写于属性标签内，即为引用内部Bean

5.2.4.3级联属性赋值
步骤一：在引用内部Bean的基础上

<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <property name="clazz" ref="clazzOne"></property>
    <property name="clazz.clazzId" value="3333"></property>
    <property name="clazz.clazzName" value="最强王者班"></property>
</bean>
1
2
3
4
5
6
7
8
9
5.2.5注入数组类型属性值
步骤一：在Student类中中添加成员变量数组和getter于setter方法

private String[] hobbies;

public String[] getHobbies() {
    return hobbies;
}

public void setHobbies(String[] hobbies) {
    this.hobbies = hobbies;
}
1
2
3
4
5
6
7
8
9
步骤二：配置Bean

<bean id="studentFour" class="com.atguigu.spring.bean6.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->
    <property name="clazz" ref="clazzOne"></property>
    <property name="hobbies">
        <array>
            <value>抽烟</value>
            <value>喝酒</value>
            <value>烫头</value>
        </array>
    </property>
</bean>
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
说明：

​ 当注入数组类型数据时，需要使用标签

5.2.6注入集合类型属性值
5.2.6.1注入List集合类型属性值
步骤一：在Clazz类中添加添加成员变量集合和getter于setter方法

private List<Student> students;

public List<Student> getStudents() {
    return students;
}

public void setStudents(List<Student> students) {
    this.students = students;
}
1
2
3
4
5
6
7
8
9
步骤二：配置Bean

<bean id="clazzTwo" class="com.atguigu.spring6.bean.Clazz">
    <property name="clazzId" value="4444"></property>
    <property name="clazzName" value="Javaee0222"></property>
    <property name="students">
        <list>
            <ref bean="studentOne"></ref>
            <ref bean="studentTwo"></ref>
            <ref bean="studentThree"></ref>
        </list>
    </property>
</bean>
1
2
3
4
5
6
7
8
9
10
11
说明：

​ 当注入List集合类型数据时，需要使用标签

细节：

​ 因为List students，List集合中引用的是Student对象，因此注入时需要使用标签，进行引用对象

5.2.6.2注入Map集合类型属性值
步骤一：创建Student类

package com.atguigu.spring6.bean;
public class Teacher {

    private Integer teacherId;

    private String teacherName;

    public Integer getTeacherId() {
        return teacherId;
    }

    public void setTeacherId(Integer teacherId) {
        this.teacherId = teacherId;
    }

    public String getTeacherName() {
        return teacherName;
    }

    public void setTeacherName(String teacherName) {
        this.teacherName = teacherName;
    }

    public Teacher(Integer teacherId, String teacherName) {
        this.teacherId = teacherId;
        this.teacherName = teacherName;
    }

    public Teacher() {

    }
    
    @Override
    public String toString() {
        return "Teacher{" +
                "teacherId=" + teacherId +
                ", teacherName='" + teacherName + '\'' +
                '}';
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
步骤二：在Student类中添加添加成员变量集合和getter于setter方法

private Map<String, Teacher> teacherMap;

public Map<String, Teacher> getTeacherMap() {
    return teacherMap;
}

public void setTeacherMap(Map<String, Teacher> teacherMap) {
    this.teacherMap = teacherMap;
}
1
2
3
4
5
6
7
8
9
步骤三：配置bean

<bean id="teacherOne" class="com.atguigu.spring6.bean.Teacher">
    <property name="teacherId" value="10010"></property>
    <property name="teacherName" value="大宝"></property>
</bean>

<bean id="teacherTwo" class="com.atguigu.spring6.bean.Teacher">
    <property name="teacherId" value="10086"></property>
    <property name="teacherName" value="二宝"></property>
</bean>

<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->
    <property name="clazz" ref="clazzOne"></property>
    <property name="hobbies">
        <array>
            <value>抽烟</value>
            <value>喝酒</value>
            <value>烫头</value>
        </array>
    </property>
    <property name="teacherMap">
        <map>
            <entry>
                <key>
                    <value>10010</value>
                </key>
                <ref bean="teacherOne"></ref>
            </entry>
            <entry>
                <key>
                    <value>10086</value>
                </key>
                <ref bean="teacherTwo"></ref>
            </entry>
        </map>
    </property>
</bean>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
说明：

当注入Map集合类型数据时，需要使用标签
需要使用表示键值对
需要使用表示键
细节：

​ 因为Map<String, Teacher> teacherMap，Map集合中引用的是Teacher对象，因此注入时需要使用标签，进行引用对象

5.2.6.2注入引用集合类型属性值
步骤一：配置对应的命名空间

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns:util="http://www.springframework.org/schema/util"
    xsi:schemaLocation="http://www.springframework.org/schema/util
    http://www.springframework.org/schema/util/spring-util.xsd
    http://www.springframework.org/schema/beans
    http://www.springframework.org/schema/beans/spring-beans.xsd">
1
2
3
4
5
6
7
8
步骤二：配置Bean

<!--list集合类型的bean-->
<util:list id="students">
    <ref bean="studentOne"></ref>
    <ref bean="studentTwo"></ref>
    <ref bean="studentThree"></ref>
</util:list>
<!--map集合类型的bean-->
<util:map id="teacherMap">
    <entry>
        <key>
            <value>10010</value>
        </key>
        <ref bean="teacherOne"></ref>
    </entry>
    <entry>
        <key>
            <value>10086</value>
        </key>
        <ref bean="teacherTwo"></ref>
    </entry>
</util:map>
<bean id="clazzTwo" class="com.atguigu.spring6.bean.Clazz">
    <property name="clazzId" value="4444"></property>
    <property name="clazzName" value="Javaee0222"></property>
    <property name="students" ref="students"></property>
</bean>
<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->
    <property name="clazz" ref="clazzOne"></property>
    <property name="hobbies">
        <array>
            <value>抽烟</value>
            <value>喝酒</value>
            <value>烫头</value>
        </array>
    </property>
    <property name="teacherMap" ref="teacherMap"></property>
</bean>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
说明：

使用标签，可以将List集合或者Map集合的属性注入变为引用的方式
在使用util标签时，需要引入相应的命名空间
5.2.7引入P命名空间属性值
步骤一：引入P命名空间

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:util="http://www.springframework.org/schema/util"
       xmlns:p="http://www.springframework.org/schema/p"
       xsi:schemaLocation="http://www.springframework.org/schema/util
       http://www.springframework.org/schema/util/spring-util.xsd
       http://www.springframework.org/schema/beans
       http://www.springframework.org/schema/beans/spring-beans.xsd">
1
2
3
4
5
6
7
8
9
步骤二：通过p命名空间方式为bean的各个属性赋值

<bean id="studentSix" class="com.atguigu.spring6.bean.Student"
    p:id="1006" p:name="小明" p:clazz-ref="clazzOne" p:teacherMap-ref="teacherMap"></bean>
1
2
说明：

​ 通过p:成员属性，即可完成各个属性的赋值.

5.2.8引入外部属性文件
步骤一：添加依赖

 <!-- MySQL驱动 -->
<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <version>8.0.30</version>
</dependency>

<!-- 数据源 -->
<dependency>
    <groupId>com.alibaba</groupId>
    <artifactId>druid</artifactId>
    <version>1.2.15</version>
</dependency>
1
2
3
4
5
6
7
8
9
10
11
12
13
步骤二：创建外部属性文件

jdbc.user=root
jdbc.password=atguigu
jdbc.url=jdbc:mysql://localhost:3306/ssm?serverTimezone=UTC
jdbc.driver=com.mysql.cj.jdbc.Driver
1
2
3
4
说明：

​ 在resources文件下创建jdbc.properties文件

步骤三：引入属性文件

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:context="http://www.springframework.org/schema/context"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
                           http://www.springframework.org/schema/beans/spring-beans.xsd
                           http://www.springframework.org/schema/context
                           http://www.springframework.org/schema/context/spring-context.xsd">
    <!-- 引入外部属性文件 -->
    <context:property-placeholder location="classpath:jdbc.properties"/>
</beans>
1
2
3
4
5
6
7
8
9
10
11
注意：

​ 在使用 <context:property-placeholder> 元素加载外包配置文件功能前，首先需要在 XML 配置的一级标签 中添加 context 相关的约束。

步骤四：配置Bean

<!--完成数据库信息注入-->
<bean id="druidDataSource" class="com.alibaba.druid.pool.DruidDataSource">
    <property name="url" value="${jdbc.url}"/>
    <property name="driverClassName" value="${jdbc.driver}"/>
    <property name="username" value="${jdbc.user}"/>
    <property name="password" value="${jdbc.password}"/>
</bean>
1
2
3
4
5
6
7
说明：

​ 取外部文件中的值时，需要根据外部文件中属性的名字，可以把相应值取得

步骤五：演示

@Test
public void testDataSource() throws SQLException {
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-datasource.xml");
    DataSource dataSource = ac.getBean(DruidDataSource.class);
    Connection connection = dataSource.getConnection();
    System.out.println(connection);
}
1
2
3
4
5
6
7
5.2.9引入Bean的作用域
步骤一：创建类User

package com.atguigu.spring6.bean;
public class User {

    private Integer id;

    private String username;

    private String password;

    private Integer age;

    public User() {
    }

    public User(Integer id, String username, String password, Integer age) {
        this.id = id;
        this.username = username;
        this.password = password;
        this.age = age;
    }

    public Integer getId() {
        return id;
    }

    public void setId(Integer id) {
        this.id = id;
    }

    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public String getPassword() {
        return password;
    }

    public void setPassword(String password) {
        this.password = password;
    }

    public Integer getAge() {
        return age;
    }

    public void setAge(Integer age) {
        this.age = age;
    }

    @Override
    public String toString() {
        return "User{" +
                "id=" + id +
                ", username='" + username + '\'' +
                ", password='" + password + '\'' +
                ", age=" + age +
                '}';
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
步骤二：配置bean

<!-- scope属性：取值singleton（默认值），bean在IOC容器中只有一个实例，IOC容器初始化时创建对象 -->
<!-- scope属性：取值prototype，bean在IOC容器中可以有多个实例，getBean()时创建对象 -->
<bean class="com.atguigu.spring6.bean.User" scope="prototype"></bean>
1
2
3
说明：

属性值：
singleton（默认），在IOC容器中，这个bean的对象始终为单实例，当IOC容器初始化时即可创建对象
prototype，在IOC容器中，这个bean在IOC容器中有多个实例，当 获取bean时可创建对象
步骤三：演示

@Test
public void testBeanScope(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-scope.xml");
    User user1 = ac.getBean(User.class);
    User user2 = ac.getBean(User.class);
    System.out.println(user1==user2);
}
1
2
3
4
5
6
7
5.2.10Bean的生命周期
流程

bean对象创建（调用无参构造器）

bean对象设置属性

bean的后置处理器（初始化之前）

bean对象初始化（需在配置bean时指定初始化方法）

bean的后置处理器（初始化之后）

bean对象就绪可以使用

bean对象销毁（需在配置bean时指定销毁方法）

IOC容器关闭

步骤一：修改User类

public class User {

    private Integer id;

    private String username;

    private String password;

    private Integer age;

    public User() {
        System.out.println("生命周期：1、创建对象");
    }

    public User(Integer id, String username, String password, Integer age) {
        this.id = id;
        this.username = username;
        this.password = password;
        this.age = age;
    }

    public Integer getId() {
        return id;
    }

    public void setId(Integer id) {
        System.out.println("生命周期：2、依赖注入");
        this.id = id;
    }

    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public String getPassword() {
        return password;
    }

    public void setPassword(String password) {
        this.password = password;
    }

    public Integer getAge() {
        return age;
    }

    public void setAge(Integer age) {
        this.age = age;
    }

    public void initMethod(){
        System.out.println("生命周期：3、初始化");
    }

    public void destroyMethod(){
        System.out.println("生命周期：5、销毁");
    }

    @Override
    public String toString() {
        return "User{" +
                "id=" + id +
                ", username='" + username + '\'' +
                ", password='" + password + '\'' +
                ", age=" + age +
                '}';
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
64
65
66
67
68
69
70
71
72
说明：

​ 其中的initMethod()和destroyMethod()，可以通过配置Bean指定为初始化和销毁的方法

步骤二：创建Bean 的后置处理器

package com.atguigu.spring6.process;
    
import org.springframework.beans.BeansException;
import org.springframework.beans.factory.config.BeanPostProcessor;

public class MyBeanProcessor implements BeanPostProcessor {
    
    @Override
    public Object postProcessBeforeInitialization(Object bean, String beanName) throws BeansException {
        System.out.println("☆☆☆" + beanName + " = " + bean);
        return bean;
    }
    
    @Override
    public Object postProcessAfterInitialization(Object bean, String beanName) throws BeansException {
        System.out.println("★★★" + beanName + " = " + bean);
        return bean;
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
注意：

​ bean的后置处理器会在生命周期的初始化前后添加额外的操作，需要实现BeanPostProcessor接口，且配置到IOC容器中，需要注意的是，bean后置处理器不是单独针对某一个bean生效，而是针对IOC容器中所有bean都会执行

步骤三：配置Bean

<!-- 使用init-method属性指定初始化方法 -->
<!-- 使用destroy-method属性指定销毁方法 -->
<bean class="com.atguigu.spring6.bean.User" scope="prototype" init-method="initMethod" destroy-method="destroyMethod">
    <property name="id" value="1001"></property>
    <property name="username" value="admin"></property>
    <property name="password" value="123456"></property>
    <property name="age" value="23"></property>
</bean>
<!-- bean的后置处理器要放入IOC容器才能生效 -->
<bean id="myBeanProcessor" class="com.atguigu.spring6.process.MyBeanProcessor"/>
1
2
3
4
5
6
7
8
9
10
说明：

在配置Bean时，需要使用init-method属性和destroy-method属性进行配置Bean的初始化方法与销毁的方法
在配置Bean时，需要将Bean的后置处理器放入IOC容器才能生效
步骤四：演示

@Test
public void testLife(){
    ClassPathXmlApplicationContext ac = new ClassPathXmlApplicationContext("spring-lifecycle.xml");
    User bean = ac.getBean(User.class);
    System.out.println("生命周期：4、通过IOC容器获取bean并使用");
    ac.close();
}
1
2
3
4
5
6
7
5.2.11引入FactoryBean属性值


说明：

​ FactoryBean是Spring提供的一种整合第三方框架的常用机制。和普通的bean不同，配置一个FactoryBean类型的bean，在获取bean的时候得到的并不是class属性中配置的这个类的对象，而是getObject()方法的返回值。通过这种机制，Spring可以帮我们把复杂组件创建的详细过程和繁琐细节都屏蔽起来，只把最简洁的使用界面展示给我们。

步骤一 ：创建类UserFactoryBean

package com.atguigu.spring6.bean;
public class UserFactoryBean implements FactoryBean<User> {
    @Override
    public User getObject() throws Exception {
        return new User();
    }

    @Override
    public Class<?> getObjectType() {
        return User.class;
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
步骤二：配置bean

<bean id="user" class="com.atguigu.spring6.bean.UserFactoryBean"></bean>
1
步骤三：演示

@Test
public void testUserFactoryBean(){
    //获取IOC容器
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-factorybean.xml");
    User user = (User) ac.getBean("user");
    System.out.println(user);
}
1
2
3
4
5
6
7
说明：

​ 此时获取到的容器对象，并不是UserFactoryBean，而是User

5.2.12引入xml自动装配
步骤一：环境准备

1.创建UserController类

package com.atguigu.spring6.autowire.controller
public class UserController {

    private UserService userService;

    public void setUserService(UserService userService) {
        this.userService = userService;
    }

    public void saveUser(){
        userService.saveUser();
    }

}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
2.创建UserService接口

package com.atguigu.spring6.autowire.service
public interface UserService {

    void saveUser();

}
1
2
3
4
5
6
3.创建UserServiceImpl类实现UserService接口

package com.atguigu.spring6.autowire.service.impl
public class UserServiceImpl implements UserService {

    private UserDao userDao;

    public void setUserDao(UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void saveUser() {
        userDao.saveUser();
    }

}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
4.创建UserDao接口

package com.atguigu.spring6.autowire.dao
public interface UserDao {

    void saveUser();

}
1
2
3
4
5
6
5.创建UserDaoImpl类实现UserDao接口

package com.atguigu.spring6.autowire.dao.impl
public class UserDaoImpl implements UserDao {

    @Override
    public void saveUser() {
        System.out.println("保存成功");
    }

}
1
2
3
4
5
6
7
8
9
步骤二：配置bean

<bean id="userController" class="com.atguigu.spring6.autowire.controller.UserController" autowire="byType"></bean>

<bean id="userService" class="com.atguigu.spring6.autowire.service.impl.UserServiceImpl" autowire="byType"></bean>

<bean id="userDao" class="com.atguigu.spring6.autowire.dao.impl.UserDaoImpl"></bean>
1
2
3
4
5
说明：

当使用Bean标签的autowire属性是，通过byType的方式进行自动装配
byType：根据类型匹配IOC容器中的某个兼容类型的bean，为属性自动赋值
若在IOC中，没有任何一个兼容类型的bean能够为属性赋值，则该属性不装配，即值为默认值null
若在IOC中，有多个兼容类型的bean能够为属性赋值，则抛出异常NoUniqueBeanDefinitionException
byName：将自动装配的属性的属性名，作为bean的id在IOC容器中匹配相对应的bean进行赋值
步骤三：演示

@Test
public void testAutoWireByXML(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("autowire-xml.xml");
    UserController userController = ac.getBean(UserController.class);
    userController.saveUser();
}
1
2
3
4
5
6
说明：

​ 当使用标签中的属性时，使用Autowire属性使用byType的方式即可实现属性的自动注入

5.3基于注解管理Bean（重点）
笔记小结：

概述：

简介：Java 增加了对注解（Annotation）的支持，它是代码中的一种特殊标记，可以在编译、类加载和运行时被读取，执行相应的处理。
使用注解：
@Component：表示泛化组件
@Repository：表示数据访问层组件
@Service：表示业务层组件
@Controller：：表示控制层组件
开启组件扫描

概述：通过 <context:component-scan> 元素开启 Spring Beans的自动扫描功能。Spring 会自动从扫描指定的包（base-package 属性设置）及其子包下的所有类，如果类上使用了 @Component 注解，就将该类装配到容器中
基本用例：使用标签<context:component-scan></context:component-scan>
添加conentt约束
开启扫描方式
指定要排除的组件： <context:exclude-filter></context:exclude-filter>
仅扫描指定组件： <context:include-filter></context:include-filter
使用注解定义Bean

使用@Autowired注入：

属性注入

@Autowired
private UserDao userDao;
1
2
setter注入

private UserDao userDao;
@Autowired
public void setUserDao(UserDao userDao) {
    this.userDao = userDao;
}
1
2
3
4
5
构造方法注入

private UserDao userDao;
@Autowired
public UserServiceImpl(UserDao userDao) {
	this.userDao = userDao;
}
1
2
3
4
5
形参注入

private UserDao userDao;
public UserServiceImpl(@Autowired UserDao userDao) {
    this.userDao = userDao;
}
1
2
3
4
无注解注入：当构造函数仅有一个需要注入的构造参数时，@Autowired可以省略

private UserDao userDao;
public UserServiceImpl(UserDao userDao) {
    this.userDao = userDao;
}
1
2
3
4
联合**@Qualifier注解注入：适用于一个接口多个实现类的注解区别**

@Autowired
@Qualifier("userDaoImpl") // 指定bean的名字
private UserDao userDao;
1
2
3
使用@Resource注入：

Name注入：在使用注解时，配置name属性

@Resource(name = "myUserDao")
1
未知Name注入：不配置name属性，注入属性的成员变量但需要与Bean 的名称同名

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {
    ……
@Resource
private UserDao myUserDao;
1
2
3
4
5
类型注入：不配置name属性，名称都不同时，注入属性的成员类型会根据Bean实现的接口类型进行匹配

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {
    ……
@Resource
private UserDao userDao1;
1
2
3
4
5
全注解开发：不再使用spring配置文件了，写一个配置类来代替配置文件

@Configuration
//@ComponentScan({"com.atguigu.spring6.controller", "com.atguigu.spring6.service","com.atguigu.spring6.dao"})
@ComponentScan("com.atguigu.spring6") //开启包扫描
public class Spring6Config {
}
1
2
3
4
5
说明：用全注解开发方式时，需要指定包扫描所属的范围，便于Spring框架确定扫描而注入Bean的范围

5.3.1概述
5.3.1.1简介
​ 从 Java 5 开始，Java 增加了对注解（Annotation）的支持，它是代码中的一种特殊标记，可以在编译、类加载和运行时被读取，执行相应的处理。开发人员可以通过注解在不改变原有代码和逻辑的情况下，在源代码中嵌入补充信息。

​ Spring 从 2.5 版本开始提供了对注解技术的全面支持，我们可以使用注解来实现自动装配，简化 Spring 的 XML 配置。

5.3.1.2步骤
引入依赖
开启组件扫描
使用注解定义 Bean
依赖注入
5.3.1.3使用注解
​ Spring 提供了以下多个注解，这些注解可以直接标注在 Java 类上，将它们定义成 Spring Bean

注解	说明
@Component	该注解用于描述 Spring 中的 Bean，它是一个泛化的概念，仅仅表示容器中的一个组件（Bean），并且可以作用在应用的任何层次，例如 Service 层、Dao 层等。 使用时只需将该注解标注在相应类上即可。
@Repository	该注解用于将数据访问层（Dao 层）的类标识为 Spring 中的 Bean，其功能与 @Component 相同。
@Service	该注解通常作用在业务层（Service 层），用于将业务层的类标识为 Spring 中的 Bean，其功能与 @Component 相同。
@Controller	该注解通常作用在控制层（如SpringMVC 的 Controller），用于将控制层的类标识为 Spring 中的 Bean，其功能与 @Component 相同。
5.3.2开启组件扫描
5.3.2.1概述
​ Spring 默认不使用注解装配 Bean，因此我们需要在 Spring 的 XML 配置中，通过 <context:component-scan> 元素开启 Spring Beans的自动扫描功能。开启此功能后，Spring 会自动从扫描指定的包（base-package 属性设置）及其子包下的所有类，如果类上使用了 @Component 注解，就将该类装配到容器中。

5.3.2.2基本用例-实现组件扫描
步骤一：添加约束

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:context="http://www.springframework.org/schema/context"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
    http://www.springframework.org/schema/beans/spring-beans-3.0.xsd
    http://www.springframework.org/schema/context
            http://www.springframework.org/schema/context/spring-context.xsd">
</beans>
1
2
3
4
5
6
7
8
9
说明：

​ 在 XML 配置的一级标签 中添加 context 相关的约束

步骤二：开启扫描方式

<context:component-scan base-package="com.atguigu.spring6">
</context:component-scan>
1
2
说明：

​ 在Beans.xml文件中，设置开启扫描方式即可

5.3.2.3指定要排除的组件
<context:component-scan base-package="com.atguigu.spring6">
    <!-- context:exclude-filter标签：指定排除规则 -->
    <!-- 
 		type：设置排除或包含的依据
		type="annotation"，根据注解排除，expression中设置要排除的注解的全类名
		type="assignable"，根据类型排除，expression中设置要排除的类型的全类名
	-->
    <context:exclude-filter type="annotation" expression="org.springframework.stereotype.Controller"/>
        <!--<context:exclude-filter type="assignable" expression="com.atguigu.spring6.controller.UserController"/>-->
</context:component-scan>
1
2
3
4
5
6
7
8
9
10
说明：

<context:exclude-filter></context:exclude-filter>标签，指定排除规则
type属性：设置排除或包含的依据
属性值：annotation，根据注解排除
属性值：assignable，根据类型排除
expression属性：设置要排除的注解或类型的全类名
5.3.2.4仅扫描指定组件
<context:component-scan base-package="com.atguigu" use-default-filters="false">
    <!-- context:include-filter标签：指定在原有扫描规则的基础上追加的规则 -->
    <!-- use-default-filters属性：取值false表示关闭默认扫描规则 -->
    <!-- 此时必须设置use-default-filters="false"，因为默认规则即扫描指定包下所有类 -->
    <context:include-filter type="annotation" expression="org.springframework.stereotype.Controller"/>
    <!--<context:include-filter type="assignable" expression="com.atguigu.spring6.controller.UserController"/>-->
</context:component-scan>
1
2
3
4
5
6
7
说明：

use-default-filters="false"，表示关闭默认扫描规则
<context:include-filter></context:include-filter>，表示指定的过滤条件来确定哪些类应该被包含在组件扫描中
5.3.2使用注解定义Bean
5.3.3使用@Autowired注入
5.3.3.1概述


说明：

@Autowired注解可以标注在：构造方法上、方法上、形参上、属性上、注解上
@Autowired注解的required属性，
属性值为True：表示注入的时候要求被注入的Bean必须是存在的，如果不存在则报错
属性值为False：：表示注入的时候要求被注入的Bean不一定是存在的，如果存在的话就注入，不存在的话，也不报错
细节：

单独使用@Autowired注解时，默认是根据类型装配，默认是"byType"，例如基于XML管理Bean
<bean id="userService" class="com.atguigu.spring6.autowire.service.impl.UserServiceImpl" autowire="byType"></bean>
1
5.3.3.2属性注入
步骤一：搭建环境

1.创建UserDao接口

package com.atguigu.spring6.dao;

public interface UserDao {

    public void print();
}
1
2
3
4
5
6
2.创建UserDaoImpl实现

package com.atguigu.spring6.dao.impl;

import com.atguigu.spring6.dao.UserDao;
import org.springframework.stereotype.Repository;

@Repository
public class UserDaoImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
3.创建UserService接口

package com.atguigu.spring6.service;

public interface UserService {

    public void out();
}
1
2
3
4
5
6
4.创建UserServiceImpl实现类

package com.atguigu.spring6.service.impl;

import com.atguigu.spring6.dao.UserDao;
import com.atguigu.spring6.service.UserService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;

@Service
public class UserServiceImpl implements UserService {

    @Autowired
    private UserDao userDao;

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
5.创建UserController类

package com.atguigu.spring6.controller;

import com.atguigu.spring6.service.UserService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Controller;

@Controller
public class UserController {

    @Autowired
    private UserService userService;

    public void out() {
        userService.out();
        System.out.println("Controller层执行结束。");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

当使用@Autowired注解注入时，可不提供构造方法喝Setter方法，也可以注入成功
结果：
5.3.3.3set注入
步骤一：搭建环境

1.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    private UserDao userDao;

    @Autowired
    public void setUserDao(UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
2.修改UserController类

@Controller
public class UserController {

    private UserService userService;

    @Autowired
    public void setUserService(UserService userService) {
        this.userService = userService;
    }

    public void out() {
        userService.out();
        System.out.println("Controller层执行结束。");
    }

}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

​ 通过在需要注入的setter方法上进行添加@Autowired注解

5.3.3.4构造方法注入
步骤一：搭建环境

1.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    private UserDao userDao;

    @Autowired
    public UserServiceImpl(UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
2.修改UserController类

@Controller
public class UserController {

    private UserService userService;

    @Autowired
    public UserController(UserService userService) {
        this.userService = userService;
    }

    public void out() {
        userService.out();
        System.out.println("Controller层执行结束。");
    }

}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

​ 通过在需要注入的构造器方法上进行添加@Autowired注解

5.3.3.5形参注入
步骤一：搭建环境

1.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    private UserDao userDao;

    public UserServiceImpl(@Autowired UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
2.修改UserController类

@Controller
public class UserController {

    private UserService userService;

    public UserController(@Autowired UserService userService) {
        this.userService = userService;
    }

    public void out() {
        userService.out();
        System.out.println("Controller层执行结束。");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

​ 通过在需要注入的形参上进行添加@Autowired注解

5.3.3.6无注解注入
步骤一：搭建环境

1.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

 
    private UserDao userDao;

    public UserServiceImpl(UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

​ 当有参数的构造方法只有一个时，@Autowired注解可以省略

5.3.3.7联合@Qualifier注解注入
步骤一：搭建环境

1.添加UserDaoRedisImpl类

@Repository
public class UserDaoRedisImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Redis Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
说明：

此时，添加实现UserDao接口类，已经造成一个接口对应两个实现类
此时，程序错误，信息中说：不能装配，UserDao这个Bean的数量等于2
步骤二：修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    @Autowired
    @Qualifier("userDaoImpl") // 指定bean的名字
    private UserDao userDao;

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
说明：

​ 当需要注入的接口有多个实现类时，可以联合使用@Qualifier(“userDaoImpl”) 注解，并指定实现类的名字，即可完成属性注入

5.3.4使用@Resource注入
5.3.4.1概述
​ @Resource注解是通过名称匹配的方式来实现注入的，默认按照名称进行匹配，如果找不到匹配的名称，则会尝试按照类型匹配。

​ @Resource注解是JDK扩展包中的，也就是说属于JDK的一部分。所以该注解是标准注解，更加具有通用性。(JSR-250标准中制定的注解类型。JSR是Java规范提案。)



说明：

如果是JDK8的话不需要额外引入依赖。高于JDK11或低于JDK8需要引入以下依赖
<dependency>
    <groupId>jakarta.annotation</groupId>
    <artifactId>jakarta.annotation-api</artifactId>
    <version>2.1.1</version>
</dependency>
1
2
3
4
5
5.3.4.2Name注入
步骤一：搭建环境

1.修改UserDaoImpl类

package com.atguigu.spring6.dao.impl;

import com.atguigu.spring6.dao.UserDao;
import org.springframework.stereotype.Repository;

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
说明：

​ 当使用注解时，在小括号内写上属性名称表示为此Bean定义别名

2.修改UserServiceImpl类

package com.atguigu.spring6.service.impl;

import com.atguigu.spring6.dao.UserDao;
import com.atguigu.spring6.service.UserService;
import jakarta.annotation.Resource;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.beans.factory.annotation.Qualifier;
import org.springframework.stereotype.Service;

@Service
public class UserServiceImpl implements UserService {

    @Resource(name = "myUserDao")
    private UserDao myUserDao;

    @Override
    public void out() {
        myUserDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
说明：

​ 当使用@Resource注解时，可以使用name属性指定属性注入的别名

步骤二：演示

5.3.4.3未知Name注入
步骤一：搭建环境

1.修改UserDaoImpl类

package com.atguigu.spring6.dao.impl;

import com.atguigu.spring6.dao.UserDao;
import org.springframework.stereotype.Repository;

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
2.修改UserServiceImpl类

package com.atguigu.spring6.service.impl;

import com.atguigu.spring6.dao.UserDao;
import com.atguigu.spring6.service.UserService;
import jakarta.annotation.Resource;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.beans.factory.annotation.Qualifier;
import org.springframework.stereotype.Service;

@Service
public class UserServiceImpl implements UserService {

    @Resource
    private UserDao myUserDao;

    @Override
    public void out() {
        myUserDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
说明：

​ 当使用@Resource注解时，在name属性未知的情况下，将属性注入的成员属性变量名定义为与Bean同名，即可完成注入

步骤二：演示

5.3.4.4类型注入
步骤一：搭建环境

1.原UserDaoImpl类

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
2.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    @Resource
    private UserDao userDao1;

    @Override
    public void out() {
        userDao1.print();
        System.out.println("Service层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
说明：

​ 当使用@Resource注解时，现在userDao1属性名不存在，但仍然可以注入成功。因为，UserDao他们的类型名相同

5.3.5全注解开发
5.3.5.1概述
​ 全注解开发就是不再使用spring配置文件了，写一个配置类来代替配置文件

5.3.5.2基本用例-全注解开发实现
步骤一：创建配置类

@Configuration
//@ComponentScan({"com.atguigu.spring6.controller", "com.atguigu.spring6.service","com.atguigu.spring6.dao"})
@ComponentScan("com.atguigu.spring6")
public class Spring6Config {
}
1
2
3
4
5
说明：

​ 使用@ComponentScan注解，进行组件扫描，从而替代了原有在xml文件中的配置

步骤二：演示

@Test
public void testAllAnnotation(){
    ApplicationContext context = new AnnotationConfigApplicationContext(Spring6Config.class);
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
    logger.info("执行成功");
}
1
2
3
4
5
6
7
说明：

​ 需要使用AnnotationConfigApplicationContext类来获取Spring6Config的字节码文件

5.4原理
笔记小结：

扫描指定的包，获取所有需要管理的类的类名。
实例化需要管理的类，通过反射机制调用构造器来实现。
通过反射机制调用setter方法或者构造器注入属性值。
维护对象之间的依赖关系，实现对象之间的解耦。
将实例化好的对象注册到IOC容器中，便于后续使用。
说明：



步骤一：环境搭建

1.创建注解

创建Bean注解

// 此注解用于定义容器对象，类似于@Componet、@Service、@Controller注解等作用
@Target(ElementType.TYPE)
@Retention(RetentionPolicy.RUNTIME)
public @interface Bean {
}
1
2
3
4
5
创建依赖注入注解

// 此注解用于完成成员属性的依赖注入，类似于@Autoware、@Resource注解等作用
@Target({ElementType.FIELD})
@Retention(RetentionPolicy.RUNTIME)
public @interface Di {
}
1
2
3
4
5
2.创建IOC核心逻辑

定义bean容器接口

package com.atguigu.spring.core;

public interface ApplicationContext {

    Object getBean(Class clazz);
}
1
2
3
4
5
6
编写注解bean容器接口实现

public class AnnotationApplicationContext implements ApplicationContext {

    // 存储Bean的容器
    private HashMap<Class, Object> beanFactory = new HashMap<>();

    // 根据字节码文件获取Bean容器中的对象
    @Override
    public Object getBean(Class clazz) {
        return beanFactory.get(clazz);
    }

    /**
     * 根据包扫描加载bean
     * @param basePackage
     */
    public AnnotationApplicationContext(String basePackage) {
        try {
            String packageDirName = basePackage.replaceAll("\\.", "\\\\");
            Enumeration<URL> dirs =Thread.currentThread().getContextClassLoader().getResources(packageDirName);
            while (dirs.hasMoreElements()) {
                URL url = dirs.nextElement();
                String filePath = URLDecoder.decode(url.getFile(),"utf-8");
                rootPath = filePath.substring(0, filePath.length()-packageDirName.length());
                // 扫描包下的Bean
                loadBean(new File(filePath));
            }

        } catch (Exception e) {
            throw new RuntimeException(e);
        }
        //依赖注入
        loadDi();
    }


    private  void loadBean(File fileParent) {
        if (fileParent.isDirectory()) {
            File[] childrenFiles = fileParent.listFiles();
            if(childrenFiles == null || childrenFiles.length == 0){
                return;
            }
            for (File child : childrenFiles) {
                if (child.isDirectory()) {
                    //如果是个文件夹就继续调用该方法,使用了递归
                    loadBean(child);
                } else {
                    //通过文件路径转变成全类名,第一步把绝对路径部分去掉
                    String pathWithClass = child.getAbsolutePath().substring(rootPath.length() - 1);
                    //选中class文件
                    if (pathWithClass.contains(".class")) {
                        //    com.xinzhi.dao.UserDao
                        //去掉.class后缀，并且把 \ 替换成 .
                        String fullName = pathWithClass.replaceAll("\\\\", ".").replace(".class", "");
                        try {
                            Class<?> aClass = Class.forName(fullName);
                            //把非接口的类实例化放在map中
                            if(!aClass.isInterface()){
                                Bean annotation = aClass.getAnnotation(Bean.class);
                                if(annotation != null){
                                    Object instance = aClass.newInstance();
                                    //判断一下有没有接口
                                    if(aClass.getInterfaces().length > 0) {
                                        //如果有接口把接口的class当成key，实例对象当成value
                                        System.out.println("正在加载【"+ aClass.getInterfaces()[0] +"】,实例对象是：" + instance.getClass().getName());
                                        beanFactory.put(aClass.getInterfaces()[0], instance);
                                    }else{
                                        //如果有接口把自己的class当成key，实例对象当成value
                                        System.out.println("正在加载【"+ aClass.getName() +"】,实例对象是：" + instance.getClass().getName());
                                        beanFactory.put(aClass, instance);
                                    }
                                }
                            }
                        } catch (ClassNotFoundException | IllegalAccessException | InstantiationException e) {
                            e.printStackTrace();
                        }
                    }
                }
            }
        }
    }

    private void loadDi() {
        for(Map.Entry<Class,Object> entry : beanFactory.entrySet()){
            //就是咱们放在容器的对象
            Object obj = entry.getValue();
            Class<?> aClass = obj.getClass();
            Field[] declaredFields = aClass.getDeclaredFields();
            for (Field field : declaredFields){
                Di annotation = field.getAnnotation(Di.class);
                if( annotation != null ){
                    field.setAccessible(true);
                    try {
                        System.out.println("正在给【"+obj.getClass().getName()+"】属性【" + field.getName() + "】注入值【"+ beanFactory.get(field.getType()).getClass().getName() +"】");
                        field.set(obj,beanFactory.get(field.getType()));
                    } catch (IllegalAccessException e) {
                        e.printStackTrace();
                    }
                }
            }
        }
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
64
65
66
67
68
69
70
71
72
73
74
75
76
77
78
79
80
81
82
83
84
85
86
87
88
89
90
91
92
93
94
95
96
97
98
99
100
101
102
说明：

可将此代码复制到IDEA中查看逻辑更详细

3.创建Dao层

创建UserDao接口
public interface UserDao {

    public void print();
}
1
2
3
4
创建UserDaoImpl实现
@Bean
public class UserDaoImpl implements UserDao {
    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}

1
2
3
4
5
6
7
8
说明：

当此类实现了UserDao这个接口时，会将UserDao这个接口作为容器的Key值，来获取UserDaoImpl这个实现类

这也就是为什么一个接口不能对应多个实现类，因为HashMap的Key值不能重复

// 参数解释，参数1：实现类上实现的第一个接口或者实现类的字节码文件；参数2：实现类实例
beanFactory.put(aClass.getInterfaces()[0], instance);
// 此处，参数1：接口为UserDao；参数2，实现类实例为UserDaoImpl
1
2
3
4.创建Service层

创建UserService接口

public interface UserService {
    public void out();
}
1
2
3
创建UserServiceImpl实现类

@Bean
public class UserServiceImpl implements UserService {

    @DI
    private UserDao userDao;

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
说明：

当此类里包含了依赖注入这个接口时，会将UserServiceImpl这个实现类实例作为依赖注入的Key值，并且根据依赖注入的变量名确定所需要依赖注入的实现类实例

// 参数解释，参数1：设置字段值的对象实例；参数2：需要设置的字段值
field.set(obj, beanFactory.get(field.getType()));
//此处，参数1：实现类实例UserServiceImpl；参数2：实现类实例UserDaoImpl
1
2
3
步骤二：演示

ApplicationContext applicationContext = new AnnotationApplicationContext("org.example");
UserService bean = (UserService) applicationContext.getBean(UserService.class);
bean.out();
1
2
3
6.面向切面：AOP (重点)
笔记小结：

概述：

含义：AOP（Aspect Oriented Programming）是一种设计思想，是软件设计领域中的面向切面编程
作用：
简化开发：分离关注点，让各个一些通用的行为（日志、事务、安全）实现重用
降低代码耦合度：将不同的关注点分离开来，提高代码可复用性和可维护性
横切关注点：横切关注点是指跨越应用程序多个模块的功能或行为。例如日志记录、安全性等与业务逻辑无关的功能
通知：通知（增强）是指在 AOP 中定义的一种特殊类型的方法，它包含要在连接点（join point）执行的一些行为。例如在某个方法执行前、中、后需要加上一些输出日志等这样的逻辑
切面：切面指的是横切关注点和通知的组合，简单的说，切面就是封装通知方法的类
目标：目标（Target）是指被通知的对象或者被切面所影响的对象。例如类、接口、方法这类元素
代理：代理是指控制对目标对象的访问，并在访问过程中插入额外的逻辑。简单的说，代理就是向目标对象应用通知之后创建的代理对象
连接点：连接点（Join Point）表示在程序执行过程中能够插入一个切面的点。简单的说，连接点就是代理对象中的执行逻辑
切入点：切入点（Pointcut）表示在目标对象中定义的一个或多个特定的方法或方法执行位置，它表示在何处应该插入切面的逻辑
代理模式：代理模式是一种结构型设计模式，它使得代理对象可以代表另一个对象进行访问

静态代理：静态代理是用代码的方式实现方法之前或之后执行一些附加操作
动态代理：它允许在运行时动态地创建代理对象，并将切面逻辑织入到目标对象的方法中
分类：基于接口的代理（有接口情况）、基于类的代理（无接口情况）
切入点表达式：用于匹配目标对象中的方法，并提供切入点的精确定义



基于注解的AOP：各个小结模块，请查看此小结（重点）

基于XML的AOP：通过XML 的方式来实现切面的定义和应用（了解）

6.1概述
6.1.1定义
​ AOP（Aspect Oriented Programming）是一种设计思想，是软件设计领域中的面向切面编程，它是面向对象编程的一种补充和完善，它以通过预编译方式和运行期动态代理方式实现，在不修改源代码的情况下，给程序动态统一添加额外功能的一种技术。利用AOP可以对业务逻辑的各个部分进行隔离，从而使得业务逻辑各部分之间的耦合度降低，提高程序的可重用性，同时提高了开发的效率

6.1.2作用
代码重用和模块化：AOP可以将一些通用的行为（例如日志记录、安全控制、事务管理等）抽象出来，形成可重用的模块，避免在每个业务逻辑中都重复编写这些代码。

分离关注点：AOP将不同的关注点分离开来，使得各个模块间职责更加清晰明确，代码的可读性和可维护性也更强。

简化开发：AOP可以帮助开发人员将关注点从业务逻辑中分离出来，使得开发更加简单明了。

提高系统的可扩展性：在系统需求变化时，只需要修改AOP模块而不是修改业务逻辑，这可以使得系统更加易于扩展和维护。

降低代码耦合度：AOP的作用是将不同的关注点分离开来，这可以避免代码之间的紧耦合，提高代码的可复用性和可维护性。

6.1.3横切关注点
​ 在 AOP 中，横切关注点指的是在应用程序中影响多个类或对象的横切性质的行为，比如日志记录、性能监控、事务处理等等。这些行为可能分散在整个应用程序中的不同类和方法中，而不是与应用程序的核心业务逻辑紧密相关。

​ 使用 AOP 技术，可以将这些横切关注点从应用程序的核心业务逻辑中分离出来，并将它们模块化为可重用的模块，从而实现更好的代码结构和更好的可维护性。



6.1.4通知（增强）
​ 通知（advice）也被称为增强（advice），是指在 AOP 中定义的一种特殊类型的方法，它包含要在连接点（join point）执行的一些行为。通知可以在目标方法执行之前、之后或异常时被执行，也可以在目标方法返回一个结果后被执行。通知的目的是在不修改目标对象的情况下，将增强（如日志、事务管理等）应用于应用程序的特定方法或切入点。通知是实现 AOP 的核心组件之一，通过将通知应用于特定的连接点（join point）来实现面向切面编程

简单来说：通知就是你想要增强的功能，比如 安全，事务，日志等

通知分类：

前置通知：在被代理的目标方法前执行
返回通知：在被代理的目标方法成功结束后执行（寿终正寝）
异常通知：在被代理的目标方法异常结束后执行（死于非命）
后置通知：在被代理的目标方法最终结束后执行（盖棺定论）
环绕通知：使用try…catch…finally结构围绕整个被代理的目标方法，包括上面四种通知对应的所有位置


6.1.5切面
​ 在AOP中，切面指的是横切关注点和通知的组合，它是一个模块化的横向分割，可以理解为一个横向的切片。切面是对横切关注点和通知的封装，它包含了一组切点和通知，用于描述在何处、何时、以及如何执行横切逻辑。切面可以在不修改原代码的情况下，对原有的代码进行功能的增强或改变。通常，切面是以一个类的形式存在的，它包含了一个或多个通知和一个或多个切点。

简单来说：切面就是封装通知方法的类



6.1.6目标
​ 在AOP（Aspect-Oriented Programming）中，目标（Target）是指被通知的对象或者被切面所影响的对象。它是应用程序中的一个具体元素，可以是类、接口、方法或者字段等。简单点说，目标就是被代理的目标对象

6.1.7代理
​ 在AOP（Aspect-Oriented Programming）中，代理（Proxy）是一种设计模式，用于控制对目标对象的访问，并在访问过程中插入额外的逻辑。简单点说，代理就是向目标对象应用通知之后创建的代理对象

6.1.8连接点
​ 在 AOP 中，连接点（Join Point）表示在程序执行过程中能够插入一个切面的点，例如方法调用、异常处理、字段访问等。连接点定义了在程序中的哪个位置可以应用切面。切面可以在连接点前后增加额外的处理逻辑，从而影响程序的行为。通俗地讲，连接点就是在程序执行中可以被拦截的地方



说明：

​ 把方法排成一排，每一个横切位置看成x轴方向，把方法从上到下执行的顺序看成y轴，x轴和y轴的交叉点就是连接点。通俗说，就是spring允许你使用通知的地方

6.1.9切入点
​ 在 AOP 中，切入点（Join Point）是指程序执行过程中明确的点，通常是方法调用的时候，也可以是异常处理程序的处理过程。切入点定义了哪些方法是需要被拦截或增强的，是 AOP 中最重要的概念之一。切入点通常以方法的形式被定义，比如某个类的所有方法、某个包下的所有方法等等。在 AOP 中，通常会使用表达式语言定义切入点，如使用 Spring AOP 中的 @Pointcut 注解定义。

6.2代理模式
6.2.1概述
​ 代理模式是一种结构型设计模式，它使得代理对象可以代表另一个对象进行访问。它是二十三种设计模式中的一种，属于结构型模式。它的作用就是通过提供一个代理类，让我们在调用目标方法的时候，不再是直接对目标方法进行调用，而是通过代理类间接调用。让不属于目标方法核心逻辑的代码从目标方法中剥离出来——解耦。调用目标方法时先调用代理对象的方法，减少对目标方法的调用和打扰，同时让附加功能能够集中在一起也有利于统一维护。



​

代理：将非核心逻辑剥离出来以后，封装这些非核心逻辑的类、对象、方法

6.2.2静态代理
​ 在静态代理中，代理类是在编译时期创建的，代理类和委托类实现相同的接口或继承相同的类，并在代理类中实现委托类中的方法，在调用委托类的方法之前或之后执行一些附加操作

public class CalculatorStaticProxy implements Calculator {
    
    // 将被代理的目标对象声明为成员变量
    private Calculator target;
    
    public CalculatorStaticProxy(Calculator target) {
        this.target = target;
    }
    
    @Override
    public int add(int i, int j) {
    
        // 附加功能由代理类中的代理方法来实现
        System.out.println("[日志] add 方法开始了，参数是：" + i + "," + j);
    
        // 通过目标对象来实现核心业务逻辑
        int addResult = target.add(i, j);
    
        System.out.println("[日志] add 方法结束了，结果是：" + addResult);
    
        return addResult;
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
说明：

​ 静态代理确实实现了解耦，但是由于代码都写死了，完全不具备任何的灵活性

6.2.3动态代理
6.2.3.1概述
6.2.3.1.1定义
​ 在动态代理中，代理类是在运行时期动态创建的。它不需要事先知道委托类的接口或实现类，而是在运行时期通过 Java 反射机制动态生成代理类



6.2.3.1.2分类
动态代理分类

基于接口的代理（有接口情况）
基于类的代理（无接口情况）


说明：

​ AspectJ：是AOP思想的一种实现。本质上是静态代理，将代理逻辑“织入”被代理的目标类编译得到的字节码文件，所以最终效果是动态的。weaver就是织入器。Spring只是借用了AspectJ中的注解。



说明：

当动态代理是基于接口的代理情况时，此种方式是JDK原生的实现方式。需要被代理的目标类必须**实现接口。因为这个技术要求代理对象和目标对象实现同样的接口**
当动态代理是基于类的代理情况时，通过**继承被代理的目标类**实现代理。因此不需要目标类实现接口
补充：

JDK动态代理动态生成的代理类会在com.sun.proxy包下，类名为$proxy1，和目标类实现相同的接口
cglib动态代理动态生成的代理类会和目标在在相同的包下，会继承目标类
6.2.3.2基本用例-实现动态代理
步骤一：创建ProxyFactory类

public class ProxyFactory {

    private Object target;

    public ProxyFactory(Object target) {
        this.target = target;
    }

    public Object getProxy(){
        /**
         * newProxyInstance()：创建一个代理实例
         * 其中有三个参数：
         * 1、classLoader：加载动态生成的代理类的类加载器
         * 2、interfaces：目标对象实现的所有接口的class对象所组成的数组
         * 3、invocationHandler：设置代理对象实现目标对象方法的过程，即代理类中如何重写接口中的抽象方法
         */
        ClassLoader classLoader = target.getClass().getClassLoader();
        Class<?>[] interfaces = target.getClass().getInterfaces();
        InvocationHandler invocationHandler = new InvocationHandler() {
            @Override
            public Object invoke(Object proxy, Method method, Object[] args) throws Throwable {
                /**
                 * proxy：代理对象
                 * method：代理对象需要实现的方法，即其中需要重写的方法
                 * args：method所对应方法的参数
                 */
                Object result = null;
                try {
                    System.out.println("[动态代理][日志] "+method.getName()+"，参数："+ Arrays.toString(args));
                    result = method.invoke(target, args);
                    System.out.println("[动态代理][日志] "+method.getName()+"，结果："+ result);
                } catch (Exception e) {
                    e.printStackTrace();
                    System.out.println("[动态代理][日志] "+method.getName()+"，异常："+e.getMessage());
                } finally {
                    System.out.println("[动态代理][日志] "+method.getName()+"，方法执行完毕");
                }
                return result;
            }
        };

        return Proxy.newProxyInstance(classLoader, interfaces, invocationHandler);
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
说明：

动态代理需要使用Proxy.newProxyInstance()方法
需要设置代理对象实现目标对象的方法过程
步骤二：演示

@Test
public void testDynamicProxy(){
    ProxyFactory factory = new ProxyFactory(new CalculatorLogImpl());
    Calculator proxy = (Calculator) factory.getProxy();
    proxy.div(1,0);
    //proxy.div(1,1);
}
1
2
3
4
5
6
7
6.3切入点表达式
​ 在 AOP 中，切入点表达式指定了哪些方法需要被织入增强逻辑。它是一个表达式，用于匹配目标对象中的方法，并提供切入点的精确定义



说明：

​ 在切入点表达式语法中，用*号代替“权限修饰符”和“返回值”部分表示“权限修饰符”和“返回值”不限

6.4基于注解的AOP
笔记小结：

概述：在Java类、方法、参数等上添加注解的方式来实现切面的定义和应用

基本用例：

步骤一：导入依赖

步骤二：创建切面类（需要选择通知方式）

步骤三：添加xml配置文件

通知方式：

前置通知：@Before
异常通知：@AfterThrowing
返回通知：@AfterReturning
后置通知：@After
环绕通知：@Around
获取通知信息

获取连接点：在方法中使用JoinPoint即可获取连接点信息

public void beforeMethod(JoinPoint joinPoint)
1
获取目标对象的返回值：在目标对象的返回通知上添加returning属性

@AfterReturning(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", returning = "result")
public void afterReturningMethod(JoinPoint joinPoint, Object result)
1
2
获取目标对象的异常：在目标对象的异常通知上添加throwing属性

@AfterThrowing(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", throwing = "ex")
public void afterThrowingMethod(JoinPoint joinPoint, Throwable ex)
1
2
重用切入点表达式

声明：在空参、空方法体、空返回值的方法上使用**@Pointcut**注解

@Pointcut("execution(* com.atguigu.aop.annotation.*.*(..))")
public void pointCut(){}
1
2
同切面使用：在同一切面中直接引用即可

@Before("pointCut()")
1
不同切面使用：在不同切面中

@Before("com.atguigu.aop.CommonPointCut.pointCut()")
1
6.4.1概述
​ 基于注解的AOP是一种AOP的实现方式，它通过在Java类、方法、参数等上添加注解的方式来实现切面的定义和应用，相比于传统的XML配置方式更加便捷和灵活

6.4.2基本用例-注解实现AOP
步骤一：导入依赖

 <!--spring aop依赖-->
    <dependency>
        <groupId>org.springframework</groupId>
        <artifactId>spring-aop</artifactId>
        <version>6.0.2</version>
    </dependency>
    <!--spring aspects依赖-->
    <dependency>
        <groupId>org.springframework</groupId>
        <artifactId>spring-aspects</artifactId>
        <version>6.0.2</version>
    </dependency>
1
2
3
4
5
6
7
8
9
10
11
12
步骤二：创建接口以及实现类

1.接口

public interface Calculator {
    int add(int i, int j); 
}
1
2
3
2.实现类

@Component
public class CalculatorImpl implements Calculator {

    @Override
    public int add(int i, int j) {
        int result = i + j;
        System.out.println("方法内部 result = " + result);
        return result;
    }
}
1
2
3
4
5
6
7
8
9
10
说明：

​ 此实现类，也需要添加@Component注解，便于Spring容器进行管理

步骤三：创建切面类

@Aspect
@Component
public class LogAspect {
    // 前置通知
    // 异常通知
    // 返回通知
    // 后置通知
    // 环绕通知
    ……
}
1
2
3
4
5
6
7
8
9
10
注意：

​ 此处需要配置切面类的通知方式！

说明：

@Aspect表示这个类是一个切面类
@Component注解保证这个切面类能够放入IOC容器
步骤四：配置Spring配置文件

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:context="http://www.springframework.org/schema/context"
       xmlns:aop="http://www.springframework.org/schema/aop"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
       http://www.springframework.org/schema/beans/spring-beans.xsd
       http://www.springframework.org/schema/context
       http://www.springframework.org/schema/context/spring-context.xsd
       http://www.springframework.org/schema/aop
       http://www.springframework.org/schema/aop/spring-aop.xsd">
    <!--
        基于注解的AOP的实现：
        1、将目标对象和切面交给IOC容器管理（注解+扫描）
        2、开启AspectJ的自动代理，为目标对象自动生成代理
        3、将切面类通过注解@Aspect标识
    -->
    <context:component-scan base-package="com.atguigu.aop.annotation"></context:component-scan>

    <aop:aspectj-autoproxy />
</beans>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
补充：

​ 当学习了SpringBoot后，通过SpringBoot来实现AOP，可省略此文件。因为SpringBoot以实现包扫描和切面标识

步骤五：演示

@Test
public void testAdd(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("beans.xml");
    Calculator calculator = ac.getBean( Calculator.class);
    int add = calculator.add(1, 1);
}
1
2
3
4
5
6
说明：

​

6.4.3通知方式
6.4.3.1前置通知
使用@Before注解标识，在被代理的目标方法前执行

@Before("execution(public int com.atguigu.aop.annotation.CalculatorImpl.*(..))")
public void beforeMethod(JoinPoint joinPoint){
    // getSignature（）获取连接点签名，getName（）获取连接点名称
    String methodName = joinPoint.getSignature().getName();
    String args = Arrays.toString(joinPoint.getArgs());
    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);
}
1
2
3
4
5
6
7
说明：

@Before注解内为切入点表达式
JoinPoint 是指程序执行过程中明确的点，比如方法的调用或异常的处理。JoinPoint 提供了一个可供切面通知获取方法的关键信息的方式
6.4.3.2异常通知
使用@AfterThrowing注解标识，在被代理的目标方法异常结束后执行

@AfterThrowing(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", throwing = "ex")
public void afterThrowingMethod(JoinPoint joinPoint, Throwable ex){
    String methodName = joinPoint.getSignature().getName();
    System.out.println("Logger-->异常通知，方法名："+methodName+"，异常："+ex);
}

1
2
3
4
5
6
说明：

​ @AfterThrowing注解内为切入点表达式

6.4.3.3返回通知
使用@AfterReturning注解标识，在被代理的目标方法成功结束后执行

@AfterReturning(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", returning = "result")
public void afterReturningMethod(JoinPoint joinPoint, Object result){
    String methodName = joinPoint.getSignature().getName();
    System.out.println("Logger-->返回通知，方法名："+methodName+"，结果："+result);
}

1
2
3
4
5
6
说明：

​ @AfterReturning注解内为切入点表达式

6.4.3.4后置通知
使用@After注解标识，在被代理的目标方法最终结束后执行

  @After("execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))")
    public void afterMethod(JoinPoint joinPoint){
        String methodName = joinPoint.getSignature().getName();
        System.out.println("Logger-->后置通知，方法名："+methodName);
    }

1
2
3
4
5
6
说明：

​ @After注解内为切入点表达式

6.4.3.5环绕通知
使用@Around注解标识，使用try…catch…finally结构围绕整个被代理的目标方法，包括上面四种通知对应的所有位置

@Around("execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))")
public Object aroundMethod(ProceedingJoinPoint joinPoint){
    String methodName = joinPoint.getSignature().getName();
    String args = Arrays.toString(joinPoint.getArgs());
    Object result = null;
    try {
        System.out.println("环绕通知-->目标对象方法执行之前");
        //目标对象（连接点）方法的执行
        result = joinPoint.proceed();
        System.out.println("环绕通知-->目标对象方法返回值之后");
    } catch (Throwable throwable) {
        throwable.printStackTrace();
        System.out.println("环绕通知-->目标对象方法出现异常时");
    } finally {
        System.out.println("环绕通知-->目标对象方法执行完毕");
    }
    return result;
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
说明：

@Around注解内为切入点表达式
ProceedingJoinPoint 继承自 JoinPoint 接口，是用于环绕通知的特殊类型的 JoinPoint，它可以用于在通知中控制目标方法的执行。在环绕通知中，ProceedingJoinPoint 提供了一个 proceed() 方法，该方法会执行目标方法，并返回其结果。
6.4.4获取通知信息
6.4.4.1获取连接点信息
在任何通知方式中，获取连接点信息可以在通知方法的参数位置设置JoinPoint类型的形参

@Before("execution(public int com.atguigu.aop.annotation.CalculatorImpl.*(..))")
public void beforeMethod(JoinPoint joinPoint){
    //获取连接点的签名信息
    String methodName = joinPoint.getSignature().getName();
    //获取目标方法到的实参信息
    String args = Arrays.toString(joinPoint.getArgs());
    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);
}
1
2
3
4
5
6
7
8
6.4.4.2获取目标方法的返回值
@AfterReturning中的属性returning，用来将通知方法的某个形参，接收目标方法的返回值

@AfterReturning(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", returning = "result")
public void afterReturningMethod(JoinPoint joinPoint, Object result){
    String methodName = joinPoint.getSignature().getName();
    System.out.println("Logger-->返回通知，方法名："+methodName+"，结果："+result);
}
1
2
3
4
5
6.4.4.3获取目标方法的异常
@AfterThrowing中的属性throwing，用来将通知方法的某个形参，接收目标方法的异常

@AfterThrowing(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", throwing = "ex")
public void afterThrowingMethod(JoinPoint joinPoint, Throwable ex){
    String methodName = joinPoint.getSignature().getName();
    System.out.println("Logger-->异常通知，方法名："+methodName+"，异常："+ex);
}
1
2
3
4
5
6.4.5重用切入点表达式
说明：

​ 切入点表达式可参考本节面向切面：AOP中的概述部分

简化切入点的书写

6.4.5.1声明
@Pointcut("execution(* com.atguigu.aop.annotation.*.*(..))")
public void pointCut(){}
1
2
6.4.5.2同切面使用
@Before("pointCut()")
public void beforeMethod(JoinPoint joinPoint){
    String methodName = joinPoint.getSignature().getName();
    String args = Arrays.toString(joinPoint.getArgs());
    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);
}
1
2
3
4
5
6
6.4.5.3不同切面使用
@Before("com.atguigu.aop.CommonPointCut.pointCut()")
public void beforeMethod(JoinPoint joinPoint){
    String methodName = joinPoint.getSignature().getName();
    String args = Arrays.toString(joinPoint.getArgs());
    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);
}
1
2
3
4
5
6
6.5基于XML的AOP（了解）
<context:component-scan base-package="com.atguigu.aop.xml"></context:component-scan>

<aop:config>
    <!--配置切面类-->
    <aop:aspect ref="loggerAspect">
        <aop:pointcut id="pointCut" 
                   expression="execution(* com.atguigu.aop.xml.CalculatorImpl.*(..))"/>
        <aop:before method="beforeMethod" pointcut-ref="pointCut"></aop:before>
        <aop:after method="afterMethod" pointcut-ref="pointCut"></aop:after>
        <aop:after-returning method="afterReturningMethod" returning="result" pointcut-ref="pointCut"></aop:after-returning>
        <aop:after-throwing method="afterThrowingMethod" throwing="ex" pointcut-ref="pointCut"></aop:after-throwing>
        <aop:around method="aroundMethod" pointcut-ref="pointCut"></aop:around>
    </aop:aspect>
</aop:config>
1
2
3
4
5
6
7
8
9
10
11
12
13
14
知识加油站
1.自动装配和依赖注入的区别与联系
​ 依赖注入（Dependency Injection） 是一种设计模式，旨在通过将依赖关系从一个对象传递给另一个对象，来实现对象之间的解耦。在Spring中，依赖注入通过容器来管理和传递对象之间的依赖关系，而不是由对象自身来创建或管理它们的依赖。这可以通过构造函数注入、Setter方法注入或字段注入等方式来实现

​ 自动装配（Autowired） 是Spring Framework提供的一种依赖注入的方式，用于自动将合适的依赖注入到相应的位置，无需手动指定每个依赖的注入方式。通过使用@Autowired注解，Spring会自动在容器中查找匹配的依赖，并将其注入到需要的位置

总结：

自动装配是Spring框架的特性，用于自动连接应用程序中的组件。
依赖注入是自动装配的一种具体实现方式，使用**@Autowired注解来标识需要自动注入**的属性、构造函数或方法参数。
2.依赖注入的两种方式
依赖注入（Dependency Injection）有两种常见的方式：

构造函数注入（Constructor Injection）：通过构造函数来注入依赖对象。在目标类的构造函数中声明参数，并在创建目标对象时通过构造函数传入依赖对象。这种方式可以保证依赖对象在目标对象创建时就被传入，从而确保了目标对象的完整性和一致性。
Setter方法注入（Setter Injection）：通过Setter方法来注入依赖对象。在目标类中定义对应的Setter方法，并在方法中接收依赖对象作为参数，通过调用Setter方法来注入依赖对象。这种方式可以在目标对象创建后动态地设置依赖对象，灵活性较高。
————————————————

                            版权声明：本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。
                        
原文链接：https://blog.csdn.net/D_boj/article/details/132286492>)](<文章目录
1.概述
1.1定义
1.2作用
1.3简介
1.4狭义和广义
1.5模块组成
1.5.1Spring Core（核心容器）
1.5.2Spring AOP（面向切面编程）
1.5.3Spring Data Access（数据访问）
1.5.4Spring Web（应用程序）
1.5.5Spring Message（消息传递）
1.5.6Spring test（测试）
1.6Spring Framework（框架）
1.6.1概述
1.6.2作用
1.6.3特点
1.7 特点
2.基本用例-Spring框架基本使用
3.原理
4.启用日志框架
4.1概述
4.2组成
4.3基本用例-Log4j2基本使用
5.容器：IoC（重点）
5.1概述
5.1.1定义
5.1.2简介
5.1.3作用
5.1.4依赖注入
5.1.4.1定义
5.1.4.2作用
5.1.4.3实现方式
5.1.5实现
5.2基于XML管理Bean（了解）
5.2.1获取Bean的方式
5.2.1.1根据ID获取Bean
5.2.1.2根据类型获取Bean
5.2.1.3根据Id和类型获取Bean
5.2.2依赖注入
5.2.2.1根据setter注入
5.2.2.2根据构造器注入
5.2.3特殊值处理
5.2.3.1字面量赋值
5.2.3.2null值
5.2.3.3xml实体
5.2.3.4CDATA节
5.2.4注入对象类型属性值
5.2.4.1引用外部Bean
5.2.4.2引用内部Bean
5.2.4.3级联属性赋值
5.2.5注入数组类型属性值
5.2.6注入集合类型属性值
5.2.6.1注入List集合类型属性值
5.2.6.2注入Map集合类型属性值
5.2.6.2注入引用集合类型属性值
5.2.7引入P命名空间属性值
5.2.8引入外部属性文件
5.2.9引入Bean的作用域
5.2.10Bean的生命周期
5.2.11引入FactoryBean属性值
5.2.12引入xml自动装配
5.3基于注解管理Bean（重点）
5.3.1概述
5.3.1.1简介
5.3.1.2步骤
5.3.1.3使用注解
5.3.2开启组件扫描
5.3.2.1概述
5.3.2.2基本用例-实现组件扫描
5.3.2.3指定要排除的组件
5.3.2.4仅扫描指定组件
5.3.2使用注解定义Bean
5.3.3使用@Autowired注入
5.3.3.1概述
5.3.3.2属性注入
5.3.3.3set注入
5.3.3.4构造方法注入
5.3.3.5形参注入
5.3.3.6无注解注入
5.3.3.7联合@Qualifier注解注入
5.3.4使用@Resource注入
5.3.4.1概述
5.3.4.2Name注入
5.3.4.3未知Name注入
5.3.4.4类型注入
5.3.5全注解开发
5.3.5.1概述
5.3.5.2基本用例-全注解开发实现
5.4原理
6.面向切面：AOP (重点)
6.1概述
6.1.1定义
6.1.2作用
6.1.3横切关注点
6.1.4通知（增强）
6.1.5切面
6.1.6目标
6.1.7代理
6.1.8连接点
6.1.9切入点
6.2代理模式
6.2.1概述
6.2.2静态代理
6.2.3动态代理
6.2.3.1概述
6.2.3.1.1定义
6.2.3.1.2分类
6.2.3.2基本用例-实现动态代理
6.3切入点表达式
6.4基于注解的AOP
6.4.1概述
6.4.2基本用例-注解实现AOP
6.4.3通知方式
6.4.3.1前置通知
6.4.3.2异常通知
6.4.3.3返回通知
6.4.3.4后置通知
6.4.3.5环绕通知
6.4.4获取通知信息
6.4.4.1获取连接点信息
6.4.4.2获取目标方法的返回值
6.4.4.3获取目标方法的异常
6.4.5重用切入点表达式
6.4.5.1声明
6.4.5.2同切面使用
6.4.5.3不同切面使用
6.5基于XML的AOP（了解）
知识加油站
1.自动装配和依赖注入的区别与联系
2.依赖注入的两种方式
1.概述
笔记小结：

含义：Spring 是一款主流的 Java EE 轻量级开源框架，包含Spring MVC、Spring Boot、Spring Cloud等
作用：简化 Java 企业级应用的开发难度和开发周期，提供了整合其他技术和框架的能力
简介：核心功能是控制反转(IoC)和面向切面(AOP)
组成：
Spring Core（核心容器）
Spring AOP（面向切面编程）
Spring **Data Access（**数据访问）
Spring Web（应用程序）
Spring Message（消息传递）
Spring test（测试）
Spring Framework（框架）
概述：Spring Framework是Spring项目的核心框架
作用：Spring Framework实现IOC容器和AOP技术的功能模块
特点：
非侵入式
控制反转
面向切面编程
容器
组件化
特点：
轻：框架轻量级，不依赖其余Spring的对象
控制反转（IOC）：实现了对象之间的松耦合
面向切面（AOP）：分离应用的业务逻辑与系统级服务
容器：Spring包含并管理应用对象的配置和生命周期
1.1定义
​ Spring 是一款主流的 Java EE 轻量级开源框架 ，由于其轻便、易用和高效，被广泛应用于企业级Java应用开发中。

​ Spring包含了很多子框架和扩展，如Spring MVC、Spring Boot、Spring Cloud等。

​ Spring的主要特点是IOC容器和AOP技术，它们使得Java应用的开发和管理更加简单和高效。

1.2作用
​ Spring 目的是用于简化 Java 企业级应用的开发难度和开发周期。Spring 框架除了自己提供功能外，还提供整合其他技术和框架的能力

1.3简介
​ 自 2004 年 4 月，Spring 1.0 版本正式发布以来，Spring 已经步入到了第 6 个大版本，也就是 Spring 6。



说明：

​ 参考链接：Spring Framework

Spring是一个轻量级的控制反转(IoC)和面向切面(AOP)的容器框架。
Spring最初的出现是为了解决EJB臃肿的设计，以及难以测试等问题。
Spring为简化开发而生，让程序员只需关注核心业务的实现，尽可能的不再关注非业务逻辑代码（事务控制，安全日志等）。
1.4狭义和广义
广义的 Spring：Spring 技术栈
​ 广义上的 Spring 泛指以 Spring Framework 为核心的 Spring 技术栈。

​ 经过十多年的发展，Spring 已经不再是一个单纯的应用框架，而是逐渐发展成为一个由多个不同子项目（模块）组成的成熟技术，例如 Spring Framework、Spring MVC、SpringBoot、Spring Cloud、Spring Data、Spring Security 等，其中 Spring Framework 是其他子项目的基础。

​ 这些子项目涵盖了从企业级应用开发到云计算等各方面的内容，能够帮助开发人员解决软件发展过程中不断产生的各种实际问题，给开发人员带来了更好的开发体验。

狭义的 Spring：Spring Framework
​ 狭义的 Spring 特指 Spring Framework，通常我们将它称为 Spring 框架。

​ Spring 框架是一个分层的、面向切面的 Java 应用程序的一站式轻量级解决方案，它是 Spring 技术栈的核心和基础，是为了解决企业级应用开发的复杂性而创建的。

Spring 有两个最核心模块： IoC 和 AOP。

IoC：Inverse of Control 的简写，译为“控制反转”，指把创建对象过程交给 Spring 进行管理。
AOP：Aspect Oriented Programming 的简写，译为“面向切面编程”。AOP 用来封装多个类的公共行为，将那些与业务无关，却为业务模块所共同调用的逻辑封装起来，减少系统的重复代码，降低模块间的耦合度。另外，AOP 还解决一些系统层面上的问题，比如日志、事务、权限等。
1.5模块组成


说明：

​ 上图中包含了 Spring 框架的所有模块，这些模块可以满足一切企业级应用开发的需求，在开发过程中可以根据需求有选择性地使用所需要的模块。下面分别对这些模块的作用进行简单介绍。

1.5.1Spring Core（核心容器）
​ spring core提供了IOC,DI,Bean配置装载创建的核心实现。核心概念： Beans、BeanFactory、BeanDefinitions、ApplicationContext。

spring-core ：IOC和DI的基本实现

spring-beans：BeanFactory和Bean的装配管理(BeanFactory)

spring-context：Spring context上下文，即IOC容器(AppliactionContext)

spring-expression：spring表达式语言

1.5.2Spring AOP（面向切面编程）
spring-aop：面向切面编程的应用模块，整合ASM，CGLib，JDK Proxy
spring-aspects：集成AspectJ，AOP应用框架
spring-instrument：动态Class Loading模块
1.5.3Spring Data Access（数据访问）
spring-jdbc：spring对JDBC的封装，用于简化jdbc操作
spring-orm：java对象与数据库数据的映射框架
spring-oxm：对象与xml文件的映射框架
spring-jms： Spring对Java Message Service(java消息服务)的封装，用于服务之间相互通信
spring-tx：spring jdbc事务管理
1.5.4Spring Web（应用程序）
spring-web：最基础的web支持，建立于spring-context之上，通过servlet或listener来初始化IOC容器
spring-webmvc：实现web mvc
spring-websocket：与前端的全双工通信协议
spring-webflux：Spring 5.0提供的，用于取代传统java servlet，非阻塞式Reactive Web框架，异步，非阻塞，事件驱动的服务
1.5.5Spring Message（消息传递）
Spring-messaging：spring 4.0提供的，为Spring集成一些基础的报文传送服务
1.5.6Spring test（测试）
spring-test：集成测试支持，主要是对junit的封装
1.6Spring Framework（框架）
1.6.1概述
​ Spring Framework是Spring项目的核心框架，而Spring是整个Spring项目的总称，包括了Spring Framework和其他相关的子项目和扩展



1.6.2作用
​ Spring Framework实现IOC容器和AOP技术的功能模块

​ Spring Framework包含了许多模块，如Core模块、Beans模块、Context模块、AOP模块、Web模块等，每个模块都提供了不同的功能，可以灵活地选择使用。Spring Framework的目标是为了简化企业级Java开发，提高开发效率和质量。

1.6.3特点
非侵入式：使用 Spring Framework 开发应用程序时，Spring 对应用程序本身的结构影响非常小。对领域模型可以做到零污染；对功能性组件也只需要使用几个简单的注解进行标记，完全不会破坏原有结构，反而能将组件结构进一步简化。这就使得基于 Spring Framework 开发应用程序时结构清晰、简洁优雅。

控制反转：IoC——Inversion of Control，翻转资源获取方向。把自己创建资源、向环境索取资源变成环境将资源准备好，我们享受资源注入。

面向切面编程：AOP——Aspect Oriented Programming，在不修改源代码的基础上增强代码功能。

容器：Spring IoC 是一个容器，因为它包含并且管理组件对象的生命周期。组件享受到了容器化的管理，替程序员屏蔽了组件创建过程中的大量细节，极大的降低了使用门槛，大幅度提高了开发效率。

组件化：Spring 实现了使用简单的组件配置组合成一个复杂的应用。在 Spring 中可以使用 XML 和 Java 注解组合这些对象。这使得我们可以基于一个个功能明确、边界清晰的组件有条不紊的搭建超大型复杂应用系统。

一站式：在 IoC 和 AOP 的基础上可以整合各种企业应用的开源框架和优秀的第三方类库。而且 Spring 旗下的项目已经覆盖了广泛领域，很多方面的功能性需求可以在 Spring Framework 的基础上全部使用 Spring 来实现。

1.7 特点
轻
从大小与开销两方面而言Spring都是轻量的。完整的Spring框架可以在一个大小只有1MB多的JAR文件里发布。并且Spring所需的处理开销也是微不足道的。
Spring是非侵入式的：Spring应用中的对象不依赖于Spring的特定类。
控制反转
Spring通过一种称作控制反转（IoC）的技术促进了松耦合。当应用了IoC，一个对象依赖的其它对象会通过被动的方式传递进来，而不是这个对象自己创建或者查找依赖对象。你可以认为IoC与JNDI相反——不是对象从容器中查找依赖，而是容器在对象初始化时不等对象请求就主动将依赖传递给它。
面向切面
Spring提供了面向切面编程的丰富支持，允许通过分离应用的业务逻辑与系统级服务（例如审计（auditing）和事务（transaction）管理）进行内聚性的开发。应用对象只实现它们应该做的——完成业务逻辑——仅此而已。它们并不负责（甚至是意识）其它的系统级关注点，例如日志或事务支持。
容器
Spring包含并管理应用对象的配置和生命周期，在这个意义上它是一种容器，你可以配置你的每个bean如何被创建——基于一个可配置原型（prototype），你的bean可以创建一个单独的实例或者每次需要时都生成一个新的实例——以及它们是如何相互关联的。然而，Spring不应该被混同于传统的重量级的EJB容器，它们经常是庞大与笨重的，难以使用。
框架
Spring可以将简单的组件配置、组合成为复杂的应用。在Spring中，应用对象被声明式地组合，典型地是在一个XML文件里。Spring也提供了很多基础功能（事务管理、持久化框架集成等等），将应用逻辑的开发留给了你。
说明：

​ 所有Spring的这些特征使你能够编写更干净、更可管理、并且更易于测试的代码。它们也为Spring中的各种模块提供了基础支持。

Spring6要求JDK最低版本是JDK17


2.基本用例-Spring框架基本使用
说明：

​ 本基本用例演示，通过XML方式，实现Bean的自动注入

补充：环境

JDK：Java17+（Spring6要求JDK最低版本是Java17）

Maven：3.6+

Spring：6.0.2

步骤一：构建模块

通过Idea开发工具，创建空项目后创建子模块


说明：

​ 在空项目中，创建子模块

步骤二：导入依赖

修改模块的pom.xml文件
%3Cdependencies%3E
    <!--spring context依赖-->
    <!--当你引入Spring Context依赖之后，表示将Spring的基础依赖引入了-->
    <dependency>
        <groupId>org.springframework</groupId>
        <artifactId>spring-context</artifactId>
        <version>6.0.2</version>
    </dependency>

    <!--junit5测试-->
    <!--此依赖可选，主要便于junit进行测试使用-->
    <dependency>
        <groupId>org.junit.jupiter</groupId>
        <artifactId>junit-jupiter-api</artifactId>
        <version>5.3.1</version>
    </dependency>
</dependencies>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
说明：

​ 在pom.xml文件中，添加如上依赖

补充：

添加完成后，可在IDEA工具中的最右侧点击Maven进行查看


步骤三：创建实体

package org.example.entity;

public class User {
    public void add() {
        System.out.println("add……");
    }
}

1
2
3
4
5
6
7
8
说明：

​ 在org.example.entity包下，创建User实体

步骤四：创建配置文件

在模块的resources目录下，创建beans.xml文件
说明：

​ 创建beans.xml文件，是为了完成通过xml的方式实现依赖的自动注入

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd">

    <!--id是该bean的唯一标识符，在整个应用程序上下文中用于获取该bean实例-->
    <!--class是该bean所属的Java类的全限定名（包括包名），它告诉Spring需要实例化哪个类-->
    <bean id="user" class="org.example.entity.User"/>
</beans>
1
2
3
4
5
6
7
8
9
说明：

在beans,xml文件中，有bean标签
在beans,xml文件中，bean标签有Id属性，与class属性
步骤五：演示

在模块中的test.java包下，创建UserTest类
public class UserTest {
    @Test
    void newTest() {
        ApplicationContext applicationContext = new ClassPathXmlApplicationContext("beans.xml");
        User user = (User) applicationContext.getBean("user");
        user.add(); // add……
    }
}
1
2
3
4
5
6
7
8
补充：

@Test 是 JUnit 框架中的一个注解，表示该方法是一个测试方法，会被 JUnit 框架执行。

3.原理
笔记小结：通过XML方式，实现Bean的自动注入的基本用例原理

创建对象时，会调用无参构造方法
Spring 是通过反射机制调用无参构造方法创建对象
Spring 创建的对象（Bean对象），最终存储在Spring容器中
1.创建对象时，会调用无参构造方法

public class HelloWorld {
    public HelloWorld() {
        System.out.println("无参数构造方法执行");
    }
    public void sayHello(){
        System.out.println("helloworld");
    }
}
1
2
3
4
5
6
7
8
说明：



2.Spring 是通过反射机制调用无参构造方法创建对象

// dom4j解析beans.xml文件，从中获取class属性值，类的全类名
// 通过反射机制调用无参数构造方法创建对象
Class clazz = Class.forName("com.atguigu.spring6.bean.HelloWorld");
//Object obj = clazz.newInstance();
Object object = clazz.getDeclaredConstructor().newInstance();
1
2
3
4
5
3.Spring 创建的对象（Bean对象），最终存储在Spring容器中

private final Map<String, BeanDefinition> beanDefinitionMap = new ConcurrentHashMap<>(256);
1
说明：

Spring容器底层就是一个map集合
存储bean的map在DefaultListableBeanFactory类中
Spring容器加载到Bean类时 , 会把这个类的描述信息, 以包名加类名的方式存到beanDefinitionMap 中
Map<String,BeanDefinition> , 其中 String是Key , 默认是类名首字母小写 。BeanDefinition , 存的是类的定义(描述信息) , 我们通常叫BeanDefinition接口为 : bean的定义对象。
4.启用日志框架
笔记小结：

概述：Log4j2是一个开源的Java日志框架，帮助Java开发人员在应用程序中实现灵活和可配置的日志记录

组成：

日志信息的优先级：TRACE < DEBUG < INFO < WARN < ERROR < FATAL
日志信息的输出目的地：控制台或者本地文件
日志信息的输出格式：日志信息的显示内容
基本用例：

导入依赖：
<!--log4j2的依赖-->
<dependency>
  <groupId>org.apache.logging.log4j</groupId>
  <artifactId>log4j-core</artifactId>
  <version>2.19.0</version>
</dependency>
<dependency>
  <groupId>org.apache.logging.log4j</groupId>
  <artifactId>log4j-slf4j2-impl</artifactId>
  <version>2.19.0</version>
</dependency>
1
2
3
4
5
6
7
8
9
10
11
创建日志配置文件：建议复制根据需求修改

使用日志

private Logger logger = LoggerFactory.getLogger(HelloWorldTest.class);
……
logger.info("执行成功");
1
2
3
结果：



4.1概述
​ Log4j2是一个开源的Java日志框架，是Log4j的升级版。它可以帮助Java开发人员在应用程序中实现灵活和可配置的日志记录，支持异步日志记录、多线程安全等特性

4.2组成
日志信息的优先级，日志信息的优先级从高到低有TRACE < DEBUG < INFO < WARN < ERROR < FATAL

说明：

TRACE：追踪，是最低的日志级别，相当于追踪程序的执行
DEBUG：调试，一般在开发中，都将其设置为最低的日志级别
INFO：信息，输出重要的信息，使用较多
WARN：警告，输出警告的信息
ERROR：错误，输出错误信息
FATAL：严重错误
日志信息的输出目的地，日志信息的输出目的地指定了日志将打印到控制台还是文件中；

日志信息的输出格式，而输出格式则控制了日志信息的显示内容。

4.3基本用例-Log4j2基本使用
步骤一：引入Log4j2依赖

修改模块中的pom.xml文件
<!--log4j2的依赖-->
<dependency>
    <groupId>org.apache.logging.log4j</groupId>
    <artifactId>log4j-core</artifactId>
    <version>2.19.0</version>
</dependency>
<dependency>
    <groupId>org.apache.logging.log4j</groupId>
    <artifactId>log4j-slf4j2-impl</artifactId>
    <version>2.19.0</version>
</dependency>
1
2
3
4
5
6
7
8
9
10
11
说明：

​ log4j的Maven使用光有核心core依赖不够，还需要有实现impl依赖

步骤二：创建日志配置文件

在模块文件路径在resource的根路径下，配置文件名为log4j2.xml
<?xml version="1.0" encoding="UTF-8"?>
<configuration>
    <loggers>
        <!--
            level指定日志级别，从低到高的优先级：
                TRACE < DEBUG < INFO < WARN < ERROR < FATAL
                trace：追踪，是最低的日志级别，相当于追踪程序的执行
                debug：调试，一般在开发中，都将其设置为最低的日志级别
                info：信息，输出重要的信息，使用较多
                warn：警告，输出警告的信息
                error：错误，输出错误信息
                fatal：严重错误
        -->
        <root level="DEBUG">
            <appender-ref ref="spring6log"/>
            <appender-ref ref="RollingFile"/>
            <appender-ref ref="log"/>
        </root>
    </loggers>

    <appenders>
        <!--输出日志信息到控制台-->
        <console name="spring6log" target="SYSTEM_OUT">
            <!--控制日志输出的格式-->
            <PatternLayout pattern="%d{yyyy-MM-dd HH:mm:ss SSS} [%t] %-3level %logger{1024} - %msg%n"/>
        </console>

        <!--文件会打印出所有信息，这个log每次运行程序会自动清空，由append属性决定，适合临时测试用-->
        <File name="log" fileName="d:/spring6_log/test.log" append="false">
            <PatternLayout pattern="%d{HH:mm:ss.SSS} %-5level %class{36} %L %M - %msg%xEx%n"/>
        </File>

        <!-- 这个会打印出所有的信息，
            每次大小超过size，
            则这size大小的日志会自动存入按年份-月份建立的文件夹下面并进行压缩，
            作为存档-->
        <RollingFile name="RollingFile" fileName="d:/spring6_log/app.log"
                     filePattern="log/$${date:yyyy-MM}/app-%d{MM-dd-yyyy}-%i.log.gz">
            <PatternLayout pattern="%d{yyyy-MM-dd 'at' HH:mm:ss z} %-5level %class{36} %L %M - %msg%xEx%n"/>
            <SizeBasedTriggeringPolicy size="50MB"/>
            <!-- DefaultRolloverStrategy属性如不设置，
            则默认为最多同一文件夹下7个文件，这里设置了20 -->
            <DefaultRolloverStrategy max="20"/>
        </RollingFile>
    </appenders>
</configuration>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
步骤三：日常使用

在日常中，只用log4j2，此处创建HelloWorldTest使用
public class HelloWorldTest {

    // 1.通过日志工程获取日志对象记录器
    private Logger logger = LoggerFactory.getLogger(HelloWorldTest.class);
 
    @Test
    public void testHelloWorld(){
        ApplicationContext ac = new ClassPathXmlApplicationContext("beans.xml");
        HelloWorld helloworld = (HelloWorld) ac.getBean("helloWorld");
        helloworld.sayHello();
        // 2.记录日志
        logger.info("执行成功");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
说明：

​ 创建日志记录器

步骤四：演示



说明：

​ 当完成以上步骤后，运行，日志就会输出在控制台

5.容器：IoC（重点）
笔记小结：见各个小节

5.1概述
笔记小结：

定义：IoC (Inversion of Control)，即控制反转，是一种设计模式或者说设计思想
简介：Spring 通过 IoC 容器来管理所有 Java 对象的实例化和初始化，控制对象与对象之间的依赖关系
作用：通过容器来管理对象的创建、销毁、依赖注入等操作，而应用程序本身只需要使用这些对象即可
依赖注入:
含义：以解耦对象之间的依赖关系
作用：Spring通过依赖注入的方式来完成Bean管理的。换句话说，依赖注入，依赖注入实现了控制反转的思想
实现方式（重点）：
setter注入
构造注入
实现接口以及常用类：
BeanFactory接口：面向 Spring 本身，不提供给开发人员使用
ApplicationContext接口：面向 Spring 的使用者，几乎所有场合（创建、管理Bean实例，支持国际化、资源访问、消息传递）都适用
常用类：
FileSystemXmlApplicationContext：通过文件系统路径读取 XML 格式的配置文件创建 IOC 容器对象
ClassPathXmlApplicationContext：通过读取类路径下的 XML 格式的配置文件创建 IOC 容器对象
5.1.1定义
​ IoC (Inversion of Control)，即控制反转，是一种设计模式或者说设计思想，它是面向对象编程中的一种概念，用来描述对象之间的依赖关系，指导我们如何设计出松耦合、更优良的程序。

5.1.2简介
​ Spring 通过 IoC 容器来管理所有 Java 对象的实例化和初始化，控制对象与对象之间的依赖关系。我们将由 IoC 容器管理的 Java 对象称为 Spring Bean，它与使用关键字 new 创建的 Java 对象没有任何区别。

5.1.3作用
​ 在 IoC 模式中，控制权从程序代码中转移到了容器中，即通过容器来管理对象的创建、销毁、依赖注入等操作，而应用程序本身只需要使用这些对象即可。这样，应用程序就不需要自己管理对象之间的依赖关系，而是由容器来管理，从而实现了代码的解耦和更好的可维护性，提高程序扩展力。

说明：

将对象的创建权利交出去，交给第三方容器负责
将对象和对象之间关系的维护权交出去，交给第三方容器负责
5.1.4依赖注入
5.1.4.1定义
​ 依赖注入（Dependency Injection，DI）是一种设计模式，其主要思想是在程序运行的过程中，通过外部容器（如Spring容器）动态地将依赖对象注入到程序中，以解耦对象之间的依赖关系，从而提高程序的灵活性、可维护性和可测试性。

5.1.4.2作用
​ **Spring通过依赖注入的方式来完成Bean管理的。**换句话说，依赖注入，依赖注入实现了控制反转的思想。依赖指的是对象和对象之间的关联关系。注入指的是一种数据传递行为，通过注入行为来让对象和对象产生关系。

补充：

​ Bean管理说的是：Bean对象的创建，以及Bean对象中属性的赋值（或者叫做Bean对象之间关系的维护）。

5.1.4.3实现方式
第一种：set注入
第二种：构造注入
5.1.5实现
​ Spring 的框架中，IoC 容器是通过 BeanFactory 和 ApplicationContext 接口实现的。BeanFactory 接口是 Spring 框架最底层的接口，提供了基本的 IoC 功能；ApplicationContext 接口是 BeanFactory 接口的子接口，提供了更高级的特性和功能，如 AOP、国际化、事件驱动等。其中BeanFactory 接口，最重要的方法是getBean()方法，用于从容器中获取对象。

​ Spring 的 IoC 容器就是 IoC思想的一个落地的产品实现。IoC容器中管理的组件也叫做 bean。在创建 bean 之前，首先需要创建IoC 容器。Spring 提供了IoC 容器的两种实现方式：

BeanFactory：这是 IoC 容器的基本实现，是 Spring 内部使用的接口。面向 Spring 本身，不提供给开发人员使用。
ApplicationContext：BeanFactory 的子接口，提供了更多高级特性。面向 Spring 的使用者，几乎所有场合都使用 ApplicationContext 而不是底层的 BeanFactory
ApplicationContext的主要实现类:

类型名	简介
ClassPathXmlApplicationContext	通过读取类路径下的 XML 格式的配置文件创建 IOC 容器对象
FileSystemXmlApplicationContext	通过文件系统路径读取 XML 格式的配置文件创建 IOC 容器对象
ConfigurableApplicationContext	ApplicationContext 的子接口，包含一些扩展方法 refresh() 和 close() ，让 ApplicationContext 具有启动、关闭和刷新上下文的能力。
WebApplicationContext	专门为 Web 应用准备，基于 Web 环境创建 IOC 容器对象，并将对象引入存入 ServletContext 域中。


说明：

​ ApplicationContext有众多的实现类，其中最常用的就是ClassPathXmlApplicationContext与FileSystemXmlApplicationContext实现类

5.2基于XML管理Bean（了解）
笔记小结：

获取Bean的方式：

根据ID：

User user = (User) applicationContext.getBean("user");
1
根据类型：

 User user = (User) applicationContext.getBean(User.class);
1
根据Id和类型:

User user = (User) applicationContext.getBean("user", User.class);
1
依赖注入

根据Setter注入：<property/>
根据构造器注入：<constructor-arg/>
特殊值处理

字面量赋值<property>
Null值<null>
Xml实体：属性值value="a &lt; b"
CDATA节：标签内容<![CDATA[a < b]]>
注入对象类型属性值

引用外部Bean：属性ref
引用内部Bean：bean嵌套
级联属性赋值：引入对象后，级联赋值name="clazz.clazzId"
注入数组类型属性值：<array></array>

注入集合类型属性值：

注入List集合类型属性值： <list> </list>
注入Map集合类型属性值：<map><entry><<key>/key><value></value></entry></map>
注入引用集合类型属性值：<util></util>
注意：使用前，需要引入util命名空间
引入P命名空间属性值：属性p:

注意：使用前，需要引入p命名空间
引入外部属性文件：<context:property-placeholder location="classpath:jdbc.properties"/>

引入Bean的作用域：属性scope属性值prototype（多例）、singleton（单例）

Bean的生命周期：

bean对象创建（调用无参构造器）

bean对象设置属性

bean的后置处理器（初始化之前）

bean对象初始化（需在配置bean时指定初始化方法）

bean的后置处理器（初始化之后）

bean对象就绪可以使用

bean对象销毁（需在配置bean时指定销毁方法）

IOC容器关闭

引入FactoryBean属性值：实现FactoryBean<T>接口

引入自动装配：属性值autowire属性值byType、byName

5.2.1获取Bean的方式
5.2.1.1根据ID获取Bean
public class UserTest {
    @Test
    void newTest() {
        ApplicationContext applicationContext = new ClassPathXmlApplicationContext("beans.xml");
        User user = (User) applicationContext.getBean("user");
        user.add(); // add……
    }
}
1
2
3
4
5
6
7
8
说明：

​ 此获取方式，需要基于第2.基本用例进行查看

5.2.1.2根据类型获取Bean
public class UserTest {
    @Test
    void newTest() {
        ApplicationContext applicationContext = new ClassPathXmlApplicationContext("beans.xml");
        User user = (User) applicationContext.getBean(User.class);
        user.add(); // add……
    }
}
1
2
3
4
5
6
7
8
注意：

当根据类型获取bean时，要求IOC容器中指定类型的bean有且只能有一个

org.springframework.beans.factory.NoUniqueBeanDefinitionException: No qualifying bean of type 'com.atguigu.spring6.bean.HelloWorld' available: expected single matching bean but found 2: helloworldOne,helloworldTwo
1
说明：

​ 此获取方式，需要基于第2.基本用例进行查看

5.2.1.3根据Id和类型获取Bean
public class UserTest {
    @Test
    void newTest() {
        ApplicationContext applicationContext = new ClassPathXmlApplicationContext("beans.xml");
        User user = (User) applicationContext.getBean("user", User.class);
        user.add(); // add……
    }
}
1
2
3
4
5
6
7
8
补充：

​ 如果组件类实现了接口，可以根据接口类型获取Bean，但前提是Bean唯一

说明：

​ 此获取方式，需要基于第2.基本用例进行查看

5.2.2依赖注入
5.2.2.1根据setter注入
步骤一：创建学生类Student

package com.atguigu.spring6.bean;

public class Student {

    private Integer id;

    private String name;

    private Integer age;

    private String sex;

    public Student() {
    }

    public Integer getId() {
        return id;
    }

    public void setId(Integer id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public Integer getAge() {
        return age;
    }

    public void setAge(Integer age) {
        this.age = age;
    }

    public String getSex() {
        return sex;
    }

    public void setSex(String sex) {
        this.sex = sex;
    }

    @Override
    public String toString() {
        return "Student{" +
                "id=" + id +
                ", name='" + name + '\'' +
                ", age=" + age +
                ", sex='" + sex + '\'' +
                '}';
    }

}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
步骤二：配置bean时为属性赋值

<bean id="studentOne" class="com.atguigu.spring6.bean.Student">
    <!-- property标签：通过组件类的setXxx()方法给组件对象设置属性 -->
    <!-- name属性：指定属性名（这个属性名是getXxx()、setXxx()方法定义的，和成员变量无关） -->
    <!-- value属性：指定属性值 -->
    <property name="id" value="1001"></property>
    <property name="name" value="张三"></property>
    <property name="age" value="23"></property>
    <property name="sex" value="男"></property>
</bean>
1
2
3
4
5
6
7
8
9
说明：

​ 当使用标签标签完成对象的属性创建时，name需要跟对象中的成员变量同名

步骤三：演示

@Test
public void testDIBySet(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-di.xml");
    Student studentOne = ac.getBean("studentOne", Student.class);
    System.out.println(studentOne);
}
1
2
3
4
5
6
说明：

​ 当打印输出是，由于基于XML根据Setter注入方式进行对象的创建，此时输出可获得成员方法tostring的内容

5.2.2.2根据构造器注入
步骤一：在基于根据setter注入的基础上，在Student类中添加有参构造

public Student(Integer id, String name, Integer age, String sex) {
    this.id = id;
    this.name = name;
    this.age = age;
    this.sex = sex;
}
1
2
3
4
5
6
步骤二：配置bean

<bean id="studentTwo" class="com.atguigu.spring6.bean.Student">
    <constructor-arg name="id" value="1002"></constructor-arg>
    <constructor-arg name="name" value="李四"></constructor-arg>
    <constructor-arg name="age"value="33"></constructor-arg>
    <constructor-arg name="sex" value="女"></constructor-arg>
</bean>
1
2
3
4
5
6
说明：

constructor-arg标签属性描述构造器参数：
index属性：指定参数所在位置的索引（从0开始）
name属性：指定参数名，name需要跟对象中的成员变量同名
步骤三：演示

@Test
public void testDIByConstructor(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-di.xml");
    Student studentOne = ac.getBean("studentTwo", Student.class);
    System.out.println(studentOne);
}
1
2
3
4
5
6
说明：

​ 当打印输出是，由于基于XML根据构造器注入方式进行对象的创建，此时输出可获得成员方法tostring的内容

5.2.3特殊值处理
5.2.3.1字面量赋值
<!-- 使用value属性给bean的属性赋值时，Spring会把value属性的值看做字面量 -->
<property name="name" value="张三"/>
1
2
5.2.3.2null值
<property name="name">
    <null />
</property>
1
2
3
细节：

<property name="name" value="null"></property>
1
以上写法，为name所赋值为字符串null

5.2.3.3xml实体
<!-- 解决方案一：使用XML实体来代替 -->
<property name="expression" value="a &lt; b"/>
1
2
说明：

​ 小于号在XML文档中用来定义标签的开始，不能随便使用

5.2.3.4CDATA节
<property name="expression">
    <!-- 解决方案二：使用CDATA节 -->
    <value><![CDATA[a < b]]></value>
</property>
1
2
3
4
说明：

CDATA中的C代表Character，是文本、字符的含义，CDATA就表示纯文本数据
ML解析器看到CDATA节就知道这里是纯文本，就不会当作XML标签或属性来解析
所以CDATA节中写什么符号都随意
5.2.4注入对象类型属性值
5.2.4.1引用外部Bean
步骤一：配置Clazz类型的bean

<bean id="clazzOne" class="com.atguigu.spring6.bean.Clazz">
    <property name="clazzId" value="1111"></property>
    <property name="clazzName" value="财源滚滚班"></property>
</bean>
1
2
3
4
步骤二：为Student中的clazz属性赋值

<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->
    <property name="clazz" ref="clazzOne"></property>
</bean>
1
2
3
4
5
6
7
8
说明：

​ 当引用外部对象时，需要将ref属性变为Value属性。ref属性，值表示引用对象、value属性，值表示字符串

5.2.4.2引用内部Bean
步骤一：在引用外部Bean的基础上

<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <property name="clazz">
        <!-- 在一个bean中再声明一个bean就是内部bean -->
        <!-- 内部bean只能用于给属性赋值，不能在外部通过IOC容器获取，因此可以省略id属性 -->
        <bean id="clazzInner" class="com.atguigu.spring6.bean.Clazz">
            <property name="clazzId" value="2222"></property>
            <property name="clazzName" value="远大前程班"></property>
        </bean>
    </property>
</bean>
1
2
3
4
5
6
7
8
9
10
11
12
13
14
说明：

​ 将Bean写于属性标签内，即为引用内部Bean

5.2.4.3级联属性赋值
步骤一：在引用内部Bean的基础上

<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <property name="clazz" ref="clazzOne"></property>
    <property name="clazz.clazzId" value="3333"></property>
    <property name="clazz.clazzName" value="最强王者班"></property>
</bean>
1
2
3
4
5
6
7
8
9
5.2.5注入数组类型属性值
步骤一：在Student类中中添加成员变量数组和getter于setter方法

private String[] hobbies;

public String[] getHobbies() {
    return hobbies;
}

public void setHobbies(String[] hobbies) {
    this.hobbies = hobbies;
}
1
2
3
4
5
6
7
8
9
步骤二：配置Bean

<bean id="studentFour" class="com.atguigu.spring.bean6.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->
    <property name="clazz" ref="clazzOne"></property>
    <property name="hobbies">
        <array>
            <value>抽烟</value>
            <value>喝酒</value>
            <value>烫头</value>
        </array>
    </property>
</bean>
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
说明：

​ 当注入数组类型数据时，需要使用标签

5.2.6注入集合类型属性值
5.2.6.1注入List集合类型属性值
步骤一：在Clazz类中添加添加成员变量集合和getter于setter方法

private List<Student> students;

public List<Student> getStudents() {
    return students;
}

public void setStudents(List<Student> students) {
    this.students = students;
}
1
2
3
4
5
6
7
8
9
步骤二：配置Bean

<bean id="clazzTwo" class="com.atguigu.spring6.bean.Clazz">
    <property name="clazzId" value="4444"></property>
    <property name="clazzName" value="Javaee0222"></property>
    <property name="students">
        <list>
            <ref bean="studentOne"></ref>
            <ref bean="studentTwo"></ref>
            <ref bean="studentThree"></ref>
        </list>
    </property>
</bean>
1
2
3
4
5
6
7
8
9
10
11
说明：

​ 当注入List集合类型数据时，需要使用标签

细节：

​ 因为List students，List集合中引用的是Student对象，因此注入时需要使用标签，进行引用对象

5.2.6.2注入Map集合类型属性值
步骤一：创建Student类

package com.atguigu.spring6.bean;
public class Teacher {

    private Integer teacherId;

    private String teacherName;

    public Integer getTeacherId() {
        return teacherId;
    }

    public void setTeacherId(Integer teacherId) {
        this.teacherId = teacherId;
    }

    public String getTeacherName() {
        return teacherName;
    }

    public void setTeacherName(String teacherName) {
        this.teacherName = teacherName;
    }

    public Teacher(Integer teacherId, String teacherName) {
        this.teacherId = teacherId;
        this.teacherName = teacherName;
    }

    public Teacher() {

    }
    
    @Override
    public String toString() {
        return "Teacher{" +
                "teacherId=" + teacherId +
                ", teacherName='" + teacherName + '\'' +
                '}';
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
步骤二：在Student类中添加添加成员变量集合和getter于setter方法

private Map<String, Teacher> teacherMap;

public Map<String, Teacher> getTeacherMap() {
    return teacherMap;
}

public void setTeacherMap(Map<String, Teacher> teacherMap) {
    this.teacherMap = teacherMap;
}
1
2
3
4
5
6
7
8
9
步骤三：配置bean

<bean id="teacherOne" class="com.atguigu.spring6.bean.Teacher">
    <property name="teacherId" value="10010"></property>
    <property name="teacherName" value="大宝"></property>
</bean>

<bean id="teacherTwo" class="com.atguigu.spring6.bean.Teacher">
    <property name="teacherId" value="10086"></property>
    <property name="teacherName" value="二宝"></property>
</bean>

<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->
    <property name="clazz" ref="clazzOne"></property>
    <property name="hobbies">
        <array>
            <value>抽烟</value>
            <value>喝酒</value>
            <value>烫头</value>
        </array>
    </property>
    <property name="teacherMap">
        <map>
            <entry>
                <key>
                    <value>10010</value>
                </key>
                <ref bean="teacherOne"></ref>
            </entry>
            <entry>
                <key>
                    <value>10086</value>
                </key>
                <ref bean="teacherTwo"></ref>
            </entry>
        </map>
    </property>
</bean>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
说明：

当注入Map集合类型数据时，需要使用标签
需要使用表示键值对
需要使用表示键
细节：

​ 因为Map<String, Teacher> teacherMap，Map集合中引用的是Teacher对象，因此注入时需要使用标签，进行引用对象

5.2.6.2注入引用集合类型属性值
步骤一：配置对应的命名空间

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns:util="http://www.springframework.org/schema/util"
    xsi:schemaLocation="http://www.springframework.org/schema/util
    http://www.springframework.org/schema/util/spring-util.xsd
    http://www.springframework.org/schema/beans
    http://www.springframework.org/schema/beans/spring-beans.xsd">
1
2
3
4
5
6
7
8
步骤二：配置Bean

<!--list集合类型的bean-->
<util:list id="students">
    <ref bean="studentOne"></ref>
    <ref bean="studentTwo"></ref>
    <ref bean="studentThree"></ref>
</util:list>
<!--map集合类型的bean-->
<util:map id="teacherMap">
    <entry>
        <key>
            <value>10010</value>
        </key>
        <ref bean="teacherOne"></ref>
    </entry>
    <entry>
        <key>
            <value>10086</value>
        </key>
        <ref bean="teacherTwo"></ref>
    </entry>
</util:map>
<bean id="clazzTwo" class="com.atguigu.spring6.bean.Clazz">
    <property name="clazzId" value="4444"></property>
    <property name="clazzName" value="Javaee0222"></property>
    <property name="students" ref="students"></property>
</bean>
<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->
    <property name="clazz" ref="clazzOne"></property>
    <property name="hobbies">
        <array>
            <value>抽烟</value>
            <value>喝酒</value>
            <value>烫头</value>
        </array>
    </property>
    <property name="teacherMap" ref="teacherMap"></property>
</bean>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
说明：

使用标签，可以将List集合或者Map集合的属性注入变为引用的方式
在使用util标签时，需要引入相应的命名空间
5.2.7引入P命名空间属性值
步骤一：引入P命名空间

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:util="http://www.springframework.org/schema/util"
       xmlns:p="http://www.springframework.org/schema/p"
       xsi:schemaLocation="http://www.springframework.org/schema/util
       http://www.springframework.org/schema/util/spring-util.xsd
       http://www.springframework.org/schema/beans
       http://www.springframework.org/schema/beans/spring-beans.xsd">
1
2
3
4
5
6
7
8
9
步骤二：通过p命名空间方式为bean的各个属性赋值

<bean id="studentSix" class="com.atguigu.spring6.bean.Student"
    p:id="1006" p:name="小明" p:clazz-ref="clazzOne" p:teacherMap-ref="teacherMap"></bean>
1
2
说明：

​ 通过p:成员属性，即可完成各个属性的赋值.

5.2.8引入外部属性文件
步骤一：添加依赖

 <!-- MySQL驱动 -->
<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <version>8.0.30</version>
</dependency>

<!-- 数据源 -->
<dependency>
    <groupId>com.alibaba</groupId>
    <artifactId>druid</artifactId>
    <version>1.2.15</version>
</dependency>
1
2
3
4
5
6
7
8
9
10
11
12
13
步骤二：创建外部属性文件

jdbc.user=root
jdbc.password=atguigu
jdbc.url=jdbc:mysql://localhost:3306/ssm?serverTimezone=UTC
jdbc.driver=com.mysql.cj.jdbc.Driver
1
2
3
4
说明：

​ 在resources文件下创建jdbc.properties文件

步骤三：引入属性文件

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:context="http://www.springframework.org/schema/context"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
                           http://www.springframework.org/schema/beans/spring-beans.xsd
                           http://www.springframework.org/schema/context
                           http://www.springframework.org/schema/context/spring-context.xsd">
    <!-- 引入外部属性文件 -->
    <context:property-placeholder location="classpath:jdbc.properties"/>
</beans>
1
2
3
4
5
6
7
8
9
10
11
注意：

​ 在使用 <context:property-placeholder> 元素加载外包配置文件功能前，首先需要在 XML 配置的一级标签 中添加 context 相关的约束。

步骤四：配置Bean

<!--完成数据库信息注入-->
<bean id="druidDataSource" class="com.alibaba.druid.pool.DruidDataSource">
    <property name="url" value="${jdbc.url}"/>
    <property name="driverClassName" value="${jdbc.driver}"/>
    <property name="username" value="${jdbc.user}"/>
    <property name="password" value="${jdbc.password}"/>
</bean>
1
2
3
4
5
6
7
说明：

​ 取外部文件中的值时，需要根据外部文件中属性的名字，可以把相应值取得

步骤五：演示

@Test
public void testDataSource() throws SQLException {
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-datasource.xml");
    DataSource dataSource = ac.getBean(DruidDataSource.class);
    Connection connection = dataSource.getConnection();
    System.out.println(connection);
}
1
2
3
4
5
6
7
5.2.9引入Bean的作用域
步骤一：创建类User

package com.atguigu.spring6.bean;
public class User {

    private Integer id;

    private String username;

    private String password;

    private Integer age;

    public User() {
    }

    public User(Integer id, String username, String password, Integer age) {
        this.id = id;
        this.username = username;
        this.password = password;
        this.age = age;
    }

    public Integer getId() {
        return id;
    }

    public void setId(Integer id) {
        this.id = id;
    }

    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public String getPassword() {
        return password;
    }

    public void setPassword(String password) {
        this.password = password;
    }

    public Integer getAge() {
        return age;
    }

    public void setAge(Integer age) {
        this.age = age;
    }

    @Override
    public String toString() {
        return "User{" +
                "id=" + id +
                ", username='" + username + '\'' +
                ", password='" + password + '\'' +
                ", age=" + age +
                '}';
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
步骤二：配置bean

<!-- scope属性：取值singleton（默认值），bean在IOC容器中只有一个实例，IOC容器初始化时创建对象 -->
<!-- scope属性：取值prototype，bean在IOC容器中可以有多个实例，getBean()时创建对象 -->
<bean class="com.atguigu.spring6.bean.User" scope="prototype"></bean>
1
2
3
说明：

属性值：
singleton（默认），在IOC容器中，这个bean的对象始终为单实例，当IOC容器初始化时即可创建对象
prototype，在IOC容器中，这个bean在IOC容器中有多个实例，当 获取bean时可创建对象
步骤三：演示

@Test
public void testBeanScope(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-scope.xml");
    User user1 = ac.getBean(User.class);
    User user2 = ac.getBean(User.class);
    System.out.println(user1==user2);
}
1
2
3
4
5
6
7
5.2.10Bean的生命周期
流程

bean对象创建（调用无参构造器）

bean对象设置属性

bean的后置处理器（初始化之前）

bean对象初始化（需在配置bean时指定初始化方法）

bean的后置处理器（初始化之后）

bean对象就绪可以使用

bean对象销毁（需在配置bean时指定销毁方法）

IOC容器关闭

步骤一：修改User类

public class User {

    private Integer id;

    private String username;

    private String password;

    private Integer age;

    public User() {
        System.out.println("生命周期：1、创建对象");
    }

    public User(Integer id, String username, String password, Integer age) {
        this.id = id;
        this.username = username;
        this.password = password;
        this.age = age;
    }

    public Integer getId() {
        return id;
    }

    public void setId(Integer id) {
        System.out.println("生命周期：2、依赖注入");
        this.id = id;
    }

    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public String getPassword() {
        return password;
    }

    public void setPassword(String password) {
        this.password = password;
    }

    public Integer getAge() {
        return age;
    }

    public void setAge(Integer age) {
        this.age = age;
    }

    public void initMethod(){
        System.out.println("生命周期：3、初始化");
    }

    public void destroyMethod(){
        System.out.println("生命周期：5、销毁");
    }

    @Override
    public String toString() {
        return "User{" +
                "id=" + id +
                ", username='" + username + '\'' +
                ", password='" + password + '\'' +
                ", age=" + age +
                '}';
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
64
65
66
67
68
69
70
71
72
说明：

​ 其中的initMethod()和destroyMethod()，可以通过配置Bean指定为初始化和销毁的方法

步骤二：创建Bean 的后置处理器

package com.atguigu.spring6.process;
    
import org.springframework.beans.BeansException;
import org.springframework.beans.factory.config.BeanPostProcessor;

public class MyBeanProcessor implements BeanPostProcessor {
    
    @Override
    public Object postProcessBeforeInitialization(Object bean, String beanName) throws BeansException {
        System.out.println("☆☆☆" + beanName + " = " + bean);
        return bean;
    }
    
    @Override
    public Object postProcessAfterInitialization(Object bean, String beanName) throws BeansException {
        System.out.println("★★★" + beanName + " = " + bean);
        return bean;
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
注意：

​ bean的后置处理器会在生命周期的初始化前后添加额外的操作，需要实现BeanPostProcessor接口，且配置到IOC容器中，需要注意的是，bean后置处理器不是单独针对某一个bean生效，而是针对IOC容器中所有bean都会执行

步骤三：配置Bean

<!-- 使用init-method属性指定初始化方法 -->
<!-- 使用destroy-method属性指定销毁方法 -->
<bean class="com.atguigu.spring6.bean.User" scope="prototype" init-method="initMethod" destroy-method="destroyMethod">
    <property name="id" value="1001"></property>
    <property name="username" value="admin"></property>
    <property name="password" value="123456"></property>
    <property name="age" value="23"></property>
</bean>
<!-- bean的后置处理器要放入IOC容器才能生效 -->
<bean id="myBeanProcessor" class="com.atguigu.spring6.process.MyBeanProcessor"/>
1
2
3
4
5
6
7
8
9
10
说明：

在配置Bean时，需要使用init-method属性和destroy-method属性进行配置Bean的初始化方法与销毁的方法
在配置Bean时，需要将Bean的后置处理器放入IOC容器才能生效
步骤四：演示

@Test
public void testLife(){
    ClassPathXmlApplicationContext ac = new ClassPathXmlApplicationContext("spring-lifecycle.xml");
    User bean = ac.getBean(User.class);
    System.out.println("生命周期：4、通过IOC容器获取bean并使用");
    ac.close();
}
1
2
3
4
5
6
7
5.2.11引入FactoryBean属性值


说明：

​ FactoryBean是Spring提供的一种整合第三方框架的常用机制。和普通的bean不同，配置一个FactoryBean类型的bean，在获取bean的时候得到的并不是class属性中配置的这个类的对象，而是getObject()方法的返回值。通过这种机制，Spring可以帮我们把复杂组件创建的详细过程和繁琐细节都屏蔽起来，只把最简洁的使用界面展示给我们。

步骤一 ：创建类UserFactoryBean

package com.atguigu.spring6.bean;
public class UserFactoryBean implements FactoryBean<User> {
    @Override
    public User getObject() throws Exception {
        return new User();
    }

    @Override
    public Class<?> getObjectType() {
        return User.class;
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
步骤二：配置bean

<bean id="user" class="com.atguigu.spring6.bean.UserFactoryBean"></bean>
1
步骤三：演示

@Test
public void testUserFactoryBean(){
    //获取IOC容器
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-factorybean.xml");
    User user = (User) ac.getBean("user");
    System.out.println(user);
}
1
2
3
4
5
6
7
说明：

​ 此时获取到的容器对象，并不是UserFactoryBean，而是User

5.2.12引入xml自动装配
步骤一：环境准备

1.创建UserController类

package com.atguigu.spring6.autowire.controller
public class UserController {

    private UserService userService;

    public void setUserService(UserService userService) {
        this.userService = userService;
    }

    public void saveUser(){
        userService.saveUser();
    }

}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
2.创建UserService接口

package com.atguigu.spring6.autowire.service
public interface UserService {

    void saveUser();

}
1
2
3
4
5
6
3.创建UserServiceImpl类实现UserService接口

package com.atguigu.spring6.autowire.service.impl
public class UserServiceImpl implements UserService {

    private UserDao userDao;

    public void setUserDao(UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void saveUser() {
        userDao.saveUser();
    }

}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
4.创建UserDao接口

package com.atguigu.spring6.autowire.dao
public interface UserDao {

    void saveUser();

}
1
2
3
4
5
6
5.创建UserDaoImpl类实现UserDao接口

package com.atguigu.spring6.autowire.dao.impl
public class UserDaoImpl implements UserDao {

    @Override
    public void saveUser() {
        System.out.println("保存成功");
    }

}
1
2
3
4
5
6
7
8
9
步骤二：配置bean

<bean id="userController" class="com.atguigu.spring6.autowire.controller.UserController" autowire="byType"></bean>

<bean id="userService" class="com.atguigu.spring6.autowire.service.impl.UserServiceImpl" autowire="byType"></bean>

<bean id="userDao" class="com.atguigu.spring6.autowire.dao.impl.UserDaoImpl"></bean>
1
2
3
4
5
说明：

当使用Bean标签的autowire属性是，通过byType的方式进行自动装配
byType：根据类型匹配IOC容器中的某个兼容类型的bean，为属性自动赋值
若在IOC中，没有任何一个兼容类型的bean能够为属性赋值，则该属性不装配，即值为默认值null
若在IOC中，有多个兼容类型的bean能够为属性赋值，则抛出异常NoUniqueBeanDefinitionException
byName：将自动装配的属性的属性名，作为bean的id在IOC容器中匹配相对应的bean进行赋值
步骤三：演示

@Test
public void testAutoWireByXML(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("autowire-xml.xml");
    UserController userController = ac.getBean(UserController.class);
    userController.saveUser();
}
1
2
3
4
5
6
说明：

​ 当使用标签中的属性时，使用Autowire属性使用byType的方式即可实现属性的自动注入

5.3基于注解管理Bean（重点）
笔记小结：

概述：

简介：Java 增加了对注解（Annotation）的支持，它是代码中的一种特殊标记，可以在编译、类加载和运行时被读取，执行相应的处理。
使用注解：
@Component：表示泛化组件
@Repository：表示数据访问层组件
@Service：表示业务层组件
@Controller：：表示控制层组件
开启组件扫描

概述：通过 <context:component-scan> 元素开启 Spring Beans的自动扫描功能。Spring 会自动从扫描指定的包（base-package 属性设置）及其子包下的所有类，如果类上使用了 @Component 注解，就将该类装配到容器中
基本用例：使用标签<context:component-scan></context:component-scan>
添加conentt约束
开启扫描方式
指定要排除的组件： <context:exclude-filter></context:exclude-filter>
仅扫描指定组件： <context:include-filter></context:include-filter
使用注解定义Bean

使用@Autowired注入：

属性注入

@Autowired
private UserDao userDao;
1
2
setter注入

private UserDao userDao;
@Autowired
public void setUserDao(UserDao userDao) {
    this.userDao = userDao;
}
1
2
3
4
5
构造方法注入

private UserDao userDao;
@Autowired
public UserServiceImpl(UserDao userDao) {
	this.userDao = userDao;
}
1
2
3
4
5
形参注入

private UserDao userDao;
public UserServiceImpl(@Autowired UserDao userDao) {
    this.userDao = userDao;
}
1
2
3
4
无注解注入：当构造函数仅有一个需要注入的构造参数时，@Autowired可以省略

private UserDao userDao;
public UserServiceImpl(UserDao userDao) {
    this.userDao = userDao;
}
1
2
3
4
联合**@Qualifier注解注入：适用于一个接口多个实现类的注解区别**

@Autowired
@Qualifier("userDaoImpl") // 指定bean的名字
private UserDao userDao;
1
2
3
使用@Resource注入：

Name注入：在使用注解时，配置name属性

@Resource(name = "myUserDao")
1
未知Name注入：不配置name属性，注入属性的成员变量但需要与Bean 的名称同名

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {
    ……
@Resource
private UserDao myUserDao;
1
2
3
4
5
类型注入：不配置name属性，名称都不同时，注入属性的成员类型会根据Bean实现的接口类型进行匹配

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {
    ……
@Resource
private UserDao userDao1;
1
2
3
4
5
全注解开发：不再使用spring配置文件了，写一个配置类来代替配置文件

@Configuration
//@ComponentScan({"com.atguigu.spring6.controller", "com.atguigu.spring6.service","com.atguigu.spring6.dao"})
@ComponentScan("com.atguigu.spring6") //开启包扫描
public class Spring6Config {
}
1
2
3
4
5
说明：用全注解开发方式时，需要指定包扫描所属的范围，便于Spring框架确定扫描而注入Bean的范围

5.3.1概述
5.3.1.1简介
​ 从 Java 5 开始，Java 增加了对注解（Annotation）的支持，它是代码中的一种特殊标记，可以在编译、类加载和运行时被读取，执行相应的处理。开发人员可以通过注解在不改变原有代码和逻辑的情况下，在源代码中嵌入补充信息。

​ Spring 从 2.5 版本开始提供了对注解技术的全面支持，我们可以使用注解来实现自动装配，简化 Spring 的 XML 配置。

5.3.1.2步骤
引入依赖
开启组件扫描
使用注解定义 Bean
依赖注入
5.3.1.3使用注解
​ Spring 提供了以下多个注解，这些注解可以直接标注在 Java 类上，将它们定义成 Spring Bean

注解	说明
@Component	该注解用于描述 Spring 中的 Bean，它是一个泛化的概念，仅仅表示容器中的一个组件（Bean），并且可以作用在应用的任何层次，例如 Service 层、Dao 层等。 使用时只需将该注解标注在相应类上即可。
@Repository	该注解用于将数据访问层（Dao 层）的类标识为 Spring 中的 Bean，其功能与 @Component 相同。
@Service	该注解通常作用在业务层（Service 层），用于将业务层的类标识为 Spring 中的 Bean，其功能与 @Component 相同。
@Controller	该注解通常作用在控制层（如SpringMVC 的 Controller），用于将控制层的类标识为 Spring 中的 Bean，其功能与 @Component 相同。
5.3.2开启组件扫描
5.3.2.1概述
​ Spring 默认不使用注解装配 Bean，因此我们需要在 Spring 的 XML 配置中，通过 <context:component-scan> 元素开启 Spring Beans的自动扫描功能。开启此功能后，Spring 会自动从扫描指定的包（base-package 属性设置）及其子包下的所有类，如果类上使用了 @Component 注解，就将该类装配到容器中。

5.3.2.2基本用例-实现组件扫描
步骤一：添加约束

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:context="http://www.springframework.org/schema/context"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
    http://www.springframework.org/schema/beans/spring-beans-3.0.xsd
    http://www.springframework.org/schema/context
            http://www.springframework.org/schema/context/spring-context.xsd">
</beans>
1
2
3
4
5
6
7
8
9
说明：

​ 在 XML 配置的一级标签 中添加 context 相关的约束

步骤二：开启扫描方式

<context:component-scan base-package="com.atguigu.spring6">
</context:component-scan>
1
2
说明：

​ 在Beans.xml文件中，设置开启扫描方式即可

5.3.2.3指定要排除的组件
<context:component-scan base-package="com.atguigu.spring6">
    <!-- context:exclude-filter标签：指定排除规则 -->
    <!-- 
 		type：设置排除或包含的依据
		type="annotation"，根据注解排除，expression中设置要排除的注解的全类名
		type="assignable"，根据类型排除，expression中设置要排除的类型的全类名
	-->
    <context:exclude-filter type="annotation" expression="org.springframework.stereotype.Controller"/>
        <!--<context:exclude-filter type="assignable" expression="com.atguigu.spring6.controller.UserController"/>-->
</context:component-scan>
1
2
3
4
5
6
7
8
9
10
说明：

<context:exclude-filter></context:exclude-filter>标签，指定排除规则
type属性：设置排除或包含的依据
属性值：annotation，根据注解排除
属性值：assignable，根据类型排除
expression属性：设置要排除的注解或类型的全类名
5.3.2.4仅扫描指定组件
<context:component-scan base-package="com.atguigu" use-default-filters="false">
    <!-- context:include-filter标签：指定在原有扫描规则的基础上追加的规则 -->
    <!-- use-default-filters属性：取值false表示关闭默认扫描规则 -->
    <!-- 此时必须设置use-default-filters="false"，因为默认规则即扫描指定包下所有类 -->
    <context:include-filter type="annotation" expression="org.springframework.stereotype.Controller"/>
    <!--<context:include-filter type="assignable" expression="com.atguigu.spring6.controller.UserController"/>-->
</context:component-scan>
1
2
3
4
5
6
7
说明：

use-default-filters="false"，表示关闭默认扫描规则
<context:include-filter></context:include-filter>，表示指定的过滤条件来确定哪些类应该被包含在组件扫描中
5.3.2使用注解定义Bean
5.3.3使用@Autowired注入
5.3.3.1概述


说明：

@Autowired注解可以标注在：构造方法上、方法上、形参上、属性上、注解上
@Autowired注解的required属性，
属性值为True：表示注入的时候要求被注入的Bean必须是存在的，如果不存在则报错
属性值为False：：表示注入的时候要求被注入的Bean不一定是存在的，如果存在的话就注入，不存在的话，也不报错
细节：

单独使用@Autowired注解时，默认是根据类型装配，默认是"byType"，例如基于XML管理Bean
<bean id="userService" class="com.atguigu.spring6.autowire.service.impl.UserServiceImpl" autowire="byType"></bean>
1
5.3.3.2属性注入
步骤一：搭建环境

1.创建UserDao接口

package com.atguigu.spring6.dao;

public interface UserDao {

    public void print();
}
1
2
3
4
5
6
2.创建UserDaoImpl实现

package com.atguigu.spring6.dao.impl;

import com.atguigu.spring6.dao.UserDao;
import org.springframework.stereotype.Repository;

@Repository
public class UserDaoImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
3.创建UserService接口

package com.atguigu.spring6.service;

public interface UserService {

    public void out();
}
1
2
3
4
5
6
4.创建UserServiceImpl实现类

package com.atguigu.spring6.service.impl;

import com.atguigu.spring6.dao.UserDao;
import com.atguigu.spring6.service.UserService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;

@Service
public class UserServiceImpl implements UserService {

    @Autowired
    private UserDao userDao;

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
5.创建UserController类

package com.atguigu.spring6.controller;

import com.atguigu.spring6.service.UserService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Controller;

@Controller
public class UserController {

    @Autowired
    private UserService userService;

    public void out() {
        userService.out();
        System.out.println("Controller层执行结束。");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

当使用@Autowired注解注入时，可不提供构造方法喝Setter方法，也可以注入成功
结果：
5.3.3.3set注入
步骤一：搭建环境

1.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    private UserDao userDao;

    @Autowired
    public void setUserDao(UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
2.修改UserController类

@Controller
public class UserController {

    private UserService userService;

    @Autowired
    public void setUserService(UserService userService) {
        this.userService = userService;
    }

    public void out() {
        userService.out();
        System.out.println("Controller层执行结束。");
    }

}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

​ 通过在需要注入的setter方法上进行添加@Autowired注解

5.3.3.4构造方法注入
步骤一：搭建环境

1.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    private UserDao userDao;

    @Autowired
    public UserServiceImpl(UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
2.修改UserController类

@Controller
public class UserController {

    private UserService userService;

    @Autowired
    public UserController(UserService userService) {
        this.userService = userService;
    }

    public void out() {
        userService.out();
        System.out.println("Controller层执行结束。");
    }

}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

​ 通过在需要注入的构造器方法上进行添加@Autowired注解

5.3.3.5形参注入
步骤一：搭建环境

1.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    private UserDao userDao;

    public UserServiceImpl(@Autowired UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
2.修改UserController类

@Controller
public class UserController {

    private UserService userService;

    public UserController(@Autowired UserService userService) {
        this.userService = userService;
    }

    public void out() {
        userService.out();
        System.out.println("Controller层执行结束。");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

​ 通过在需要注入的形参上进行添加@Autowired注解

5.3.3.6无注解注入
步骤一：搭建环境

1.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

 
    private UserDao userDao;

    public UserServiceImpl(UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

​ 当有参数的构造方法只有一个时，@Autowired注解可以省略

5.3.3.7联合@Qualifier注解注入
步骤一：搭建环境

1.添加UserDaoRedisImpl类

@Repository
public class UserDaoRedisImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Redis Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
说明：

此时，添加实现UserDao接口类，已经造成一个接口对应两个实现类
此时，程序错误，信息中说：不能装配，UserDao这个Bean的数量等于2
步骤二：修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    @Autowired
    @Qualifier("userDaoImpl") // 指定bean的名字
    private UserDao userDao;

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
说明：

​ 当需要注入的接口有多个实现类时，可以联合使用@Qualifier(“userDaoImpl”) 注解，并指定实现类的名字，即可完成属性注入

5.3.4使用@Resource注入
5.3.4.1概述
​ @Resource注解是通过名称匹配的方式来实现注入的，默认按照名称进行匹配，如果找不到匹配的名称，则会尝试按照类型匹配。

​ @Resource注解是JDK扩展包中的，也就是说属于JDK的一部分。所以该注解是标准注解，更加具有通用性。(JSR-250标准中制定的注解类型。JSR是Java规范提案。)



说明：

如果是JDK8的话不需要额外引入依赖。高于JDK11或低于JDK8需要引入以下依赖
<dependency>
    <groupId>jakarta.annotation</groupId>
    <artifactId>jakarta.annotation-api</artifactId>
    <version>2.1.1</version>
</dependency>
1
2
3
4
5
5.3.4.2Name注入
步骤一：搭建环境

1.修改UserDaoImpl类

package com.atguigu.spring6.dao.impl;

import com.atguigu.spring6.dao.UserDao;
import org.springframework.stereotype.Repository;

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
说明：

​ 当使用注解时，在小括号内写上属性名称表示为此Bean定义别名

2.修改UserServiceImpl类

package com.atguigu.spring6.service.impl;

import com.atguigu.spring6.dao.UserDao;
import com.atguigu.spring6.service.UserService;
import jakarta.annotation.Resource;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.beans.factory.annotation.Qualifier;
import org.springframework.stereotype.Service;

@Service
public class UserServiceImpl implements UserService {

    @Resource(name = "myUserDao")
    private UserDao myUserDao;

    @Override
    public void out() {
        myUserDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
说明：

​ 当使用@Resource注解时，可以使用name属性指定属性注入的别名

步骤二：演示

5.3.4.3未知Name注入
步骤一：搭建环境

1.修改UserDaoImpl类

package com.atguigu.spring6.dao.impl;

import com.atguigu.spring6.dao.UserDao;
import org.springframework.stereotype.Repository;

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
2.修改UserServiceImpl类

package com.atguigu.spring6.service.impl;

import com.atguigu.spring6.dao.UserDao;
import com.atguigu.spring6.service.UserService;
import jakarta.annotation.Resource;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.beans.factory.annotation.Qualifier;
import org.springframework.stereotype.Service;

@Service
public class UserServiceImpl implements UserService {

    @Resource
    private UserDao myUserDao;

    @Override
    public void out() {
        myUserDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
说明：

​ 当使用@Resource注解时，在name属性未知的情况下，将属性注入的成员属性变量名定义为与Bean同名，即可完成注入

步骤二：演示

5.3.4.4类型注入
步骤一：搭建环境

1.原UserDaoImpl类

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
2.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    @Resource
    private UserDao userDao1;

    @Override
    public void out() {
        userDao1.print();
        System.out.println("Service层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
说明：

​ 当使用@Resource注解时，现在userDao1属性名不存在，但仍然可以注入成功。因为，UserDao他们的类型名相同

5.3.5全注解开发
5.3.5.1概述
​ 全注解开发就是不再使用spring配置文件了，写一个配置类来代替配置文件

5.3.5.2基本用例-全注解开发实现
步骤一：创建配置类

@Configuration
//@ComponentScan({"com.atguigu.spring6.controller", "com.atguigu.spring6.service","com.atguigu.spring6.dao"})
@ComponentScan("com.atguigu.spring6")
public class Spring6Config {
}
1
2
3
4
5
说明：

​ 使用@ComponentScan注解，进行组件扫描，从而替代了原有在xml文件中的配置

步骤二：演示

@Test
public void testAllAnnotation(){
    ApplicationContext context = new AnnotationConfigApplicationContext(Spring6Config.class);
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
    logger.info("执行成功");
}
1
2
3
4
5
6
7
说明：

​ 需要使用AnnotationConfigApplicationContext类来获取Spring6Config的字节码文件

5.4原理
笔记小结：

扫描指定的包，获取所有需要管理的类的类名。
实例化需要管理的类，通过反射机制调用构造器来实现。
通过反射机制调用setter方法或者构造器注入属性值。
维护对象之间的依赖关系，实现对象之间的解耦。
将实例化好的对象注册到IOC容器中，便于后续使用。
说明：



步骤一：环境搭建

1.创建注解

创建Bean注解

// 此注解用于定义容器对象，类似于@Componet、@Service、@Controller注解等作用
@Target(ElementType.TYPE)
@Retention(RetentionPolicy.RUNTIME)
public @interface Bean {
}
1
2
3
4
5
创建依赖注入注解

// 此注解用于完成成员属性的依赖注入，类似于@Autoware、@Resource注解等作用
@Target({ElementType.FIELD})
@Retention(RetentionPolicy.RUNTIME)
public @interface Di {
}
1
2
3
4
5
2.创建IOC核心逻辑

定义bean容器接口

package com.atguigu.spring.core;

public interface ApplicationContext {

    Object getBean(Class clazz);
}
1
2
3
4
5
6
编写注解bean容器接口实现

public class AnnotationApplicationContext implements ApplicationContext {

    // 存储Bean的容器
    private HashMap<Class, Object> beanFactory = new HashMap<>();

    // 根据字节码文件获取Bean容器中的对象
    @Override
    public Object getBean(Class clazz) {
        return beanFactory.get(clazz);
    }

    /**
     * 根据包扫描加载bean
     * @param basePackage
     */
    public AnnotationApplicationContext(String basePackage) {
        try {
            String packageDirName = basePackage.replaceAll("\\.", "\\\\");
            Enumeration<URL> dirs =Thread.currentThread().getContextClassLoader().getResources(packageDirName);
            while (dirs.hasMoreElements()) {
                URL url = dirs.nextElement();
                String filePath = URLDecoder.decode(url.getFile(),"utf-8");
                rootPath = filePath.substring(0, filePath.length()-packageDirName.length());
                // 扫描包下的Bean
                loadBean(new File(filePath));
            }

        } catch (Exception e) {
            throw new RuntimeException(e);
        }
        //依赖注入
        loadDi();
    }


    private  void loadBean(File fileParent) {
        if (fileParent.isDirectory()) {
            File[] childrenFiles = fileParent.listFiles();
            if(childrenFiles == null || childrenFiles.length == 0){
                return;
            }
            for (File child : childrenFiles) {
                if (child.isDirectory()) {
                    //如果是个文件夹就继续调用该方法,使用了递归
                    loadBean(child);
                } else {
                    //通过文件路径转变成全类名,第一步把绝对路径部分去掉
                    String pathWithClass = child.getAbsolutePath().substring(rootPath.length() - 1);
                    //选中class文件
                    if (pathWithClass.contains(".class")) {
                        //    com.xinzhi.dao.UserDao
                        //去掉.class后缀，并且把 \ 替换成 .
                        String fullName = pathWithClass.replaceAll("\\\\", ".").replace(".class", "");
                        try {
                            Class<?> aClass = Class.forName(fullName);
                            //把非接口的类实例化放在map中
                            if(!aClass.isInterface()){
                                Bean annotation = aClass.getAnnotation(Bean.class);
                                if(annotation != null){
                                    Object instance = aClass.newInstance();
                                    //判断一下有没有接口
                                    if(aClass.getInterfaces().length > 0) {
                                        //如果有接口把接口的class当成key，实例对象当成value
                                        System.out.println("正在加载【"+ aClass.getInterfaces()[0] +"】,实例对象是：" + instance.getClass().getName());
                                        beanFactory.put(aClass.getInterfaces()[0], instance);
                                    }else{
                                        //如果有接口把自己的class当成key，实例对象当成value
                                        System.out.println("正在加载【"+ aClass.getName() +"】,实例对象是：" + instance.getClass().getName());
                                        beanFactory.put(aClass, instance);
                                    }
                                }
                            }
                        } catch (ClassNotFoundException | IllegalAccessException | InstantiationException e) {
                            e.printStackTrace();
                        }
                    }
                }
            }
        }
    }

    private void loadDi() {
        for(Map.Entry<Class,Object> entry : beanFactory.entrySet()){
            //就是咱们放在容器的对象
            Object obj = entry.getValue();
            Class<?> aClass = obj.getClass();
            Field[] declaredFields = aClass.getDeclaredFields();
            for (Field field : declaredFields){
                Di annotation = field.getAnnotation(Di.class);
                if( annotation != null ){
                    field.setAccessible(true);
                    try {
                        System.out.println("正在给【"+obj.getClass().getName()+"】属性【" + field.getName() + "】注入值【"+ beanFactory.get(field.getType()).getClass().getName() +"】");
                        field.set(obj,beanFactory.get(field.getType()));
                    } catch (IllegalAccessException e) {
                        e.printStackTrace();
                    }
                }
            }
        }
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
64
65
66
67
68
69
70
71
72
73
74
75
76
77
78
79
80
81
82
83
84
85
86
87
88
89
90
91
92
93
94
95
96
97
98
99
100
101
102
说明：

可将此代码复制到IDEA中查看逻辑更详细

3.创建Dao层

创建UserDao接口
public interface UserDao {

    public void print();
}
1
2
3
4
创建UserDaoImpl实现
@Bean
public class UserDaoImpl implements UserDao {
    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}

1
2
3
4
5
6
7
8
说明：

当此类实现了UserDao这个接口时，会将UserDao这个接口作为容器的Key值，来获取UserDaoImpl这个实现类

这也就是为什么一个接口不能对应多个实现类，因为HashMap的Key值不能重复

// 参数解释，参数1：实现类上实现的第一个接口或者实现类的字节码文件；参数2：实现类实例
beanFactory.put(aClass.getInterfaces()[0], instance);
// 此处，参数1：接口为UserDao；参数2，实现类实例为UserDaoImpl
1
2
3
4.创建Service层

创建UserService接口

public interface UserService {
    public void out();
}
1
2
3
创建UserServiceImpl实现类

@Bean
public class UserServiceImpl implements UserService {

    @DI
    private UserDao userDao;

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
说明：

当此类里包含了依赖注入这个接口时，会将UserServiceImpl这个实现类实例作为依赖注入的Key值，并且根据依赖注入的变量名确定所需要依赖注入的实现类实例

// 参数解释，参数1：设置字段值的对象实例；参数2：需要设置的字段值
field.set(obj, beanFactory.get(field.getType()));
//此处，参数1：实现类实例UserServiceImpl；参数2：实现类实例UserDaoImpl
1
2
3
步骤二：演示

ApplicationContext applicationContext = new AnnotationApplicationContext("org.example");
UserService bean = (UserService) applicationContext.getBean(UserService.class);
bean.out();
1
2
3
6.面向切面：AOP (重点)
笔记小结：

概述：

含义：AOP（Aspect Oriented Programming）是一种设计思想，是软件设计领域中的面向切面编程
作用：
简化开发：分离关注点，让各个一些通用的行为（日志、事务、安全）实现重用
降低代码耦合度：将不同的关注点分离开来，提高代码可复用性和可维护性
横切关注点：横切关注点是指跨越应用程序多个模块的功能或行为。例如日志记录、安全性等与业务逻辑无关的功能
通知：通知（增强）是指在 AOP 中定义的一种特殊类型的方法，它包含要在连接点（join point）执行的一些行为。例如在某个方法执行前、中、后需要加上一些输出日志等这样的逻辑
切面：切面指的是横切关注点和通知的组合，简单的说，切面就是封装通知方法的类
目标：目标（Target）是指被通知的对象或者被切面所影响的对象。例如类、接口、方法这类元素
代理：代理是指控制对目标对象的访问，并在访问过程中插入额外的逻辑。简单的说，代理就是向目标对象应用通知之后创建的代理对象
连接点：连接点（Join Point）表示在程序执行过程中能够插入一个切面的点。简单的说，连接点就是代理对象中的执行逻辑
切入点：切入点（Pointcut）表示在目标对象中定义的一个或多个特定的方法或方法执行位置，它表示在何处应该插入切面的逻辑
代理模式：代理模式是一种结构型设计模式，它使得代理对象可以代表另一个对象进行访问

静态代理：静态代理是用代码的方式实现方法之前或之后执行一些附加操作
动态代理：它允许在运行时动态地创建代理对象，并将切面逻辑织入到目标对象的方法中
分类：基于接口的代理（有接口情况）、基于类的代理（无接口情况）
切入点表达式：用于匹配目标对象中的方法，并提供切入点的精确定义



基于注解的AOP：各个小结模块，请查看此小结（重点）

基于XML的AOP：通过XML 的方式来实现切面的定义和应用（了解）

6.1概述
6.1.1定义
​ AOP（Aspect Oriented Programming）是一种设计思想，是软件设计领域中的面向切面编程，它是面向对象编程的一种补充和完善，它以通过预编译方式和运行期动态代理方式实现，在不修改源代码的情况下，给程序动态统一添加额外功能的一种技术。利用AOP可以对业务逻辑的各个部分进行隔离，从而使得业务逻辑各部分之间的耦合度降低，提高程序的可重用性，同时提高了开发的效率

6.1.2作用
代码重用和模块化：AOP可以将一些通用的行为（例如日志记录、安全控制、事务管理等）抽象出来，形成可重用的模块，避免在每个业务逻辑中都重复编写这些代码。

分离关注点：AOP将不同的关注点分离开来，使得各个模块间职责更加清晰明确，代码的可读性和可维护性也更强。

简化开发：AOP可以帮助开发人员将关注点从业务逻辑中分离出来，使得开发更加简单明了。

提高系统的可扩展性：在系统需求变化时，只需要修改AOP模块而不是修改业务逻辑，这可以使得系统更加易于扩展和维护。

降低代码耦合度：AOP的作用是将不同的关注点分离开来，这可以避免代码之间的紧耦合，提高代码的可复用性和可维护性。

6.1.3横切关注点
​ 在 AOP 中，横切关注点指的是在应用程序中影响多个类或对象的横切性质的行为，比如日志记录、性能监控、事务处理等等。这些行为可能分散在整个应用程序中的不同类和方法中，而不是与应用程序的核心业务逻辑紧密相关。

​ 使用 AOP 技术，可以将这些横切关注点从应用程序的核心业务逻辑中分离出来，并将它们模块化为可重用的模块，从而实现更好的代码结构和更好的可维护性。



6.1.4通知（增强）
​ 通知（advice）也被称为增强（advice），是指在 AOP 中定义的一种特殊类型的方法，它包含要在连接点（join point）执行的一些行为。通知可以在目标方法执行之前、之后或异常时被执行，也可以在目标方法返回一个结果后被执行。通知的目的是在不修改目标对象的情况下，将增强（如日志、事务管理等）应用于应用程序的特定方法或切入点。通知是实现 AOP 的核心组件之一，通过将通知应用于特定的连接点（join point）来实现面向切面编程

简单来说：通知就是你想要增强的功能，比如 安全，事务，日志等

通知分类：

前置通知：在被代理的目标方法前执行
返回通知：在被代理的目标方法成功结束后执行（寿终正寝）
异常通知：在被代理的目标方法异常结束后执行（死于非命）
后置通知：在被代理的目标方法最终结束后执行（盖棺定论）
环绕通知：使用try…catch…finally结构围绕整个被代理的目标方法，包括上面四种通知对应的所有位置


6.1.5切面
​ 在AOP中，切面指的是横切关注点和通知的组合，它是一个模块化的横向分割，可以理解为一个横向的切片。切面是对横切关注点和通知的封装，它包含了一组切点和通知，用于描述在何处、何时、以及如何执行横切逻辑。切面可以在不修改原代码的情况下，对原有的代码进行功能的增强或改变。通常，切面是以一个类的形式存在的，它包含了一个或多个通知和一个或多个切点。

简单来说：切面就是封装通知方法的类



6.1.6目标
​ 在AOP（Aspect-Oriented Programming）中，目标（Target）是指被通知的对象或者被切面所影响的对象。它是应用程序中的一个具体元素，可以是类、接口、方法或者字段等。简单点说，目标就是被代理的目标对象

6.1.7代理
​ 在AOP（Aspect-Oriented Programming）中，代理（Proxy）是一种设计模式，用于控制对目标对象的访问，并在访问过程中插入额外的逻辑。简单点说，代理就是向目标对象应用通知之后创建的代理对象

6.1.8连接点
​ 在 AOP 中，连接点（Join Point）表示在程序执行过程中能够插入一个切面的点，例如方法调用、异常处理、字段访问等。连接点定义了在程序中的哪个位置可以应用切面。切面可以在连接点前后增加额外的处理逻辑，从而影响程序的行为。通俗地讲，连接点就是在程序执行中可以被拦截的地方



说明：

​ 把方法排成一排，每一个横切位置看成x轴方向，把方法从上到下执行的顺序看成y轴，x轴和y轴的交叉点就是连接点。通俗说，就是spring允许你使用通知的地方

6.1.9切入点
​ 在 AOP 中，切入点（Join Point）是指程序执行过程中明确的点，通常是方法调用的时候，也可以是异常处理程序的处理过程。切入点定义了哪些方法是需要被拦截或增强的，是 AOP 中最重要的概念之一。切入点通常以方法的形式被定义，比如某个类的所有方法、某个包下的所有方法等等。在 AOP 中，通常会使用表达式语言定义切入点，如使用 Spring AOP 中的 @Pointcut 注解定义。

6.2代理模式
6.2.1概述
​ 代理模式是一种结构型设计模式，它使得代理对象可以代表另一个对象进行访问。它是二十三种设计模式中的一种，属于结构型模式。它的作用就是通过提供一个代理类，让我们在调用目标方法的时候，不再是直接对目标方法进行调用，而是通过代理类间接调用。让不属于目标方法核心逻辑的代码从目标方法中剥离出来——解耦。调用目标方法时先调用代理对象的方法，减少对目标方法的调用和打扰，同时让附加功能能够集中在一起也有利于统一维护。



​

代理：将非核心逻辑剥离出来以后，封装这些非核心逻辑的类、对象、方法

6.2.2静态代理
​ 在静态代理中，代理类是在编译时期创建的，代理类和委托类实现相同的接口或继承相同的类，并在代理类中实现委托类中的方法，在调用委托类的方法之前或之后执行一些附加操作

public class CalculatorStaticProxy implements Calculator {
    
    // 将被代理的目标对象声明为成员变量
    private Calculator target;
    
    public CalculatorStaticProxy(Calculator target) {
        this.target = target;
    }
    
    @Override
    public int add(int i, int j) {
    
        // 附加功能由代理类中的代理方法来实现
        System.out.println("[日志] add 方法开始了，参数是：" + i + "," + j);
    
        // 通过目标对象来实现核心业务逻辑
        int addResult = target.add(i, j);
    
        System.out.println("[日志] add 方法结束了，结果是：" + addResult);
    
        return addResult;
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
说明：

​ 静态代理确实实现了解耦，但是由于代码都写死了，完全不具备任何的灵活性

6.2.3动态代理
6.2.3.1概述
6.2.3.1.1定义
​ 在动态代理中，代理类是在运行时期动态创建的。它不需要事先知道委托类的接口或实现类，而是在运行时期通过 Java 反射机制动态生成代理类



6.2.3.1.2分类
动态代理分类

基于接口的代理（有接口情况）
基于类的代理（无接口情况）


说明：

​ AspectJ：是AOP思想的一种实现。本质上是静态代理，将代理逻辑“织入”被代理的目标类编译得到的字节码文件，所以最终效果是动态的。weaver就是织入器。Spring只是借用了AspectJ中的注解。



说明：

当动态代理是基于接口的代理情况时，此种方式是JDK原生的实现方式。需要被代理的目标类必须**实现接口。因为这个技术要求代理对象和目标对象实现同样的接口**
当动态代理是基于类的代理情况时，通过**继承被代理的目标类**实现代理。因此不需要目标类实现接口
补充：

JDK动态代理动态生成的代理类会在com.sun.proxy包下，类名为$proxy1，和目标类实现相同的接口
cglib动态代理动态生成的代理类会和目标在在相同的包下，会继承目标类
6.2.3.2基本用例-实现动态代理
步骤一：创建ProxyFactory类

public class ProxyFactory {

    private Object target;

    public ProxyFactory(Object target) {
        this.target = target;
    }

    public Object getProxy(){
        /**
         * newProxyInstance()：创建一个代理实例
         * 其中有三个参数：
         * 1、classLoader：加载动态生成的代理类的类加载器
         * 2、interfaces：目标对象实现的所有接口的class对象所组成的数组
         * 3、invocationHandler：设置代理对象实现目标对象方法的过程，即代理类中如何重写接口中的抽象方法
         */
        ClassLoader classLoader = target.getClass().getClassLoader();
        Class<?>[] interfaces = target.getClass().getInterfaces();
        InvocationHandler invocationHandler = new InvocationHandler() {
            @Override
            public Object invoke(Object proxy, Method method, Object[] args) throws Throwable {
                /**
                 * proxy：代理对象
                 * method：代理对象需要实现的方法，即其中需要重写的方法
                 * args：method所对应方法的参数
                 */
                Object result = null;
                try {
                    System.out.println("[动态代理][日志] "+method.getName()+"，参数："+ Arrays.toString(args));
                    result = method.invoke(target, args);
                    System.out.println("[动态代理][日志] "+method.getName()+"，结果："+ result);
                } catch (Exception e) {
                    e.printStackTrace();
                    System.out.println("[动态代理][日志] "+method.getName()+"，异常："+e.getMessage());
                } finally {
                    System.out.println("[动态代理][日志] "+method.getName()+"，方法执行完毕");
                }
                return result;
            }
        };

        return Proxy.newProxyInstance(classLoader, interfaces, invocationHandler);
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
说明：

动态代理需要使用Proxy.newProxyInstance()方法
需要设置代理对象实现目标对象的方法过程
步骤二：演示

@Test
public void testDynamicProxy(){
    ProxyFactory factory = new ProxyFactory(new CalculatorLogImpl());
    Calculator proxy = (Calculator) factory.getProxy();
    proxy.div(1,0);
    //proxy.div(1,1);
}
1
2
3
4
5
6
7
6.3切入点表达式
​ 在 AOP 中，切入点表达式指定了哪些方法需要被织入增强逻辑。它是一个表达式，用于匹配目标对象中的方法，并提供切入点的精确定义



说明：

​ 在切入点表达式语法中，用*号代替“权限修饰符”和“返回值”部分表示“权限修饰符”和“返回值”不限

6.4基于注解的AOP
笔记小结：

概述：在Java类、方法、参数等上添加注解的方式来实现切面的定义和应用

基本用例：

步骤一：导入依赖

步骤二：创建切面类（需要选择通知方式）

步骤三：添加xml配置文件

通知方式：

前置通知：@Before
异常通知：@AfterThrowing
返回通知：@AfterReturning
后置通知：@After
环绕通知：@Around
获取通知信息

获取连接点：在方法中使用JoinPoint即可获取连接点信息

public void beforeMethod(JoinPoint joinPoint)
1
获取目标对象的返回值：在目标对象的返回通知上添加returning属性

@AfterReturning(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", returning = "result")
public void afterReturningMethod(JoinPoint joinPoint, Object result)
1
2
获取目标对象的异常：在目标对象的异常通知上添加throwing属性

@AfterThrowing(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", throwing = "ex")
public void afterThrowingMethod(JoinPoint joinPoint, Throwable ex)
1
2
重用切入点表达式

声明：在空参、空方法体、空返回值的方法上使用**@Pointcut**注解

@Pointcut("execution(* com.atguigu.aop.annotation.*.*(..))")
public void pointCut(){}
1
2
同切面使用：在同一切面中直接引用即可

@Before("pointCut()")
1
不同切面使用：在不同切面中

@Before("com.atguigu.aop.CommonPointCut.pointCut()")
1
6.4.1概述
​ 基于注解的AOP是一种AOP的实现方式，它通过在Java类、方法、参数等上添加注解的方式来实现切面的定义和应用，相比于传统的XML配置方式更加便捷和灵活

6.4.2基本用例-注解实现AOP
步骤一：导入依赖

 <!--spring aop依赖-->
    <dependency>
        <groupId>org.springframework</groupId>
        <artifactId>spring-aop</artifactId>
        <version>6.0.2</version>
    </dependency>
    <!--spring aspects依赖-->
    <dependency>
        <groupId>org.springframework</groupId>
        <artifactId>spring-aspects</artifactId>
        <version>6.0.2</version>
    </dependency>
1
2
3
4
5
6
7
8
9
10
11
12
步骤二：创建接口以及实现类

1.接口

public interface Calculator {
    int add(int i, int j); 
}
1
2
3
2.实现类

@Component
public class CalculatorImpl implements Calculator {

    @Override
    public int add(int i, int j) {
        int result = i + j;
        System.out.println("方法内部 result = " + result);
        return result;
    }
}
1
2
3
4
5
6
7
8
9
10
说明：

​ 此实现类，也需要添加@Component注解，便于Spring容器进行管理

步骤三：创建切面类

@Aspect
@Component
public class LogAspect {
    // 前置通知
    // 异常通知
    // 返回通知
    // 后置通知
    // 环绕通知
    ……
}
1
2
3
4
5
6
7
8
9
10
注意：

​ 此处需要配置切面类的通知方式！

说明：

@Aspect表示这个类是一个切面类
@Component注解保证这个切面类能够放入IOC容器
步骤四：配置Spring配置文件

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:context="http://www.springframework.org/schema/context"
       xmlns:aop="http://www.springframework.org/schema/aop"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
       http://www.springframework.org/schema/beans/spring-beans.xsd
       http://www.springframework.org/schema/context
       http://www.springframework.org/schema/context/spring-context.xsd
       http://www.springframework.org/schema/aop
       http://www.springframework.org/schema/aop/spring-aop.xsd">
    <!--
        基于注解的AOP的实现：
        1、将目标对象和切面交给IOC容器管理（注解+扫描）
        2、开启AspectJ的自动代理，为目标对象自动生成代理
        3、将切面类通过注解@Aspect标识
    -->
    <context:component-scan base-package="com.atguigu.aop.annotation"></context:component-scan>

    <aop:aspectj-autoproxy />
</beans>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
补充：

​ 当学习了SpringBoot后，通过SpringBoot来实现AOP，可省略此文件。因为SpringBoot以实现包扫描和切面标识

步骤五：演示

@Test
public void testAdd(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("beans.xml");
    Calculator calculator = ac.getBean( Calculator.class);
    int add = calculator.add(1, 1);
}
1
2
3
4
5
6
说明：

​

6.4.3通知方式
6.4.3.1前置通知
使用@Before注解标识，在被代理的目标方法前执行

@Before("execution(public int com.atguigu.aop.annotation.CalculatorImpl.*(..))")
public void beforeMethod(JoinPoint joinPoint){
    // getSignature（）获取连接点签名，getName（）获取连接点名称
    String methodName = joinPoint.getSignature().getName();
    String args = Arrays.toString(joinPoint.getArgs());
    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);
}
1
2
3
4
5
6
7
说明：

@Before注解内为切入点表达式
JoinPoint 是指程序执行过程中明确的点，比如方法的调用或异常的处理。JoinPoint 提供了一个可供切面通知获取方法的关键信息的方式
6.4.3.2异常通知
使用@AfterThrowing注解标识，在被代理的目标方法异常结束后执行

@AfterThrowing(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", throwing = "ex")
public void afterThrowingMethod(JoinPoint joinPoint, Throwable ex){
    String methodName = joinPoint.getSignature().getName();
    System.out.println("Logger-->异常通知，方法名："+methodName+"，异常："+ex);
}

1
2
3
4
5
6
说明：

​ @AfterThrowing注解内为切入点表达式

6.4.3.3返回通知
使用@AfterReturning注解标识，在被代理的目标方法成功结束后执行

@AfterReturning(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", returning = "result")
public void afterReturningMethod(JoinPoint joinPoint, Object result){
    String methodName = joinPoint.getSignature().getName();
    System.out.println("Logger-->返回通知，方法名："+methodName+"，结果："+result);
}

1
2
3
4
5
6
说明：

​ @AfterReturning注解内为切入点表达式

6.4.3.4后置通知
使用@After注解标识，在被代理的目标方法最终结束后执行

  @After("execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))")
    public void afterMethod(JoinPoint joinPoint){
        String methodName = joinPoint.getSignature().getName();
        System.out.println("Logger-->后置通知，方法名："+methodName);
    }

1
2
3
4
5
6
说明：

​ @After注解内为切入点表达式

6.4.3.5环绕通知
使用@Around注解标识，使用try…catch…finally结构围绕整个被代理的目标方法，包括上面四种通知对应的所有位置

@Around("execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))")
public Object aroundMethod(ProceedingJoinPoint joinPoint){
    String methodName = joinPoint.getSignature().getName();
    String args = Arrays.toString(joinPoint.getArgs());
    Object result = null;
    try {
        System.out.println("环绕通知-->目标对象方法执行之前");
        //目标对象（连接点）方法的执行
        result = joinPoint.proceed();
        System.out.println("环绕通知-->目标对象方法返回值之后");
    } catch (Throwable throwable) {
        throwable.printStackTrace();
        System.out.println("环绕通知-->目标对象方法出现异常时");
    } finally {
        System.out.println("环绕通知-->目标对象方法执行完毕");
    }
    return result;
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
说明：

@Around注解内为切入点表达式
ProceedingJoinPoint 继承自 JoinPoint 接口，是用于环绕通知的特殊类型的 JoinPoint，它可以用于在通知中控制目标方法的执行。在环绕通知中，ProceedingJoinPoint 提供了一个 proceed() 方法，该方法会执行目标方法，并返回其结果。
6.4.4获取通知信息
6.4.4.1获取连接点信息
在任何通知方式中，获取连接点信息可以在通知方法的参数位置设置JoinPoint类型的形参

@Before("execution(public int com.atguigu.aop.annotation.CalculatorImpl.*(..))")
public void beforeMethod(JoinPoint joinPoint){
    //获取连接点的签名信息
    String methodName = joinPoint.getSignature().getName();
    //获取目标方法到的实参信息
    String args = Arrays.toString(joinPoint.getArgs());
    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);
}
1
2
3
4
5
6
7
8
6.4.4.2获取目标方法的返回值
@AfterReturning中的属性returning，用来将通知方法的某个形参，接收目标方法的返回值

@AfterReturning(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", returning = "result")
public void afterReturningMethod(JoinPoint joinPoint, Object result){
    String methodName = joinPoint.getSignature().getName();
    System.out.println("Logger-->返回通知，方法名："+methodName+"，结果："+result);
}
1
2
3
4
5
6.4.4.3获取目标方法的异常
@AfterThrowing中的属性throwing，用来将通知方法的某个形参，接收目标方法的异常

@AfterThrowing(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", throwing = "ex")
public void afterThrowingMethod(JoinPoint joinPoint, Throwable ex){
    String methodName = joinPoint.getSignature().getName();
    System.out.println("Logger-->异常通知，方法名："+methodName+"，异常："+ex);
}
1
2
3
4
5
6.4.5重用切入点表达式
说明：

​ 切入点表达式可参考本节面向切面：AOP中的概述部分

简化切入点的书写

6.4.5.1声明
@Pointcut("execution(* com.atguigu.aop.annotation.*.*(..))")
public void pointCut(){}
1
2
6.4.5.2同切面使用
@Before("pointCut()")
public void beforeMethod(JoinPoint joinPoint){
    String methodName = joinPoint.getSignature().getName();
    String args = Arrays.toString(joinPoint.getArgs());
    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);
}
1
2
3
4
5
6
6.4.5.3不同切面使用
@Before("com.atguigu.aop.CommonPointCut.pointCut()")
public void beforeMethod(JoinPoint joinPoint){
    String methodName = joinPoint.getSignature().getName();
    String args = Arrays.toString(joinPoint.getArgs());
    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);
}
1
2
3
4
5
6
6.5基于XML的AOP（了解）
<context:component-scan base-package="com.atguigu.aop.xml"></context:component-scan>

<aop:config>
    <!--配置切面类-->
    <aop:aspect ref="loggerAspect">
        <aop:pointcut id="pointCut" 
                   expression="execution(* com.atguigu.aop.xml.CalculatorImpl.*(..))"/>
        <aop:before method="beforeMethod" pointcut-ref="pointCut"></aop:before>
        <aop:after method="afterMethod" pointcut-ref="pointCut"></aop:after>
        <aop:after-returning method="afterReturningMethod" returning="result" pointcut-ref="pointCut"></aop:after-returning>
        <aop:after-throwing method="afterThrowingMethod" throwing="ex" pointcut-ref="pointCut"></aop:after-throwing>
        <aop:around method="aroundMethod" pointcut-ref="pointCut"></aop:around>
    </aop:aspect>
</aop:config>
1
2
3
4
5
6
7
8
9
10
11
12
13
14
知识加油站
1.自动装配和依赖注入的区别与联系
​ 依赖注入（Dependency Injection） 是一种设计模式，旨在通过将依赖关系从一个对象传递给另一个对象，来实现对象之间的解耦。在Spring中，依赖注入通过容器来管理和传递对象之间的依赖关系，而不是由对象自身来创建或管理它们的依赖。这可以通过构造函数注入、Setter方法注入或字段注入等方式来实现

​ 自动装配（Autowired） 是Spring Framework提供的一种依赖注入的方式，用于自动将合适的依赖注入到相应的位置，无需手动指定每个依赖的注入方式。通过使用@Autowired注解，Spring会自动在容器中查找匹配的依赖，并将其注入到需要的位置

总结：

自动装配是Spring框架的特性，用于自动连接应用程序中的组件。
依赖注入是自动装配的一种具体实现方式，使用**@Autowired注解来标识需要自动注入**的属性、构造函数或方法参数。
2.依赖注入的两种方式
依赖注入（Dependency Injection）有两种常见的方式：

构造函数注入（Constructor Injection）：通过构造函数来注入依赖对象。在目标类的构造函数中声明参数，并在创建目标对象时通过构造函数传入依赖对象。这种方式可以保证依赖对象在目标对象创建时就被传入，从而确保了目标对象的完整性和一致性。
Setter方法注入（Setter Injection）：通过Setter方法来注入依赖对象。在目标类中定义对应的Setter方法，并在方法中接收依赖对象作为参数，通过调用Setter方法来注入依赖对象。这种方式可以在目标对象创建后动态地设置依赖对象，灵活性较高。
————————————————

                            版权声明：本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。
                        
原文链接：https://blog.csdn.net/D_boj/article/details/132286492>)](<文章目录
1.概述
1.1定义
1.2作用
1.3简介
1.4狭义和广义
1.5模块组成
1.5.1Spring Core（核心容器）
1.5.2Spring AOP（面向切面编程）
1.5.3Spring Data Access（数据访问）
1.5.4Spring Web（应用程序）
1.5.5Spring Message（消息传递）
1.5.6Spring test（测试）
1.6Spring Framework（框架）
1.6.1概述
1.6.2作用
1.6.3特点
1.7 特点
2.基本用例-Spring框架基本使用
3.原理
4.启用日志框架
4.1概述
4.2组成
4.3基本用例-Log4j2基本使用
5.容器：IoC（重点）
5.1概述
5.1.1定义
5.1.2简介
5.1.3作用
5.1.4依赖注入
5.1.4.1定义
5.1.4.2作用
5.1.4.3实现方式
5.1.5实现
5.2基于XML管理Bean（了解）
5.2.1获取Bean的方式
5.2.1.1根据ID获取Bean
5.2.1.2根据类型获取Bean
5.2.1.3根据Id和类型获取Bean
5.2.2依赖注入
5.2.2.1根据setter注入
5.2.2.2根据构造器注入
5.2.3特殊值处理
5.2.3.1字面量赋值
5.2.3.2null值
5.2.3.3xml实体
5.2.3.4CDATA节
5.2.4注入对象类型属性值
5.2.4.1引用外部Bean
5.2.4.2引用内部Bean
5.2.4.3级联属性赋值
5.2.5注入数组类型属性值
5.2.6注入集合类型属性值
5.2.6.1注入List集合类型属性值
5.2.6.2注入Map集合类型属性值
5.2.6.2注入引用集合类型属性值
5.2.7引入P命名空间属性值
5.2.8引入外部属性文件
5.2.9引入Bean的作用域
5.2.10Bean的生命周期
5.2.11引入FactoryBean属性值
5.2.12引入xml自动装配
5.3基于注解管理Bean（重点）
5.3.1概述
5.3.1.1简介
5.3.1.2步骤
5.3.1.3使用注解
5.3.2开启组件扫描
5.3.2.1概述
5.3.2.2基本用例-实现组件扫描
5.3.2.3指定要排除的组件
5.3.2.4仅扫描指定组件
5.3.2使用注解定义Bean
5.3.3使用@Autowired注入
5.3.3.1概述
5.3.3.2属性注入
5.3.3.3set注入
5.3.3.4构造方法注入
5.3.3.5形参注入
5.3.3.6无注解注入
5.3.3.7联合@Qualifier注解注入
5.3.4使用@Resource注入
5.3.4.1概述
5.3.4.2Name注入
5.3.4.3未知Name注入
5.3.4.4类型注入
5.3.5全注解开发
5.3.5.1概述
5.3.5.2基本用例-全注解开发实现
5.4原理
6.面向切面：AOP (重点)
6.1概述
6.1.1定义
6.1.2作用
6.1.3横切关注点
6.1.4通知（增强）
6.1.5切面
6.1.6目标
6.1.7代理
6.1.8连接点
6.1.9切入点
6.2代理模式
6.2.1概述
6.2.2静态代理
6.2.3动态代理
6.2.3.1概述
6.2.3.1.1定义
6.2.3.1.2分类
6.2.3.2基本用例-实现动态代理
6.3切入点表达式
6.4基于注解的AOP
6.4.1概述
6.4.2基本用例-注解实现AOP
6.4.3通知方式
6.4.3.1前置通知
6.4.3.2异常通知
6.4.3.3返回通知
6.4.3.4后置通知
6.4.3.5环绕通知
6.4.4获取通知信息
6.4.4.1获取连接点信息
6.4.4.2获取目标方法的返回值
6.4.4.3获取目标方法的异常
6.4.5重用切入点表达式
6.4.5.1声明
6.4.5.2同切面使用
6.4.5.3不同切面使用
6.5基于XML的AOP（了解）
知识加油站
1.自动装配和依赖注入的区别与联系
2.依赖注入的两种方式
1.概述
笔记小结：

含义：Spring 是一款主流的 Java EE 轻量级开源框架，包含Spring MVC、Spring Boot、Spring Cloud等
作用：简化 Java 企业级应用的开发难度和开发周期，提供了整合其他技术和框架的能力
简介：核心功能是控制反转(IoC)和面向切面(AOP)
组成：
Spring Core（核心容器）
Spring AOP（面向切面编程）
Spring **Data Access（**数据访问）
Spring Web（应用程序）
Spring Message（消息传递）
Spring test（测试）
Spring Framework（框架）
概述：Spring Framework是Spring项目的核心框架
作用：Spring Framework实现IOC容器和AOP技术的功能模块
特点：
非侵入式
控制反转
面向切面编程
容器
组件化
特点：
轻：框架轻量级，不依赖其余Spring的对象
控制反转（IOC）：实现了对象之间的松耦合
面向切面（AOP）：分离应用的业务逻辑与系统级服务
容器：Spring包含并管理应用对象的配置和生命周期
1.1定义
​ Spring 是一款主流的 Java EE 轻量级开源框架 ，由于其轻便、易用和高效，被广泛应用于企业级Java应用开发中。

​ Spring包含了很多子框架和扩展，如Spring MVC、Spring Boot、Spring Cloud等。

​ Spring的主要特点是IOC容器和AOP技术，它们使得Java应用的开发和管理更加简单和高效。

1.2作用
​ Spring 目的是用于简化 Java 企业级应用的开发难度和开发周期。Spring 框架除了自己提供功能外，还提供整合其他技术和框架的能力

1.3简介
​ 自 2004 年 4 月，Spring 1.0 版本正式发布以来，Spring 已经步入到了第 6 个大版本，也就是 Spring 6。



说明：

​ 参考链接：Spring Framework

Spring是一个轻量级的控制反转(IoC)和面向切面(AOP)的容器框架。
Spring最初的出现是为了解决EJB臃肿的设计，以及难以测试等问题。
Spring为简化开发而生，让程序员只需关注核心业务的实现，尽可能的不再关注非业务逻辑代码（事务控制，安全日志等）。
1.4狭义和广义
广义的 Spring：Spring 技术栈
​ 广义上的 Spring 泛指以 Spring Framework 为核心的 Spring 技术栈。

​ 经过十多年的发展，Spring 已经不再是一个单纯的应用框架，而是逐渐发展成为一个由多个不同子项目（模块）组成的成熟技术，例如 Spring Framework、Spring MVC、SpringBoot、Spring Cloud、Spring Data、Spring Security 等，其中 Spring Framework 是其他子项目的基础。

​ 这些子项目涵盖了从企业级应用开发到云计算等各方面的内容，能够帮助开发人员解决软件发展过程中不断产生的各种实际问题，给开发人员带来了更好的开发体验。

狭义的 Spring：Spring Framework
​ 狭义的 Spring 特指 Spring Framework，通常我们将它称为 Spring 框架。

​ Spring 框架是一个分层的、面向切面的 Java 应用程序的一站式轻量级解决方案，它是 Spring 技术栈的核心和基础，是为了解决企业级应用开发的复杂性而创建的。

Spring 有两个最核心模块： IoC 和 AOP。

IoC：Inverse of Control 的简写，译为“控制反转”，指把创建对象过程交给 Spring 进行管理。
AOP：Aspect Oriented Programming 的简写，译为“面向切面编程”。AOP 用来封装多个类的公共行为，将那些与业务无关，却为业务模块所共同调用的逻辑封装起来，减少系统的重复代码，降低模块间的耦合度。另外，AOP 还解决一些系统层面上的问题，比如日志、事务、权限等。
1.5模块组成


说明：

​ 上图中包含了 Spring 框架的所有模块，这些模块可以满足一切企业级应用开发的需求，在开发过程中可以根据需求有选择性地使用所需要的模块。下面分别对这些模块的作用进行简单介绍。

1.5.1Spring Core（核心容器）
​ spring core提供了IOC,DI,Bean配置装载创建的核心实现。核心概念： Beans、BeanFactory、BeanDefinitions、ApplicationContext。

spring-core ：IOC和DI的基本实现

spring-beans：BeanFactory和Bean的装配管理(BeanFactory)

spring-context：Spring context上下文，即IOC容器(AppliactionContext)

spring-expression：spring表达式语言

1.5.2Spring AOP（面向切面编程）
spring-aop：面向切面编程的应用模块，整合ASM，CGLib，JDK Proxy
spring-aspects：集成AspectJ，AOP应用框架
spring-instrument：动态Class Loading模块
1.5.3Spring Data Access（数据访问）
spring-jdbc：spring对JDBC的封装，用于简化jdbc操作
spring-orm：java对象与数据库数据的映射框架
spring-oxm：对象与xml文件的映射框架
spring-jms： Spring对Java Message Service(java消息服务)的封装，用于服务之间相互通信
spring-tx：spring jdbc事务管理
1.5.4Spring Web（应用程序）
spring-web：最基础的web支持，建立于spring-context之上，通过servlet或listener来初始化IOC容器
spring-webmvc：实现web mvc
spring-websocket：与前端的全双工通信协议
spring-webflux：Spring 5.0提供的，用于取代传统java servlet，非阻塞式Reactive Web框架，异步，非阻塞，事件驱动的服务
1.5.5Spring Message（消息传递）
Spring-messaging：spring 4.0提供的，为Spring集成一些基础的报文传送服务
1.5.6Spring test（测试）
spring-test：集成测试支持，主要是对junit的封装
1.6Spring Framework（框架）
1.6.1概述
​ Spring Framework是Spring项目的核心框架，而Spring是整个Spring项目的总称，包括了Spring Framework和其他相关的子项目和扩展



1.6.2作用
​ Spring Framework实现IOC容器和AOP技术的功能模块

​ Spring Framework包含了许多模块，如Core模块、Beans模块、Context模块、AOP模块、Web模块等，每个模块都提供了不同的功能，可以灵活地选择使用。Spring Framework的目标是为了简化企业级Java开发，提高开发效率和质量。

1.6.3特点
非侵入式：使用 Spring Framework 开发应用程序时，Spring 对应用程序本身的结构影响非常小。对领域模型可以做到零污染；对功能性组件也只需要使用几个简单的注解进行标记，完全不会破坏原有结构，反而能将组件结构进一步简化。这就使得基于 Spring Framework 开发应用程序时结构清晰、简洁优雅。

控制反转：IoC——Inversion of Control，翻转资源获取方向。把自己创建资源、向环境索取资源变成环境将资源准备好，我们享受资源注入。

面向切面编程：AOP——Aspect Oriented Programming，在不修改源代码的基础上增强代码功能。

容器：Spring IoC 是一个容器，因为它包含并且管理组件对象的生命周期。组件享受到了容器化的管理，替程序员屏蔽了组件创建过程中的大量细节，极大的降低了使用门槛，大幅度提高了开发效率。

组件化：Spring 实现了使用简单的组件配置组合成一个复杂的应用。在 Spring 中可以使用 XML 和 Java 注解组合这些对象。这使得我们可以基于一个个功能明确、边界清晰的组件有条不紊的搭建超大型复杂应用系统。

一站式：在 IoC 和 AOP 的基础上可以整合各种企业应用的开源框架和优秀的第三方类库。而且 Spring 旗下的项目已经覆盖了广泛领域，很多方面的功能性需求可以在 Spring Framework 的基础上全部使用 Spring 来实现。

1.7 特点
轻
从大小与开销两方面而言Spring都是轻量的。完整的Spring框架可以在一个大小只有1MB多的JAR文件里发布。并且Spring所需的处理开销也是微不足道的。
Spring是非侵入式的：Spring应用中的对象不依赖于Spring的特定类。
控制反转
Spring通过一种称作控制反转（IoC）的技术促进了松耦合。当应用了IoC，一个对象依赖的其它对象会通过被动的方式传递进来，而不是这个对象自己创建或者查找依赖对象。你可以认为IoC与JNDI相反——不是对象从容器中查找依赖，而是容器在对象初始化时不等对象请求就主动将依赖传递给它。
面向切面
Spring提供了面向切面编程的丰富支持，允许通过分离应用的业务逻辑与系统级服务（例如审计（auditing）和事务（transaction）管理）进行内聚性的开发。应用对象只实现它们应该做的——完成业务逻辑——仅此而已。它们并不负责（甚至是意识）其它的系统级关注点，例如日志或事务支持。
容器
Spring包含并管理应用对象的配置和生命周期，在这个意义上它是一种容器，你可以配置你的每个bean如何被创建——基于一个可配置原型（prototype），你的bean可以创建一个单独的实例或者每次需要时都生成一个新的实例——以及它们是如何相互关联的。然而，Spring不应该被混同于传统的重量级的EJB容器，它们经常是庞大与笨重的，难以使用。
框架
Spring可以将简单的组件配置、组合成为复杂的应用。在Spring中，应用对象被声明式地组合，典型地是在一个XML文件里。Spring也提供了很多基础功能（事务管理、持久化框架集成等等），将应用逻辑的开发留给了你。
说明：

​ 所有Spring的这些特征使你能够编写更干净、更可管理、并且更易于测试的代码。它们也为Spring中的各种模块提供了基础支持。

Spring6要求JDK最低版本是JDK17


2.基本用例-Spring框架基本使用
说明：

​ 本基本用例演示，通过XML方式，实现Bean的自动注入

补充：环境

JDK：Java17+（Spring6要求JDK最低版本是Java17）

Maven：3.6+

Spring：6.0.2

步骤一：构建模块

通过Idea开发工具，创建空项目后创建子模块


说明：

​ 在空项目中，创建子模块

步骤二：导入依赖

修改模块的pom.xml文件
%3Cdependencies%3E
    <!--spring context依赖-->
    <!--当你引入Spring Context依赖之后，表示将Spring的基础依赖引入了-->
    <dependency>
        <groupId>org.springframework</groupId>
        <artifactId>spring-context</artifactId>
        <version>6.0.2</version>
    </dependency>

    <!--junit5测试-->
    <!--此依赖可选，主要便于junit进行测试使用-->
    <dependency>
        <groupId>org.junit.jupiter</groupId>
        <artifactId>junit-jupiter-api</artifactId>
        <version>5.3.1</version>
    </dependency>
</dependencies>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
说明：

​ 在pom.xml文件中，添加如上依赖

补充：

添加完成后，可在IDEA工具中的最右侧点击Maven进行查看


步骤三：创建实体

package org.example.entity;

public class User {
    public void add() {
        System.out.println("add……");
    }
}

1
2
3
4
5
6
7
8
说明：

​ 在org.example.entity包下，创建User实体

步骤四：创建配置文件

在模块的resources目录下，创建beans.xml文件
说明：

​ 创建beans.xml文件，是为了完成通过xml的方式实现依赖的自动注入

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd">

    <!--id是该bean的唯一标识符，在整个应用程序上下文中用于获取该bean实例-->
    <!--class是该bean所属的Java类的全限定名（包括包名），它告诉Spring需要实例化哪个类-->
    <bean id="user" class="org.example.entity.User"/>
</beans>
1
2
3
4
5
6
7
8
9
说明：

在beans,xml文件中，有bean标签
在beans,xml文件中，bean标签有Id属性，与class属性
步骤五：演示

在模块中的test.java包下，创建UserTest类
public class UserTest {
    @Test
    void newTest() {
        ApplicationContext applicationContext = new ClassPathXmlApplicationContext("beans.xml");
        User user = (User) applicationContext.getBean("user");
        user.add(); // add……
    }
}
1
2
3
4
5
6
7
8
补充：

@Test 是 JUnit 框架中的一个注解，表示该方法是一个测试方法，会被 JUnit 框架执行。

3.原理
笔记小结：通过XML方式，实现Bean的自动注入的基本用例原理

创建对象时，会调用无参构造方法
Spring 是通过反射机制调用无参构造方法创建对象
Spring 创建的对象（Bean对象），最终存储在Spring容器中
1.创建对象时，会调用无参构造方法

public class HelloWorld {
    public HelloWorld() {
        System.out.println("无参数构造方法执行");
    }
    public void sayHello(){
        System.out.println("helloworld");
    }
}
1
2
3
4
5
6
7
8
说明：



2.Spring 是通过反射机制调用无参构造方法创建对象

// dom4j解析beans.xml文件，从中获取class属性值，类的全类名
// 通过反射机制调用无参数构造方法创建对象
Class clazz = Class.forName("com.atguigu.spring6.bean.HelloWorld");
//Object obj = clazz.newInstance();
Object object = clazz.getDeclaredConstructor().newInstance();
1
2
3
4
5
3.Spring 创建的对象（Bean对象），最终存储在Spring容器中

private final Map<String, BeanDefinition> beanDefinitionMap = new ConcurrentHashMap<>(256);
1
说明：

Spring容器底层就是一个map集合
存储bean的map在DefaultListableBeanFactory类中
Spring容器加载到Bean类时 , 会把这个类的描述信息, 以包名加类名的方式存到beanDefinitionMap 中
Map<String,BeanDefinition> , 其中 String是Key , 默认是类名首字母小写 。BeanDefinition , 存的是类的定义(描述信息) , 我们通常叫BeanDefinition接口为 : bean的定义对象。
4.启用日志框架
笔记小结：

概述：Log4j2是一个开源的Java日志框架，帮助Java开发人员在应用程序中实现灵活和可配置的日志记录

组成：

日志信息的优先级：TRACE < DEBUG < INFO < WARN < ERROR < FATAL
日志信息的输出目的地：控制台或者本地文件
日志信息的输出格式：日志信息的显示内容
基本用例：

导入依赖：
<!--log4j2的依赖-->
<dependency>
  <groupId>org.apache.logging.log4j</groupId>
  <artifactId>log4j-core</artifactId>
  <version>2.19.0</version>
</dependency>
<dependency>
  <groupId>org.apache.logging.log4j</groupId>
  <artifactId>log4j-slf4j2-impl</artifactId>
  <version>2.19.0</version>
</dependency>
1
2
3
4
5
6
7
8
9
10
11
创建日志配置文件：建议复制根据需求修改

使用日志

private Logger logger = LoggerFactory.getLogger(HelloWorldTest.class);
……
logger.info("执行成功");
1
2
3
结果：



4.1概述
​ Log4j2是一个开源的Java日志框架，是Log4j的升级版。它可以帮助Java开发人员在应用程序中实现灵活和可配置的日志记录，支持异步日志记录、多线程安全等特性

4.2组成
日志信息的优先级，日志信息的优先级从高到低有TRACE < DEBUG < INFO < WARN < ERROR < FATAL

说明：

TRACE：追踪，是最低的日志级别，相当于追踪程序的执行
DEBUG：调试，一般在开发中，都将其设置为最低的日志级别
INFO：信息，输出重要的信息，使用较多
WARN：警告，输出警告的信息
ERROR：错误，输出错误信息
FATAL：严重错误
日志信息的输出目的地，日志信息的输出目的地指定了日志将打印到控制台还是文件中；

日志信息的输出格式，而输出格式则控制了日志信息的显示内容。

4.3基本用例-Log4j2基本使用
步骤一：引入Log4j2依赖

修改模块中的pom.xml文件
<!--log4j2的依赖-->
<dependency>
    <groupId>org.apache.logging.log4j</groupId>
    <artifactId>log4j-core</artifactId>
    <version>2.19.0</version>
</dependency>
<dependency>
    <groupId>org.apache.logging.log4j</groupId>
    <artifactId>log4j-slf4j2-impl</artifactId>
    <version>2.19.0</version>
</dependency>
1
2
3
4
5
6
7
8
9
10
11
说明：

​ log4j的Maven使用光有核心core依赖不够，还需要有实现impl依赖

步骤二：创建日志配置文件

在模块文件路径在resource的根路径下，配置文件名为log4j2.xml
<?xml version="1.0" encoding="UTF-8"?>
<configuration>
    <loggers>
        <!--
            level指定日志级别，从低到高的优先级：
                TRACE < DEBUG < INFO < WARN < ERROR < FATAL
                trace：追踪，是最低的日志级别，相当于追踪程序的执行
                debug：调试，一般在开发中，都将其设置为最低的日志级别
                info：信息，输出重要的信息，使用较多
                warn：警告，输出警告的信息
                error：错误，输出错误信息
                fatal：严重错误
        -->
        <root level="DEBUG">
            <appender-ref ref="spring6log"/>
            <appender-ref ref="RollingFile"/>
            <appender-ref ref="log"/>
        </root>
    </loggers>

    <appenders>
        <!--输出日志信息到控制台-->
        <console name="spring6log" target="SYSTEM_OUT">
            <!--控制日志输出的格式-->
            <PatternLayout pattern="%d{yyyy-MM-dd HH:mm:ss SSS} [%t] %-3level %logger{1024} - %msg%n"/>
        </console>

        <!--文件会打印出所有信息，这个log每次运行程序会自动清空，由append属性决定，适合临时测试用-->
        <File name="log" fileName="d:/spring6_log/test.log" append="false">
            <PatternLayout pattern="%d{HH:mm:ss.SSS} %-5level %class{36} %L %M - %msg%xEx%n"/>
        </File>

        <!-- 这个会打印出所有的信息，
            每次大小超过size，
            则这size大小的日志会自动存入按年份-月份建立的文件夹下面并进行压缩，
            作为存档-->
        <RollingFile name="RollingFile" fileName="d:/spring6_log/app.log"
                     filePattern="log/$${date:yyyy-MM}/app-%d{MM-dd-yyyy}-%i.log.gz">
            <PatternLayout pattern="%d{yyyy-MM-dd 'at' HH:mm:ss z} %-5level %class{36} %L %M - %msg%xEx%n"/>
            <SizeBasedTriggeringPolicy size="50MB"/>
            <!-- DefaultRolloverStrategy属性如不设置，
            则默认为最多同一文件夹下7个文件，这里设置了20 -->
            <DefaultRolloverStrategy max="20"/>
        </RollingFile>
    </appenders>
</configuration>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
步骤三：日常使用

在日常中，只用log4j2，此处创建HelloWorldTest使用
public class HelloWorldTest {

    // 1.通过日志工程获取日志对象记录器
    private Logger logger = LoggerFactory.getLogger(HelloWorldTest.class);
 
    @Test
    public void testHelloWorld(){
        ApplicationContext ac = new ClassPathXmlApplicationContext("beans.xml");
        HelloWorld helloworld = (HelloWorld) ac.getBean("helloWorld");
        helloworld.sayHello();
        // 2.记录日志
        logger.info("执行成功");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
说明：

​ 创建日志记录器

步骤四：演示



说明：

​ 当完成以上步骤后，运行，日志就会输出在控制台

5.容器：IoC（重点）
笔记小结：见各个小节

5.1概述
笔记小结：

定义：IoC (Inversion of Control)，即控制反转，是一种设计模式或者说设计思想
简介：Spring 通过 IoC 容器来管理所有 Java 对象的实例化和初始化，控制对象与对象之间的依赖关系
作用：通过容器来管理对象的创建、销毁、依赖注入等操作，而应用程序本身只需要使用这些对象即可
依赖注入:
含义：以解耦对象之间的依赖关系
作用：Spring通过依赖注入的方式来完成Bean管理的。换句话说，依赖注入，依赖注入实现了控制反转的思想
实现方式（重点）：
setter注入
构造注入
实现接口以及常用类：
BeanFactory接口：面向 Spring 本身，不提供给开发人员使用
ApplicationContext接口：面向 Spring 的使用者，几乎所有场合（创建、管理Bean实例，支持国际化、资源访问、消息传递）都适用
常用类：
FileSystemXmlApplicationContext：通过文件系统路径读取 XML 格式的配置文件创建 IOC 容器对象
ClassPathXmlApplicationContext：通过读取类路径下的 XML 格式的配置文件创建 IOC 容器对象
5.1.1定义
​ IoC (Inversion of Control)，即控制反转，是一种设计模式或者说设计思想，它是面向对象编程中的一种概念，用来描述对象之间的依赖关系，指导我们如何设计出松耦合、更优良的程序。

5.1.2简介
​ Spring 通过 IoC 容器来管理所有 Java 对象的实例化和初始化，控制对象与对象之间的依赖关系。我们将由 IoC 容器管理的 Java 对象称为 Spring Bean，它与使用关键字 new 创建的 Java 对象没有任何区别。

5.1.3作用
​ 在 IoC 模式中，控制权从程序代码中转移到了容器中，即通过容器来管理对象的创建、销毁、依赖注入等操作，而应用程序本身只需要使用这些对象即可。这样，应用程序就不需要自己管理对象之间的依赖关系，而是由容器来管理，从而实现了代码的解耦和更好的可维护性，提高程序扩展力。

说明：

将对象的创建权利交出去，交给第三方容器负责
将对象和对象之间关系的维护权交出去，交给第三方容器负责
5.1.4依赖注入
5.1.4.1定义
​ 依赖注入（Dependency Injection，DI）是一种设计模式，其主要思想是在程序运行的过程中，通过外部容器（如Spring容器）动态地将依赖对象注入到程序中，以解耦对象之间的依赖关系，从而提高程序的灵活性、可维护性和可测试性。

5.1.4.2作用
​ **Spring通过依赖注入的方式来完成Bean管理的。**换句话说，依赖注入，依赖注入实现了控制反转的思想。依赖指的是对象和对象之间的关联关系。注入指的是一种数据传递行为，通过注入行为来让对象和对象产生关系。

补充：

​ Bean管理说的是：Bean对象的创建，以及Bean对象中属性的赋值（或者叫做Bean对象之间关系的维护）。

5.1.4.3实现方式
第一种：set注入
第二种：构造注入
5.1.5实现
​ Spring 的框架中，IoC 容器是通过 BeanFactory 和 ApplicationContext 接口实现的。BeanFactory 接口是 Spring 框架最底层的接口，提供了基本的 IoC 功能；ApplicationContext 接口是 BeanFactory 接口的子接口，提供了更高级的特性和功能，如 AOP、国际化、事件驱动等。其中BeanFactory 接口，最重要的方法是getBean()方法，用于从容器中获取对象。

​ Spring 的 IoC 容器就是 IoC思想的一个落地的产品实现。IoC容器中管理的组件也叫做 bean。在创建 bean 之前，首先需要创建IoC 容器。Spring 提供了IoC 容器的两种实现方式：

BeanFactory：这是 IoC 容器的基本实现，是 Spring 内部使用的接口。面向 Spring 本身，不提供给开发人员使用。
ApplicationContext：BeanFactory 的子接口，提供了更多高级特性。面向 Spring 的使用者，几乎所有场合都使用 ApplicationContext 而不是底层的 BeanFactory
ApplicationContext的主要实现类:

类型名	简介
ClassPathXmlApplicationContext	通过读取类路径下的 XML 格式的配置文件创建 IOC 容器对象
FileSystemXmlApplicationContext	通过文件系统路径读取 XML 格式的配置文件创建 IOC 容器对象
ConfigurableApplicationContext	ApplicationContext 的子接口，包含一些扩展方法 refresh() 和 close() ，让 ApplicationContext 具有启动、关闭和刷新上下文的能力。
WebApplicationContext	专门为 Web 应用准备，基于 Web 环境创建 IOC 容器对象，并将对象引入存入 ServletContext 域中。


说明：

​ ApplicationContext有众多的实现类，其中最常用的就是ClassPathXmlApplicationContext与FileSystemXmlApplicationContext实现类

5.2基于XML管理Bean（了解）
笔记小结：

获取Bean的方式：

根据ID：

User user = (User) applicationContext.getBean("user");
1
根据类型：

 User user = (User) applicationContext.getBean(User.class);
1
根据Id和类型:

User user = (User) applicationContext.getBean("user", User.class);
1
依赖注入

根据Setter注入：<property/>
根据构造器注入：<constructor-arg/>
特殊值处理

字面量赋值<property>
Null值<null>
Xml实体：属性值value="a &lt; b"
CDATA节：标签内容<![CDATA[a < b]]>
注入对象类型属性值

引用外部Bean：属性ref
引用内部Bean：bean嵌套
级联属性赋值：引入对象后，级联赋值name="clazz.clazzId"
注入数组类型属性值：<array></array>

注入集合类型属性值：

注入List集合类型属性值： <list> </list>
注入Map集合类型属性值：<map><entry><<key>/key><value></value></entry></map>
注入引用集合类型属性值：<util></util>
注意：使用前，需要引入util命名空间
引入P命名空间属性值：属性p:

注意：使用前，需要引入p命名空间
引入外部属性文件：<context:property-placeholder location="classpath:jdbc.properties"/>

引入Bean的作用域：属性scope属性值prototype（多例）、singleton（单例）

Bean的生命周期：

bean对象创建（调用无参构造器）

bean对象设置属性

bean的后置处理器（初始化之前）

bean对象初始化（需在配置bean时指定初始化方法）

bean的后置处理器（初始化之后）

bean对象就绪可以使用

bean对象销毁（需在配置bean时指定销毁方法）

IOC容器关闭

引入FactoryBean属性值：实现FactoryBean<T>接口

引入自动装配：属性值autowire属性值byType、byName

5.2.1获取Bean的方式
5.2.1.1根据ID获取Bean
public class UserTest {
    @Test
    void newTest() {
        ApplicationContext applicationContext = new ClassPathXmlApplicationContext("beans.xml");
        User user = (User) applicationContext.getBean("user");
        user.add(); // add……
    }
}
1
2
3
4
5
6
7
8
说明：

​ 此获取方式，需要基于第2.基本用例进行查看

5.2.1.2根据类型获取Bean
public class UserTest {
    @Test
    void newTest() {
        ApplicationContext applicationContext = new ClassPathXmlApplicationContext("beans.xml");
        User user = (User) applicationContext.getBean(User.class);
        user.add(); // add……
    }
}
1
2
3
4
5
6
7
8
注意：

当根据类型获取bean时，要求IOC容器中指定类型的bean有且只能有一个

org.springframework.beans.factory.NoUniqueBeanDefinitionException: No qualifying bean of type 'com.atguigu.spring6.bean.HelloWorld' available: expected single matching bean but found 2: helloworldOne,helloworldTwo
1
说明：

​ 此获取方式，需要基于第2.基本用例进行查看

5.2.1.3根据Id和类型获取Bean
public class UserTest {
    @Test
    void newTest() {
        ApplicationContext applicationContext = new ClassPathXmlApplicationContext("beans.xml");
        User user = (User) applicationContext.getBean("user", User.class);
        user.add(); // add……
    }
}
1
2
3
4
5
6
7
8
补充：

​ 如果组件类实现了接口，可以根据接口类型获取Bean，但前提是Bean唯一

说明：

​ 此获取方式，需要基于第2.基本用例进行查看

5.2.2依赖注入
5.2.2.1根据setter注入
步骤一：创建学生类Student

package com.atguigu.spring6.bean;

public class Student {

    private Integer id;

    private String name;

    private Integer age;

    private String sex;

    public Student() {
    }

    public Integer getId() {
        return id;
    }

    public void setId(Integer id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public Integer getAge() {
        return age;
    }

    public void setAge(Integer age) {
        this.age = age;
    }

    public String getSex() {
        return sex;
    }

    public void setSex(String sex) {
        this.sex = sex;
    }

    @Override
    public String toString() {
        return "Student{" +
                "id=" + id +
                ", name='" + name + '\'' +
                ", age=" + age +
                ", sex='" + sex + '\'' +
                '}';
    }

}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
步骤二：配置bean时为属性赋值

<bean id="studentOne" class="com.atguigu.spring6.bean.Student">
    <!-- property标签：通过组件类的setXxx()方法给组件对象设置属性 -->
    <!-- name属性：指定属性名（这个属性名是getXxx()、setXxx()方法定义的，和成员变量无关） -->
    <!-- value属性：指定属性值 -->
    <property name="id" value="1001"></property>
    <property name="name" value="张三"></property>
    <property name="age" value="23"></property>
    <property name="sex" value="男"></property>
</bean>
1
2
3
4
5
6
7
8
9
说明：

​ 当使用标签标签完成对象的属性创建时，name需要跟对象中的成员变量同名

步骤三：演示

@Test
public void testDIBySet(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-di.xml");
    Student studentOne = ac.getBean("studentOne", Student.class);
    System.out.println(studentOne);
}
1
2
3
4
5
6
说明：

​ 当打印输出是，由于基于XML根据Setter注入方式进行对象的创建，此时输出可获得成员方法tostring的内容

5.2.2.2根据构造器注入
步骤一：在基于根据setter注入的基础上，在Student类中添加有参构造

public Student(Integer id, String name, Integer age, String sex) {
    this.id = id;
    this.name = name;
    this.age = age;
    this.sex = sex;
}
1
2
3
4
5
6
步骤二：配置bean

<bean id="studentTwo" class="com.atguigu.spring6.bean.Student">
    <constructor-arg name="id" value="1002"></constructor-arg>
    <constructor-arg name="name" value="李四"></constructor-arg>
    <constructor-arg name="age"value="33"></constructor-arg>
    <constructor-arg name="sex" value="女"></constructor-arg>
</bean>
1
2
3
4
5
6
说明：

constructor-arg标签属性描述构造器参数：
index属性：指定参数所在位置的索引（从0开始）
name属性：指定参数名，name需要跟对象中的成员变量同名
步骤三：演示

@Test
public void testDIByConstructor(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-di.xml");
    Student studentOne = ac.getBean("studentTwo", Student.class);
    System.out.println(studentOne);
}
1
2
3
4
5
6
说明：

​ 当打印输出是，由于基于XML根据构造器注入方式进行对象的创建，此时输出可获得成员方法tostring的内容

5.2.3特殊值处理
5.2.3.1字面量赋值
<!-- 使用value属性给bean的属性赋值时，Spring会把value属性的值看做字面量 -->
<property name="name" value="张三"/>
1
2
5.2.3.2null值
<property name="name">
    <null />
</property>
1
2
3
细节：

<property name="name" value="null"></property>
1
以上写法，为name所赋值为字符串null

5.2.3.3xml实体
<!-- 解决方案一：使用XML实体来代替 -->
<property name="expression" value="a &lt; b"/>
1
2
说明：

​ 小于号在XML文档中用来定义标签的开始，不能随便使用

5.2.3.4CDATA节
<property name="expression">
    <!-- 解决方案二：使用CDATA节 -->
    <value><![CDATA[a < b]]></value>
</property>
1
2
3
4
说明：

CDATA中的C代表Character，是文本、字符的含义，CDATA就表示纯文本数据
ML解析器看到CDATA节就知道这里是纯文本，就不会当作XML标签或属性来解析
所以CDATA节中写什么符号都随意
5.2.4注入对象类型属性值
5.2.4.1引用外部Bean
步骤一：配置Clazz类型的bean

<bean id="clazzOne" class="com.atguigu.spring6.bean.Clazz">
    <property name="clazzId" value="1111"></property>
    <property name="clazzName" value="财源滚滚班"></property>
</bean>
1
2
3
4
步骤二：为Student中的clazz属性赋值

<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->
    <property name="clazz" ref="clazzOne"></property>
</bean>
1
2
3
4
5
6
7
8
说明：

​ 当引用外部对象时，需要将ref属性变为Value属性。ref属性，值表示引用对象、value属性，值表示字符串

5.2.4.2引用内部Bean
步骤一：在引用外部Bean的基础上

<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <property name="clazz">
        <!-- 在一个bean中再声明一个bean就是内部bean -->
        <!-- 内部bean只能用于给属性赋值，不能在外部通过IOC容器获取，因此可以省略id属性 -->
        <bean id="clazzInner" class="com.atguigu.spring6.bean.Clazz">
            <property name="clazzId" value="2222"></property>
            <property name="clazzName" value="远大前程班"></property>
        </bean>
    </property>
</bean>
1
2
3
4
5
6
7
8
9
10
11
12
13
14
说明：

​ 将Bean写于属性标签内，即为引用内部Bean

5.2.4.3级联属性赋值
步骤一：在引用内部Bean的基础上

<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <property name="clazz" ref="clazzOne"></property>
    <property name="clazz.clazzId" value="3333"></property>
    <property name="clazz.clazzName" value="最强王者班"></property>
</bean>
1
2
3
4
5
6
7
8
9
5.2.5注入数组类型属性值
步骤一：在Student类中中添加成员变量数组和getter于setter方法

private String[] hobbies;

public String[] getHobbies() {
    return hobbies;
}

public void setHobbies(String[] hobbies) {
    this.hobbies = hobbies;
}
1
2
3
4
5
6
7
8
9
步骤二：配置Bean

<bean id="studentFour" class="com.atguigu.spring.bean6.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->
    <property name="clazz" ref="clazzOne"></property>
    <property name="hobbies">
        <array>
            <value>抽烟</value>
            <value>喝酒</value>
            <value>烫头</value>
        </array>
    </property>
</bean>
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
说明：

​ 当注入数组类型数据时，需要使用标签

5.2.6注入集合类型属性值
5.2.6.1注入List集合类型属性值
步骤一：在Clazz类中添加添加成员变量集合和getter于setter方法

private List<Student> students;

public List<Student> getStudents() {
    return students;
}

public void setStudents(List<Student> students) {
    this.students = students;
}
1
2
3
4
5
6
7
8
9
步骤二：配置Bean

<bean id="clazzTwo" class="com.atguigu.spring6.bean.Clazz">
    <property name="clazzId" value="4444"></property>
    <property name="clazzName" value="Javaee0222"></property>
    <property name="students">
        <list>
            <ref bean="studentOne"></ref>
            <ref bean="studentTwo"></ref>
            <ref bean="studentThree"></ref>
        </list>
    </property>
</bean>
1
2
3
4
5
6
7
8
9
10
11
说明：

​ 当注入List集合类型数据时，需要使用标签

细节：

​ 因为List students，List集合中引用的是Student对象，因此注入时需要使用标签，进行引用对象

5.2.6.2注入Map集合类型属性值
步骤一：创建Student类

package com.atguigu.spring6.bean;
public class Teacher {

    private Integer teacherId;

    private String teacherName;

    public Integer getTeacherId() {
        return teacherId;
    }

    public void setTeacherId(Integer teacherId) {
        this.teacherId = teacherId;
    }

    public String getTeacherName() {
        return teacherName;
    }

    public void setTeacherName(String teacherName) {
        this.teacherName = teacherName;
    }

    public Teacher(Integer teacherId, String teacherName) {
        this.teacherId = teacherId;
        this.teacherName = teacherName;
    }

    public Teacher() {

    }
    
    @Override
    public String toString() {
        return "Teacher{" +
                "teacherId=" + teacherId +
                ", teacherName='" + teacherName + '\'' +
                '}';
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
步骤二：在Student类中添加添加成员变量集合和getter于setter方法

private Map<String, Teacher> teacherMap;

public Map<String, Teacher> getTeacherMap() {
    return teacherMap;
}

public void setTeacherMap(Map<String, Teacher> teacherMap) {
    this.teacherMap = teacherMap;
}
1
2
3
4
5
6
7
8
9
步骤三：配置bean

<bean id="teacherOne" class="com.atguigu.spring6.bean.Teacher">
    <property name="teacherId" value="10010"></property>
    <property name="teacherName" value="大宝"></property>
</bean>

<bean id="teacherTwo" class="com.atguigu.spring6.bean.Teacher">
    <property name="teacherId" value="10086"></property>
    <property name="teacherName" value="二宝"></property>
</bean>

<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->
    <property name="clazz" ref="clazzOne"></property>
    <property name="hobbies">
        <array>
            <value>抽烟</value>
            <value>喝酒</value>
            <value>烫头</value>
        </array>
    </property>
    <property name="teacherMap">
        <map>
            <entry>
                <key>
                    <value>10010</value>
                </key>
                <ref bean="teacherOne"></ref>
            </entry>
            <entry>
                <key>
                    <value>10086</value>
                </key>
                <ref bean="teacherTwo"></ref>
            </entry>
        </map>
    </property>
</bean>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
说明：

当注入Map集合类型数据时，需要使用标签
需要使用表示键值对
需要使用表示键
细节：

​ 因为Map<String, Teacher> teacherMap，Map集合中引用的是Teacher对象，因此注入时需要使用标签，进行引用对象

5.2.6.2注入引用集合类型属性值
步骤一：配置对应的命名空间

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns:util="http://www.springframework.org/schema/util"
    xsi:schemaLocation="http://www.springframework.org/schema/util
    http://www.springframework.org/schema/util/spring-util.xsd
    http://www.springframework.org/schema/beans
    http://www.springframework.org/schema/beans/spring-beans.xsd">
1
2
3
4
5
6
7
8
步骤二：配置Bean

<!--list集合类型的bean-->
<util:list id="students">
    <ref bean="studentOne"></ref>
    <ref bean="studentTwo"></ref>
    <ref bean="studentThree"></ref>
</util:list>
<!--map集合类型的bean-->
<util:map id="teacherMap">
    <entry>
        <key>
            <value>10010</value>
        </key>
        <ref bean="teacherOne"></ref>
    </entry>
    <entry>
        <key>
            <value>10086</value>
        </key>
        <ref bean="teacherTwo"></ref>
    </entry>
</util:map>
<bean id="clazzTwo" class="com.atguigu.spring6.bean.Clazz">
    <property name="clazzId" value="4444"></property>
    <property name="clazzName" value="Javaee0222"></property>
    <property name="students" ref="students"></property>
</bean>
<bean id="studentFour" class="com.atguigu.spring6.bean.Student">
    <property name="id" value="1004"></property>
    <property name="name" value="赵六"></property>
    <property name="age" value="26"></property>
    <property name="sex" value="女"></property>
    <!-- ref属性：引用IOC容器中某个bean的id，将所对应的bean为属性赋值 -->
    <property name="clazz" ref="clazzOne"></property>
    <property name="hobbies">
        <array>
            <value>抽烟</value>
            <value>喝酒</value>
            <value>烫头</value>
        </array>
    </property>
    <property name="teacherMap" ref="teacherMap"></property>
</bean>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
说明：

使用标签，可以将List集合或者Map集合的属性注入变为引用的方式
在使用util标签时，需要引入相应的命名空间
5.2.7引入P命名空间属性值
步骤一：引入P命名空间

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:util="http://www.springframework.org/schema/util"
       xmlns:p="http://www.springframework.org/schema/p"
       xsi:schemaLocation="http://www.springframework.org/schema/util
       http://www.springframework.org/schema/util/spring-util.xsd
       http://www.springframework.org/schema/beans
       http://www.springframework.org/schema/beans/spring-beans.xsd">
1
2
3
4
5
6
7
8
9
步骤二：通过p命名空间方式为bean的各个属性赋值

<bean id="studentSix" class="com.atguigu.spring6.bean.Student"
    p:id="1006" p:name="小明" p:clazz-ref="clazzOne" p:teacherMap-ref="teacherMap"></bean>
1
2
说明：

​ 通过p:成员属性，即可完成各个属性的赋值.

5.2.8引入外部属性文件
步骤一：添加依赖

 <!-- MySQL驱动 -->
<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <version>8.0.30</version>
</dependency>

<!-- 数据源 -->
<dependency>
    <groupId>com.alibaba</groupId>
    <artifactId>druid</artifactId>
    <version>1.2.15</version>
</dependency>
1
2
3
4
5
6
7
8
9
10
11
12
13
步骤二：创建外部属性文件

jdbc.user=root
jdbc.password=atguigu
jdbc.url=jdbc:mysql://localhost:3306/ssm?serverTimezone=UTC
jdbc.driver=com.mysql.cj.jdbc.Driver
1
2
3
4
说明：

​ 在resources文件下创建jdbc.properties文件

步骤三：引入属性文件

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:context="http://www.springframework.org/schema/context"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
                           http://www.springframework.org/schema/beans/spring-beans.xsd
                           http://www.springframework.org/schema/context
                           http://www.springframework.org/schema/context/spring-context.xsd">
    <!-- 引入外部属性文件 -->
    <context:property-placeholder location="classpath:jdbc.properties"/>
</beans>
1
2
3
4
5
6
7
8
9
10
11
注意：

​ 在使用 <context:property-placeholder> 元素加载外包配置文件功能前，首先需要在 XML 配置的一级标签 中添加 context 相关的约束。

步骤四：配置Bean

<!--完成数据库信息注入-->
<bean id="druidDataSource" class="com.alibaba.druid.pool.DruidDataSource">
    <property name="url" value="${jdbc.url}"/>
    <property name="driverClassName" value="${jdbc.driver}"/>
    <property name="username" value="${jdbc.user}"/>
    <property name="password" value="${jdbc.password}"/>
</bean>
1
2
3
4
5
6
7
说明：

​ 取外部文件中的值时，需要根据外部文件中属性的名字，可以把相应值取得

步骤五：演示

@Test
public void testDataSource() throws SQLException {
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-datasource.xml");
    DataSource dataSource = ac.getBean(DruidDataSource.class);
    Connection connection = dataSource.getConnection();
    System.out.println(connection);
}
1
2
3
4
5
6
7
5.2.9引入Bean的作用域
步骤一：创建类User

package com.atguigu.spring6.bean;
public class User {

    private Integer id;

    private String username;

    private String password;

    private Integer age;

    public User() {
    }

    public User(Integer id, String username, String password, Integer age) {
        this.id = id;
        this.username = username;
        this.password = password;
        this.age = age;
    }

    public Integer getId() {
        return id;
    }

    public void setId(Integer id) {
        this.id = id;
    }

    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public String getPassword() {
        return password;
    }

    public void setPassword(String password) {
        this.password = password;
    }

    public Integer getAge() {
        return age;
    }

    public void setAge(Integer age) {
        this.age = age;
    }

    @Override
    public String toString() {
        return "User{" +
                "id=" + id +
                ", username='" + username + '\'' +
                ", password='" + password + '\'' +
                ", age=" + age +
                '}';
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
步骤二：配置bean

<!-- scope属性：取值singleton（默认值），bean在IOC容器中只有一个实例，IOC容器初始化时创建对象 -->
<!-- scope属性：取值prototype，bean在IOC容器中可以有多个实例，getBean()时创建对象 -->
<bean class="com.atguigu.spring6.bean.User" scope="prototype"></bean>
1
2
3
说明：

属性值：
singleton（默认），在IOC容器中，这个bean的对象始终为单实例，当IOC容器初始化时即可创建对象
prototype，在IOC容器中，这个bean在IOC容器中有多个实例，当 获取bean时可创建对象
步骤三：演示

@Test
public void testBeanScope(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-scope.xml");
    User user1 = ac.getBean(User.class);
    User user2 = ac.getBean(User.class);
    System.out.println(user1==user2);
}
1
2
3
4
5
6
7
5.2.10Bean的生命周期
流程

bean对象创建（调用无参构造器）

bean对象设置属性

bean的后置处理器（初始化之前）

bean对象初始化（需在配置bean时指定初始化方法）

bean的后置处理器（初始化之后）

bean对象就绪可以使用

bean对象销毁（需在配置bean时指定销毁方法）

IOC容器关闭

步骤一：修改User类

public class User {

    private Integer id;

    private String username;

    private String password;

    private Integer age;

    public User() {
        System.out.println("生命周期：1、创建对象");
    }

    public User(Integer id, String username, String password, Integer age) {
        this.id = id;
        this.username = username;
        this.password = password;
        this.age = age;
    }

    public Integer getId() {
        return id;
    }

    public void setId(Integer id) {
        System.out.println("生命周期：2、依赖注入");
        this.id = id;
    }

    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public String getPassword() {
        return password;
    }

    public void setPassword(String password) {
        this.password = password;
    }

    public Integer getAge() {
        return age;
    }

    public void setAge(Integer age) {
        this.age = age;
    }

    public void initMethod(){
        System.out.println("生命周期：3、初始化");
    }

    public void destroyMethod(){
        System.out.println("生命周期：5、销毁");
    }

    @Override
    public String toString() {
        return "User{" +
                "id=" + id +
                ", username='" + username + '\'' +
                ", password='" + password + '\'' +
                ", age=" + age +
                '}';
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
64
65
66
67
68
69
70
71
72
说明：

​ 其中的initMethod()和destroyMethod()，可以通过配置Bean指定为初始化和销毁的方法

步骤二：创建Bean 的后置处理器

package com.atguigu.spring6.process;
    
import org.springframework.beans.BeansException;
import org.springframework.beans.factory.config.BeanPostProcessor;

public class MyBeanProcessor implements BeanPostProcessor {
    
    @Override
    public Object postProcessBeforeInitialization(Object bean, String beanName) throws BeansException {
        System.out.println("☆☆☆" + beanName + " = " + bean);
        return bean;
    }
    
    @Override
    public Object postProcessAfterInitialization(Object bean, String beanName) throws BeansException {
        System.out.println("★★★" + beanName + " = " + bean);
        return bean;
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
注意：

​ bean的后置处理器会在生命周期的初始化前后添加额外的操作，需要实现BeanPostProcessor接口，且配置到IOC容器中，需要注意的是，bean后置处理器不是单独针对某一个bean生效，而是针对IOC容器中所有bean都会执行

步骤三：配置Bean

<!-- 使用init-method属性指定初始化方法 -->
<!-- 使用destroy-method属性指定销毁方法 -->
<bean class="com.atguigu.spring6.bean.User" scope="prototype" init-method="initMethod" destroy-method="destroyMethod">
    <property name="id" value="1001"></property>
    <property name="username" value="admin"></property>
    <property name="password" value="123456"></property>
    <property name="age" value="23"></property>
</bean>
<!-- bean的后置处理器要放入IOC容器才能生效 -->
<bean id="myBeanProcessor" class="com.atguigu.spring6.process.MyBeanProcessor"/>
1
2
3
4
5
6
7
8
9
10
说明：

在配置Bean时，需要使用init-method属性和destroy-method属性进行配置Bean的初始化方法与销毁的方法
在配置Bean时，需要将Bean的后置处理器放入IOC容器才能生效
步骤四：演示

@Test
public void testLife(){
    ClassPathXmlApplicationContext ac = new ClassPathXmlApplicationContext("spring-lifecycle.xml");
    User bean = ac.getBean(User.class);
    System.out.println("生命周期：4、通过IOC容器获取bean并使用");
    ac.close();
}
1
2
3
4
5
6
7
5.2.11引入FactoryBean属性值


说明：

​ FactoryBean是Spring提供的一种整合第三方框架的常用机制。和普通的bean不同，配置一个FactoryBean类型的bean，在获取bean的时候得到的并不是class属性中配置的这个类的对象，而是getObject()方法的返回值。通过这种机制，Spring可以帮我们把复杂组件创建的详细过程和繁琐细节都屏蔽起来，只把最简洁的使用界面展示给我们。

步骤一 ：创建类UserFactoryBean

package com.atguigu.spring6.bean;
public class UserFactoryBean implements FactoryBean<User> {
    @Override
    public User getObject() throws Exception {
        return new User();
    }

    @Override
    public Class<?> getObjectType() {
        return User.class;
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
步骤二：配置bean

<bean id="user" class="com.atguigu.spring6.bean.UserFactoryBean"></bean>
1
步骤三：演示

@Test
public void testUserFactoryBean(){
    //获取IOC容器
    ApplicationContext ac = new ClassPathXmlApplicationContext("spring-factorybean.xml");
    User user = (User) ac.getBean("user");
    System.out.println(user);
}
1
2
3
4
5
6
7
说明：

​ 此时获取到的容器对象，并不是UserFactoryBean，而是User

5.2.12引入xml自动装配
步骤一：环境准备

1.创建UserController类

package com.atguigu.spring6.autowire.controller
public class UserController {

    private UserService userService;

    public void setUserService(UserService userService) {
        this.userService = userService;
    }

    public void saveUser(){
        userService.saveUser();
    }

}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
2.创建UserService接口

package com.atguigu.spring6.autowire.service
public interface UserService {

    void saveUser();

}
1
2
3
4
5
6
3.创建UserServiceImpl类实现UserService接口

package com.atguigu.spring6.autowire.service.impl
public class UserServiceImpl implements UserService {

    private UserDao userDao;

    public void setUserDao(UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void saveUser() {
        userDao.saveUser();
    }

}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
4.创建UserDao接口

package com.atguigu.spring6.autowire.dao
public interface UserDao {

    void saveUser();

}
1
2
3
4
5
6
5.创建UserDaoImpl类实现UserDao接口

package com.atguigu.spring6.autowire.dao.impl
public class UserDaoImpl implements UserDao {

    @Override
    public void saveUser() {
        System.out.println("保存成功");
    }

}
1
2
3
4
5
6
7
8
9
步骤二：配置bean

<bean id="userController" class="com.atguigu.spring6.autowire.controller.UserController" autowire="byType"></bean>

<bean id="userService" class="com.atguigu.spring6.autowire.service.impl.UserServiceImpl" autowire="byType"></bean>

<bean id="userDao" class="com.atguigu.spring6.autowire.dao.impl.UserDaoImpl"></bean>
1
2
3
4
5
说明：

当使用Bean标签的autowire属性是，通过byType的方式进行自动装配
byType：根据类型匹配IOC容器中的某个兼容类型的bean，为属性自动赋值
若在IOC中，没有任何一个兼容类型的bean能够为属性赋值，则该属性不装配，即值为默认值null
若在IOC中，有多个兼容类型的bean能够为属性赋值，则抛出异常NoUniqueBeanDefinitionException
byName：将自动装配的属性的属性名，作为bean的id在IOC容器中匹配相对应的bean进行赋值
步骤三：演示

@Test
public void testAutoWireByXML(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("autowire-xml.xml");
    UserController userController = ac.getBean(UserController.class);
    userController.saveUser();
}
1
2
3
4
5
6
说明：

​ 当使用标签中的属性时，使用Autowire属性使用byType的方式即可实现属性的自动注入

5.3基于注解管理Bean（重点）
笔记小结：

概述：

简介：Java 增加了对注解（Annotation）的支持，它是代码中的一种特殊标记，可以在编译、类加载和运行时被读取，执行相应的处理。
使用注解：
@Component：表示泛化组件
@Repository：表示数据访问层组件
@Service：表示业务层组件
@Controller：：表示控制层组件
开启组件扫描

概述：通过 <context:component-scan> 元素开启 Spring Beans的自动扫描功能。Spring 会自动从扫描指定的包（base-package 属性设置）及其子包下的所有类，如果类上使用了 @Component 注解，就将该类装配到容器中
基本用例：使用标签<context:component-scan></context:component-scan>
添加conentt约束
开启扫描方式
指定要排除的组件： <context:exclude-filter></context:exclude-filter>
仅扫描指定组件： <context:include-filter></context:include-filter
使用注解定义Bean

使用@Autowired注入：

属性注入

@Autowired
private UserDao userDao;
1
2
setter注入

private UserDao userDao;
@Autowired
public void setUserDao(UserDao userDao) {
    this.userDao = userDao;
}
1
2
3
4
5
构造方法注入

private UserDao userDao;
@Autowired
public UserServiceImpl(UserDao userDao) {
	this.userDao = userDao;
}
1
2
3
4
5
形参注入

private UserDao userDao;
public UserServiceImpl(@Autowired UserDao userDao) {
    this.userDao = userDao;
}
1
2
3
4
无注解注入：当构造函数仅有一个需要注入的构造参数时，@Autowired可以省略

private UserDao userDao;
public UserServiceImpl(UserDao userDao) {
    this.userDao = userDao;
}
1
2
3
4
联合**@Qualifier注解注入：适用于一个接口多个实现类的注解区别**

@Autowired
@Qualifier("userDaoImpl") // 指定bean的名字
private UserDao userDao;
1
2
3
使用@Resource注入：

Name注入：在使用注解时，配置name属性

@Resource(name = "myUserDao")
1
未知Name注入：不配置name属性，注入属性的成员变量但需要与Bean 的名称同名

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {
    ……
@Resource
private UserDao myUserDao;
1
2
3
4
5
类型注入：不配置name属性，名称都不同时，注入属性的成员类型会根据Bean实现的接口类型进行匹配

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {
    ……
@Resource
private UserDao userDao1;
1
2
3
4
5
全注解开发：不再使用spring配置文件了，写一个配置类来代替配置文件

@Configuration
//@ComponentScan({"com.atguigu.spring6.controller", "com.atguigu.spring6.service","com.atguigu.spring6.dao"})
@ComponentScan("com.atguigu.spring6") //开启包扫描
public class Spring6Config {
}
1
2
3
4
5
说明：用全注解开发方式时，需要指定包扫描所属的范围，便于Spring框架确定扫描而注入Bean的范围

5.3.1概述
5.3.1.1简介
​ 从 Java 5 开始，Java 增加了对注解（Annotation）的支持，它是代码中的一种特殊标记，可以在编译、类加载和运行时被读取，执行相应的处理。开发人员可以通过注解在不改变原有代码和逻辑的情况下，在源代码中嵌入补充信息。

​ Spring 从 2.5 版本开始提供了对注解技术的全面支持，我们可以使用注解来实现自动装配，简化 Spring 的 XML 配置。

5.3.1.2步骤
引入依赖
开启组件扫描
使用注解定义 Bean
依赖注入
5.3.1.3使用注解
​ Spring 提供了以下多个注解，这些注解可以直接标注在 Java 类上，将它们定义成 Spring Bean

注解	说明
@Component	该注解用于描述 Spring 中的 Bean，它是一个泛化的概念，仅仅表示容器中的一个组件（Bean），并且可以作用在应用的任何层次，例如 Service 层、Dao 层等。 使用时只需将该注解标注在相应类上即可。
@Repository	该注解用于将数据访问层（Dao 层）的类标识为 Spring 中的 Bean，其功能与 @Component 相同。
@Service	该注解通常作用在业务层（Service 层），用于将业务层的类标识为 Spring 中的 Bean，其功能与 @Component 相同。
@Controller	该注解通常作用在控制层（如SpringMVC 的 Controller），用于将控制层的类标识为 Spring 中的 Bean，其功能与 @Component 相同。
5.3.2开启组件扫描
5.3.2.1概述
​ Spring 默认不使用注解装配 Bean，因此我们需要在 Spring 的 XML 配置中，通过 <context:component-scan> 元素开启 Spring Beans的自动扫描功能。开启此功能后，Spring 会自动从扫描指定的包（base-package 属性设置）及其子包下的所有类，如果类上使用了 @Component 注解，就将该类装配到容器中。

5.3.2.2基本用例-实现组件扫描
步骤一：添加约束

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:context="http://www.springframework.org/schema/context"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
    http://www.springframework.org/schema/beans/spring-beans-3.0.xsd
    http://www.springframework.org/schema/context
            http://www.springframework.org/schema/context/spring-context.xsd">
</beans>
1
2
3
4
5
6
7
8
9
说明：

​ 在 XML 配置的一级标签 中添加 context 相关的约束

步骤二：开启扫描方式

<context:component-scan base-package="com.atguigu.spring6">
</context:component-scan>
1
2
说明：

​ 在Beans.xml文件中，设置开启扫描方式即可

5.3.2.3指定要排除的组件
<context:component-scan base-package="com.atguigu.spring6">
    <!-- context:exclude-filter标签：指定排除规则 -->
    <!-- 
 		type：设置排除或包含的依据
		type="annotation"，根据注解排除，expression中设置要排除的注解的全类名
		type="assignable"，根据类型排除，expression中设置要排除的类型的全类名
	-->
    <context:exclude-filter type="annotation" expression="org.springframework.stereotype.Controller"/>
        <!--<context:exclude-filter type="assignable" expression="com.atguigu.spring6.controller.UserController"/>-->
</context:component-scan>
1
2
3
4
5
6
7
8
9
10
说明：

<context:exclude-filter></context:exclude-filter>标签，指定排除规则
type属性：设置排除或包含的依据
属性值：annotation，根据注解排除
属性值：assignable，根据类型排除
expression属性：设置要排除的注解或类型的全类名
5.3.2.4仅扫描指定组件
<context:component-scan base-package="com.atguigu" use-default-filters="false">
    <!-- context:include-filter标签：指定在原有扫描规则的基础上追加的规则 -->
    <!-- use-default-filters属性：取值false表示关闭默认扫描规则 -->
    <!-- 此时必须设置use-default-filters="false"，因为默认规则即扫描指定包下所有类 -->
    <context:include-filter type="annotation" expression="org.springframework.stereotype.Controller"/>
    <!--<context:include-filter type="assignable" expression="com.atguigu.spring6.controller.UserController"/>-->
</context:component-scan>
1
2
3
4
5
6
7
说明：

use-default-filters="false"，表示关闭默认扫描规则
<context:include-filter></context:include-filter>，表示指定的过滤条件来确定哪些类应该被包含在组件扫描中
5.3.2使用注解定义Bean
5.3.3使用@Autowired注入
5.3.3.1概述


说明：

@Autowired注解可以标注在：构造方法上、方法上、形参上、属性上、注解上
@Autowired注解的required属性，
属性值为True：表示注入的时候要求被注入的Bean必须是存在的，如果不存在则报错
属性值为False：：表示注入的时候要求被注入的Bean不一定是存在的，如果存在的话就注入，不存在的话，也不报错
细节：

单独使用@Autowired注解时，默认是根据类型装配，默认是"byType"，例如基于XML管理Bean
<bean id="userService" class="com.atguigu.spring6.autowire.service.impl.UserServiceImpl" autowire="byType"></bean>
1
5.3.3.2属性注入
步骤一：搭建环境

1.创建UserDao接口

package com.atguigu.spring6.dao;

public interface UserDao {

    public void print();
}
1
2
3
4
5
6
2.创建UserDaoImpl实现

package com.atguigu.spring6.dao.impl;

import com.atguigu.spring6.dao.UserDao;
import org.springframework.stereotype.Repository;

@Repository
public class UserDaoImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
3.创建UserService接口

package com.atguigu.spring6.service;

public interface UserService {

    public void out();
}
1
2
3
4
5
6
4.创建UserServiceImpl实现类

package com.atguigu.spring6.service.impl;

import com.atguigu.spring6.dao.UserDao;
import com.atguigu.spring6.service.UserService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;

@Service
public class UserServiceImpl implements UserService {

    @Autowired
    private UserDao userDao;

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
5.创建UserController类

package com.atguigu.spring6.controller;

import com.atguigu.spring6.service.UserService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Controller;

@Controller
public class UserController {

    @Autowired
    private UserService userService;

    public void out() {
        userService.out();
        System.out.println("Controller层执行结束。");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

当使用@Autowired注解注入时，可不提供构造方法喝Setter方法，也可以注入成功
结果：
5.3.3.3set注入
步骤一：搭建环境

1.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    private UserDao userDao;

    @Autowired
    public void setUserDao(UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
2.修改UserController类

@Controller
public class UserController {

    private UserService userService;

    @Autowired
    public void setUserService(UserService userService) {
        this.userService = userService;
    }

    public void out() {
        userService.out();
        System.out.println("Controller层执行结束。");
    }

}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

​ 通过在需要注入的setter方法上进行添加@Autowired注解

5.3.3.4构造方法注入
步骤一：搭建环境

1.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    private UserDao userDao;

    @Autowired
    public UserServiceImpl(UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
2.修改UserController类

@Controller
public class UserController {

    private UserService userService;

    @Autowired
    public UserController(UserService userService) {
        this.userService = userService;
    }

    public void out() {
        userService.out();
        System.out.println("Controller层执行结束。");
    }

}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

​ 通过在需要注入的构造器方法上进行添加@Autowired注解

5.3.3.5形参注入
步骤一：搭建环境

1.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    private UserDao userDao;

    public UserServiceImpl(@Autowired UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
2.修改UserController类

@Controller
public class UserController {

    private UserService userService;

    public UserController(@Autowired UserService userService) {
        this.userService = userService;
    }

    public void out() {
        userService.out();
        System.out.println("Controller层执行结束。");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
14
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

​ 通过在需要注入的形参上进行添加@Autowired注解

5.3.3.6无注解注入
步骤一：搭建环境

1.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

 
    private UserDao userDao;

    public UserServiceImpl(UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
步骤二：演示

@Test
public void testAnnotation(){
    ApplicationContext context = new ClassPathXmlApplicationContext("Beans.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
}
1
2
3
4
5
6
说明：

​ 当有参数的构造方法只有一个时，@Autowired注解可以省略

5.3.3.7联合@Qualifier注解注入
步骤一：搭建环境

1.添加UserDaoRedisImpl类

@Repository
public class UserDaoRedisImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Redis Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
说明：

此时，添加实现UserDao接口类，已经造成一个接口对应两个实现类
此时，程序错误，信息中说：不能装配，UserDao这个Bean的数量等于2
步骤二：修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    @Autowired
    @Qualifier("userDaoImpl") // 指定bean的名字
    private UserDao userDao;

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
说明：

​ 当需要注入的接口有多个实现类时，可以联合使用@Qualifier(“userDaoImpl”) 注解，并指定实现类的名字，即可完成属性注入

5.3.4使用@Resource注入
5.3.4.1概述
​ @Resource注解是通过名称匹配的方式来实现注入的，默认按照名称进行匹配，如果找不到匹配的名称，则会尝试按照类型匹配。

​ @Resource注解是JDK扩展包中的，也就是说属于JDK的一部分。所以该注解是标准注解，更加具有通用性。(JSR-250标准中制定的注解类型。JSR是Java规范提案。)



说明：

如果是JDK8的话不需要额外引入依赖。高于JDK11或低于JDK8需要引入以下依赖
<dependency>
    <groupId>jakarta.annotation</groupId>
    <artifactId>jakarta.annotation-api</artifactId>
    <version>2.1.1</version>
</dependency>
1
2
3
4
5
5.3.4.2Name注入
步骤一：搭建环境

1.修改UserDaoImpl类

package com.atguigu.spring6.dao.impl;

import com.atguigu.spring6.dao.UserDao;
import org.springframework.stereotype.Repository;

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
说明：

​ 当使用注解时，在小括号内写上属性名称表示为此Bean定义别名

2.修改UserServiceImpl类

package com.atguigu.spring6.service.impl;

import com.atguigu.spring6.dao.UserDao;
import com.atguigu.spring6.service.UserService;
import jakarta.annotation.Resource;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.beans.factory.annotation.Qualifier;
import org.springframework.stereotype.Service;

@Service
public class UserServiceImpl implements UserService {

    @Resource(name = "myUserDao")
    private UserDao myUserDao;

    @Override
    public void out() {
        myUserDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
说明：

​ 当使用@Resource注解时，可以使用name属性指定属性注入的别名

步骤二：演示

5.3.4.3未知Name注入
步骤一：搭建环境

1.修改UserDaoImpl类

package com.atguigu.spring6.dao.impl;

import com.atguigu.spring6.dao.UserDao;
import org.springframework.stereotype.Repository;

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
13
2.修改UserServiceImpl类

package com.atguigu.spring6.service.impl;

import com.atguigu.spring6.dao.UserDao;
import com.atguigu.spring6.service.UserService;
import jakarta.annotation.Resource;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.beans.factory.annotation.Qualifier;
import org.springframework.stereotype.Service;

@Service
public class UserServiceImpl implements UserService {

    @Resource
    private UserDao myUserDao;

    @Override
    public void out() {
        myUserDao.print();
        System.out.println("Service层执行结束");
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
说明：

​ 当使用@Resource注解时，在name属性未知的情况下，将属性注入的成员属性变量名定义为与Bean同名，即可完成注入

步骤二：演示

5.3.4.4类型注入
步骤一：搭建环境

1.原UserDaoImpl类

@Repository("myUserDao")
public class UserDaoImpl implements UserDao {

    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}
1
2
3
4
5
6
7
8
2.修改UserServiceImpl类

@Service
public class UserServiceImpl implements UserService {

    @Resource
    private UserDao userDao1;

    @Override
    public void out() {
        userDao1.print();
        System.out.println("Service层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
说明：

​ 当使用@Resource注解时，现在userDao1属性名不存在，但仍然可以注入成功。因为，UserDao他们的类型名相同

5.3.5全注解开发
5.3.5.1概述
​ 全注解开发就是不再使用spring配置文件了，写一个配置类来代替配置文件

5.3.5.2基本用例-全注解开发实现
步骤一：创建配置类

@Configuration
//@ComponentScan({"com.atguigu.spring6.controller", "com.atguigu.spring6.service","com.atguigu.spring6.dao"})
@ComponentScan("com.atguigu.spring6")
public class Spring6Config {
}
1
2
3
4
5
说明：

​ 使用@ComponentScan注解，进行组件扫描，从而替代了原有在xml文件中的配置

步骤二：演示

@Test
public void testAllAnnotation(){
    ApplicationContext context = new AnnotationConfigApplicationContext(Spring6Config.class);
    UserController userController = context.getBean("userController", UserController.class);
    userController.out();
    logger.info("执行成功");
}
1
2
3
4
5
6
7
说明：

​ 需要使用AnnotationConfigApplicationContext类来获取Spring6Config的字节码文件

5.4原理
笔记小结：

扫描指定的包，获取所有需要管理的类的类名。
实例化需要管理的类，通过反射机制调用构造器来实现。
通过反射机制调用setter方法或者构造器注入属性值。
维护对象之间的依赖关系，实现对象之间的解耦。
将实例化好的对象注册到IOC容器中，便于后续使用。
说明：



步骤一：环境搭建

1.创建注解

创建Bean注解

// 此注解用于定义容器对象，类似于@Componet、@Service、@Controller注解等作用
@Target(ElementType.TYPE)
@Retention(RetentionPolicy.RUNTIME)
public @interface Bean {
}
1
2
3
4
5
创建依赖注入注解

// 此注解用于完成成员属性的依赖注入，类似于@Autoware、@Resource注解等作用
@Target({ElementType.FIELD})
@Retention(RetentionPolicy.RUNTIME)
public @interface Di {
}
1
2
3
4
5
2.创建IOC核心逻辑

定义bean容器接口

package com.atguigu.spring.core;

public interface ApplicationContext {

    Object getBean(Class clazz);
}
1
2
3
4
5
6
编写注解bean容器接口实现

public class AnnotationApplicationContext implements ApplicationContext {

    // 存储Bean的容器
    private HashMap<Class, Object> beanFactory = new HashMap<>();

    // 根据字节码文件获取Bean容器中的对象
    @Override
    public Object getBean(Class clazz) {
        return beanFactory.get(clazz);
    }

    /**
     * 根据包扫描加载bean
     * @param basePackage
     */
    public AnnotationApplicationContext(String basePackage) {
        try {
            String packageDirName = basePackage.replaceAll("\\.", "\\\\");
            Enumeration<URL> dirs =Thread.currentThread().getContextClassLoader().getResources(packageDirName);
            while (dirs.hasMoreElements()) {
                URL url = dirs.nextElement();
                String filePath = URLDecoder.decode(url.getFile(),"utf-8");
                rootPath = filePath.substring(0, filePath.length()-packageDirName.length());
                // 扫描包下的Bean
                loadBean(new File(filePath));
            }

        } catch (Exception e) {
            throw new RuntimeException(e);
        }
        //依赖注入
        loadDi();
    }


    private  void loadBean(File fileParent) {
        if (fileParent.isDirectory()) {
            File[] childrenFiles = fileParent.listFiles();
            if(childrenFiles == null || childrenFiles.length == 0){
                return;
            }
            for (File child : childrenFiles) {
                if (child.isDirectory()) {
                    //如果是个文件夹就继续调用该方法,使用了递归
                    loadBean(child);
                } else {
                    //通过文件路径转变成全类名,第一步把绝对路径部分去掉
                    String pathWithClass = child.getAbsolutePath().substring(rootPath.length() - 1);
                    //选中class文件
                    if (pathWithClass.contains(".class")) {
                        //    com.xinzhi.dao.UserDao
                        //去掉.class后缀，并且把 \ 替换成 .
                        String fullName = pathWithClass.replaceAll("\\\\", ".").replace(".class", "");
                        try {
                            Class<?> aClass = Class.forName(fullName);
                            //把非接口的类实例化放在map中
                            if(!aClass.isInterface()){
                                Bean annotation = aClass.getAnnotation(Bean.class);
                                if(annotation != null){
                                    Object instance = aClass.newInstance();
                                    //判断一下有没有接口
                                    if(aClass.getInterfaces().length > 0) {
                                        //如果有接口把接口的class当成key，实例对象当成value
                                        System.out.println("正在加载【"+ aClass.getInterfaces()[0] +"】,实例对象是：" + instance.getClass().getName());
                                        beanFactory.put(aClass.getInterfaces()[0], instance);
                                    }else{
                                        //如果有接口把自己的class当成key，实例对象当成value
                                        System.out.println("正在加载【"+ aClass.getName() +"】,实例对象是：" + instance.getClass().getName());
                                        beanFactory.put(aClass, instance);
                                    }
                                }
                            }
                        } catch (ClassNotFoundException | IllegalAccessException | InstantiationException e) {
                            e.printStackTrace();
                        }
                    }
                }
            }
        }
    }

    private void loadDi() {
        for(Map.Entry<Class,Object> entry : beanFactory.entrySet()){
            //就是咱们放在容器的对象
            Object obj = entry.getValue();
            Class<?> aClass = obj.getClass();
            Field[] declaredFields = aClass.getDeclaredFields();
            for (Field field : declaredFields){
                Di annotation = field.getAnnotation(Di.class);
                if( annotation != null ){
                    field.setAccessible(true);
                    try {
                        System.out.println("正在给【"+obj.getClass().getName()+"】属性【" + field.getName() + "】注入值【"+ beanFactory.get(field.getType()).getClass().getName() +"】");
                        field.set(obj,beanFactory.get(field.getType()));
                    } catch (IllegalAccessException e) {
                        e.printStackTrace();
                    }
                }
            }
        }
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
64
65
66
67
68
69
70
71
72
73
74
75
76
77
78
79
80
81
82
83
84
85
86
87
88
89
90
91
92
93
94
95
96
97
98
99
100
101
102
说明：

可将此代码复制到IDEA中查看逻辑更详细

3.创建Dao层

创建UserDao接口
public interface UserDao {

    public void print();
}
1
2
3
4
创建UserDaoImpl实现
@Bean
public class UserDaoImpl implements UserDao {
    @Override
    public void print() {
        System.out.println("Dao层执行结束");
    }
}

1
2
3
4
5
6
7
8
说明：

当此类实现了UserDao这个接口时，会将UserDao这个接口作为容器的Key值，来获取UserDaoImpl这个实现类

这也就是为什么一个接口不能对应多个实现类，因为HashMap的Key值不能重复

// 参数解释，参数1：实现类上实现的第一个接口或者实现类的字节码文件；参数2：实现类实例
beanFactory.put(aClass.getInterfaces()[0], instance);
// 此处，参数1：接口为UserDao；参数2，实现类实例为UserDaoImpl
1
2
3
4.创建Service层

创建UserService接口

public interface UserService {
    public void out();
}
1
2
3
创建UserServiceImpl实现类

@Bean
public class UserServiceImpl implements UserService {

    @DI
    private UserDao userDao;

    @Override
    public void out() {
        userDao.print();
        System.out.println("Service层执行结束");
    }
}
1
2
3
4
5
6
7
8
9
10
11
12
说明：

当此类里包含了依赖注入这个接口时，会将UserServiceImpl这个实现类实例作为依赖注入的Key值，并且根据依赖注入的变量名确定所需要依赖注入的实现类实例

// 参数解释，参数1：设置字段值的对象实例；参数2：需要设置的字段值
field.set(obj, beanFactory.get(field.getType()));
//此处，参数1：实现类实例UserServiceImpl；参数2：实现类实例UserDaoImpl
1
2
3
步骤二：演示

ApplicationContext applicationContext = new AnnotationApplicationContext("org.example");
UserService bean = (UserService) applicationContext.getBean(UserService.class);
bean.out();
1
2
3
6.面向切面：AOP (重点)
笔记小结：

概述：

含义：AOP（Aspect Oriented Programming）是一种设计思想，是软件设计领域中的面向切面编程
作用：
简化开发：分离关注点，让各个一些通用的行为（日志、事务、安全）实现重用
降低代码耦合度：将不同的关注点分离开来，提高代码可复用性和可维护性
横切关注点：横切关注点是指跨越应用程序多个模块的功能或行为。例如日志记录、安全性等与业务逻辑无关的功能
通知：通知（增强）是指在 AOP 中定义的一种特殊类型的方法，它包含要在连接点（join point）执行的一些行为。例如在某个方法执行前、中、后需要加上一些输出日志等这样的逻辑
切面：切面指的是横切关注点和通知的组合，简单的说，切面就是封装通知方法的类
目标：目标（Target）是指被通知的对象或者被切面所影响的对象。例如类、接口、方法这类元素
代理：代理是指控制对目标对象的访问，并在访问过程中插入额外的逻辑。简单的说，代理就是向目标对象应用通知之后创建的代理对象
连接点：连接点（Join Point）表示在程序执行过程中能够插入一个切面的点。简单的说，连接点就是代理对象中的执行逻辑
切入点：切入点（Pointcut）表示在目标对象中定义的一个或多个特定的方法或方法执行位置，它表示在何处应该插入切面的逻辑
代理模式：代理模式是一种结构型设计模式，它使得代理对象可以代表另一个对象进行访问

静态代理：静态代理是用代码的方式实现方法之前或之后执行一些附加操作
动态代理：它允许在运行时动态地创建代理对象，并将切面逻辑织入到目标对象的方法中
分类：基于接口的代理（有接口情况）、基于类的代理（无接口情况）
切入点表达式：用于匹配目标对象中的方法，并提供切入点的精确定义



基于注解的AOP：各个小结模块，请查看此小结（重点）

基于XML的AOP：通过XML 的方式来实现切面的定义和应用（了解）

6.1概述
6.1.1定义
​ AOP（Aspect Oriented Programming）是一种设计思想，是软件设计领域中的面向切面编程，它是面向对象编程的一种补充和完善，它以通过预编译方式和运行期动态代理方式实现，在不修改源代码的情况下，给程序动态统一添加额外功能的一种技术。利用AOP可以对业务逻辑的各个部分进行隔离，从而使得业务逻辑各部分之间的耦合度降低，提高程序的可重用性，同时提高了开发的效率

6.1.2作用
代码重用和模块化：AOP可以将一些通用的行为（例如日志记录、安全控制、事务管理等）抽象出来，形成可重用的模块，避免在每个业务逻辑中都重复编写这些代码。

分离关注点：AOP将不同的关注点分离开来，使得各个模块间职责更加清晰明确，代码的可读性和可维护性也更强。

简化开发：AOP可以帮助开发人员将关注点从业务逻辑中分离出来，使得开发更加简单明了。

提高系统的可扩展性：在系统需求变化时，只需要修改AOP模块而不是修改业务逻辑，这可以使得系统更加易于扩展和维护。

降低代码耦合度：AOP的作用是将不同的关注点分离开来，这可以避免代码之间的紧耦合，提高代码的可复用性和可维护性。

6.1.3横切关注点
​ 在 AOP 中，横切关注点指的是在应用程序中影响多个类或对象的横切性质的行为，比如日志记录、性能监控、事务处理等等。这些行为可能分散在整个应用程序中的不同类和方法中，而不是与应用程序的核心业务逻辑紧密相关。

​ 使用 AOP 技术，可以将这些横切关注点从应用程序的核心业务逻辑中分离出来，并将它们模块化为可重用的模块，从而实现更好的代码结构和更好的可维护性。



6.1.4通知（增强）
​ 通知（advice）也被称为增强（advice），是指在 AOP 中定义的一种特殊类型的方法，它包含要在连接点（join point）执行的一些行为。通知可以在目标方法执行之前、之后或异常时被执行，也可以在目标方法返回一个结果后被执行。通知的目的是在不修改目标对象的情况下，将增强（如日志、事务管理等）应用于应用程序的特定方法或切入点。通知是实现 AOP 的核心组件之一，通过将通知应用于特定的连接点（join point）来实现面向切面编程

简单来说：通知就是你想要增强的功能，比如 安全，事务，日志等

通知分类：

前置通知：在被代理的目标方法前执行
返回通知：在被代理的目标方法成功结束后执行（寿终正寝）
异常通知：在被代理的目标方法异常结束后执行（死于非命）
后置通知：在被代理的目标方法最终结束后执行（盖棺定论）
环绕通知：使用try…catch…finally结构围绕整个被代理的目标方法，包括上面四种通知对应的所有位置


6.1.5切面
​ 在AOP中，切面指的是横切关注点和通知的组合，它是一个模块化的横向分割，可以理解为一个横向的切片。切面是对横切关注点和通知的封装，它包含了一组切点和通知，用于描述在何处、何时、以及如何执行横切逻辑。切面可以在不修改原代码的情况下，对原有的代码进行功能的增强或改变。通常，切面是以一个类的形式存在的，它包含了一个或多个通知和一个或多个切点。

简单来说：切面就是封装通知方法的类



6.1.6目标
​ 在AOP（Aspect-Oriented Programming）中，目标（Target）是指被通知的对象或者被切面所影响的对象。它是应用程序中的一个具体元素，可以是类、接口、方法或者字段等。简单点说，目标就是被代理的目标对象

6.1.7代理
​ 在AOP（Aspect-Oriented Programming）中，代理（Proxy）是一种设计模式，用于控制对目标对象的访问，并在访问过程中插入额外的逻辑。简单点说，代理就是向目标对象应用通知之后创建的代理对象

6.1.8连接点
​ 在 AOP 中，连接点（Join Point）表示在程序执行过程中能够插入一个切面的点，例如方法调用、异常处理、字段访问等。连接点定义了在程序中的哪个位置可以应用切面。切面可以在连接点前后增加额外的处理逻辑，从而影响程序的行为。通俗地讲，连接点就是在程序执行中可以被拦截的地方



说明：

​ 把方法排成一排，每一个横切位置看成x轴方向，把方法从上到下执行的顺序看成y轴，x轴和y轴的交叉点就是连接点。通俗说，就是spring允许你使用通知的地方

6.1.9切入点
​ 在 AOP 中，切入点（Join Point）是指程序执行过程中明确的点，通常是方法调用的时候，也可以是异常处理程序的处理过程。切入点定义了哪些方法是需要被拦截或增强的，是 AOP 中最重要的概念之一。切入点通常以方法的形式被定义，比如某个类的所有方法、某个包下的所有方法等等。在 AOP 中，通常会使用表达式语言定义切入点，如使用 Spring AOP 中的 @Pointcut 注解定义。

6.2代理模式
6.2.1概述
​ 代理模式是一种结构型设计模式，它使得代理对象可以代表另一个对象进行访问。它是二十三种设计模式中的一种，属于结构型模式。它的作用就是通过提供一个代理类，让我们在调用目标方法的时候，不再是直接对目标方法进行调用，而是通过代理类间接调用。让不属于目标方法核心逻辑的代码从目标方法中剥离出来——解耦。调用目标方法时先调用代理对象的方法，减少对目标方法的调用和打扰，同时让附加功能能够集中在一起也有利于统一维护。



​

代理：将非核心逻辑剥离出来以后，封装这些非核心逻辑的类、对象、方法

6.2.2静态代理
​ 在静态代理中，代理类是在编译时期创建的，代理类和委托类实现相同的接口或继承相同的类，并在代理类中实现委托类中的方法，在调用委托类的方法之前或之后执行一些附加操作

public class CalculatorStaticProxy implements Calculator {
    
    // 将被代理的目标对象声明为成员变量
    private Calculator target;
    
    public CalculatorStaticProxy(Calculator target) {
        this.target = target;
    }
    
    @Override
    public int add(int i, int j) {
    
        // 附加功能由代理类中的代理方法来实现
        System.out.println("[日志] add 方法开始了，参数是：" + i + "," + j);
    
        // 通过目标对象来实现核心业务逻辑
        int addResult = target.add(i, j);
    
        System.out.println("[日志] add 方法结束了，结果是：" + addResult);
    
        return addResult;
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
说明：

​ 静态代理确实实现了解耦，但是由于代码都写死了，完全不具备任何的灵活性

6.2.3动态代理
6.2.3.1概述
6.2.3.1.1定义
​ 在动态代理中，代理类是在运行时期动态创建的。它不需要事先知道委托类的接口或实现类，而是在运行时期通过 Java 反射机制动态生成代理类



6.2.3.1.2分类
动态代理分类

基于接口的代理（有接口情况）
基于类的代理（无接口情况）


说明：

​ AspectJ：是AOP思想的一种实现。本质上是静态代理，将代理逻辑“织入”被代理的目标类编译得到的字节码文件，所以最终效果是动态的。weaver就是织入器。Spring只是借用了AspectJ中的注解。



说明：

当动态代理是基于接口的代理情况时，此种方式是JDK原生的实现方式。需要被代理的目标类必须**实现接口。因为这个技术要求代理对象和目标对象实现同样的接口**
当动态代理是基于类的代理情况时，通过**继承被代理的目标类**实现代理。因此不需要目标类实现接口
补充：

JDK动态代理动态生成的代理类会在com.sun.proxy包下，类名为$proxy1，和目标类实现相同的接口
cglib动态代理动态生成的代理类会和目标在在相同的包下，会继承目标类
6.2.3.2基本用例-实现动态代理
步骤一：创建ProxyFactory类

public class ProxyFactory {

    private Object target;

    public ProxyFactory(Object target) {
        this.target = target;
    }

    public Object getProxy(){
        /**
         * newProxyInstance()：创建一个代理实例
         * 其中有三个参数：
         * 1、classLoader：加载动态生成的代理类的类加载器
         * 2、interfaces：目标对象实现的所有接口的class对象所组成的数组
         * 3、invocationHandler：设置代理对象实现目标对象方法的过程，即代理类中如何重写接口中的抽象方法
         */
        ClassLoader classLoader = target.getClass().getClassLoader();
        Class<?>[] interfaces = target.getClass().getInterfaces();
        InvocationHandler invocationHandler = new InvocationHandler() {
            @Override
            public Object invoke(Object proxy, Method method, Object[] args) throws Throwable {
                /**
                 * proxy：代理对象
                 * method：代理对象需要实现的方法，即其中需要重写的方法
                 * args：method所对应方法的参数
                 */
                Object result = null;
                try {
                    System.out.println("[动态代理][日志] "+method.getName()+"，参数："+ Arrays.toString(args));
                    result = method.invoke(target, args);
                    System.out.println("[动态代理][日志] "+method.getName()+"，结果："+ result);
                } catch (Exception e) {
                    e.printStackTrace();
                    System.out.println("[动态代理][日志] "+method.getName()+"，异常："+e.getMessage());
                } finally {
                    System.out.println("[动态代理][日志] "+method.getName()+"，方法执行完毕");
                }
                return result;
            }
        };

        return Proxy.newProxyInstance(classLoader, interfaces, invocationHandler);
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
说明：

动态代理需要使用Proxy.newProxyInstance()方法
需要设置代理对象实现目标对象的方法过程
步骤二：演示

@Test
public void testDynamicProxy(){
    ProxyFactory factory = new ProxyFactory(new CalculatorLogImpl());
    Calculator proxy = (Calculator) factory.getProxy();
    proxy.div(1,0);
    //proxy.div(1,1);
}
1
2
3
4
5
6
7
6.3切入点表达式
​ 在 AOP 中，切入点表达式指定了哪些方法需要被织入增强逻辑。它是一个表达式，用于匹配目标对象中的方法，并提供切入点的精确定义



说明：

​ 在切入点表达式语法中，用*号代替“权限修饰符”和“返回值”部分表示“权限修饰符”和“返回值”不限

6.4基于注解的AOP
笔记小结：

概述：在Java类、方法、参数等上添加注解的方式来实现切面的定义和应用

基本用例：

步骤一：导入依赖

步骤二：创建切面类（需要选择通知方式）

步骤三：添加xml配置文件

通知方式：

前置通知：@Before
异常通知：@AfterThrowing
返回通知：@AfterReturning
后置通知：@After
环绕通知：@Around
获取通知信息

获取连接点：在方法中使用JoinPoint即可获取连接点信息

public void beforeMethod(JoinPoint joinPoint)
1
获取目标对象的返回值：在目标对象的返回通知上添加returning属性

@AfterReturning(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", returning = "result")
public void afterReturningMethod(JoinPoint joinPoint, Object result)
1
2
获取目标对象的异常：在目标对象的异常通知上添加throwing属性

@AfterThrowing(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", throwing = "ex")
public void afterThrowingMethod(JoinPoint joinPoint, Throwable ex)
1
2
重用切入点表达式

声明：在空参、空方法体、空返回值的方法上使用**@Pointcut**注解

@Pointcut("execution(* com.atguigu.aop.annotation.*.*(..))")
public void pointCut(){}
1
2
同切面使用：在同一切面中直接引用即可

@Before("pointCut()")
1
不同切面使用：在不同切面中

@Before("com.atguigu.aop.CommonPointCut.pointCut()")
1
6.4.1概述
​ 基于注解的AOP是一种AOP的实现方式，它通过在Java类、方法、参数等上添加注解的方式来实现切面的定义和应用，相比于传统的XML配置方式更加便捷和灵活

6.4.2基本用例-注解实现AOP
步骤一：导入依赖

 <!--spring aop依赖-->
    <dependency>
        <groupId>org.springframework</groupId>
        <artifactId>spring-aop</artifactId>
        <version>6.0.2</version>
    </dependency>
    <!--spring aspects依赖-->
    <dependency>
        <groupId>org.springframework</groupId>
        <artifactId>spring-aspects</artifactId>
        <version>6.0.2</version>
    </dependency>
1
2
3
4
5
6
7
8
9
10
11
12
步骤二：创建接口以及实现类

1.接口

public interface Calculator {
    int add(int i, int j); 
}
1
2
3
2.实现类

@Component
public class CalculatorImpl implements Calculator {

    @Override
    public int add(int i, int j) {
        int result = i + j;
        System.out.println("方法内部 result = " + result);
        return result;
    }
}
1
2
3
4
5
6
7
8
9
10
说明：

​ 此实现类，也需要添加@Component注解，便于Spring容器进行管理

步骤三：创建切面类

@Aspect
@Component
public class LogAspect {
    // 前置通知
    // 异常通知
    // 返回通知
    // 后置通知
    // 环绕通知
    ……
}
1
2
3
4
5
6
7
8
9
10
注意：

​ 此处需要配置切面类的通知方式！

说明：

@Aspect表示这个类是一个切面类
@Component注解保证这个切面类能够放入IOC容器
步骤四：配置Spring配置文件

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:context="http://www.springframework.org/schema/context"
       xmlns:aop="http://www.springframework.org/schema/aop"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
       http://www.springframework.org/schema/beans/spring-beans.xsd
       http://www.springframework.org/schema/context
       http://www.springframework.org/schema/context/spring-context.xsd
       http://www.springframework.org/schema/aop
       http://www.springframework.org/schema/aop/spring-aop.xsd">
    <!--
        基于注解的AOP的实现：
        1、将目标对象和切面交给IOC容器管理（注解+扫描）
        2、开启AspectJ的自动代理，为目标对象自动生成代理
        3、将切面类通过注解@Aspect标识
    -->
    <context:component-scan base-package="com.atguigu.aop.annotation"></context:component-scan>

    <aop:aspectj-autoproxy />
</beans>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
补充：

​ 当学习了SpringBoot后，通过SpringBoot来实现AOP，可省略此文件。因为SpringBoot以实现包扫描和切面标识

步骤五：演示

@Test
public void testAdd(){
    ApplicationContext ac = new ClassPathXmlApplicationContext("beans.xml");
    Calculator calculator = ac.getBean( Calculator.class);
    int add = calculator.add(1, 1);
}
1
2
3
4
5
6
说明：

​

6.4.3通知方式
6.4.3.1前置通知
使用@Before注解标识，在被代理的目标方法前执行

@Before("execution(public int com.atguigu.aop.annotation.CalculatorImpl.*(..))")
public void beforeMethod(JoinPoint joinPoint){
    // getSignature（）获取连接点签名，getName（）获取连接点名称
    String methodName = joinPoint.getSignature().getName();
    String args = Arrays.toString(joinPoint.getArgs());
    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);
}
1
2
3
4
5
6
7
说明：

@Before注解内为切入点表达式
JoinPoint 是指程序执行过程中明确的点，比如方法的调用或异常的处理。JoinPoint 提供了一个可供切面通知获取方法的关键信息的方式
6.4.3.2异常通知
使用@AfterThrowing注解标识，在被代理的目标方法异常结束后执行

@AfterThrowing(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", throwing = "ex")
public void afterThrowingMethod(JoinPoint joinPoint, Throwable ex){
    String methodName = joinPoint.getSignature().getName();
    System.out.println("Logger-->异常通知，方法名："+methodName+"，异常："+ex);
}

1
2
3
4
5
6
说明：

​ @AfterThrowing注解内为切入点表达式

6.4.3.3返回通知
使用@AfterReturning注解标识，在被代理的目标方法成功结束后执行

@AfterReturning(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", returning = "result")
public void afterReturningMethod(JoinPoint joinPoint, Object result){
    String methodName = joinPoint.getSignature().getName();
    System.out.println("Logger-->返回通知，方法名："+methodName+"，结果："+result);
}

1
2
3
4
5
6
说明：

​ @AfterReturning注解内为切入点表达式

6.4.3.4后置通知
使用@After注解标识，在被代理的目标方法最终结束后执行

  @After("execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))")
    public void afterMethod(JoinPoint joinPoint){
        String methodName = joinPoint.getSignature().getName();
        System.out.println("Logger-->后置通知，方法名："+methodName);
    }

1
2
3
4
5
6
说明：

​ @After注解内为切入点表达式

6.4.3.5环绕通知
使用@Around注解标识，使用try…catch…finally结构围绕整个被代理的目标方法，包括上面四种通知对应的所有位置

@Around("execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))")
public Object aroundMethod(ProceedingJoinPoint joinPoint){
    String methodName = joinPoint.getSignature().getName();
    String args = Arrays.toString(joinPoint.getArgs());
    Object result = null;
    try {
        System.out.println("环绕通知-->目标对象方法执行之前");
        //目标对象（连接点）方法的执行
        result = joinPoint.proceed();
        System.out.println("环绕通知-->目标对象方法返回值之后");
    } catch (Throwable throwable) {
        throwable.printStackTrace();
        System.out.println("环绕通知-->目标对象方法出现异常时");
    } finally {
        System.out.println("环绕通知-->目标对象方法执行完毕");
    }
    return result;
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
说明：

@Around注解内为切入点表达式
ProceedingJoinPoint 继承自 JoinPoint 接口，是用于环绕通知的特殊类型的 JoinPoint，它可以用于在通知中控制目标方法的执行。在环绕通知中，ProceedingJoinPoint 提供了一个 proceed() 方法，该方法会执行目标方法，并返回其结果。
6.4.4获取通知信息
6.4.4.1获取连接点信息
在任何通知方式中，获取连接点信息可以在通知方法的参数位置设置JoinPoint类型的形参

@Before("execution(public int com.atguigu.aop.annotation.CalculatorImpl.*(..))")
public void beforeMethod(JoinPoint joinPoint){
    //获取连接点的签名信息
    String methodName = joinPoint.getSignature().getName();
    //获取目标方法到的实参信息
    String args = Arrays.toString(joinPoint.getArgs());
    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);
}
1
2
3
4
5
6
7
8
6.4.4.2获取目标方法的返回值
@AfterReturning中的属性returning，用来将通知方法的某个形参，接收目标方法的返回值

@AfterReturning(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", returning = "result")
public void afterReturningMethod(JoinPoint joinPoint, Object result){
    String methodName = joinPoint.getSignature().getName();
    System.out.println("Logger-->返回通知，方法名："+methodName+"，结果："+result);
}
1
2
3
4
5
6.4.4.3获取目标方法的异常
@AfterThrowing中的属性throwing，用来将通知方法的某个形参，接收目标方法的异常

@AfterThrowing(value = "execution(* com.atguigu.aop.annotation.CalculatorImpl.*(..))", throwing = "ex")
public void afterThrowingMethod(JoinPoint joinPoint, Throwable ex){
    String methodName = joinPoint.getSignature().getName();
    System.out.println("Logger-->异常通知，方法名："+methodName+"，异常："+ex);
}
1
2
3
4
5
6.4.5重用切入点表达式
说明：

​ 切入点表达式可参考本节面向切面：AOP中的概述部分

简化切入点的书写

6.4.5.1声明
@Pointcut("execution(* com.atguigu.aop.annotation.*.*(..))")
public void pointCut(){}
1
2
6.4.5.2同切面使用
@Before("pointCut()")
public void beforeMethod(JoinPoint joinPoint){
    String methodName = joinPoint.getSignature().getName();
    String args = Arrays.toString(joinPoint.getArgs());
    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);
}
1
2
3
4
5
6
6.4.5.3不同切面使用
@Before("com.atguigu.aop.CommonPointCut.pointCut()")
public void beforeMethod(JoinPoint joinPoint){
    String methodName = joinPoint.getSignature().getName();
    String args = Arrays.toString(joinPoint.getArgs());
    System.out.println("Logger-->前置通知，方法名："+methodName+"，参数："+args);
}
1
2
3
4
5
6
6.5基于XML的AOP（了解）
<context:component-scan base-package="com.atguigu.aop.xml"></context:component-scan>

<aop:config>
    <!--配置切面类-->
    <aop:aspect ref="loggerAspect">
        <aop:pointcut id="pointCut" 
                   expression="execution(* com.atguigu.aop.xml.CalculatorImpl.*(..))"/>
        <aop:before method="beforeMethod" pointcut-ref="pointCut"></aop:before>
        <aop:after method="afterMethod" pointcut-ref="pointCut"></aop:after>
        <aop:after-returning method="afterReturningMethod" returning="result" pointcut-ref="pointCut"></aop:after-returning>
        <aop:after-throwing method="afterThrowingMethod" throwing="ex" pointcut-ref="pointCut"></aop:after-throwing>
        <aop:around method="aroundMethod" pointcut-ref="pointCut"></aop:around>
    </aop:aspect>
</aop:config>
1
2
3
4
5
6
7
8
9
10
11
12
13
14
知识加油站
1.自动装配和依赖注入的区别与联系
​ 依赖注入（Dependency Injection） 是一种设计模式，旨在通过将依赖关系从一个对象传递给另一个对象，来实现对象之间的解耦。在Spring中，依赖注入通过容器来管理和传递对象之间的依赖关系，而不是由对象自身来创建或管理它们的依赖。这可以通过构造函数注入、Setter方法注入或字段注入等方式来实现

​ 自动装配（Autowired） 是Spring Framework提供的一种依赖注入的方式，用于自动将合适的依赖注入到相应的位置，无需手动指定每个依赖的注入方式。通过使用@Autowired注解，Spring会自动在容器中查找匹配的依赖，并将其注入到需要的位置

总结：

自动装配是Spring框架的特性，用于自动连接应用程序中的组件。
依赖注入是自动装配的一种具体实现方式，使用**@Autowired注解来标识需要自动注入**的属性、构造函数或方法参数。
2.依赖注入的两种方式
依赖注入（Dependency Injection）有两种常见的方式：

构造函数注入（Constructor Injection）：通过构造函数来注入依赖对象。在目标类的构造函数中声明参数，并在创建目标对象时通过构造函数传入依赖对象。这种方式可以保证依赖对象在目标对象创建时就被传入，从而确保了目标对象的完整性和一致性。
Setter方法注入（Setter Injection）：通过Setter方法来注入依赖对象。在目标类中定义对应的Setter方法，并在方法中接收依赖对象作为参数，通过调用Setter方法来注入依赖对象。这种方式可以在目标对象创建后动态地设置依赖对象，灵活性较高。
————————————————

                            版权声明：本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。
                        
原文链接：https://blog.csdn.net/D_boj/article/details/132286492>)