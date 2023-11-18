# 使用

`Inkar Suki`是一个开源的项目，它自身具有的功能相当多样，同时非常欢迎社区成员对我们的项目进行贡献！

> 本章节所有命令中，以`+`开头的命令可以省略前方的任何标点，以`-`开头的表示只能且必须使用`-`作为前缀。
>
> 例如`+cmd`，使用`cmd`即可触发，而`-cmd`只可使用`-cmd`触发。
>
> 本章节中带`<>`的参数为必选参数，带`[]`的参数为可选参数，可以省略。

## Arcaea

`Arcaea`（韵律源点）相关功能。

贡献者：`HornCopper`。

> 该插件需要注册才可使用。

> 当用户已使用`+arcbind`进行绑定后，`+arcuser`不需要使用参数，且`+arcbest`需要绑定后才可使用。

!> 由于`Arcaea Unlimited API`的相关变动，该功能可能暂时失效。<br>
`Arcara Unlimited API`已改变为`Unoffical Arcaea API`。

|命令|格式|别名|描述|权限|示例|
|-----|-----|-----|-----|-----|-----|
|`+arcuser`|`+arcuser <usercode\|username>`|`-`|`查询用户信息和最近一次游玩记录。`|`-`|`暂无`|
|`+arcbind`|`+arcbind <usercode\|username>`|`-`|`在群内绑定自己的Arcaea账号。`|`-`|`暂无`|
|`+arcbest`|`+arcbest <songname> <difficulty>`|`-`|`查询个人单曲最佳成绩。`|`-`|`暂无`|
|`+arcunbind`|`+arcunbind`|`-`|`在群内取消绑定自己的Arcaea账号。`|`-`|`暂无`|

`usercode`是用户码，`username`是昵称。

`songname`是歌曲名，`difficulty`是难度，有`pst``prs``ftr``byn`等。

> `usercode`只接受纯数字，`difficulty`也接受`0-3`、全称等。

## Assistance

`剑网3`开团工具。

贡献者：`HornCopper`。

