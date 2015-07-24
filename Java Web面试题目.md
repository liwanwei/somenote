

1、jsp和servlet的区别、共同点、各自应用的范围？？

JSP是Servlet技术的扩展，本质上就是Servlet的简易方式。JSP编译后是“类servlet”。Servlet和JSP最主要的不同点在于，Servlet的应用逻辑是在Java文件中，并且完全从表示层中的HTML里分离开来。而JSP的情况是Java和HTML可以组合成一个扩展名为.jsp的文件。JSP侧重于视图，Servlet主要用于控制逻辑。在struts框架中,JSP位于MVC设计模式的视图层,而Servlet位于控制层.

 

2、cookie和session的作用、区别、应用范围，session的工作原理？？？

Cookie:主要用在保存客户端，其值在客户端与服务端之间传送，不安全，存储的数据量有限。

Session:保存在服务端，每一个session在服务端有一个sessionID作一个标识。存储的数据量大，安全性高。占用服务端的内存资源。

 

3、jstl是什么？优点有哪些？？

JSTL（JSP Standard　Tag　Library　，JSP标准标签库)是一个不断完善的开放源代码的JSP标签库，由四个定制标记库（core、format、xml 和 sql）和一对通用标记库验证器（ScriptFreeTLV 和 PermittedTaglibsTLV）组成。优点有：

1、 在应用程序服务器之间提供了一致的接口，最大程序地提高了WEB应用在各应用服务器之间的移植。

2、 简化了JSP和WEB应用程序的开发。

3、 以一种统一的方式减少了JSP中的scriptlet代码数量，可以达到没有任何scriptlet代码的程序。在我们公司的项目中是不允许有任何的scriptlet代码出现在JSP中。

4、 允许JSP设计工具与WEB应用程序开发的进一步集成。相信不久就会有支持JSTL的IDE开发工具出现。

 

4、j2ee的优越性主要表现在哪些方面？MVC模式

a、 J2EE基于JAVA 技术，与平台无关

b、 J2EE拥有开放标准，许多大型公司实现了对该规范支持的应用服务器。如BEA ,IBM,ORACLE等。

c、 J2EE提供相当专业的通用软件服务。

d、 J2EE提供了一个优秀的企业级应用程序框架，对快速高质量的开发系统打下了基础。

Model模型：应用程序的主体部分，用于表示业务逻辑。

View视图：应用程序中用户界面相关的部分，是用户看到并与之交互的界面。

Controller控制器：用于根据用户的输入，控制用户界面数据显示，更新Model对象状态。

MVC模式的出现不仅实现了功能模块和显示模块的分离，同时还提够了应用系统的可维护、可扩展性、可移植性、和组建的可复用性。

 

5、Struts的优点

a、实现MVC模式，结构清晰，使开发者只需关注业务逻辑的实现。

b、有丰富的tag可以用，能大大提够开发效率，缩短开发时间。

c、页面导航。通过一个配置文件，即可把握整个系统各部分之间的联系，这对于后期的维护有很大的好处

d、提供Exception处理机制

e、支持L18N

6、为什么要用struts？

　　JSP、Servlet、JavaBean技术的出现给我们构建强大的企业应用系统提供了可能。但用这些技术构建的系统非常的繁乱，所以在此之上，我们需要一个规则、一个把这些技术组织起来的规则，这就是框架，Struts便应运而生。

　　基于Struts开发的应用由3类组件构成：控制器组件、模型组件、视图组件

 

7、Sturt1的核心类、核心标签库？

ActionServlet 控制器、ActionMapping状态改变事件 、 Action控制器的一部分、ActionForward用户指向、ActionForm状态改变的数据

Html标签、bean标签、logic标签、tiles标签、nested标签

 

8、struts1与sturts2的区别（struts2是struts1和webwork的结合体）

1、struts1要求Action类继承一个抽象基类，而不是接口。

    struts2的action类可以实现一个action接口，也可以实现其他接口。

2、sturts1 action是单例模式，线程是安全的。

    struts2 action线程是不安全的，action为每一个请求都生成了一个实例。

3、sturts1过去依赖serlet API，不容易测试。

    struts2不依赖于容器，允许Action脱离容器单独被测试。

4、Struts1 使用ActionForm对象捕获输入。所有的ActionForm必须继承一个基类。

    Struts 2直接使用Action属性作为输入属性，消除了对第二个输入对象的需求。 

5、Struts1 整合了JSTL，因此使用JSTL EL。这种EL有基本对象图遍历，但是对集合和索引属性的支持很弱。

      Struts2可以使用JSTL，但是也支持一个更强大和灵活的表达式语言－－"Object Graph Notation Language"  (OGNL).

6、Struts 1使用标准JSP机制把对象绑定到页面中来访问。

    Struts 2 使用 "ValueStack"技术，使taglib能够访问值而不需要把你的页面（view）和对象绑定起来。

7、Struts 1 ActionForm 属性通常都是String类型。Struts1使用Commons-Beanutils进行类型转换。

   Struts2 使用OGNL进行类型转换。提供基本和常用对象的转换器。

8、Struts 1支持在ActionForm的validate方法中手动校验，或者通过Commons Validator的扩展来校验。

    Struts2支持通过validate方法和XWork校验框架来进行校验。  

9、Struts1支持每一个模块有单独的Request Processors（生命周期），但是模块中的所有Action必须共享相同的生命周期。

Struts2支持通过拦截器堆栈（Interceptor Stacks）为每一个Action创建不同的生命周期。堆栈能够根据需要和不同的Action一起使用。

 

9、过滤器和拦截器的区别

1、拦截器是基于java的反射机制的，而过滤器是基于函数回调

2、过滤器依赖于servlet容器，而拦截器不依赖于servlet容器

3、拦截器只能对action请求起作用，而过滤器则可以对几乎所有的请求起作用

4、拦截器可以访问action上下文、值栈里的对象，而过滤器不能

5、在action的生命周期中，拦截器可以多次被调用，而过滤器只在容器初始化时调用一次

  拦截器 ：是在面向切面编程的就是在你的service或者一个方法，前调用一个方法，或者在方法后调用一个方法比如动态代理就是拦截器的简单实现，在你调用方法前打印出字符串（或者做其它业务逻辑的操作），也可以在你调用方法后打印出字符串，甚至在你抛出异常的时候做业务逻辑的操作。

   过滤器：是在java web中，你传入的request,response提前过滤掉一些信息，或者提前设置一些参数，然后再传入servlet或者struts的 action进行业务逻辑，比如过滤掉非法url（不是login.do的地址请求，如果用户没有登陆都过滤掉）,或者在传入servlet或者 struts的action前统一设置字符集，或者去除掉一些非法字符.

 

 

10、Hibernate是一个开放源代码的对象关系映射框架，它对JDBC进行了非常轻量级的对象封装，使得java程序员可以随心所欲的使用对象编程思维来操纵数据库。

工作原理：

1.读取并解析配置文件2.读取并解析映射信息，创建SessionFactory 3.打开Sesssion 4.创建事务Transation 5.持久化操作6.提交事务7.关闭Session 8.关闭SesstionFactory

 

优点有：

1. 对JDBC访问数据库的代码做了封装，大大简化了数据访问层繁琐的重复性代码。

2. Hibernate是一个基于JDBC的主流持久化框架，是一个优秀的ORM实现。他很大程度的简化DAO层的编码工作

3、  Hibernate使用Java反射机制而不是字节码增强程序来实现透明性。

4、  Hibernate的性能好，映射的灵活性比较出色。它支持各种关系数据库，从一对一到多对多的各种复杂关系。

 

11、hibernate的核心类是什么？？重要方法是什么？？

Configuration、SessionFactory

 Session如下方法 Save、 load、 Update、Delete

 Query q=CreateQuery(“from Customer where customerName=:customerName”)

 beginTransaction、close、Transaction、Commit()

 

12、session.load()和session.get()的区别

Session.load/get方法均可以根据指定的实体类和id从数据库读取记录，并返回与之对应的实体对象。其区别在于：

如果未能发现符合条件的记录，get方法返回null，而load方法会抛出一个ObjectNotFoundException。

 

13、hql和sql的区别【可以这样说，hibernate是面向对象语言与关系型数据库之间的桥梁，他使得程序员可以不用关心底层数据库连接的代码，而可以专心写业务逻辑。】

sql是面向数据库表查询

hql是面向对象查询的,其form子句返回的是对象的实例。

 

14、hibernate与jdbc之间的区别【可以这样说，hibernate是面向对象语言与关系型数据库之间的桥梁，他使得程序员可以不用关心底层数据库连接的代码，而可以专心写业务逻辑。】

Hibernate作为一个O/R Mapping,比JDBC具备的优势有：

1.编程思想上，更加符合人的逻辑思维习惯，面向对象比面向过程更加容易理解，测试和维护

2.开发维护速度上，Hibernate显著的快，代码量显著小

3.通过Annotation进行数据库的字段加密

4.对Sql不熟的菜鸟来说可以自动调优

5.结合Spring，通过声明式事务可以省略事务的控制，事务以横切面形式出现

 

Jdbc比Hibernate具备的优势有：

1.大数据量访问时，Jdbc的效率显著快

2.直接操作数据库比较灵活

 

15、Hibernate是如何延迟加载？

当Hibernate在查询数据的时候，数据并没有存在与内存中，当程序真正对数据的操作时，对象才存在与内存中，就实现了延迟加载，他节省了服务器的内存开销，从而提高了服务器的性能。

 

16、说下Hibernate的缓存机制

　　1. 内部缓存存在Hibernate中又叫一级缓存，属于应用事物级缓存

　　2. 二级缓存：

　　a) 应用及缓存

　　b) 分布式缓存

c) 第三方缓存的实现

 

17、spring工作机制及为什么要用?【spring是一个轻量的控制反转和面向切面的容器框架】

　　1.springmvc把所有的请求都提交给DispatcherServlet,它会委托应用系统的其他模块负责对请求进行真正的处理工作。

　　2.DispatcherServlet查询一个或多个HandlerMapping,找到处理请求的Controller.

　　3.DispatcherServlet把请求提交到目标Controller

　　4.Controller进行业务逻辑处理后，会返回一个ModelAndView

　　5.Dispathcher查询一个或多个ViewResolver视图解析器,找到ModelAndView对象指定的视图对象

　　6.视图对象负责渲染返回给客户端。

IoC就是由容器来控制业务对象之间的依赖关系。控制反转的本质，是控制权由应用代码转到了外部容器，控制器的转移既是所谓的反转。控制权的转移带来的好处就是降低了业务对象之间的依赖程度，即实现了解耦。

DI/IOC,对持久层和表示层的控制与分配，增加系统的灵活性和稳定性. AOP,面向切面,利用代理对程序的有效管理.

