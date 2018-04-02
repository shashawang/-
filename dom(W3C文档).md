# dom(W3C文档)

1. html dom定义了html元素的对象、属性和访问方法，将文档表达为树结构访问和操作。是html文档对象模型、编程接口（html元素被定义为对象，对象属性和方法是编程接口）
2. dom定义访问和更新html和xml文档内容、结构、样式的标准
3. W3C dom标准包括三部分：核心dom，针对任何结构化文档；针对xml和html的标准模型
4. 节点。整个文档、元素、元素属性、元素内容、注释，都可用js访问，进行增删改。它们关系：根、父子、同胞
5. 方法：在节点上执行的动作。常用：getElementById(id)/TagName()/ClassName()获取指定id的节点、getAttribute()/setAttritube()获取/设置属性；appendChild(node)/remove/replaceChild(node)插入删除子节点；createAttribute/Element和appendChild区别是啥/TextNode
6. 属性：获取或设置的节点值。常用innerHTML/parentNode/childNodes/attributes节点（元素）文本值/父节点/子节点/属性节点
   nodeName节点名称，元素/属性节点，文本/文档节点是#text/document;
   nodeValue：元素的节点值是null/undefined；属性和文本是其值；
   nodeType元素、属性、文本、注释、文档的nodeType值是1,2,3,8,9
7. 访问。getElementById(id)/TagName()/ClassName()类名在IE5678中无效
8. 修改，属性、样式：拿到节点.style.color/、事件；增删元素需要先创建好元素节点和内容节点。
9. dom内容，修改html内容。拿到节点.innerHtml
10. 元素增删改。父元素节点.appendChild(待添加节点)将新元素作为父元素的最后一个子元素添加；父元素节点.insertBefore(建好的节点，在哪个节点前插入)；删除元素要先找到父元素和待删子元素节点，然后parent.removeChild(child)或child.parentNode.removeChild(child);父元素节点.replaceChild(用来替换的新节点，被替换的旧节点)
11. 事件：元素有事情发生时，浏览器就生成事件，比如点击元素、加载页面、改变输入字段。onclick=事件函数名（节点名称/this）/this.innerHTML=。侦探昨晚讲了dom对象中可以用this指代，这边理解就清楚了
    我们可以用事件属性给元素分配事件，就是属性=“事件名”；用js向元素分配事件，是用js添加属性和属性值，属性值为函数/方法名，猜对~看一下例子就知道，我们都不一定需要在html元素属性里直接绑定事件名了，元素里有id或类，在js里我可以取到这个元素.事件名/innerHTML=方法()也行。不过好像还蛮麻烦的，直接在html元素里写事件名更省事，那啥时候用到属性给元素分配事件咧，只关注js的时候？
    具体事件：
    进入/离开页面：onload/onunload，可用作属性名，绑定检查访客浏览器类型和版本信息（据此加载相应版本网页）；处理cookies
    改变输入字段：onchange，我们常调用字符转换函数，用来验证输入字段内容
    鼠标指针移动/离开元素：onmouseover/onmouseout。小栗子不是很简单，蛮好玩
    鼠标点击全过程----鼠标点击、松开，完成点击：onmousedown/onmouseup/onclick。例子类似，看清楚它们有什么动作，难度降低很多。先页面，两个事件属性和盒子样式，事件方法的参数就是盒子所在页面，所以this即可；js里，属性做相应动作
12. 导航，使用节点关系在节点树中导航。可以获得节点列表的数组（getElementBy())；节点对象有length属性，可以用for循环把它们写入页面来循环输出它们
    三个节点属性就可以在文档结构中导航：首尾子元素和父节点
    根节点：document.documentElement/document.body这两是属性？不是节点嘛
    获取元素内容：innerHTML/childNodes[索引]nodeValue，了解一下可以用节点导航就好了
13. 总结。还有实例和参考可以看；服务器上也可以使用脚本实现网页动效，服务器端脚本有Php/asp/.net。dom实例超级多，针对不同对象实现不同效果，链接、文档、事件、鼠标、表单输入、框架、图像、定位、导航、下拉列表、屏幕、表格各部分、浏览器对象
14. 参考：js参考手册----js本地和内置对象；浏览器对象；文档对象
    js本地和内置对象：数字、字符串、布尔值、数组、日期、正则、数学、全局；高级教程里有对象定义、作用域、类型、应用、修改
    浏览器对象：window、导航、屏幕、历史记录、定位；
    文档对象：………………

大概6h