# zsh-vi-mode 高级实用
- 选中后 S + "  添加 双引号
- 选中后 y + s + " 添加双引号
- 修改单词双引号 → 单引号 ：选中 单词 c + s + " + '
- 删除单词双引号 ： d + s + "
# 改键
1. 通过 .zshrc 文件中的 source 的路径找到 zsh-vi-mode 的位置。
2. 在 zsh-vi-mode 文件夹中的有一个 zsh-vi-mode.zsh 文件。在这个文件中可以完成自己想要的逻辑编辑。
```zsh
function jump_end_of_line(){
  zvm_navigation_handler $
}
function jump_start_of_line(){
   zvm_navigation_handler ^
}
function zvm_after_lazy_keybindings(){
  zvm_define_widget jump_end_of_line
  zvm_define_widget jump_start_of_line
  zvm_bindkey vicmd 'L' jump_end_of_line
  zvm_bindkey visual 'L' jump_end_of_line
  zvm_bindkey vicmd 'H' jump_start_of_line
  zvm_bindkey visual 'H' jump_start_of_line
}
```
# 修改复制
```zsh
function zvm_vi_yank() {
   zvm_yank
   echo ${CUTBUFFER} | pbcopy
   zvm_exit_visual_mode
}
```