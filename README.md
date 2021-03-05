#  mURL (my url)
![myrand](https://github.com/m-sql/myrand/blob/master/templates/control/img/myrand.png)

## 是一个对文件URL压缩短链的自动化工具（文件上传+文件短网址）服务 🚀

# 功能特点
* 跨平台支持（支持Linux, Mac环境，Windows环境理论上也支持，不过未全面测试）
* 目前只支持 PNG、JPG、JPEG 等 文件上传
* 支持批量文件上传
* 支持自定义Route 和 API快速定制

#  安装使用

## 依赖软件

### 一般依赖
* go 1.14+
* git

## 1、下载源码
```linux
 [root@lidi home]# git clone https://github.com/m-sql/myrand
  Cloning into 'myrand'...
  remote: Enumerating objects: 26, done.
  remote: Counting objects: 100% (26/26), done.
  remote: Compressing objects: 100% (21/21), done.
```

## 2、检测DNS配置: .env
``` linux
DB_TYPE="mysql"
DB_DSN="root:123456@tcp(localhost:3306)/go?charset=utf8&parseTime=True&loc=Local"
JWT_KEY="jwt_secret"
JWT_ISSUER="123456"
REDIS_DB="0"
REDIS_ADDR="localhost:6379"
REDIS_PWD=""
FILE_URL=""
PROXY_URL="此项目服务地址"
```

## 3、linux下执行Go
``` linux
cd myrand

[root@test1 myrand]# go run go.main
 [GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.
 
 [GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
  - using env:   export GIN_MODE=release
  - using code:  gin.SetMode(gin.ReleaseMode)
 
 [GIN-debug] GET    /v2/:short_url            --> myrand/controller.Short2Long (4 handlers)
 [GIN-debug] POST   /api/user/login           --> myrand/controller.Login (4 handlers)
 [GIN-debug] POST   /api/user/register        --> myrand/controller.Register (4 handlers)
 [GIN-debug] POST   /api/long/short           --> myrand/controller.Long2Short (4 handlers)
 [GIN-debug] GET    /templates/*filepath      --> github.com/gin-gonic/gin.(*RouterGroup).createStaticHandler.func1 (4 handlers)
 [GIN-debug] HEAD   /templates/*filepath      --> github.com/gin-gonic/gin.(*RouterGroup).createStaticHandler.func1 (4 handlers)
 [GIN-debug] GET    /upload/*filepath         --> github.com/gin-gonic/gin.(*RouterGroup).createStaticHandler.func1 (4 handlers)
 [GIN-debug] HEAD   /upload/*filepath         --> github.com/gin-gonic/gin.(*RouterGroup).createStaticHandler.func1 (4 handlers)
 [GIN-debug] GET    /upload                   --> myrand/controller.UploadHtml (4 handlers)
 [GIN-debug] POST   /upload/UploadAction      --> myrand/controller.UploadFile (4 handlers)
 [GIN-debug] Listening and serving HTTP on :9090

```

## 4、立刻即用
```linux

访问即可 ： http://localhost:9090/upload

```

.

## 5、样例图片

![myrand-demo](https://github.com/m-sql/myrand/blob/master/doc/1.png)

.

## 6、体验-demo

点击访问：http://47.104.70.146:9090/upload

.

## 7、License

Completely MIT Licensed. Including ALL dependencies. If you love or like it ！Please join us!

[MIT : license](https://github.com/m-sql/myrand/blob/master/LICENSE)

.

