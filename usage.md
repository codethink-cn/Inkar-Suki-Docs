# 使用

`Inkar Suki`是一个开源的项目，它自身具有的功能相当多样，同时非常欢迎社区成员对我们的项目进行贡献！

如果你只想看剑网3相关功能，在看完下面这个消息框后可以直接[点此跳转](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/#/usage?id=jx3)，或使用左侧的搜索框进行搜索。

> 在阅读本章节之前，推荐您先阅读：[如何正确使用文档](/docs_usage)。

## ban

`Inkar Suki`封禁系统。

贡献者：`HornCopper`。

> 当权限等级为`10`时，免疫该机制。

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+ban`|`+ban <QQ>`|`-`|`封禁一个指定用户。`|`10`|`暂无`|
|`+unban`|`+unban <QQ>`|`-`|`解封一个指定用户。`|`10`|`暂无`|

该插件具有一个消息检测器，每一条消息均会进行检测发送人是否被封禁，如果是，则阻断该次事件的再次传递。

> 该插件全域生效。

!> 当尝试封禁配置文件中`owner`列表中用户时，自身会被封禁，~~还会被嘲讽~~。

## blacklist

避雷名单。

贡献者：`HornCopper`。

> 群聊之间数据不互通。

### 添加黑名单

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+block`|`+block <避雷对象> <原因>`|`+加入黑名单`、`+避雷`|`将某人添加至群内避雷名单。`|`5/群管`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/blacklist_block.png)|

### 移除黑名单

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+unblock`|`+unblock <避雷对象>`|`+移出黑名单`|`解除某人的避雷。`|`5/群管`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/blacklist_unblock.png)|

### 查询黑名单

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+sblock`|`+sblock <查找对象>`|`+查黑`|`查询某人是否在避雷名单中。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/blacklist_sblock.png)|

### 列出黑名单

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+lblock`|`+lblock`|`+本群黑名单`、`+列出黑名单`|`查询所有避雷人员。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/blacklist_lblock.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/blacklist_lblock_response.jpg)|

## bmi

BMI（身体质量指数）计算器。

> 贡献者：`HornCopper`。

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+bmi`|`+bmi <身高(M)> <体重(kg)>`|`+BMI`、`+身体质量指数`|`计算BMI指数。`|`-`|`暂无`|

## bulletin

喜报/悲报生成器。

> 贡献者：`HornCopper`。

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+喜报`|`+喜报 <文字(20以内)>`|`+喜报`|`生成喜报图片`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/bulletin_good.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/bulletin_good_response.jpg)|
|`+悲报`|`+悲报 <文字(20以内)>`|`+悲报`|`生成悲报图片。`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/bulletin_bad.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/bulletin_bad_response.jpg)|

## developer_tools

用于给`开发者`进行调试的插件。

贡献者：`HornCopper`，`Serfend`。

> 该功能并不会面向用户，因此文档内暂不提供示例。

### 杂类

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+purge`|`+purge`|`-`|`清除图片缓存。`|`1`|`暂无`|
|`+shutdown`|`+shutdown`|`+poweroff`|`关闭Inkar Suki。`|`10`|`暂无`|
|`+restart`|`+restart`|`-`|`重启Inkar Suki。`|`5`|`暂无`|
|`+echo`|`+echo <消息>`|`-`|`让Inkar Suki发送指定信息。`|`9`|`暂无`|
|`+say`|`+say <消息\|CQCode>`|`-`|`让Inkar Suki发送指定信息，会解析其中的CQ码。`|`9`|`暂无`|
|`+ping`|`+ping`|`-测试`|`测试Inkar Suki是否处于能够处理消息的状态。`|`-`|`暂无`|
|`+post`|`+post <消息>`|`-公告`|`向Inkar Suki加入的所有群聊发送指定信息。`|`10`|`暂无`|
|`+call_api`|`+call_api <api>`|`+api`|`调用Go-CQHTTP的HTTP API。`|`10`|`暂无`|
|`+voice`|`+voice <消息>`|`-`|`使用企鹅的TTS接口生成语音。`|`10`|`暂无`|

