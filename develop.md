# 开发

本章节主要讲述如何在`Inkar Suki`的基础代码上进行开发以及代码规范。

!> 如果您是所谓的职业开发者并尝试对音卡使用所谓的行业规范，请立刻关闭本页面，我们不欢迎一味追求自己的行业规范的开发者。

点击[此处](/utils)可以查看对于`Inkar Suki`开发的一些组件和帮助。

## 代码规范

尽可能贴近[PEP-8](https://peps.python.org/pep-0008/)，但部分例外由仓库主进行制定，幅度不大，因此你可以按`PEP-8`提交，剩下的交给`Review Request`。

## GitHub

### Commit

**如果您具有仓库的`Write`权限，请不要把`Pull Request`当做`Push`使用！**

`Commit`的规范在这里特别强调，我们推荐使用中文，但开发者仍然可以提交英文，唯注意下面的格式即可。

格式：`<模块名>[类型]概述`。

类型的标识符大小写均可以接受，推荐使用小写英文，例如：`<jx3>[feat]更新副本记录[feat]删除交易行`（仅作举例，不对应任何`commit`）。

如果一个`commit`包含多个更改，若来自同一个模块可以省去`<>`，但仍需要标注修改类型！

类型和标识符列表：

|类型|标识符简写|标识符全称|介绍|示例|
|-----|-----|-----|-----|-----|
|`feature（特性）`|`feat`|`feature`|`特性的更改（包括更新、删除等）。`|`<jx3>[feat]交易行重写。`|
|`refactor（格式化）`|`ref`|`refactor`|`代码整理（不影响或极少影响功能本体）。`|`<jx3>[feat]整理楚天社代码。`|

目前大概只需要这两个标识符，如有其他需求，请对文档进行`Pull Request`！

### 代码所有权

**当您上传您的代码到音卡的仓库时，您仍然具有代码的所有权，不过保留与否取决于仓库主，因此如果您脱离`Inkar Suki`的开发且仓库主并不想删除的情况下，您无法删除您在本仓库所作出的贡献！同时，如果使用同样的代码，需要遵守AGPLv3.0协议，对修改后的代码进行再次开源！**