# PHP学习笔记

 

什么是PHP：

 

PHP（“超文本预处理器”）是一种通用开源脚本语言。语法吸收了C语言、Java和Perl的特点，利于学习，使用广泛，主要适用于Web开发领域。PHP 独特的语法混合了C、Java、Perl以及PHP自创的语法。它可以更快速地执行动态网页。

 

我所下载软件;

 

\1.  Phpstudy2018(环境集成软件);

 

下载地址：http://www.121down.com/soft/softview-104163.html

 

\2.  Sublime(开发工具)

 

下载地址：http://www.sublimetext.com/3

 

下载环境集成软件也可以选择:1.wampserver; 2.xmapp 3.appserver。

 

下载开发工具也可以选择：vim notepad++ phpstrom NetBeans等等。

 

我们在写php代码时要统统写在WWW目录下。例如我的是在D:\phpStudy\PHPTutorial\WWW，在安装phpstudy时尽量安装在D盘。因为c盘是系统盘，重装系统后可能就会没了。

 

## 软件编码不会自动保存的解决方案

 

第一次使用sublime编写php文件时，想输出hello world，但在我写代码，打开127.0.0.1时却是一片空白。

 

​                   [![1603020383468](https://github.com/al1623232873/PicGO/raw/master/img/1603020383468.png)](https://github.com/al1623232873/PicGO/blob/master/img/1603020383468.png)

 

[![160020407731](https://github.com/al1623232873/PicGO/raw/master/img/1603020407731.png)](https://github.com/al1623232873/PicGO/blob/master/img/1603020407731.png)

 

于是我开始不断百度，但我发现我这个问题好像很罕见，根本搜索不到类似的问题，全是关于127.0.0.1无法打开之类的问题，而我是可以正常打开，环境也没有问题。如果是编码出了问题应该是会报错，而不是一片空白。

 

[![1603020475067](https://github.com/al1623232873/PicGO/raw/master/img/1603020475067.png)](https://github.com/al1623232873/PicGO/blob/master/img/1603020475067.png)

 

于是乎我将开发工具换成了Notepad++，再进行编码，但结果依旧如此。

 

[![1603020490636](https://github.com/al1623232873/PicGO/raw/master/img/1603020490636.png)](https://github.com/al1623232873/PicGO/blob/master/img/1603020490636.png)

 

[![1603020503540](https://github.com/al1623232873/PicGO/raw/master/img/1603020503540.png)](https://github.com/al1623232873/PicGO/blob/master/img/1603020503540.png)

 

后来我打算关闭Notepad++软件时，我对它进行保存，毕竟不能白打，而我再打开127.0.0.1时神奇的一幕发生了，上面终于出现了我期待很久的hello world。原来我这个编码完成后是需要进行保存才行。保存快捷键是：Ctrl+s。

 

[![1603020535034](https://github.com/al1623232873/PicGO/raw/master/img/1603020535034.png)](https://github.com/al1623232873/PicGO/blob/master/img/1603020535034.png)

 

而每次编完码之后都要保存就很麻烦，而sublime是可以自动保存的，设置步骤如下：

 

一、打开sublime编辑器，按快捷键Ctrl+Shift+p调出命令面板，或者在工具栏中点击：工具>命令面板；

 

[![1603020547478](https://github.com/al1623232873/PicGO/raw/master/img/1603020547478.png)](https://github.com/al1623232873/PicGO/blob/master/img/1603020547478.png)

 

二、搜索框中输入 P 找到Preferences:Settings 选项，单击；

 

[![1603020552228](https://github.com/al1623232873/PicGO/raw/master/img/1603020552228.png)](https://github.com/al1623232873/PicGO/blob/master/img/1603020552228.png)

 

三、进入这个页面；

 

[![1603020559597](https://github.com/al1623232873/PicGO/raw/master/img/1603020559597.png)](https://github.com/al1623232873/PicGO/blob/master/img/1603020559597.png)

 

四、在Preferences:Settings - User下面添加一行代码"save_on_focus_lost": true，然后按ctrl+s保存后退出即可。

 

[![1603020565142](https://github.com/al1623232873/PicGO/raw/master/img/1603020565142.png)](https://github.com/al1623232873/PicGO/blob/master/img/1603020565142.png)

 

## Php有四种标记风格：

 

\1.   XML风格。

  \2.   短标签风格  

\3.   ASP风格

 

<%

 

你写的代码

 

%>

 

\4.   JavaScript风格

 <script languange="php">   你写的代码  </script> 

## 变量

 

变量：$ 符号开始，后面跟着变量的名称.。

 

\1.   变量名称必须以字母为开头；

 

\2.   构成变量名的字符（A-z、0-9 和 _ ）；

 

\3.   php是一种弱类型的语言所以可以无需声明变量直接使用，也无需声明变量类型。

 

[![1603020579859](https://github.com/al1623232873/PicGO/raw/master/img/1603020579859.png)](https://github.com/al1623232873/PicGO/blob/master/img/1603020579859.png)

 

定义变量等于什么时，如果是数字不用加””,但如果是英文字母是则要加””。

 

全局变量，在函数内调用全局变量需要global关键字，也可以使用参数作用域调用全局变量。

 

## 系统常量(魔术常量)

 

| ID   | 常量         | 注释                                           |
| ---- | ------------ | ---------------------------------------------- |
| 1    | **FILE**     | 当前文件路径                                   |
| 2    | **DIR**      | 当前文件目录                                   |
| 3    | **LINE**     | 在文件文件的那一行                             |
| 4    | **FUNCTION** | 在当前文件的那个函数中 返回 函数名             |
| 5    | **CLASS**    | 在当前文件中的那个类中 返回 类名               |
| 6    | **METHOD**   | 在当前文件的类中的那个方法中 返回 类名::方法名 |

 

## 5种基本输出

 

\1.   echo  只能打印字符串；

 

\2.   print_r 能够打印数组和字符串；

 

\3.   var_dump 能够打印数组和字符串同时输出打印内容的数据型

 

\4.   var_export 能够将字符串转换为php代码，第二个参数设置为true能够返 回值

 

\5.   die 结束程序并打印内容

 

## 作用域

 

参数作用域可以不用global就可以调用全局变量，static作用域是可以让变量在函数运行后不被销毁。

 

## 分支语句

 

if语句和switch语句