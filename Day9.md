
# 想去哪就去哪

## vim-easymotion

### 配置

```JSON
"vim.easymotion": true, // 开启 vim-easymotion
"vim.leader": "<Space>", // 设置开启键为 空格
```

### 命令

- 只会识别英文，中文不参加
- space + space 开启
  - w : 向下指向每个单词的首字母
  - e : 向下指向每个单词的结尾字母
  - l : 向下指向每个单词的首尾字母
  - b : 向上指向每个单词的首字母
  - ge : 向上指向每个单词的结尾字母
  - h : 向上指向每个单词的的首尾字母
  - j : 向下指向没一行
  - k : 向上指定每一行
- space + space + space + j : 搜索所有的单词的首尾

## vim-sneak
### 配置
主要完成三件事：
- 开启 sneak 功能
- 将 s 键的功能替换回原来的 s 键功能
- 将 f 键功能替换成 vim-sneak 插件
```json
 {
   "vim.sneak": true,
   "vim.normalModeKeyBindingsNonRecursive": [
        {
            "before":[
                "f"
            ],
            "after": [
                "s"
            ],
        },
        {
            "before": [
                "F"
            ],
            "after": [
                "S"
            ]
        },
        {
            "before": [
                "s"
            ],
            "after": [
                "c",
                "l"
            ]
        },
        {
            "before": [
                "S"
            ],
            "after": [
                "^",
                "C"
            ]
        },
    ],
    "vim.visualModeKeyBindingsNonRecursive": [
        {
            "before": [
                "f"
            ],
            "after": [
                "s"
            ]
        },
    ],
    "vim.operatorPendingModeKeyBindingsNonRecursive": [
        {
            "before": [
                "f"
            ],
            "after": [
                "z"
            ]
        },
        {
            "before": [
                "F"
            ],
            "after": [
                "Z"
            ]
        },
    ],
 }

```
### 命令
- f + 两个字符向下搜索这两个字符
- F + 两个字符向上搜索这两个字符