spring是一个轻量级的IOC和AOP框架，通过spring的IOC实现松耦合，而作为一个AOP框架他又能分离系统服务，实现内聚开发  Spring 最好的地方是它有助于您替换对象。有了 Spring，只要用 JavaBean 属性和配置文件加入依赖性（协作对象）。然后可以很容易地在需要时替换具有类似接口的协作对象。}
Spring对多种ORM框架提供了很好的支持


Web项目答辩问题

1. css和div 开发的优势？
A、显示和内容实现分离
B、有利于搜索引擎搜索
C、有利于维护和程序的扩展
2. 谈谈页面间的参数传递有哪些方式 ？
A、通过作用域对象session、request 的setAttribute()和getAttribute()方法进行参数传递。
B、<jsp:forward>
        <jsp:param name= value=>
   </jsp:forward>
C、request.gerRequestDispatcher(“1.jsp?name=XX”).forward(request,response);
D、<jsp:useBean id=  class= scope=request/session>
3. hidden表单域有什么作用？
A、多个表单的区分
B、多个提交按钮
4. jsp有哪些内置对象?
pageContex,request,session,application,out,exception,config,page,
5. request的作用有哪些？
获取客户端传递的参数值
获取客户端请求头信息
获取会话
获取转发对象
可作为容器使用, 利用setAttribute()和getAttribute()方法进行参数传递
6. session有什么作用。
因为http协议是无状态的协议，但我们需要保存客户端在多次请求之间状态信息的时候，我们需要session来维护客户端的状态
Session对象类似于一个容器，可以存放任何对象，以供不同页面间共享数据

7. application有什么作用。
保存的一些全局性的对象信息。
8. 在jsp中怎样操作page作用域
特定于 JSP 的一个类型，代表当前的 JSP 页面。pageContext.setAttribute(“java”,”lovo”);
9. jsp有哪些动作?作用分别是什么?
<jsp:include />   包含
<jsp:forward />  转发到另一页面相当于
               request.getRequestDispatcher(“1.jsp?name=XX”).forward(request,response);
<jsp:usebean />  设置javaBean
<jsp:setProperty /> 设置属性
<jsp:getProperty />  获得属性
<jsp:plugin />    设置插件
10. java servlet api中forward() 与redirect()的区别？
1. forward客户端请求服务器一次，redirect请求服务器两次，所以forward方式可以获得request作用域的信息，而redirect方式不能获得。
2. forward由request对象发出，而redirect由response对象发起
3. redirect()可以跨越不同的工程之间。而forward()只能在一个工程中使用
11. class.forname的作用?为什么要用?
加载类；一般使用这个方法是反射方式创建对象；从而可以将一些类信息写在文件中，避免硬编码，增加灵活性。
12. 分页是怎么实现的？
Select top 5 * from 表名 where id not in(select top 10 id from 表名)
13. cookie被禁止后怎样使用session？
URL重写，对所有页面涉及的连接都使用url重写方式。从而将JsessionID以参数的方式链接到URL后面。保证每次页面提交时服务器都能获得sessionID，从而维持和客户端的状态。
14. 项目开发经历了哪几个阶段？
需求分析，设计(找用例，写用例文本，找实体，编写数据字典，画数据流图)，编码，测试，部署；
15. 谈谈项目的体系统架构：（客户层，表示层）web层，业务层，数据层？
客户层：IE浏览器，Applet小应用程序，在客户度允许
表示层：html静态页面，jsp页面，servlet在服务器上运行；
业务层：实现业务逻辑，服务器提供系统级服务，如事务管理，安全性，并非控制
数据层：如dao部分，实现对数据的增删改查等。

16. J2EE规范中的组件技术在项目中用到了哪些？
JDBC,jsp,servlet,javabean,xml,JNDI
17. TCP/IP通讯和UDP通迅的区别？
1) TCP/IP面向连接，可靠连接，UDP面向不连接，不可靠连接
2) 建立连接经历3次握手，udp无需连接，ip和port封装在datagram数据包中，自寻址。
18. 浏览器和WEB服务器是用什么协议通迅的？
应用层使用的是 HTTP协议，传输和路由使用的是TCP/IP
19. 网络通讯中，端口有什么含义。端口的取值范围？
端口用于区分基于TCP/IP通讯的不同应用程序, 每个基于TCP/IP应用程序都会向操作系统申请注册一个服务，这个服务用端口表示。本质上说，端口就是一段内存中的缓冲区。可以认为是计算机与外界交流的出口。
建议用户使用的端口号 1024-----65535系统使用的端口范围0 --- 1024
20. 说出3个常见协议的默认端口。
Web服务器80，ftp 21，telenet 23,smtp 25
21. socket是什么，它有什么作用？
Socket是通讯的端点，是客户端和服务器进行通讯的端点
22. TCP/IP通讯的基本步骤是什么？
基于TCP/IP通讯的程序：必须先建立和服务器端的连接，然后才能通讯。
服务器端：ServerSocket  ss = new ServerSocket(port); 创建serverSocket对象
          ss.accept()在port端口监听，等待客户端请求到来
客户端：  Socket s = new Socket(ip,port); 建立和服务器的连接；连接不成功，抛出异常
          s.getOutputStream()和s.getInputStream()和向服务器发送请求信息和接收服务器返回的信息
23. UDP通讯的基本步骤是什么？
1） 创建DatagramSocket对象
2） 通过datagramSocket发送(接收)datagramPacket数据包
3） 从datagramPacket数据包中取出接收和封装要发送的数据
24. JDBC访问数据库的基本步骤是什么？
1） 加载驱动
2） 通过DriverManager对象获取连接对象Connection
3） 通过连接对象获取会话
4） 通过会话进行数据的增删改查，封装对象
5） 关闭资源
25. 说说preparedStatement和Statement的区别
1） 效率：预编译会话比普通会话对象，数据库系统不会对相同的sql语句不会再次编译
2） 安全性，可以有效的避免sql注入攻击！sql注入攻击就是从客户端输入一些非法的特殊字符，而使服务器端在构造sql语句的时候仍然能够正确构造，从而收集程序和服务器的信息和数据。
比如：“select * from t_user where userName = ‘” + userName + “ ’ and password =’” + password + “’”
如果用户名和密码输入的是’1’ or ‘1’=’1’ ;  则生产的sql语句是：
“select * from t_user where userName = ‘1’ or ‘1’ =’1’  and password =’1’  or ‘1’=’1’  这个语句中的where 部分没有起到对数据筛选的作用。
26. 说说事务的概念，在JDBC编程中处理事务的步骤。
1） 事务是作为单个逻辑工作单元执行的一系列操作。
2） 一个逻辑工作单元必须有四个属性，称为原子性、一致性、隔离性和持久性 (ACID) 属性，只有这样才能成为一个事务
事务处理步骤：
3） conn.setAutoComit(false);设置提交方式为手工提交
4） conn.commit()提交事务
5） 出现异常，回滚 conn.rollback();

27. 数据库连接池的原理。为什么要使用连接池。
1） 数据库连接是一件费时的操作，连接池可以使多个操作共享一个连接。
2） 数据库连接池的基本思想就是为数据库连接建立一个“缓冲池”。预先在缓冲池中放入一定数量的连接，当需要建立数据库连接时，只需从“缓冲池”中取出一个，使用完毕之后再放回去。我们可以通过设定连接池最大连接数来防止系统无尽的与数据库连接。更为重要的是我们可以通过连接池的管理机制监视数据库的连接的数量?使用情况，为系统开发?测试及性能调整提供依据。
3） 使用连接池是为了提高对数据库连接资源的管理
28. 谈谈DAO模式的原理的作用。
DAO是一种设计模式
包括三个部分1）DAO接口
2）DAO接口实现类，
3）PO持久化对象，它和数据库相对应
29. servlet和jsp有什么关系？
       Servlet和JSP都是服务器的组件。
       Servlet是一个接口，也是SUN公司提出的一种用户和WEB容器之间通信的标准。由用户实现其中的service()方法供WEB容器进行调用，从而实现servlet和WEB容器之间的交互。所以当用户要和WEB容器通信时必须实现这种标准。而JSP规范规定，由容器翻译好的JAVA类必须实现HttpJspPage接口，而这个接口是servlet的子接口，从这个意义上说，JSP的本质还是servlet。
      JSP重在表示，解决了servlet页面输出困难的问题。而servlet重在业务处理，避免在页面出现过多的业务处理带来的阅读性和维护性的困难。它们可以很好的结合。
      Servlet编写后需要在WEB应用的web.xml进行注册，从而能让WEB容器识别用户编码的Servlet。但JSP由容器来管理，所以无需注册。
30. jsp是如何被容器调用和执行的？
1）由JSP引擎将JSP页面翻译成JAVA代码
2）将JAVA代码编译成class字节码文件
3）加载到容器
4）由容器实例化成对象
5）初始化阶段相关的方法是jspInit()
6）请求到达，调用服务阶段相关的方法是_jspService()
7）销毁阶段相关的方法是jspDestroy()
31. 编写一个servlet的步骤。
1）新建一个类继承于HttpServlet
2) 重写其中的doGet和doPost方法
3）完成servlet的注册。在web.xml中加入<serlvet><servlet-mapping>标记
32. doGet和doPost方法各有什么作用？
doGet完成Get方式的请求处理。doPost完成Post方式请求处理
33. 为什么要为servlet配置URL映射？
Servlet注册包括两部分，第一，容器如何找到Servlet，利用
<servlet>
     <servlet-name></servlet-name>Servlet名字
     <servlet-class></servlet-class>Servlet类的全路径
</servlet>
完成。
第二，客户端如何找到当前的Servlet。利用
<servlet-mapping>
     <servlet-name></servlet-name>Servlet名字
     <url-pattern></ url-pattern >客户端请求路径
</servlet-mapping>
完成。
配置URL的主要作用是客户端通过什么路径能去找到Servlet
34. servlet的类架构是什么样的。
Servlet是Sun公司提供的用户和WEB服务器通讯的接口，所有Servlet都必须实现这个接口。J2EE API中提供了一个类GenericServlet对Servlet接口作了简单的实现。同时，这个类还实现了ServletConfig接口。来对Servlet进行一些配置。GenericServlet有一个专门针对于Http协议进行实现的一个子类HttpServlet。
35. 谈谈servlet的生命周期？
1）容器装载并实例化Servlet
2) 调用init()方法完成Servlet初始化
3）当请求到达时，调用service()方法处理请求，产生响应
4）销毁阶段调用destroy()方法完成清理工作。
36. servlet是线程安全的吗？为什么？
不安全。因为Servlet对象在整个过程中，至始至终只有一个对象。以节约服务器资源的消耗，这就意味着很多个线程会同时访问一个Servlet对象。所以线程不安全。
37. 你是如何处理servlet线程安全问题的？
解决Servlet线程安全问题方法有三种
1）编写Servlet类的时候，实现SingleThreadModel接口，将Servlet变成单线程机制。
2）涉及对共享资源访问的时候，使用synchronized同步加锁，实现共享资源的保护。
3）尽量不在Servlet中定义成员变量，使用局部变量。
在三种方法中，最好使用第三种，这样线程安全，并且性能最高。
38. 如何得到客户端的请求参数？
request.getParameter()单个数据
request.getParameterValues()一组数据
request.getParameterMap()返回所有的键值对
39. request.getParameter和request.getParameterValues的区别，它们的返回值是什么类型？
     request.getParameter获得单个表单的数据。返回值是String类型。而request.getParameterValues()是获得表单元素名相同的一组数据。返回值是String[]数组。
