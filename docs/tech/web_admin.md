# 站务备忘

## 本地启动 & 远程部署
- 本地启动：`mkdocs serve`
- 部署到Github Pages：`mkdocs gh-deploy`

## 目录结构
在目录下新建`index.md`，即为该目录的默认根目录文件。

## 文章加密
- 插件：`mkdocs-encryptcontent-plugin`
- 在 md 文件顶部添加 YAML Front Matter：
```md
---
password: very_secret_password
---
```
注意设置密码的文档，一定要添加到`.gitignore`中，否则将造成密码泄露。

## 设置文档状态
- 在 md 文件顶部添加 YAML Front Matter：
```md
---
status: <状态>
---
```
- 可设置3种状态：`new`(新内容),`deprecated`(已弃用),`draft`(草稿)

## Github 提示框
- 插件：`Admonitions`
```md
!!! <类型>["标题"]
    1个缩进开始正文内容
```
- 类型包括：`note`(注释),`abstract`(摘要),`info`(信息),`tip`(提示),`success`(成功),`question`(问题),`warning`(警告),`failure`(失败),`danger`(危险),`bug`,`example`(示例),`quote`(引用)
- 折叠框：
```md
??? <类型>["标题"]
    1个缩进开始正文内容
```