### 群聊处理

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+邀请列表`|`+邀请列表`|`-`|`查看当前待处理的邀请列表。`|`10`|`暂无`|
|`+同意申请`|`+同意申请 <群号>`|`+同意邀请 <群号>`|`同意某一个群聊的邀请。`|`10`|`暂无`|
|`+拒绝申请`|`+拒绝申请 <群号>`|`+拒绝邀请 <群号>`|`拒绝某一个群聊的邀请。`|`10`|`暂无`|

> 若发送`+ping`的人具有至少`1`级权限，则会回复系统占用等信息。

!> 若有群聊禁言了`Inkar Suki`，可能会因为发送消息失败（误判为风控等）导致全域公告发送不完全。<br>
若未正确填写`cqhttp`（配置文件）的值，会导致`+call_api`调用失败。

!> `+call_api`命令的`api`参数按`url-json`格式填写，例如：`single_api?arg1=value1&arg2=value2`。

## drifting

漂流瓶。

> 贡献者：`HornCopper`。

### 投掷漂流瓶

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+投掷漂流瓶`|`+投掷漂流瓶 <内容> [是否匿名(默认否)]`|`-`|`投掷一个漂流瓶到池塘。`|`-`|`暂无`|

### 收回漂流瓶

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+收回漂流瓶`|`+收回漂流瓶 <瓶ID>`|`-`|`从池塘收回一个漂流瓶。`|`-`|`暂无`|

> 若回收者具有`10`级权限，则无视该瓶是否属于回收者。

### 举报漂流瓶

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+举报漂流瓶`|`+举报漂流瓶 <瓶ID>`|`-`|`举报一个打捞得到的漂流瓶。`|`-`|`暂无`|

### 查看漂流瓶

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+查看漂流瓶`|`+查看漂流瓶 <瓶ID>`|`-`|`查看某漂流瓶的实际内容。`|`10`|`暂无`|

> 该功能为机器人管理者所设置，使用`+查看漂流瓶`对特定漂流瓶进行检查的时候，会直接显示投掷者的`QQ号`，无论是否匿名，而`+随机漂流瓶`会在匿名开启的时候对投掷者的`QQ号`进行隐藏。

### 随机漂流瓶

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+随机漂流瓶`|`+随机漂流瓶`|`-`|`随机获得一个漂流瓶。`|`-`|`暂无`|

## event_notice

事件响应器。

贡献者：`HornCopper`。

### 入群语修改

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+welcome`|`+welcome <欢迎语>`|`+设置入群欢迎语`|`设置入群欢迎语。`|`5/群`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/event_notice_welcome.png)|

> 如果`Inkar Suki`被移出群聊或被禁言，将会封禁操作人员。

!> 如果您使用的是公共`Inkar Suki`且不想再继续使用，请联系`HornCopper`进行退群而绝不是自行将`Inkar Suki`移出群聊。

## github

GitHub处理器。

贡献者：`HornCopper`。

!> 该插件涉及到`Webhook`，请确保您的网络安全，概不负责。<br>
如果您使用的是内网，可以考虑使用内网穿透技术或不使用`Webhook`。

### 查看仓库

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+repo`|`+repo <author/repository>`|`-`|`查看GitHub仓库。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/github_repo.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/github_repo_response.jpg)||

### 绑定仓库

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+bindrepo`|`+bindrepo <author/repository>`|`+webhook`|`绑定仓库，使收到的属于该仓库的Webhook全部推送至该群聊。`|`9/群`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/github_bindrepo.png)|

