## jx3 - 剑网3

本文档有简化后的版本，[点击查看](/jx3_easy.md)。

[剑网3](https://jx3.xoyo.com)查询工具。

贡献者：`HornCopper`、`Serfend`、`OasisAkari`。

> 当群聊绑定服务器后，命令中`必选`的`服务器`均为`可选`。

### 服务器和新闻类

#### 绑定群聊

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_bind`|`+jx3_bind <服务器>`|`+绑定`|`绑定群聊区服。`|`8/群管`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_bind.png)|

#### 获取新闻列表

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_news`|`+jx3_news`|`+新闻`|`获取官方最近4条新闻。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_news.png)|

#### 获取开服信息

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_server`|`+jx3_server <服务器>`|`+开服`|`获取服务器状态。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_server_status.png)|

#### 获取日常

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_daily`|`+jx3_daily`|`+日常`|`获取日常\|周常。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_daily.png)|
|`+jx3_calendar|`+jx3_calendar`|`+活动日历`、`+剑三日历`|`获取7天内日常。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_calendar.png)|

#### 功能开关

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_subscribe`|`+jx3_subscribe <内容>`|`+订阅`、`+开启`|`订阅事件推送。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_subscribe.png)|
|`+jx3_unsubscribe`|`+jx3_unsubscribe <内容>`|`+退订、关闭`|`取消订阅事件推送。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_unsubscribe.png)|
|`+jx3_about`|`+jx3_about`|`+关于`|`查看群聊功能开关等信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_about.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_about_response.png)|

> 可供订阅的内容或附加功能可以在订阅任意一项后，使用`+关于`查看。

> 订阅信息存储在`options.json`中，具体路径为：`src/plugins/jx3/subscribe/options.json`，点[此](https://github.com/codethink-cn/Inkar-Suki/blob/main/src/plugins/jx3/subscribe/options.json)查看。

> 附加功能存储在`addtions.json`中，具体路径为：`src/plugins/jx3/subscribe/addtions.json`，点[此](https://github.com/codethink-cn/Inkar-Suki/blob/main/src/plugins/jx3/subscribe/addtions.json)查看。

#### 维护公告/更新查看

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_announce`|`+jx3_announce`|`+维护公告`、`+更新公告`、`+公告`、`+更新`|`获取维护公告(图片)。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_announce.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_announce_response.jpg)|

### 用户数据类

#### 查询个人奇遇

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_serendipity`|`+jx3_serendipity <服务器> <ID>`|`+奇遇`、`+查询`|`获取个人奇遇记录。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_qiyu.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_qiyu_response.jpg)|
|`+jx3_serendipity_v2`|`+jx3_serendipity_v2 <服务器> <ID>`|`+奇遇v2`|`获取个人奇遇记录（过滤宠物奇遇）。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_serendipity.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_serendipity_response.png)|
|`+jx3_pet_serendipity`|`+jx3_pet_serendipity <服务器> <ID>`|`+宠物奇遇`|`获取个人宠物奇遇记录（过滤普通和绝世奇遇）。`|`-`|`暂无`|


#### 查询个人装备属性

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_addritube`|`+jx3_addritube <服务器> <ID>`|`+属性v1`、`+查装v1`|`获取角色装备。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_attribute.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_attribute_response.jpg)|
|`+jx3_addritube_v2`|`+jx3_addritube_v2 <服务器> <ID>`|`+属性`、`+查装`|`获取自身装备属性(重写)。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_attribute2.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_attribute2_response.jpg)|
|`+jx3_player`|`+jx3_player <服务器> <ID>`|`+玩家信息`|`获取玩家信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_playerinfo.png)|

> 默认属性搜索界面已切换至`v2`。

!> `v2`的界面以及素材均来自于`JX3BOX`，但是原理**完全不一致**，`JX3BOX`使用`canvas`画布进行绘制，而音卡使用`PIL`手动测绘坐标进行绘制！

#### 查询个人成就/资历/进度类

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_machi`|`+jx3_machi <服务器> <ID> <成就\|副本>`|`+进度`|`获取某一个副本的成就进度。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_machi.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_machi_response.jpg)|
|`+jx3_achievement_v2`|`+jx3_achievement_v2 <服务器> <ID> <成就\|副本>`|`+进度v2`|`获取某成就或某副本的进度（重写）。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_machi_v2.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_machi_v2_response.jpg)|
|`+jx3_zoneachi`|`+jx3_zoneachi <服务器> <ID> <副本> [难度]`|`+团本成就`|`获取某副本所有成就的完成进度。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_zoneachi.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_zoneachi_response.jpg)|
|`+jx3_zone_detail`|`+jx3_zone_detail <服务器> <ID>`|`+副本总览`|`获取个人副本总览资历概况。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_detail.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_detail_response.png)|

> 在`+jx3_zoneachi`命令中，如果省略`难度`参数，则为`10人普通`。

> 在`+jx3_machi`命令中，成就允许填写单个成就，请勿使用俗称等非准确名称。<br>
> `副本`支持格式：`25人英雄范阳夜变`（示例）。<br>
> 对于`敖龙岛`以前（不含）的副本，建议使用单成就查询，或使用`团本成就`命令。

#### 个人副本通关记录

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_zones`|`+jx3_zones <服务器> <ID>`|`+副本`|`获取副本通关记录`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_zone.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_zone_response.jpg)|

