# iTerm 插件
## copypath & copyfile
- 安装 ： 插件是自带的，不需要进行安装。
- 配置 ： 直接在 plugins 中配置即可
- 使用 ： 直接打 `copypath` 和 `copyfile` 命令即可
- 功能 ： copypath 复制当前文件路径， copyfile 复制当前文件内容
##  zsh-autosuggestions
- 安装 ：git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
- 官网 ：https://github.com/zsh-users/zsh-autosuggestions
- 作用 ：在输入命令时不正确时候颜色会不对
- 使用 ：被动
## autojump
- 安装 ：brew install autojump
- 官网 ：https://github.com/wting/autojump
- 配置 ：直接在
- 作用 ： 可以直接跳转到经常使用的文件夹
- 使用 ：
  - j xx ： 进入某文件
  - jo xx ： 打开某文件
  - j -i ： 为当前路径增加权重
  - j -d ： 为当前路径减少权重
  - j -s ： 查看记录 
## zsh-syntax-highlighting
- 安装 ： git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
- 官网 ： https://github.com/zsh-users/zsh-syntax-highlighting
- 配置 ： 直接在 plugins 中配置即可
- 作用 ： 提示经常写的内容
- 使用 ： → 选择
# 原理
.zshrc 文件中的 plugin 会在 .oh-my-zs 目录的 plugins 或 custom/plugins 中找以.plugin.zsh结尾的文件执行。