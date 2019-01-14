快速开始

### 开发人员搭建

- git clone https://github.com/tomoya92/pybbs
- 使用idea打开，项目用的是idea开发的，如果你对eclipse熟悉，也是可以的
- idea打开它会自动构建项目，构建工具是maven
- 修改配置文件 `src/main/resources/application.yml` 里的数据库相关配置
- 找到`co.yiiu.pybbs.PybbsApplication`类，直接运行main方法即可启动
- 浏览器运行 `http://localhost:8080` , 后台地址 `http://localhost:8080/adminlogin` 后台用户名 admin 密码 123123

### 非开发人员搭建

- 首先保证你服务器上配置好了 java 环境，版本 jdk1.8 和 MySQL服务器，版本 5.7.x 其它可选环境配置参见 [网站准备工作](https://tomoya92.github.io/pybbs/#/ready)
- 然后下载最新的一键启动压缩包，下载地址：[https://github.com/tomoya92/pybbs/releases](https://github.com/tomoya92/pybbs/releases)
- 解压, 修改解压出来的文件夹里的 `application-prod.yml` 文件，只需要修改一个地方，就是数据库的连接信息，[配置方法](https://tomoya92.github.io/pybbs/#/base)
- 运行压缩包里的脚本 `sh start.sh`
- 关闭服务运行 `sh shutdown.sh` 
- 查看启动日志 `tail -200f log.file`
- 查看服务是否启动 `ps -ef|grep pybbs` 如果有pybbs的进程，就说明服务启动了
- 网站的其它配置，参见文档

### docker运行

- 保证服务器有docker和docker-compose环境
- git clone https://github.com/tomoya92/pybbs或下载最新版
- cd pybbs进入项目
- 运行 `docker-compose up` 命令

  **第一次运行会比较慢,视服务器性能和网速决定**
  **项目根目录下会生成 `mysql` 文件夹为数据库文件,注意谨慎操作**