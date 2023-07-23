# AICHAT

#### 系统介绍

基于[ChatGPT-Next-Web](https://github.com/Yidadaa/ChatGPT-Next-Web.git)开源项目进行二次开发，增加用户注册登录、用户管理、套餐管理等功能，并提供可自行部署的解决方案。

#### 系统功能

| 功能                                                     |
| -------------------------------------------------------- |
| 用户管理（User Management）                              |
| 额度管理（Quota Management）                             |
| 注册额度赠送（Registration limit gift）                  |
| 邮箱验证码注册（Email verification code registration）   |
| 调用频率限制（User based call frequency limit）          |
| 图形验证码注册（Graphic verification code registration） |
| 网站标题（Website Title Customization）                  |
| 套餐管理（Package Management）                           |
| 自定义敏感词拦截（Custom sensitive word interception）   |
| 忘记/重置密码（Reset Password）                          |
| API KEY余额自动查询（Auto Query Balance/Quota）          |

#### 安装部署

1. 在安全组中放行80端口和8080端口
2. 连接云服务器，在命令行中运行以下代码

```
bash <(curl -s https://raw.githubusercontent.com/Nanjiren01/AIChatWeb/main/scripts/setup.sh)
```

命令运行过程中，需要设置超级管理员的账号和密码（请将aichat888更改为自己的账号密码并牢记），如下所示：

```
Please input the super admin username. 
Only letters and numbers are supported, the length should between 6 and 20, and they cannot start with a number.
Username: aichat888
Super Admin Username is valid.
Please input the super admin password. 
Only letters and numbers are supported, and the length should between 6 and 20. 
You can change it on the web page after the Application running
Password: aichat888
Super Admin Password is valid.
```

当出现以下提示，说明部署成功

```
[+] Running 5/5
 ✔ Network root_default      Created
 ✔ Container aichat-db       Started
 ✔ Container aichat-admin    Started
 ✔ Container aichat-console  Started
 ✔ Container aichat-web      Started         
```

稍等几秒钟应用初始化，即可打开[http://IP访问前台页面，打开http://IP:8080访问后台服务。](http://xn--ip%2Chttp-u00lu5jg61bpditx3klx1a4ie3ve//IP:8080访问后台服务。)

#### 项目截图

![image-20230722230951283](C:\Users\Naomi\AppData\Roaming\Typora\typora-user-images\image-20230722230951283.png)

![image-20230722230828352](C:\Users\Naomi\AppData\Roaming\Typora\typora-user-images\image-20230722230828352.png)

![image-20230722230920513](C:\Users\Naomi\AppData\Roaming\Typora\typora-user-images\image-20230722230920513.png)

![image-20230722231323654](C:\Users\Naomi\AppData\Roaming\Typora\typora-user-images\image-20230722231323654.png)

![image-20230722231342674](C:\Users\Naomi\AppData\Roaming\Typora\typora-user-images\image-20230722231342674.png)

账号：aichat 密码：aichatadmin