### 解绑仓库

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+unbindrepo`|`+unbindrepo <author/repository>`|`+unbind_webhook`|`解绑仓库，功能同上相反。`|`9/群`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/github_unbindrepo.png)|

## grab

~~不知道干什么的~~综合搜索模块。

贡献者：`HornCopper`、`Serfend`。

> 该插件并非由贡献者所著，而是通过移植的实现。

> 本插件中的`/`表示的是多选一。

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+[今/明/后][天/日]<早上/中午/晚上><吃/喝><什么/啥/点啥>`|`-`|`-`|`让Inkar Suki决定自己某顿吃什么。`|`-`|`暂无`|
|`+查[看/询]<菜/饮><单/料/品>`|`-`|`-`|`查看目前的菜品。`|`-`|`暂无`|
|`+添[加]<菜/饮><单/料/品>`|`-`|`-`|`添加菜品到数据中。`|`-`|`暂无`|
|`+删[除]<菜/饮><单/料/品>`|`-`|`-`|`将数据中某一菜品删除。`|`-`|`暂无`|

## jx3

[剑网3](https://jx3.xoyo.com)查询工具。

贡献者：`HornCopper`、`Serfend`、`OasisAkari`。

> 当群聊绑定服务器后，命令中`必选`的`服务器`均为`可选`。

### 服务器和新闻类

#### 绑定群聊

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_bind`|`+jx3_bind <服务器>`|`+绑定`|`绑定群聊区服。`|`8/群管`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_bind.png)|

#### 获取新闻列表

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_news`|`+jx3_news`|`+新闻`|`获取官方最近4条新闻。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_news.png)|

#### 获取开服信息

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_server`|`+jx3_server <服务器>`|`+服务器、+开服`|`获取服务器状态。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_server_status.png)|

#### 获取周常

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_daily`|`+jx3_daily [服务器]`|`+日常、+周常`|`获取日常\|周常。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_daily.png)|

#### 订阅推送

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_subscribe`|`+jx3_subscribe <内容>`|`+订阅、+开启`|`订阅事件推送。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_subscribe.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_subscribe_response.jpg)|
|`+jx3_unsubscribe`|`+jx3_unsubscribe <内容>`|`+退订、关闭`|`取消订阅事件推送。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_unsubscribe.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_unsubscribe_response.jpg)|

> 可供订阅的内容可以在订阅任意一项后，使用`+关于`查看。

> 订阅信息存储在`options.json`中，具体路径为：`src/plugins/jx3/subscribe/options.json`，点[此](https://github.com/codethink-cn/Inkar-Suki/blob/main/src/plugins/jx3/subscribe/options.json)查看。

#### 维护公告/更新查看

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_announce`|`+jx3_announce`|`+维护公告`|`获取维护公告(图片)。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_announce.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_announce_response.jpg)|

### 用户数据类

#### 查询个人奇遇

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_serendipity`|`+jx3_serendipity <服务器> <ID>`|`+奇遇`|`获取个人奇遇记录。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_qiyu.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_qiyu_response.jpg)|
|`+jx3_serendipity_v2`|`+jx3_serendipity_v2 <服务器> <ID>`|`+奇遇v2`|`获取个人奇遇记录（过滤宠物奇遇）。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_serendipity.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_serendipity_response.jpg)|


#### 查询个人装备属性

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_addritube`|`+jx3_addritube <服务器> <ID>`|`+属性v1、+查装v1`|`获取角色装备。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_attribute.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_attribute_response.jpg)|
|`+jx3_addritube_v2`|`+jx3_addritube_v2 <服务器> <ID>`|`+属性、+查装`|`获取自身装备属性(重写)。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_attribute2.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_attribute2_response.jpg)|
|`+jx3_player`|`+jx3_player <服务器> <ID>`|`玩家信息`|`获取玩家信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_playerinfo.png)|

> 默认属性搜索界面已切换至`v2`。

!> `v2`的界面以及素材均来自于`JX3BOX`，但是原理**完全不一致**，`JX3BOX`使用`canvas`画布进行绘制，而音卡使用`PIL`手动测绘坐标进行绘制！

#### 查询个人成就/资历/进度类

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_machi`|`+jx3_machi <服务器> <ID> <成就\|副本>`|`+进度`|`获取某一个副本的成就进度。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_machi.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_machi_response.jpg)|
|`+jx3_achievement_v2`|`+jx3_achievement_v2 <服务器> <ID> <成就\|副本>`|`+进度v2`|`获取某成就或某副本的进度（重写）。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_machi_v2.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_machi_v2_response.jpg)|
|`+jx3_zoneachi`|`+jx3_zoneachi <服务器> <ID> <副本> [难度]`|`+团本成就`|`获取某副本所有成就的完成进度。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_zoneachi.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_zoneachi_response.jpg)|
|`+jx3_zone_detail`|`+jx3_zone_detail <服务器> <ID>`|`+副本总览`|`获取个人副本总览资历概况。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_detail.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_detail_response.png)|

