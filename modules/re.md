# re

> `python`中的正则表达式库，有第三方包[`regex`](https://pypi.org/project/regex/)提供同样的接口，以及额外的功能和`Unicode`支持

## 常用方法

- `re.compile(pattern, flags=0)` 编译一个正则表达式对象，以便后续使用

- `re.search(pattern, string, flags=0)` 扫描整个 字符串 找到匹配样式的第一个位置，并返回一个相应的 匹配对象

- `re.match(pattern, string, flags=0)` 如果 string 开始的0或者多个字符匹配到了正则表达式样式，就返回一个相应的 匹配对象 。 如果没有匹配，就返回 None

- `re.fullmatch(pattern, string, flags=0)` 如果整个 string 匹配到正则表达式样式，就返回一个相应的 匹配对象 。 否则就返回一个 None 

- `re.split(pattern, string, maxsplit=0, flags=0)` 用 pattern 分开 string 。 如果在 pattern 中捕获到括号，那么所有的组里的文字也会包含在列表里。如果 maxsplit 非零， 最多进行 maxsplit 次分隔， 剩下的字符全部返回到列表的最后一个元素

- `re.findall(pattern, string, flags=0)` 对 string 返回一个不重复的 pattern 的匹配列表， string 从左到右进行扫描，匹配按找到的顺序返回

- `re.finditer(pattern, string, flags=0)` pattern 在 string 里所有的非重复匹配，返回为一个迭代器 iterator 保存了 匹配对象 。 string 从左到右扫描，匹配按顺序排列。空匹配也包含在结果里

- `re.sub(pattern, repl, string, count=0, flags=0)` 返回通过使用 repl 替换在 string 最左边非重叠出现的 pattern 而获得的字符串

- `re.subn(pattern, repl, string, count=0, flags=0)` 行为与 sub() 相同，但是返回一个元组 (字符串, 替换次数)

- `re.escape(pattern)` 转义 pattern 中的特殊字符

- `re.purge()` 清除正则表达式缓存

- `exception` `re.error(msg, pattern=None, pos=None)` raise 一个例外。当传递到函数的字符串不是一个有效正则表达式的时候（比如，包含一个不匹配的括号）或者其他错误在编译时或匹配时产生。如果字符串不包含样式匹配，是不会被视为错误的。错误实例有以下附加属性：
  - `msg` 未格式化的错误消息
  - `pattern` 正则表达式样式
  - `pos` 编译失败的 pattern 的位置索引（可以是 None ）
  - `lineno` 对应 pos (可以是 None) 的行号
  - `colno` 对应 pos (可以是 None) 的列号
