# 总览

欢迎来到`Inkar Suki`使用文档！

本文档的目的是帮助用户清晰了解音卡（即`Inkar Suki`）的功能，请了解以下内容：
- 尖括号`<>`包裹的代表为必选参数，但如果是包裹的`服务器`，那么在绑定群聊服务器之后可以不写服务器；
- 方括号`[]`包裹的代表为可选参数，可以不填写；
- 在使用时请不要将方括号和尖括号代入！
- 阅读本文默认您同意[Inkar Suki 用户协议](https://inkar-suki.codethink.cn/Inkar-Suki-Docs/#/license)。

# 授权

- *Internel Code: activation*

**该功能的本意是防止音卡出现无效服务（例如根本不需要音卡的群但邀请了音卡），真正需要音卡的群而言，30天授权一次并不算频繁。**

**本功能不产生任何费用，更不是商业化！**

- 命令：`授权 天数`

> 该命令使用后，音卡到期时间是发送命令的时间再加上所给出的天数。<br>
> 如果用户在第一天授权了30天，在第二天又授权了7天，则实际到期是第二天的7天后而非第一天的30天后，请注意避免短时授权覆盖！

- 命令：`查看授权`

**该命令需要@音卡后才会响应！**

!> 授权系统运作后，假设授权是19:01到期，但由于授权系统仅会在`19:00`扫描一次，所以实际到期是第二天的`19:00`，在此之前授权均不会影响正常使用。<br>
但如果到期为`18:59`，那么在`19:00`扫描时会直接执行退群（因为扫描时间已经晚于过期时间），请留意到期时间！

# 偏好

- *Internel Code: preferences*

**音卡尊重用户的使用习惯，欢迎用户自定义音卡的部分设置，追求个性化的使用！**

- 命令：`偏好`

> 该命令会直接显示目前所有可用的偏好项，以及当前选择（包含默认值）和可选项等。

- 命令：`偏好 偏好项`

> 偏好项可从上一个命令的回复图片中获得。或者在本文档中，支持自定义偏好的内容也会标明`偏好项`的名称。<br>
> 该命令用于查询某一个偏好项的当前设定值。

- 命令：`偏好 偏好项 设定值`

> 该命令用户设置某个偏好项的值，例如将`属性`默认设置为`v2r`，请发送：`偏好 属性 v2r`。

!> 上述命令（包含子命令）的作用域为全域，即用户在A群设定的内容会同步至B群。

# 剑网3

- *Internel Code: jx3*

**音卡是完全脱机的项目，如果出现搜索玩家名但是显示未找到，需要提交`UID`的，您可以按照以下方法操作：**

- 在世界频道发言。
- 按住`Ctrl`，将鼠标移动至您的`ID`上。
- 此时会显示您的`玩家ID`，这就是`UID`，随后在音卡的任意一个实例处发送：`提交角色 服务器 您的UID`，即可将您的角色提交到音卡的数据库中。
- 如果从其他地方获得自己的`UID`也可以提交！

如果觉得不错的话，点击[这里](/donate)支持下音卡宝宝，~~求求了QAQ~~

## 服务器和新闻

### 绑定群聊

- 命令：`绑定 [服务器]`或`绑定区服 [服务器]`

!> 如果只发送`绑定`二字（也就是服务器为空），则是清除本群的绑定。<br>`绑定`和`绑定角色`并非同一个命令，请确认无误后再发送！

### 获取开服

- 命令：`开服 <服务器>`

### 获取日常

- 命令：`日常`

### 剑三黄历

- 命令：`剑三黄历 [ID(可留空)]`

### 功能开关

#### 订阅开关

- 命令：`订阅 <订阅内容>`或者`开启 <订阅内容>`

- 命令：`退订 <订阅内容>`或者`关闭 <订阅内容>`

> 什么是`订阅内容`？简而言之，参考下面的命令（`关于`）。<br>
> 回复的图片中有很多小方框，订阅内容就是他们的标题，一次可以订阅多个内容，以空格分割即可，例如`订阅 日常 开服 更新`，退订同理。

#### 查看订阅

- 命令：`关于`

### 维护公告

- 命令：`维护公告`或者`更新公告`或者`公告`或者`更新`

> 如果需要查看`测试服`的更新公告，请发送`体服公告`。

## 用户数据

### 绑定角色

- 命令：`绑定角色 <服务器> <ID>`

- 命令：`绑定角色 <服务器> <ID串>`

针对单个角色的绑定角色与其他常规命令格式一致，但ID串较为特殊，本意是方便用户一次绑定多个。

`ID串`支持多种格式：

**从游戏内直接复制**：[玩家1][玩家2][玩家3][玩家4]

**标点符号分割**：玩家1，玩家2，玩家3，玩家4
<br>支持中文逗号、中文顿号、英文逗号、中文句号，不支持空格分割！

> 每一个玩家名都支持尾随服务器后缀，例如`[玩家1·唯我独尊][玩家2·梦江南]`。<br>
> 若ID串中有ID未尾随服务器后缀：<br>
> 如果命令中有服务器参数，则按用户给出的服务器进行角色检索。<br>
> 如果命令中没有服务器参数，则按群聊绑定的服务器进行角色检索。<br>
> 若既未给出服务器，服务器也未绑定服务器，则命令报错。

- 命令：`解绑角色 <服务器> <ID/ID串>`

格式与`绑定角色`基本一致。

- 命令：`角色列表`

### 奇遇记录

> 偏好项名称：`奇遇`，默认为`v2`，可选值：`v2`、`v3`。

- 命令：`奇遇v2 <服务器> <ID>`或者`查询v2 <服务器> <ID>`

> 该命令会过滤宠物奇遇！

- 命令：`奇遇v3 <服务器> <ID>`或者`查询 <服务器> <ID>`

> 该命令会给出奇遇面板，展示所有触发和未触发的奇遇！

- 命令：`宠物奇遇 <服务器> <ID>`

> 该命令会过滤非宠物奇遇！

### 装备属性

> 该功能支持偏好设置，可使用`偏好 属性 版本号`自定义默认的属性命令。<br>
> 偏好项名称：`属性`，默认为`v4`，可选值：`v2`、`v2r`、`v4`。

- 命令：`属性v4 <服务器> <ID>`或者`查装v4 <服务器> <ID>`

- 命令：`属性v2r <服务器> <ID>`或者`查装v2r <服务器> <ID>`

- 命令：`属性v2 <服务器> <ID>`或者`查装v4 <服务器> <ID>`

> 属性目前会将用户的装备数据进行缓存，会产生一个标签（例如`DPSPVE`、`TPVE`、`HPSPVP`等）。<br>
> 标签中的`DPS/HPS/T`是由当前识别的心法所决定，而`PVE/PVX/PVP`是由当前识别的装备所决定。<br>
> 不存在`TPVX`和`TPVP`。且唐门和纯阳双DPS心法并不使用`DPS`作为标签，而是`TL/JY/QC/JC`。<br>
> 仅`属性v4`支持显示缓存装备和查询缓存装备，但所有版本的属性命令均会对装备进行缓存！
> `属性v2r`与`属性v4`会显示镶嵌孔内容，仅`属性v4`会显示装备特效词条。

#### DPS计算器

**目前仅支持`凌雪阁`的DPS计算。**

- 命令：`凌雪计算器 <服务器> <ID> [-A]`

*作者：猜猜我是谁@梦江南*

#### RDPS计算器

**本质是复盘战斗信息。**

*作者：花姐*

使用方法：

- 从茗伊插件集（团队-团队工具-小齿轮）勾选`战斗事件记录`，勾选`在秘境地图中启用`。
- 在BOSS离开战斗后，点击`打开数据目录`，复制路径，在本地资源管理器中打开。
- 将`JCL`文件拖到其他目录，在文件名前方加入`IKS-`（标记这个文件需要音卡分析）。
- 将重命名后的文件上传至群文件，并等待`1-3`分钟，音卡将会发送`RDPS`和`RHPS`统计图。

> `RDPS`（`Raid Damage Per Second`）通俗来讲可以用公式形容（`面板DPS` - `享受的增益` + `提供的增益`）。<br>
> `RHPS`（`Raid Health Per Second`）请移步[重新定义HPS——一种更适应剑三治疗环境的评价体系 by 花姐](https://www.jx3box.com/bps/43357)。

!> 您所上传的JCL文件将会同步至花姐的服务器，如有异议请勿使用本功能！

> 剑三警长是一款剑网三战斗日志分析工具，在使用本工具之前，我们需要部分授权，需要您的同意：<br>
> 1. 本工具会读取茗伊插件集生成的战斗复盘日志，其中的信息包括但不限于：全部技能与buff的时间与数值、玩家ID与门派、区服、重伤记录。这些读取的内容只会在本地进行运算。<br>
> 2.本工具会上传战斗复盘结果图中的所有信息到作者的服务器，包括但不限于：DPS/HPS统计，区服，玩家ID与门派，打分，犯错记录。收集这些信息是为了进行进一步研究，对之后的的开发提供数据支持。由于上传的数据只有全局信息，因此您无需担心打法被泄漏。<br>
> 3.对于上传的数据，可能会以HPS天梯/评分百分比的形式，进行数据公开。作者在公开数据时，有对玩家个人信息进行保密的义务，包括玩家ID与团队构建等信息，应在去特征化后再发布。但演员不在此列，对于表现明显低于正常水平的玩家，可能会有其它安排。<br>
> 4. 即使没有显式同意本协议，使用本工具依然需要协议的内容经过授权。尝试绕过本协议并不能免除您的义务。<br>
> 5. 本协议仅对jx3bla主仓库的主分支有效，开发者如果需要修改代码，需要同时维护此协议，否则视为本协议无效。<br>
> 6. 本工具使用花姐的“剑三警长”进行分析，上述协议从程序内复制而来，使用本功能也需要遵守上述协议！

### 成就进度

- 命令：`进度 <服务器> <ID> <关键词>`

- 命令：`团本成就 <服务器> <ID> <副本名称> [难度]`

> `副本名称`不需要携带难度，而`难度`在未给出的情况下，默认为`10人普通`。

- 命令：`资历分布 <服务器> <ID>`

> 使用命令后会给出子类，回复前方序号即可！

### 副本通关

- 命令：`副本 <服务器> <ID>`

- 命令：`副本 <服务器> <ID串>`

> `ID串`即一串ID（多个ID），使用英文分号`;`分隔，例如：`副本 幽月轮 玩家1;玩家2;玩家3`。

- 命令：`副本 *`

- 命令：`副本列表 [关键词]`

> 该命令的前提是需要绑定角色，未绑定任何角色的情况下无法使用`副本 *`直接查询所有副本的通关记录。<br>
> 不带参数的`副本列表`与`副本 *`等效。<br>
> `副本列表`的的关键词假设为`太极宫`，那么会同时匹配`10人普通太极宫`（`10人普通`会被省略）、`25人普通太极宫`、`25人英雄太极宫`。

### 名剑大会

- 命令：`战绩 <服务器> <ID>`

### 账号查询

- 命令：`查人 <QQ号>`

### 情缘系统

#### 绑定情缘

- 命令：`绑定情缘 <自己游戏ID> <对方游戏ID> <对方QQ> [自定义起始时间]`

> 双方的ID都要位于发这条命令的群聊所绑定的服务器中。自定义起始时间接受的格式为：`YYYY-mm-dd`或者`YYYY年mm月dd日`。

#### 解绑情缘

- 命令：`解除情缘`

#### 情缘证书

- 命令：`查看情缘证书`

## 信息查询

### 科举答案

- 命令：`科举 <关键词>`

### 阵眼效果

- 命令：`阵眼 <心法>`

### 奇穴信息

- 命令：`奇穴 <心法> [名称]`

> 奇穴名称支持模糊搜索，或者直接留空。<br>
> 留空时给出该心法的所有奇穴（按顺序）。

### 技能信息

- 命令：`技能 <心法> <名称>`

> 技能名称支持模糊搜索，不可留空。

### 心法宏库

- 命令：`宏 <心法>`

### 小药列表

- 命令：`小药`

## 娱乐类

### 随机骚话

- 命令：`骚话`

### 舔狗日记

- 命令：`舔狗`

### 模拟黑本

- 命令：`黑本 <副本名> <难度>`

### 模拟翻牌

- 命令：`翻牌 <层数> <序号>`

> `层数`和`序号`都只支持纯数字，层数依据赛季进度决定最大值为`70`或`120`层，`序号`仅支持`1-5`。<br>
> `黑本`功能严格遵循副本掉落规则，如有不同可以反馈/发起`issue`。

## 交易类

### 查看金价

- 命令：`金价 <服务器>`

### 外观物价

- 命令：`物价 <关键词>`

### 交易行

> 该功能支持偏好设置，可使用`偏好 交易行 版本号`自定义默认的属性命令。<br>
> 偏好项名称：`交易行`，默认为`v2`，可选值：`v2`、`v3`。<br>
> 该偏好同时适用于`交易行`和`交易行试炼`。

#### 常规物品

**该命令不支持试炼之地装备！**

- 命令：`交易行v2 <服务器> <关键词>`

- 命令：`交易行v3 <服务器> <关键词>`

> `服务器`还可以是`全服`，此时给出全服价格。<br>
> 如果使用精准物品检索，可以使用`[]`（方括号）将物品名称包裹（或从游戏内复制，同样效果）。

#### 试炼装备

- 命令：`交易行试炼 <服务器> <词条>`

- 示例：`交易行试炼 全服 30200内功双会无暗器`
- 示例：`交易行试炼 幽月轮 30200内功双会招项链`

> `服务器`还可以是`全服`，此时给出全服价格。<br>
> `词条`需要包含`品级`、`内外功`、`属性`、`部位`四个内容。<br>
> 例如`25500外功双会头`（`25500`品级，`外功`内外功，`双会`属性，`头`部位）。<br>
> 另请仔细区分`破招`和`破防`的区别，`破招`仅可在与`破防`共存时简写为`破破`（破防破招），其余情况应写为`招`而非`破`。

### 盆栽蹲号/蹲外观

- 命令：`蹲号 <条件>`

> 如果有多个条件，请以`空格`分割，例如：`蹲号 军萝 蝶金`。

- 命令：`贴吧物价 <名称>`

### 成本计算

- 命令：`成本 <名称>`

> 物品名称支持不完整名称，会给出选项，回复序号即可搜索。

## 服务器内

### 抓马信息

- 命令：`马场 <服务器>`或者`抓马 <服务器>`

### 副本掉落

- 命令：`掉落 <物品名称>`

## 榜单类

### 资历榜单

- 命令：`资历排行 [服务器] [门派]`

> `服务器`为空时为全服，`门派`为空时为`全门派`，两者均可为空。

### 天梯

- 命令：`RD天梯/RH天梯 <副本名> <副本难度> <首领名> <心法名>`

*榜单数据来源为剑三警长（无论通过警长本体亦或是音卡群文件分析均可参与天梯排名）。*

> 目前，全难度太极宫的六号首领`薛琢玉`需要写为`杨玉环`方可查询。

## 杂类

### 楚天云从

- 命令：`诛恶 <服务器>`

- 命令：`楚天社`

- 命令：`云从社`

### 随机表情

- 命令：`随机表情`

> 音卡的表情随机来自魔盒，如果因此破防而移出音卡，可能会受到封禁。

### 奇遇攻略

- 命令：`攻略 <奇遇名>`

### 掉落列表

- 命令：`掉落列表 <副本> <难度> <BOSS名>`

> 副本和难度支持模糊搜索，例如`牢`（武狱黑牢）、`25pt`（25人普通）、`dmd`（达摩洞）。

### 推荐配装

- 命令：`配装 <心法> <PVE/PVP>`

> `心法`和`标签`可以反过来写。

### 百战地图

- 命令：`百战`

!> 数据来源为魔盒，可能更新不及时！

## 开团辅助

### 创建团队

- 命令：`创建团队 <关键词/序号> [限制]`

> `限制`是一个词条，用于限制此次团队的各种职业数量，示例：`1T2N3D4B`，表示本次团队需要`1`位防御心法，`2`位治疗心法，`3`位输出心法和`4`位躺拍老板，如果开团之后需要修改，请参考下面的`修改团队限制`。

### 解散团队

- 命令：`解散团队 <关键词/序号>`

### 修改限制

- 命令：`修改团队限制 <关键词/序号> <限制>`

> 如果要取消掉限制，对应参数请填写`无`。

### 预定

- 命令：`报名 <关键词/序号> <ID> <职业>`

> 命令别名为：`预定`、`预订`。

> `Inkar Suki`支持预留团队成员位置（仅创建人），在`ID`前方加一个`#`表示此次报名只预留了一个对应职业的位置，并不指定具体玩家，如果团长设置的职业限制已达上限且具有这种预留位，那么该职业的玩家仍然可以进行报名，会对该位置进行替换！

### 取消预定

- 命令：`取消报名 <关键词/序号> <ID>`

> 命令别名为：`取消预定`、`取消报名`。

### 查看团队

- 命令：`查看团队 <关键词/序号>`

### 团队列表

- 命令：`团队列表`。

> 该命令会列出群内所有进行中的团队、团队序号以及团队职业限制。

### 共享团队

- 命令：`共享团队 <群号> <关键词/序号>`

> 该功能适用于优先小群报名随后共享给伐木群的情况。需要注意，共享为一次性共享，如果任意一方的团队有更新，另一方并不会同步更新，且只有同一个创建人的团队可以共享，序号和关键词为原群的序号或关键词，而不是目标群的。

## 黑名单

### 加入黑名单

- 命令：`避雷 <名称> <原因>`

!> 原因中不支持包含空格！

### 移出黑名单

- 命令：`撤销避雷 <名称>`或`取消避雷 <名称>`

### 本群黑名单

- 命令：`黑名单`或`避雷名单`

# 娱乐

- *Internel Code: twenty_four, stastic, notice, bulletin*

## 小游戏

- 命令：`对诗`

- 命令：`24点`

## 发言统计

- 命令：`本群发言统计 [日期/all]`

## 欢迎语

- 命令：`修改欢迎语 内容`

> 内容暂时只支持文字！

## 喜报悲报

- 命令：`喜报/悲报 文字`

> 文字支持至高20字！

# Minecraft

- *Internel Code: minecraft*

## 版本获取

- 命令：`mcjv`

> 获取`Java版`最新版本号。

- 命令：`mcbv`

> 获取`基岩版`最新版本号。

## 服务器

- 命令：`jes <IP>`

- 获取`Java版`服务器信息。

- 命令：`bes <IP>`

- 获取`基岩版`服务器信息。

# 雀魂麻将

- *Internel Code: Majsoul*

**暂时只支持四麻查询！**

> 数据来源于雀魂牌谱屋，但是牌谱屋只收录雀杰及以上段位的玩家，所以低段位玩家可能无法搜索出来。

## 玩家检索

- 命令：`mssp <玩家名>`

## PT查询

- 命令：`mspt <玩家名>`

## 最近对局

- 命令：`msgr <玩家名>`

## 对战月报

- 命令：`msmr <玩家名> [区间]`

> `区间`默认为上一个月，如需指定请按`YYYY-mm`格式给出！