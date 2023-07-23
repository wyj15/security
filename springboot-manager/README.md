# springboot-manager

## 介绍
基于SpringBoot + Thymeleaf + Layui + Apache Shiro + Redis + Mybatis Plus 的后台管理系统  
支持菜单权限与数据权限    
数据库支持 MySQL、Oracle、sqlServer 等主流数据库  
提供代码生成器，基本增删改查无需编写，可快速完成开发任务。  
后台接口RESTful 风格，支持前后端分离，可与app公用一套接口。  

## 特征
- 后台接口RESTful 风格，支持前后端分离，可与app公用一套接口
- 采用RBAC的权限控制，支持数据权限（用法见下）
- 统一响应结果封装及生成工具
- 统一异常处理
- Shiro + Redis 实现 Token 角色权限认证
- 使用Druid Spring Boot Starter 集成Druid数据库连接池与监控
- 集成MyBatis-Plus，实现单表业务零SQL
- 支持多数据源，自由切换，只需方法或类上用 @DS 切换数据源
- 集成国人风格的knife4j，自动生成接口文档
- 提供代码生成器(MySQL、Oracle、sqlServer等主流数据库)，生成从Html到Mapper，爽歪歪  

## 安装部署

1. 下载redis 启动`redis`

2. 创建数据库, 导入`doc/mysql.sql`

3. 配置`application-dev.yml`中的`redis`以及`数据库`连接

4. 运行项目

5. 直接运行`CompanyProjectApplication.java`

6. 项目根目录下执行:

   ```
   mvn -X clean package -Dmaven.test.skip=true
   ```

7. 编译打包，然后执行:

   ```
   java -jar manager.jar
   ```

   - 登录地址 [http://localhost:8080/index/login](https://gitee.com/link?target=http%3A%2F%2Flocalhost%3A8080%2Findex%2Flogin) 用户名密码:admin/123456

## 系统截图

![image-20230723014807504](C:\Users\Naomi\AppData\Roaming\Typora\typora-user-images\image-20230723014807504.png)

![image-20230723014848071](C:\Users\Naomi\AppData\Roaming\Typora\typora-user-images\image-20230723014848071.png)

## 代码结构

```
├─main
│  ├─java
│  │  └─com
│  │      └─company
│  │          └─project
│  │              ├─CompanyProjectApplication.java 项目启动类
│  │              ├─common      公共资源，如注解、切面、定时、全局异常处理、shiro集成、通用工具类等
│  │              ├─controller  Controler层
│  │              ├─entity      实体类
│  │              ├─mapper      DAO层
│  │              ├─service     Service层
│  │              │  └─impl     Service层实现
│  └─resources
│      ├── application-dev.yml  开发环境配置文件
│      ├── application-test.yml 测试环境配置文件
│      ├── application-prod.yml 生产环境配置文件
│      ├── application.yml      通用配置文件
│      ├── logback-spring.xml   日志配置文件
│      ├─mapper                 Mybatis XML文件
│      ├─static                 静态文件
│      │  ├─css                 通用css文件
│      │  ├─images              静态图片
│      │  ├─js                  通用js文件
│      │  ├─layui               layui库
│      │  └─layui-ext           layui插件库
│      ├─template               代码生成模版
│      └─templates              项目页面目录
│          ├─depts              部门管理
│          ├─error              错误页面
│          ├─generator          代码生成管理
│          ├─logs               日志管理
│          ├─menus              菜单管理
│          ├─roles              角色管理
│          ├─syscontent         内容管理
│          ├─sysdict            字典管理
│          ├─sysfiles           文件管理
│          ├─sysjob             定时任务管理
│          ├─sysjoblog          定时任务日志管理
│          └─users              用户管理
└─test
    └─java
        └─com
            └─company
                └─project
                    ├── CompanyFrameApplicationTests.java 单元测试
```

用户名密码:admin/123456

