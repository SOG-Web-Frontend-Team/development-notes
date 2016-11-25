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

安装插件：<br />
①. AdvancedNewFile     —— 快捷键`Ctrl + Alt + N`新建并保持文件<br />
②. SyncedSideBar   ——当编辑某个文件时，对应在左边栏高亮该文件，快捷键`Ctrl + K+ B`显示左边栏<br />
③. MarkdownHighlighting   ——markdown语法高亮<br />
④. Markdown HTML Preview   ——快捷键`Ctrl + Shift + M`浏览器浏览md文件<br />
⑤. LESS<br />
⑥. All Autocomplete   ——代码提示，快捷键`Tab`自动补全<br />
⑦. HTML-CSS-JS Prettify   ——格式化代码，快捷键`Ctrl + Shift + H<br />`
⑧. SideBarEnhancements   ——自定义打开方式快捷键，定义不同的快捷键打开不同的浏览器<br />
⑨. SublimeLinter   ——语法检测，提示用户编写的代码存在不规范和错误的写法<br />
⑩. Jshint   ——运行命令：`jshit --verbose a.js`，查找对应编号代码，当js文件使用`use strict`格式时忽略警告或报错，`/* jshint -w0136 */`<br />

<br />
常见设置：

1. Sublime Text 3： How to change font size on Sidebar?
You will need to edit the  `Default.sublime-theme` file to do this,not your preferences.Unfortunately,in Sublime Text 3 this file is contained in a zipped.`.sublime-package` file.so you'll need to extract that first.Install the `PackageResourceViewer` plugin via Package Control,then hit `Ctrl + Shift +P`(`⌘ +Shift +P` on OS X) and type `prv` to bring up the PackageResourceViewer options.Select `Open Resource`,scroll down to `Theme - Default`,hit `Enter`,scroll down to `Default.sublime-theme`,and hit `Enter` again to open it.
Next,search for `sidebar_label` and modifu the first one(on line 362)to look like this(it needs to be valid JSON):

```
{
        "class": "sidebar_label",
        "color": [200, 200, 200],   //[125, 125, 125]
        "shadow_color": [0, 0, 0],
        "shadow_offset": [0, -1],
        "font.bold": false,
        "font.italic": false,
        "font.size": 16 // <-- new line
    }
```
If you want to do this in Sublime Text 2 ,it's a bit easier,as nothing is zipped up,Select `Preferences -> Browse Packgages...` to open up your `Packages` folder in your operating system's file navigator.Enter the `Theme - Default` subdirectory and open `Default.sublime-theme` as a JSON file,then edit it as above.
来源：[http://stackoverflow.com/questions/24029820/sublime-3-how-to-change-font-size-on-sidebar-ubuntu-version](http://stackoverflow.com/questions/24029820/sublime-3-how-to-change-font-size-on-sidebar-ubuntu-version)


<br /><br />





 
 
 