# <center><span style="color:#5c46b3">周广明_JavaEE工程师简历</span></center>

------


# <span style="color:#5c46b3">个人信息</span>

 - 周广明/男/1995 
 - 本科/南昌航空大学 软件工程
 - 专科/江西生物科技职业学院 软件技术
 - 工作年限：3年
 - 技术博客：https://blog.csdn.net/GMingZhou
 - Github：https://github.com/zgmFlashy
 - 期望职位：Java高级程序员，应用架构师
 - 期望薪资：面议
 - 期望城市：深圳

---


# <span style="color:#5c46b3">专业技能</span>

<h4>&nbsp;以下均为我熟练使用的技能</h4>

- Web开发：Java/JavaEE/Servlet/JSP/Node
- Web框架：Spring/Struts/SpringMVC/SpringBoot/Spring Cloud/Hibernate/Mybatis
- Web中间件：Tomcat/Nginx/Redis/Dubbo/ZooKeeper/RabbitMQ/WebService
- 前端框架：JavaScript/JQuery/Ajax/Bootstrap/Vue/ElementUI/HTML/CSS
- 开发工具：IDEA/Eclipse/VS Code/Maven/Gradle/UML
- 数据库相关：MySQL/Oracle/SQL Service
- 版本管理、文档和自动化部署工具：Git/SVN/Swagger/Markdown/Jenkins/Docker
- 单元测试：Junit4/Mock/SoapUI/Postman
- 操作系统：Linux/Windows

---


# <span style="color:#5c46b3">工作经历</span>

##  [中兴软件技术(南昌)有限公司][1]（2015年10月 ~ 2016年1月）

工作描述：
职位是对外事业部的Java开发工程师，主要负责[蓝凌][2]项目的维护和开发。
工作期间参与需求的调研、分析评估和方案输出，参与项目代码的编写、测试、部署及bug修复。

## [深圳市蓝凌软件股份有限公司][2]（2016年1月 ~ 2019年2月）

工作描述：
职位是大客户部的开发顾问，为[国内500强企业][3]服务。
先后参与东风汽车、华星光电、佰仟金融、安信证券、民生银行、华彬集团、嘉宝莉、宏珏、国信证券、深圳教育局
等公司的OA系统的搭建、改造、系统对接、升级和维护工作。

---


# <span style="color:#5c46b3">项目经历</span>

---

### <span style="color:#08c">蓝凌EKP系统简介</span>

<span style="color:#0b74a9">EKP 是企业知识门户（Enterprise Knowledge Portal，EKP）的简称。它是基于知识管理的企业协同办公平台，是企业员工日常工作所涉及相关的主题内容的统一入口。通过它了解当天的最新消息，工作内容及所需的知识等。实时地与其他成员取得联系、找到能提供帮助的专家或知识。知识门户是企业实现高效管理的重要工具和手段。</span>
<br/><br/>![蓝凌][4]<br/><br/>
<span style="color:#0b74a9">蓝凌EKP系统是由成熟的SSH框架搭建的SOA架构系统，平台为通用开发平台。其中核心服务包括通过AOP实现的插件工厂、基于JBPM流程引擎改造的LBPM流程引擎、基于SVG实现的自定义表单系统、自定义公式、通用岗位和角色线，常用服务有如版本机制、标签机制、导出导入、点评机制、订阅机制、定时任务、附件机制、权限机制、收搜机制、通知机制、推荐机制、通知机制...... &nbsp;通过建模工具设计好模型，可一键生成模块基础代码，模块之间相互独立，是一套完善的企业系统开发平台，类似于现在流行的 Spring Cloud工具集。</span>

---

### 华星移动门户系统
华星光电是TCL集团旗下的显示器生产厂家，除了为TCL提供生产时自己也有海量的国内外生产订单。华星门户系统是对本企业员工、供应商、客户开放的一个门户平台，每天都有大量的业务在上面处理。
华星移动门户系统核心是以蓝凌KEP为后台支持，移动端系统由自己团队负责开发。系统设计为前后端分离项目，前端采用 HTML5 + Bootstrap + AngularJS + Node 构建，后台为基于SpringBoot的 Eureka + Hystrix + Zuul + Feign微服务架构。移动端系统通过RabbitMQ与EKP交互数据，EKP本身支持WebService服务调用，为适配移动端系统也做了通过Dubbo的调用实现。
<div style="margin-top: 10px;"></div>
这个项目我主要负责后台通用流程审批（机器自动审批）系统的开发，流程审批是个大模块，几乎所有业务都要走流程，系统之前是只对企业员工开放，客户和供应商之间的所有业务都有华星这边处理，大部分流程都是人工审批，后来流程模块的业务重新整理了一遍，一分为二，一部分继续走人工，大部分走机器了。由于系统对外开放这时对系统的性能也提出了新的挑战。业务量大时EKP系统需要控制业务流量，EKP做了之前就做了3台机器的集群，现在加到了6台机器，高峰期时，6台机器也显的有点吃力！于是就在负载均衡服务器上加了一层消息中间件用于限流和加强服务监控，业务处理为异步响应式处理。<br/>通过这两步，保证了系统的高可用性。💪

