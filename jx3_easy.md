# jx3 - 剑网3

**本篇目为主章节的简化版，相信幼儿园毕业也可以看懂，如果仍有问题，请前往文档首页并加入我们的用户群。**

> 当群聊绑定服务器后，- 命令中`必选`的`服务器`（或写为`区服`）均为`可选`，也就是可以不填写，有特殊说明的除外。

**文档里面的大括号，中括号，小括号，麻烦各位实际使用的时候不要打进去，只是起一个标记的作用，表示这是一个参数，不是命令的一部分。**

如果觉得不错的话，点击[这里](/donate)支持下音卡宝宝，~~求求了QAQ~~

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

## 服务器和新闻类

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 绑定群聊

- 命令：`绑定 [服务器]`

!> 如果只发送`绑定`二字（也就是服务器为空），则是清除本群的绑定。

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_bind.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 获取新闻列表

- 命令：`新闻`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_news.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 获取开服信息

- 命令：`开服 <服务器>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_server_status.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 获取日常

- 命令：`日常`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_daily.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

- 命令：`剑三日历`或者`活动日历`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_calendar.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 功能开关

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

#### 订阅推送/开关功能

- 命令：`订阅 <订阅内容>`或者`开启 <订阅内容>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_subscribe.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

- 命令：`退订 <订阅内容>`或者`关闭 <订阅内容>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_unsubscribe.png)

> 什么是`订阅内容`？简而言之，参考下面的- 命令（`关于`），回复的图片中有很多小方框，订阅内容就是他们的标题，一次可以订阅多个内容，以空格分割即可，例如`订阅 玄晶 抓马 扶摇`，退订同理。

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

#### 查看本群订阅信息

- 命令：`关于`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_about.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 维护公告/更新查看

- 命令：`维护公告`或者`更新公告`或者`公告`或者`更新`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_announce.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

## 用户数据类

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 查询个人奇遇

- 命令：`奇遇v1 <服务器> <ID>`或者`查询v1 <服务器> <ID>`

**该- 命令会给出所有奇遇！**

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_qiyu.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

- 命令：`奇遇 <服务器> <ID>`或者`查询 <服务器> <ID>`

**该- 命令会过滤宠物奇遇！**

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_serendipity.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

- 命令：`宠物奇遇 <服务器> <ID>`

**该- 命令会过滤非宠物奇遇！**

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_pet_serendipity.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 查询个人装备属性和基本信息

- 命令：`属性v1 <服务器> <ID>`或者`查装v1 <服务器> <ID>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_attribute.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

- 命令：`属性 <服务器> <ID>`或者`查装 <服务器> <ID>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_attribute2.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

- 命令：`玩家信息 <服务器> <ID>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_playerinfo.png)|

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 查询个人成就/资历/进度类

- 命令：`进度 <服务器> <ID> <关键词>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_machi.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

- 命令：`进度v2 <服务器> <ID> <关键词>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_machi_v2.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

- 命令：`团本成就 <服务器> <ID> <副本名称(不带难度)> [难度(不写就是10人)]`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_zoneachi.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

- 命令：`副本总览 <服务器> <ID>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_detail.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 个人副本通关记录

- 命令：`副本 <服务器> <ID>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_zone.png)

> 灰色小猫头表示已通过，橘色小猫头表示尚未通过。

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 名剑大会

- 命令：`名剑 战绩 <服务器> <ID> [模式(不填就是22)]`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_arena_record.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

- 命令：`名剑 排行 <模式>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_arena_rank.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

- 命令：`名剑 统计 <模式>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_arena_stastic.png)

> 模式有`22`、`33`和`55`。

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 骗子查询

- 命令：`查人 <QQ号>`或`骗子 <QQ号>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_cheater.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

## 信息查询类

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 科举答案查询

- 命令：`科举 <问题关键词>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_exam.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 阵眼效果查询

- 命令：`阵眼 <心法>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_martix.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 获取特定奇穴信息

- 命令：`奇穴 <心法> <奇穴名称>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_talent.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 获取BUFF效果

- 命令：`buff <关键词>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_buff.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 获取宠物信息

- 命令：`宠物 <宠物名>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_pet.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 获取成就信息

- 命令：`成就 <关键词>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_achi.png)

> 注意，成就信息是真的只有信息，需要个人进度查询的请查看`进度`或者`团本成就`。

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 获取任务信息

- 命令：`任务 <关键词>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_task.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 获取宏命令

- 命令：`宏 <心法>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_macro.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 统战YY

- 命令：`统战 <服务器>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_duowan.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

## 娱乐类

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 随机骚话

- 命令：`骚话`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_saohua.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 舔狗日记

- 命令：`舔狗`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_tiangou.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

## 交易类

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 查看金价

- 命令：`金价 <服务器>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_demon.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 外观物价

- 命令：`物价 <关键词>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_feiniu_wujia.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 交易行物品价格

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

#### 一般物品（无封除外）

- 命令：`交易行 <服务器> <关键词>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_trade.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

#### 无封装备

- 命令：`交易行无封 <服务器> <词条>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_trade_wufeng.png)

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

### 盆栽蹲号/蹲外观