> 该插件需要注册才可使用。<br>
> 该插件需要绑定服务器后才可以使用。

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+创建团队`|`+创建团队 <关键词>`|`-`|`群内创建团队。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/create_team.png)|
|`+预定`|`+预定 <关键词> <ID> <职业>`|`+预订、+报名`|`群内预定留坑。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/book.png)|
|`+取消预定`|`+取消预定 <关键词> <ID>`|`+取消报名、+取消预订`|`群内取消留坑。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/cancel_book.png)|
|`+解散团队`|`+解散团队 <关键词>`|`+取消开团`|`解散一个现有的团队。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/delete_team.png)|
|`+查看团队`|`+查看团队 <关键词>`|`-`|`查看一个现有的团队。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/team_status.png)|
|`+随机抽取`|`+随机抽取 <关键词>`|`-`|`在一个现有的团队中随机抽取一个团队成员。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/random_team.png)|

## ban

`Inkar Suki`封禁系统。

贡献者：`HornCopper`。

> 该插件需要注册才可使用。

> 当权限等级为`10`时，免疫该机制。

|命令|格式|别名|描述|权限|
|-----|-----|-----|-----|-----|
|`+ban`|`+ban <QQ>`|`-`|`封禁一个指定用户。`|`10`|
|`+unban`|`+unban <QQ>`|`-`|`解封一个指定用户。`|`10`|

该插件具有一个消息检测器，每一条消息均会进行检测发送人是否被封禁，如果是，则阻断该次事件的再次传递。

> 该插件全域生效。

!> 当尝试封禁配置文件中`owner`列表中用户时，自身会被封禁，~~还会被嘲讽~~。

## banword

`Inkar Suki`违禁词系统。

贡献者：`HornCopper`。

> 该插件需要注册才可使用。

> 当权限等级**≥**`5`时，免疫该机制。

|命令|格式|别名|描述|权限|
|-----|-----|-----|-----|-----|
|`+banword`|`+banword <word>`|`-`|`封禁一个指定词语。`|`-`|
|`+unbanword`|`+unbanword <word>`|`-`|`解封一个指定词语。`|`-`|

该插件也具有一个消息检测器，每一条消息均会检测消息中是否包含违禁词，如果是，则禁言（`1min`）并撤回。

## blacklist

避雷名单。

贡献者：`HornCopper`。

> 该插件需要注册才可使用。

|命令|格式|别名|描述|权限|
|-----|-----|-----|-----|-----|
|`+block`|`+block <person> <reason>`|`+加黑、+避雷`|`将某人添加至群内避雷名单。`|`5/群`|
|`+unblock`|`+unblock <person>`|`+删黑`|`解除某人的避雷。`|`5/群`|
|`+sblock`|`+sblock <person>`|`+查黑`|`查询某人是否在避雷名单中。`|`-`|
|`+lblock`|`+lblock`|`+列黑`|`查询所有避雷人员。`|`-`|

## developer_tools

用于给`开发者`进行调试的插件。

贡献者：`HornCopper`。

> 该插件需要注册才可使用。

|命令|格式|别名|描述|权限|
|-----|-----|-----|-----|-----|
|`+purge`|`+purge`|`-`|`清除图片缓存。`|`1`|
|`+shutdown`|`+shutdown`|`+poweroff`|`关闭Inkar Suki。`|`10`|
|`+restart`|`+restart`|`-`|`重启Inkar Suki。`|`5`|
|`+echo`|`+echo <msg>`|`-`|`让Inkar Suki发送指定信息。`|`9`|
|`+say`|`+say <msg\|CQCode>`|`-`|`让Inkar Suki发送指定信息，会解析其中的CQ码。`|`9`|
|`+ping`|`+ping`|`-测试`|`测试Inkar Suki是否处于能够处理消息的状态。`|`-`|
|`+back`|`+back <cmd>`|`-`|`让Inkar Suki在后台执行操作。`|`10`|
|`+front`|`+front <cmd>`|`-`|`让Inkar Suki执行操作，并返回输出信息。`|`10`|
|`+post`|`+post <msg>`|`-公告`|`向Inkar Suki加入的所有群聊发送指定信息。`|`10`|
|`+call_api`|`+call_api <api>`|`+api`|`调用Go-CQHTTP的HTTP API。`|`10`|

> 若发送`+ping`的人具有至少`1`级权限，则会回复系统占用等信息。

!> 若有群聊禁言了`Inkar Suki`，可能会因为发送消息失败（误判为风控等）导致全域公告发送不完全。<br>
若未正确填写`cqhttp`（配置文件）的值，会导致`+call_api`调用失败。

## event_notice

事件响应器。

贡献者：`HornCopper`。

> 该插件需要注册才可使用。

|命令|格式|别名|描述|权限|
|-----|-----|-----|-----|-----|
|`+welcome`|`+welcome <msg>`|`-`|`设置入群欢迎语。`|`5/群`|

> 如果`Inkar Suki`被移出群聊，将会封禁此人。

!> 如果您使用的是公共`Inkar Suki`且不想再继续使用，请联系`HornCopper`进行退群而绝不是自行将`Inkar Suki`移出群聊。

## github

GitHub处理器。

贡献者：`HornCopper`。

> 该插件需要注册才可使用。

!> 该插件涉及到`Webhook`，请确保您的网络安全，概不负责。<br>
如果您使用的是内网，可以考虑使用内网穿透技术或不使用`Webhook`。

|命令|格式|别名|描述|权限|
|-----|-----|-----|-----|-----|
|`+repo`|`+repo <author/repository>`|`-`|`查看GitHub仓库。`|`-`|
|`+bindrepo`|`+bindrepo <author/repository>`|`+webhook`|`绑定仓库，使收到的属于该仓库的Webhook全部推送至该群聊。`|`9/群`|
|`+unbindrepo`|`+unbindrepo <author/repository>`|`+unbind_webhook`|`解绑仓库，功能同上相反。`|`9/群`|

## grab

综合搜索器。

贡献者：`HornCopper`、`Serfend`。

> 该插件需要注册才可使用。

> 本插件中的`/`表示的是多选一。

|命令|格式|别名|描述|权限|
|-----|-----|-----|-----|-----|
|`+[今/明/后][天/日]<早上/中午/晚上><吃/喝><什么/啥/点啥>`|`-`|`-`|`让Inkar Suki决定自己某顿吃什么。`|`-`|
|`+查[看/询]<菜/饮><单/料/品>`|`-`|`-`|`查看目前的菜品。`|`-`|
|`+添[加]<菜/饮><单/料/品>`|`-`|`-`|`添加菜品到数据中。`|`-`|
|`+删[除]<菜/饮><单/料/品>`|`-`|`-`|`将数据中某一菜品删除。`|`-`|
|`-tieba`|`-tieba <tid>`|`-贴吧`|`查询某一帖子的信息。`|`-`|
|`+jx3_cheater`|`+jx3_cheater <QQ>`|`-骗子、-查人`|`查询某人是否在贴吧被避雷。`|`-`|

## help

帮助文件。

贡献者：`HornCopper`、`OasisAkari`。

> 该插件需要注册才可使用。

|命令|格式|别名|描述|权限|
|-----|-----|-----|-----|-----|
|`+help`|`+help [plugin]`|`+帮助、+功能`|`查看帮助文件，实时生成。`|`-`|

## jx3

[剑网3](https://jx3.xoyo.com)搜索器。

贡献者：`HornCopper`、`Serfend`、`OasisAkari`。

> 该插件需要注册才可使用。

> 当群聊绑定服务器后，命令中`必选`的`服务器`均为`可选`。

### 服务器和新闻类

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_news`|`+jx3_news`|`+新闻`|`获取官方最近4条新闻。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_news.png)|
|`+jx3_server`|`+jx3_server <服务器>`|`+服务器、+开服`|`获取服务器状态。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/server_status.png)|
|`+jx3_daily`|`+jx3_daily [服务器]`|`+日常、+周常`|`获取日常\|周常。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_daily.png)|
|`+jx3_subscribe`|`+jx3_subscribe <内容>`|`+订阅`|`订阅事件推送。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/subscribe.png)/[返回图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/subscribe_response.jpg)|
|`+jx3_unsubscribe`|`+jx3_unsubscribe <内容>`|`+退订`|`取消订阅事件推送。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/unsubscribe.png)/[返回图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/unsubscribe_response.jpg)|
|`+jx3_announce`|`+jx3_announce`|`+维护公告`|`获取维护公告(图片)。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_announce.png)/[返回图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_announce_response.jpg)|

