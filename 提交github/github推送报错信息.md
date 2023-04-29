# `github推送报错信息`

## 前言

执行`git push -u origin master`时，出现报错信息：

- 格式：

fatal: unable to access 'https://github.com/XXX.git/': XXX（报错信息）

- 报错信息：
  1. OpenSSL SSL_read: Connection was reset, errno 10054
  2. Failed to connect to github.com port 443 after 21154 ms: Timed out

## 1.OpenSSL SSL_read: Connection was reset, errno 10054

解决方案

```bash
$ git config --global http.sslVerify "false"
```

## 2.Failed to connect to github.com port 443 after 21154 ms: Timed out

解决方案

```bash
$ ipconfig /flushdns

# Windows IP 配置

# 已成功刷新 DNS 解析缓存。
```

## 参考链接

[OpenSSL SSL_read: Connection was reset, errno 10054](https://developer.aliyun.com/article/880504)
