# 自搭建

本节主要讲述如何在自己的服务器上搭建`Inkar Suki`，请具备一定的计算机基础知识。

本章节不讲述如何配置`Go-CQHTTP`，相关内容请访问[Go-CQHTTP文档](https://docs.go-cqhttp.org/guide/#go-cqhttp)。

**2023年9月23日新增文档：[Go-CQHTTP相关配置](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/#/gocq)。**

**2024年3月4日新增文档：[Lagrange相关配置](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/#/lagrange)。**

> 请`仔细且完整`地阅读完毕整个文档，如果发生基础错误且文档内有出示我们可能不会为您提供支持或服务。

## 下载本体

使用`Git`从仓库拉取，或者直接下载压缩包（`Lastest`或`Releases`）。

推荐使用`Git`拉取，因为可以随时更新。

## 环境配置

`Inkar Suki`需要以下内容：
* Python
* 任意`Onebot V11`协议端（例如：`Go-CQHTTP`，`Lagrange`等）
* [Git](https://git-scm.com/)

如果`Python`[官网](https://www.python.org)缓慢或无法访问，可以前往淘宝的`Python`镜像站：[传送门](https://registry.npmmirror.com/binary.html?path=python/)。

> 推荐使用`conda`对`Python`进行管理，关于如何配置`conda`，请自行搜索。关于如何安装`Python`，也请自行搜索。

首先切换至`Inkar Suki`的主目录，使用`ls`可以发现目录下有`requirements.txt`，使用以下命令安装依赖即可：
```bash
pip install -r requirements.txt
```

安装完毕后，安装`Playwright`的依赖：
```bash
playwright install-deps`
```

随后再安装`Playwright`需要的浏览器：
```bash
playwright install
```

如果启动时发现`Nonebot`报错，请参考[FAQ](/faq.md)。

## 本体配置

理论上其他文件不需要修改，我们只需要关注主目录下的`.env.dev`和`src/tools/config`目录。

可以直接清空`.env.dev`，然后按需填写下面的内容：
```
HOST=0.0.0.0
PORT=2333
COMMAND_START=["+","","-"]
APSCHEDULER_AUTOSTART=true

[FastAPI]
fastapi_reload = true
```

`HOST`和`PORT`为`Nonebot`的监听地址和端口，请确保和协议端配置的监听地址和端口一致。`Nonebot`默认使用反向`Websocket`与协议端通信。

`COMMAND_START`为命令前缀，如果命令没有其中之一的前缀，那么`on_command`响应器不会被触发，命令也不会被响应。

`fastapi_reload`为`FastAPI`的配置，如果设置为`true`，则会自动监听文件更改，和`git`配合使用，可以省去每次手动重启。

!> 如果您使用`Windows`搭建`Inkar Suki`，请确保`.env.dev`中的`fastapi_reload`的值为`false`，否则`Playwright`库无法正常工作，抛出的错误一般是`NotImplementedError`，详情请见[Nonebot 2官方文档](https://nonebot.dev/docs/advanced/driver#fastapi_reload)。<br>
表现为使用了浏览器生成图片的所有功能无法使用，使用`PIL`（`Pillow`）的不受此影响。在`Windows`下，可以在启动时使用`--reload`参数实现相同的效果。

而`src/tools/config`目录下有示例配置文件：`config_example.py`。

下面是示例配置的代码，可以复制后自行使用。填写完毕后，请将文件名改为`config.py`，因为`Inkar Suki`会读取该文件。

```python
import os
import inspect

class Config:
    config_py_path = os.path.abspath(inspect.getfile(inspect.currentframe()))[:-10] # 请勿修改
    global_path = config_py_path[:-6]+"/" # 请勿修改

    name = "音卡" # 机器人名称，可自定义，推荐使用默认

    web_path = "/webhook" # GitHub Webhook的地址，如无需求可直接使用默认

    platform = True # 平台标识，`True`为Linux，`False`为`Windows`

    owner = [""] # Bot主人，每个元素为QQ号，变量类型为`str`

    size = global_path + "/tools/size.txt" # 请勿修改
    html_path = global_path + "/plugins/help/help.html" # 请勿修改
    chromedriver_path = global_path + "/tools/chromedriver" # 请勿修改
    help_image_save_to = global_path + "/plugins/help/help.png" # 请勿修改
    font_path = "file://"+ global_path + "/assets/font/custom.ttf" # 请勿修改

    cqhttp = "" # CQHTTP地址，参考`https://go-cqhttp.org`。
    # 已弃用，请留空。

    proxy = "" # 代理服务器地址，以`http://`开头或`https://`开头，可以跟端口。
    # 已弃用，请留空。

    auaurl = "" # Arcaea Unlimited API地址
    # 已弃用，请留空。

    auatok = "" # Arcaea Unlimited API Token
    # 已弃用，请留空。

    jx3api_wslink = "" # JX3API WebSocket地址
    # 参考`https://www.jx3api.com/`

    jx3api_wstoken = "" # JX3API WebSocket Token
    # 该值请询问JX3API管理员

    jx3api_globaltoken = "" # JX3API API Token
    # 该值请访问`https://store.nicemoe.cn`
    # 以上三者都请进群：119032235

    ght = "" # GitHub Personal Access Token

    jx3_token = "" # 推栏Token
    # 请自行抓包推栏
    
    repo_name = "codethink-cn/Inkar-Suki" # 仓库地址
    # 根据情况而定
    # 如果使用`Git`从官方仓库拉取，请使用`codethink-cn/Inkar-Suki`
    # 如果使用`Git`从`Fork`仓库拉取，请使用自定义仓库地址
    # 如果是压缩包，该值无意义。
    
    jx3api_link = "" # JX3API 地址
    # 访问JX3API官网即可，有时JX3API会更新版本。
    
    notice_to = {
        "your_bot_uin": "admin_group_uin" # 
    }
    # key为`Bot`的`QQ`号，value为`Bot`要通知的群号
    
    bot = list(notice_to) # 请勿修改
    
    inkarsuki_offical_apitoken = "" # 除非是`Inkar Suki`官方，否则请留空
```

### 完成

以上内容配置完毕后，在`Inkar-Suki`目录下运行`nb run`进行启动。

### 参见

* [FAQ](/faq)
* [使用](/usage)