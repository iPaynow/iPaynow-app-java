现在支付-中小开发者商户服务端接口服务接入指南

2014-08-21

==== 基本要求 ====

    JDK 1.5及以上版本


==== 文件结构 ====

<devplat_mch_sdk>
  │
  ├src┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈类文件夹
  │  │
  │  ├com.ipaynow.filter
  │  │  │
  │  │  └CharacterEncodingFilter.java┈┈┈┈┈┈Web字符过滤器
  │  │
  │  ├com.ipaynow.utils
  │  │  │
  │  │  ├FormDateReportConvertor.java┈┈┈ 表单数据型报文数据转换器
  │  │  │
  │  │  ├HttpClientUtil.java┈┈┈┈┈Http协议客户端工具类
  │  │  │
  │  │  ├MD5.java┈┈┈┈ MD5加密基本工具类
  │  │  │
  │  │  └MD5Facade.java┈┈┈┈┈ MD5门面接口工具
  │  │
  │  ├com.ipaynow.notify
  │  │  │
  │  │  └MchNotifyServlet.java┈┈┈┈┈ 商户接收现在支付订单支付结果通知的Servlet
  │  │
  │  └com.ipaynow.query
  │      │
  │      ├MchQuery.java┈┈┈┈┈┈ 商户调用 现在支付服务端 订单查询接口 实例类
  │      
  │
  ├WebRoot┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈WEB根， 可以直接放在Tomcat上进行运行查看效果
  │  │  
  │  │
  │  └WEB-INF
  │      |
  │      |-lib（如果JAVA项目中包含这些jar包，则不需要导入）
  │      |  │
  │      |  ├commons-logging-1.1.1.jar
  │      |  │
  │      |  ├httpclient-4.1.2.jar
  │      |  │
  │      |  └httpcore-4.1.2.jar| 
  │      |
  |       |-web.xml ------配置了字符过滤器和  商户接收现在支付通知的Servlet
  |
  |-readme.txt ┈┈┈┈┈┈┈┈┈┈┈使用说明文本


==== 注意事项 ====

    请修改配置文件：src/config.properties    里面是中小开发者商户自己 在现在支付平台上注册的应用的ID--appId   应用对应的md5Key   以及现在支付的服务URL

    本代码示例中获取远程HTTP信息使用的是httpclient-4.1.2 版本的第三方jar包。
    如果您不想使用该方式实现获取远程HTTP功能，可用其他方式替代，此时需您自行编写代码。

