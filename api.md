# API

`Inkar Suki`官方文档开放了极少数接口供`Inkar Suki`实例调用。

本站`Token`请自行在互联网搜索，**请勿提交`JX3API`的`token`！**下面的`Token`均为示例，并无效。

如果没有特殊说明，所有参数均为必选！

## 交易行物品

> 贡献者：`HornCopper`。

> 请求方式(GET)

```
https://inkar-suki.codethink.cn/trade
```

> 请求参数

```json
{
    "server": "幽月轮",
    "name": "泣麟砂",
    "token": "114514"
}
```

> 返回样例

```json
{
    "code": 200,
    "data": [
        {
            "icon": "https://icon.jx3box.com/icon/20061.png",
            "color": "(254, 45, 254)",
            "name": "泣麟砂",
            "time_str": "03月12日 22:24:51",
            "time_raw": 1710253491,
            "limit": "1",
            "price_str": "1 砖 6226 金 88 银",
            "price_raw": 162268800,
            "overview": {
                "low": "1 砖 1000 金 5 银",
                "avg": "1 砖 3070 金 3 银 41 铜",
                "high": "1 砖 3999 金 87 银"
            }
        },
        {
            "icon": "https://icon.jx3box.com/icon/20061.png",
            "color": "(254, 45, 254)",
            "name": "泣麟砂",
            "time_str": "03月12日 22:24:51",
            "time_raw": 1710253491,
            "limit": "2",
            "price_str": "1 砖 4326 金 88 银",
            "price_raw": 143268800,
            "overview": {
                "low": "1 砖 1000 金 5 银",
                "avg": "1 砖 3070 金 3 银 41 铜",
                "high": "1 砖 3999 金 87 银"
            }
        },
        {
            "icon": "https://icon.jx3box.com/icon/20061.png",
            "color": "(254, 45, 254)",
            "name": "泣麟砂",
            "time_str": "03月12日 22:24:51",
            "time_raw": 1710253491,
            "limit": "1",
            "price_str": "1 砖 3999 金 87 银",
            "price_raw": 139998700,
            "overview": {
                "low": "1 砖 1000 金 5 银",
                "avg": "1 砖 3070 金 3 银 41 铜",
                "high": "1 砖 3999 金 87 银"
            }
        },
        {
            "icon": "https://icon.jx3box.com/icon/20061.png",
            "color": "(254, 45, 254)",
            "name": "泣麟砂",
            "time_str": "03月12日 22:24:51",
            "time_raw": 1710253491,
            "limit": "1",
            "price_str": "1 砖 3999 金 84 银",
            "price_raw": 139998400,
            "overview": {
                "low": "1 砖 1000 金 5 银",
                "avg": "1 砖 3070 金 3 银 41 铜",
                "high": "1 砖 3999 金 87 银"
            }
        },
        {
            "icon": "https://icon.jx3box.com/icon/20061.png",
            "color": "(254, 45, 254)",
            "name": "泣麟砂",
            "time_str": "03月12日 22:24:51",
            "time_raw": 1710253491,
            "limit": "1",
            "price_str": "1 砖 3999 金 29 银",
            "price_raw": 139992900,
            "overview": {
                "low": "1 砖 1000 金 5 银",
                "avg": "1 砖 3070 金 3 银 41 铜",
                "high": "1 砖 3999 金 87 银"
            }
        },
        {
            "icon": "https://icon.jx3box.com/icon/20061.png",
            "color": "(254, 45, 254)",
            "name": "泣麟砂",
            "time_str": "03月12日 22:24:51",
            "time_raw": 1710253491,
            "limit": "1",
            "price_str": "1 砖 2761 金 99 银",
            "price_raw": 127619900,
            "overview": {
                "low": "1 砖 1000 金 5 银",
                "avg": "1 砖 3070 金 3 银 41 铜",
                "high": "1 砖 3999 金 87 银"
            }
        },
        {
            "icon": "https://icon.jx3box.com/icon/20061.png",
            "color": "(254, 45, 254)",
            "name": "泣麟砂",
            "time_str": "03月12日 22:24:51",
            "time_raw": 1710253491,
            "limit": "1",
            "price_str": "1 砖 2666 金 66 银",
            "price_raw": 126666600,
            "overview": {
                "low": "1 砖 1000 金 5 银",
                "avg": "1 砖 3070 金 3 银 41 铜",
                "high": "1 砖 3999 金 87 银"
            }
        },
        {
            "icon": "https://icon.jx3box.com/icon/20061.png",
            "color": "(254, 45, 254)",
            "name": "泣麟砂",
            "time_str": "03月12日 22:24:51",
            "time_raw": 1710253491,
            "limit": "1",
            "price_str": "1 砖 2555 金 29 银",
            "price_raw": 125552900,
            "overview": {
                "low": "1 砖 1000 金 5 银",
                "avg": "1 砖 3070 金 3 银 41 铜",
                "high": "1 砖 3999 金 87 银"
            }
        },
        {
            "icon": "https://icon.jx3box.com/icon/20061.png",
            "color": "(254, 45, 254)",
            "name": "泣麟砂",
            "time_str": "03月12日 22:24:51",
            "time_raw": 1710253491,
            "limit": "1",
            "price_str": "1 砖 2554 金 27 银",
            "price_raw": 125542700,
            "overview": {
                "low": "1 砖 1000 金 5 银",
                "avg": "1 砖 3070 金 3 银 41 铜",
                "high": "1 砖 3999 金 87 银"
            }
        },
        {
            "icon": "https://icon.jx3box.com/icon/20061.png",
            "color": "(254, 45, 254)",
            "name": "泣麟砂",
            "time_str": "03月12日 22:24:51",
            "time_raw": 1710253491,
            "limit": "1",
            "price_str": "1 砖 2478 金 5 银",
            "price_raw": 124780500,
            "overview": {
                "low": "1 砖 1000 金 5 银",
                "avg": "1 砖 3070 金 3 银 41 铜",
                "high": "1 砖 3999 金 87 银"
            }
        },
        {
            "icon": "https://icon.jx3box.com/icon/20061.png",
            "color": "(254, 45, 254)",
            "name": "泣麟砂",
            "time_str": "03月12日 22:24:51",
            "time_raw": 1710253491,
            "limit": "2",
            "price_str": "1 砖 2477 金 88 银",
            "price_raw": 124778800,
            "overview": {
                "low": "1 砖 1000 金 5 银",
                "avg": "1 砖 3070 金 3 银 41 铜",
                "high": "1 砖 3999 金 87 银"
            }
        },
        {
            "icon": "https://icon.jx3box.com/icon/20061.png",
            "color": "(254, 45, 254)",
            "name": "泣麟砂",
            "time_str": "03月12日 22:24:51",
            "time_raw": 1710253491,
            "limit": "3",
            "price_str": "1 砖 2477 金 5 银",
            "price_raw": 124770500,
            "overview": {
                "low": "1 砖 1000 金 5 银",
                "avg": "1 砖 3070 金 3 银 41 铜",
                "high": "1 砖 3999 金 87 银"
            }
        },
        {
            "icon": "https://icon.jx3box.com/icon/20061.png",
            "color": "(254, 45, 254)",
            "name": "泣麟砂",
            "time_str": "03月12日 22:24:51",
            "time_raw": 1710253491,
            "limit": "1",
            "price_str": "1 砖 2077 金 88 银",
            "price_raw": 120778800,
            "overview": {
                "low": "1 砖 1000 金 5 银",
                "avg": "1 砖 3070 金 3 银 41 铜",
                "high": "1 砖 3999 金 87 银"
            }
        },
        {
            "icon": "https://icon.jx3box.com/icon/20061.png",
            "color": "(254, 45, 254)",
            "name": "泣麟砂",
            "time_str": "03月12日 22:24:51",
            "time_raw": 1710253491,
            "limit": "1",
            "price_str": "1 砖 1878 金 5 银",
            "price_raw": 118780500,
            "overview": {
                "low": "1 砖 1000 金 5 银",
                "avg": "1 砖 3070 金 3 银 41 铜",
                "high": "1 砖 3999 金 87 银"
            }
        },
        {
            "icon": "https://icon.jx3box.com/icon/20061.png",
            "color": "(254, 45, 254)",
            "name": "泣麟砂",
            "time_str": "03月12日 22:24:51",
            "time_raw": 1710253491,
            "limit": "1",
            "price_str": "1 砖 1776 金 5 银",
            "price_raw": 117760500,
            "overview": {
                "low": "1 砖 1000 金 5 银",
                "avg": "1 砖 3070 金 3 银 41 铜",
                "high": "1 砖 3999 金 87 银"
            }
        }
    ]
}
```

