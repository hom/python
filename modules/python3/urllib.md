# urllib

> `Python`中发送网络请求

## Python2

### 常用方法

- `urllib.urlopen(url[, data[, proxies[, context]]])` 打开一个连接，返回描述符
  - `f.info()` 返回的头部信息
  - `f.geturl()` 请求的`url`
  - `f.getcode` 获取返回的状态码
  - `f.read()` 获取返回的响应内容
  - `f.readline()` 读取响应的一行
  - `f.readlines()` 读取响应的多行
  - `f.close()` 关闭请求

- `urllib.urlencode()`编码请求的参数

## Python3

> `urllib`是一个收集了多个用到`URL`的模块的包

### 常用方法

- `urllib.request` 打开和读取 `URL`
  - `urllib.request.urlopen(url, data=None, [timeout, ]*, cafile=None, capath=None, cadefault=False, context=None)`
  - `urllib.request.Request(url, data=None, headers={}, origin_req_host=None, unverifiable=False, method=None)` 和`urllib2.Request`使用方法一致
- `urllib.error` 包含 `urllib.request` 抛出的异常
  - `urllib.error.URLError`
  - `urllib.error.HTTPError`
- `urllib.parse` 用于解析 `URL`
- `urllib.robotparser` 用于解析 `robots.txt` 文件
