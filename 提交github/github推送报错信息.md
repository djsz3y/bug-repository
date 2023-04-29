# `github推送报错信息`

> fatal: unable to access 'https://github.com/djsz3y/bug-repository.git/': OpenSSL SSL_read: Connection was reset, errno 10054

## 前言

执行`git push -u origin master`时，出现报错信息：

- 格式：

fatal: unable to access 'https://github.com/djsz3y/bug-repository.git/': XXX（报错信息）

- 报错信息：
  1. OpenSSL SSL_read: Connection was reset, errno 10054
  2. Failed to connect to github.com port 443 after 21154 ms: Timed out

## 解决方案

```bash
# 查看用户名，邮箱
git config user.name
git config user.email
# 修改，用户名，邮箱（我没修改，可省略）
git config --global user.name "xxx"
git config --global user.email "xxx"
# 移除仓库，重新添加
git remote rm origin
git remote add origin https://github.com/djsz3y/bug-repository.git
# 解除SSL认证
git config --global http.sslVerify "false"
# 刷新 DNS 解析缓存
#（第一次推送另一个仓库这一步完成就推送成功了）
ipconfig /flushdns
# 文件过大，超过上限
#（本仓库推送到这一步才成功）
git config http.postBuffer 5242880003
# 再次推送
git push -u origin master
```

## 参考链接

[OpenSSL SSL_read: Connection was reset, errno 10054](https://developer.aliyun.com/article/880504)
