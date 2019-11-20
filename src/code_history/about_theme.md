# 关于代码主题的问题

## 如何获取主题所在的目录

主题的目录一般为了防止丢失，

存放的目录："~/Library/Containers/com.techidaily.XPotter.Editor/Data/Library/Application Support/XPotter/themes"
这么做的有利于后面将主题包作为付费插件来实现安装。

## 对应的Rust编码部分

```rust
/// core-lib/src/config.rs

/// Path to themes sub directory inside config directory.
/// Creates one if not present.
pub(crate) fn get_themes_dir(&self) -> Option<PathBuf> {
    let themes_dir = self.config_dir.as_ref().map(|p| p.join("themes"));

    if let Some(p) = themes_dir {
        if p.exists() {
            return Some(p);
        }
        if fs::DirBuilder::new().create(&p).is_ok() {
            return Some(p);
        }
    }
    None
}
```