### 用户数据类

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_serendipity`|`+jx3_serendipity <服务器> <ID>`|`+奇遇`|`获取个人奇遇记录。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_qiyu.png)/[返回图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_qiyu_response.jpg)|
|`+jx3_addritube`|`+jx3_addritube <服务器> <ID>`|`+属性、+查装`|`获取角色装备。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_attribute.png)/[返回图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_attribute_response.jpg)|
|`+jx3_machi`|`+jx3_machi <服务器> <ID> <成就\|副本>`|`+进度`|`获取某一个副本的成就进度。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_machi.png)/[返回图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_machi_response.jpg)|
|`+jx3_achievement_v2`|`+jx3_achievement_v2 <服务器> <ID> <成就\|副本>`|`+进度v2`|`获取某成就或某副本的进度（重写）。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_machi_v2.png)/[返回图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_machi_v2_response.jpg)|
|`+jx3_zoneachi`|`+jx3_zoneachi <服务器> <ID> <副本> [难度]`|`+团本成就`|`获取某副本所有成就的完成进度。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_zoneachi.png)/[返回图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_zoneachi_response.jpg)|
|`+jx3_player`|`+jx3_player <服务器> <ID>`|`玩家信息`|`获取玩家信息。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_playerinfo.png)|
|`+jx3_zones`|`+jx3_zones <服务器> <ID>`|`+副本`|`获取副本通关记录，特别感谢@厌睢 提供的猫猫头素材！`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_zone.png)/[返回图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_zone_response.jpg)|
|`+jx3_firework_v2`|`+jx3_firework_v2 <服务器> <ID>`|`+烟花v2`|`获取个人烟花收发记录。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_firework.png)/[返回图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_firework_response.jpg)|
|`+jx3_addritube_v2`|`+jx3_addritube_v2 <服务器> <ID>`|`+属性v2`|`获取自身装备属性(重写)。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_attribute2.png)/[返回图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_attribute2_response.jpg)|
|`+jx3_arena`|`+jx3_arena <战绩\|排行\|统计> <服务器\|模式> <ID>`|`+名剑`|`获取名剑大会信息。`|`-`|


### 信息查询类

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_exam`|`+jx3_exam <问题关键词>`|`+科举`|`获取科举答案。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_exam.png)|
|`+jx3_matrix`|`+jx3_matrix <心法>`|`+阵眼`|`获取阵眼效果。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_martix.png)|
|`+jx3_skill`|`+jx3_skill <心法> <技能>`|`+技能`|`获取技能。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_skill.png)|
|`+jx3_talent`|`+jx3_talent <心法> <奇穴> [赛季]`|`+奇穴`|`获取奇穴信息。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_talent.png)|
|`+jx3_buff`|`+jx3_buff <buff>`|`+buff、+debuff`|`获取buff信息。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_buff.png)|
|`+jx3_pet`|`+jx3_pet`|`+宠物 <名称>`|`获取宠物信息。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_pet.png)|
|`+jx3_adventure`|`+jx3_adventure <成就>`|`+成就`|`获取成就信息。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_achi.png)|
|`+jx3_task`|`+jx3_task`|`+任务 <任务名>`|`查询任务信息。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_task.png)|
|`+jx3_macro`|`+jx3_macro <心法>`|`+宏`|`查询宏命令。`|`-`|`暂无`|
|`+jx3_ct`|`+jx3_ct <服务器>`|`+赤兔`|`获取赤兔刷新。`|`-`|`暂无`|
|`+jx3_bind`|`+jx3_bind <服务器>`|`+绑定`|`绑定群聊区服。`|`8/群`|`暂无`|