#### 个人烟花收放记录

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_firework_v2`|`+jx3_firework_v2 <服务器> <ID>`|`+烟花v2`|`获取个人烟花收发记录。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_firework.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_firework_response.jpg)|

!> 尽量不要将该功能用于捉奸等不良行为！

#### 名剑大会

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_arena 战绩`|`+jx3_arena 战绩 <服务器> <ID> [模式]`|`+名剑 战绩`|`获取名剑大会个人战绩。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_arena_record.png)|
|`+jx3_arena 排行`|`+jx3_arena 排行 <模式>`|`+名剑 排行`|`获取名剑大会排行。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_arena_rank.png)|
|`+jx3_arena 统计`|`+jx3_arena 统计 <模式>`|`+名剑 统计`|`获取名剑大会统计信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_arena_stastic.png)|

> 在`+jx3_arena`命令中，当第一参数为`战绩`时，第二参数为`服务器`，第三参数为`ID`，第四参数为**可选**的`模式`（默认为`22`）。<br>
> 当第一参数为`排行`或`统计`时，第二参数为`模式`，没有第三参数。
> `模式`接受的值：`22`、`33`、`55`。

#### 骗子查询

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_cheater`|`+jx3_cheater <QQ>`|`+骗子`、`+查人`|`获取某个QQ的贴吧记录。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_cheater.png)|


### 信息查询类

#### 科举答案查询

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_exam`|`+jx3_exam <问题关键词>`|`+科举`|`获取科举答案。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_exam.png)|

#### 阵眼效果查询

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_matrix`|`+jx3_matrix <心法>`|`+阵眼`|`获取阵眼效果。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_martix.png)|

#### 获取特定奇穴信息

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_talent`|`+jx3_talent <心法> <奇穴> [赛季]`|`+奇穴`|`获取奇穴信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_talent.png)|

#### 获取BUFF效果

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_buff`|`+jx3_buff <buff>`|`+buff`、`+debuff`|`获取buff信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_buff.png)|

#### 获取宠物信息

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_pet`|`+jx3_pet`|`+宠物 <名称>`|`获取宠物信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_pet.png)|

#### 获取成就信息

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_adventure`|`+jx3_adventure <成就>`|`+成就`|`获取成就信息（真的只有信息）。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_achi.png)|

> 注意，成就信息是真的只有信息，需要个人进度查询的请查看前文。

#### 获取任务信息

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_task`|`+jx3_task`|`+任务 <任务名>`|`查询任务信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_task.png)|

#### 获取宏命令

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_macro_v2`|`+jx3_macro_v2 <心法>`|`+宏`|`查询宏命令（对接魔盒）。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_macro.png)|

#### 统战YY

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_duowan`|`+jx3_duowan <区服>`|`+统战`|`查询目标区服统战YY。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_duowan.png)|


### 娱乐类

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_random`|`+jx3_random`|`+骚话`|`获取剑网3“万花谷”频道骚话。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_saohua.png)|
|`+jx3_tiangou`|`+jx3_tiangou`|`+舔狗`|`获取舔狗日志。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_tiangou.png)|

### 交易类

#### 查看金价

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_demon`|`+jx3_demon`|`+金价 <服务器>`|`获取金价。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_demon.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_demon_response.jpg)|

#### 外观物价

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_price`|`+jx3_price`|`+物价 <物品>`|`获取外观物价。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_feiniu_wujia.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_feiniu_wujia_response.jpg)|

#### 交易行物品价格

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_trade`|`+jx3_trade <服务器> <物品>`|`+交易行`|`获取交易行物品价格（不支持无封）。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_trade.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_trade_response.jpg)|
|`+jx3_wufeng`|`+jx3_trade <服务器> <词条>`|`+交易行无封`|`获取交易行无封数据。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_trade_wufeng.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_trade_wufeng_response.png)|

