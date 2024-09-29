# 开发指南

本章中，路径是`Python`导入使用的，如果`直接导入`可用，那么最小分类的下的函数、类、变量均可以直接导入，不需要继续细化路径。

**不要使用`from your_code import *`进行泛导入！请导入确切的函数、类或变量！**

本章中的类属性可能无序，如需传参，推荐使用关键字参数。

## Account

|路径|直接导入|贡献者|作用|
|-----|-----|-----|-----|
|`src.accounts`|`否`|HornCopper|`-`|
|`src.accounts.manage`|`是`|HornCopper|账户管理，包含权限、数值等。|

### _class_ `CheckinRewards`

- **导入** `src.accounts.manage`

- **说明:** 签到奖励。**一般不会主动创建该类实例，而是由`AccountManage`类方法函数返回实例**。继承自`pydantic.BaseModel`。

- **属性**
    - `coin` (bool) 签到获得的金币
    - `is_lucky` (bool) 是否触发额外奖励
    - `lucky_value` (int) 今日幸运值
    - `total_days` (int) 累计签到次数

### _class_ `AccountManage`

- **导入** `src.accounts.manage`

- **说明:** 账户管理类。

- **参数**
    - `user_id` (int | str) 用户账号

- **方法**
    - _property_ `checkin_counts` (int)
        - **说明:** 累计签到次数。
    
    - _property_ `coins` (int)
        - **说明:** 用户的金币数量。

    - _property_ `permission` (int)
        - **说明:** 用户的权限等级（内部权限，`1-10`）。

    - _property_ `checkin_status` (bool)
        - **说明:** 判断用户在本周期内是否能签到。

    - _method_ `checkin`
        - **说明:** 用户签到。

        - **返回**
            - `checkin_status` (CheckinRewards | False) 当返回值为`False`时，代表该用户今日已经签到过了，无法重复签到；否则返回`CheckinRewards`类实例。

    - _method_ `add_coin`
        - **说明:** 向用户账户内追加金币。
        
        - **参数**
            - `counts` (int) 要追加的金币数量。
            
    - _method_ `reduce_coin`
        - **说明:** 向用户账户内扣除金币。

        - **参数**
            - `counts` (int) 要扣除的金币数量。

    - _method_ `add_checkin_counts`
        - **说明:** 增加用户的签到天数。**建议不要自行调用该方法，该方法由`self.checkin`方法进行调用。**

        - **参数**
            - `counts` (int) 要增加的天数。

    - _method_ `_update_last_checkin`
        - **说明:** **私有方法，不要显式调用。**刷新用户的签到时间，用于下次签到判断是否在对应周期内（`self.checkin_status`）。

## Assets

|路径|直接导入|贡献者|作用|
|-----|-----|-----|-----|
|`src.assets`|`否`|`-`|`-`|

资源文件，无任何逻辑代码。

!> 向该文件夹添加内容时，请确保内容的合规性！

## Cache

|路径|直接导入|贡献者|作用|
|-----|-----|-----|-----|
|`src.cache`|`否`|`-`|`-`|

缓存文件，无任何逻辑代码。

## Config

|路径|直接导入|贡献者|作用|
|-----|-----|-----|-----|
|`src.config`|`是`|HornCopper|将配置文件导出为类。|

### _variable_ Config

- **导入** `src.config`

- **类型** config

与`config.yml`结构一致，不再赘述。

如有疑问可查看`src/config/__init__.py`。

## Const

|路径|直接导入|贡献者|作用|
|-----|-----|-----|-----|
|`src.const`|`否`|`-`|`-`|
|`src.const.path`|`是`|HornCopper|`src`目录下的子目录路径常量、构建路径函数。|
|`src.const.prompts`|`是`|HornCopper|插件部分常用回复语。|
|`src.const.jx3`|`否`|`-`|`-`|
|`src.const.jx3.constant`|`是`|HornCopper|同目录下其他代码从这里读取已加载的常量，也可以直接从此导出常量使用。|
|`src.const.jx3.server`|`是`|HornCopper|剑网3服务器常量，包含`Server`类。|
|`src.const.jx3.school`|`是`|HornCopper|剑网3门派常量，包含`School`类。|
|`src.const.jx3.dungeon`|`是`|HornCopper|剑网3副本常量，包含`Dungeon`类。|
|`src.const.jx3.kungfu`|`是`|HornCopper|剑网3心法常量，包含`Kungfu`类。|