- 命令：`蹲号 <条件>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_dh.png)

> 如果有多个条件，请以`空格`分割，例如：`蹲号 军萝 蝶金`。

<div style="border-top: 1px solid black; margin-top: 20px; margin-bottom: 20px;"></div>

- 命令：`贴吧物价 <名称>`

![](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_price_tieba.png)

## 服务器内信息类

### 全服奇遇查询

|- 命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_statistical`|`+jx3_statistical <服务器> [奇遇]`|`+近期奇遇`|`获取服务器近期奇遇。`|`-`|`暂无`|
|`+jx3_gserendipity`|`+jx3_gserendipity <奇遇>`|`+全服奇遇`|`获取各服特定奇遇记录。`|`-`|`暂无`|
|`+jx3_gstatistical`|`+jx3_gstatistical <奇遇>`|`+全服统计`|`获取全服特定奇遇记录。`|`-`|`暂无`|

### 阵营沙盘

|- 命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_sandbox`|`+jx3_sandbox <服务器>`|`+沙盘`|`获取沙盘。`|`-`|`暂无`|

### 招募查询

|- 命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_recruit`|`+jx3_recruit <服务器> <关键词>`|`+招募v1`|`获取团队招募。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_recruit.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_recruit_response.jpg)|
|`+jx3_recruit_v2`|`+jx3_recruit <服务器> <关键词>`|`+招募`|`获取团队招募。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_recruit_v2.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_recruit_v2_response.png)|
|`+jx3_recruit_local`|`+jx3_recruit_local <服务器> <关键词>`|`+本服招募`|`获取本服的招募，过滤跨服招募。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_recruit_local.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_recruit_local_response.png)|

> **附加功能：**`招募过滤`。
>
> 对招募的内容进行检测，将疑似广告的招募进行隐藏处理。

### 抓马信息

|- 命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_horse`|`+jx3_horse <服务器>`|`+抓马`、`+马场`|`获取服务器马场信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_horse.png)|
|`+jx3_dilu`|`+jx3_dilu`|`+的卢统计`|`获取全服的卢刷新、捕获及拍卖信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_dilu.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_dilu_response.png)|

### 副本掉落

|- 命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_itemdrop`|`+jx3_itemdrop <服务器> <物品>`|`+掉落`|`获取副本掉落特殊物品。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_itemdrop.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_itemdrop_response.png)|

## 榜单类

|- 命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_top100`|`+jx3_top100 <服务器> <BOSS> [团队]`|`+百强`|`获取魔盒秘境百强团信息。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_top100.png)|
|`+jx3_rank`|`+jx3_rank <个人\|帮会\|战功\|试炼> <服务器> <类型\|门派>`|`+榜单`|`获取榜单。`|`-`|`暂无`|

!> 由于参数过于多样化，此处不提供图片示例！

> <br>当第一参数为`个人`时，第二参数为`服务器`，第三参数为类型，接受的值：
> <br>`[名士五十强 老江湖五十强 兵甲藏家五十强 名师五十强 阵营英雄五十强 薪火相传五十强 庐园广记一百强]`。<br>
> <br>当第一参数为`帮会`时，第二参数为`服务器`，第三参数为类型，接受的值：
> <br>`[浩气神兵宝甲五十强 恶人神兵宝甲五十强 浩气爱心帮会五十强 恶人爱心帮会五十强]`。<br>
> <br>当第一参数为`阵营`时，第二参数为`服务器`，第三参数为类型，接受的值：
> <br>`[赛季恶人五十强 赛季浩气五十强 上周恶人五十强 上周浩气五十强 本周恶人五十强 本周浩气五十强]`。<br>
> <br>当第一参数为`试炼`时，第二参数为`服务器`，第三参数为门派，接受的值：
> <br>`[万花 七秀 少林 纯阳 天策 五毒 唐门 明教 苍云 长歌 藏剑 丐帮 霸刀 蓬莱 凌雪 衍天 药宗 刀宗]`。<br>

## 杂类

### 楚天云从

|- 命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_zhue`|`+jx3_zhue`|`+诛恶`|`获取服务器近期诛恶记录。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_zhue.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_zhue_response.png)|
|`+jx3_chutian`|`+jx3_chutian`|`+楚天社`|`获取当前楚天社阶段`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_chutian.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_chutian_response.png)|
|`+jx3_yuncong`|`+jx3_yuncong`|`+云从社`|`获取当前云从社阶段`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_yuncong.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_yuncong_response.png)|

### 挂件详情

|- 命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_pendents`|`+jx3_pendents <挂件名称>`|`+挂件`|`获取游戏内挂件详情。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_guajian.png)|

### 随机表情包

|- 命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_emoji`|`+jx3_emoji`|`+随机表情`|`从魔盒取一张随机表情包。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_emoji.png)|

### 奇遇前置/攻略

|- 命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_preposition`|`+jx3_preposition <奇遇>`|`+前置`、`+攻略`|`获取奇遇攻略。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_preposition.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_preposition_response.png)|

### BOSS掉落物详情

|- 命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_drops`|`+jx3_drops <副本> <难度> <BOSS>`|`+掉落列表`|`获取副本掉落列表。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_droplist.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_droplist_response.png)|

> 副本和难度支持模糊搜索，例如`牢`（武狱黑牢）、`25pt`（25人普通）、`dmd`（达摩洞）。

### 推栏推荐配装

|- 命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_eqrec`|`+jx3_receq <心法> [标签]`|`+配装v2`|`获取推栏推荐配装。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_equiprec.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_equiprec_response.png)|

### 本周百战地图

|- 命令|格式|别名|描述|权限|图片|
|-----|-----|-----|-----|-----|-----|
|`+jx3_monster_v2`|`-jx3_monster`|`+百战`|`获取百战BOSS列表。`|`-`|[示例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_monsters.png)/[图例](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/img/examples/jx3_monsters_response.png)|

!> 对于`-`开头的- 命令，即使绑定了服务器也不可以省略服务器，但可以正常映射。<br>
