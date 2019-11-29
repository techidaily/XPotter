# 如何解决

## plist 文件批量重改如何做

PlistBuddy
[介绍](https://www.jianshu.com/p/2167f755c47e)
[http://fgimian.github.io/blog/2015/06/27/a-simple-plistbuddy-tutorial/](http://fgimian.github.io/blog/2015/06/27/a-simple-plistbuddy-tutorial/)

1. 批量添加 `LSHandlerRank`='Owner'

[https://forum.xojo.com/54662-mas-incomplete-document-type-configuration/0](https://forum.xojo.com/54662-mas-incomplete-document-type-configuration/0)

由于PlistBuddy并不在Mac默认的Path里，所以我们得通过绝对路径来引用这个工具：

```bash
/usr/libexec/PlistBuddy --help
```

