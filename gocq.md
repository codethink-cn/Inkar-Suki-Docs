# Go-CQHTTP 相关配置

本章节主要讲述如何搭建`go-cqhttp`以搭建`Inkar Suki`。

!> 阅读本章节之前，请注意：**本章节所述内容可能不具有任何时效性，甚至可能不存在任何有用信息，且本页已经放弃维护**，参考阅读[Go-CQHTTP#2471](https://github.com/Mrs4s/go-cqhttp/issues/2471)。

正文中未讲解的配置内容需要自行查询[Go-CQHTTP 官方文档](https://docs.go-cqhttp.org/)，**未讲解的内容与您的Bot搭建大部分是没有任何关系的，也就是他们一般来说不需要配置，使用默认方案即可。**

!> 本章节是计划外的章节，`Inkar Suki`原文档计划中并没有本章节，由于多数用户的需要，故创作本章节。
<br>
欢迎对于本章节的内容进行提问，不过请记住，开发者**没有义务**回答问题，但是我们会尽可能地解决您的问题。

## 配置文件

配置文件位于`go-cqhttp`工作目录下的`config.yml`。

### 账号密码相关

```yaml
account: # 账号相关
  uin: 123456 # QQ账号
  password: '' # 密码为空时使用扫码登录
  encrypt: false  # 是否开启密码加密
  status: 0      # 在线状态 请参考 https://docs.go-cqhttp.org/guide/config.html#在线状态
  relogin: # 重连设置
    delay: 3   # 首次重连延迟, 单位秒
    interval: 3   # 重连间隔
    max-times: 0  # 最大重连次数, 0为无限制
```

`uin`是`bot`的QQ号，不需要使用任何引号，直接将`123456`替换为`QQ号`即可。

`password`是`bot`的QQ密码，需要使用单引号包裹。

> 如果密码为空，则需要手动修改`device.json`的`protocol`字段为`2`，并确保手机QQ可以扫码登录。此时`go-cqhttp`使用协议`Android Watch`。

!> 自2023年5月29日（不准确时间）起，`Android Watch`协议似乎不再可用，即使使用`Android Phone`或`Android Pad`协议，也需要配置`qsign`（[传送门-GoCQHTTP#2183](https://github.com/Mrs4s/go-cqhttp/issues/2183)以及[传送门-unidbg-fetch-qsign](https://github.com/fuqiuluo/unidbg-fetch-qsign)，至于配置`qsign`的方法，请参考下一小章节）。

### 签名服务器

签名服务器，或称之为`qsign`，是用于给`go-cqhttp`发送给企鹅服务器的信息进行数据签名的程序，仓库地址在上面已经提到过，此处不再赘述。

> 如果您正在使用`正式版`（截至2023年9月23日16:55，最新版本为`v1.1.0`）的`go-cqhttp`，那么请下载`1.1.0`的`qsign`。<br>
> 如果您使用`dev`的`go-cqhttp`，那么请直接下载最新版本的`qsign`。<br>
> 如果您正在使用本章节提供的`go-cqhttp`，请下载`b1.1.7`的`qsign`，更新或者更旧的版本尚未测试过。

`qsign`下载之后解压，查找一个名为`txlib`的文件夹，里面应当有很多`X.X.XX`格式的文件夹，这是协议版本。

一般而言，`qsign`会附带一些协议以及协议的文件。这里以`8.9.58`协议为例（`txlib/8.9.58/config.json`）：

```json
{
  "server": {
    "host": "0.0.0.0",
    "port": 8080
  },
  "key": "1919810",
  "auto_register": false,
  "protocol": {
    "qua": "V1_AND_SQ_8.9.58_4106_YYB_D",
    "version": "8.9.58",
    "code": "4106"
  },
  "unidbg": {
    "dynarmic": false,
    "unicorn": true,
    "debug": false
  },
  "black_list": [
    1008611
  ]
}
```

如果您只需要本地能够访问，`host`可以改为`"127.0.0.1"`，`port`字段是访问的端口，亦可修改，`key`字段是访问接口的“钥匙”，这个值需要与`gocq`的配置中相同。

> 请记得修改您的云服务器防火墙设置，以确保能够从外部访问。

!> 如果您使用的`gocq`配置文件中，没有提供`qsign`的`key`设置，那么您的`gocq`不适合该`qsign`，请自行搭配。
<br>
或者如果您的`qsign`配置中不存在这个文件，请将`go-cqhttp`配置文件的`is-below-110`设置为`True`。

`go-cqhttp`对于`qsign`的配置如下（已去除注释）：

```yaml
  sign-server: 'http://1.14.51.4:114514'
  sign-server-bearer: '-'
  is-below-110: false
  key: '114514'
  auto-register: false
  auto-refresh-token: false
  refresh-interval: 40
```

我们只需要关注`sign-server`，如果你的`sign`访问地址为`http://127.0.0.1:19810/txsb/qsign`，那么请填写`http://127.0.0.1:19810/txsb`，以此类推。

> 确保`go-cqhttp`配置文件中的`key`与`qsign`配置文件中的`key`**完全一致**。

随后切换到`qsign`工作目录（也就是目录下有`lib`、`txlib`、`bin`三个文件夹的目录），使用命令：`bash bin/unidbg-fetch-qsign --basePath=txlib/8.9.71`。

这里使用的是`8.9.71`协议，如果您使用的是其他的，请自行修改协议。

### 与Nonebot连接

本小节所指的`Nonebot`若无特殊声明，均为`Nonebot 2`。

`go-cqhttp`提供了多种通信方式，这里我们使用`反向Websocket`与`Nonebot`进行连接。

另外由于`Inkar Suki`的`+api`命令使用了`go-cqhttp`的`HTTP API`，所以也需要修改一下。

找到配置文件中的`servers:`，追加这两行：

```yaml
  - http: # HTTP 通信设置
      address: 0.0.0.0:2334 # HTTP监听地址
      version: 11     # OneBot协议版本, 支持 11/12
      timeout: 5      # 反向 HTTP 超时时间, 单位秒，<5 时将被忽略
      long-polling:   # 长轮询拓展
        enabled: false       # 是否开启
        max-queue-size: 2000 # 消息队列大小，0 表示不限制队列大小，谨慎使用
      middlewares:
        <<: *default # 引用默认中间件
      post:           # 反向HTTP POST地址列表
      #- url: ''                # 地址
      #  secret: ''             # 密钥
      #  max-retries: 3         # 最大重试，0 时禁用
      #  retries-interval: 1500 # 重试时间，单位毫秒，0 时立即
      #- url: http://127.0.0.1:5701/ # 地址
      #  secret: ''                  # 密钥
      #  max-retries: 10             # 最大重试，0 时禁用
      #  retries-interval: 1000      # 重试时间，单位毫秒，0 时立即
  # 反向WS设置
  - ws-reverse:
      # 反向WS Universal 地址
      # 注意 设置了此项地址后下面两项将会被忽略
      universal: ws://127.0.0.1:2333/onebot/v11/ws
      # 反向WS API 地址
      api: ws://your_websocket_api.server
      # 反向WS Event 地址
      event: ws://your_websocket_event.server
      # 重连间隔 单位毫秒
      reconnect-interval: 3000
      middlewares:
        <<: *default # 引用默认中间件
```

只需要注意`- http:`下的`address`，可以使用`0.0.0.0`或者`127.0.0.1`，端口自行决定，然后复制形如`http://127.0.0.1:14514/`，填写至`Inkar Suki`的`config.py`的`cqhttp`变量。

以及`- ws-reverse:`，只需要设置下方的`universal`，如果`Inkar Suki`与`Go-CQHTTP`都在本地，那么使用`ws://127.0.0.1:port/onebot/v11/ws`，`port`请修改为可用的随意端口（1-65536）。

!> 此处的`port`需要与`Inkar Suki`目录下的`.env.dev`的`PORT`值相同！

到这里也就配置完毕了，在`go-cqhttp`目录下运行`./go-cqhttp faststart`（`Linux`）即可运行啦！