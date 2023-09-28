# 开发

本章节主要讲述如何在`Inkar Suki`的基础代码上进行开发以及代码规范。

关于什么函数该导入什么库，请参考[Nonebot 文档](https://nonebot.dev/docs/)。

## 字符串

关于字符串的处理方式。

### 拼接

如果你要拼接两个字符串，加号之间需要间隔一个空格。

```python
string = string_1 + string_2
string_ = "string" + "string"
```

### 标识

当你想表示一个字符串的时候，它的最外面应当使用`""`而非`''`。

> `"`即英文双引号，`''`是两个英文单引号，我们要求的是英文双引号（`U+0023`）。

```python
string = "string"
```

## 函数

### 定义

函数的定义应在一行代码内，异步函数和同步函数的格式完全相同。

定义的参数与参数之间，参数与类型之间均有一个空格，参数与冒号之间没有空格。

函数与函数之间需要隔行，有且只能有一行。

```python
async def function(arg1: type, arg2: type) -> type:
    ...
```

> `-> type`是可选的。

### 调用

调用的参数应该在同一行内。

```python
async def function(arg1: str, arg2: str):
    data = await get_data(arg1, arg2)
    # 或者
    data = await get_data(arg1=arg2, arg2=arg1)
```

!> `kwargs`不需要使用`=`。

## 库

### 导入

导入库的第一优先级是完整导入`import`，第二优先级是部分导入`from lib import class`，第三优先级是本地库导入`from src.tools.file import class`，第四优先级是同层库导入`from .a import b`。

如果需要拿到`src`目录下的文件夹，可以用`TOOLS = nonebot.get_driver().config.tools_path`进行获取，且该语句需要放置在第二和第三优先级之间。

```python
# src/plugins/wiki/wikilib.py
import nonebot
import json
import re

from urllib import parse
from bs4 import BeautifulSoup

TOOLS = nonebot.get_driver().config.tools_path
DATA = TOOLS.replace("tools","data")

from src.tools.utils import get_api, get_url
```

> 请尽可能避免使用`from a import *`。

!> 禁止使用`sys`库改变路径进行导入。

## Nonebot

### 插件

首先定义响应器，然后定义装饰器，最后定义函数。

大概像下面的代码：
```python
command = on_command("cmd", aliases = {"cmd1"}, priority = 5)

@command.handle()
async def function(event: GroupMessageEvent, args: Message = CommandArg()):
    ...
```

> 多个响应器之间请换行。

## GitHub

### Commit

`Commit`的内容请使用中文，英文只是方便国际友人。

格式：`[类型]概述`。

类型可以是：`修复`、`更新`、`优化`、`删除`等，这里可以使用英文缩写：`FIX`、`UPD`、`OPT`、`DEL`（大小写均可）。

示例：`[upd]加入副本记录。`。