### _variable_ BOT_PATH

- **导入** `src.const.path`

一共有`7`个变量，均位于`src/const/path.py`，变量名为本页面所有二级标题的全大写（如`ASSETS`）。

在路径构建函数`build_path`中，第一个参数需要这些常量其一。

### _function_ build_path

- **导入** `src.const.path`

- **参数**
    - `const` (str) 上方的`BOT_PATH`中任选其一填入（`BOT_PATH`并非类）。
    - `path` (List[str]) 剩余路径，例如`a/b/c.txt`，传参`["a", "b", "c.txt"]`。
    - `end_with_slash` (bool) 是否在路径末尾追加一个斜杠。

- **返回**
    - `path` (str) 最终路径。

> 本函数主要是为了兼容多平台的路径，内部使用`os.sep`而非直接使用斜杠`/`。

### _class_ PROMPT

- **导入** `src.const.prompts`

- **说明:** `Inkar Suki`回复语。

> 由于语句非常多，请直接查看`src/const/prompts.py`。

### _variable_ dungeon_name_data

- **导入** `src.const.jx3.constant`

- **说明:** 副本名称数据，`Key`为副本实际名称，`Value`为字符串列表，元素为副本别名（包含本名）。

- **类型** Dict[str, List[str]]

### _variable_ dungeon_mode_data

- **导入** `src.const.jx3.constant`

- **说明:** 副本模式数据，`Key`为实际难度名称，`Value`为字符串列表，元素为难度别名（包含本名）。

- **类型** Dict[str, List[str]]

### _variable_ kungfu_aliases_data

- **导入** `src.const.jx3.constant`

- **说明:** 心法名称数据，`Key`为心法实际名称，`Value`为字符串列表，元素为心法别名（包含本名）。

- **类型** Dict[str, List[str]]

### _variable_ kungfu_colors_data

- **导入** `src.const.jx3.constant`

- **说明:** 心法颜色数据，`Key`为心法实际名称，`Value`为心法对应颜色（十六进制）。

- **类型** Dict[str, str]

### _variable_ kungfu_internel_id_data

- **导入** `src.const.jx3.constant`

- **说明:** 心法ID数据，`Key`为心法实际名称，`Value`为心法对应ID。

- **类型** Dict[str, str]

### _variable_ kungfu_baseattr_data

- **导入** `src.const.jx3.constant`

- **说明:** 心法基础属性数据，`Key`为基础属性名称，`Value`为字符串列表，元素为心法名称。

- **类型** Dict[str, List[str]]

### _variable_ school_aliases_data

- **导入** `src.const.jx3.constant`

- **说明:** 门派名称数据，`Key`为门派名称，`Value`为字符串列表，元素为门派别名（包含本名）。

- **类型** Dict[str, List[str]]

### _variable_ school_internel_id_data

- **导入** `src.const.jx3.constant`

- **说明:** 门派ID数据，`Key`为门派ID，`Value`为门派名称。

- **类型** Dict[str, str]

### _variable_ server_aliases_data

- **导入** `src.const.jx3.constant`

- **说明:** 服务器名称数据，`Key`为服务器名称，`Value`为字符串列表，元素为服务器别名（包含本名）。

- **类型** Dict[str, List[str]]

### _variable_ server_zones_mapping_data

- **导入** `src.const.jx3.constant`

- **说明:** 服务器大区数据，`Key`为大区名称，`Value`为字符串列表，元素为大区包含的服务器。**大区名为合并前大区名。**

- **类型** Dict[str, List[str]]

### _class_ Dungeon

- **导入** `src.const.jx3.dungeon`

- **说明:** 副本类。

- **参数**
    - `name` (str) 副本名称
    - `mode` (str) 副本难度

- **方法**
    - _property_ `name` (str | None)
        - **说明:** 副本实际名称。

    - _property_ `mode` (str | None)
        - **说明:** 副本实际难度。

### _class_ Kungfu

- **导入** `src.const.jx3.kungfu`

- **说明:** 心法类。

- **参数**
    - `kungfu_name` (str | None) 心法名称

