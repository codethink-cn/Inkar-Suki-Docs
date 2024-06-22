# 常见问题解答

## 文件缺失

该问题报错形如`FileNotFoundError: [Errno 2] No such file or directory: C:\Users\Administrator\Desktop\Inkar-Suki\src\tools\permission.json`。

解决方式很简单，在上面报错信息所给出的路径中直接创建一个`permission.json`，内容为`{"您的QQ号":"10"}`。

此处指`Bot`的QQ号而非您的。

> 请注意：该文件的内容的`key`与`value`均为`str`，`QQ号`与权限等级均使用字符串进行存储。

## 机器人无响应

以下的原因均会导致机器人搭建完毕后没有响应，请逐一核对检查：

* 配置有误，例如`协议端`没有成功连接`Nonebot`；
* 账号被风控，具体体现为发出消息没有报错，但其他账号无法收到；
* 账号触发业务违规，表现同上，但是可以通过：`https://accounts.qq.com/safe/message/unlock?lock_info=5_5`，该地址进行解封，解封完毕即可使用；
* 自身账号被加入黑名单。

## 插件缺失

`Nonebot`在加载插件时，若出现`ModuleNotFoundError: No module named 'xxx'`，请检查`requirements.txt`中的库是否全部安装。

如果是`nonebot_plugin_xxx`，请检查`nonebot_plugin_xxx`是否安装，可以通过`nb plugin install nonebot_plugin_xxx`进行安装。

!> 针对`nonebot_plugin_xxx`，不要使用`pip`进行安装！

## 运行卡顿

如果你发现`Nonebot`运行卡顿（高度卡顿），`CPU`占用率甚至超过`100%`，按以下顺序进行排查：

* 查看`Pydantic`版本，目前似乎对`Pydantic V2`的兼容性欠佳，考虑降级至`Pydantic V1`，例如`v1.10.15`；
* 尝试使用正向`Websocket`而不是反向`Websocket`进行连接，查看响应处理速度；
* 检查`CPU`占用，系统资源是否充裕；
* 重启重装重买。