40. response对象的作用？
Response对象是对服务器的响应信息作出的一个封装对象。主要作用有：
1）可以从response中获得输出流对象，从而可以向客户端输出信息
2）可以实现重定向，response.sendRedirect();
3) 可以设置响应头和状态码。
4）可以实现URL重写
41. request对象的作用范围是什么？
一次请求响应完成后，就会销毁。
42. session对象的作用范围是什么
在一个用户会话期间有效。
43. application对象的作用范围是什么。
存在于整个web应用。当WEB容器关闭时，才会销毁
44. session对象是什么时候产生的，什么时候销毁的？
当用户访问web容器，而容器调用了request.getSession()方法后，产生Session对象。用以保存客户端在服务器上的信息。同时给这个Session分配一个唯一的标识ID。并产生一个set-cookies的响应头，以JsessionID作为键，标识ID作为值向客户端的cookie中写入内容，当客户端下次再发出请求时，就会将这个JsessionID以请求头的方式向服务器进行发送。而容器读取了JsessionID请求头后，就会根据这个ID找到相对应的Session对象，从而维持服务器和客户端的状态。
销毁session方法有三种
1）session超时
2）调用session对象的invalidate()方法
3）web容器关闭或崩溃
程序能控制是前二种。

45. 项目中用到了session对象吗，在哪里用到的？
登陆时，使用session保持用户信息。购物车制作时，使用session保持用户的购物信息
46. session和cookie有什么区别。
1) session保存在服务器，客户端不知道它的信息；而cookie保存在客户端，服务器知道其中的信息。
2) session中 保存的是对象，而cookie中保存的是字符串
3) session是不能区分路径的，同一个客户在访问web服务器之间，在任何地方都能够访问得到session中保存的信息的。而cookie如果设置了路径参数，同一个网站下的不同路径的cookie互相是访问不到的。
4) session是以cookie或URL重写为基础的，默认使用cookie来实现，系统会创造一个名为JSESSIONID的输出cookie，我们叫做session cookie,以区别persistent cookies,也就是我们通常所说的cookie,注意session cookie是存储于浏览器内存中的，并不是写到硬盘上的，这也就是我们刚才看到的JSESSIONID，我们通常情是看不到JSESSIONID的，但是当我们把浏览器的cookie禁止后，web服务器会采用URL重写的方式传递Sessionid，我们就可以在地址栏看到sessionid=KWJHUG6JJM65HS2K6之类的字符串。
47. .Http协议是无状态的，服务器是用什么方式为一个客户端保存状态的？
Hidden表单域   cookie   session   URL重写
48. servlet或jsp能同时响应多个客户端的请求吗？是通过什么方式做到的？
能够。多线程
49. 请简述servlet多线程的实现方式？
每次客户端请求过来的时候，WEB容器会产生一个线程来处理这个请求，这样就实现了servlet多线程。
50. 在servlet中定义成员变量(全局变量)，有线程安全问题吗？如何处理？
有。避免使用实例变量是保证servlet线程安全的最佳选择。每个线程有自己私有的栈空间，方法中的临时变量是在栈上分配空间，他们不会影响线程的安全。
51. 请求转发和重定向的区别。
1） 内部转发客户端向服务器发起一次请求，重定向客户端向服务器发出两次请求
2） 内部转发由request对象发起，重定向是response发起的
3） 内部转发不会引起地址栏的变化，而重定向会导致地址栏变化
52. JSP中动态包含和静态包含的区别。
1) 静态包含在转换成为java文件的时候将要包含的文件包含进来，作为一个整体编译。动态包含是各个包含文件分别转换，分别编译。
2) 静态包含在两个文件中不能有相同的变量，动态包含允许
3) 静态包含只能包含文件，动态包含还可以包含servlet输出的结果
4) 静态包含不能使用变量作为文件名，动态包含可以使用变量作为文件名
5) 动态包含文件发生变化，包含文件会感知变化。


53. 谈谈MVC设计模式的概念，使用MVC的好处。
M模型层：模型层专注于处理业务逻辑和业务数据，它可以为多个视图准备数据，提高了应用的可重用性。
V视图层：用户看到的并与系统交互的界面，接收用户数据，向用户显示相关的数据。
C控制层：是模型层和视图层联系的纽带；接收视图层提交的请求，调用模型层的业务逻辑，根据业务逻辑的调用结果，控制系统转发的页面。
MVC模式的好处：实现了业务逻辑和界面显示处理的分离；J2EE架构实现了业务逻辑和数据存储的分离，界面显示和业务逻辑的分离。各层之间不受影响。
54. 模式1和模式2和区别。
模式1：jsp+javabean
模式2：jsp+servlet+javabean
55. 你的项目中建有多少张表，字段最多的表是哪一张？每张表里都有些什么字段？
56. 说说你项目开发的流程？
57. 说说你所开发模块的业务流程，业务是什么？
58. 谈谈监听器的原理、配置及使用。你在项目中是怎么用的？
用于监听请求，会话，上下文件对象相关事件，并在事件发生后作出处理。
只要写一个类实现相应的监听器接口，就写了一个相应的监听处理类。
在web.xml中使用<listener><listener-class></listener-class></listener>
59. 谈谈过滤器的原理，配置及使用。有多个过滤器如何进行配置？
过滤器允许你拦截请求，还可以允许你控制响应。还可以能够对请求头、响应头、消息体的数据进行更改。同时，还可以对返回的流信息进行压缩。项目中使用字符编码格式的处理使用了过滤器和包装器。过滤器需要在web.xml容器中进行注册，才能被web容器识别
<filter><filter-name></filter-name><filter-class><filter-class></filter>
<filter-mapping><filter-name></filter-name>
<url-pattern></url-pattern >(<servlet-name></servlet-name>)</filter-mapping >

如果有多个过滤器优先执行url-pattern，再执行servlet-name;如果有多个url-pattern按web.xml布署顺序执行。
60. 你在项目中的角色是什么，你是如何进行工作的？
61. 你所做的工作，如何和小组其它人员所做的工作进行协调（数据库设计、程序模块编写等两个方面来说）；
62. 一个页面中有两个form，如何处理提交？
可以使用提交按钮的名称来判断，也可以使用hidden隐藏表单进行值的区分。
63. web项目与java项目有什么区别？
64. 不用eclipse，如何手工发布tomcat项目？
65. MVC模式在项目中，都是怎么用的？
   
66. 请谈谈请求转发的原理？
请求转发是针对同一工程下资源的转发。客户端在这个过程中，只请求服务器一次，请求转发由request.getRequestDispather(“”).forward(request,response).
67. 请说明重定向的原理？
重定向由response发起。当用户请求服务器时，由服务器向客户端发送一个302的状态码，并产生一个Location的响应头。当客户端接受到这样的状态码时，会马上读取Location响应头，并将地址栏改为Location里的内容。然后再向服务器发出请求。这个过程中客户端发出了两次请求。并可向不同的服务器发送请求。
68. 你是否从其它人的表中调用数据，如何进行协调？
69. 在家开发的模块，如何拿到公司与小组成员的进行合并？
70. 你在项目中是如何处理乱码的？
1) 使用过滤器和包装器设置统一的字符编码格式。
2) 页面使用统一的编码格式<%@page contentType=”text/html;charset=utf-8”%>
71. 谈谈项目中分页的实现？
    select top "+ count+" * from t_info where id not in(select top "
+(page-1)* count+" id from t_info)
72. CSS有哪几中选择器？有什么区别？
类选择器  ID选择器  元素选择器
73. 你在web项目中，数据共享有哪些方式 ？如果实现的？
Request,session,application(servletContext).   通过setAttribute和getAttribute实现
74. 项目各个阶段会产生什么样的文档？都有什么作用？
75. 项目结构是如何划分的？应该注意些什么？
76. servlet中，如何取得HTTP头信息？
Request.getHeader();
Request.getHeaders();

77. servlet程序中，可以获得客户机的IP地址吗？如何得到？
request.getRemoteAddr(); request.getRemoteHost(),request.getRemotePort(),request.getRemoteUser
78. URL与URI的区别？
    url:统一资源定位符， url定位客户端连接到服务器所需要的信息
uri:统一资源标志符：
    uri是url的一部分，没有域名和查询字符串，即域名之后查询字符串之前所有的信息，用于指定资源
79. servlet中的service方法在什么时候调用？
每一次客户端请求一个servlet资源的时候，由web容器调用。
80. 文件上传的原理是什么？
<form method=POST, enctype=”multipart/form-data” action=””>
<input type=file name=filesss />
    浏览器会把 文件内容连同 form的所有字段 格式化后传递到服务器，以二进制方式读取流后，就不能以request.getParameter的方式读取表单中的参数信息了。
81. 文件上传的form编写中，应该注意些什么？
    enctype=multipart/form-data method=post
82. 在项目中，文件上传到服务器上后，你是怎么处理的？
使用request.getInputStream()获得字节流，然后将字节流写入文件。
83. 如何打包一个web项目？
Jar  –cf   xx.war  WEB-INF  *.html  *.jsp  *.jpg
84. MIME的作用是什么？
告诉客户端浏览器你返回的内容是哪一种类型的，让浏览器采取相应的策略来显示处理你返回的文档或者文件。
85. tomcat容器是如何创建servlet类实例？用到了什么原理？
当容器启动时，会读取在webapps目录下所有的web应用中的web.xml文件，然后对xml文件进行解析，并读取servlet注册信息。然后，将每个应用中注册的servlet类都进行加载，并通过反射的方式实例化。（有时候也是在第一次请求时实例化）
在servlet注册时加上<load-on-startup>1</load-on-startup>如果为正数，则在一开始就实例化，如果不写或为负数，则第一次请求实例化。
86. servlet构造函数中可以执行初始化代码，为什么还要init方法呢？
如果在servlet构造函数中放置初始化代码，很容易导致servlet实例的创建失败。这样会导致Servlet无法响应客户端的请求
87. HttpServletRequest和HttpServletResponse是在哪里创建的？
当客户端请求到来的时候，由web容器创建。
88. 如何在一个servlet中，把页面转到www.qq.com.页面中。
Response.sendRedirect(“http://www.qq.com”);
89. ServletRequest与HttpServletRequest有什么区别与联系？
ServletRequest是HttpServletRequest的父接口，HttpServletRequest是特别针对Http协议而定义的接口，里面定义了得到http协议请求信息的方法。
90. servlet中如何到得项目的绝对路径？
Request.getContextPath();
91. jsp中taglib指令的作用是什么？
这个指令是标签库指令。指示标签库的逻辑路径，以及标签库的使用前缀。
使用taglib指令<%@taglib uri=””  prefix=””  %>
92. 文件下载如何实现？如何保证授权用户的下载？
1） 设置setContextType(),MIME类型。
2） 打开文件，按照二进制流的方式将字节数发往客户端。
93. 在servlet中，如何得到web.xml中配置的初始化参数？
      ServletConfig.getInitParameter()
94. 在doGet方法中，使用synchronized会产生什么样的后果？
这是由于对共享资源的访问而采取的线程安全措施，但是在多线程环境下，同步加锁会带来性能的下降。
95. 如何进行URL重写？要用到什么方法？
当客户端禁用cookie后，服务器的sessionID就无法发送给客户端。从而无法维持和客户端的状态。解决方法是，对链接重新编码。在链接产生时，在链接后面加上一个JsessionID用以维持客户端和服务器的状态
Response.encodeURL();
96. session如何过期？项目中该怎么应用？
setMaxInternalTime(); session.invalide();….
在web.xml中加入
<session-config>
        <session-timeout>30</session-timeout>
</session-config>
97. tomcat容器的作用是什么？
   a) 通信支持：
   b) 生命周期管理。
   c) 多线程支持:
   d) jsp支持
   e) 安全性管理