- **方法**
    - _classmethod_ `with_internel_id`
        - **说明:** 使用心法ID创建`Kungfu`实例。

        - **参数**
            - `internel_id` (str | int) 心法ID
            
        - **返回**
            - `cls` (Kungfu) `Kungfu`类实例。
    
    - _property_ `name` (str | None)
        - **说明:** 心法实际名称。

    - _property_ `school` (str | None)
        - **说明:** 心法所属门派。

    - _property_ `color` (str)
        - **说明:** 心法颜色。
    
    - _property_ `icon` (str)
        - **说明:** 心法图标。

    - _property_ `base` (str | None)
        - **说明:** 心法基础属性。

    - _property_ `id` (int | None)
        - **说明:** 心法ID。

### _class_ School

- **导入** `src.const.jx3.school`

- **说明:** 门派类。

- **参数**
    - `school_name` (str | None) 

- **方法**
    - _classmethod_ `with_internel_id`
        - **说明:** 使用门派ID创建`School`实例。

        - **参数**
            - `internel_id` (int | str) 门派ID
        
        - **返回**
            - `cls` (Kungfu) `Kungfu`类实例
            
    - _property_ `name`
        - **说明:** 门派实际名称。
        
    - _property_ `internel_id`
        - **说明:** 门派ID。

    - _property_ `color`
        - **说明:** 门派颜色。

    - _property_ `icon`
        - **说明:** 门派图标。

### _class_ Server

- **导入** `src.const.jx3.server`

- **说明:** 区服类。

- **参数**
    - `server_name` (str | None) 服务器名称。
    - `group_id` (int | None) 群聊ID。

    !> 初始化`Server`实例时，至少传入`server_name`和`group_id`其一，可同时传入。

- **方法**
    - _property_ `server_raw`
        - **说明:** 服务器原始名称，不会受到`group_id`的影响。

    - _property_ `server`
        - **说明:** 最终服务器名称，命令服务器 > 群聊绑定服务器。

    - _property_ `zone_legacy`
        - **说明:** 区服的合并前大区名。

    - _property_ `zone`
        - **说明:** 区服的合并后大区名。

        > 如果为`无界区`，那么`zone_legacy`与`zone`一致。

## Data

|路径|直接导入|贡献者|作用|
|-----|-----|-----|-----|
|`src.data`|`否`|Snowykami|`Inkar Suki`本地数据库。|

## Plugins

|路径|直接导入|贡献者|作用|
|-----|-----|-----|-----|
|`src.config`|`否`|参考`GitHub`|`Inkar Suki`插件目录。|

> 一般不推荐在插件目录中发生插件导入插件，如有必要，可以考虑将其转移至`src/utils`或在`src`目录下新建一个子目录。

## Templates

|路径|直接导入|贡献者|作用|
|-----|-----|-----|-----|
|`src.templates`|`是`|HornCopper|`Inkar Suki`模板目录。|

### _class_ HTMLSourceCode

- **导入** `src.templates`

- **说明:** 使用统一模板（`src/templates/universe.html`）生成表格。

- **参数**
    - `application_name` (str) 页脚的应用名称。
    - `font_path` (str) 自定义字体。
    - `footer` (str) 页脚最后一行。
    - `additional_css` (str) 额外的`CSS`，支持`File URL`或代码。
    - `additional_js` (Path | None) 额外的`JavaScript`，支持`Path`对象。
    - `**kwargs` (dict) 额外键值对，将直接进行替换。

    > 除`application`外均不是必选参数，`font_path`和`footer`建议留空。`**kwagrs`建议传入`table_head`和`table_body`。

- **方法**
    - _method_ `__str__`
        - **说明:** 可直接使用`str()`，获得`HTML`填充完毕后的源代码。

        - **返回**
            - `source_code` (str) `HTML`源代码。

### _class_ SimpleHTML

- **导入** `src.templates`

- **说明:** 使用自定义模板生成内容。

- **参数**
    - `html_type` (str) `HTML`类型，对应`src/templates`下的文件夹名。
    - `html_template` (str) `HTML`文件名（可省略后缀名），对应`src/templates/(html_type)/`下的文件名。
    - `outside_js` (str) 外部`JavaScript`，接受文件路径或`URL`（含`File URL`）。
    - `outside_css` (str) 外部`CSS`，接受文件路径或`URL`（含`File URL`）。
    - `**kwargs` (dict) 额外键值对，将直接进行替换。

    > `html_type`和`html_template`为必选参数，其他均为可选。

