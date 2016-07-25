###文件/资源命名
所有HTML内资源的以xxx-xxx.js, xxx-xxx.css class&id格式也应该是xxx-xx。
不推荐
MyScript.js
myCamelCaseName.css
i_love_underscores.html
1001-scripts.js //命名禁止编号
my-file-min.css
js内请使用驼峰命名。


###http/https
当引入图片或其他媒体文件，还有样式和脚本时，URLs 所指向的具体路径，不要指定协议部分（http:, https:），除非这两者协议都不可用。不推荐
<script src="http://cdn.com/xxx.min.js"></script>
推荐
<script src="//cdn.com/xxx.min.js"></script>
不推荐
.example {
  background: url(http://static.example.com/images/bg.jpg);
}
推荐
.example {
  background: url(//static.example.com/images/bg.jpg);
}
在本地的时候可以用http，上传服务器的时候请抹掉。

###文本缩进
请设置缩进为tab。不要使用实际空格。这样在层次少的时候可以设置tab缩进等于4个空格。层多可以设置为2个空格

###注释
注释是你自己与你的小伙伴们了解代码写法和目的的唯一途径。特别是在写一些看似琐碎的无关紧要的代码时，由于记忆点不深刻，注释就变得尤为重要了。

编写自解释代码只是一个传说，没有任何代码是可以完全自解释的。而代码注释，则是永远也不嫌多。

当你写注释时一定要注意：不要写你的代码都干了些什么，而要写你的代码为什么要这么写，背后的考量是什么。当然也可以加入所思考问题或是解决方案的链接地址。

不推荐
var offset = 0;
 
if(includeLabels) {
  // Add offset of 20
  offset = 20;
}
推荐
var offset = 0;
 
if(includeLabels) {
  // If the labels are included we need to have a minimum offset of 20 pixels
  // We need to set it explicitly because of the following bug: http://somebrowservendor.com/issue-tracker/ISSUE-1
  offset = 20;
}
一些注释工具可以帮助你写出更好的注释。JSDoc 或 YUIDoc 就是用来写 JavaScript 注释用的。你甚至可以使用工具来为这些注释生成文档，这也是激励开发者们写注释的一个好方法，因为一旦有了这样方便的生成文档的工具，他们通常会开始花更多时间在注释细节上。

###代码检查

对于比较宽松自由的编程语言来说，严格遵循编码规范和格式化风格指南就显得极为重要。遵循规范固然很好，但是有自动化流程来确保其执行情况，岂不更佳。Trust is good, control is better.

对于 JavaScript，建议使用 JSLint 或 JSHint。