#### 个人副本通关记录

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_zones`|`+jx3_zones <服务器> <ID>`|`+副本`|`获取副本通关记录`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_zone.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_zone_response.jpg)|

#### 个人烟花收放记录

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_firework_v2`|`+jx3_firework_v2 <服务器> <ID>`|`+烟花v2`|`获取个人烟花收发记录。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_firework.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_firework_response.jpg)|

!> 尽量不要将该功能用于捉奸等不良行为！

#### 名剑大会

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_arena 战绩`|`+jx3_arena 战绩 <服务器> <ID> [模式]`|`+名剑 战绩`|`获取名剑大会个人战绩。`|`-`|`暂无`|
|`+jx3_arena 排行`|`+jx3_arena 排行 <模式> <ID>`|`+名剑 排行`|`获取名剑大会排行。`|`-`|`暂无`|
|`+jx3_arena 统计`|`+jx3_arena 统计 <模式> <ID>`|`+名剑 统计`|`获取名剑大会统计信息。`|`-`|`暂无`|


### 信息查询类

#### 科举答案查询

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_exam`|`+jx3_exam <问题关键词>`|`+科举`|`获取科举答案。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_exam.png)|

#### 阵眼效果查询

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_matrix`|`+jx3_matrix <心法>`|`+阵眼`|`获取阵眼效果。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_martix.png)|

#### 心法所有技能

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_skill`|`+jx3_skill <心法> <技能>`|`+技能`|`获取技能。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_skill.png)|

> 由于企鹅公司的制裁，该功能可能无法使用。

#### 获取特定奇穴信息

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_talent`|`+jx3_talent <心法> <奇穴> [赛季]`|`+奇穴`|`获取奇穴信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_talent.png)|

#### 获取BUFF效果

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_buff`|`+jx3_buff <buff>`|`+buff、+debuff`|`获取buff信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_buff.png)|

#### 获取宠物信息

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_pet`|`+jx3_pet`|`+宠物 <名称>`|`获取宠物信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_pet.png)|

#### 获取成就信息

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_adventure`|`+jx3_adventure <成就>`|`+成就`|`获取成就信息（真的只有信息）。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_achi.png)|

> 注意，成就信息是真的只有信息，需要个人进度查询的请查看前文。

#### 获取任务信息

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_task`|`+jx3_task`|`+任务 <任务名>`|`查询任务信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_task.png)|

#### 获取宏命令

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_macro`|`+jx3_macro <心法>`|`+宏v1`|`查询宏命令。`|`-`|`暂无`|
|`+jx3_macro_v2`|`+jx3_macro_v2 <心法>`|`+宏`|`查询宏命令（对接魔盒）。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_macro.png)||