- **方法**
    - _method_ `__str__`
        - **说明:** 可直接使用`str()`，获得`HTML`填充完毕后的源代码。

        - **返回**
            - `source_code` (str) `HTML`源代码。

## Utils

|路径|直接导入|贡献者|作用|
|-----|-----|-----|-----|
|`src.utils`|`否`|`-`|`-`|
|`src.utils.database`|`是`|Snowykami, HornCopper|数据库实例。|
|`src.utils.database.lib`|`是`|Snowykami|数据库核心代码。|
|`src.utils.database.classes`|`是`|HornCopper|数据存储类。|
|`src.utils.database.operation`|`是`|HornCopper|数据基本操作。|
|`src.utils.database.player`|`是`|HornCopper|玩家数据库。|
|`src.utils.analyze`|`是`|HornCopper|数据分析。|
|`src.utils.decorators`|`是`|HornCopper|装饰器。|
|`src.utils.file`|`是`|HornCopper|文件操作。|
|`src.utils.generate`|`是`|HornCopper|Playwright渲染。|
|`src.utils.network`|`是`|HornCopper|网络请求。|
|`src.utils.permission`|`是`|HornCopper|权限控制。|
|`src.utils.time`|`是`|HornCopper|时间计算。|
|`src.utils.typing`|`是`|HornCopper|类型注解。|

`Inkar Suki`开发工具。

### _variable_ db

- **导入** `src.utils.database`

- **说明:** `Inkar Suki`显示操作数据库时需要使用该变量进行操作。

- **类型** Database

### _class_ LiteModel

- **导入** `src.utils.database.lib`

- **说明:** **不要直接使用`LiteModel`类创建实例！**可在`src/utils/database/classes.py`中定义一个新类，继承`LiteModel`类并创建类属性`TABLE_NAME`，其他类属性即为创建的字段。

!> 继承该父类的子类务必写好类型注解以及默认值，否则`Pydantic`会报错！并在`src/database/__init__.py`中的`db.auto_migrate()`函数中追加新类的实例。

### _class_ Database

- **导入** `src.utils.database.lib`

- **说明:** **不建议自行创建实例，使用`db`变量。**

- **方法**
    > 本类的方法较多且复杂，主要介绍读写。具体可查看`src/utils/database/lib.py`

    - _method_ `where_one`
        - **说明:** 查询第一个对象。

        - **参数**
            - `model` (LiteModel) 继承`LiteModel`的子类（在`src/utils/database/classes.py`中定义）

            !> 注意，类型注解为`LiteModel`而非`Type[LiteModel]`，也就是不可传入继承`LiteModel`的类，而是其对应实例！
            
            - `condition` (str) 判定条件，需要`SQL`语句，如果需要传参，请使用`?`进行替换，而后传入`*args`
            - `*args` (tuple) 根据`condition`的占位符数量传入额外的参数
            - `default` (Any) 当没有满足条件的对象时，返回的默认值

            > `default`参数不会涉及**写**数据库，如果不存在可以自行创建新实例并传参，最后进行保存。

        - **返回**
            - `Object` (model | type(default)) 满足条件的`LiteModel`子类实例或`default`参数值
    
    - _method_ `where_all`
        - **说明:** 查询所有满足条件的对象

        - **参数**
            与`where_one`方法参数完全一致。
        
        - **返回**
            - `Object` (List[model] | type(default)) 满足条件的`LiteModel`子类实例列表或`default`参数值

    - _method_ `save`
        - **说明:** 保存实例。
        
        - **参数**
            - `*args` (LiteModel) 同`where_one`的`model`含义
        
    - _method_ `delete`
        - **说明:** 删除实例。

        - **参数**
            与`where_one`方法一致，但不存在`default`参数，且多出下面的`allow_empty`参数。

            - `allow_empty` (bool) 是否允许空条件删除。

### _function_ get_group_settings

- **导入** `src.utils.database.operation`

- **说明:** 获取群聊配置的某一项的值。

- **参数**
    - `group_id` (str | int) 群号
    - `key` (str) 要获取的数据键