## 百战异闻录

> 贡献者：`HornCopper`。

> 请求方式（GET）

```
https://inkar-suki.codethink.cn/monsters
```

> 请求参数

```json
{
    "token": "114514"
}
```

> 返回样例

```json
{
    "code": 200,
    "map": [
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 1,
            "name": "肖童",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/4558.png",
            "count": 2,
            "name": "鬼影小次郎",
            "desc": "",
            "coin": "+100"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 3,
            "name": "秦雷",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 4,
            "name": "程沐华",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/4577.png",
            "count": 5,
            "name": "方宇谦",
            "desc": "后六翻倍",
            "coin": "+50"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 6,
            "name": "冯度",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 7,
            "name": "源明雅",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/13547.png",
            "count": 8,
            "name": "罗翼",
            "desc": "稀有提高",
            "coin": "+80"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 9,
            "name": "陆寻",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 10,
            "name": "武逸青",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/3313.png",
            "count": 11,
            "name": "源明雅",
            "desc": "随机前进",
            "coin": "+80"
        },
        {
            "icon": "https://icon.jx3box.com/icon/13548.png",
            "count": 12,
            "name": "钱宗龙",
            "desc": "秒杀首领",
            "coin": "+80"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 13,
            "name": "华鹤炎",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/3313.png",
            "count": 14,
            "name": "冯度",
            "desc": "随机前进",
            "coin": "+80"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 15,
            "name": "陆寻",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 16,
            "name": "罗翼",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/4577.png",
            "count": 17,
            "name": "上衫勇刀",
            "desc": "后六翻倍",
            "coin": "+50"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 18,
            "name": "韦柔丝",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 19,
            "name": "肖童",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 20,
            "name": "牡丹",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 21,
            "name": "华鹤炎",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/4573.png",
            "count": 22,
            "name": "肖童",
            "desc": "",
            "coin": "+300"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 23,
            "name": "程沐华",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/13548.png",
            "count": 24,
            "name": "陆寻",
            "desc": "秒杀首领",
            "coin": "+80"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 25,
            "name": "冯度",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/4543.png",
            "count": 26,
            "name": "钱宗龙",
            "desc": "前六减半",
            "coin": "+50"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 27,
            "name": "秦雷",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 28,
            "name": "罗翼",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/4576.png",
            "count": 29,
            "name": "韦柔丝",
            "desc": "后跃三步",
            "coin": "+100"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 30,
            "name": "谢云流",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 31,
            "name": "华鹤炎",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/13547.png",
            "count": 32,
            "name": "源明雅",
            "desc": "稀有提高",
            "coin": "+80"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 33,
            "name": "钱南撰",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 34,
            "name": "韦柔丝",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/3313.png",
            "count": 35,
            "name": "秦雷",
            "desc": "随机前进",
            "coin": "+80"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 36,
            "name": "方宇谦",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 37,
            "name": "罗翼",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 38,
            "name": "程沐华",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 39,
            "name": "上衫勇刀",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/4533.png",
            "count": 40,
            "name": "提多罗吒",
            "desc": "",
            "coin": "+300"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 41,
            "name": "华鹤炎",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 42,
            "name": "恶战灵霄峡",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/4543.png",
            "count": 43,
            "name": "韦柔丝",
            "desc": "前六减半",
            "coin": "+50"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 44,
            "name": "陆寻",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 45,
            "name": "冯度",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/13548.png",
            "count": 46,
            "name": "钱宗龙",
            "desc": "秒杀首领",
            "coin": "+80"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 47,
            "name": "源明雅",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 48,
            "name": "钱南撰",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/4576.png",
            "count": 49,
            "name": "程沐华",
            "desc": "后跃三步",
            "coin": "+100"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 50,
            "name": "悉达罗摩",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 51,
            "name": "鬼影小次郎",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 52,
            "name": "华鹤炎",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 53,
            "name": "秦雷",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/4577.png",
            "count": 54,
            "name": "方宇谦",
            "desc": "后六翻倍",
            "coin": "+50"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 55,
            "name": "韦柔丝",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/4558.png",
            "count": 56,
            "name": "钱南撰",
            "desc": "",
            "coin": "+100"
        },
        {
            "icon": "https://icon.jx3box.com/icon/13547.png",
            "count": 57,
            "name": "源明雅",
            "desc": "稀有提高",
            "coin": "+80"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 58,
            "name": "冯度",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 59,
            "name": "上衫勇刀",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 60,
            "name": "卫栖梧",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 61,
            "name": "上衫勇刀",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/4573.png",
            "count": 62,
            "name": "恶战日轮山城",
            "desc": "",
            "coin": "+300"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 63,
            "name": "方宇谦",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/4558.png",
            "count": 64,
            "name": "冯度",
            "desc": "",
            "coin": "+100"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 65,
            "name": "韦柔丝",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/3313.png",
            "count": 66,
            "name": "源明雅",
            "desc": "随机前进",
            "coin": "+80"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 67,
            "name": "程沐华",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/4533.png",
            "count": 68,
            "name": "陆寻",
            "desc": "",
            "coin": "+300"
        },
        {
            "icon": "https://icon.jx3box.com/icon/18505.png",
            "count": 69,
            "name": "钱南撰",
            "desc": "",
            "coin": ""
        },
        {
            "icon": "https://icon.jx3box.com/icon/13547.png",
            "count": 70,
            "name": "阿基修斯",
            "desc": "稀有提高",
            "coin": "+80"
        }
    ],
    "start": 1710777600,
    "start_str": "03月19日 00:00:00",
    "update": 1710850636,
    "update_str": "03月19日 20:17:16"
}
```