### 娱乐类

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_random`|`+jx3_random`|`+骚话`|`获取剑网3“万花谷”频道骚话。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_saohua.png)|
|`+jx3_tiangou`|`+jx3_tiangou`|`+舔狗`|`获取舔狗日志。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_tiangou.png)|

### 交易类

#### 查看金价

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_demon`|`+jx3_demon`|`+金价 <服务器>`|`获取金价。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_demon.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_demon_response.jpg)|

#### 外观物价

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_price`|`+jx3_price`|`+物价 <物品>`|`获取外观物价。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_feiniu_wujia.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_feiniu_wujia_response.jpg)|

#### 交易行物品价格

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_trade`|`+jx3_trade <服务器> <物品>`|`+交易行`|`获取交易行物品价格。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_trade.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_trade_response.jpg)|

#### 盆栽蹲号/蹲外观

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_dh`|`+jx3_dh <条件(多个以空格分割)>`|`+蹲号`|`获取盆栽蹲号的角色价格。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_dh.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_dh_response.jpg)|
|`+jx3_wg`|`+jx3_wg <条件(多个以空格分割)>`|`+贴吧物价`|`获取盆栽蹲号的外观价格。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_dh.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_dh_response.jpg)|

### 服务器内信息类

#### 全服奇遇查询

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_statistical`|`+jx3_statistical <服务器> [奇遇]`|`+近期奇遇`|`获取服务器近期奇遇。`|`-`|`暂无`|
|`+jx3_gserendipity`|`+jx3_gserendipity <奇遇>`|`+全服奇遇`|`获取各服特定奇遇记录。`|`-`|`暂无`|
|`+jx3_gstatistical`|`+jx3_gstatistical <奇遇>`|`+全服统计`|`获取全服特定奇遇记录。`|`-`|`暂无`|

#### 阵营沙盘

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_sandbox`|`+jx3_sandbox <服务器>`|`+沙盘`|`获取沙盘。`|`-`|`暂无`|

#### 招募查询

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_recruit`|`+jx3_recruit <服务器> <关键词>`|`+招募`|`获取团队招募。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_recruit.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_recruit_response.png)|
|`+jx3_recruit_local`|`+jx3_recruit_local <服务器> <关键词>`|`+本服招募`|`获取本服的招募，过滤跨服招募。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_recruit_local.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_recruit_local_response.png)|

#### 抓马信息

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_horse`|`+jx3_horse <服务器>`|`+抓马、+马场`|`获取服务器马场信息。`|`-`|`暂无`|
|`+jx3_dilu`|`+jx3_dilu`|`+的卢统计`|`获取全服的卢刷新、捕获及拍卖信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_dilu.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_dilu_response.png)|

#### 副本掉落

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_itemdrop`|`+jx3_itemdrop <服务器> <物品>`|`+掉落`|`获取副本掉落特殊物品。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_itemdrop.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_itemdrop_response.png)|

### 榜单类

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_top100`|`+jx3_top100 <服务器> <BOSS> [团队]`|`+百强`|`获取魔盒秘境百强团信息。`|`-`|`暂无`|
|`+jx3_rank`|`+jx3_rank <个人\|帮会\|战功\|试炼> <服务器> <类型\|门派>`|`+榜单`|`获取榜单。`|`-`|`暂无`|

### 杂类

#### 挂件详情

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_pendents`|`+jx3_pendents <挂件名称>`|`+挂件`|`获取游戏内挂件详情。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_guajian.png)|

#### 随机表情包

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_emoji`|`+jx3_emoji`|`+随机表情`|`从魔盒取一张随机表情包。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_emoji.png)|

#### 奇遇前置/攻略

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_preposition`|`+jx3_preposition <奇遇>`|`+前置`|`获取奇遇前置。`|`-`|`无`|
|`+jx3_recipe`|`+jx3_recipe <奇遇>`|`+攻略`|`获取奇遇攻略。`|`-`|`无`|

> 图片来源于隐元秘鉴，注意版权问题！仅可以在合理使用的范围内使用图片。

> 由于版权问题，此处不提供示例。

#### BOSS掉落物详情

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_drops`|`+jx3_drops <副本> <难度> <BOSS>`|`+掉落列表`|`获取副本掉落列表。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_droplist.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_droplist_response.png)|

> 副本和难度支持模糊搜索，例如`牢`（武狱黑牢）、`25pt`（25人普通）、`dmd`（达摩洞）。

#### 推栏推荐配装

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_eqrec`|`+jx3_receq <心法> [标签]`|`+配装v2`|`获取推栏推荐配装。`|`-`|`暂无`|

