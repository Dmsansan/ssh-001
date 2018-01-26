Struts2+spring+4Hibernate5整合

1、Struts2整合
	struts2框架具有MVC的作用，url访问控制器Action或者Action里面的具体方法需要在struts2的
核心文件struts.xml中配置。当然，首先需要到struts官方网站上面去下载struts需要的相应jar包。
配置文件一般放在src下面，当然你也可以放在其他的路径下面，只不过在项目web.xml中配置文件路
径正确也行。其次就是关于url访问路由的配置机制了，namespace是用于区分访问的，对url优化有
一定的作用。一般都是以‘/’开始的。其次就是action配置里面的name顾名思义就是访问Action类中方
法的名字，至于后面method目前在下还没有看出他的门道，只知道method必须和name保持一致才能实现
访问url.剩下的就是关于方法中返回的相关参数的一些处理。result中属性值有两种配置方式：1、name
对应返回的jsp文件，当然也可以设置文件路径在摸个文件夹下面。2、type返回json数据，用于编写接口代码时使用。

2、Hibernate整合
	Hibernate也适用于数据库连接，有一个SessionFactory机制实现与数据库的数据连接，需要编写*.hmb.xml
	文件与数据库结构一致。其配置文件同样在src文件夹下面，hibernate.cnf.xml文件配置，一定要注意Hibernate
	的版本信息，还有就是关于Hibernate的配置数据库引擎很多时候是InnoDB,针对mysql数据库时需要配置为MyISAM。
	引入对应的hibernate jar包后，可以再项目中新建测试类实现与数据库的交互。
