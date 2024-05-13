## github - GitHub

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