### 佰仟金融HR系统
本次项目是企业内部使用的HR系统，基于EKP平台的定制化开发，标准模块有新闻、待办、日程管理、会议管理、组织架构，组织架构数据同步于金蝶EAS。
定制化开发我负责的模块有入职、离职申请、试用期员工转正、调薪(职能)、异动申请五个表单的开发。业务方面由自己与佰仟那边的技术和人事直接沟通，技术方面是通过EKP自带的自定义表单系统和流程引擎，再加上权限机制，实现快速开发。
<div style="margin-top: 10px;"></div>
本系统属于小型系统，总体上简单，说难点的话有以下两个：
1. 采用自定义表单系统是当时最新的版本，可能是系统版本兼容原因，表单页面还有比较多的bug，很多时候都需要通过修改生成的源码来实现业务。
2. 组织架构同步耗时久！处理方案是 1.本地增加全量同步增量同步切换方法；2.通过消息中间件进行同步，改手动/定时任务模式为消息订阅模式。方法一主要是系统初始化时会用到，默认使用消息中间件，同步几乎无感知。
<br/>
关于消息中间件，之前一直是在理论和观望状态，实践之后对它有了更多的了解。实践出真知！👊

### 民生银行综合OA系统
此项目是EKP系统的二次迭代开发，本次升级客户要求替换门户所有的UI，由于蓝凌EKP的门户是通过组件拖拉拽方式配置出来的，所以此次工程量非常大！相当于再次封装系统组件，最大的问题就是组件JSP页面中包含的Java代码，JSP表达式、各组件间的层级关系，拿出来后重写很容易出错。
之后还负责了新闻、知识、论坛、消息模块PC端和移动端的缓存功能开发，改造之前系统的订阅号功能，将其从原来新闻模块中拆开，负责日程管理和收藏机制的接口开发，总结计划模块的定制开发。
最后还负责修改扫描出来的安全漏洞，银行的安全部门有专门的黑客，他们会不断的攻击我们的系统。
<div style="margin-top: 10px;"></div>
此次项目最大的收获是缓存系统的设计和使用，项目使用的是服务端缓存，缓存设计是本地缓存 + Redis。粒度拆分按功能，简单数据存本地一级缓存，对象类、集合类数据使用Redis存储。缓存结构设计了链表结构和树结构两种，更新策略是主动更新，可设置缓存的最小最大容量值，缓存没有被动失效功能，系统可动态维护内存缓存数量。
<br/>
做这个项目的期间真是个光荣岁月啊！连续上班一个月，几乎每天都是凌晨一两点回家的！😭

### 智慧园区系统
此系统是个办公园区管理系统，包括考勤管理、会议室申请、门禁管理、智慧食堂、智慧停车、公务用车、物品放行、物品报修等主要模块。项目是基于Spring Cloud的前后端分离项目。前端采用 HTML5 + Bootstrap + Vue + Node 构建，后台为Eureka + Ribbon + Hystrix + Zuul + Feign微服务架构。
项目中我主要负责物品报修模块，用户共有普通用户、维修工、物业管理三个角色，业务流程是普通用户发现问题，APP上保修 —> 分发到负责该区域的物业管理员 —> 管理员选维修工 —> 维修工接单 —> 完成订单—> 用户评价 —> 结束。
<div style="margin-top: 10px;"></div>
此业务有个难点就是物业部人员提交的申请与普通用户提交的申请审批流程不一致，由于这个业务是基于原系统改造的，数据库表沿用以前的表，数据结构有点复杂，判断用户角色、岗位和用户领导是个较麻烦事情，还有一点是小系统没有流程机制，纯靠代码控制业务逻辑走向！项目文档通过Swagger2接口测试工具生成。
<br/>
整个项目中比较有成就感的是给项目做了个代码生成工具，通过模板，数据库建模后可自动生成前后端通用代码。😍

---


# <span style="color:#5c46b3">自我评价</span>

 - 爱学习，爱阅读
 - 坚持早起、坚持锻炼
 - 热衷于公益活动，参加读书会、喜欢经典文化
 - 工作态度认真、刻苦，富有团队合作精神
 - 有上进心、学习能力强、能尽快适应新的环境及工作
 - 为人诚恳，积累了一定的开发经验，具有规范的编程习惯和严谨的编程风格

---


# <span style="color:#5c46b3">联系方式</span>

- <i class="icon-phone"></i> 手机：<a href="tel://17620469900">17620469900</a>
- <i class="icon-comments"></i> QQ/微信：<a href="tel://17620469900">614254327</a>
- <i class="icon-envelope"></i> Email：<a href="mailto:zhouguangming_sz@landray.com.cn">zhouguangming_sz@landray.com.cn</a>

---

# <span style="color:#5c46b3">附件下载</span>

- [周广明_JavaEE工程师简历(打印版).PDF][8]
- [周广明_JavaEE工程师简历(移动端查看).PNG][6]

---


# <span style="color:#5c46b3">致谢</span>
感谢您花时间阅读我的简历，期待能有机会和您共事。🌹 <p>&nbsp; <p><center>![扫一扫，加我抖音和微信！][5]</center></p><br/>

<!--佰仟金融是一家提供金融服务的公司，总部位于深圳。产品涵盖消费金融服务、汽车金融服务等。-->

  [1]: http://www.zte-s.com.cn
  [2]: http://www.landray.com.cn/index
  [3]: http://www.landray.com.cn/lanling
  [4]: http://39.108.110.187/logo.png
  [5]: http://39.108.110.187/dv2.jpg
  [6]: http://39.108.110.187/周广明_JavaEE工程师简历.PNG
  [8]: http://39.108.110.187/周广明_JavaEE工程师简历_打印.PDF