#### 本周百战地图

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_monster_v2`|`-jx3_monster`|`+百战`|`获取百战BOSS列表。`|`-`|`暂无`|

!> 对于`-`开头的命令，即使绑定了服务器也不可以省略服务器，但可以正常映射。<br>

> 在`+jx3_machi`命令中，成就允许填写单个成就，请勿使用俗称等非准确名称。<br>
> `副本`支持格式：`25人英雄范阳夜变`（示例）。<br>
> 对于`敖龙岛`以前（不含）的副本，建议使用单成就查询，或使用`团本成就`命令。
>
> 在`+jx3_arena`命令中，当第一参数为`战绩`时，第二参数为`服务器`，第三参数为`ID`。<br>
> 当第一参数为`排行`或`统计`时，第二参数为`模式`，没有第三参数。
> `模式`接受的值：`22`、`33`、`55`。
> 
> 在`+jx3_zoneachi`命令中，如果省略`难度`参数，则为`10人普通`。
>
> 在`+jx3_rank`命令中，<br>
> <br>当第一参数为`个人`时，第二参数为`服务器`，第三参数为类型，接受的值：
> <br>`[名士五十强 老江湖五十强 兵甲藏家五十强 名师五十强 阵营英雄五十强 薪火相传五十强 庐园广记一百强]`。<br>
> <br>当第一参数为`帮会`时，第二参数为`服务器`，第三参数为类型，接受的值：
> <br>`[浩气神兵宝甲五十强 恶人神兵宝甲五十强 浩气爱心帮会五十强 恶人爱心帮会五十强]`。<br>
> <br>当第一参数为`阵营`时，第二参数为`服务器`，第三参数为类型，接受的值：
> <br>`[赛季恶人五十强 赛季浩气五十强 上周恶人五十强 上周浩气五十强 本周恶人五十强 本周浩气五十强]`。<br>
> <br>当第一参数为`试炼`时，第二参数为`服务器`，第三参数为门派，接受的值：
> <br>`[万花 七秀 少林 纯阳 天策 五毒 唐门 明教 苍云 长歌 藏剑 丐帮 霸刀 蓬莱 凌雪 衍天 药宗 刀宗]`。<br>

## minecraft

[Minecraft](https://www.minecraft.net/zh-hans)（我的世界）搜索器。

贡献者：`HornCopper`、`LittleC`。

### 游戏版本

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+mcbv`|`+mcbv`|`-`|`获取目前Minecraft基岩版最新版本。`|`-`|`暂无`|
|`+mcjv`|`+mcjv`|`-`|`获取目前Minecraft Java版最新版本。`|`-`|`暂无`|

### 游戏服务器

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+bes`|`+bes <IP\|Domain>`|`-`|`获取基岩版服务器。`|`-`|`暂无`|
|`+jes`|`+jes <IP\|Domain>`|`-`|`获取Java版服务器`|`-`|`暂无`|

## music

点歌插件。

贡献者：`HornCopper`。

### 歌曲检索

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+search_music`|`+search_music <平台> <歌曲>`|`+搜歌`|`在某平台搜索歌曲。`|`-`|`暂无`|
|`+get_music`|`+get_music <平台> <歌曲> [歌手]`|`+点歌`|`直接获取歌曲最相似候选项。`|`-`|`暂无`|