98. 在servlet中，怎么直接往客户端输出信息？
out = response.getWriter(),  out = response.getOutputStream().
99. 直接在jsp中调用DAO的方法，并显示数据，可以吗？这种方式有什么缺点？
可以在jsp中调用DAO的方法，显示数据。但是这种方式使得数据显示和数据持久化混杂在一起，不利于代码的维护。使得数据操作和页面显示耦合在了一起。
100. jsp中的import指令有什么作用？
导入在jsp中要使用的类文件。
101. 如何在jsp中使用bean?
使用javabean。
<jsp:userBean  id=  class=  />设置JavaBean
<jsp:setProperty name=  property=  value=>设置JavaBean属性值
<jsp:getProperty name=  property=  >获得JavaBean属性值

102. 请写出DAO中，针对User的CRUD方法设计。
Public void save(BookInfoPO po);
Public void update(BookInfoPO po);
Public void del(int  id);
Public List  findAll();

103. 发布项目时，把一jsp文件放到webroot下，与放在web-inf下，有什么区别？
因为web-inf下,应用服务器把它指为禁访目录,即直接在浏览器里是不能访问到的.  
  但是可以让servlet进行访问,如web-inf下有a.jsp则可以用  request.getRequestDispatcher("/WEB-INF/a.jsp").forward(request,response); 
<jsp:forward page="/WEB-INF/a.jsp"></jsp:forward>
104. web.xml中welcome-file配置项的作用是什么？
当我们在访问web应用时，如果没有指定访问的页面的时候，会自动定向到welcome-file所指定的页面
105. servlet中的response.sendError的作用是什么？
这是设置响应信息中状态码的方法。当我们使用response.sendError(404,”file  not  found”);之后就是发送了一个404的状态码，并作了状态码的描述。浏览器接受了状态码后，就可对不同的状态码作出相应的处理。
106. 如何用过滤器实现用户登录认证？
107. xml有什么作用？
108. 请说明什么是格式良好的xml文档？
109. 请说明什么是格式有效的xml文档？
110. 一个格式良好的xml文档有哪些规范？请列举？
111. DTD和schema有什么作用？两者什么区别？
112. 请谈谈你所知道的xml解析方式？
113. 不使用eclipse，如何启动tomcat?
114. jstl是什么？
标准标签库，对于在JSP页面上的JAVA常用的代码作出了一些封装，并以标记的格式显示。从而避免在JSP页面上直接写入java代码，增加页面的可读性和可维护性。
115. 对客户输入的数据，可以在哪些方面对数据格式的合法性进行验证？
在服务器端写入方法对客户端的数据进行合性性验证。主要有长度判断，正规表达式等等。
116. 在web项目中，如何配置出错页面？
在web.xml中写入：
<error-page>
<error-code>404</error-code>
<location>/error.jsp</location>
   <error-page>
117. 任意抽取一段学生所写的代码，谈谈这段代码的作用。
118. ajax的基本原理是什么。
Javascript + asynchornors + xml 异步向服务器发起请求，AJAX可以像桌面应用程序一样只同服务器进行数据交换，却不用每次都刷新界面，也不用每次将数据处理的工作都交给服务器来做；这样既可减轻服务器负担又加快了响应速度、缩短了用户等待时间。
119. 119、jsp和javascript的区别？
Jsp是服务器端的动态网页技术，javascrip是操作客户端浏览器上元素的语言。 

1、JSP页面是如何被执行的？JSP执行效率比Servlet低吗？
当客户端向一个JSP页面发出请求时，Web Container将JSP转化成Servlet的源代码(只在第一次请求时)，然后编译转化后的Servlet并加载到内存中执行，执行的结果Response到客户端。
JSP只在第一次执行的时候会转化为Servlet，以后每次执行Web容器都是直接执行编译后的Servlet,所以JSP和Servlet只是在第一次执行的时候不一样，JSP慢一点，以后的执行都是相同的。

2、JSP如何处理运行时异常(run-time)exceptions?

可以使用页面的errorPage属性捕获没有处理的运行时异常，然后自动转向到一个错误处理页面，代码如下：
<%@ page errorPage=”error.jsp” %>
如果在页面请求时出现运行时异常是，以上代码会把页面转向到JSP页面error.jsp，在error.jsp里面，可以通过以下代码定义这个页面是错误处理页:

< %@ page isErrorPage=”true” %>

这样描述错误信息的Throwable对象就可以在error.jsp页面里面访问到。

3、如果jsp表单元素的值为空，如何避免null出现在页面上？

可以写一个简单的函数对空值进行处理，判断值是否为空，如果是空就返回空字符串。实例代码如下：
< %! String blanknull(String s){ return (s == null) ? “” : s; } %>
在你的JSP里面，可以使用以上函数输出文本框或者其他页面元素的值，实例代码如下：

<input type=”text” name=”shoesize” value=”<% =blanknull(shoesize) %>” />

4、如何避免JSP页面自动生成session对象？为什么要这么做？

在默认情况下，在对一个JSP页面发出请求时，如果session还没有建立，JSP页面会自动为请求建立一个session对象，但是session是比较消耗资源的，如果没必要保持和使用session，就不应该创建session, 例如一些只是用来宣传产品的网站，往往没必要使用session来保存信息，可以使用jsp页面指令session=”false”来避免JSP页面为每个请求都自动创建session.实例代码如下：

< %@ page session=”false”>

5、在servlets和JSP之间能共享session对象吗？

当然可以，
HttpSession session = request.getSession(true);
session.putValue(”variable”,”value”);

6、Servlet都有哪些方法？主要作用是什么？

HttpServlet 类包含 init() 、 destroy() 、 service() 等方法。其中 init() 和 destroy() 方法是继承的。
(1) init() 方法
在 Servlet 的生命期中，仅执行一次 init() 方法。它是在服务器装入 Servlet 时执行的。 可以配置服务器，以在启动服务器或客户机首次访问 Servlet 时装入 Servlet 。 无论有多少客户机访问 Servlet ，都不会重复执行 init() 。
缺省的 init() 方法通常是符合要求的，但也可以用定制 init() 方法来覆盖它，典型的是管理服务器端资源。 例如，可能编写一个定制 init() 来只用于一次装入 GIF 图像，改进 Servlet 返回 GIF 图像和含有多个客户机请求的性能。另一个示例是初始化数据库连接。缺省的 init() 方法设置了 Servlet 的初始化参数，并用它的 ServletConfig 对象参数来启动配置， 因此所有覆盖 init() 方法的Servlet 应调用 super.init() 以确保仍然执行这些任务。在调用 service() 方法之前，应确保已完成了 init() 方法。
(2) service() 方法
service() 方法是 Servlet 的核心。每当一个客户请求一个 HttpServlet 对象，该对象的 service() 方法就要被调用，而且传递给这个方法一个“请求”（ ServletRequest ）对象和一个“响应”（ ServletResponse ）对象作为参数。 在 HttpServlet 中已存在 service() 方法。缺省的服务功能是调用与 HTTP 请求的方法相应的 do 功能。例如， 如果 HTTP 请求方法为 GET ，则缺省情况下就调用doGet() 。 Servlet 应该为 Servlet 支持的 HTTP 方法覆盖 do 功能。因为 HttpServlet.service() 方法会检查请求方法是否调用了适当的处理方法，不必要覆盖 service() 方法。只需覆盖相应的 do 方法就可以了。
= 当一个客户通过 HTML 表单发出一个 HTTP POST 请求时， doPost （）方法被调用。 与 POST 请求相关的参数作为一个单独的 HTTP请求从浏览器发送到服务器。当需要修改服务器端的数据时，应该使用 doPost() 方法。
= 当一个客户通过 HTML 表单发出一个 HTTP GET 请求或直接请求一个 URL 时， doGet() 方法被调用。 与 GET 请求相关的参数添加到 URL 的后面，并与这个请求一起发送。当不会修改服务器端的数据时，应该使用 doGet() 方法。
Servlet 的响应可以是下列几种类型：
一个输出流，浏览器根据它的内容类型（如 text/HTML ）进行解释。
一个 HTTP 错误响应 , 重定向到另一个 URL 、 servlet 、 JSP 。
(3) destroy() 方法
destroy() 方法仅执行一次，即在服务器停止且卸装 Servlet 时执行该方法。典型的，将 Servlet 作为服务器进程的一部分来关闭。缺省的 destroy() 方法通常是符合要求的，但也可以覆盖它，典型的是管理服务器端资源。例如，如果 Servlet 在运行时会累计统计数据，则可以编写一个 destroy() 方法，该方法用于在未装入 Servlet 时将统计数字保存在文件中。另一个示例是关闭数据库连接。
当服务器卸装 Servlet 时，将在所有 service() 方法调用完成后，或在指定的时间间隔过后调用 destroy() 方法。一个 Servlet 在运行 service() 方法时可能会产生其它的线程，因此请确认在调用 destroy() 方法时，这些线程已终止或完成。
(4) GetServletConfig（）方法
GetServletConfig （）方法返回一个 ServletConfig 对象，该对象用来返回初始化参数和 ServletContext 。 ServletContext 接口提供有关 servlet 的环境信息。
(5) GetServletInfo（）方法
GetServletInfo （）方法是一个可选的方法，它提供有关 servlet 的信息，如作者、版本、版权。
当服务器调用 sevlet 的 Service （）、 doGet （）和 doPost （）这三个方法时，均需要 “请求”和“响应”对象作为参数。“请求”对象提供有关请求的信息，而“响应”对象提供了一个将响应信息返回给浏览器的一个通信途径。 javax.servlet 软件包中的相关类为 ServletResponse 和 ServletRequest ，而 javax.servlet.http 软件包中的相关类为 HttpServletRequest 和 HttpServletResponse 。 Servlet 通过这些对象与服务器通信并最终与客户机通信。 Servlet 能通过调用“请求”对象的方法获知客户机环境，服务器环境的信息和所有由客户机提供的信息。 Servlet 可以调用“响应”对象的方法发送响应，该响应是准备发回客户机的。