- **返回**
    - `content` (Any) 数据内容

### _function_ set_group_settings

- **导入** `src.utils.database.operation`

- **说明:** 对群聊某项配置进行赋值。

- **参数**
    - `group_id` (str | int) 群号
    - `key` (str) 要更改的数据键
    - `content` (Any) 更改内容。

### _function_ get_groups

- **导入** `src.utils.database.operation`

- **说明:** 获取所有群聊。

- **返回**
    - `result` (List[int]) 数字列表，元素为群号

### _function_ (async)send_subscribe

- **导入** `src.utils.database.operation`

- **说明:** 按订阅发送消息。

- **参数**
    - `subscribe` (str) 订阅内容
    - `msg` (str) 消息内容
    - `server` (str | None) 服务器

    > 如果服务器为`None`，那么该订阅发送的时候不会匹配群聊绑定的服务器，反之则会匹配，不匹配的群聊不会推送。

### _function_ (async)get_uid_data

- **导入** `src.utils.database.player`

- **说明:** 获取并记录`UID`对应的玩家数据。

- **参数**
    - `role_id` (str) 玩家UID
    - `server` (str) 服务器

- **返回**
    - `message` (str) 记录数据的消息。

### _class_ Player

- **导入** `src.utils.database.player`

- **说明:** 建议只用于类型注解。

> 本类不应用于创建新实例，故不给出参数，方法只给出`format_jx3api`。

- **方法**
    - _method_ format_jx3api
        - **说明:** 按`JX3API`的数据格式给出一个字典。

        - **返回**
            - `result` (dict) 玩家数据

            > 若没有找到，`code`为`404`。

### _function_ (async)search_player

- **导入** `src.utils.database.player`

- **说明:** 在本地数据库中查找玩家。

- **参数**
    - `role_name` (str) 玩家ID
    - `role_id` (str) 玩家UID
    - `server_name` (str) 服务器

- **返回**
    - `result` (Player) 玩家数据

> 当启用`JX3API`或自行定义`get_uid`函数后，可以直接将`ID`转为`UID`。

### _function_ invert_dict

- **导入** `src.utils.analyze`

- **说明:** 将键值均为字符串的字典进行键值互换。

- **参数**
    - `raw_dict` (Dict[str, str]) 需转换的字典

- **返回**
    - `result` (Dict[str, str]) 转换后的字典

### _function_ sort_dict_list

- **导入** `src.utils.analyze`

- **说明:** 按字典的共有键进行排序。键对应值需要是`int`或其他可比较的类型。

- **参数**
    - `raw_list` (List[dict]) 包含 含相同键的字典 的列表

- **返回**
    - `result` (List[dict]) 排序完成的列表

### _function_ merge_dict_lists

- **导入** `src.utils.analyze`

- **说明:** 将包含的字典的键均相同的两个列表进行合并。

- **参数**
    - `list_1` 第一个列表
    - `list_2` 第二个列表
    
- **返回**
    - `merged_list` 合并后的字典列表

> `list_2`的优先级高于`list_1`，同时包含数据的时候，`list_2`优先覆盖。

### _function_ check_number

- **导入** `src.utils.analyze`

- **说明:** 判断某个字符串是否为数字（`int`或`float`）。

- **参数**
    - `raw_string` (str) 需要判断的字符串
    
- **返回**
    - `is_num` (bool) 是否为数字

### _function_ extract_numbers

- **导入** `src.utils.analyze`

- **说明:** 从字符串中提取数字。

- **参数**
    - `raw_string` (str) 需要提取的字符串
    
- **返回**
    - numbers (List[int]) 字符串中包含的数字

### _function_ (decorator)ticket_required

- **导入** `src.utils.decorators`

- **说明:** **装饰器函数**，被装饰的函数需要具有`ticket`参数，自动传入`ticket`参数。

### _function_ (decorator)token_required

- **导入** `src.utils.decorators`

- **说明:** **装饰器函数**，被装饰的函数需要具有`token`参数，自动传入`token`参数。

### _function_ (decorator)time_record

- **导入** `src.utils.decorators`

- **说明:** **装饰器函数**，对函数进行计时。

### _function_ read

- **导入** `src.utils.file`

