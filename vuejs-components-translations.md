##Vue组件
#####什么是组件？
---
组件是Vue最强大的功能之一。它们帮助你扩展基本的HTML元素以封装可重用的代码。在高级别中，组件是Vue编译器附加行为的自定义元素。在某些情况下，它们也可能显示为使用特殊is属性扩展的本地HTML元素。
#####使用组件
<span style="color:#42b983;">#</span> <strong>注册</strong><br>
我们在前面的章节中学到，我们可以创建一个新的Vue实例：<br>
```markup
new Vue({
    el: '#some-element',
    // 选项
})
```
要注册全局组件，可以使用`Vue.component(tagName,options)`。例如：

```markup
Vue.component('my-component',{
    // 选项
})
```
> 请注意，Vue不强制执行自定义标记名称的[W3C规则](http://www.w3.org/TR/custom-elements/#concepts)（全小写，必须包含连字符），但遵循此约定是良好的做法。
注册后，组件可以在实例的模板中用作自定义元素`<my-component></my-component>`。在实例化根Vue实例之前，请确保组件已注册，这里是完整的例子：

<br>

```markup
<div id="example">
    <my-component></my-component>
</div>
```

```markup
//注册
Vue.component('my-component',{
    template: '<div>一个自定义组件！</div>'
})

//创建根实例
new Vue({
    el: '#example'
})
```

其中将呈现：<br>

```markup
<div id="example">
    <div>一个自定义组件！</div>
</div>
```
```
一个自定义组件！
```

<br>
<span style="color:#42b983;">#</span> <strong>本地注册</strong><br>

你不必在全球注册每个组件。通过使用`components instance`选项注册，可以使组件仅在另一个实例/组件的作用域可用：
<br>

```markup
var Child = {
    template: '<div>一个自定义组件！</div>'
}
new Vue({
    // ...
    components: {
        // <my-component> 将仅在父级模块中可用
        'my-component': Child
   }
})
```

相同的封装适用于其他可注册的Vue特征，例如指令。

<br>
<span style="color:#42b983;">#</span> <strong>DOM模板解析</strong><br>

当使用DOM作为模板（例如，使用`el`选项来安装具有现有内容的元素）时，你将受到HTML工作原理的一些限制，因为Vue只能在浏览器解析并标准化之后检索模板内容。最值得注意的是，某些元素（例如`<ul>,<ol>,<table>`和`<select>`）对其中可能出现的元素有限制，而某些元素（如`<option>`）只能出现在某些其他元素中。
当使用具有此类限制的元素的自定义组件时，这将导致问题，例如：

```markup
<table>
    <my-row>...</my-row>
</table>
```

自定义组件`<my-row>`将被提升为无效内容，从而导致最终呈现的输出错误。解决方法是使用特殊属性：
```markup
<table>
    <tr is='my-row'>...</tr>
</table>
```
应当注意，如果使用来自以下来源之一的字符串模板，这些限制不适用：
- `<script type="text/x-template"`>
- JavaScript inline template strings
- `.vue` components
<br>

因此，尽可能使用字符串模板。




