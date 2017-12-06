### Numbers

最近需要用到Numbers简单处理/展示一些小东西, 上手过程中几经波折. 怕以后忘记, 简单整理了下.

直观感受:
Numbers像是电子表格软件, 用表格/图表/文字共同来组织内容和排版, 在展现数据的同时呈现给我们一个优美的结果, 表格只是其中的主要组件.
Excel则是基于表格的数据分析软件, 到处皆'单元'的风格突出了其对数据的重视, 在数据分析手段和各种专业函数上被Numbers详细很多, 还有很多Numbers不具备的功能, 例如OLE对象/宏/外部数据/数据透视表等等.

日常生活中, Numbers就够用了. 内置的模板比较实用.
Numbers定位: 制作以数据展现为目的的报表和报告, 基于页面承载数据来进行数据分析, 作为清单和计划安排类的文稿来实用.

下面简要列出一些与Excel异同:

Excel -- "格子里的世界", 到处都是单元格  <br />
Numbers -- "能移动的表格", 表格作为一个对象放置在空白页面(风格上有点儿像Microsoft OneNote), 一个表单中可以有多个表格对象, 除了表格还可方便的插入图片/文本框/图表, 整个制作过程感觉像排版, 当移动或缩放对象时有智能辅助线作参考.

> 每个Numbers文件可包含多个表单, 每个表单相当于一页, 每页中可含多个表格和其他对象(图表/文本框/图像/媒体), 每个表格都有各自不同且唯一的名称.

> 单元格上的黄色控制点(上下或左右, 而非右下角)只能在正文或标题行列中进行横向或纵向复制, 不能跨越标题和正文列, 也不能同时复制行和列.

Numbers面对对象的格式化概念和Excel中面对选择区域格式化的概念是完全不同的, 也是从Excel转到Numbers时需要特别区分的地方.
边框设置过程中, 无法修改表格默认格线样式(粗细/颜色/样式), 更像是覆盖性的展现; 且设置边框时, 若对结果不满意, 需要先点击"还原"回到最初状态后, 再重新设置.
发现个展示小bug: 在表头中想用"\"分隔行列标题栏, 由于没有系统设置格式可供选择, 采用`Shape(形状)`中画线功能, 然后添加两个文本框, 调整各自位置和样式.
当滑动表单内容时, 如果采用默认的"冻结标题行"样式, 当标题行冻结时, 反向斜线和文本框随背景画布一块儿被滑出了屏幕. 另外, 当移动表单中上述表格, 表格位置改变后, 反向斜线和文本框仍保持在原有位置. 从原理上来讲, 斜线和文本框是跟表格'并列'的单独的对象(并列?), 而非表格的子对象, 这样方便呈现不同表格或其它媒体对象元素, 因而出现上述情况. 那么当我们需要添加相对于某表格的对象元素时, 如何保持与该表格相对关系, 也就是随着表格而相应改变? 不知是否有更好的处理方式, 还需多多学习 QAQ!

单元格中公式计算风格样式, Excel原始展现输入字符; Numbers将函数名/函数参数/括号等各区块设置不同的颜色和样式, 且单元格引用时会显示所对应行或列的标题栏名称.
例如: 如果是在同页的另一个表中引用C列的第4行显示会是`表格1::$C$4`, 如果是在其他表单中的公式调用会是`工作表1::表格1::$C$4`, 采用双冒号来依次分隔表单名称/表格名称/单元格, 内容范围上采用单个冒号来表示.
个人觉得不太方便的是, 当修改单元格内容时(含公式的单元格需要双击进入编辑模式, 也可用`option+return`快捷键), 只能在对应单元格处理, 而无法在底部的显示行修改(Excel则可以在顶部的编辑行中修改).

可以将Numbers整个表单内容直接复制粘贴到Pages中, 内容和公式都会被完整的保留下来, 样式有时稍有调整. 这种将表格作为对象来使用的特性，使得iWork套件相互间更加兼容. 且能方便保存到iCloud, 在各设备上浏览/编辑.

Numbers"协作"功能, 由于没有多人合作过, 不清楚具体细则. 不知是否跟GIT类似.

关于计算公式, 很多时候会使用逻辑函数`IF`来处理例外和异常, 然而加入了逻辑判断后，会使公式变得很长而且也容易出错.
针对内容的`条件高亮显示`很多时候可以起到同样的判断作用, 且设置更简单, 通过添加规则用颜色/填充/加粗等醒目的方式进行区分.
条件高亮规则分数字/文本/日期/持续时间/空白等几个类别, 每一类规则中都包含了固定的一些判断条件, 不能自行设置包含运算和函数的判断.
通过添加规则我们可以直观地对一些单独数据进行醒目展示, 以作为数据分拣时的辅助手段来使用.

在Numbers的使用逻辑中, 每个表单可以理解成一个没有大小限制的承载表格和图表等对象的页, 只有在打印输出时才会和实际的纸张大小进行大小的适配, 在表单中排布元素和对象时可以基于所见即所得的方式来排版和设置字体的大小, 如果是计划输出打印的表单页可以添加标尺来划定内容排布的范围.


---

prefers  <br />
[Numbers 函数列表](https://www.apple.com/cn/mac/numbers/compatibility/functions.html)  <br />
[Numbers 公式与函数帮助](http://help.apple.com/functions/mac/5.0/#/ffaef5aeec8)

reference to  <br />
[Numbers 使用技巧](https://www.zhihu.com/topic/19620969/hot)
[Numbers](http://www.jianshu.com/p/2bc7c210b7d9)  <br />
[使用numbers怎么制作下图这样的单元格内的斜线呢?](http://bbs.feng.com/read-htm-tid-7693040.html)