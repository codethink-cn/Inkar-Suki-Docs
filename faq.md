# 常见问题解答

## `Permission.json`系列问题

该问题报错形如`FileNotFoundError: [Errno 2] No such file or directory: C:\Users\Administrator\Desktop\Inkar-Suki\src\tools\permission.json`。

解决方式很简单，在上面报错信息所给出的路径中直接创建一个`permission.json`，内容为`{"您的QQ号":"10"}`。

此处指`Bot`的QQ号而非您的。

> 请注意：该文件的内容的`key`与`value`均为`str`，`QQ号`与权限等级均使用字符串进行存储。