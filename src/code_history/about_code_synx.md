# 关于支持的代码格式，扩展名，展示样式的处理

## 目录说明

支持代码格式，主要来源于 `syntect-plugin` 插件。

`../XPotter/xi-editor/rust/syntect-plugin` 目录下面有一个重要的资源：`syntect-resources` 目录
这个目录是一个git submodule 更新的。git远程地址现在为：

* 首先，需要在 `../XPotter/xi-editor/rust/syntect-plugin/example` 目录中，生成 `make_manifest` 可执行文件

* 其次，将来自 `~/GitHub/rust-lang/good-projects/bat/assets/syntaxes` 目录下的所有文件，（将目录下`Packages`目录排除）比较合并到 `../XPotter/xi-editor/rust/syntect-plugin/syntect-resources/Packages` 下面；同理，将`~/GitHub/rust-lang/good-projects/bat/assets/syntaxes/Packages` 目录下的文件同步到 `../XPotter/xi-editor/rust/syntect-plugin/syntect-resources/Packages` 下面，

* 然后，将生成的 `make_manifest` 可执行文件，放到与 ``../XPotter/xi-editor/rust/syntect-plugin` 目录下，与 `syntect-resources` 在同一目录下面。 然后执行 `make_mainfest` 文件。

## front 获取语法说明

1. 前端所有的消息都靠这个来处理： `Sources/Editor/Core/CoreNotification.swift`

## 更新说明

### 2019.11.20

* `~/GitHub/rust-lang/good-projects/bat/assets/syntaxes` 版本号：9b1930b2b303309374502dc98989322a8ddd15be