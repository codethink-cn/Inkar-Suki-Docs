## wiki - Wiki搜索

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
