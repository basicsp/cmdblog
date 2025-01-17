# Summary

## url

https://baike.baidu.com/item/tmux/10234491?fr=aladdin

##  [系统操作]查看当前会话 

tmux ls
## [系统操作]回到上一个会话
tmux attach
## [系统操作]切换到name=x的会话
tmux attach -t x

## [系统操作]退出当前attach（并不关闭attach）

ctrl+b d

## [窗口操作]前后一个屏幕

ctrl+b n/p

## [窗口操作]创建一个新窗口

ctrl+b c

## [面板操作]在当前面板中翻页/退出翻页

ctrl+b pgup/esc

## [面板操作]上下分屏/左右分屏

ctrl + b “  或者  %

## [面板操作]关闭当前面板

ctrl+b x（不会关闭整个tmux会话）

## [面板操作]上下<->左右分屏互相转换

ctrl + b  再按空格键

## [面板操作]同一分屏内切换面板

ctrl+b o


# Usage

| Ctrl+b      | 激活控制台；此时以下按键生效                                 |                          |
| ----------- | :----------------------------------------------------------- | ------------------------ |
| 系统操作    | ?                                                            | 列出所有快捷键；按q返回  |
| d           | 脱离当前会话；这样可以暂时返回Shell界面，输入tmux attach能够重新进入之前的会话 |                          |
| D           | 选择要脱离的会话；在同时开启了多个会话时使用                 |                          |
| Ctrl+z      | 挂起当前会话                                                 |                          |
| r           | 强制重绘未脱离的会话                                         |                          |
| s           | 选择并切换会话；在同时开启了多个会话时使用                   |                          |
| :           | 进入命令行模式；此时可以输入支持的命令，例如kill-server可以关闭服务器 |                          |
| [           | 进入复制模式；此时的操作与vi/emacs相同，按q/Esc退出          |                          |
| ~           | 列出提示信息缓存；其中包含了之前tmux返回的各种提示信息       |                          |
| 窗口操作    | c                                                            | 创建新窗口               |
| &           | 关闭当前窗口                                                 |                          |
| 数字键      | 切换至指定窗口                                               |                          |
| p           | 切换至上一窗口                                               |                          |
| n           | 切换至下一窗口                                               |                          |
| l           | 在前后两个窗口间互相切换                                     |                          |
| w           | 通过窗口列表切换窗口                                         |                          |
| ,           | 重命名当前窗口；这样便于识别                                 |                          |
| .           | 修改当前窗口编号；相当于窗口重新排序                         |                          |
| f           | 在所有窗口中查找指定文本                                     |                          |
| 面板操作    | ”                                                            | 将当前面板平分为上下两块 |
| %           | 将当前面板平分为左右两块                                     |                          |
| x           | 关闭当前面板                                                 |                          |
| !           | 将当前面板置于新窗口；即新建一个窗口，其中仅包含当前面板     |                          |
| Ctrl+方向键 | 以1个单元格为单位移动边缘以调整当前面板大小                  |                          |
| Alt+方向键  | 以5个单元格为单位移动边缘以调整当前面板大小                  |                          |
| Space       | 在预置的面板布局中循环切换；依次包括even-horizontal、even-vertical、main-horizontal、main-vertical、tiled |                          |
| q           | 显示面板编号                                                 |                          |
| o           | 在当前窗口中选择下一面板                                     |                          |
| 方向键      | 移动光标以选择面板                                           |                          |
| {           | 向前置换当前面板                                             |                          |
| }           | 向后置换当前面板                                             |                          |
| Alt+o       | 逆时针旋转当前窗口的面板                                     |                          |
| Ctrl+o      | 顺时针旋转当前窗口的面板                                     |                          |