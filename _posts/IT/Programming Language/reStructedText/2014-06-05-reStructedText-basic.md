# reStructedText

reStructedText属于轻量级的 **标记语言** ，标记语言创建了丰富多彩的Web世界，但HTML与XML等语言并不易读，对机器友好而非对人友好。轻量级标记语言则不同，这些语言 *对人友好* ，同时 *语法简单* ，没有古怪的标签：

    1. 可以使用最简单的文本编辑器；

    1. 所见即所得，WYSIWTG；

    1. 可版本控制；

    1. 可以实现单一源文件出版；

最为著名的几种轻量级标记语言有：

    1. Markdown(Github常用)

    1. reStructedText(Python文档使用)

    1. Textile(Ruby使用)

    1. AsciiDoc

    1. Org-mode(Emacs)

这篇basic主要记录reStructedText的学习过程，其他应该大同小异。

## 题目和章节

    =================
    一级题目
    =================

    以后依次是“-”，“～”，“^”，“+”，“`”

## 标题

    一级标题
    ==================

    以下依次是“-”，“～”，“^”，“+”，“`”

## 段落

1. 段落使用空行分隔，仅一个换行不分段，续上段。使用\\在行尾可以使续行与原行尾不留白

1. "| "可以用来保持换行符，下一行行不续行

    | this line，
    | new line.

1. 段落缩进，WYSIWYG，直接缩进就好

## 代码块

1. 双冒号缩进为代码

    printf "Hello, reStructedText!\n"

1. 还可以声明语言类型

    .. code-block:: c 
    
        printf("%s\n", "Hello, reStructedText!");

## 无序列表

1. 星号，减号，加号可以开始无序列表

1. 列表层级和缩进有关

1. 和具体符号无关
   
   * level 1
     
   * level 1
      
        * level 2

            * level 3

   * level 1

## 有序列表

1. 数字和点开始编号

1. 大小写字母和点

   A. test

   B. test2

        a. test3

        b. test4

1. 在括号里的大小写罗马字母

   (I) test1

   (II) test2

        i) test3

        ii) test4

## 列表续行、段落和代码块

1. 列表可以折行，折行后对齐自动续行

1. 列表项目可以包含段落，空行开始新段落，新段落要与列表项对齐

   example

1. 列表项目可以包含代码段

   $ printf "hello, reStructedText"

## 定义

reStructedText
    simple and beautiful.

## 分割线

四个减号或以上显示为分割线

-----

上面是分割线

## 字体

1. 这是 **粗体** , 这是 *斜体* , 这是\ **去掉空格的粗体**\ ,这是\ *去掉空格的斜体*\ 。

1. 这是 :del:`删除线` 效果 ???

1. 这是 :ul:`下划线` 效果 ???

1. 这是 文字\ :sub:`下标` , 这是 文字\ :sup:`上标` 。

1. 这是 ``等宽字体`` ， ``'123, kiss me~'`` 

1. 引言

   `地球绕太阳转。` ——哥白尼

# 链接

1. URL自动链接，例如：http://www.baidu.com

1. 文字链接

   i) 访问 `百度 <http://www.baidu.com>`

   ii) 直接引用已定义过的 百度\_ 链接 

   iii) 链接地址在后面定义，如 `GitHub`\_ 。

1. 内部跳转

   \.. anchor: 定义了一个锚，点击 anchor\_ 跳转到文章第一段。

   或点击 `这里 <#anchor>`\_ 跳转到文章第一段

1. 脚注

   i) 脚注可以手动用#自动分配数字 \[#]\_ , 例如 \[#]\_

   ii) 自动分配脚注也可以作为标签多次引用 \[#label]\_

   iii) `可以用星号做脚注 [*]_ , 这样 [*]_ ，以及这样 [*]_`

   iv ) 单词也可以做脚注 \[EI-1834]\_

# 图片

1. 规定大小的、位置的图片

   .. figure:: pic/girl.jpg
    :width: 150
    :align: center

1. 图片链接 |girllink|\_

## 表格

1. 示例：

   .. table:: 表格标题
        :class: classic

        +--------+---------+--------+
        | head1  |  head2  | head3  |
        +========+=========+========+
        |        |  cell   | cell   |
        | row-   +---------+--------+
        | span   |  * item1         |
        |        |  * item2         |
        +--------+---------+--------+


## 注释

“.. ”后的内容为注释, “.. ”必须在行首，如：

.. comment



-------



.. \_girllink: http://www.baidu.com

.. |girllink| image:: pic/girl.jpg
                :width: 100

.. \_GitHub: http://github.com

.. \[#] 井号自动编号

.. \[#] 井号自动编号1

.. \[#label] label编号

上帝，原谅我拿markdown写曾经的reStructedText说明。我已经了解了reStructedText文档，只是同步下而已，效果真烂。
