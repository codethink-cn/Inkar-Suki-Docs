# 自搭建

本节主要讲述如何在自己的服务器上搭建`Inkar Suki`，请具备一定的计算机基础知识。

本章节不讲述如何配置`Go-CQHTTP`，相关内容请访问[Go-CQHTTP文档](https://docs.go-cqhttp.org/guide/#go-cqhttp)。

**2023年9月23日新增文档：[Go-CQHTTP相关配置](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/#/gocq)。**

> 请`仔细且完整`地阅读完毕整个文档，如果发生基础错误且文档内有出示我们可能不会为您提供支持或服务。

## 下载

### 环境配置

`Inkar Suki`需要以下内容：
* Python
* GO-CQHTTP
* [Git](https://git-scm.com/)

如果`Python`[官网](https://www.python.org)缓慢或无法访问，可以前往淘宝的`Python`镜像站：[传送门](https://registry.npmmirror.com/binary.html?path=python/)。

> 请注意，`Inkar Suki`所需的`Python`版本至少为`3.8`，不建议使用`3.10+`，但仍然可用。

`Go-CQHTTP`项目地址：`Mrs4s/go-cqhttp`（[传送门](https://github.com/Mrs4s/go-cqhttp)），请下载最新版本。

> 亦可选择使用`nonebot-plugin-gocqhttp`，这样可以不再自己搭建`Go-CQHTTP`，但是需要自行配置该插件，项目地址：`mnixry/nonebot-plugin-gocqhttp`（[传送门](https://github.com/mnixry/nonebot-plugin-gocqhttp)）。<br>

!> 由于企鹅公司修改了算法，导致大部分`Go-CQHTTP`会触发风控/封号，无法正常发送消息，请尝试自行搭建签名服务器，详情请见[Go-CQHTTP#2183](https://github.com/Mrs4s/go-cqhttp/issues/2183)。

安装好`Python`后，使用`python --version`测试是否安装成功，必要时替换为`python3`。

> 为什么需求中不列出`Nonebot`？<br>
> `Inkar Suki`所需要的`Python`库，在`Bot`文件夹使用`pip install -r requirements.txt`即可一键下载，必要时请更改为`pip3`而非`pip`。

在使用一键命令安装完毕所有需求的`Python`库之后，请使用`playwright install`安装`Playwright`所需要的库。

!> 如果您使用`Windows`搭建`Inkar Suki`，请确保`.env.dev`中的`fastapi_reload`的值为`false`，否则`Playwright`库无法正常工作，抛出的错误一般是`NotImplementedError`，详情请见[Nonebot 2官方文档](https://nonebot.dev/docs/advanced/driver#fastapi_reload)。<br>
表现为使用了浏览器生成图片的所有功能无法使用，使用`PIL`（`Pillow`）的不受此影响。

### 本体下载

**强烈建议使用`Git`从仓库进行拉取而非自行下载压缩包！**

#### 从Releases下载

进入[Releases](https://github.com/codethink-cn/Inkar-Suki/releases)，选择任一（最好是最新）版本，下载`Source code`（格式不限），并放置到任一文件夹中解压。

#### 从主页下载

进入仓库[主页](https://github.com/codethink-cn/Inkar-Suki)，点击绿色按钮的`<> Code`，点击`Download ZIP`，获取最新代码，请注意，由于是最新的代码，不确保稳定，~~其实连Releases也不确保是稳定的~~。

#### 从Git下载（强烈推荐）

进入随意文件夹，执行以下命令：
```
git clone https://github.com/codethink-cn/Inkar-Suki.git
```

> 使用Git下载的话，配置最为简便，日后的更新可以通过`git pull`直接实现。<br>
> 如果使用主页或`Releases`下载，将无法使用`git`相关命令（未配置的情况下）。

### 配置文件

打开我们的`config.sample.py`，使用`vi/vim`、`记事本`、`Visual Studios Code`看个人喜好。

```python
###############################
# 请将该文件改为 config.py 后使用
###############################

from src.tools.local_version import ikv, nbv
from src.tools.file import get_resource_path
from pathlib import Path
import os
class Config:
    '''
    这里是`Inkar Suki`的配置文件，从`V0.8.3-Hotfix-3起，我们删除了`initialization.py`。
    取消了问答式配置，改为了用户自己填写。
    需要您填写的是末尾有注释的行，其他行请勿改动，感谢使用！
    此处的内容填写完毕后，请将文件名称改为`config.py`~
    '''
    config_py_path = __file__[:-10]
    global_path = config_py_path[:-6]+"/"

    web_path = ""  # GitHub Webhook的地址，填写`/a`，则内网地址为`http://127.0.0.1:<NB端口>/a`，`NB端口`在`.env.dev`中的`PORT`

    bot = [""]  # Bot的QQ号，此处请只填写一个，用`str`存在`list`中。

    platform = True  # 平台标识，`True`为Linux，`False`为`Windows`

    owner = [""]  # Bot主人，可以有多个，用`str`存在`list`中

    size = global_path+"/tools/size.txt"
    html_path = global_path+"/plugins/help/help.html"
    chromedriver_path = global_path+"/tools/chromedriver"
    help_image_save_to = global_path+"/plugins/help/help.png"
    font_path = Path(get_resource_path(f'font{os.sep}custom.ttf')).as_uri()

    cqhttp = ""  # CQHTTP地址，参考`https://go-cqhttp.org`。

    welcome_file = global_path+"/tools/welcome.txt"
    version = ikv
    nonebot = nbv

    proxy = ""  # 代理服务器地址，以`http://`开头或`https://`开头，可以跟端口。

    auaurl = ""  # Arcaea Unlimited API地址

    auatok = ""  # Arcaea Unlimited API Token
    # 以上两者都请进群：“574250621”

    jx3api_wslink = ""  # JX3API WebSocket地址

    jx3api_wstoken = ""  # JX3API WebSocket Token

    jx3api_globaltoken = ""  # JX3API API Token

    ght = ""  # GitHub Personal Access Token

    jx3_token = "123"  # 推栏Token，抓包可得

    repo_name = ""  # 该`Inkar-Suki`的副本的来源，若从主仓库克隆，则填写`codethink-cn/Inkar-Suki`，若为fork之后克隆的仓库，则填写`<你的GitHub用户名>/Inkar-Suki`

    jx3api_link = "" #JX3API API链接

    notice_to = [""] # 当音卡触发特定事件时推送到群聊，可以有多个

    inkarsuki_offical_apitoken = "" # 留空即可
```

后面没有注释的代码行可以忽略。

#### web_path

类型：`str`

该值决定`Webhook`的入口地址，填写`/webhook`，则会在`http://127.0.0.1:<ENV.PORT>/webhook`开启`FastAPI`入口。

#### bot

类型：`list`

该值虽为`list`，请只填写一个元素，为`Bot`的`QQ`号，未来可能会支持多机器人。

#### platform

类型：`bool`

若为`True`，则为`Linux`系统，若为`False`，则为`Windows`系统。

!> `Inkar-Suki`的搭建环境不建议使用`Windows`系统，具体原因在`环境配置`中已讲述过，对于`Linux`，我们建议使用`Debian 11/Ubuntu 20.04`及以上系统，因为他们的自带`Python 3`版本较高。

#### owner

类型：`list`

机器人主人列表，元素为`QQ`号，需要**能够**转换为`int`的`str`值。

#### cqhttp

类型：`str`

`Go-CQHTTP`的`HTTP API`地址，一般是内网地址，以`/`结尾，例如：`http://127.0.0.1:80/`。

#### proxy

类型：`str`

代理服务器，仅支持本地代理。

#### auaurl & auatok

类型：`str`

`Arcaea Unlimited API`的`URL`和`Token`，两项均前往`574250621`群内找群主申请。

#### jx3api_wslink & jx3api_wstoken
#### jx3api_globaltoken & jx3api_link

类型：`str`

参见[JX3API](https://jx3api.com/#/?id=socket)和[神奇的生活馆](https://store.nicemoe.cn/)。

`jx3api_link`以`/`结尾，以`https://`开头，格式同`cqhttp`。

#### jx3_token

类型：`str`

由抓包软件抓取推栏`m.pvp.xoyo.com`数据包的`headers`中`token`字段而得。

#### repo_name

类型：`str`

该`Inkar-Suki`副本的`Repository`来源，格式为`Author/Repository`。

#### ght

类型：`str`

参考[GitHub Personal Access Token](https://github.com/settings/tokens)。

### 权限控制

`Inkar-Suki`自带一套较为完善的权限系统，该权限系统分为`0-10`，共`11`个等级，每个等级对应的特权不同，但高权限包含低权限。

> 只有同时具有`10`级权限以及处于配置文件中`owner`的列表中的用户具有给予`10`级权限的能力。<br>


|权限等级|权限内容|备注|
|-----|-----|-----|
|`0`|`-`|`-`|
|`1`|`ping`命令能够回复服务器负载相关信息。<br>能够使用`purge`清除图片缓存。|`-`|
|`2`|`-`|`-`|
|`3`|`-`|`-`|
|`4`|`-`|`-`|
|`5`|能够自行设置违禁词。<br>免疫违禁词封禁。<br>能够修改入群欢迎语。<br>能够设置自定义`Interwiki`。<br>能够自行设置避雷名单。|`-`|
|`6`|`-`|`-`|
|`7`|`-`|`-`|
|`8`|无须群主/管理员权限亦可绑定群聊的服务器。<br>可以将新群注册或退出某群。<br>|处理申请时会由机器人超管给予`8`级权限以供注册。|
|`9`|可以使用`echo`和`say`。<br>可以体验内测功能。<br>可以重启`Inkar Suki`。|内测功能的内测资格为`9`级权限。|
|`10`|除`机器人公告`外所有功能。|`机器人公告`需求权限等级为`owner`。|

> 使用`setop <QQ> <LEVEL>`在聊天中进行权限修改。

### 完成

以上内容配置完毕后，在`Inkar-Suki`目录下运行`nb run`进行启动。

### 参见

* [FAQ](/faq)
* [使用](/usage)