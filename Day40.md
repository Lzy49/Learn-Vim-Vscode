# zellij 高级使用
## 回话功能
> 可以保存一个tag里的所有内容
- zellij a -c xx 创建一个叫 xx 的回话
- zellij o d 保存当前创建的回话（如果不保存直接 q 的话不会保存回话）
- zellij a xx 打开xx 回话
- zellij ls 查看所有回话
- zellij k xx 删除 xx 回话
- zellij ka 删除全部回话
## 同步所有窗口一起输入
- control t s 开启同步
- control t s 关闭同步
## 内容滚动
- control s  开启滚动模式
- hjkl 
- u d 翻页
## 清空
- clear 清空

## 修改配置
- 创建配置：mkdir ~/.config/zellij
- 将默认配置挡下来：zellij setup --dump-config > ~/.config/zellij/
config.yaml
- vim  ~/.config/zellij/config.yaml
- 然后开始愉快的改改改 