> `平台`参数会尽可能识别给出的平台，
> <br>这些词语会被识别为`QQ音乐`：<br>
> `["QQ","QQ音乐","qq","q","Q","tx","tc","tencent","腾讯","腾讯音乐","qq音乐","Qq","Qq音乐","qQ","qQ音乐"]`
> <br>这些词语会被识别为`网易云音乐`：<br>
> `["网易","163","网抑云","网抑","网","netease","n","网易云音乐","网抑云音乐","网易云","wy","w"]`<br><br>
> 当歌曲名出现空格时，请使用`_`替代。

## nbnhhsh

[能不能好好说话](https://lab.magiconch.com/nbnhhsh/?from=home)。

> 贡献者：`HornCopper、OasisAkari`。

### 查询缩写含义

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+nbnhhsh`|`+nbnhhsh <词语>`|`+能不能好好说话`|`查询缩略词的含义。`|`-`|`暂无`|

## op

权限管理。

> 贡献者：`HornCopper`。

### 给予权限

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+setop`|`+setop <QQ> <level>`|`+admin、+setadmin`|`设置机器人管理员。`|`10`|`暂无`|

!> 慎给机器人管理员！拥有`10`级权限的用户将可以执行`反弹shell`等操作！

> `10`级用户最多只能设置到`9`级权限，自身可以降低自身的权限，拥有`owner`和`10`级权限的人才可以添加`10`级权限至任何人。

## poem

没什么用的对诗工具。

> 贡献者：`HornCopper`。

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+randomPoem`|`+对诗`|`+对诗`|`与音卡对诗。`|`-`|`暂无`|

> 如果取得胜利，将会获得`50`金币奖励。如果回答错误，会失去`70`枚金币。

## sign

签到工具。

> 贡献者：`HornCopper`。

### 签到

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+签到`|`+签到`|`+打卡`|`签到，所有群同步。`|`-`|`暂无`|
|`+金币`|`+金币`|`+余额`|`查询自身金币余额。`|`-`|`暂无`|

## twenty_four

24点小游戏。

> 贡献者：`DoroWolf`。

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+twentyFour`|`+24点`|`+24点`|`玩24点游戏。`|`-`|`暂无`|

> 如果取得胜利，将会获得`50`金币奖励。如果回答“无解”错误，则会失去`50`枚金币。

### 管理工具

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+增加金币`|`+增加金币 <QQ号> <增加量>`|`-`|`向某用户的账户增加金币。`|`-`|`暂无`|
|`+减少金币`|`+减少金币 <QQ号> <减少量>`|`-`|`向某用户的账户减少金币。`|`-`|`暂无`|

> 金币可用于漂流瓶的投掷。

## wiki

Wiki（维基）搜索。

> 贡献者：`HornCopper`。

### 在起始Wiki搜索

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+wiki`|`+wiki [iwprefix:]<title>`|`-`|`搜索起始Wiki的相关内容，可以使用该Wiki定义好的Interwiki前缀。`|`-`|`暂无`|

> 如果没有绑定起始Wiki，将搜索失败。

### 设置起始Wiki

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+setwiki`|`+setwiki <wikilink>`|`-`|`设置一个起始Wiki，使用任意Wiki页面均可。`|`-`|`暂无`|

> 该起始Wiki仅在本群聊生效。

### 设置跨Wiki前缀

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+interwiki`|`+interwiki <add\|del\|upd> <prefix> <wikilink>`|`+iw`|`设置一个自定义Interwiki前缀。`|`5/群`|`暂无`|

### 搜索跨Wiki内容

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+iwiki`|`+iwiki <iwprefix:><title>`|`-`|`搜索自定义Interwiki内容。`|`-`|`暂无`|

> `+wiki`如果携带`Interwiki`前缀，只能使用该`Wiki`设置的`Interwiki`前缀，`+iwiki`必须携带`Interwiki`前缀，且只能使用自定义前缀。

## 参见

* [FAQ](/faq)
* [更新日志](/changelog)
* [开发](/develop)