7、Java Servlet的主要功能和作用是什么？
Servlet 通过创建一个框架来扩展服务器的能力，以提供在 Web 上进行请求和响应服务。当客户机发送请求至服务器时，服务器可以将请求信息发送给 Servlet ，并让 Servlet 建立起服务器返回给客户机的响应。 当启动 Web 服务器或客户机第一次请求服务时，可以自动装入 Servlet 。装入后， Servlet 继续运行直到其它客户机发出请求。 Servlet 的功能涉及范围很广。例如， Servlet 可完成如下功能：
(1) 创建并返回一个包含基于客户请求性质的动态内容的完整的 HTML 页面。
(2) 创建可嵌入到现有 HTML 页面中的一部分 HTML 页面（ HTML 片段）。
(3) 与其它服务器资源（包括数据库和基于 Java 的应用程序）进行通信。
(4) 用多个客户机处理连接，接收多个客户机的输入，并将结果广播到多个客户机上。例如， Servlet 可
以是多参与者的游戏服务器。
(5) 当允许在单连接方式下传送数据的情况下，在浏览器上打开服务器至 applet 的新连接，并将该连
接保持在打开状态。当允许客户机和服务器简单、高效地执行会话的情况下， applet 也可以启动客户浏览器和服务器之间的连接。可以通过定制协议或标准（如 IIOP ）进行通信。
(6) 对特殊的处理采用 MIME 类型过滤数据，例如图像转换和服务器端包括（ SSI ）。
(7) 将定制的处理提供给所有服务器的标准例行程序。例如， Servlet 可以修改如何认证用户。

8、Request对象的主要方法有哪些？
setAttribute(String name,Object)：设置名字为name的request的参数值
getAttribute(String name)：返回由name指定的属性值
getAttributeNames()：返回request对象所有属性的名字集合，结果是一个枚举的实例
getCookies()：返回客户端的所有Cookie对象，结果是一个Cookie数组
getCharacterEncoding()：返回请求中的字符编码方式
getContentLength()：返回请求的Body的长度
实例
getInputStream()：返回请求的输入流，用于获得请求中的数据
getMethod()：获得客户端向服务器端传送数据的方法
getParameter(String name)：获得客户端传送给服务器端的有name指定的参数值
getParameterNames()：获得客户端传送给服务器端的所有参数的名字，结果是一个枚举的实例
getParameterValues(String name)：获得有name指定的参数的所有值
getProtocol()：获取客户端向服务器端传送数据所依据的协议名称
getQueryString()：获得查询字符串
getRequestURI()：获取发出请求字符串的客户端地址
getRemoteAddr()：获取客户端的IP地址
getRemoteHost()：获取客户端的名字
getSession([Boolean create])：返回和请求相关Session
getServerName()：获取服务器的名字
getServletPath()：获取客户端所请求的脚本文件的路径
getServerPort()：获取服务器的端口号
removeAttribute(String name)：删除请求中的一个属性

9、使用JSP连接到数据库连接缓冲池的最好方法是什么？

1.使用JDBC2。0中带有此服务的Driver
2.使用提供有此服务的Application server
3.自己写

10、在JSP中如何写文本文件？

使用PrintWriter对象，如：
< %@ page import=”java.io.*” %>
< % String str = “print me”; String nameOfTextFile = “/usr/anil/imp.txt”; try { PrintWriter pw = new PrintWriter(new FileOutputStream(nameOfTextFile)); pw.println(str); pw.close(); } catch(IOException e) { out.println(e.getMessage()); } %>
11、JSP的缺点？

1.对JAVA程序进行调试没有好东东
2.因大多数的servlet引擎不支持connection pooling
3.Servlet引擎没有标准
4.JSP与其它脚本语言的交互

12、在JSP中如何删除一个COOKIE?
< % Cookie killMyCookie = new Cookie(”mycookie”, null); killMyCookie.setMaxAge(0); killMyCookie.setPath(”/”); response.addCookie(killMyCookie); %>
13、如何现实servlet的单线程模式？

< %@ page isThreadSafe=”false”%>

14、说出Servlet和CGI的区别？
与cgi的区别在于servlet处于服务器进程中，它通过多线程方式运行其service方法，一个实例可以服务于多个请求，并且其实例一般不会销毁，而CGI对每个请求都产生新的进程，服务完成后就销毁，所以效率上低于servlet。

15、Servlet的生命周期？

Servlet是一种可以 在Servlet容器中运行的组件，那么理所当然就应该有一个从创建到销毁的过程，这个过程我们可以称之为Servlet生命周期。Servlet的生命 周期可以分为加载、实例化、初始化、处理客户请求和卸载五个阶段，体现在方法上主要是init（）、service（）和destroy（）三个方法。生 命周期的具体说明如下：

Servlet容器完成加载Servlet类和实例化一个Servlet对象

init（）方法完成初始化工作，该方法由Servlet容器调用完成

service（）方法处理客户端请求，并返回响应结果

destroy（）方法在Servlet容器卸载Servlet之前被调用，释放一些资源

16、介绍一下javax.servlet.Servlet接口及其主要方法？

Servlet接口的主要作用是提供Servlet生命周期的init()、service()和destroy()方法。
servlet接口中的主要方法有：
void init(ServletConfit config)throws ServletException
在servlet被载入后和实施服务前由servlet引擎进行一次性调用。如果init()产生溢出UnavailableException，则 servle退出服务。

ServletConfig getServletConfig()
返回传递到servlet的init()方法的ServletConfig对象
void service(ServletRequest request, ServletResponse response)throws ServletException,IOException
处理request对象中描述的请求，使用response对象返回请求结果
String getServletInfo()
返回描述servlet的一个字符串
void destory()
当servlet将要卸载时由servlet引擎调用，销毁Servlet实例。

17、HttpServlet类中的主要方法都有哪些？各自的作用是什么？

HttpServlet的主要方法有 doGet, doPost, doPut, doDelete, doTrace等等

Void doGet(HttpServletRequest request,HttpServletResponse response)throws ServletException,IOException
由servlet引擎调用用处理一个HTTP GET请求。输入参数、HTTP头标和输入流可从request对象、response头标和response对象的输出流中获得。
Void doPost(HttpServletRequest request,HttpServletResponse response)throws ServletException,IOException
由servlet引擎调用用处理一个HTTP POST请求。输入参数、HTTP头标和输入流可从request对象、response头标和response对象的输出流中获得。
Void doPut(HttpServletRequest request,HttpServletResponse response)throws ServletException,IOException
由servlet引擎调用用处理一个HTTP PUT请求。本方法中请求URI指出被载入的文件位置。
Void doDelete(HttpServletRequest request,HttpServletResponse response)throws ServletException,IOException
由servlet引擎调用用处理一个HTTP DELETE请求。请求URI指出资源被删除。
Void doOptions(HttpServletRequest request,HttpServletResponse response)throws ServletException,IOException
由servlet引擎调用用处理一个HTTP OPTIONS请求。返回一个Allow响应头标表明此servlet支持的HTTP方法。一个servlet不需要覆盖此方法，因为 HttpServlet方法已经实现规范所需的功能。
Void doTrace(HttpServletRequest request,HttpServletResponse response)throws ServletException,IOException
由servlet引擎调用用处理一个HTTP TRACE请求。使得请求头标被反馈成响应关标。一个servlet不需要覆盖此方法，因为HttpServlet方法已经实现HTTP规范所需的功能。
Void service(HttpServletRequest request,HttpServletResponse response)throws ServletException,IOException
Service(Request request,Response response)调用的一个立即方法，带有指定HTTP请求和响应。此方法实际上将请求导向doGet()、doPost()等等。不应该覆盖此方法。
Void service(Request request,Response response)throws ServletException,IOException
将请求和响应对象置入其指定的HTTP子类，并调用指定HTTP的service()方法。

18、XML文档定义有几种形式？它们之间有何本质区别？解析XML文档有哪几种方式？

a: 两种形式 dtd schema，

b: 本质区别:schema本身是xml的，可以被XML解析器解析(这也是从DTD上发展schema的根本目的)。

c:有DOM,SAX,STAX等
DOM:处理大型文件时其性能下降的非常厉害。这个问题是由DOM的树结构所造成的，这种结构占用的内存较多，而且DOM必须在解析文件之前把整个文档装入内存,适合对XML的随机访问；SAX:不现于DOM,SAX是事件驱动型的XML解析方式。它顺序读取XML文件，不需要一次全部装载整个文件。当遇到像文件开头，文档结束，或者标

