# 自搭建

本节主要讲述如何在自己的服务器上搭建`Inkar Suki`，请具备一定的计算机基础知识。

`Inkar Suki`基于`Nonebot`的`OneBot V11`标准，也就是说，您必须找到一个`OneBot V11`协议端方可使用`Inkar Suki`。

所谓`协议端`，例如`Go-CQHTTP`等，用于在本地和机器人平台通信的协议端，此处并不举例，请自行寻找。

# 下载

## 本体

目前强烈推荐从`GitHub`上直接进行拉取，使用下面的命令：
```
git clone https://github.com/HornCopper/Inkar-Suki.git
```

## 环境

> `Inkar Suki`目前没有提供`Docker`部署方法，你可以自行探索（线索：[群友的Docker部署](https://github.com/102375470/Inkar-Suki-Docker)）。

`Inkar Suki`需求的`Python`为`Python 3.10+`，推荐使用`Linux`。

推荐使用`conda`管理`Python`环境，可前往[清华大学开源软件镜像站](https://mirrors.tuna.tsinghua.edu.cn/anaconda/miniconda/)的`Miniconda`。

在`Python`环境创建**并激活**之后，切换到`Inkar Suki`主目录，使用下面的命令安装依赖：
```
pip install pdm && pdm install
```

## 配置

由于`.gitignore`的存在，`.env.dev`文件在主目录可能不存在，需要手动创建。
```
HOST=127.0.0.1
PORT=2333
COMMAND_START=["", "+"]
```

在非`Windows`的平台上，可以追加一行：`fastapi_reload=true`，但在`Windows`上，使用该语句会导致`Playwright`无法正常工作。

比起`fastapi_reload`，`Nonebot 2`更推荐使用`nb run --reload`，使用`--reload`进行启动，效果与`fastapi_reload`类似。

上述配置完毕后，在`Inkar Suki`目录下使用`nb run`启动一次，**初次启动不存在`src/tools/config/config.yml`**，音卡本体会自动创建配置文件在`src/config/`目录下，请自行填写完毕后重新启动。

如果某些配置项并不知道如何填写，前往官方群聊可能会有帮助。

## 完成

以上内容配置完毕后，在`Inkar-Suki`目录下运行`nb run`进行启动。

# 参见

* [FAQ](/faq)
* [使用](/usage)