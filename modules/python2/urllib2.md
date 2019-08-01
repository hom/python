# urllib2

> 主要在`Python2`中使用，在`Python`包装到`urllib`中的`urllib.request`和`urllib.error`

## 方法

- `urllib2.urlopen(url[, data[, timeout[, cafile[, capath[, cadefault[, context]]]]])` 发送请求，可以自定义`data`和`headers`
  - `f.info()`
  - `f.read()`
  - `f.geturl()`
  - `f.getcode()`
  - `f.readline()`
  - `f.readlines()`
- `urllib2.Request(url[, data][, headers][, origin_req_host][, unverifiable])` 初始化一个`request`实例，可以在`urlopen`中使用
- `urllib2.URLError`
- `urllib2.HTTPError`