签开头与标签结束时，它会触发一个事件，用户通过在其回调事件中写入处理代码来处理XML文件，适合对XML的顺序访问
STAX:Streaming API for XML (StAX）

19、你在项目中用到了xml技术的哪些方面?如何实现的?

用到了数据存储，信息配置两方面。在做数据交换平台时，将不能数据源的数据组装成XML文件，然后将XML文件压缩打包加密后通过网络传送给接收者，接收解密与解压缩后再同XML文件中还原相关信息进行处理。在做软件配置时，利用XML可以很方便的进行，软件的各种配置参数都存储在XML文件中。

① web前端优化

② 事件冒泡（选项卡的实现）

③ CSS布局相关

④ 应该用float吗？

⑤ 模块化编程

⑥ 为什么有闭包

⑦ 延迟请求

① 作用域问题

PS：其实是settimeout会抛往主干流程外......
② 语义化标签

这道题我确实没辙，之前其实差点写类似的博客，却没有写，今天结束后补上吧！

1）tite与h1的区别

2）b与strong的区别

3）i与em的区别

PS：不要小看这些题，80%人答不上来

#前端开发面试题（题目列表+答案 完整版）


## <a name='list'>目录</a>

  1. [前言](#preface)
  1. [HTML 部分](#html)
  1. [CSS  部分](#css)
  1. [JavaScript 部分](#js)
  1. [其他问题](#other)
  1. [优质网站推荐](#web)



## <a name='preface'>前言</a> ##
 
本文总结了一些优质的前端面试题（多数源于网络），初学者阅后也要用心钻研其中的原理，重要知识需要系统学习，透彻学习，形成自己的知识链。万不可投机取巧，只求面试过关是错误的！

 ###面试有几点需注意：(来源程劭非老师 github:@wintercn)

1. 面试题目： 根据你的等级和职位变化，入门级到专家级：广度↑、深度↑。

1. 题目类型： 技术视野、项目细节、理论知识，算法，开放性题，工作案例。

1. 细节追问： 可以确保问到你开始不懂或面试官开始不懂为止，这样可以大大延展题目的区分度和深度，知道你的实际能力。因为这种关联知识是长时期的学习，绝对不是临时记得住的。

1. 回答问题再棒，面试官（可能是你面试职位的直接领导），会考虑我要不要这个人做我的同事？所以态度很重要。（感觉更像是相亲）

1. 资深的工程师能把absolute和relative弄混，这样的人不要也罢，因为团队需要的是：你这个人具有可以依靠的才能（靠谱）。



**前端开发面试知识点大纲：**

	HTML&CSS：
		对Web标准的理解、浏览器内核差异、兼容性、hack、CSS基本功：布局、盒子模型、选择器优先级及使用、HTML5、CSS3、移动端

	JavaScript：
        数据类型、面向对象、继承、闭包、插件、作用域、跨域、原型链、模块化、自定义事件、内存泄漏、事件机制、异步装载回调、模板引擎、Nodejs、JSON、ajax等。

	其他：
       HTTP、WEB安全、正则、优化、重构、响应式、团队协作、可维护、SEO、UED、架构、职业生涯


作为一名前端工程师，**无论工作年头长短都应该必须掌握的知识点**：

此条由 王子墨 发表在 [前端随笔](http://julying.com/blog/front-end-engineers-must-master-knowledge/)

		1、DOM结构 —— 两个节点之间可能存在哪些关系以及如何在节点之间任意移动。

		2、DOM操作  ——如何添加、移除、移动、复制、创建和查找节点等。

		3、事件    —— 如何使用事件，以及IE和标准DOM事件模型之间存在的差别。

		4、XMLHttpRequest —— 这是什么、怎样完整地执行一次GET请求、怎样检测错误。

		5、严格模式与混杂模式 —— 如何触发这两种模式，区分它们有何意义。

		6、盒模型 —— 外边距、内边距和边框之间的关系，及IE8以下版本的浏览器中的盒模型

		7、块级元素与行内元素 —— 怎么用CSS控制它们、以及如何合理的使用它们

		8、浮动元素——怎么使用它们、它们有什么问题以及怎么解决这些问题。

		9、HTML与XHTML——二者有什么区别，你觉得应该使用哪一个并说出理由。

		10、JSON  —— 作用、用途、设计结构。




**备注：**

根据自己需要选择性阅读，面试题是对理论知识的总结，让自己学会应该如何表达。

资料答案不够正确和全面，**欢迎补充**答案、题目；最好是现在网上没有的。

格式不断修改更新中。


## <a name='html'>HTML</a>

- Doctype作用? 严格模式与混杂模式如何区分？它们有何意义?

		（1）、<!DOCTYPE> 声明位于文档中的最前面，处于 <html> 标签之前。告知浏览器的解析器，
              用什么文档类型 规范来解析这个文档。

		（2）、严格模式的排版和 JS 运作模式是  以该浏览器支持的最高标准运行。

		（3）、在混杂模式中，页面以宽松的向后兼容的方式显示。模拟老式浏览器的行为以防止站点无法工作。

		（4）、DOCTYPE不存在或格式不正确会导致文档以混杂模式呈现。

- 行内元素有哪些？块级元素有哪些？ 空(void)元素有那些？

		（1）CSS规范规定，每个元素都有display属性，确定该元素的类型，每个元素都有默认的display值，
		  比如div默认display属性值为“block”，成为“块级”元素；
		  span默认display属性值为“inline”，是“行内”元素。

		（2）行内元素有：a b span img input select strong（强调的语气）
		 块级元素有：div ul ol li dl dt dd h1 h2 h3 h4…p

		（3）知名的空元素：
		<br> <hr> <img> <input> <link> <meta>
		鲜为人知的是：
		<area> <base> <col> <command> <embed> <keygen> <param> <source> <track> <wbr>


- link 和@import 的区别是？


		（1）link属于XHTML标签，而@import是CSS提供的;

		（2）页面被加载的时，link会同时被加载，而@import引用的CSS会等到页面被加载完再加载;

		（3）import只在IE5以上才能识别，而link是XHTML标签，无兼容问题;

		（4）link方式的样式的权重 高于@import的权重.

- 浏览器的内核分别是什么?

	     * IE浏览器的内核Trident、Mozilla的Gecko、Chrome的Blink（WebKit的分支）、Opera内核原为Presto，现为Blink；


- 常见兼容性问题？

	    * png24位的图片在iE6浏览器上出现背景，解决方案是做成PNG8.

		* 浏览器默认的margin和padding不同。解决方案是加一个全局的*{margin:0;padding:0;}来统一。

		* IE6双边距bug:块属性标签float后，又有横行的margin情况下，在ie6显示margin比设置的大。

		  浮动ie产生的双倍距离 #box{ float:left; width:10px; margin:0 0 0 100px;}

	     这种情况之下IE会产生20px的距离，解决方案是在float的标签样式控制中加入 ——_display:inline;将其转化为行内属性。(_这个符号只有ie6会识别)

		  渐进识别的方式，从总体中逐渐排除局部。

		  首先，巧妙的使用“\9”这一标记，将IE游览器从所有情况中分离出来。
		  接着，再次使用“+”将IE8和IE7、IE6分离开来，这样IE8已经独立识别。

          css
	          .bb{
	           background-color:#f1ee18;/*所有识别*/
	          .background-color:#00deff\9; /*IE6、7、8识别*/
	          +background-color:#a200ff;/*IE6、7识别*/
	          _background-color:#1e0bd1;/*IE6识别*/
	          }

		*  IE下,可以使用获取常规属性的方法来获取自定义属性,
		   也可以使用getAttribute()获取自定义属性;
           Firefox下,只能使用getAttribute()获取自定义属性.
           解决方法:统一通过getAttribute()获取自定义属性.

		* IE下,even对象有x,y属性,但是没有pageX,pageY属性;
          Firefox下,event对象有pageX,pageY属性,但是没有x,y属性.

		* 解决方法：（条件注释）缺点是在IE浏览器下可能会增加额外的HTTP请求数。

		* Chrome 中文界面下默认会将小于 12px 的文本强制按照 12px 显示,
		  可通过加入 CSS 属性 -webkit-text-size-adjust: none; 解决.

		超链接访问过后hover样式就不出现了 被点击访问过的超链接样式不在具有hover和active了解决方法是改变CSS属性的排列顺序:
	    L-V-H-A :  a:link {} a:visited {} a:hover {} a:active {}



- html5有哪些新特性、移除了那些元素？如何处理HTML5新标签的浏览器兼容问题？如何区分 HTML 和
HTML5？


		* HTML5 现在已经不是 SGML 的子集，主要是关于图像，位置，存储，多任务等功能的增加。

		* 绘画 canvas
		  用于媒介回放的 video 和 audio 元素
		  本地离线存储 localStorage 长期存储数据，浏览器关闭后数据不丢失；
          sessionStorage 的数据在浏览器关闭后自动删除

		  语意化更好的内容元素，比如 article、footer、header、nav、section
		  表单控件，calendar、date、time、email、url、search
		  新的技术webworker, websockt, Geolocation

		* 移除的元素

		纯表现的元素：basefont，big，center，font, s，strike，tt，u；

		对可用性产生负面影响的元素：frame，frameset，noframes；

	    支持HTML5新标签：

		* IE8/IE7/IE6支持通过document.createElement方法产生的标签，
		  可以利用这一特性让这些浏览器支持HTML5新标签，

          浏览器支持新标签后，还需要添加标签默认的样式：

		* 当然最好的方式是直接使用成熟的框架、使用最多的是html5shim框架
		   <!--[if lt IE 9]>
		   <script> src="http://html5shim.googlecode.com/svn/trunk/html5.js"</script>
		   <![endif]-->
		如何区分： DOCTYPE声明\新增的结构元素\功能元素


- 语义化的理解？

		用正确的标签做正确的事情！
	    html语义化就是让页面的内容结构化，便于对浏览器、搜索引擎解析；
	    在没有样式CCS情况下也以一种文档格式显示，并且是容易阅读的。
	    搜索引擎的爬虫依赖于标记来确定上下文和各个关键字的权重，利于 SEO。
	    使阅读源代码的人对网站更容易将网站分块，便于阅读维护理解。

- HTML5的离线储存？

	    localStorage    长期存储数据，浏览器关闭后数据不丢失；
        sessionStorage  数据在浏览器关闭后自动删除。

- (写)描述一段语义的html代码吧。

	    （HTML5中新增加的很多标签（如：<article>、<nav>、<header>和<footer>等）
         就是基于语义化设计原则）
			< div id="header">
			< h1>标题< /h1>
			< h2>专注Web前端技术< /h2>
			< /div>


- iframe有那些缺点？

		*iframe会阻塞主页面的Onload事件；

		*iframe和主页面共享连接池，而浏览器对相同域的连接有限制，所以会影响页面的并行加载。
        使用iframe之前需要考虑这两个缺点。如果需要使用iframe，最好是通过javascript
        动态给iframe添加src属性值，这样可以可以绕开以上两个问题。
 
- HTML5的form如何关闭自动完成功能？

		给不想要提示的 form 或下某个input 设置为 autocomplete=off。


- 请描述一下 cookies，sessionStorage 和 loc
- Storage 的区别？

 		cookie在浏览器和服务器间来回传递。 sessionStorage和localStorage不会
		sessionStorage和localStorage的存储空间更大；
		sessionStorage和localStorage有更多丰富易用的接口；
		sessionStorage和localStorage各自独立的存储空间；

- 如何实现浏览器内多个标签页之间的通信? (阿里)

		调用localstorge、cookies等本地存储方式

- webSocket如何兼容低浏览器？(阿里)

		Adobe Flash Socket 、 ActiveX HTMLFile (IE) 、 基于 multipart 编码发送 XHR 、 基于长轮询的 XHR


## <a name='css'>CSS</a>

- 介绍一下CSS的盒子模型？

		（1）有两种， IE 盒子模型、标准 W3C 盒子模型；IE的content部分包含了 border 和 pading;

		（2）盒模型： 内容(content)、填充(padding)、边界(margin)、 边框(border).



- CSS 选择符有哪些？哪些属性可以继承？优先级算法如何计算？ CSS3新增伪类有那些？

		*   1.id选择器（ # myid）
			2.类选择器（.myclassname）
			3.标签选择器（div, h1, p）
			4.相邻选择器（h1 + p）
			5.子选择器（ul < li）
			6.后代选择器（li a）
			7.通配符选择器（ * ）
			8.属性选择器（a[rel = "external"]）
			9.伪类选择器（a: hover, li: nth - child）

		*   可继承的样式： font-size font-family color, UL LI DL DD DT;

		*   不可继承的样式：border padding margin width height ;

		*   优先级就近原则，同权重情况下样式定义最近者为准;

		*   载入样式以最后载入的定位为准;

	优先级为:

		   !important >  id > class > tag

		   important 比 内联优先级高

	CSS3新增伪类举例：

		p:first-of-type	选择属于其父元素的首个 <p> 元素的每个 <p> 元素。
		p:last-of-type	选择属于其父元素的最后 <p> 元素的每个 <p> 元素。
        p:only-of-type	选择属于其父元素唯一的 <p> 元素的每个 <p> 元素。
		p:only-child	选择属于其父元素的唯一子元素的每个 <p> 元素。
		p:nth-child(2)	选择属于其父元素的第二个子元素的每个 <p> 元素。
 	    :enabled  :disabled 控制表单控件的禁用状态。
		:checked        单选框或复选框被选中。


- 如何居中div？如何居中一个浮动元素？


	*  给div设置一个宽度，然后添加margin:0 auto属性

			div{
				width:200px;
				margin:0 auto;
			 }


	*  居中一个浮动元素

			  确定容器的宽高 宽500 高 300 的层
			  设置层的外边距

		     .div {
			  Width:500px ; height:300px;//高度可以不设
			  Margin: -150px 0 0 -250px;
			  position:relative;相对定位
              background-color:pink;//方便看效果
			  left:50%;
			  top:50%;
			}


- 列出display的值，说明他们的作用。position的值， relative和absolute定位原点是？


	      1.
	      block 象块类型元素一样显示。
		  none 缺省值。象行内元素类型一样显示。
		  inline-block 象行内元素一样显示，但其内容象块类型元素一样显示。
		  list-item 象块类型元素一样显示，并添加样式列表标记。

	      2.
		  *absolute
				生成绝对定位的元素，相对于 static 定位以外的第一个父元素进行定位。

		  *fixed （老IE不支持）
				生成绝对定位的元素，相对于浏览器窗口进行定位。

		  *relative
				生成相对定位的元素，相对于其正常位置进行定位。

		  * static	默认值。没有定位，元素出现在正常的流中
		  *（忽略 top, bottom, left, right z-index 声明）。

		  * inherit	规定从父元素继承 position 属性的值。

- CSS3有哪些新特性？

  		  CSS3实现圆角（border-radius:8px），阴影（box-shadow:10px），
		  对文字加特效（text-shadow、），线性渐变（gradient），旋转（transform）
          transform:rotate(9deg) scale(0.85,0.90) translate(0px,-30px) skew(-9deg,0deg);//旋转,缩放,定位,倾斜
          增加了更多的CSS选择器  多背景 rgba

- 一个满屏 品 字布局 如何设计?

- 经常遇到的CSS的兼容性有哪些？原因，解决方法是什么？



- 为什么要初始化CSS样式。

		- 因为浏览器的兼容问题，不同浏览器对有些标签的默认值是不同的，如果没对CSS初始化往往会出现浏览器之间的页面显示差异。

		- 当然，初始化样式会对SEO有一定的影响，但鱼和熊掌不可兼得，但力求影响最小的情况下初始化。

		*最简单的初始化方法就是： * {padding: 0; margin: 0;} （不建议）

		淘宝的样式初始化：
		body, h1, h2, h3, h4, h5, h6, hr, p, blockquote, dl, dt, dd, ul, ol, li, pre, form, fieldset, legend, button, input, textarea, th, td { margin:0; padding:0; }
		body, button, input, select, textarea { font:12px/1.5tahoma, arial, \5b8b\4f53; }
		h1, h2, h3, h4, h5, h6{ font-size:100%; }
		address, cite, dfn, em, var { font-style:normal; }
		code, kbd, pre, samp { font-family:couriernew, courier, monospace; }
		small{ font-size:12px; }
		ul, ol { list-style:none; }
		a { text-decoration:none; }
		a:hover { text-decoration:underline; }
		sup { vertical-align:text-top; }
		sub{ vertical-align:text-bottom; }
		legend { color:#000; }
		fieldset, img { border:0; }
		button, input, select, textarea { font-size:100%; }
		table { border-collapse:collapse; border-spacing:0; }



- absolute的containing block计算方式跟正常流有什么不同？

- position跟display、margin collapse、overflow、float这些特性相互叠加后会怎么样？

- 对BFC规范的理解？

		（W3C CSS 2.1 规范中的一个概念,它决定了元素如何对其内容进行定位,以及与其他元素的关 系和相互作用。）
- css定义的权重

		以下是权重的规则：标签的权重为1，class的权重为10，id的权重为100，以下例子是演示各种定义的权重值：

		/*权重为1*/
		div{
		}
		/*权重为10*/
		.class1{
		}
		/*权重为100*/
		#id1{
		}
		/*权重为100+1=101*/
		#id1 div{
		}
		/*权重为10+1=11*/
		.class1 div{
		}
		/*权重为10+10+1=21*/
		.class1 .class2 div{
		}

		如果权重相同，则最后定义的样式会起作用，但是应该避免这种情况出现


- 解释下浮动和它的工作原理？清除浮动的技巧

- 用过媒体查询，针对移动端的布局吗？

- 使用 CSS 预处理器吗？喜欢那个？

		SASS

- 如果需要手动写动画，你认为最小时间间隔是多久，为什么？（阿里）

		多数显示器默认频率是60Hz，即1秒刷新60次，所以理论上最小间隔为1/60＊1000ms ＝ 16.7ms


- display:inline-block 什么时候会显示间隙？(携程)

		移除空格、使用margin负值、使用font-size:0、letter-spacing、word-spacing



## <a name='js'>JavaScript</a>

-  JavaScript原型，原型链 ? 有什么特点？

-  eval是做什么的？

		它的功能是把对应的字符串解析成JS代码并运行；
		应该避免使用eval，不安全，非常耗性能（2次，一次解析成js语句，一次执行）。

-  null，undefined 的区别？

-  写一个通用的事件侦听器函数。

			// event(事件)工具集，来源：github.com/markyun
			markyun.Event = {
				// 页面加载完成后
				readyEvent : function(fn) {
					if (fn==null) {
						fn=document;
					}
					var oldonload = window.onload;
					if (typeof window.onload != 'function') {
						window.onload = fn;
					} else {
						window.onload = function() {
							oldonload();
							fn();
						};
					}
				},
				// 视能力分别使用dom0||dom2||IE方式 来绑定事件
				// 参数： 操作的元素,事件名称 ,事件处理程序
				addEvent : function(element, type, handler) {
					if (element.addEventListener) {
						//事件类型、需要执行的函数、是否捕捉
						element.addEventListener(type, handler, false);
					} else if (element.attachEvent) {
						element.attachEvent('on' + type, function() {
							handler.call(element);
						});
					} else {
						element['on' + type] = handler;
					}
				},
				// 移除事件
				removeEvent : function(element, type, handler) {
					if (element.removeEventListener) {
						element.removeEventListener(type, handler, false);
					} else if (element.datachEvent) {
						element.detachEvent('on' + type, handler);
					} else {
						element['on' + type] = null;
					}
				},
				// 阻止事件 (主要是事件冒泡，因为IE不支持事件捕获)
				stopPropagation : function(ev) {
					if (ev.stopPropagation) {
						ev.stopPropagation();
					} else {
						ev.cancelBubble = true;
					}
				},
				// 取消事件的默认行为
				preventDefault : function(event) {
					if (event.preventDefault) {
						event.preventDefault();
					} else {
						event.returnValue = false;
					}
				},
				// 获取事件目标
				getTarget : function(event) {
					return event.target || event.srcElement;
				},
				// 获取event对象的引用，取到事件的所有信息，确保随时能使用event；
				getEvent : function(e) {
					var ev = e || window.event;
					if (!ev) {
						var c = this.getEvent.caller;
						while (c) {
							ev = c.arguments[0];
							if (ev && Event == ev.constructor) {
								break;
							}
							c = c.caller;
						}
					}
					return ev;
				}
			};



-  Node.js的适用场景？

		高并发、聊天、实时消息推送

-  介绍js的基本数据类型。

		number,string,boolean,object,undefined

-  Javascript如何实现继承？

		通过原型和构造器

-  ["1", "2", "3"].map(parseInt) 答案是多少？

		 [1, NaN, NaN] 因为 parseInt 需要两个参数 (val, radix)，其中 radix 表示解析时用的基数。map 传了 3 个 (element, index, array)，对应的 radix 不合法导致解析失败。

-  如何创建一个对象? （画出此对象的内存图）

		  function Person(name, age) {
		    this.name = name;
		    this.age = age;
		    this.sing = function() { alert(this.name) }
		  }


-  谈谈This对象的理解。

		this是js的一个关键字，随着函数使用场合不同，this的值会发生变化。

	    但是有一个总原则，那就是this指的是调用函数的那个对象。

	    this一般情况下：是全局对象Global。 作为方法调用，那么this就是指这个对象

-  事件是？IE与火狐的事件机制有什么区别？ 如何阻止冒泡？

		 1. 我们在网页中的某个操作（有的操作对应多个事件）。例如：当我们点击一个按钮就会产生一个事件。是可以被 JavaScript 侦测到的行为。
		 2. 事件处理机制：IE是事件冒泡、火狐是 事件捕获；
		 3. ev.stopPropagation();

-  什么是闭包（closure），为什么要用它？


		执行say667()后,say667()闭包内部变量会存在,而闭包内部函数的内部变量不会存在.使得Javascript的垃圾回收机制GC不会收回say667()所占用的资源，因为say667()的内部函数的执行需要依赖say667()中的变量。这是对闭包作用的非常直白的描述.

		  function say667() {
			// Local variable that ends up within closure
			var num = 666;
			var sayAlert = function() { alert(num); }
			num++;
			return sayAlert;
		}

		 var sayAlert = say667();
		 sayAlert()//执行结果应该弹出的667


-  "use strict";是什么意思 ? 使用它的好处和坏处分别是什么？

-  如何判断一个对象是否属于某个类？



 		  使用instanceof （待完善）

	       if(a instanceof Person){
	           alert('yes');
	       }
-  new操作符具体干了什么呢?

			 1、创建一个空对象，并且 this 变量引用该对象，同时还继承了该函数的原型。
	  	  	 2、属性和方法被加入到 this 引用的对象中。
	 		 3、新创建的对象由 this 所引用，并且最后隐式的返回 this 。

		var obj  = {};
		obj.__proto__ = Base.prototype;
		Base.call(obj);

-  Javascript中，有一个函数，执行时对象查找时，永远不会去查找原型，这个函数是？

		hasOwnProperty

-  JSON 的了解？

		JSON(JavaScript Object Notation) 是一种轻量级的数据交换格式。
		它是基于JavaScript的一个子集。数据格式简单, 易于读写, 占用带宽小
        {"age":"12", "name":"back"}

-  js延迟加载的方式有哪些？

		defer和async、动态创建DOM方式（用得最多）、按需异步载入js


-  ajax 是什么?

-  同步和异步的区别?

-  如何解决跨域问题?

		jsonp、 iframe、window.name、window.postMessage、服务器上设置代理页面
-  模块化怎么做？



	 [ 立即执行函数](http://benalman.com/news/2010/11/immediately-invoked-function-expression/),不暴露私有成员

		    var module1 = (function(){
		    　　　　var _count = 0;
		    　　　　var m1 = function(){
		    　　　　　　//...
		    　　　　};
		    　　　　var m2 = function(){
		    　　　　　　//...
		    　　　　};
		    　　　　return {
		    　　　　　　m1 : m1,
		    　　　　　　m2 : m2
		    　　　　};
		    　　})();

-  AMD（Modules/Asynchronous-Definition）、CMD（Common Module Definition）规范区别？

-  异步加载的方式有哪些？


	      (1) defer，只支持IE

	      (2) async：

	      (3) 创建script，插入到DOM中，加载完毕后callBack

- documen.write和 innerHTML的区别

document.write只能重绘整个页面

innerHTML可以重绘页面的一部分


-  .call() 和 .apply() 的区别？


		  例子中用 add 来替换 sub，add.call(sub,3,1) == add(3,1) ，所以运行结果为：alert(4);

		  注意：js 中的函数其实是对象，函数名是对 Function 对象的引用。

			function add(a,b)
			{
			    alert(a+b);
			}

			function sub(a,b)
			{
			    alert(a-b);
			}

			add.call(sub,3,1);

-  Jquery与jQuery UI 有啥区别？


		*jQuery是一个js库，主要提供的功能是选择器，属性修改和事件绑定等等。

		*jQuery UI则是在jQuery的基础上，利用jQuery的扩展性，设计的插件。
         提供了一些常用的界面元素，诸如对话框、拖动行为、改变大小行为等等


-  JQuery的源码看过吗？能不能简单说一下它的实现原理？

-  jquery 中如何将数组转化为json字符串，然后再转化回来？


jQuery中没有提供这个功能，所以你需要先编写两个jQuery的扩展：

		$.fn.stringifyArray = function(array) {
		    return JSON.stringify(array)
		}

		$.fn.parseArray = function(array) {
		    return JSON.parse(array)
		}

		然后调用：
		$("").stringifyArray(array)


-  针对 jQuery 的优化方法？

		*基于Class的选择性的性能相对于Id选择器开销很大，因为需遍历所有DOM元素。

		*频繁操作的DOM，先缓存起来再操作。用Jquery的链式调用更好。
         比如：var str=$("a").attr("href");

		*for (var i = size; i < arr.length; i++) {}
         for 循环每一次循环都查找了数组 (arr) 的.length 属性，在开始循环的时候设置一个变量来存储这个数字，可以让循环跑得更快：
         for (var i = size, length = arr.length; i < length; i++) {}


-  JavaScript中的作用域与变量声明提升？

-  如何编写高性能的Javascript？

-  那些操作会造成内存泄漏？



	    内存泄漏指任何对象在您不再拥有或需要它之后仍然存在。
        垃圾回收器定期扫描对象，并计算引用了每个对象的其他对象的数量。如果一个对象的引用数量为 0（没有其他对象引用过该对象），或对该对象的惟一引用是循环的，那么该对象的内存即可回收。

        setTimeout 的第一个参数使用字符串而非函数的话，会引发内存泄漏。
		闭包、控制台日志、循环（在两个对象彼此引用且彼此保留时，就会产生一个循环）

-  JQuery一个对象可以同时绑定多个事件，这是如何实现的？

- 如何判断当前脚本运行在浏览器还是node环境中？（阿里）

		通过判断Global对象是否为window，如果不为window，当前脚本没有运行在浏览器中


## <a name='other'>其他问题</a>


- 你遇到过比较难的技术问题是？你是如何解决的？

- 常使用的库有哪些？常用的前端开发工具？开发过什么应用或组件？

- 页面重构怎么操作？

- 列举IE 与其他浏览器不一样的特性？

- 99%的网站都需要被重构是那本书上写的？

- 什么叫优雅降级和渐进增强？

- WEB应用从服务器主动推送Data到客户端有那些方式？

- 对Node的优点和缺点提出了自己的看法？


		*（优点）因为Node是基于事件驱动和无阻塞的，所以非常适合处理并发请求，
          因此构建在Node上的代理服务器相比其他技术实现（如Ruby）的服务器表现要好得多。
		  此外，与Node代理服务器交互的客户端代码是由javascript语言编写的，
	      因此客户端和服务器端都用同一种语言编写，这是非常美妙的事情。

		*（缺点）Node是一个相对新的开源项目，所以不太稳定，它总是一直在变，
          而且缺少足够多的第三方库支持。看起来，就像是Ruby/Rails当年的样子。


- 你有哪些性能优化的方法？


		 （看雅虎14条性能优化原则）。

		  （1） 减少http请求次数：CSS Sprites, JS、CSS源码压缩、图片大小控制合适；网页Gzip，CDN托管，data缓存 ，图片服务器。

		  （2） 前端模板 JS+数据，减少由于HTML标签导致的带宽浪费，前端用变量保存AJAX请求结果，每次操作本地变量，不用请求，减少请求次数

		  （3） 用innerHTML代替DOM操作，减少DOM操作次数，优化javascript性能。

		  （4） 当需要设置的样式很多时设置className而不是直接操作style。

		  （5） 少用全局变量、缓存DOM节点查找的结果。减少IO读取操作。

		  （6） 避免使用CSS Expression（css表达式)又称Dynamic properties(动态属性)。

		  （7） 图片预加载，将样式表放在顶部，将脚本放在底部  加上时间戳。

		  （8） 避免在页面的主体布局中使用table，table要等其中的内容完全下载之后才会显示出来，显示比div+css布局慢。

- http状态码有那些？分别代表是什么意思？

		100-199 用于指定客户端应相应的某些动作。
		200-299 用于表示请求成功。
		300-399 用于已经移动的文件并且常被包含在定位头信息中指定新的地址信息。
		400-499 用于指出客户端的错误。400	1、语义有误，当前请求无法被服务器理解。401	当前请求需要用户验证 403	服务器已经理解请求，但是拒绝执行它。
		500-599 用于支持服务器错误。 503 – 服务不可用

- 一个页面从输入 URL 到页面加载显示完成，这个过程中都发生了什么？（流程说的越详细越好）


			查找浏览器缓存
		    DNS解析、查找该域名对应的IP地址、重定向（301）、发出第二个GET请求
		    进行HTTP协议会话
		    客户端发送报头(请求报头)
		    服务器回馈报头(响应报头)
		    html文档开始下载
		    文档树建立，根据标记请求所需指定MIME类型的文件
		    文件显示
			[
			浏览器这边做的工作大致分为以下几步：

			加载：根据请求的URL进行域名解析，向服务器发起请求，接收文件（HTML、JS、CSS、图象等）。

			解析：对加载到的资源（HTML、JS、CSS等）进行语法解析，建议相应的内部数据结构（比如HTML的DOM树，JS的（对象）属性表，CSS的样式规则等等）
			}
- 除了前端以外还了解什么其它技术么？你最最厉害的技能是什么？

- 你常用的开发工具是什么，为什么？

- 对前端界面工程师这个职位是怎么样理解的？它的前景会怎么样？

		     前端是最贴近用户的程序员，比后端、数据库、产品经理、运营、安全都近。
			1、实现界面交互
			2、提升用户体验
			3、有了Node.js，前端可以实现服务端的一些事情


		前端是最贴近用户的程序员，前端的能力就是能让产品从 90分进化到 100 分，甚至更好，

         参与项目，快速高质量完成实现效果图，精确到1px；

         与团队成员，UI设计，产品经理的沟通；

         做好的页面结构，页面重构和用户体验；

         处理hack，兼容、写出优美的代码格式；

         针对服务器的优化、拥抱最新前端技术。
- 加班的看法？


   		加班就像借钱，原则应当是------救急不救穷



- 平时如何管理你的项目？

				先期团队必须确定好全局样式（globe.css），编码模式(utf-8) 等；

				编写习惯必须一致（例如都是采用继承式的写法，单样式都写成一行）；

				标注样式编写人，各模块都及时标注（标注关键样式调用的地方）；

				页面进行标注（例如 页面 模块 开始和结束）；

				CSS跟HTML 分文件夹并行存放，命名都得统一（例如style.css）；

				JS 分文件夹存放 命名以该JS功能为准的英文翻译。

				图片采用整合的 images.png png8 格式文件使用 尽量整合在一起使用方便将来的管理
- 如何设计突发大规模并发架构？


- 说说最近最流行的一些东西吧？常去哪些网站？

			Node.js、Mongodb、npm、MVVM、MEAN、three.js

- 移动端（Android IOS）怎么做好用户体验?

			清晰的视觉纵线、信息的分组、极致的减法、
			利用选择代替输入、标签及文字的排布方式、
			依靠明文确认密码、合理的键盘利用、

- 你在现在的团队处于什么样的角色，起到了什么明显的作用？

- 你认为怎样才是全端工程师（Full Stack developer）？


- 介绍一个你最得意的作品吧？

- 你的优点是什么？缺点是什么？

- 如何管理前端团队?


- 最近在学什么？能谈谈你未来3，5年给自己的规划吗？

- 想问公司的问题？

			问公司问题：
			目前关注哪些最新的Web前端技术（未来的发展方向）？
			前端团队如何工作的（实现一个产品的流程）？
			公司的薪资结构是什么样子的？


## <a name='web'>优质网站推荐</a>

1. 极客标签：		 http://www.gbtags.com/


2. 码农周刊：		 http://weekly.manong.io/issues/


3. 前端周刊：		 http://www.feweekly.com/issues


9. 极客头条： 	 http://geek.csdn.net/


3. Startup News：http://news.dbanotes.net/


4. Hacker News： https://news.ycombinator.com/news


7. InfoQ：  		 http://www.infoq.com/


10. w3cplus：     http://www.w3cplus.com/


10. Stack Overflow： http://stackoverflow.com/


6. Atp：  		 http://atp-posts.b0.upaiyun.com/posts/



###last updated:  2015-03-25

	爱机车、爱骑行、爱旅行、爱摄影、爱阅读的理想青年，前端开发攻城师。

	我的微博：http://weibo.com/920802999