### 娱乐类

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_random`|`+jx3_random`|`+骚话`|`获取剑网3“万花谷”频道骚话。`|`-`|[例图](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_saohua.png)|
|`+jx3_tiangou`|`+jx3_tiangou`|`+舔狗`|`获取舔狗日志。`|`-`|`暂无`|

### 交易类

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_demon`|`+jx3_demon`|`+金价 <服务器>`|`获取金价。`|`-`|`暂无`|
|`+jx3_price`|`+jx3_price`|`+物价 <物品>`|`获取外观物价。`|`-`|`暂无`|
|`+jx3_trade`|`+jx3_trade <服务器> <物品>`|`+交易行`|`获取交易行物品价格。`|`-`|`暂无`|
|`+jx3_wbl`|`+jx3_wbl <角色/外观> <编号>`|`+万宝楼`|`获取万宝楼商品价格。`|`-`|`暂无`|
|`+jx3_dh`|`+jx3_dh <条件>`|`+蹲号`|`获取盆栽蹲号。`|`-`|`暂无`|

### 服务器内信息类

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_statistical`|`+jx3_statistical <服务器> [奇遇]`|`+近期奇遇`|`获取服务器近期奇遇。`|`-`|`暂无`|
|`+jx3_gserendipity`|`+jx3_gserendipity <奇遇>`|`+全服奇遇`|`获取各服特定奇遇记录。`|`-`|`暂无`|
|`+jx3_gstatistical`|`+jx3_gstatistical <奇遇>`|`+全服统计`|`获取全服特定奇遇记录。`|`-`|`暂无`|
|`+jx3_sandbox`|`+jx3_sandbox <服务器>`|`+沙盘`|`获取沙盘。`|`-`|`暂无`|
|`+jx3_cd`|`+jx3_cd <服务器> <物品\|奇遇>`|`+cd`|`获取各种奇遇的上次触发。`|`-`|`暂无`|
|`+jx3_recruit`|`+jx3_recruit <服务器> <关键词>`|`+招募`|`获取团队招募。`|`-`|`暂无`|
|`+jx3_horse`|`+jx3_horse <服务器>`|`+抓马、+马场`|`获取服务器马场信息。`|`-`|`暂无`|
|`+jx3_dilu`|`+jx3_dilu`|`+的卢统计`|`获取全服的卢刷新、捕获及拍卖信息。`|`-`|`暂无`|

### 榜单类

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_top100`|`+jx3_top100 <服务器> <BOSS> [团队]`|`+百强`|`获取魔盒秘境百强团信息。`|`-`|`暂无`|
|`+jx3_rank`|`+jx3_rank <个人\|帮会\|战功\|试炼> <服务器> <类型\|门派>`|`+榜单`|`获取榜单。`|`-`|`暂无`|
|`+jx3_zlrank`|`+jx3_zlrank [服务器] <门派>`|`+资历排行`|`获取资历排行榜。`|`-`|`暂无`|

### 杂类

|命令|格式|别名|描述|权限|图片示例|
|-----|-----|-----|-----|-----|-----|
|`+jx3_item`|`+jx3_item <物品ID>`|`+物品`|`获取物品截图。`|`-`|`暂无`|
|`+jx3_preposition`|`+jx3_preposition <奇遇>`|`+前置`|`获取奇遇前置。`|`-`|`暂无`|
|`+jx3_recipe`|`+jx3_recipe <奇遇>`|`+攻略`|`获取奇遇攻略。`|`-`|`暂无`|
|`+jx3_drops`|`+jx3_drops <副本> <难度> <BOSS>`|`+掉落列表`|`获取副本掉落列表。`|`-`|`暂无`|
|`+jx3_eqrec`|`+jx3_receq <心法> [标签]`|`+配装v2`|`获取推栏推荐配装。`|`-`|`暂无`|
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

> 该插件需要注册才可使用。

