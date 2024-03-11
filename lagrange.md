# Lagrange 配置

~~其实我觉得[Lagrange官方文档](https://lagrangedev.github.io/Lagrange.Doc/)和没有差不多。~~

本章节讲述如何部署`Lagrange`供`Inkar-Suki`使用。

!> 再次强调，**如果您从互联网上得到了`Lagrange`可以使用的`QSign`地址，请不要以任何方式进行外传，这只会增加我们无法继续使用`Lagrange`进行机器人搭建的风险！**

## .NET

根据系统选择合适的页面：

- [Windows](https://learn.microsoft.com/zh-cn/dotnet/core/install/windows)
- [macOS](https://learn.microsoft.com/zh-cn/dotnet/core/install/macos)
- [Linux](https://learn.microsoft.com/zh-cn/dotnet/core/install/linux)

请先配置完毕`.NET 8`，随后再阅读下面的内容。

## 下载

首先前往`Lagrange`的`GitHub`存储库，项目地址：[LagrangeDev/Lagrange.Core](https://github.com/LagrangeDev/Lagrange.Core)。

点击[Actions](https://github.com/LagrangeDev/Lagrange.Core/actions)，随后点击左侧的`Lagrange.OneBot Build`，选择最新一个，并将页面拉至最底部，选择适合系统版本的`Lagrange`。

!> 如果不熟悉`arm64`、`amd64`、`x86`、`x64`的区别，请先学习后阅读。

点击对应版本进行下载，解压后会得到四个文件：`Lagrange.Core.pdb`、`Lagrange.OneBot`、`Lagrange.OneBot.pdb`、`libSilkCodec.so`

此处根据平台差异，后缀会有不同。

随后运行`Lagrange.Onebot`，初次使用后会生成`appsettings.json`，大概像这样：

```json
{
    "Logging": {
        "LogLevel": {
            "Default": "Debug",
            "Microsoft": "Warning",
            "Microsoft.Hosting.Lifetime": "Information"
        }
    },
    "SignServerUrl": "",
    "Account": {
        "Uin": ,
        "Password": "",
        "Protocol": "Linux",
        "AutoReconnect": true,
        "GetOptimumServer": true
    },
    "Message": {
      "IgnoreSelf": true
    },
    "Implementations": [
        {
            "Type": "ReverseWebSocket",
            "Host": "127.0.0.1",
            "Port": 2333,
            "Suffix": "/onebot/v11/ws",
            "ReconnectInterval": 5000,
            "HeartBeatInterval": 5000,
            "AccessToken": ""
        },
        {
            "Type": "Http",
            "Host": "127.0.0.1",
            "Port": 2334,
            "HeartBeatInterval": 5000,
            "AccessToken": ""
        }
    ]
}
```

这个是`Inkar Suki`公共实例的`appsettings.json`，差异的地方可以直接照搬，下面我们来讲解各字段的作用。

### Logging
#### LogLevel
##### Default

默认日志等级，推荐：`Information`，若不想有日志，可以选择`Warning`，调试可以使用`Trace`。

### SignServerUrl

签名服务器，与`Go-CQHTTP`的签名服务不同，具体地址请自行在互联网搜索。

### Account
#### Uin

QQ号，`int`变量，不需要引号。

#### Password

QQ密码，`str`变量，需要双引号。

#### Protocol

NTQQ的协议，可选：`Linux`、`Windows`、`macOS`（猜测）。

### Implementations

传输方式，为`JSON`数组，每一个元素像这样：

```json
{
    "Type": "ReverseWebSocket", // 反向WebSocket
    "Host": "127.0.0.1", // 反向WS的IP
    "Port": 2333, // 反向WS端口
    "Suffix": "/onebot/v11/ws", // 反向WS的地址
    "ReconnectInterval": 5000, // 默认即可，下同
    "HeartBeatInterval": 5000,
    "AccessToken": "" // 留空即可
}
```

Type还可选：`ForwardWebSocket`（正向`WebSocket`）、`Http`（`HTTP`服务器），这些是`Inkar Suki`可能用到的（并不使用正向WS）。

如果登录的时候遇到验证码（通常是要求输入`Ticket`和`rdstring`），可以按这样的方法操作（以`Chrome`为例，`开发者工具`已切换至中文）：

- 访问验证码的网页；
- 按下`F12`，进入开发者工具，选择`网络`（`Network`）、点击`Fetch/XHR`。
- 通过验证码，选中最后一个`Fetch/XHR`请求，点击预览（`Preview`），如果`ticket`一栏为空，重复上述步骤，如果不为空，右键`ticket`，选择`复制值`，将其输入`Lagrange`终端后回车，**先不要关闭页面**，依然在预览处，查看`rdstring`，右键`复制值`，将其输入`Lagrange`终端回车。’

首次登录使用扫码登录，后续直接登录即可。