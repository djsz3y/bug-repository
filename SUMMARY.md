# bug 仓库

- [Introduction](README.md)

## 前言：本项目创建过程

写学习笔记，推送远端报错，想起关注的大神有 bug 仓库，我也建立一个 bug 仓库吧。

```bash
nvm list
nvm use 10.16.2
gitbook --version
cd bug-repository

git init # 初始化 git
gitbook init # 初始化 gitbook
git add . # 暂存
git commit -m "first commit" # 提交
git branch -M master # 主分支 master
git remote add origin https://github.com/djsz3y/bug-repository.git # 添加远端仓库地址
git push -u origin master # 推送远端
gitbook serve # 启动 gitbook
```

## `提交github`

- [`github推送报错信息`](提交github/github推送报错信息.md)

## 友情链接

- [我的掘金主页](https://juejin.cn/user/1042768423037150)

- [我的 github 主页](https://github.com/djsz3y)

- [读书视频学习笔记](https://github.com/djsz3y/learning-notes)

- [爪哇学习笔记](https://github.com/djsz3y/zhaowa-study-notes)

- [bug 仓库](https://github.com/djsz3y/bug-repository)