- **说明:** 读取文件内容。

- **参数**
    - `path` (str) 文件路径

- **结果**
    - `content` (str) 文件内容

### _function_ write

- **导入** `src.utils.file`

- **说明:** 向文件写入内容，

- **参数**
    - `path` (str) 文件路径
    - `content` (bytes | str) 写入内容
    - `mode` (Literal["w, "wb"]) 写入模式

    > 当`content`为`bytes`时，`mode`请传入`wb`，反之则传入`w`。

### _function_ (async)generate

- **导入** `src.utils.generate`

- **说明:** 渲染截图。

- **参数**
    - `source` (str) `URL`或`HTML`源代码
    - `locate` (str) 需要定位截图的`CSS`元素
    - `first` (bool) 是否只选择第一个匹配的元素
    - `delay` (int) 等待时间
    - `additional_css` (str) 附加的`CSS`代码
    - `additional_js` (str) 附加的`JavaScript`代码
    - `viewport` (dict) 视图大小
    - `full_screen` (bool) 是否全屏截图
    - `hide_classes` (List[str]) 需要隐藏的元素
    - `device_scale_factor` (float) 视窗比例
    - `output_path` (str) 输出路径

- **返回**
    - `path` (str) 文件路径

### _class_ Request

- **导入** `src.utils.network`

- **说明:** 网络请求类。

- **参数**
    - `url` (str) 目标地址
    - `headers` (dict) 请求头
    - `params` (dict | str) 请求体
    
- **方法**
    - _method_ (async)get
        - **参数**
            - `expire_at` (int) 过期时间戳，在此时间戳前的请求全部会使用相同回复，如需避免使用缓存，在请求时将该时间戳设置为比当前早的任意时间戳即可
            - `timeout` (int) 超时时间，默认为`20`（单位`seconds`）
            - `**kwargs` (dict) 其余参数原样传入`httpx.client.get()`

        - **返回**
            - `response` (httpx.Response) 响应类
        
    - _method_ (async)post
        - **参数**
            - `tuilan` (bool) 是否构建推栏请求，**如果为`True`，则会根据传入的`params`进行构建推栏请求**
            - `timeout` (int) 超时时间，默认为`20`（单位`seconds`）
            - `**kwargs` (dict) 其余参数原样传入`httpx.client.get()`

        - **返回**
            - `response` (httpx.Response) 响应类

    - _property_ local_content
        - **说明:** 如果传入`URL`是本地`URL`，可调用`local_content`属性查看二进制内容。
        
    - _method_ _build_tuilan_request
        - **说明:** 私有方法，构建推栏请求。
    
### _function_ check_permission

- **导入** `src.utils.permission`

- **说明:** 判断用户的权限等级。

- **参数**
    - `user_id` (int | str) 用户账号
    - `level` (int | str) 需要判断的权限等级

- **返回**
    - `is_match` (bool) 是否达到该权限等级

### _function_ denied

- **导入** `src.utils.permission`

- **说明:** 给出权限不足的提示语

- **参数**
    - `level` (int | str) 没有达到的权限等级

- **返回**
    - `message` (str) 构建的消息

### _class_ Time

- **导入** `src.utils.time`

- **说明:** 时间处理对象。

- **参数**
    - `time` (int) 要处理的时间戳

- **方法**
    - _property_ raw_time
        - **说明:** 原始时间戳。
    
    - _method_ format
        - **说明:** 格式化时间。

        - **参数**
            - `form` (str) 时间格式，默认为`%Y年%m月%d日 %H:%M:%S` 

        - **返回**
            - `formatted_time` (str) 格式化的时间字符串
    
    - _method_ relate
        - **说明:** 计算相对时间。

        - **参数**
            - `time` 需要比对的时间戳。**注意是方法`time`相对实例`time`的相对时间！**
            
        - **返回**
            - `relative_time` (str) 相对时间字符串
        
### _function_ (decorator)override

- **导入** `src.utils.typing`

- **说明:** 仅用于文档和阅读，不具备任何作用。用于标记子类重写父类的方法。

### _function_ (decorator)overload

- **导入** `src.utils.typing`

- **说明:** 用于标记重载的函数，方便静态类型检查。该装饰器从`typing`中导入，后续可从`src.utils.typing`导入该装饰器。