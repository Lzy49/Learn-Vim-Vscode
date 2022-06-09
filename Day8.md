# 查询
## 行查询
### 进入搜索模式
- f + 搜索内容 : 向右搜索
- F + 搜索内容 : 向左搜索 
- t + 搜索内容 : 向右搜索
- T + 搜索内容 : 向左搜索
### 切换搜索内容
- ; 继续下一个
- , 继续上一个
### 例
```text
abc abc abcd ABCD
```
在上面这段文字中：
- 光标在 0 时 y + f + a 可以复制 `abc a`
- 光标在 0 时 y + t + a 可以复制 `abc `
- 光标在 0 时 v + f + a + ; 可以选中 `abc abc a`
### 技巧
因为 f 会将搜索字符也选中，所以在移动时使用 f，在复制，删除，选中一段内容时使用 t。
## 全局查询 某些字符
### 进入搜索
- / + 搜索内容 + enter : 向后查询 某些字符。
- ? + 搜索内容 + enter : 向前查询 某些字符。
### 移动
- n : 下一个
- N : 上一个
### 进入搜索并搜索上次搜索内容
- / or ? + k : 搜索上一次搜索内容。
### 例
```text
abcabcAbcAbc
abcabcAbcAbc
abcabcAbcAbc
abcabcAbcAbc
abcabcAbcAbc
abcabcAbcAbc
abcabcAbcAbc
```
在上面这段文字中使用：
- 在第一行0位置中 / + a + enter + n 回到第一行Abc 的位置
- 在第一行0位置中 ? + a + enter + n 会在第一行 a 的位置 (不动)
## 严格搜索某单词
### 进入
光标放到想要搜索的单词上按下以下按键：
- `#` : 向上严格搜查某单词
- `*` : 向下严格搜索某单词。
### 移动
- n : 下一个
- N : 上一个
### 例
```text
abcdefg
abcdefg
abcdefg
abcdefg
abcdefg
abcdefga

```
在以上代码中，光标在 abcdefg 上使用 `#` / `*` 时只会搜索 abcdefg 不会搜索 abcdefga
