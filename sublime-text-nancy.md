####Sublime Text 基本使用
---
由于Sublime Text支持大量插件，需要安装Package Control来进行浏览、安装和卸载这些插件，步骤为：`` Ctrl + ` ``打开控制台，黏贴下面的代码到控制台里：
``` 
import urllib.request,os,hashlib; h = 'df21e130d211cfc94d9b0905775a7c0f' + '1e3d39e33b79698005270310898eea76'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```
1. 当Package Control安装后，可以通过 `Ctrl + Shift + p` 查看默认配置文件，输入`Settings - Syntax Specific `
 
2.  通过`Ctrl + Shift + p`查看默认配置的快捷键 ，输入`Key Bindings `，可缩写成`kb`

3.  Sublime Text 快捷键

* `Ctrl + Shift + P` 打开命令面板
* `Ctrl + P` 搜索项目文件
* `Ctrl + G` 跳转到第几行
* `Ctrl + W` 关闭当前打开的文件
* `Ctrl + Shift + W` 关闭所有打开的文件
* `Ctrl + D` 选中光标所占的文本，继续操作则会选中下一个相同的文本。
* `Alt + F3` 选中文本按下快捷键，即可一次性选择全部的相同文本进行同时编辑
* `Ctrl + L` 选中整行，继续操作则继续选择下一行，效果和 Shift+↓ 效果一样。
* `Ctrl + Shift + L` 先选中多行，再按下快捷键，会在每行行尾插入光标，即可同时编辑这些行
* `Ctrl + Shift + M` 选择括号内的内容（继续选择父括号）
* `Ctrl + M` 光标移动至括号内结束或开始的位置
* `Ctrl + Enter` 在下一行插入新行
* `Ctrl + Shift + Enter` 在上一行插入新行
* `Ctrl + Shift + [` 选中代码，按下快捷键，折叠代码
* `Ctrl + Shift + ]` 选中代码，按下快捷键，展开代码
* `Ctrl + ←` 向左单位性地移动光标，快速移动光标
* `Ctrl + →` 向右单位性地移动光标，快速移动光标
* `Shift + ↑` 向上选中多行
* `Shift + ↓` 向下选中多行
* `Shift + ←` 向左选中文本
* `Shift + →` 向右选中文本
* `Ctrl + Shift + ←` 向左单位性地选中文本
* `Ctrl + Shift + →` 向右单位性地选中文本
* `Ctrl + Shift + ↑` 将光标所在行和上一行代码互换
* `Ctrl + Shift + ↓` 将光标所在行和下一行代码互换
* `Ctrl + Alt + ↑` 向上添加多行光标，可同时编辑多行
* `Ctrl + Alt + ↓` 向下添加多行光标，可同时编辑多行
* `Ctrl+J` 合并选中的多行代码为一行 
* `Ctrl+Shift+D` 复制光标所在整行，插入到下一行
* `Tab` 向右缩进
* `Shift + Tab` 向左缩进
* `Ctrl + K + K` 从光标处开始删除代码至行尾。
* `Ctrl + Shift + K` 删除整行
* `Ctrl + /` 注释单行
* `Ctrl + Shift + /` 注释多行
* `Ctrl + Z` 撤销
* `Ctrl + Y` 恢复撤销
* `Ctrl + U` 软撤销，和 `Gtrl + Z` 一样
* `Ctrl + T` 左右字母互换
* `Ctrl + Tab` 按文件浏览过的顺序，切换当前窗口的标签页
* `Ctrl + PageDown` 向左切换当前窗口的标签页
* `Ctrl + PageUp` 向右切换当前窗口的标签页
* `Alt + Shift + 1` 窗口分屏，恢复默认1屏（非小键盘的数字）
* `Alt + Shift + 2` 左右分屏-2列
* `Alt + Shift + 3` 左右分屏-3列
* `Alt + Shift + 4` 左右分屏-4列
* `Alt + Shift + 5`等分4屏
* `Ctrl + K + B` 开启/关闭侧边栏
<br /><br />



####GitHub 与 Git指令
---
1.  创建账号，登录GitHub网站 [https://github.com/](https://github.com/)




 
 
 