## 四马场刷新

> 贡献者：`HornCopper`。

> 请求方式(GET)

```
https://inkar-suki.codethink.cn/horse
```

> 请求参数

```json
{
    "token": "114514",
    "server": "唯我独尊"
}
```

> 返回样例

```json
{
    "code": 200,
    "msg": "鲲鹏岛\n时间尚久，无法预知。\n-------------------------------\n阴山大草原\n龙子/麟驹 将于10分钟后刷新\n赤兔 将于139分钟后刷新\n-------------------------------\n黑戈壁\n龙子/麟驹 将于34分钟后刷新\n------------------------------"
}
```

## 拉格兰下载

> 贡献者：`HornCopper`。

> 请求方式(GET)

```
https://inkar-suki.codethink.cn/lagrange
```

> 请求参数

```json
{
    "os": "win",
    "platform": "x64",
    "net": "8.0",
    "musl": false
}
```

> `os`、`platform`均为必选参数。<br>
> `net`、`musl`均为可选参数。

> 返回样例

```json
{
    "code": 200,
    "data": "https://productionresultssa12.blob.core.windows.net/actions-results/de82b6b5-c00a-47b7-986e-b10749f93d70/workflow-job-run-68eff7cc-7efd-56c8-0853-73f284dbdacc/artifacts/987ecb070cc7d8c8348225a4b431222e24c3e6ac4361e5ff0a23a6e8463c134b.zip?rscd=attachment%3B+filename%3D%22Lagrange.OneBot_linux-arm64_7.0.zip%22&se=2024-03-25T07%3A25%3A32Z&sig=GMQJ0F5JfqLAjMzwc7psNybvBfkgJdUuPcunH04oz%2Bo%3D&sp=r&spr=https&sr=b&st=2024-03-25T07%3A15%3A27Z&sv=2021-12-02"
}
```