#### 盆栽蹲号/蹲外观

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_dh`|`+jx3_dh <条件(多个以空格分割)>`|`+蹲号`|`获取盆栽蹲号的角色价格。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_dh.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_dh_response.jpg)|
|`+jx3_wg`|`+jx3_wg <条件(多个以空格分割)>`|`+贴吧物价`|`获取盆栽蹲号的外观价格。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_price_tieba.png)|

### 服务器内信息类

#### 全服奇遇查询

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_statistical`|`+jx3_statistical <服务器> [奇遇]`|`+近期奇遇`|`获取服务器近期奇遇。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_recent_serendipity.png)|
|`+jx3_gserendipity`|`+jx3_gserendipity <奇遇>`|`+全服奇遇`|`获取各服特定奇遇记录。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_single_serendipity.png)|
|`+jx3_gstatistical`|`+jx3_gstatistical <奇遇>`|`+全服统计`|`获取全服特定奇遇记录。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_all_serendipity.png)|


#### 阵营沙盘

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_sandbox`|`+jx3_sandbox <服务器>`|`+沙盘`|`获取沙盘。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_sandbox.png)|

#### 招募查询

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_recruit`|`+jx3_recruit <服务器> <关键词>`|`+招募v1`|`获取团队招募。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_recruit.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_recruit_response.jpg)|
|`+jx3_recruit_v2`|`+jx3_recruit <服务器> <关键词>`|`+招募`|`获取团队招募。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_recruit_v2.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_recruit_v2_response.png)|
|`+jx3_recruit_local`|`+jx3_recruit_local <服务器> <关键词>`|`+本服招募`|`获取本服的招募，过滤跨服招募。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_recruit_local.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_recruit_local_response.png)|

> **附加功能：**`招募过滤`。
>
> 对招募的内容进行检测，将疑似广告的招募进行隐藏处理。

#### 抓马信息

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_horse`|`+jx3_horse <服务器>`|`+抓马`、`+马场`|`获取服务器马场信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_horse.png)|
|`+jx3_dilu`|`+jx3_dilu`|`+的卢统计`|`获取全服的卢刷新、捕获及拍卖信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_dilu.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_dilu_response.png)|

#### 副本掉落

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_itemdrop`|`+jx3_itemdrop <服务器> <物品>`|`+掉落`|`获取副本掉落特殊物品。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_itemdrop.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_itemdrop_response.png)|

### 榜单类

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_top100`|`+jx3_top100 <服务器> <BOSS> [团队]`|`+百强`|`获取魔盒秘境百强团信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_top100.png)|
|`+jx3_rank`|`+jx3_rank <个人\|帮会\|战功\|试炼> <服务器> <类型\|门派>`|`+榜单`|`获取榜单。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_rank.png)|
!> 由于参数过于多样化，此处不提供图片示例！

> <br>当第一参数为`个人`时，第二参数为`服务器`，第三参数为类型，接受的值：
> <br>`[名士五十强 老江湖五十强 兵甲藏家五十强 名师五十强 阵营英雄五十强 薪火相传五十强 庐园广记一百强]`。<br>
> <br>当第一参数为`帮会`时，第二参数为`服务器`，第三参数为类型，接受的值：
> <br>`[浩气神兵宝甲五十强 恶人神兵宝甲五十强 浩气爱心帮会五十强 恶人爱心帮会五十强]`。<br>
> <br>当第一参数为`阵营`时，第二参数为`服务器`，第三参数为类型，接受的值：
> <br>`[赛季恶人五十强 赛季浩气五十强 上周恶人五十强 上周浩气五十强 本周恶人五十强 本周浩气五十强]`。<br>
> <br>当第一参数为`试炼`时，第二参数为`服务器`，第三参数为门派，接受的值：
> <br>`[万花 七秀 少林 纯阳 天策 五毒 唐门 明教 苍云 长歌 藏剑 丐帮 霸刀 蓬莱 凌雪 衍天 药宗 刀宗 万灵]`。<br>

### 杂类

#### 楚天云从

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_zhue`|`+jx3_zhue`|`+诛恶`|`获取服务器近期诛恶记录。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_zhue.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_zhue_response.png)|
|`+jx3_chutian`|`+jx3_chutian`|`+楚天社`|`获取当前楚天社阶段`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_chutian.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_chutian_response.png)|
|`+jx3_yuncong`|`+jx3_yuncong`|`+云从社`|`获取当前云从社阶段`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_yuncong.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_yuncong_response.png)|

#### 挂件详情

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_pendents`|`+jx3_pendents <挂件名称>`|`+挂件`|`获取游戏内挂件详情。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_guajian.png)|

#### 随机表情包

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_emoji`|`+jx3_emoji`|`+随机表情`|`从魔盒取一张随机表情包。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_emoji.png)|

#### 奇遇前置/攻略

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_preposition`|`+jx3_preposition <奇遇>`|`+前置`、`+攻略`|`获取奇遇攻略。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_preposition.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_preposition_response.png)|

#### BOSS掉落物详情

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_drops`|`+jx3_drops <副本> <难度> <BOSS>`|`+掉落列表`|`获取副本掉落列表。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_droplist.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_droplist_response.png)|

> 副本和难度支持模糊搜索，例如`牢`（武狱黑牢）、`25pt`（25人普通）、`dmd`（达摩洞）。

#### 推栏推荐配装

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_eqrec`|`+jx3_receq <心法> [标签]`|`+配装v2`|`获取推栏推荐配装。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_equiprec.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_equiprec_response.png)|

#### 本周百战地图

|命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_monster_v2`|`-jx3_monster`|`+百战`|`获取百战BOSS列表。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_monsters.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_monsters_response.png)|

!> 对于`-`开头的命令，即使绑定了服务器也不可以省略服务器，但可以正常映射。<br>
