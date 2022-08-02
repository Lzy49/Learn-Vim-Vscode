# 自定义快键键
调用内置 widgets
在 .zshrc 中直接编辑即可。
```zsh
function shibin_cls(){
  zle clear screen
}
zle -N shibin_ls
bindkey -M viins "\eg" shibin_cls
```
cat -v 查看按键对应的字符