|命令|格式|别名|描述|权限|
|-----|-----|-----|-----|-----|
|`+mcbv`|`+mcbv`|`-`|`获取目前Minecraft基岩版最新版本。`|`-`|
|`+mcjv`|`+mcjv`|`-`|`获取目前Minecraft Java版最新版本。`|`-`|
|`+bes`|`+bes <IP\|Domain>`|`-`|`获取基岩版服务器。`|`-`|
|`+jes`|`+jes <IP\|Domain>`|`-`|`获取Java版服务器`|`-`|

## music

点歌插件。

贡献者：`HornCopper`。

> 该插件需要注册才可使用。

|命令|格式|别名|描述|权限|
|-----|-----|-----|-----|-----|
|`+search_music`|`+search_music <平台> <歌曲>`|`+搜歌`|`在某平台搜索歌曲。`|`-`|
|`+get_music`|`+get_music <平台> <歌曲> [歌手]`|`+点歌`|`直接获取歌曲最相似候选项。`|`-`|

> `平台`参数会尽可能识别给出的平台，
> <br>这些词语会被识别为`QQ音乐`：<br>
> `["QQ","QQ音乐","qq","q","Q","tx","tc","tencent","腾讯","腾讯音乐","qq音乐","Qq","Qq音乐","qQ","qQ音乐"]`
> <br>这些词语会被识别为`网易云音乐`：<br>
> `["网易","163","网抑云","网抑","网","netease","n","网易云音乐","网抑云音乐","网易云","wy","w"]`<br><br>
> 当歌曲名出现空格时，请使用`_`替代。

## nbnhhsh

[能不能好好说话](https://lab.magiconch.com/nbnhhsh/?from=home)。

> 贡献者：`HornCopper`。

> 该插件需要注册才可使用。

|命令|格式|别名|描述|权限|
|-----|-----|-----|-----|-----|
|`+nbnhhsh`|`+nbnhhsh <词语>`|`+能不能好好说话`|`查询缩略词的含义。`|`-`|

## op

权限管理。

> 贡献者：`HornCopper`。

> 该插件需要注册才可使用。

|命令|格式|别名|描述|权限|
|-----|-----|-----|-----|-----|
|`+setop`|`+setop <QQ> <level>`|`+admin、+setadmin`|`设置机器人管理员。`|`10`|

!> 慎给机器人管理员！拥有`10`级权限的用户将可以执行`反弹shell`等操作！

> `10`级用户最多只能设置到`9`级权限，自身可以降低自身的权限，拥有`owner`和`10`级权限的人才可以添加`10`级权限至任何人。

## register

注册系统。

> 贡献者：`HornCopper`。

> 该插件中，除`+register`以外需要注册才可使用。

|命令|格式|别名|描述|权限|
|-----|-----|-----|-----|-----|
|`+register`|`+register`|`+reg`|`注册一个新群聊。`|`-`|
|`+flushdata`|`+flushdata`|`-`|`刷新数据，删除所有无效群聊数据。`|`10`|
|`+leave`|`+leave`|`-`|`让Inkar Suki退出群聊。`|`8`|
|`+cleardata`|`+cleardata`|`-`|`让群聊恢复未注册的状态。`|`9`|
|`+shutup`|`+shutup`|`-闭嘴`|`让音卡不再被动响应。`|`群`|
|`+unshutup`|`+unshutup`|`+speak、-解除闭嘴`|`让音卡能够继续响应命令。`|`群`|
|`+fix`|`+fix`|`-`|`修补缺少的数据文件。`|`-`|

## wiki

Wiki（维基）搜索。

> 贡献者：`HornCopper`。

> 该插件需要注册才可使用。

|命令|格式|别名|描述|权限|
|-----|-----|-----|-----|-----|
|`+wiki`|`+wiki [iwprefix:]<title>`|`-`|`搜索起始Wiki的相关内容，可以使用该Wiki定义好的Interwiki前缀。`|`-`|
|`+setwiki`|`+setwiki <wikilink>`|`-`|`设置一个起始Wiki，使用任意Wiki页面均可。`|`-`|
|`+interwiki`|`+interwiki <add\|del\|upd> <prefix> <wikilink>`|`+iw`|`设置一个自定义Interwiki前缀。`|`5/群`|
|`+iwiki`|`+iwiki <iwprefix:><title>`|`-`|`搜索自定义Interwiki内容。`|`-`|

> `+wiki`如果携带`Interwiki`前缀，只能使用该`Wiki`设置的`Interwiki`前缀，`+iwiki`必须携带`Interwiki`前缀，且只能使用自定义前缀，不可使用起始`Wiki`的`Interwiki`前缀。

## 参见

* [FAQ](/faq)
* [更新日志](/changelog)
* [开发](/develop)