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