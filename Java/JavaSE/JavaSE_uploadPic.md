**Java学习笔记**

# 第1章 Java语言概述

**Java基础知识图解**

![java基础知识图解](http://101.34.218.64/JavaSE.assets/java%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86%E5%9B%BE%E8%A7%A3.png)

第一部分：编程语言核心结构（前三章）
主要知识点：变量、基本语法、分支、循环、数组、…
第二部分：Java面向对象的核心逻辑(4-6章)
主要知识点：OOP、封装、继承、多态、接口、…
第三部分：开发Java SE高级应用程序
主要知识点：异常、集合、I/O、多线程、反射机制、网络编程、……
第四部分：实训项目
项目一：家庭收支记账软件
项目二：客户信息管理软件
项目三：开发团队人员调度软件
附加项目一：银行业务管理软件
附件项目二：单机考试管理软件

**Java基础课程体系**
第1章 Java语言概述
第2章 基本语法
第3章 数组
第4章 面向对象编程(上)
第5章 面向对象编程(中)
第6章 面向对象编程(下)
第7章 异常处理
第8章 枚举类&注解
第9章 Java集合
第10章 泛型
第11章 IO流
第12章 多线程
第13章 Java常用类
第14章 Java反射机制
第15章 网络编程
第16章 Lambda表达式与Stream API
第17章 Java 9 & 10 & 11新特性



## 1-1 软件开发介绍

**软件开发**
软件，即一系列按照特定顺序组织的计算机数据和指令的集合。有系统软件和应用软件之分。

应用程序 = 算法 + 数据结构

**人机交互方式**：图形化界面、命令行方式

**常用的DOS命令**
dir :列出当前目录下的文件以及文件夹
md :创建目录
rd :删除目录
cd :进入指定目录
cd.. : 退回到上一级目录
cd\:退回到根目录
del :删除文件
exit : 退出 dos 命令行
补充：echo javase>1.doc

## 1-2 计算机编程语言介绍

计算机语言有很多种。如：C ,C++ ,Java ,PHP , Kotlin，Python，Scala等。

第一代语言：机器语言 二进制

第二代语言：汇编语言 助记符

![汇编示意图](http://101.34.218.64/JavaSE.assets/%E6%B1%87%E7%BC%96%E7%A4%BA%E6%84%8F%E5%9B%BE.jpg)

第三代语言：高级语言

​	C、Pascal、Fortran面向过程

​	C++面向过程、面向对象

​	Java跨平台的纯面向对象的语言

​	.Net跨语言平台

​	Python、Scala...



## 1-3 Java语言概述

SUN(Stanford University Network，斯坦福大学网络公司 ) 1995年推出的一门高级编程语言

是一种面向Internet的编程语言。Java一开始富有吸引力是因为Java程序可以在Web浏览器中运行。这些Java程序被称为Java小程序（applet）。applet使用现代的图形用户界面与Web用户进行交互。applet内嵌在HTML代码中。
随着Java技术在web方面的不断成熟，已经成为Web应用程序的首选开发语言
后台开发：Java、PHP、Python、Go、Node.js



**java简史**

```
Java语言版本迭代概述
1991年 Green项目，开发语言最初命名为Oak (橡树)
1994年，开发组意识到Oak 非常适合于互联网
1996年，发布JDK 1.0，约8.3万个网页应用Java技术来制作
1997年，发布JDK 1.1，JavaOne会议召开，创当时全球同类会议规模之最
1998年，发布JDK 1.2，同年发布企业平台J2EE
1999年，Java分成J2SE、J2EE和J2ME，JSP/Servlet技术诞生
2004年，发布里程碑式版本：JDK 1.5，为突出此版本的重要性，更名为JDK 5.0
2005年，J2SE -> JavaSE，J2EE -> JavaEE，J2ME -> JavaME
2009年，Oracle公司收购SUN，交易价格74亿美元
2011年，发布JDK 7.0
2014年，发布JDK 8.0，是继JDK 5.0以来变化最大的版本
2017年，发布JDK 9.0，最大限度实现模块化
2018年3月，发布JDK 10.0，版本号也称为18.3
2018年9月，发布JDK 11.0，版本号也称为18.9
```

**Java技术体系平台**

| Java SE(Java Standard Edition)标准版   | 支持面向桌面级应用（如Windows下的应用程序）的Java平台，提供了完整的Java核心API，此版本以前称为J2SE |
| -------------------------------------- | ------------------------------------------------------------ |
| Java EE(Java Enterprise Edition)企业版 | 是为开发企业环境下的应用程序提供的一套解决方案。该技术体系中包含的技术如:Servlet 、Jsp等，主要针对于Web应用程序开发。版本以前称为J2EE |
| Java ME(Java Micro Edition)小型版      | 支持Java程序运行在移动终端（手机、PDA）上的平台，对Java API有所精简，并加入了针对移动终端的支持，此版本以前称为J2ME |
| Java Card                              | 支持一些Java小程序（Applets）运行在小内存设备（如智能卡）上的平台 |

**Java的应用**
Java Web开发：后台开发
大数据开发：数据挖掘
Android应用程序开发：客户端开发

**Java的诞生**

Java之父James Gosling

Java确实是从C语言和C++语言继承了许多成份，甚至可以将Java看成是类C语言发展和衍生的产物。比如Java语言的变量声明，操作符形式，参数传递，流程控制等方面和C语言、C++语言完全相同。但同时，Java是一个**纯粹的面向对象**的程序设计语言，它继承了C++语言面向对象技术的核心。Java**舍弃了C语言中容易引起错误的指针（以引用取代）、运算符重载（operator overloading）、多重继承（以接口取代）**等特性，**增加了垃圾回收器**功能用于回收不再被引用的对象所占据的内存空间。JDK1.5又引入了**泛型编程**（Generic Programming）、类型安全的枚举、不定长参数和自动装/拆箱

**Java语言的特点**

Java 语言有哪些特点?
①简单易学；
②面向对象（封装，继承，多态）；
两个基本概念：类、对象。三大特征：封装，继承，多态。
Java语言提供类、接口和继承等原语，为了简单起见，只支持类之间的单继承，但支持接口之间的多继承，并支持类与接口之间的实现机制（关键字为implements）。
③跨平台性/平台无关性（ Java 虚拟机实现平台无关性）；
通过Java语言编写的应用程序在不同的系统平台上都可以运行。“Write once , Run Anywhere”
原理：只要在需要运行 java 应用程序的操作系统上，先安装一个Java虚拟机 (JVM Java Virtual Machine) 即可。由JVM来负责Java程序在该系统中的运行。
④支持多线程（ C++ 语言没有内置的多线程机制，因此必须调用操作系统的多线程功能来进行多线程程序设计，而 Java 语言却提供了多线程支持）；
⑤可靠性；
吸收了C/C++语言的优点，但去掉了其影响程序健壮性的部分（如指针、内存的申请与
释放等），提供了一个相对安全的内存管理和访问机制
⑥安全性；
⑦支持网络编程并且很方便（ Java 语言诞生本身就是为简化网络编程设计的，因此 Java 语言不仅支持网络编程而且很方便）；
⑧编译与解释并存；

## 1-4 Java程序运行机制及运行过程

**Java两种核心机制**
 ①Java虚拟机 (Java Virtal Machine):
​JVM是一个虚拟的计算机，具有指令集并使用不同的存储区域。负责执行指令，管理数据、内存、寄存器。Java虚拟机机制屏蔽了底层运行平台的差别，实现了“一次编译，到处运行”
字节码并不针对一种特定的机器，因此，Java 程序无须重新编译便可在多种不同操作系统的计算机上运行。
.java源代码—编译—>.class字节码—执行—>JVM
![jvm的位置](http://101.34.218.64/JavaSE.assets/JVM%E7%9A%84%E4%BD%8D%E7%BD%AE.png)

 ②垃圾收集机制 (Garbage Collection)
   不再使用的内存空间应回收—— 垃圾回收
  在C/C++等语言中，由程序员负责回收无用内存
  Java 语言消除了程序员回收无用内存空间的责任：它提供一种系统级线程跟踪存储空间的分配情况。并在JVM空闲时，检查并释放那些可被释放的存储空间。
  垃圾回收在Java程序运行过程中自动进行，程序员无法精确控制和干预

注意：Java程序仍然会出现内存泄漏和内存溢出问题

## **1-5 Java语言的环境搭建**

**JDK、JRE、JVM的关系**

JDK(Java Development Kit Java开发工具包):JDK是提供给Java开发人员使用的，其中包含了java的开发工具，也包括了JRE。所以安装了JDK，就不用在单独安装JRE了。其中的开发工具：编译工具(javac.exe) 打包工具(jar.exe)等

JRE(Java Runtime Environment Java运行环境):包括Java虚拟机(JVM Java Virtual Machine)和Java程序所需的核心类库等，如果想要**运行**一个开发好的Java程序，计算机中只需要安装JRE即可。

![JVM、JRE、JDK的关系](http://101.34.218.64/JavaSE.assets/JVM%E3%80%81JRE%E3%80%81JDK%E7%9A%84%E5%85%B3%E7%B3%BB.png)

JDK=jRE+开发工具
JRE=JVM+JavaSE标准类库

![jdk示意.png](http://101.34.218.64/JavaSE.assets/jdk%E7%A4%BA%E6%84%8F.png)

官方网址
www.oracle.com
java.sun.com

jdk8下载
https://download.oracle.com/otn-pub/java/jdk/8u321-b07/df5ad55fdd604472a86a45a217032c7d/jdk-8u321-windows-x64.exe

1.安装JDK，路径不能有中文
安装路径不要有中文或者空格等特殊符号。
	如果操作系统是64位的，软件尽量选择支持64位的（除非软件本身不区分）。
	当提示安装 JRE 时，正常在JDK安装时已经装过了，但是为了后续使用Eclipse等开发工具不报错，建议也根据提示安装JRE。

2.配置环境变量
![配置环境变量](http://101.34.218.64/JavaSE.assets/%E9%85%8D%E7%BD%AE%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F.png)
①新建环境变量JAVA_HOME
```
JAVA_HOME=D:\Java\jdk1.8.0_321
```
②编辑环境变量Path
```
%JAVA_HOME%\bin
```
移动到最前面，会优先在此环境里找java
​win7是写在一行 后面要加冒号；


不要配置CLASSPATH!不要配置CLASSPATH!不要配置CLASSPATH!那是告诉系统字节码文件在哪的 不需要配置



3.测试验证
javac 
java 

## 1-6 HelloWorld

步骤：
1.将 Java 代码编写到扩展名为 .java 的文件中。
2.通过 javac 命令对该 java 文件进行**编译**。
3.通过 java 命令对生成的 class 文件进行**运行**。

![配置环境变量](http://101.34.218.64/JavaSE.assets/%E7%BC%96%E8%AF%91%E5%92%8C%E8%BF%90%E8%A1%8C.png)

HelloWorld.java文件内容

```java
class HelloChina{
    public static void main(String[] args){
        System.out.println("Hello,World!");
    }
}
```

![编译和运行命令](http://101.34.218.64/JavaSE.assets/%E7%BC%96%E8%AF%91%E5%92%8C%E8%BF%90%E8%A1%8C%E5%91%BD%E4%BB%A4.png)
```
javac xxx.java  
java 类名  		//注意是类名不是文件名，不要带”.class“
```
//windows下文件名不区分大小写，javac后面可以大写可以小写；但是java要区分，所以类名要严格按照大小写来写

//在包下的类，在Java源文件的地方编译后，需要到最外层包的上一级目录下运行，而且类前面需要带包名，以.隔开

①一个java源文件中可以声明多个class。但必须与源文件名是最多有一个类声明为public。而且要求声明为public的类的类名与源文件名相同。

②程序的入口是main()方法，格式是固定的。

里面的参数可以是`String[] args` （习惯上这样写）或`String args[]`或`String a[]`等

③输出语句

`System.out.print();//只输出`

`System.out.println();//先输出再换行`

④Java语言严格区分大小写



## 1-7 注释（Comment）

①单行注释 `//注释文字`
②多行注释 `/* 注释文字 */`
注：
 对于单行和多行注释，被注释的文字，**不会被JVM（java虚拟机）解释执行**。
 多行注释里面**不允许有多行注释嵌套**

③文档注释（java特有）

```java
/**
@author 指定java程序的作者
@bersion 指定源文件的版本
*/

比如
import java.util.Scanner;
/**
 * @author LoongKK
 * @version 1.0
 * 哈哈哈哈
 * 嘻嘻嘻
 嘿嘿
 */
public class HelloWorld {
    /**
     * 这是main方法
     * @param args
     */
    public static void main(String[] args){

        System.out.println("Hello,World!");
    }
}
```

注释内容可以被JDK提供的工具 javadoc 所解析，生成一套以网页文件形式体现的该程序的说明文档。

`javadoc -d myhello -author -version HelloWorld.java`

生成一个文件夹 里面首页文件index.html


## 1-9 其他

**Java API文档**

API: application programming interface
API文档：api说明书。1.6的有官方中文，后面的只有英文了。http://download.java.net/jdk/jdk-api-localizations/jdk-api-zh-cn/publish/1.6.0/chm/JDK_API_1_6_zh_CN.CHM

**编程风格**

正确的注释和注释风格
* 使用文档注释来注释整个类或整个方法。
* 如果注释方法中的某一个步骤，使用单行或多行注释。
正确的缩进和空白
* 使用一次tab操作，实现缩进
* 运算符两边习惯性各加一个空格。比如：2 + 4 * 5。
块的风格
* Java API 源代码选择了行尾风格

行尾风格

```java
public class Test {
	public static void main(String[] args){
	System.out.println("Block Style!");
	}
}
```

次行风格

```java
public class Test
{
	public static void main(String[] args)
	{
	System.out.println("Block Style!");
	}
}
```

**常见开发工具**

常见的IDE(Integrated Development Environment 集成开发环境)：
Eclipse—— IBM公司  免费
MyEclipse——Genuitec公司 收费版、免费版
Intellij IDEA——JetBrains  收费版 、社区版



# 第2章 基本语法

## 2-1 关键字和保留字

### **关键字（keyword）**

定义：被java语言赋予特殊含义，用做专门用途的字符串（单词）
特点：关键字中所有字母都为小写

https://docs.oracle.com/javase/tutorial/java/nutsandbolts/_keywords.html

![关键字](http://101.34.218.64/JavaSE.assets/%E5%85%B3%E9%94%AE%E5%AD%97.JPG)
![关键字2](http://101.34.218.64/JavaSE.assets/%E5%85%B3%E9%94%AE%E5%AD%972.png)

### **保留字(reserved word)**

Java保留字：现有Java版本尚未使用，但以后版本可能会作为关键字使
用。自己命名标识符时要避免使用这些保留字
goto 、const

## 2-2 标识符(==重点学习==)

Java 对各种变量、方法和类等要素命名时使用的字符序列称为标识符（Identifier）
技巧：**凡是自己可以起名字的地方都叫标识符。**

### **定义合法标识符的规则**

①由26个英文字母大小写，0-9 ，_或 $ 组成
②数字不可以开头。
③不可以使用关键字和保留字，但能包含关键字和保留字。
④Java中严格区分大小写，长度无限制。
⑤标识符不能包含空格。

### **Java中的名称命名规范**

* 包名：多单词组成时所有字母都小写：xxxyyyzzz
* 类名、接口名：多单词组成时，所有单词的首字母大写：XxxYyyZzz（大驼峰）
* 变量名、方法名：多单词组成时，第一个单词首字母小写，第二个单词开始每个单词首字母大写：xxxYyyZzz（小驼峰）
* 常量名：所有字母都大写。多单词时每个单词用下划线连接：XXX_YYY_ZZZ

 注意1：在起名字时，为了提高阅读性，要尽量有意义，“**见名知意**”。
 注意2：java采用unicode字符集，因此**标识符也可以使用汉字**声明，但是不建议使用。

> 总结自《代码简洁之道》
>
> 整理人：宋红康
>
> 第2章 有意义的命名
> 2.1 介绍
> 软件中随处可见命名。我们给变量、函数、参数、类和包命名。我们给源代码及源代码所在目录命名。
> 这么多命名要做，不妨做好它。下文列出了取个好名字的几条简单规则。
>
> 2.2 名副其实,见名知意
>      变量名太随意，haha、list1、ok、theList 这些都没啥意义
>
> 2.3 避免误导
>      包含List、import、java等类名、关键字或特殊字；
>      字母o与数字0，字母l与数字1等
>      提防使用不同之处较小的名称。比如：XYZControllerForEfficientHandlingOfStrings与XYZControllerForEfficientStorageOfStrings
>
> 2.4 做有意义的区分
>      反面教材，变量名：a1、a2、a3
>      避免冗余，不要出现Variable、表字段中避免出现table、字符串避免出现nameString，直接name就行，知道是字符串类型
>      再比如：定义了两个类：Customer类和CustomerObject类，如何区分？
> 	     定义了三个方法：getActiveAccount()、getActiveAccounts()、getActiveAccountInfo()，如何区分？
>
> 2.5 使用读得出来的名称
>      不要使用自己拼凑出来的单词，比如：xsxm(学生姓名)；genymdhms(生成日期，年、月、日、时、分、秒)
>      所谓的驼峰命名法，尽量使用完整的单词
>
> 2.6 使用可搜索的名称
>      一些常量，最好不直接使用数字，而指定一个变量名，这个变量名可以便于搜索到.
>      比如：找MAX_CLASSES_PER_STUDENT很容易，但想找数字7就麻烦了。
>
> 2.7 避免使用编码
>      2.7.1 匈牙利语标记法
>            即变量名表明该变量数据类型的小写字母开始。例如，szCmdLine的前缀sz表示“以零结束的字符串”。
>      2.7.2 成员前缀
>           避免使用前缀，但是Android中一个比较好的喜欢用m表示私有等，个人感觉比较好
>      2.7.3 接口和实现
>           作者不喜欢把接口使用I来开头，实现也希望只是在后面添加Imp
>
> 2.8 避免思维映射
>      比如传统上惯用单字母名称做循环计数器。所以就不要给一些非计数器的变量命名为：i、j、k等
>
> 2.9  类名
>      类名与对象名应该是名词与名词短语。如Customer、WikiPage、Account和AddressParser。避免使用Data或Info这样的类名。
>      不能使动词。比如：Manage、Process
>
> 2.10 方法名
>      方法名应当是动词或者动词短语。如postPayment、deletePage或save
>
> 2.11 别扮可爱
>      有的变量名叫haha、banana
>      别用eatMyShorts()表示abort()
>
> 2.12 每个概念对应一个词
>      项目中同时出现controllers与managers，为什么不统一使用其中一种？
>      对于那些会用到你代码的程序员，一以贯之的命名法简直就是天降福音。
>
> 2.13 别用双关语
>      有时可能使用add并不合适，比例insert、append。add表示完整的新添加的含义。     
>
> 2.14 使用解决方案领域名称
>      看代码的都是程序员，所以尽量用那些计算机科学术语、算法名、模式名、数学术语，
>      依据问题所涉领域来命名不算是聪明的做法。
>
> 2.15 使用源自所涉问题领域的名称
>      如果不能用程序员熟悉的术语来给手头的工作命名，就采用从所涉问题领域而来的名称吧。
>      至少，负责维护代码的程序员就能去请教领域专家了。
>
> 2.16 添加有意义的语境
>      可以把相关的变量放到一个类中，使用这个类来表明语境。
>
> 2.17 不要添加没用的语境
>      名字中带有项目的缩写，这样完全没有必要。比如有一个名为“加油站豪华版”（Gas Station Deluxe）的项目，
>      在其中给每个类添加GSD前缀就不是什么好策略。
>
> 2.18 最后的话
>      取好名字最难的地方在于需要良好的描述技巧和共有文化背景。

## 2-3 变量

**使用变量注意**：
* Java中每个变量必须先声明，后使用
* 使用变量名来访问这块区域的数据
* 变量的作用域：其定义所在的一对{ }内
* 变量只有在其作用域内才有效
* 同一个作用域内，不能定义重名的变量

**变量的声明和赋值**：

声明变量：<数据类型> <变量名>  如int var;
变量的赋值：<变量名> = <值>
声明同时赋值：<数据类型> <变量名>  = <值>

### **基本数据类型**

![基本数据类型](http://101.34.218.64/JavaSE.assets/%E5%9F%BA%E6%9C%AC%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B.jpg)

变量按声明位置分成员变量和局部变量：
成员变量：方法体外，类体内声明的变量
局部变量：方法体内部声明的变量
![成员变量和局部变量](http://101.34.218.64/JavaSE.assets/%E6%88%90%E5%91%98%E5%8F%98%E9%87%8F%E5%92%8C%E5%B1%80%E9%83%A8%E5%8F%98%E9%87%8F.jpg)



**整型**

Java各整数类型有固定的表数范围和字段长度，不受具体OS的影响，以保证java程序的可移植性。
java的整型常量默认为 int 型，**声明long型常量须后加‘l’或‘L’**
java程序中变量通常声明为int型，除非不足以表示较大的数，才使用long

![](http://101.34.218.64/JavaSE.assets/%E6%95%B4%E5%9E%8B.JPG)

**浮点型：float和double**

![](http://101.34.218.64/JavaSE.assets/%E6%B5%AE%E7%82%B9%E5%9E%8B.png)

Java 的浮点型常量默认为double型，声明float型常量，须后加‘f’或‘F’。
float也和int都是4字节，但是表示范围逼long还大，以为是浮点数形式存储（指数
Java中还允许使用转义字符‘\’来将其后的字符转变为特殊字符型常量。char c1='\n'
直接使用 Unicode 值来表示字符型常量：‘\uXXXX’(xxxx是十六进制数)。如`\u000a`表示`\n`



**字符类型char**

char 2个字节
Java中的所有字符都使用Unicode编码，故一个字符可以存储一个字母，一个汉字，或其他书面语的一个字符。
字符常量是用单引号(' ')括起来的单个字符。char c1='a';char c2='中'；char c3='9'；



**布尔类型：boolean**

用于if条件控制或者循环控制
取两个值true、flase
java中**不可以**使用0或非零整数代替false和true
Java虚拟机中没有任何供boolean值专用的字节码指令，Java语言表达所操作的boolean值，在编译之后都使用java虚拟机中的int数据类型来代替：true用1表示，false用0表示。———《java虚拟机规范 8版》

### **基本数据类型变量间转换**

* 除boolean之外的其他7种基本数据类型，boolean类型不能与其它基本数据类型运算。

* **自动类型转换**(只涉及7种基本数据类型）：容量(表示数的范围)小的类型自动转换为容量大的数据类型。
==**byte 、char 、short --> int --> long --> float --> double**==

有多种类型的数据混合运算时，系统首先自动将所有数据转换成容量最大的那种数据类型，然后再进行计算。
byte,short,char之间不会相互转换，他们三者在计算时首先转换为int类型。

* **强制类型转换**(只涉及7种基本数据类型，boolean类型不可以转换为其它的数据类型）：自动类型提升运算的逆运算。需要使用强转符：`()`  
例`double a=1.2;int b=(int)a`

注意： 强制类型转换，可能导致精度降低或溢出。

* 通常，字符串不能直接转换为基本类型，但通过基本类型对应的包装类则可以实现把字符串转换成基本类型。如： `String a = "43"; int i = Integer.parseInt(a);`



### **基本数据类型与String间转换**

字符串类型：String
String不是基本数据类型，属于引用数据类型。
使用方式与基本数据类型一致。例如：`String str = "abcd";`（使用一对 `""`）
一个字符串可以串接另一个字符串，也可以直接串接其他类型的数据。
**当把任何基本数据类型(8种，包括boolean型)的值和字符串(String)进行连接运算时(+)，基本数据类型的值将自动转化为字符串(String)类型。**

```java
char c='a';
int num=10;
String str="hello";
System.out.println(c+num+str);//107hello
System.out.println(c+str+num);//ahello10
System.out.println(c+(num+str));//a10hello
System.out.println(str+num+c);//hello10a
```

### **进制与进制间的转换(了解)**

 所有数字在计算机底层都以二进制形式存在。
对于整数，有四种表示方式：
* 二进制(binary)：0,1 ，满2进1.以**0b或0B**开头。
* 十进制(decimal)：0-9 ，满10进1。
* 八进制(octal)：0-7 ，满8进1. 以数字**0**开头表示。
* 十六进制(hex)：0-9及A-F，满16进1. 以**0x或0X**开头表示。此处的A-F不区分大小写。
如：0x21AF +1= 0X21B0



**二进制 ：原码、反码、补码**

正数：三码合一

负数：
负数的原码：直接将一个数值换成二进制数。最高位是符号位(符号位正0负1，负数为1)。
负数的反码：其原码符号位不变，按位取反
负数的补码：其反码加1。

二进制数据的存储方式：所有的数值，不管正负，底层都以==补码==的方式存储。

**进制间的转换：**

二转十：具体按原码、反码、补码来做转化。乘以2的幂数
十转二：除2取余的逆。（直到商的整数部分为零停止)
二转八：3位一组
二转十六：4位一组



开发中的进制转换：

Integer class
static String toBinaryString(int i) 转二进制
static String toOctalString(int i)转八进制
static String toHexString(int i)转16进制

## 2-4 运算符



### 算术运算符

| 运算符 | 运算                     | 范例       | 结果    |
| ------ | ------------------------ | ---------- | ------- |
| +      | 正号                     | +3         | 3       |
| -      | 负号                     | b=4; -b    | -4      |
| +      | 加                       | 5+5        | 10      |
| -      | 减                       | 6-4        | 2       |
| *      | 乘                       | 3*4        | 12      |
| /      | 除                       | 5/5        | 1       |
| %      | 取模(取余)               | 7%5        | 2       |
| ++     | 自增（前）：先运算后取值 | a=2;b=++a; | a=3;b=3 |
| ++     | 自增（后）：先取值后运算 | a=2;b=a++; | a=3;b=2 |
| - -    | 自减（前）：先运算后取值 | a=2;b=- -a | a=1;b=1 |
| - -    | 自减（后）：先取值后运算 | a=2;b=a- - | a=1;b=2 |
| +      | 字符串连接               | “He”+”llo” | “Hello” |

注意：
* 对于除号“/”，它的整数除和小数除是有区别的：整数之间做除法时，只保留整数部分而舍弃小数部分。

* %:取余运算

    java中的取余**可以对浮点数取余**，c/c++中不可。
    **结果的符号与被模数的符号相同**
    开发中，经常使用%来判断能否被除尽的情况。
    如果对负数取模，可以把模数负号忽略不记，如：5%-2=1。 但被模数是负数则不可忽略。此外，取模运算的结果不一定总是整数。

* `++`和`--`
    (前)++ :++a; 先自增1，后运算
    (后)++ :a++; 先运算，后自增1
    
    (前)-- :--a;先自减1，后运算
    (后)-- :a--;先运算，后自减1

* 连接符：+：只能使用在String与其他数据类型变量之间使用。“+”除字符串相加功能外，还能把非字符串转换成字符串

### 赋值运算符

1. 符号：=
* 当“=”两侧数据类型不一致时，可以使用自动类型转换或使用强制类型转换原则进行处理。
* 支持连续赋值。

```java
int i2,j2;
i2 = j2 = 10;//连续赋值
```

2. 扩展赋值运算符： +=, -=, *=, /=, %=

```java
short s1 = 10;
//s1 = s1 + 2;//编译失败
s1 += 2;//结论：不会改变变量本身的数据类型
System.out.println(s1);
```
**运算的结果不会改变变量本身的数据类型**


开发中，如果希望变量实现+2的操作，有几种方法？(前提：int num = 10;)
方式一：num = num + 2;
方式二：num += 2; (推荐)
		
开发中，如果希望变量实现+1的操作，有几种方法？(前提：int num = 10;)
方式一：num = num + 1;
方式二：num += 1; 
方式三：num++; (推荐)



思考

```java
int n=10;
n += (n++) + (++n);//相当于n=n+(n++)+(++n) 10+10+12 =32
System.out.println(n);
```



### 比较运算符（关系运算符）

| 运算符     | 运算               | 范例                      | 结果  |
| ---------- | ------------------ | ------------------------- | ----- |
| ==         | 相等于             | 4==3                      | false |
| !=         | 不等于             | 4!=3                      | true  |
| <          | 小于               | 4<3                       | false |
| >          | 大于               | 4>3                       | true  |
| <=         | 小于等于           | 4<=3                      | false |
| >=         | 大于等于           | 4>=3                      | true  |
| instanceof | 检查是否是类的对象 | “Hello” instanceof String | true  |

注意
* 比较运算符的结果都是boolean型，也就是要么是true，要么是false。
* 比较运算符“==”不能误写成“=” 。
* `<`、`>=`、`<=`:只能使用在数值类型的数据之间。
* `==` 和 `!=`: 不仅可以使用在数值类型数据之间，还可以使用在其他引用类型变量之间。
```java
Account acct1 = new Account(1000);
Account acct2 = new Account(1000);
boolean b1 = (acct1 == acct2);//比较两个Account是否是同一个账户。
boolean b2 = (acct1 != acct2);//

 String str1 = "hello";
        String str2 = "hello";
        String str3 = new String("hello");
        System.out.println(str1.equals(str2));//true
        System.out.println(str1 == str2);//true
        System.out.println(str1.equals(str3));//true
        System.out.println(str1 == str3);//false
```
### 逻辑运算符

`&` 逻辑与
`|` 逻辑或
`！` 逻辑非
`&&` 短路与
`||` 短路或
`^` 逻辑异或

| a     | b     | a&b   | a&&b  | a\|b  | a\|\|b | !a    | a^b   |
| ----- | ----- | ----- | ----- | ----- | ------ | ----- | ----- |
| true  | true  | true  | true  | true  | true   | false | false |
| true  | false | false | false | true  | true   | false | true  |
| false | true  | false | false | true  | true   | true  | true  |
| false | false | false | false | false | false  | true  | false |

注意：

①不可以写成3<x<6，应该写成x>3 && x<6 。
②逻辑运算符操作的都是 `boolean` 类型的变量。而且结果也是 `boolean` 类型
③“&”和“&&”的区别：（开发中，推荐使用&&）
（单&时，左边无论真假，右边都进行运算；双&时，如果左边为真，右边参与运算，如果左边为假，那么右边不参与运算）
  相同点：& 与  && 的运算结果相同；当符号左边是true时，二者都会执行符号右边的运算；
  不同点：当符号左边是false时，`&`继续执行符号右边的运算，`&&`不再执行符号右边的运算（“短路”）。
④“|”和“||”的区别同理，||表示：当左边为真，右边不参与运算。（开发中，推荐使用`||`）


### 位运算符


| <<   | 空位补0，被移除的高位丢弃，空缺位补0。                       |
| ---- | ------------------------------------------------------------ |
| >>   | 被移位的二进制最高位是0，右移后，空缺位补0；最高位是1，空缺位补1。 |
| >>>  | 被移位二进制最高位无论是0或者是1，空缺位都用0补。            |
| &    | 二进制位进行&运算，只有1&1时结果是1，否则是0;                |
| \|   | 二进制位进行 \| 运算，只有0 \|  0时结果是0，否则是1;         |
| ^    | 相同二进制位进行 ^ 运算，结果是0；1^1=0 , 0^0=0；不相同二进制位 ^ 运算结果是1。1^0=1 , 0^1=1 |
| ~    | 正数取反，各二进制码按补码各位取反；负数取反，各二进制码按补码各位取反 |

注意 :

* 无<<<
* 位运算符操作的都是整型的数据
* '<<'在一定范围内，每向左移1位，相当于乘以2
* '>>'在一定范围内，每向右移1位，相当于除以2
* 对于正数来说，空出来的最高位拿0补;对于负数来说：'>>'右移以后，最高空出来的位拿1去补,'>>>'右移以后，高空出来的位拿0去补。

思考：交换两个变量的值

①临时变量（第三杯水）
②加减交换 节省内存但可能超出存储范围，且只能适用于数值型运算
③位运算符

```java
num1 = num1 ^ num2;
num2 = num1 ^ num2;
num1 = num1 ^ num2;
```

### 三元运算符

又叫三目运算符
三元运算符：条件表达式? 表达式1 : 表达式2
条件表达式结果是布尔型 真 执行表达式1；否则执行表达式2

养成好习惯条件表达式加上小括号 (条件表达式)? 表达式1 : 表达式2

`表达式1 和表达式2要求是一致的(类型上)`。且要为可以赋给接收变量的类型(或可以自动转换)

三元运算符可以嵌套、可以改写为if-else结构；反之，不成立。





### 运算符的优先级

|      | . () {} ; ,           |
| ---- | --------------------- |
| R—>L | ++ --  ~ !(data type) |
| L—>R | * / %                 |
| L—>R | + -                   |
| L—>R | << >> >>>             |
| L—>R | < > <= >= instanceof  |
| L—>R | == !=                 |
| L—>R | &                     |
| L—>R | ^                     |
| L—>R | \|                    |
| L—>R | &&                    |
| L—>R | \|\|                  |
| R—>L | ? :                   |
| R—>L | = *= /= %=            |
|      | += -= <<= >>=         |
|      | >>>= &= ^= \|=        |

上一行运算符总优先于下一行。

只有单目运算符、三元运算符、赋值运算符是从右向左运算的。

技巧：想优先运算的加小括号

## 2-5 程序流程控制

### 顺序结构：
程序从上到下执行。

### 分支结构：

#### if-else

1. else 结构是可选的。

2. 针对于条件表达式：
   > 如果多个条件表达式之间是“互斥”关系(或没有交集的关系),哪个判断和执行语句声明在上面还是下面，无所谓。
   > 如果多个条件表达式之间有交集的关系，需要根据实际情况，考虑清楚应该将哪个结构声明在上面。
   > 如果多个条件表达式之间有包含的关系，通常情况下，需要将范围小的声明在范围大的上面。否则，范围小的就没机会执行了。
   
3. if-else结构是可以相互嵌套的。

4. 如果if-else结构中的执行语句只有一行时，对应的一对{}可以省略的。但是，不建议大家省略。

```java
   if (true)int a = 0;//报错 此处不允许使用变量声明
   if (true){int a = 0;}//正常

   https://zhidao.baidu.com/question/750244789601881692.html
   这个很典型的作用域问题，if后如果省略{},那么if只作用于其后面的第一行代码
   这时候如果这行代码只是个变量声明语句的话，这个变量是没有其他任何逻辑可以访问到的，因为作用域问题（如果有{}，那么声明语句中声明的变量只在这个{}内可用），由于省略了{}，作用域有且只有1行，这行代码声明的变量谁也没法访问，这条声明语句就是个废语句，是无效的声明语句，java语法 中严禁出现废语句的，所有废语句都会变成编译错误，不允许出现。
    public String getName(){
       String name = "mike";//正常
       return name;
       name  = "jack";//这条也是废语句，永远不可能被执行到，也会编译不通过
   }
      声明了变量但在后续的代码里从不用它，语法是允许的，但是声明一个根本没法用的变量就不允许了
          
          c/c++里允许废语句
       int main(){
   	if(1)int a=1;
   	return 0;
   	cout<<1;
   }
```

#### switch-case
```java
switch(表达式){
case 常量1:
	执行语句1;
	//break;
case 常量2:
	执行语句2;
	//break;
...
default:
	执行语句n;
	//break;
}
```
① 根据switch表达式中的值，依次匹配各个case中的常量。一旦匹配成功，则进入相应case结构中，调用其执行语句。
  当调用完执行语句以后，则仍然继续向下执行其他case结构中的执行语句，**直到遇到break关键字或此switch-case结构末尾结束为止**。
② break,可以使用在switch-case结构中，表示一旦执行到此关键字，就跳出switch-case结构
③ switch结构中的表达式，只能是如下的6种数据类型之一：
   **byte 、short、char、int、枚举类型(JDK5.0新增)、String类型(JDK7.0新增)**
④ case 之后只能声明常量。不能声明范围。
⑤ break关键字是可选的。
⑥ default:相当于if-else结构中的else.  
  default结构是可选的，而且位置是灵活的。

如果switch-case结构中的多个case的执行语句相同，则可以考虑进行合并。

break在switch-case中是可选的

### 循环结构：

#### for

for(①;②;④){
	③
}
执行过程：① - ② - ③ - ④ - ② - ③ - ④ - ... - ②

#### while

①
while(②){
	③;
	④;
}

执行过程：① - ② - ③ - ④ - ② - ③ - ④ - ... - ②

写while循环千万小心不要丢了迭代条件。一旦丢了，就可能导致死循环！

1. 开发中，基本上我们都会从for、while中进行选择，实现循环结构。
2. for循环和while循环是可以相互转换的！ 
    区别：for循环和while循环的初始化条件部分的作用范围不同。
3. 我们写程序，要避免出现死循环。
4. “无限循环”结构: while(true) 或 for(;;)

#### do-while
do-while循环至少会执行一次循环体！开发中，较少使用do-while


## 补充:衡量一个功能代码的优劣：

1.正确性
2.可读性
3.健壮性
4.高效率与低存储：时间复杂度 、空间复杂度 （衡量算法的好坏）

## break和continue

break和continue关键字的使用

| 关键字   | 使用范围                | 循环中使用的作用(不同点) | 相同点                     |
| -------- | ----------------------- | ------------------------ | -------------------------- |
| break    | switch-case、循环结构中 | 结束当前(一层)循环       | 关键字后面不能声明执行语句 |
| continue | 循环结构中              | 结束当次(一次)循环       | 关键字后面不能声明执行语句 |

补充：带标签的break和continue的使用

```java
label: for(int i=1;i<100;i++){
    for(int i=1;i<100;i++){
    	//break;//默认跳出包裹次关键字最近一层的循环
        //continue;//默认跳出包裹次关键字最近一层的循环的当次循环
        //break label;//跳出指定标识符的一层循环
        cnotinue label;//跳出指定标识符的一层循环的当次循环
    }
}
```

##  补充：Scanner类的应用

如何从键盘获取不同类型的变量：需要使用Scanner类

具体实现步骤：
1.导包：import java.util.Scanner;
2.Scanner的实例化:Scanner scan = new Scanner(System.in);
3.调用Scanner类的相关方法（next() / nextXxx()），来获取指定类型的变量

注意：
需要根据相应的方法，来输入指定类型的值。如果输入的数据类型与要求的类型不匹配时，会报异常：InputMisMatchException
导致程序终止。

```java
//对于char型的获取，Scanner没有提供相关的方法。只能获取一个字符串
		System.out.println("请输入你的性别：(男/女)");
		String gender = scan.next();//"男"

//补充：获取索引位置上的字符 str.charAt(index)
		char genderChar = gender.charAt(0);
		System.out.println(genderChar);	
```


# 第3章 数组



## 3.1数组的概述

（python中叫列表）

1.数组(Array)的定义：是多个**相同类型数据**按**一定顺序排列**的集合，并使用**一个名字命名**，并通过**编号**的方式对这些数据进行统一管理。

2.数组相关的概念：
 * 数组名
 * 元素
 * 角标、下标、索引
 * 数组的长度：元素的个数

3.数组的特点

  数组是序排列的
  数组属于引用数据类型的变量。数组的元素，既可以是基本数据类型，也可以是引用数据类型
  创建数组对象会在内存中开辟一整块连续的空间
  数组的长度一旦确定，就不能修改。

4.数组的分类：
  按维数：一维数组、二维数组、。。。
  按数组元素的类型：基本数据类型元素的数组、引用数据类型元素的数组

## 3.2一维数组的使用

### 1.声明方式
type var[] 或type[] var;
**==Java语言中声明数组时不能指定其长度==**(数组中元素的数)， 例如： int a[5]; //非法

### 2.初始化：分配空间+赋值

对于数组，初始化动作可以出现在代码的任何地方，但是也可以使用一种特殊的初始化表达式，它必须在创建数组的地方出现。这种特殊的初始化是由**一对花括号括起来的值**组成。这种情况下，存储空间的分配（相当于使用 new）将由编译器负责。

* 静态初始化：在定义数组的同时就为数组元素分配空间并赋值。

```java
int[] arr=new int[]{3,9,8};
或 
int[] arr={3,9,8};

String[] names1=new String[]{"小明","小红","小美"};
或
String[] names2={"小明","小红","小美"};
```

* 动态初始化：数组声明且为数组元素分配空间  与  赋值的操作分开进行

```java
String[] names=new String[3];
names[0]="小明";
names[1]="小红";
names[2]="小美";
```

错误示例：
```java
错误的方式：
(1)
//		int[] arr1 = new int[];//初始化里未指明长度
    int[] arr1 = new int[3];
(2)
//		int[5] arr2 = new int[5];//声明里不能指定长度
    int[] arr2 = new int[5];
(3)
//		int[] arr3 = new int[3]{1,2,3};//静态初始化里不要声明个数
    int[] arr3 = new int[]{1,2,3}
(4)
	//int[] arr4;//
	//arr4={1,2,3};//数组常量只能在初始化操作中使用.只能在一行里写{}的. 不能判断类型
	int[] arr4 = {1,2,3}//可以省略new int[]。创建{}里的元素可以根据前面的int有个类型判断
```

数组一旦初始化完成，其长度就确定了。



小技巧： 在 Java 中， 允许数组长度为 0。 在编写一个**结果为数组的方法时， 如果碰巧结果为空**， 则这种语法形式就显得非常有用。 此时可以**创建一个长度为 0 的数组**：
new elementType[0]
如return new int[0];
注意， **数组长度为 0 与 null 不同**。

### 3.调用数组指定位置的元素

通过角标index
角标从0开始到数组长度-1
若越界会通过编译，但运行时抛异常ArrayIndexOutOfBoundsException。
字符串使用chatAt(index)

### 4.获取数组的长度

数组名.length

### 5.如何遍历

循环

### 6.数组元素的默认初始化值

数组元素是整型(byte short int long)：0
数组元素是浮点型：0.0
数组元素是char型：0或'\u0000'(空字符，不是空格)，而非'0'
数组元素是boolean型：false

数组元素是引用数据类型：null

7.数组的内存结构

![内存结构](http://101.34.218.64/JavaSE.assets/%E5%86%85%E5%AD%98%E7%BB%93%E6%9E%84.png)

这里数组的内存涉及到栈和堆

```java
	int[] arr=new int[]{1,2,3};
	String[] arr1=new String[4];
	arr1[1]="刘德华";
	arr1[2]="张学友";
	arr1=new String[3];
```

![数组的内存结构](http://101.34.218.64/JavaSE.assets/%E6%95%B0%E7%BB%84%E7%9A%84%E5%86%85%E5%AD%98%E7%BB%93%E6%9E%84.JPG)
（这里地址是为了讲解随意给出的。而且地址不是和c里的实际的物理内存地址一样，是堆里根据hash算的）
（”刘德华“ ”张学友“其实是放在字符串常量池中，图里没体现）



## 3.3多维数组的使用

其实，从数组底层的运行机制来看，其实没有多维数组。

数组属于引用数据类型，数组的元素也可以是引用数据类型
可以看成是一维数组array1又作为另一个一维数组array2的元素而存
在。array2称为二维数组。

### 二维数组的初始化

```java
//(1)动态初始化
int[][] arr = new int[3][2];//格式1 内层元素是0
int[][] arr = new int[3][];//格式2  不同于格式1，格式2的每个一维数组(外层元素)都是默认初始化值null
可以对这三个一维数组分别进行初始化 元素个数可以不同且无限制.（格式1也可以不同且无限制，因为只是引用，new之后把新的地址给arr[index]就好了）
arr[0] = new int[3]; 
arr[1] = new int[1]; 
arr[2] = new int[2];

//int[][] arr = new int[][3]; //非法

//(2)静态初始化
int[][] arr = new int[][]{{3,8,2},{2,7},{9,0,1,6}};
```

注意特殊写法情况：`int[] x,y[]; `定义了两个数组，x是一维数组，y是二维数组。

```java
提示：
一维数组：int[] x 或者int x[]
二维数组：int[][] y 或者 int[] y[] 或者 int y[][]
```



Java中多维数组**不必**都是规则矩阵形式

### 二维数组元素的默认初始化值



针对于初始化方式一：比如：

```java 
int[][] arr1 = new int[4][3];
System.out.println(arr1[0]);//地址值
System.out.println(arr1[0][0]);//0
```
 * 外层元素的初始化值为：地址值

 * 内层元素的初始化值为：与一维数组初始化情况相同(见3.2  6)

   

 * 针对于初始化方式二：比如：
```java
int[][] arr2 = new int[4][];
System.out.println(arr2[0]);//null
//System.out.println(arr2[0][0]);//报错java.lang.NullPointerException 因为arr2[0]是null,无法找到arr2[0][0]
arr2[0]=new int[2];//给arr2[0]初始化一下就好了
System.out.println(arr2[0]);//地址值
System.out.println(arr2[0][0]);//0
```

 * 外层元素的初始化值为：null（即引用类型的默认。数组是一种引用类型）

 * 内层元素的初始化值为：不能调用，否则报错。

### 二维数组的内存分析

```java
int[][] arr1 = new int[4][];
arr1[1] = new int[]{1,2,3};
arr1[2] = new int[4];
arr1[2][1] = 30;
```

![二维数组的内存分析](http://101.34.218.64/JavaSE.assets/%E4%BA%8C%E7%BB%B4%E6%95%B0%E7%BB%84%E7%9A%84%E5%86%85%E5%AD%98%E5%88%86%E6%9E%90.png)

## 3.3数组中涉及到的常见算法

数据结构概述:
数据与数据之间的逻辑关系：集合、一对一、一对多、多对多
数据的结构：线性结构（顺序表、链表、栈、队列）、树形结构（比如：二叉树）、图形结构
算法：主要是排序、搜索

### 数组元素的赋值

(杨辉三角、回形数等)

### 求数值型数组中元素的最大值、最小值、平均数、总和等

```java
public class ArrayTest {
	public static void main(String[] args) {
		int[] arr = new int[10];
		for (int i = 0; i < arr.length; i++) {
			arr[i] = (int) (Math.random() * (99 - 10 + 1) + 10);
			System.out.print(arr[i] + " ");
		}
		// 要求"所有随机数是两位数"也就是说[10,99]
		// Math.random()//[0.0,1.0)
		// Math.random()*90//[0.0,90.0)
		// Math.random()*90+10//[10.0,100.0)
		// (int)(Math.random()*90+10)//[10,99]

		// Math.random() 范围[0.0,1.0)
		// 公式:获取[a,b]的随机数 (int)(Math.random()*(b-a+1)+a)
		int maxValue = arr[0], minValue = arr[0];
		int maxi = 0, mini = 0, sum = 0;
		for (int i = 1; i < arr.length; i++) {
			if (maxValue < arr[i]) {
				maxValue = arr[i];
				maxi = i;
			}
			if (minValue > arr[i]) {
				minValue = arr[i];
				mini = i;
			}
			sum += arr[i];
		}
		System.out.println("\n最大值：" + maxValue + "下标" + maxi + "\n最小值"+ minValue + "下标" + mini + "\n总和" + sum + "\n平均值"+ sum / (double) arr.length);
	}

}
```

==Math.random() 范围[0.0,1.0)==

==公式:获取[a,b]的随机数` (int)(Math.random()*(b-a+1)+a)`==

### 数组的复制、反转、查找(线性查找、二分法查找)

```java
public class ArrayTest2 {

	public static void main(String[] args) {

		String[] arr = new String[] { "aa", "bb", "cc", "dd", "ee" };
		// 数组复制（区别于arr1=arr;
		String[] arr1 = new String[arr.length];
		for (int i = 0; i < arr1.length; i++) {
			arr1[i] = arr[i];
		}

		// 数组反转
		for (int i = 0; i < arr1.length / 2; i++) {
			String temp = arr[i];
			arr[i] = arr[arr.length - i - 1];
			arr[arr.length - i - 1] = temp;
		}
		// 方法二
		for (int i = 0, j = arr.length - 1; i < j; i++, j--) {
			/* 交换 */}

		// 数组的查找(搜索)
		// （1）线性查找
		System.out.println("线性查找：");
		String dest = "bb";
		boolean isFlag = false;
		for (int i = 0; i < arr1.length; i++) {
			if (dest.equals(arr[i])) {
				System.out.println("找到了指定的元素，位置：" + i);
				isFlag = true;
				break;
			}
		}
		if (!isFlag) {
			System.out.println("没找到");
		}

		// （2）二分查找（折半查找）
		// 前提：所要查找的数组必须有序
		System.out.println("二分查找：");
		int[] arr2 = new int[] { -23, -12, 3, 6, 12, 34, 35, 45, 54, 67, 76, 88, 99, 100 };
		int dest2 = 34;
		int head = 0;
		int end = arr2.length - 1;
		//int count=0;
		while (head <= end) {
			int mid = (head + end) / 2;
			//count++;
			if (dest2 == arr2[mid]) {
				System.out.println("找到了" + dest2);
				//System.out.println("比较次数"+count);
				break;
			} else if (dest2 > arr2[mid]) {
				head = mid + 1;
			} else {
				end = mid - 1;
			}
		}
		if(head>end)System.out.println("查找失败");

	}
}
```


### 数组元素的排序算法

1. 衡量排序算法的优劣：
①时间复杂度：分析关键字的比较次数和记录的移动次数
②空间复杂度：分析排序算法中需要多少辅助内存
③稳定性：若两个记录A和B的关键字值**相等**，但**排序后A、B的先后次序保持不变**，则称这种排序算法是稳定的。

2. 算法的五大特征：

输入（Input）：有0个或多个输入数据，这些输入必须有清楚的描述和定义
输出（Output）：至少有1个或多个输出结果，不可以没有输出结果
有穷性（有限性，Finiteness）:算法在有限的步骤之后会自动结束而不会无限循环，并且每一个步骤可以在可接受的时间内完成
确定性（明确性，Definiteness）:算法中的每一步都有确定的含义，不会出现二义性
可行性（有效性，Effectiveness）:算法的每一步都是清楚且可行的，能让用户用纸笔计算而求出答案

(说明：满足确定性的算法也称为：确定性算法。现在人们也关注更广泛的概念，例如考虑各种非确定性的算法，如并行算法、概率算法等。另外，人们也关注并不要求终止的计算描述，这种描述有时被称为过程（procedure）。)

3. 排序算法分类：内部排序和外部排序

内部排序：整个排序过程不需要借助于外部存储器（如磁盘等），所有排序操作都在**内存**中完成。
外部排序：参与排序的数据非常多，数据量非常大，计算机无法把整个排序过程放在内存中完成，**必须借助于外部存储器**（如磁盘）。外部排序最常见的是多路归并排序。可以认为外部排序是由多次内部排序组成。

十大内部排序算法

选择排序：直接选择排序(也叫简单选择排序)、堆排序
交换排序：冒泡排序、快速排序——这两种重点掌握，要会写。开发中快速排序用的多，包中封装的也是这种
插入排序：直接插入排序、折半插入排序、shell(希尔)排序
归并排序
桶排序
基数排序

#### (1)冒泡排序

```java
public class BubbleSort {

	public static void main(String[] args) {
		int[] arr = new int[] { 43, 32, 3, 34, 23, 32, 25, 64 };
		for (int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}
//最简单的交换排序 不算是冒泡 因为不符合两两比较相邻记录
//		for (int i = 0; i < arr.length - 1; i++) {
//			for (int j = i + 1; j < arr.length; j++) {
//				if (arr[i] < arr[j]) {
//					int temp = arr[i];
//					arr[i] = arr[j];
//					arr[j] = temp;
//
//				}
//			}
//		}
//		System.out.println();
//		for (int i = 0; i < arr.length; i++) {
//			System.out.print(arr[i] + " ");
//		}

		// 冒泡排序
		int count = 0;// 比较次数
		for (int i = 0; i < arr.length - 1; i++) {// 这里的i是为了给控制arr.length-1-i的吧  其实这里 i < arr.length也行
			for (int j = 0; j < arr.length - 1 - i; j++) {
				count++;
				if (arr[j] > arr[j + 1]) {// 变小于号可以从大到小
					int temp = arr[j];
					arr[j] = arr[j + 1];
					arr[j + 1] = temp;

				}
			}
		}
		System.out.println("\n冒泡排序 比较次数" + count);
		for (int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}

		// 冒泡排序优化版 防止有序以后后面不需要交换，但程序仍比较 的问题
		count = 0;
		boolean flag = true;
		for (int i = 0; i < arr.length - 1 && flag; i++) {// flag为true表示有数据交换，仍需比较;否则，上一趟已经有序，退出循环
			flag = false;
			for (int j = 0; j < arr.length - 1 - i; j++) {
				count++;
				if (arr[j] > arr[j + 1]) {// 变小于号可以从大到小
					int temp = arr[j];
					arr[j] = arr[j + 1];
					arr[j + 1] = temp;
					flag = true;
				}
			}
		}
		System.out.println("\n冒泡排序优化版 比较次数" + count);
		for (int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}
	}

}
/*输出：
43 32 3 34 23 32 25 64 
冒泡排序 比较次数28
3 23 25 32 32 34 43 64 
冒泡排序优化版 比较次数7
3 23 25 32 32 34 43 64 
*/
```

#### (2)快速排序

快速排序(Quick Sort) 的基本思想是:通过一趟排序将待排记录分割成独立的两部分，其中一部分记录的关键字均比另一部分记录的关键字小， 则可分别对这两部分记录继续进行排序，以达到整个序列有序的目的。

基于分治的思想，每趟排序可以确定一个元素的位置（归位）。

一趟快速排序的过程称为一次划分，具体做法是:附设两个位置指示变量low和high,它们的初值分别指向序列的第一一个 记录和最后-一个记录。设枢轴记录(通常是第一个记录)的关键字为pivot,则首先从high所指位置起向前搜索,找到第一个关键字小于pivot的记录时将该记录向前移到low指示的位置，然后从low所指位置起向后搜索，找到第一一个关键字大于pivot的记录时将该记录向后移到j所指位置，重复该过程直至i与j相等为止。

以第一个元素为基准元素就    先从后往前找    再从前往后找
以最后一个元素为基准元素就  先从前往后找    再从后往前找

```java
public class QuickSort {
	private static void swap(int[] data, int i, int j) {
		int temp = data[i];
		data[i] = data[j];
		data[j] = temp;
	}

	private static void subSort(int[] data, int start, int end) {
		if (start < end) {
			int base = data[start];
			int low = start;
			int high = end + 1;
			while (true) {
				while (low < end && data[++low] - base <= 0)
					;
				while (high > start && data[--high] - base >= 0)
					;
				if (low < high) {
					swap(data, low, high);
				} else {
					break;
				}
			}
			swap(data, start, high);
			
			subSort(data, start, high - 1);//递归调用
			subSort(data, high + 1, end);
		}
	}
	public static void quickSort(int[] data){
		subSort(data,0,data.length-1);
	}
	
	
	public static void main(String[] args) {
		int[] data = { 9, -16, 30, 23, -30, -49, 25, 21, 30 };
		System.out.println("排序之前：\n" + java.util.Arrays.toString(data));
		quickSort(data);
		System.out.println("排序之后：\n" + java.util.Arrays.toString(data));
	}
}
```

#### (3)各种内部排序方法性能比较

1.从平均时间而言：快速排序最佳（记住它的复杂度nlog2N）。但在最坏情况下时间性能不如堆排序和归并排序。
2.从算法简单性看：
由于直接选择排序、直接插入排序和冒泡排序的算法比较简单，将其认为是简单算法。
对于Shell排序、堆排序、快速排序和归并排序算法，其算法比较复杂，认为是复杂排序。

3.从稳定性看：直接插入排序、冒泡排序和归并排序时稳定的；而直接选择排序、快速排序、 Shell排序和堆排序是不稳定排序
4.从待排序的记录数n的大小看，n较小时，宜采用简单排序；而n较大时宜采用改进排序。

![排序复杂度和稳定性口诀](http://101.34.218.64/JavaSE.assets/%E6%8E%92%E5%BA%8F%E5%A4%8D%E6%9D%82%E5%BA%A6%E5%92%8C%E7%A8%B3%E5%AE%9A%E6%80%A7%E5%8F%A3%E8%AF%80.png)

![排序对比表格](http://101.34.218.64/JavaSE.assets/%E6%8E%92%E5%BA%8F%E5%AF%B9%E6%AF%94%E8%A1%A8%E6%A0%BC.png)
马士兵说：30秒让你记住所有排序算法-宋词记忆法https://www.bilibili.com/video/av46648286

#### (4)排序算法的选择(了解)

(1)若n较小(如n≤50)，可采用直接插入或直接选择排序。
当记录规模较小时，直接插入排序较好；否则因为直接选择移动的记录数少于直接插入，应选直接选择排序为宜。
(2)若文件初始状态基本有序(指正序)，则应选用直接插入、冒泡或随机的快速排序为宜；
(3)若n较大，则应采用时间复杂度为O(nlgn)的排序方法：快速排序、堆排序或归并排序

## 3.4Arrays工具类的使用
java.util.Arrays   （util是工具类的意思）
 定义在java.util包下,Arrays提供了很多操作数组的方法。

```java
import java.util.Arrays;

public class ArraysTest {
	public static void main(String[] args) {
		//1.boolean equals(int[] a,int[] b):判断两个数组是否相等。
				int[] arr1 = new int[]{1,2,3,4};
				int[] arr2 = new int[]{1,3,2,4};
				boolean isEquals = Arrays.equals(arr1, arr2);
				System.out.println(isEquals);
				
				//2.String toString(int[] a):输出数组信息。
				System.out.println(Arrays.toString(arr1));
				
					
				//3.void fill(int[] a,int val):将指定值填充到数组之中。(所有的数组元素都变成val)
				Arrays.fill(arr1,10);
				System.out.println(Arrays.toString(arr1));
				

				//4.void sort(int[] a):对数组进行排序。底层是一种快速排序：DualPivotQuicksort双枢轴快速排序
				Arrays.sort(arr2);
				System.out.println(Arrays.toString(arr2));
				
				//5.int binarySearch(int[] a,int key)//对排序后的数组进行二分法检索指定的值。
				int[] arr3 = new int[]{-98,-34,2,34,54,66,79,105,210,333};
				int index = Arrays.binarySearch(arr3, 210);
				if(index >= 0){
					System.out.println(index);
				}else{
					System.out.println("未找到");
				}

	}
}
/*
false
[1, 2, 3, 4]
[10, 10, 10, 10]
[1, 2, 3, 4]
8
*/
```

注意：不仅是对数值型数组操作，其它类型也可以。会重载去调用不同的方法。

```java
//void fill(Object[] a, Object val)
				String[] strArr=new String[] {"昨天","今天","明天"};
				Arrays.fill(strArr,"后天");
				System.out.println(Arrays.toString(strArr));
```



## 3.5数组使用中的常见异常

(1)数组角标越界 ArrayIndexOutOfBoundsException。

(2)空指针异常 NullPointerException

这种异常这些情况下常见

```java
	//情况一：
//		int[] arr1 = new int[]{1,2,3};
//		arr1 = null;
//		System.out.println(arr1[0]);
		
		//情况二：
//		int[][] arr2 = new int[4][];
//		System.out.println(arr2[0][0]);
		
		//情况：
		String[] arr3 = new String[]{"AA","BB","CC"};
		arr3[0] = null;
		System.out.println(arr3[0].toString());
```


# 第4章 面向对象编程(上)

学习的三条主线：

（1）Java类及类的成员：属性、方法、构造器、代码块、内部类（后两个用的少）
（2）面向对象的三大特征：封装 、继承、 多态、（抽象性）
（3）其它关键字：this、super、static、final、abstract、interface、package、import等

## 面向过程与面向对象

1.面向过程(Procedure Oriented Programming,POP)
强调的是功能行为，以函数为最小单位，考虑怎么做。
2.面向对象(Object Oriented Programming,OOP)
强调具备了功能的对象，以类/对象为最小单位，考虑谁来做。

“万事万物皆对象”：

①在java语言范畴中，我们都将功能、结构等封装到类中，通过类的实例化，来调用具体的功能结构。
②涉及到Java语言与前端Html、后端的数据库交互时，前后端的结构在java层面交互式，都体现为类、对象。

## Java基本元素：类和对象

类(Class):对一类事物的描述，是**抽象的**、概念上的定义
对象(Object):是**实际存在的**该类事物的每个个体（**具体的**），因而也称为实例(instance)

面向对象程序设计的重点是类的设计,类的设计就是设计类的成员。

面向对象思想落地实现的规则
 * 创建类，设计类的成员
 * 创建类的对象
 * 通过“对象.属性”或“对象.方法”调用对象的结构

补充：几个概念的使用说明,不同的教程、书籍叫法不同
 *  属性 = 成员变量 = field = 域、字段
 *  方法 = 成员方法 = 函数 = method
 *  创建类的对象 = 类的实例化 = 实例化类

### 类的语法格式

修饰符 class 类名 {
属性声明;
方法声明;
}
说明：修饰符public：类可以被任意访问
类的正文要用{ }括起来
举例：

```java
public class Person{
 private int age ;//声明私有变量 age
 public void showAge(int i) { //声明方法showAge( )
 age = i;
 }
}
```

### 创建一个类的步骤

1. 定义类（考虑修饰符、类名）
2. 编写类的属性（考虑修饰符、属性类型、属性名、初始化值）
3. 编写类的方法（考虑修饰符、返回值类型、方法名、形参等）

### 对象的创建和使用

创建对象语法： 类名 对象名 = new 类名();
使用“对象名.对象成员”的方式访问对象成员（包括属性和方法）

如果创建了一个类的多个对象，则每个对象都独立的拥有一套类的属性（非static的）。意味着：如果我们修改一个对象的属性a，则不影响另外一个对象属性a的值。

### 对象的内存解析

#### JVM的内存区域

![](http://101.34.218.64/JavaSE.assets/JVM%E5%86%85%E5%AD%98%E5%8C%BA%E5%9F%9F.png)

**堆（Heap）**，此内存区域的唯一目的就是**存放对象实例**，几乎所有的对象实例都在这里分配内存。这一点在Java虚拟机规范中的描述是：所有的**对象实例以及数组**都要在堆上分配。
通常所说的**栈（Stack）**，是指**虚拟机栈**。虚拟机栈用于**存储局部变量等**。局部变量表存放了编译期可知长度的各种基本数据类型（boolean、byte、char 、 short 、 int 、 float 、 long 、double）、对象引用（reference类型，它不等同于对象本身，是对象在堆内存的首地址）。 方法执行完，自动释放(方法中的变量都是局部变量)。补充：对象的属性（非static的）加载在堆空间中。
方法区（Method Area），用于存储已被虚拟机加载的类信息、常量(常量池)、静态变量(静态域)、即时编译器编译后的代码等数据



#### 一个对象创建例子分析内存

![](http://101.34.218.64/JavaSE.assets/%E5%AF%B9%E8%B1%A1%E7%9A%84%E5%86%85%E5%AD%98%E5%88%86%E6%9E%90.JPG)

（注意 p1,p2,p3其实是在main方法中。”Tom“其实是在方法区的常量池）

栈：局部变量
堆：new 出来的结构：数组、对象

#### 对象数组的内存分析

 ![对象数组的内存分析](http://101.34.218.64/JavaSE.assets/%E5%AF%B9%E8%B1%A1%E6%95%B0%E7%BB%84%E7%9A%84%E5%86%85%E5%AD%98%E5%88%86%E6%9E%90.png)

(引用类型的变量：只可能存储两类值：null 或者地址值（含变量的类型）)

#### 匿名对象

我们也可以不定义对象的句柄(没有显式的赋给一个变量名)，而直接调用这个对象的方法。这样的对象叫做匿名对象。
如：new Person().shout();

使用情况
如果对一个对象只需要进行一次方法调用，那么就可以使用匿名对象。

```java
new Person().shout();
```

我们经常将匿名对象作为实参传递给一个方法调用。

```java
PhoneMall mall=new PhoneMall();
mall.show(new Phone());
。。。。

class PhoneMall{
    public void show(Phone phone){
        phone.sendEmail;
        phone.playGame
    }
}
```



## 类的成员之一：属性

### 语法格式：

修饰符 数据类型 属性名 = 初始化值 ;
* 说明1: 修饰符
	常用的权限修饰符有：private、缺省、protected、public
	其他修饰符：static、final (暂不考虑)
* 说明2：数据类型
	任何基本数据类型 或 任何引用数据类型。
* 说明3：属性名
	属于标识符，符合命名规则和规范即可。

### 对比：属性（成员变量）和局部变量（local variable）

复习变量的分类：

![成员变量和局部变量](http://101.34.218.64/JavaSE.assets/%E6%88%90%E5%91%98%E5%8F%98%E9%87%8F%E5%92%8C%E5%B1%80%E9%83%A8%E5%8F%98%E9%87%8F.jpg)



#### 1.相同点：

 * 1.1  定义变量的格式：数据类型  变量名 = 变量值
 * 1.2 先声明，后使用
 * 1.3 变量都其对应的作用域 

#### 2.不同点：

  2.1 在类中声明的位置的不同
 * 属性：直接定义在类的一对{}内
 * 局部变量：声明在方法内、方法形参、代码块内、构造器形参、构造器内部的变量

  2.2 关于权限修饰符的不同

 * 属性：可以在声明属性时，指明其权限，使用权限修饰符。
   > 常用的权限修饰符：private、public、缺省、protected  --->封装性
    （目前初学阶段，大家声明属性时，都使用缺省就可以了。）

 * 局部变量：不可以使用权限修饰符。

  2.3 默认初始化值的情况：

* 属性：类的属性，根据其类型，都默认初始化值。
  > 整型（byte、short、int、long：0）、浮点型（float、double：0.0）、字符型（char：0（或'\u0000'））、布尔型（boolean：false）
  > 引用数据类型（类、数组、接口：null）

* 局部变量：没默认初始化值。
 意味着，我们在调用局部变量之前，**一定要显式赋值**。
 特别地：形参在调用时，我们赋值即可。


  2.4 在内存中加载的位置：

 * 		属性：加载到堆空间中   （非static）
 * 		局部变量：加载到栈空间

总结：

|              | 成员变量                         | 局部变量                                 |
| ------------ | -------------------------------- | ---------------------------------------- |
| 声明的位置   | 直接声明在类中                   | 方法形参或内部、代码块内、构造器内等     |
| 修饰符       | private、public、static、final等 | 不能用权限修饰符修饰，可以用final修饰    |
| 初始化值     | 有默认初始化值                   | 没有默认初始化值，必须显式赋值，方可使用 |
| 内存加载位置 | 堆空间 或 静态域内               | 栈空间                                   |

## 类的成员之二：方法

### 什么是方法(method、函数):

* 方法是类或对象行为特征的抽象，用来完成某个功能操作。在某些语言中也称为函数或过程。
* 将功能封装为方法的目的是，可以实现代码重用，简化代码
* Java里的方法不能独立存在，所有的方法必须定义在类里。

### 方法的声明格式

修饰符 返回值类型 方法名（参数类型 形参1, 参数类型 形参2, ….）｛
    方法体程序代码
    return 返回值;
｝
其中：
修饰符：public,缺省,private, protected等
返回值类型：
* 没有返回值：void。
* 有返回值，声明出返回值的类型。与方法体中“return 返回值”搭配使用
方法名：属于标识符，命名时遵循标识符命名规则和规范，“见名知意”
形参列表：可以包含零个，一个或多个参数。多个参数时，中间用“,”隔开
返回值：方法在执行完毕后返还给调用它的程序的数据。

没有具体返回值的情况，返回值类型用关键字void表示，那么方法体中可以不必使用return语句。如果使用，仅用来结束方法。

方法的使用中
* 可以调用当前类的属性或方法
 	特殊的：方法A中又调用了方法A:递归方法。
* 方法中，不可以定义方法。


*新学到一个小方法：四舍五入取整：Math.round(double d)，返回值类型long

​	Math.PI是π

### 方法的重载

#### 重载的概念

在**同一个类**中，允许存在一个以上的**同名**方法，只要它们的**参数个数或者参数类型不同**即可。（两同一不同）

#### 重载的特点：
**与返回值类型无关**，只看参数列表，且参数列表必须不同(参数个数或参数类型)。调用时，根据方法**参数列表的不同**来区别。
和方法的权限修饰符、返回值类型、形参变量名、方法体都没有关系！

#### 重载的好处
减轻了起名的麻烦
减轻了记名的麻烦

#### 重载示例：
```java
//返回两个整数的和
int add(int x,int y){return x+y;}
//返回三个整数的和
int add(int x,int y,int z){return x+y+z;}
//返回两个小数的和
double add(double x,double y){return x+y;}
```

### 可变形参
jdk5.0新增Varargs(variable number of arguments)
采用可变个数形参来定义方法，**传入多个同一类型变量**

可变形参格式：`数据类型...变量名`
三个点叫扩展运算符
(三个点 前后可以有空格)

```java
public void varargsTest(int ... args) {}
public void varargsTest(int[] ... args) {}//可变参数类型可以是数组
```

注意：
 * 可变个数形参可以和普通类型的参数一起在方法的形参中，**可变形参必须声明在末尾**
```java
public void varargsTest(char a,double b,int[] ... c) {}
```

 * 可变个数形参在方法的形参中,**最多只能声明一个可变形参**。
 * 当调用可变个数形参的方法时，传入的参数个数可以是：**0个**，1个,2个，。。。(**可以是0个**,0~多)
 * 可变个数形参的方法与本类中方法名相同，形参不同的方法之间构成重载
 * 可变个数形参的方法与本类中方法名相同，形参类型也相同的**数组**之间**不构成重载**。换句话说，二者不能共存。**被认为是同一方法**。(**可变参数本质上还是数组**。)（这种情况若在子类和父类中，还可以构成重写）
```java
   public void varargsTest(int ... args) {}
   public void varargsTest(int [] args) {}
   //同时定义时会报错 存在重复的方法
```

 * 方法体内取可变参数中的某个参数**可以用索引**，当数组来处理：args[0]。

### 方法参数的值传递机制

方法，必须由其所在类或对象调用才有意义。若方法含有参数：
  形参：方法声明时的参数。（方法定义时，声明的小括号内的参数）
  实参：方法调用时实际传给形参的参数值。（方法调用时，实际传递给形参的数据）

Java的实参值如何传入方法呢？
Java里方法的参数传递方式**只有一种：值传递**。 即将实际参数值的副本（复制品）传入方法内，而参数本身不受影响。
  形参是基本数据类型：将实参基本数据类型变量的“数据值”传递给形参
  形参是引用数据类型：将实参引用数据类型变量的“地址值”传递给形参。
一些其它说法：
  如果参数是基本数据类型，此时实参赋给形参的是实参真实存储的数据值。
  如果参数是引用数据类型，此时实参赋给形参的是实参存储数据的地址值。

```java
变量赋值也是如此
int n=10;int m=n;
n=20;//此时n=20,m仍为10

Student stu1=new Student();
stu1.id=1;
Student stu2 = stu1;
stu1.id=2;//此时stu2.id也为2

注意String很特殊，也是引用数据类型，但是数据存字符串常量池中
    形参也不一定影响实参。
String s1= "hello";
String s2=s1;
System.out.println(s2);
s1="world";
System.out.println(s2);//s2仍然是hello
```

从交换两个数 来体会基本数据类型和引用数据类型的值传递的不同：

![错误的交换](http://101.34.218.64/JavaSE.assets/%E9%94%99%E8%AF%AF%E7%9A%84%E4%BA%A4%E6%8D%A2.png)

![正确的交换](http://101.34.218.64/JavaSE.assets/%E6%AD%A3%E7%A1%AE%E7%9A%84%E4%BA%A4%E6%8D%A2.png)

```java
//从交换两个数 来体会基本数据类型和引用数据类型的值传递的不同
public class valueTransferTest {
	public static void main(String[] args) {
		//基本数据类型 将实参的“数据值”传给形参
		int m = 1, n = 2;
		Tool tool = new Tool();
		tool.swap(m, n);
		System.out.println("m=" + m + " n=" + n);//m=1 n=2 没有交换
		
		//引用数据类型 将实参的“地址值”传给形参
		Data data = new Data();
		data.num1 = 1;
		data.num2 = 2;
		tool.swap(data);
		System.out.println("m=" + data.num1 + " n=" + data.num2);//m=2 n=1 交换成功
	}
}

class Tool {
	void swap(int num1, int num2) {
		int temp = num1;
		num1 = num2;
		num2 = temp;
	}
	void swap(Data data) {
		int temp = data.num1;
		data.num1 = data.num2;
		data.num2 = temp;
	}
}
class Data {
	int num1;
	int num2;
}
```

 一个课外题

```java
import java.io.PrintStream;
public class Question1 {
	public static void main(String[] args) {
		int a = 10;
		int b = 10;
		method(a, b);// 需要在method方法调用后仅打印a=100,b=200
		System.out.println("a=" + a);
		System.out.println("b=" + b);
	}
//	public static void method(int a,int b) {//方法1 提前结束程序
//		a=a*10;
//		b=b*20;
//		System.out.println(a);
//		System.out.println(b);
//		System.exit(0);
//	}
	public static void method(int a, int b) {// 方法1 重写println
		PrintStream ps = new PrintStream(System.out) {
			@Override
			public void println(String x) {
				if ("a=10".equals(x)) {
					x = "a=100";
				} else if ("b=10".equals(x)) {
					x = "b=200";
				}
				super.println(x);
			}
		};
		System.setOut(ps);
	}
}
```

### 递归方法

1.定义：
递归方法：一个方法体内调用它自身。
2.如何理解递归方法？
> 方法递归包含了一种隐式的循环，它会重复执行某段代码，但这种重复执行无须循环控制。
> 递归一定要向已知方向递归，否则这种递归就变成了无穷递归，类似于死循环。

## OOP特征一：封装与隐藏

### 为什么要引入封装性？

程序设计追求“高内聚，低耦合”：

  高内聚 ：类的内部数据操作细节自己完成，不允许外部干涉；
  低耦合 ：仅对外暴露少量的方法用于使用。

隐藏对象内部的复杂性，只对外公开简单的接口。便于外界调用，从而提高系统的可扩展性、可维护性。通俗的说，把该隐藏的隐藏起来，该暴露的暴露出来。这就是封装性的设计思想。

### 封装性思想具体的代码体现

体现一：将类的属性xxx私化(private),同时，提供公共的(public)方法来获取(getXxx)和设置(setXxx)此属性的值

```java
class Animal {
	String name;
	int age;
	private int legs;// 腿的条数 0或正偶数 设置为private私有
	public int getLegs() {//公共方法Getter
		return legs;
	}
	public void setLegs(int l) {//公共方法Setter
		if (l >= 0 && l % 2 == 0) {
			legs = l;
		} else {
			// 抛出一个异常
		}
	}
}
```

体现二：不对外暴露的私有的方法
体现三：单例模式（将构造器私有化）
体现四：如果不希望类在包外被调用，可以将类设置为缺省的。

### 四种访问权限修饰符

封装性的体现需要权限修饰符来配合
权限从小到大顺序为：private <  default缺省 < protected < public
置于**类的成员**定义前，用来限定对象对该类成员的访问权限。

| 修饰符            | 类内部 | 同一个包 | 不同包的子类 | 同一个工程 |
| ----------------- | ------ | -------- | ------------ | ---------- |
| private私有       | Yes    |          |              |            |
| (缺省)            | Yes    | Yes      |              |            |
| protected受保护的 | Yes    | Yes      | Yes          |            |
| public公共        | Yes    | Yes      | Yes          | Yes        |

对于**类**(class)的权限修饰**只可以用public和default(缺省)**。
    public类可以在任意地方被访问。
    default类只可以被同一个包内部的类访问。



## 类的成员之三：构造器Constructor
也叫构造方法
### 构造器的作用

 * 1.创建对象
 * 2.初始化对象的信息
   在创建对象时，系统会自动的调用该类的构造器完成对象的初始化。只要造对象，就得有构造器。
### 构造器的特征

它具有**与类相同的名称**
**它不声明返回值类型**。（与声明为void不同）
不能被static、final、synchronized、abstract、native修饰，可以用权限修饰符
不能有return语句返回值

### 构造器的使用

定义构造器的格式：
权限修饰符 类名 (参数列表) {
初始化语句；
}

```java
public class Persion {
	private String name;
	private int age;
	Persion() {//显式的定义一个无参构造器
	}
	Persion(String name, int age) {//有参构造器
		this.name = name;
		this.age = age;
	}
}
```
说明：
1. 一个类中，至少会有一个构造器。（抽象类也有）
2. 如果没显式的定义类的构造器的话，则系统**默认提供一个空参的构造器**（隐式无参构造器）
3. 一旦我们**显式的定义**了类的构造器之后，系统就**不再提供默认的空参构造器**,如果想用就自己显式定义一个空参构造器(一般开发中习惯上给一个类提供一个空参,涉及到反射)
4. 一个类中定义的多个构造器，彼此构成**重载**
5. **默认的无参构造器，权限修饰符与所属类的修饰符一致**
6. 父类的构造器不可被子类继承。（**构造器不能被继承**）


### 属性赋值的小总结

赋值的位置：
① 默认初始化
② 显式初始化
③ 构造器中初始化
④ 通过“对象.属性“或“对象.方法”的方式赋值

赋值的先后顺序：
① - ② - ③ - ④

## 拓展知识：

###  JavaBean

JavaBean是一种Java语言写成的可重用组件。

所谓javaBean，是指符合如下标准的Java类：
* 类是**公共**的
* 有一个**无参的公共的构造器**
* 有**属性**，且有**对应的get、set**方法

（满足以上三个条件的都可以是java bean）

用户可以使用JavaBean将功能、处理、值、数据库访问和其他任何可以用Java代码创造的对象进行打包，并且其他的开发者可以通过内部的JSP页面、Servlet、其他JavaBean、applet程序或者应用来使用这些对象。用户可以认为JavaBean提供了一种随时随地的复制和粘贴的功能，而不用关心任何改变。

### UML类图

![UML类图](http://101.34.218.64/JavaSE.assets/UML%E7%B1%BB%E5%9B%BE.png)

1. +表示 public 类型， - 表示 private 类型，#表示protected类型
2. 方法的写法:
方法的类型(+、-) 方法名(参数名： 参数类型)：返回值类型

## 关键字：this

可以调用的结构：属性、方法；构造器
1.this调用属性、方法：
   this理解为：当前对象  或 当前正在创建的对象
	(注：使用this访问属性和方法时，如果在本类中未找到，会从父类中查找)
    (1)在**类的方法**中，我们可以使用"this.属性"或"this.方法"的方式，调用当前对象属性或方法。但是，
    ​	通常情况下，我们都择省略"this."。
    ​	特殊情况下，如果**方法的形参和类的属性同名时**，我们必须**显式的使用"this.变量"的方式，表明此变量是属性，而非形参。**
    (2)在**类的构造器**中，我们可以使用"this.属性"或"this.方法"的方式，调用当前**正在创建**的对象属性或方法。但是，
    ​	通常情况下，我们都择省略"this."。
    ​	特殊情况下，如果**构造器的形参和类的属性同名时**，我们必须**显式的使用"this.变量"的方式，表明此变量是属性，而非形参**。

2.this调用构造器：
    ① 我们在类的构造器中，可以显式的使用"this(形参列表)"方式，调用本类中指定的其他构造器
    ② 构造器中**不能**通过"this(形参列表)"方式**调用自己**
    ③ 如果一个类中有n个构造器，则最多有 **n - 1**构造器中使用了"this(形参列表)"
    ④ 规定："this(形参列表)"**必须**声明在**当前构造器的首行**
    ⑤ 构造器内部，**最多只能声明一个"this(形参列表)"**，用来调用其他的构造器



## 关键字：package、import

### 包的作用

包帮助管理大型软件系统：将功能相近的类划分到同一个包中。比如：MVC的设计模式
包可以包含类和子包，划分项目层次，便于管理
解决类命名冲突的问题
控制访问权限

### 包的命名

命名规则:只能包含数字、字母、下划线、 小圆点.但不能用数字开头，不能是关键字或保留字
demo.class.exec1 对
demo.12a 错
demo.ab12.0a 错

命名规范：包通常用小写单词标识。通常使用所在公司域名的倒置
一般是**小写字母+小圆点**
一般是 **com.公司名项目名.业务模块名**
比如: com.hspedu.oa.model; com.hspedu.oa.controller;
举例:
com.sina.crm.user //用户模块
com.sina.crm.order“订单模块
com.sina crm.utils //工具类

### package关键字的使用

 * 1.为了更好的实现项目中类的管理，提供包的概念

 * 2.使用package声明类或接口所属的包，声明在源文件的首行（并不是.java文件的第一行，是代码的第一行）。表示"打包在哪个包下

 * 3.包，属于标识符，遵循标识符的命名规则、规范(xxxyyyzzz)、“见名知意”

 * 4.每"."一次，就代表一层文件目录。**用 “.” 来指明包(目录)的层次**

 * 同一个包下不能命名同名的类或接口。(包的本质 是创建不同的目录来保存类或接口文件)

### MVC设计模式

MVC是常用的设计模式之一，将整个程序分为三个层次：**视图模型层、控制器层、数据模型层**。这种将程序输入输出、数据处理，以及数据的展示分离开来的设计模式使程序结构变的灵活而且清晰，同时也描述了程序各个对象间的通信方式，降低了程序的耦合性。

![MVC设计模式](http://101.34.218.64/JavaSE.assets/MVC%E8%AE%BE%E8%AE%A1%E6%A8%A1%E5%BC%8F.png)

模型层model 主要处理数据
>数据对象封装 model.bean/domain
>数据库操作类 model.dao
>数据库 model.db

控制层 controller 处理业务逻辑
>应用界面相关 controller.activity
>存放fragment controller.fragment
>显示列表的适配器 controller.adapter
>服务相关的 controller.service
>抽取的基类 controller.base

视图层view 显示数据
>相关工具类view.utils
>自定义view view.ui

### JDK中主要的包介绍

1.java.lang----包含一些Java语言的核心类，如String、Math、Integer、 System和Thread，提供常用功能
2.java.net----包含执行与网络相关的操作的类和接口。
3.java.io----包含能提供多种输入/输出功能的类。
4.java.util----包含一些实用工具类，如定义系统特性、接口的集合框架类、使用与日期日历相关的函数。
5.java.text----包含了一些java格式化相关的类
6.java.sql----包含了java进行JDBC数据库编程的相关类/接口
7.java.awt----包含了构成抽象窗口工具集（abstract window toolkits）的多个类，这些类被用来构建和管理应用程序的图形用户界面(GUI)。 B/S  C/S

### import关键字的使用

为使用定义在不同包中的Java类，需用import语句来引入指定包层次下所需要的类或全部类(.*)。（import语句告诉编译器到哪里去寻找类。）（**导包**）

语法格式：
import 包名. 类名;

注意：
1. 在源文件中使用import显式的导入指定包下的类或接口

2. 声明在包的声明和类的声明之间。(不然会报错)
```
<包声明>
<导入声明>
<类声明>
```
3. 如果需要导入多个类或接口，那么就并列显式多个import语句即可

```java
   import java.util.Scanner;
   import java.util.Arrays;
   import java.util.HashMap;
```

4. 举例：可以使用java.util.*的方式，一次性导入util包下所有的类或接口。
```java
import java.util.*;
```
5. 如果导入的类或接口是**java.lang包下**（）的，或者是**当前包下**的，则可以**省略**此import语句。
   >有三种包在JVM运行时会自动被导入
   >1. 当前主类所在的包
   >2. java.lang包
   >3. 没有名字的包（缺省)

6. 如果在代码中**使用不同包下的同名的类**。那么就需要使用**类的全类名**的方式指明调用的是哪个类。
```java
//例如Date类 两个包里都有。java.util.Date java.sql.Date
import java.util.Date;//已经导入了一个 再导入另一个会冲突 但两个都想用时
。。。
Date date = new Date();//java.util.Date
java.sql.Date date1 = new java.sql.Date(12345L);//java.sql.Date
```

7. 如果已经导入java.a包下的类。那么如果需要使用a包的**子包下的类**的话，**仍然需要导入**。（`.*`代表的是类和接口，不能代表子包）(从编译器的角度来看， 嵌套的包之间没有任何关系)

8. **import static组合**的使用：调用指定类或接口下的**静态的属性或方法**
```java
import static java.lang.System.*;
//就可以使用 System 类的静态方法和静态域，而不必加类名前缀：(这里的.*代表静态方法和静态属性)
out.println("Goodbye, World!"); //i.e., System.out
exit⑼; //i.e., System.exit
```

# 第5章 面向对象编程(中)

## OOP特征二：继承性

### 为什么要有继承？

多个类中存在相同属性和行为时，将这些内容抽取到单独一个类中，那么多个类无需再定义这些属性和行为，只要继承那个类即可。

此处的多个类称为**子类(派生类)**，单独的这个类称为**父类(基类或超类)**。可以理解为:“子类 is a 父类”

### 类继承语法规则

```java
class SubClass extends SuperClass{ }
//Subclass:子类、派生类
//SuperClass:父类、超类、基类
```


### 继承的作用

* 继承的出现减少了代码冗余，提高了代码的**复用性**。
* 继承的出现，更有利于功能的**扩展**。
*  继承的出现让类与类之间产生了关系，提供了多态的前提。

（不要仅为了获取其他类中某个功能而去继承）

### 子类继承父类后有哪些不同

1体现：一旦子类A继承父类B以后，子类A中就**获取了父类B中声明的所有的属性和方法**。

 * 特别的，**父类中声明为private的属性或方法**，子类继承父类以后，仍然认为**获取了**父类中私有的结构。**只因为封装性**的影响，**使得子类不能直接调用父类的结构而已**。

   ​	(注：使用this访问属性和方法时，如果在本类中未找到，也会从父类中查找)

3.2 子类继承父类以后，**还可以声明自己特有的属性或方法**：实现功能的**拓展**。

 * 子类和父类的关系，不同于子集和集合的关系。(**不是"包含",而是扩展**)
 * extends：延展、扩展

### 类的继承的规则

  (1)**子类不能直接访问父类中私有的(private)的成员变量和方法**。

   子类继承了**所有**的属性和方法，非私有的属性和方法可以在子类直接访问, 但是**私有属性和方法不能在子类直接访问，要通过父类提供公共的方法去访问**。

  (2)Java只支持**单继承**和**多层继承**，**不允许多重继承**

* 单继承：**一个子类只能有一个父类**，一个父类可以派生出多个子类。区别于多重继承(可以有多个父类)。

* 多层继承：子类直接继承的父类，称为直接父类。间接继承的父类称为**间接父类**(子父类是相对的概念)。**子类继承父类以后，就获取了直接父类以及所间接父类中声明的属性和方法**。(注意：层次结构不可以循环)

```java
class SubClass extends SuperClass{};//单继承

class B extends A{};
class C extends B{};//多层继承 C继承B，B继承A。 B是C的直接父类 A是C的间接父类

class A extends B{}
class B extends A{}//错 继承的层次结构不可以循环

class C extends A,B{};//错 这是多重继承
```

### java.lang.Object类的理解

1. 如果我们没显式的声明一个类的父类的话，则此类继承于java.lang.Object类
2. 所的java类（除java.lang.Object类之外）**都直接或间接的继承于java.lang.Object类**
3. 意味着，所的java类具有java.lang.Object类声明的功能。

## 方法的重写(override)

### 什么是方法的重写(override 或 overwrite)？

子类继承父类以后，可以对父类中同名同参数的方法，进行覆盖操作.

### 重载的应用

重写以后，当创建子类对象以后，通过子类对象调用子父类中的同名同参数的方法时，**实际执行的是子类重写父类的方法。**

### 举例：

```java
class Circle{//圆
public double findArea(){}//求面积
}
class Cylinder extends Circle{//圆柱
public double findArea(){}//求表面积
}
***************
class Account{//账户 里面的钱是余额
public boolean withdraw(double amt){}//取钱
}
class CheckAccount extends Account{//可透支账户 余额+可透支额度
public boolean withdraw(double amt){}
}
```

### 重写的规则

 方法的声明

权限修饰符  返回值类型  方法名(形参列表) throws 异常的类型{
//方法体
}

  约定俗称：子类中的叫重写的方法，父类中的叫被重写的方法
① 子类重写的方法的**方法名和形参列表**与父类被重写的方法的方法名和形参列表**相同**。（方法签名相同）
② 子类重写的方法的**权限修饰符不小于父类**被重写的方法的权限修饰符（**修饰符：子>=父**)（**子类方法不能缩小父类方法的访问权限**）

 >特殊情况：子类**不能重写父类中声明为private权限的方法**

③ 返回值类型：**父：void、基本——子：相同；父：引用A类——子：A类或A类的子类**
 >父类被重写的方法的返回值类型是**void**，则子类重写的方法的返回值类型**只能是void**
 >父类被重写的方法的返回值类型是引用数据类型**A类型**，则子类重写的方法的返回值类型可以是**A类或A类的子类** （引用数据类型的返回值 子<=父）
 >父类被重写的方法的返回值类型是基本数据类型(比如：double)，则子类重写的方法的返回值类型**必须是相同的基本数据类型**(必须也是double)

④ 子类重写的方法抛出的**异常类型不大于父类**被重写的方法抛出的异常类型（具体放到异常处理时候讲）(**异常类型 子<=父** )

 ⑤ 子类和父类中的同名同参数的方法要么都声明为非static的（考虑重写），要么都声明为static的（不是重写)。（**静态方法不能重写**）

### 面试题：区分方法的重写和重载？

答：
① 二者的概念
② 重载和重写的具体规则
③ 重载：不表现为多态性。
  重写：表现为多态性。
重载，是指允许存在多个同名方法，而这些方法的参数不同。编译器根据方法不同的参数表，对同名方法的名称做修饰。对于编译器而言，这些同名方法就成了不同的方法。它们的调用地址在编译期就绑定了。Java的重载是可以包括父类和子类的，即子类可以重载父类的同名不同参数的方法。
所以：对于重载而言，在方法调用之前，编译器就已经确定了所要调用的方法，这称为“早绑定”或“静态绑定”；

而对于多态，只等到方法调用的那一刻，解释运行器才会确定所要调用的具体方法，这称为“晚绑定”或“动态绑定”。 

引用一句Bruce Eckel的话：“不要犯傻，如果它不是晚绑定，它就不是多态。”



## 关键字：super

super 关键字可以理解为："父类的"

在Java类中使用super来调用父类中的指定操作：

* super可用于子类访问**父类中定义的属性、成员方法**

* super可用于在**子类构造器中调用父类的构造器**

注意：
  * 尤其当子父类出现同名成员时，可以用super表明调用的是父类中的成员
  * **super的追溯不仅限于直接父类**
  * super和this的用法相像，this代表本类对象的引用，super代表父类的内存空间的标识

### super调用属性、方法：

可以在子类的方法或构造器中，使用"**super.属性**"或**"super.方法**"的方式，显式的调用父类中声明的属性或方法。但是，通常情况下，我们习惯省略"super."

* 特殊情况：当**子类和父类中定义了同名的属性时**，我们要**想在子类中调用父类中声明的属性**，则必须显式的使用"super.属性"的方式，表明调用的是父类中声明的属性。
* 特殊情况：当**子类重写了父类中的方法以后**，我们**想在子类的方法中调用父类中被重写的方法**时，则必须显式的使用"super.方法"的方式，表明调用的是父类中被重写的方法。

```java
  public class SuperTest {
  	public static void main(String[] args) {
  		Student stu = new Student();
  		stu.testShow();
  	}
  }
  class Person {
  	int id=1234567890;//身份证号
  	void show() {
  		System.out.println("父类的show()");
  	}
  
  }
  class Student extends Person{
  	int id=202207;//学号
  	void testShow() {
  		System.out.println(id);
  		System.out.println(super.id);
  		show();
  		super.show();
  	}
  	@Override
  	void show() {
  		System.out.println("子类的show()");
  	}
  }
```

### super()调用父类的构造器

4.1  可在子类的构造器中显式的使用"super(形参列表)"的方式，调用父类中声明的指定的构造器
4.2 "super(形参列表)"的使用，必须声明在子类构造器的**首行**！
4.3 在类的构造器中，针对于"this(形参列表)"或"super(形参列表)"只能二选一，不能同时出现
4.4 在构造器的首行，没显式的声明"this(形参列表)"或"super(形参列表)"，则默认调用的是父类中空参构造器：super()
4.5 在类的多个构造器中，至少一个类的构造器中使用了"super(形参列表)"，调用父类中的构造器

注意：

* 子类中所有的构造器默认都会访问父类中空参数的构造器。(**子类的构造器里隐含一个super()**)

  （个人理解：联系以前的知识点：**所有类中会有隐式的空参构造器; 子类的所有构造器中会有隐式的super()**）

* 当**父类中没有空参数的构造器时**，子类的构造器**必须通过this(参数列表)或者super(参数列表)语句**指定调用本类或者父类中相应的构造器。同时，只能”**二选一**”，且**必须放在构造器的首行**

  个人理解：因为子类的构造器里隐含一个super()，但是父类没有空参的。就需要在子类的构造器里显式的super(参数列表)来调用父类的有参构造器。或者是this(参数列表)来调用其它的子类构造器(其它的子类构造器中含super(参数列表))。总体思想是 让子类去调用父类的有参构造而不是无参构造(因为没无参构造)。

* 如果子类构造器中既未显式调用父类或本类的构造器，且父类中又没有无参的构造器，则编译出错。
```java
  class Person {
  	int id;//身份证号
  	//显式定义父类构造器，隐式空参构造器就无了
  	Person(int id){
  		this.id=id;
  	}
  }
  class Student extends Person{
  	int id;//学号
  	//Student(){}//再显式定义一个空参构造器会报错！！ 因为子类的构造器里隐含一个super()，但是父类没有空参的。
  	//若没有显式定义子类构造器，隐式空参构造器去调用隐含的super()。但父类没有空参构造器无影响，就会报错！
  	
  	//若显式定义子类构造器(里面是有参的super(参数列表))，隐式空参构造器就无了，不会去调用隐含的super()。故父类没有空参构造器无影响
  	Student(int id) {
  		super(id);
  	}
  	Student(int id,int id2) {
  		this(id);//这里也可以写super(id),二选一。this(id)是调用Student(id),里面再调用super(id)
  		this.id=id2;
  	}
  }
```

  

### this和super的区别

| 区别点     | this                                                   | super                                    |
| ---------- | ------------------------------------------------------ | ---------------------------------------- |
| 访问属性   | 访问本类中的属性，如果本类没有此属性则从父类中继续查找 | 直接访问父类中的属性                     |
| 调用方法   | 访问本类中的方法，如果本类没有此方法则从父类中继续查找 | 直接访问父类中的方法                     |
| 调用构造器 | 调用本类构造器，必须放在构造器的首行                   | 调用父类构造器，必须放在子类构造器的首行 |


## 子类对象实例化过程
1. 从结果上看：继承性

 * 子类继承父类以后，就获取了父类中声明的属性或方法。
 * 创建子类的对象，在**堆空间中，就会加载所父类中声明的属性**。
   ![](http://101.34.218.64/JavaSE.assets/%E5%AD%90%E7%B1%BB%E5%AF%B9%E8%B1%A1%E7%9A%84%E5%AE%9E%E4%BE%8B%E5%8C%96%E8%BF%87%E7%A8%8B%E7%A4%BA%E6%84%8F%E5%9B%BE.png)

2. 从过程上看：
 当我们通过子类的构造器创建子类对象时，我们**一定会直接或间接的调用其父类的构造器，进而调用父类的父类的构造器**，...**直到调用了java.lang.Object类中空参的构造器为止**。正因为加载过所的父类的结构，所以才可以看到内存中父类中的结构，子类对象才可以考虑进行调用。

![](http://101.34.218.64/JavaSE.assets/%E5%AD%90%E7%B1%BB%E5%AF%B9%E8%B1%A1%E7%9A%84%E5%AE%9E%E4%BE%8B%E5%8C%96%E8%BF%87%E7%A8%8B.png)

虽然创建子类对象时，调用了父类的构造器，但是自**始至终就创建过一个对象，即为new的子类对象**。

为什么super(...)和this(...)调用语句不能同时在一个构造器中出现？因为他们都要放在构造器的首行
为什么super(...)和this(...)调用语句只能作为构造器中的第一句出现？无论通过哪个构造器构建子类对象，需要保证先初始化父类。目的;当子类继承父类后，“继承”父类中所有的属性和方法，因此子类有必要知道父类如何为对象进行初始化。

## OOP特征三：多态性
### 多态性的理解：
可以理解为一个事物的多种形态。

### 方法的多态(了解)
重载和重写体现多态。
* 方法重载（overload）实现的是编译时的多态性（也称为前绑定、静态多态）
  传入不同的参数列表，就决定调用不同的方法。

* 而方法重写（override）实现的是运行时的多态性（也称为后绑定、动态多态）。
  重写的方法和被重写的方法方法签名完全一致，只能在运行时通过传入的实例来动态决定

> 补充知识：方法签名:方法名称+参数列表(包括参数顺序和类型) 

   运行时的多态是面向对象最精髓的东西。
重写是多态，但重载是不是多态没有定论。按照目前计算机科学领域主流的定义，重载属于多态。但在Java中，多态往往指的是动态多态。

### 对象的多态(重要)

**父类的引用指向子类的对象（子类的对象赋给父类的引用**）——**向上转型**(upcasting)
  (可以直接应用在抽象类和接口上)
一个变量只能有一种确定的数据类型
一个引用类型变量可能指向(引用)多种不同类型的对象）



### 多态性的使用细节：

虚拟方法(虚方法)调用

子类中定义了与父类同名同参数的方法，在**多态情况下，将此时父类的方法称为虚拟方法**，父类根据赋给它的不同子类对象，动态调用属于子类的该方法。这样的方法调用在编译期是无法确定的。
```java
父类 变量=new 子类();
Animal animal = new Dog();
animal.shout();//汪汪  （执行的Dog类里的shout方法）

另一种方式：方法声明的形参类型为父类类型，可以使用子类的对象作为实参调用该方法
public void shout(Animal animal){
    animal.shout();
}
调用时
    Animal animal = new Animal();
    animal.shout(new Dig());//汪汪 里面的传参过程相当于Animal animal = new Dog();
    animal.shout(new Cat());//喵喵
```
有了对象的多态性以后，我们在**编译期，只能调用父类中声明的方法**，但在**运行期**，我们**实际执行的是子类重写父类的方法**。

> 可以调用父类中的所有成员(需要遵守访问权限)(如果是被重写的方法，实际运行时执行的是子类重写的方法) ；**不能调用子类中的特有成员**
>
> 对象的多态性，只适用于方法，**不适用于属性（编译和运行都看左边）**。
>
> ```java
> public class Test2 {
> 	public static void main(String[] args) {
> 		Person p=new Student();
> 		System.out.println(p.name);//null 父类有
> 		System.out.println(p.id);//1 父类有 虽然子类特有 但重名
> 		//System.out.println(p.grade);//编译报错 父类中没有,子类特有
> 		p.showId();//子类的id：2    重写，而且重写方法里的访问的是子类的属性
> 		//p.showId1();//编译报错 父类中没有 子类特有
> 		
> 	}
> }
> class Person {
> 	int id=1;//身份证号
> 	String name="小明";
> 	void showId(){
> 		System.out.println("父类的id："+id);
> 	}
> }
> class Student extends Person{
> 	int id=2;//学号	子类特有的成员 只是同名了
> 	int grade;//年级 子类特有的成员
> 	@Override
> 	void showId(){//重写的方法
> 		System.out.println("子类的id："+id);
> 	}
> 	void showId1() {//子类特有的
> 		System.out.println("(showId1)子类的id："+id);
> 	}
> }
> ```
>
> ![](http://101.34.218.64/JavaSE.assets/%E5%A4%9A%E6%80%81%E6%80%A7%E4%B8%8D%E9%80%82%E7%94%A8%E4%BA%8E%E5%B1%9E%E6%80%A7.png)
>
> （个人总结）**多态情况下**的调用：
>
> | 成员 | 父类有，子类没有 | 父类有，子类有(重名)       | 父类没有，子类有(子类特有) |
> | ---- | ---------------- | -------------------------- | -------------------------- |
> | 属性 | 父类             | 调父类的(子类重名的算特有) | 编译报错                   |
> | 方法 | 父类             | 调子类的(重写)             | 编译报错                   |
> 总结：**属性只调父类的**。编译和运行都看左边
> 		**方法也只调父类的，但遇到被重写方法要执行子类的重写方法**，而且重写方法里可以访问子类的属性
>
> (实际开发中，避免子类和父类中定义同名属性)

>若子类重写了父类方法，就意味着子类里定义的方法**彻底覆盖**了父类里的同名方法，系统将不可能把父类里的方法转移到子类中。
>对于实例变量则不存在这样的现象，即使子类里定义了与父类完全相同的实例变量，这个实例变量依然不可能覆盖父类中定义的实例变量

> Java引用变量有两个类型：编译时类型和运行时类型。
> 编译时类型由声明该变量时使用的类型决定(静态绑定、前期绑定)；
> 运行时类型由实际赋给该变量的对象决定（动态绑定、后期绑定）。

> 总结：**编译，看左边；运行，看右边。**

### 多态性的使用前提：

① 类的继承关系(或对于接口来说，是实现关系)  ② 方法的重写

### 多态性的引用举例

```java
举例一：
	public void func(Animal animal){//func(new Dog())相当于Animal animal = new Dog();
		animal.eat();
		animal.shout();
	}
举例二：
public void method(Object obj){//根父类Object作为形参类型 传入具体的对象类型 调不同的重写方法
		
	}
举例三：
class Driver{
	public void doData(Connection conn){//对于不同的数据库有不同的连接方法，conn = new MySQlConnection(); 或conn = new OracleConnection();等
		//规范的步骤去操作数据
//		conn.method1();
//		conn.method2();
//		conn.method3();
		
	}
}
```

### 多态小总结

多态作用：提高了代码的通用性，常称作接口重用
 前提：需要存在继承或者实现关系；有方法的重写
 成员方法：
* 编译时：要查看引用变量所声明的类中是否有所调用的方法。
* 运行时：调用实际new的对象所属的类中的重写方法。  

成员变量：不具备多态性，只看引用变量所声明的类

### 多态的面试题

谈谈你对多态性的理解？
① 实现代码的通用性。
② Object类中定义的public boolean equals(Object obj){  }
  JDBC:使用java程序操作(获取数据库连接、CRUD)数据库(MySQL、Oracle、DB2、SQL Server)
③ 抽象类、接口的使用肯定体现了多态性。（抽象类、接口不能实例化）

多态是编译时行为还是**运行时行为**？

### 向下转型downcasting

关于向上转型与向下转型：

* 向上转型： 多态

* 向下转型： (子)父类的引用 // 一般是指向子类对象的父类的引用

为什么使用向下转型：
  有了对象的多态性以后，内存中实际上是加载了子类特有的属性和方法的，但是由于变量声明为父类类型，导致编译时，只能调用父类中声明的属性和方法。子类特有的属性和方法不能调用。如何才能调用子类特有的属性和方法？使用向下转型。

如何实现向下转型：使用强制类型转换符：()  对象的强制类型转换也叫造型

>从子类到父类的类型转换可以自动进行
>从父类到子类的类型转换必须通过造型(强制类型转换)实现
>无继承关系的引用类型间的转换是非法的
>在造型前可以使用instanceof操作符测试一个对象的类型

使用时的注意点：

  * 使用强转时，可能出现ClassCastException的异常。
  * 为了避免在向下转型时出现ClassCastException的异常，我们在向下转型之前，先进行instanceof的判断，一旦返回true，就进行向下转型。如果返回false，不进行向下转型。
  > instanceof的使用：
  ① a instanceof A:判断对象a是否是类A的实例。如果是，返回true；如果不是，返回false。

  ② 若类B是类A的父类，如果 a instanceof A返回true,则 a instanceof B也返回true.(**“子类对象 instanceof 间接父类”也可以**)
  ③ 要求a所属的类与类A必须是子类和父类的关系，否则编译错误。(无继承关系的引用类型间的转换是非法的)

```java
public class Test {
    public static void main(String[] args) {
        B a = new A();
        //a.haha();//父类型不能调用子类特有的方法 报错
        if (a instanceof A) {
            A a2 = (A) a; //向下转型
            a2.haha();
        }
    }
}
class B { }
class A extends B { void haha(){System.out.println("哈哈");} }
```

```java
public class DowncastTest {
	public static void main(String[] args) {
		//1.运行通过
		//①子类对象->父类引用->强转为子类类型
		Person p=new Man();
		Man m=(Man)p;
		//②子类对象->间接父类引用->强转为直接父类或子类类型
		Object obj=new Man();
		Person p2=(Person)obj;
		Man p3=(Man)obj;
		
		//2.编译时通过 运行时不通过
		//①子类对象->父类引用->强转为另一个子类
		//Person p4 = new Woman();
		//Man m2=(Man)p4;
		//②父类对象->父类引用->强转为子类
		//Person p5 = new Person();
		//Man m3=(Man)p4;
		
		//3.编译不通过
		//Man m4=new Woman();//类型不匹配
	}
}
class Person{}
class Man extends Person{}
class Woman extends Person{}
```

一个技巧 如果不是XXX的实例： if (!(o instanceof XXX)){  }

学到一个随机数小技巧：int n=new Random().nextInt(3);//返回0或1或2的随机数

## Object类

1. **Object类是所有Java类的根父类**

数组也作为Object类的子类出现，可以调用Object中声明的方法

2. 如果在类的声明中**未使用extends关键字指明**其父类，则**默认父类为java.lang.Object类**

```java
public class Person {
...
}
等价于：
public class Person extends Object {
...
}

method(Object obj){…} //可以接收任何类作为其参数
```


3. Object类中的功能(属性、方法)就具通用性。

 * **属性：无**
 * 方法：
    equals() / toString()这两个重点讲

  getClass()学反射的时候讲 /hashCode() 学集合的时候讲/ clone() 用的少/ finalize()交给垃圾回收机制
     
  wait() 、 notify()、notifyAll() 多线程的时候讲

4. Object类**只声明了一个空参的构造器**


Object类中的主要结构

| 方法名称                          | 类型 | 描述           |
| --------------------------------- | ---- | -------------- |
| public Object()                   | 构造 | 构造器         |
| public boolean equals(Object obj) | 普通 | 对象比较       |
| public int hashCode()             | 普通 | 取得Hash码     |
| public String toString()          | 普通 | 对象打印时调用 |

> API中的方法
>
> | 方法                                | 功能                                                         |
> | ----------------------------------- | ------------------------------------------------------------ |
> | protected Object clone()            | 创建并返回此对象的一个副本。                                 |
> | boolean equals(Object obj)          | 指示其他某个对象是否与此对象“相等”。                         |
> | protected void  finalize()          | 当垃圾回收器确定不存在对该对象的更多引用时，由对象的垃圾回收器调用此方法。 |
> | Class<?> getClass()                 | 返回此 Object 的运行时类。                                   |
> | int hashCode()                      | 返回该对象的哈希码值。                                       |
> | void  notify()                      | 唤醒在此对象监视器上等待的单个线程。                         |
> | void  notifyAll()                   | 唤醒在此对象监视器上等待的所有线程。                         |
> | String toString()                   | 返回该对象的字符串表示。                                     |
> | void  wait()                        | 在其他线程调用此对象的 notify() 方法或 notifyAll() 方法前，导致当前线程等待。 |
> | void wait(long timeout)             | 在其他线程调用此对象的 notify() 方法或 notifyAll() 方法，或者超过指定的时间量前，导致当前线程等待。 |
> | void  wait(long timeout, int nanos) | 在其他线程调用此对象的 notify() 方法或 notifyAll() 方法，或者其他某个线程中断当前线程，或者已超过某个实际时间量前，导致当前线程等待。 |

>垃圾回收机制关键点
>垃圾回收机制只回收JVM堆内存里的对象空间。
>对其他物理连接，比如数据库连接、输入流输出流、Socket连接无能为力
>现在的JVM有多种垃圾回收实现算法，表现各异。
>垃圾回收发生具有不可预知性，程序无法精确控制垃圾回收机制执行。
>可以将对象的引用变量设置为null，暗示垃圾回收机制可以回收该对象。
>程序员可以通过System.gc()或者Runtime.getRuntime().gc()来通知系统进行垃圾回收，会有一些效果，但是系统是否进行垃圾回收依然不确定。
>垃圾回收机制回收任何对象之前，总会先调用它的finalize方法（如果覆盖该方法，让一个新的引用变量重新引用该对象，则会重新激活对象）。
>永远不要主动调用某个对象的finalize方法，应该交给垃圾回收机制调用。

### equals方法

#### 回顾 == 运算符的使用

== 是运算符，可以使用在基本数据类型变量和引用数据类型变量中
 * 如果比较的是基本数据类型变量：比较两个变量保存的**数据**是否相等。（不一定类型要相同）
 * 如果比较的是引用数据类型变量：比较两个对象的**地址值**是否相同.即两个引用是否指向同一个对象实体

补充： == 符号使用时，必须保证符号左右两边的变量类型一致(可自动转换的基本数据类型除外)。

```java
int i=10;
int j=10;
double d=10;
char c=10
sout(i==j);//true
sout(i==d);//true
sout(i==c);//true
```

#### equals方法的使用

  1. 是一个方法，而非运算符
  2. 只能适用于引用数据类型
  3. Object类中equals()的定义：
```java
public boolean equals(Object obj) {
	return (this == obj);
}
```
  说明：**Object类中定义的equals()和==的作用是相同的**：比较**两个对象的地址值是否相同**.即两个引用是否指向同一个对象实体

  4. 像**String、Date、File、包装类等都重写了Object类中的equals()方法**。重写以后，比较的不是两个引用的地址是否相同，而是**比较两个对象的"实体内容"是否相同**。

  5. 通常情况下，我们自定义的类如果使用equals()的话，也通常是比较两个对象的"实体内容"是否相同。那么，我们就需要对Object类中的equals()进行重写.
     重写的原则：比较两个对象的实体内容是否相同.
     
     >重写equals()方法的原则 
     >对称性：如果x.equals(y)返回是“true”，那么y.equals(x)也应该返回是“true”。
     >自反性：x.equals(x)必须返回是“true”。
     >传递性：如果x.equals(y)返回是“true”，而且y.equals(z)返回是“true”，那么z.equals(x)也应该返回是“true”。
     >一致性：如果x.equals(y)返回是“true”，只要x和y内容一直不变，不管你重复x.equals(y)多少次，返回都是“true”。
     >任何情况下，x.equals(null)，永远返回是“false”；
     >x.equals(和x不同类型的对象)永远返回是“false”。

#### 如何重写equals()

手动重写举例：
```java
class User{
String name;
int age;
	//重写其equals()方法
	public boolean equals(Object obj){
		if(obj == this){
			return true;
		}
		if(obj instanceof User){
			User u = (User)obj;
			return this.age == u.age && this.name.equals(u.name);
		}
		return false;
	}
}
```

开发中如何实现：自动生成的 eclipse——源码——生成hashCode()和equals()



### toString()方法

#### toString()的使用

  1. 当我们输出一个对象的引用时，实际上就是调用当前对象的toString()
 2. Object类中toString()的定义：toString()方法在Object类中定义，其返回值是String类型，返回:类名@它的引用地址。
   ```java
public String toString() {
        return getClass().getName() + "@" + Integer.toHexString(hashCode());
     }
   ```

  3. 像String、Date、File、包装类等都重写了Object类中的toString()方法。
     使得在调用对象的toString()时，返回"实体内容"信息
     
     ```java
     //String 类重写了toString()方法，返回字符串的值。
     s1=“hello”;
     System.out.println(s1);//相当于System.out.println(s1.toString());
     
     //在进行String与其它类型数据的连接操作时，自动调用toString()方法
     Date now=new Date();
     System.out.println(“now=”+now); 
     //相当于System.out.println(“now=”+now.toString());//Date中重写的toString()
     
     //基本类型数据转换为String类型时，调用了对应包装类的toString()方法
     int a=10;
     System.out.println(“a=”+a);//包装类的toString()
     ```
     
     
     
  4. 自定义类也可以重写toString()方法，当调用此方法时，返回对象的"实体内容"
#### 如何重写toString()
举例：
```java
//自动实现
	@Override
	public String toString() {
		return "Customer [name=" + name + ", age=" + age + "]";
	}
```

面试题：

① final、finally、finalize的区别？
②  == 和 equals() 区别



字符串忽略大小写比较   "hello".equalsIgnoreCase("Hello");

## 补充：单元测试方法

 Java中的JUnit单元测试
 （以eclipse为例）
 步骤：
 1.选中当前工程 - 右键选择：build path - add libraries - JUnit 4 - 下一步
 2.创建Java类，进行单元测试。
   此时的Java类要求：① 此类是public的  ②此类提供公共的无参的构造器
 3.此类中声明单元测试方法。
   此时的单元测试方法：方法的权限是public,没返回值，没形参。(一般习惯上测试方法的方法名为testXxx)
 4.此单元测试方法上需要声明注解：@Test,并在单元测试类中导入：import org.junit.Test;
 5.声明好单元测试方法以后，就可以在方法体内测试相关的代码。
 6.写完代码以后，左键双击单元测试方法名，右键：run as - JUnit Test
```java
import org.junit.Test;
// java中的JUnit单元测试
public class JUnitTest {
	int num;
	@Test
	public void testEquals() {// 选中测试方法 然后运行 不需要改main方法
		String s1 = "MM";
		String s2 = "MM";
		System.out.println(s1.equals(s2));
		System.out.println(num);// 不用造对象就可以调用类里属性 其实是里面省略this的情况
		show();// 可以不造对象调用方法
	}
	public void show() {// 可以定义方法
		num = 20;
		System.out.println(num);
	}
	
	@Test
	public void testPrintln() {// 可以定义多个测试方法 想执行哪个选中哪个
		System.out.println("haha");
	}
}
```

 说明：在Console可以看到结果，在JUnit可以看到条的颜色
 1.如果执行结果没任何异常：绿条
 2.如果执行结果出现异常：红条

## 包装类Wrapper Class

也叫封装类

### 为什么要有包装类

为了使基本数据类型的变量具有类的特征，引入包装类。（就可以具有类的特征，调用方法了）

如：类Inerger 里面属性是int value，

基本数据类型包装成包装类的实例——装箱

获取包装类对象中包装的基本类型变量——拆箱

### 基本数据类型与对应的包装类

java提供了8种基本数据类型对应的包装类

| 基本数据类型 | 包装类**（位于java.lang包中）** |
| :----------: | :-----------------------------: |
|     byte     |              Byte               |
|    short     |              Short              |
|     int      |           **Integer**           |
|     long     |              Long               |
|    float     |              Float              |
|    double    |             Double              |
|   boolean    |             Boolean             |
|     char     |          **Character**          |

（**注意Integer和Character的写法**，别的都是首字母大写即可。）

前6个数值型Byte、Short、Integer、Long、 Float 、Double的**父类是java.lang.Number**

（后面两个java.lang.Character和java.lang.Boolean）



### 装箱和拆箱

#### 装箱

基本数据类型包装成包装类的实例——装箱

~~①通过**包装类的构造器**实现：~~
~~`int i = 500; `~~
~~`Integer t = new Integer(i);`~~
~~②构造器还可以通过**字符串参数**构造包装类对象：~~
~~`Float f = new Float(“4.56”);`~~
~~`Long l = new Long(“asdf”); //NumberFormatException`~~
~~如果字符串参数的内容无法正确转换为对应的基本类型，则会抛出java.lang.NumberFormatException异常~~
③自动装箱

注意：

①从jdk1.9开始就不建议用构造器构建包（构建包：指构造包装类）了，官方推荐使用**valueOf**方法（包装类中的静态方法）来构建包。所以以前用
 `new 包装类构造器(基本数据类型或字符串类型的变量或常量)`
 的地方都可以换成
 **`包装类.valueOf(基本数据类型或字符串类型的变量或常量)`** 

(注意 构造器Character(...) 、Character.valueOf(...)都只能接受char型参数，不可以用String型)

 ```java
 int i = 500; 
//Integer t = new Integer(i);
Integer in = Integer.valueOf(i);
System.out.println(in.toString());//装箱之后可以使用t来调用一些方法了		
		
//Integer in1 = new Integer("123");
Integer in1 = Integer.valueOf("123");
//Integer in2 = new Integer("1abc");//如果字符串参数的内容无法正确转换为对应的基本类型，则会抛出java.lang.NumberFormatException异常
Integer in2 = Integer.valueOf("1abc");//NumberFormatException
		
Float f1 = Float.valueOf(1.23f);
Float f2 = Float.valueOf("1.23f");
		
Boolean b1=Boolean.valueOf(true);
Boolean b2=Boolean.valueOf("true");

//Character ch=new Character('h');
Character ch=Character.valueOf('a');
//Character ch=Character.valueOf("a");//报错 注意对于Character，只能接受char型参数 不可以用String
 ```

②注意包装类属性和基本数据类型的默认值不同！包装类是引用数据类型，默认值是null
```java
	class Test{
	boolean flag;//flase
	Boolean flag;//null
	}
```

#### 拆箱

获取包装类对象中包装的基本类型变量——拆箱

①调用包装类Xxx的.xxxValue()方法

`包装类对象.基本数据类型Value()`

```java
Integer Int = Integer.valueOf("123");
int in = Int.intValue();

Boolean Bool=Boolean.valueOf(true);
Boolean bool = Bool.booleanValue();

Character ch=Character.valueOf('a');
char c=ch.charValue();
```

②自动拆箱

#### 自动装箱和自动拆箱

JDK1.5之后，支持自动装箱，自动拆箱。但类型必须匹配。
> Java以“语法糖”来实现自动装箱与拆箱- -这纯粹由Java语言编译器(例如javac) 实现。
> 当javac发现在一个需要Object、Number、Integer的上下文里出现了int类型的值，就会自动把这个值装箱为Integer,通过Integer.valueOf();
> 反之，在一个需要int的上下文里出现了Integer类型的值的话，就会自动把资格值拆箱为int,通过Integer.intValue()。 其它基本类型同理。

```java
@Test
	public void test2() {
		Integer i = 4;//自动装箱。相当于Integer i = Integer.valueOf(4);
		i = i + 5;//等号右边：将i对象转成基本数值(自动拆箱) i.intValue() + 5;
		//加法运算完成后，再次装箱，把基本数值转成对象。i=Integer.valueOf(i.intValue() + 5)
		System.out.println(i);//9
		
		int j=i;//自动拆箱 相当于int j  = i.intvalueOf();
		System.out.println(j);//9
		
		method(i);//Object
		method(j);//int
		//method方法重载时，两个各找各妈,不发生自动装箱或拆箱;若注释掉任意一个method方法，都不会报错，因为类型不匹配的那个会自动装箱或拆箱
		
		method1(i);//Object
		method1(j);//Object 自动装箱
		method2(i);//int 自动拆箱
		method2(j);//int
	}
	public void method(Object obj) {System.out.println("Object");
          /*// 若在方法里处理数据 可先对obj向下转型。
		if (obj instanceof Integer) {
			Integer in = (Integer) obj;
			int i = in.intValue();//jdk 5.0以后可以直接int i=in;自动拆箱
			// ...
		}*/
	}                
	public void method(int i) {System.out.println("int");}
	public void method1(Object obj) {System.out.println("Object");}
	public void method2(int i) {System.out.println("int");}
```



### String和基本数据类型或包装类之间的转换

```java
//①String——>基本数据类型
String s="100";
int i = Integer.parseInt(s);//包装类的静态方法parseXxx(String)。
//如果字符串参数的内容无法正确转换为对应的基本类型，则会抛出java.lang.NumberFormatException异常。
//除了Character类之外，其他所有包装类都具有parseXxx静态方法可以将字符串参数转换为对应的基本类型
int i2= Integer.valueOf(s);//发生了自动拆箱 相当于Integer temp=Integer.valueOf(s);int i2=temp;

//②基本数据类型——>String
String s1=String.valueOf(i);//String类的静态方法valueOf()。底层是Integer.toString(i)
String s2=i+"";//字符串连接符

//③String——>包装类 
Integer I=Integer.valueOf(s1);//Integer类的静态方法valueOf()

//④包装类——>String
String s3=I.toString();//包装类对象调用toString()
String s4=Integer.toString(I);//包装类的静态toString(形参)
```

包装类在实际开发中用的最多的 ： 字符串变为基本数据类型 （parseXxx(String)方法很重要）

### 三者之间的转换总结

![基本数据类型、包装类和String类间的转化](http://101.34.218.64/JavaSE.assets/%E5%9F%BA%E6%9C%AC%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B%E3%80%81%E5%8C%85%E8%A3%85%E7%B1%BB%E5%92%8CString%E7%B1%BB%E9%97%B4%E7%9A%84%E8%BD%AC%E5%8C%96.png)

重点记忆的：

基本数据类型<--->包装类：JDK 5.0 新特性：自动装箱 与自动拆箱
基本数据类型、包装类--->String:调用String重载的valueOf(Xxx xxx)
String--->基本数据类型、包装类:调用包装类的parseXxx(String s)
     注意：转换时，可能会报NumberFormatException

### 包装类面试题

1.如下两个题目输出结果相同吗？各是什么

```java
@Test
	public void test() {
		Object o1 = true ? new Integer(1) : new Double(2.0);
		System.out.println(o1);//1.0
        //三元运算符后面的表达式1和表达式2要求是一致的。new Integer(1)会自动提升为Double
		Object o2;
		if (true)
		o2 = new Integer(1);
		else
		o2 = new Double(2.0);
		System.out.println(o2);//1
```

2.

```java
public void method1() {
		Integer i = new Integer(1);
		Integer j = new Integer(1);
		System.out.println(i == j);//false new了两个对象
		Integer m = 1;
		Integer n = 1;
		System.out.println(m == n);//true 自动装箱
		Integer x = 128;
		Integer y = 128;
		System.out.println(x == y);//false 自动装箱
    	//内部类IntegerCache有个固定长度的数组Integer cache[],数组中提前存了-128~127(这个范围用的比较高频，只做了-128~127的映射)
		//如果i的值是在-128 到 127 之间就直接在cache缓存数组中去取Integer对象。而不在此范围内的数值则要new到堆中了
		//阿里的代码规范里有一条【强制】所有的相同类型的包装类对象之间值的比较，全部使用 equals 方法比较。
		//说明：对于 Integer var = ? 在-128 至 127 范围内的赋值，Integer 对象是在 IntegerCache.cache 产生，会复用已有对象，这个区间内的 Integer 值可以直接使用==进行 判断，但是这个区间之外的所有数据，都会在堆上产生，并不会复用已有对象，这是一个大坑， 推荐使用 equals 方法进行判断。
		}
```

代码规范：**所有的相同类型的包装类对象之间值的比较，全部使用 equals 方法比较。**

### 应用场景举例：

① Vector类中关于添加元素，只定义了形参为Object类型的方法：
v.addElement(Object obj);   //基本数据类型 --->包装类 --->使用多态



## 课外拓展(了解） native 关键字的理解

使用 native 关键字说明这个方法是原生函数，也就是这个方法是用 C/C++等非
Java 语言实现的，并且被编译成了 DLL，由 java 去调用。
（1）为什么要用 native 方法
java 使用起来非常方便，然而有些层次的任务用 java 实现起来不容易，或者我们
对程序的效率很在意时，问题就来了。例如：有时 java 应用需要与 java 外面的
环境交互。这是本地方法存在的主要原因，你可以想想 java 需要与一些底层系
统如操作系统或某些硬件交换信息时的情况。本地方法正是这样一种交流机制：
它为我们提供了一个非常简洁的接口，而且我们无需去了解 java 应用之外的繁
琐的细节。
（2）native 声明的方法，对于调用者，可以当做和其他 Java 方法一样使用
一个 native method 方法可以返回任何 java 类型，包括非基本类型，而且同样可
以进行异常控制。
native method 的存在并不会对其他类调用这些本地方法产生任何影响，实际上
调用这些方法的其他类甚至不知道它所调用的是一个本地方法。JVM 将控制调用
本地方法的所有细节。
如果一个含有本地方法的类被继承，子类会继承这个本地方法并且可以用 java
语言重写这个方法（如果需要的话）。

# 第6章 面向对象编程(下)

## 关键字：static

static 静态的

有时候希望无论是否产生了对象或无论产生了多少对象的情况下，某些特定的数据在内存空间里只有一份。

### 类属性、类方法的设计思想

实例变量(instance variable)，它属于类的每一个对象，不能被同一个类的不同对象所共享。**如果想让一个类的所有实例共享数据，就用类变量！**

类属性作为该类各个对象之间共享的变量。在设计类时,分析哪些属性**不因对象的不同而改变**，将这些属性设置为类属性。

相应的方法设置为类方法。如果方法与调用者无关，则这样的方法通常被声明为**类方法，由于不需要创建对象就可以调用类方法，从而简化了方法的调用**

### static使用范围

可以用来修饰的结构：主要用来修饰类的内部结构
属性、方法、代码块、内部类

修饰后叫类xx或静态xx： 静态属性\类变量(类属性)  、类方法\静态方法、 静态代码块、 静态内部类

### **被修饰后的成员具备以下特点：**

* 随着类的加载而加载
* 优先于对象存在
* 修饰的成员，被所有对象所共享
* 访问权限允许时，可不创建对象，直接被类调用

### 静态变量（或类变量）

static修饰属性

（1）属性，是否使用static修饰，又分为：静态属性  vs 非静态属性(实例变量)
* 实例变量：我们创建了类的多个对象，每个对象都独立的拥一套类中的非静态属性。当修改其中一个对象中的非静态属性时，不会导致其他对象中同样的属性值的修改。
* 静态变量：我们创建了类的多个对象，**多个对象共享同一个静态变量**。当通过某一个对象修改静态变量时，会导致其他对象调用此静态变量时，是修改过了的。

 (2) static修饰属性的其他说明：
  ① **静态变量随着类的加载而加载**。可以通过"**类.静态变量**"的方式进行调用
  ② **静态变量的加载要早于对象的创建。**
  ③ 由于类只会加载一次，则静态变量**在内存中也只会存在一份**：存在**方法区的静态域**中。
  ④权限允许时，类变量可以由类或对象调用，实例变量由对象调用

|      | 类变量 | 实例变量 |
| ---- | ------ | -------- |
| 类   | yes    | no       |
| 对象 | yes    | yes      |

(3) 静态属性举例：System.out; Math.PI;

(4) 静态变量内存解析

 由于类只会加载一次，则静态变量**在内存中也只会存在一份**：存在**方法区的静态域**中。

![静态变量内存解析](http://101.34.218.64/JavaSE.assets/%E9%9D%99%E6%80%81%E5%8F%98%E9%87%8F%E5%86%85%E5%AD%98%E8%A7%A3%E6%9E%90.png)

### 静态方法(或类方法)

static修饰方法：静态方法、类方法
① 随着类的加载而加载，可以通过"类.静态方法"的方式进行调用
②访问权限允许的情况下，静态方法可以被类或对象调用，非静态方法只能被对象调用

|      | 静态方法 | 非静态方法 |
| ---- | -------- | ---------- |
| 类   | yes      | no         |
| 对象 | yes      | yes        |

③ **静态方法中可以直接调用静态方法或属性，但不能直接调用非静态方法或属性(需要通过对象来访问)**

>因为静态方法是属于类的，动态方法属于实例对象，动态方法只有在对象实例化之后才存在，
>如果静态方法能调用动态方法的话，那如果别人通过类名调用静态方法时实例对象可能并不存在，但是方法内又调用了对象的方法，由于对象不存在，所以动态方法也不存在，程序肯定报错，所以java直接在编译阶段检查这种错误，避免运行时异常
>http://zhidao.baidu.com/question/365105825696817172/answer/2721286602

   非静态方法中，既可以调用非静态的方法或属性，也可以调用静态的方法或属性

```java
public class TestStatic {
	int i;
	static int j;
	public void f1() {}
	public static void f2() {}
	public static void main(String[] args) {
		//f1();//报错 不能对非静态方法 f1（）进行静态引用
		new TestStatic().f1();//可以通过对象来访问非静态方法
		f2();//都是静态的,属于同一类，就可以省略类名，直接通过方法名调用
		
		//System.out.println(i);//报错 不可以调用非静态属性
		new TestStatic().f1();//可以通过对象来访问非静态方法
		System.out.println(j);//可以调用静态属性
		
		//Test.f3();//报错 不能对非静态方法 f3（）进行静态引用
		new Test().f3();
		Test.f4();
		//System.out.println(Test.a);//报错
		System.out.println(Test.b);
	}
}
class Test{
	int a;
	static int b;
	public void f3() {System.out.println(a);System.out.println(b);}
	public static void f4() {
		//System.out.println(a);
		//System.out.println(this.b);//不能用this
		System.out.println(b);}
}
```



④在静态的方法内，**不能使用this关键字、super关键字**

⑤static修饰的方法**不能被重写**

### static的注意点：

* **在静态的方法内，不能使用this关键字、super关键字**

* 关于静态属性和静态方法的使用，大家都从**生命周期的角度**去理解。

  静态的成员和类的加载和消亡是同步的，动态的成员和对象的加载和消亡是同步的

  (Java类加载机制的七个阶段:加载、验证、准备、解析、初始化、使用、销毁)

### 开发中，如何判定属性和方法应该使用static关键字：

属性：
1.属性是可以**被多个对象所共享的**，不会随着对象的不同而不同的。
2.**类中的常量(用final修饰的)**也常常声明为static。public static final myPI = 3.14;

方法：
1.**操作静态属性的方法**，通常设置为static的
2.**工具类中的方法**，习惯上声明为static的。 比如：Math、Arrays、Collections

### 使用举例

使用举例：
举例一：Arrays、Math、Collections等工具类
举例二：单例模式
举例三：

```java
class Circle{
	
	private double radius;
	private int id;//自动赋值
	
	public Circle(){
		id = init++;
		total++;
	}
	
	public Circle(double radius){
		this();
//		id = init++;
//		total++;
		this.radius = radius;	
	}
	
	private static int total;//记录创建的圆的个数
	private static int init = 1001;//static声明的属性被有对象所共享
	
	public double findArea(){
		return 3.14 * radius * radius;
	}

	public double getRadius() {
		return radius;
	}

	public void setRadius(double radius) {
		this.radius = radius;
	}

	public int getId() {
		return id;
	}

	public static int getTotal() {
		return total;
	}
}
```

还有设置一个静态变量 这样 每次新生成对象 +1   都会有唯一id

## 单例(Singleton)设计模式

### 设计模式是什么

设计模式是在大量的实践中总结和理论化之后优的代码结构、编程风格、以及解决问题的思考方式。

设计模式共23种：

* 创建型模式，共5种：

  工厂方法模式、抽象工厂模式、单例模式、建造者模式、原型模式

* 结构型模式，共7种：

  适配器模式、装饰器模式、代理模式、外观模式、桥接模式、组合模式、享元模式

* 行为型模式，共11种：

  策略模式、模板方法模式、观察者模式、迭代子模式、责任链模式、命令模式、备忘录模式、状态模式、访问者模式、中介者模式、解释器模式。

### 单例模式

所谓类的单例设计模式，就是采取一定的方法保证在整个的软件系统中，对**某个类只能存在一个对象实例**。

**保证一个类仅有一个实例，并提供一个访问它的全局访问点。**

单例模式的**关键代码**：**构造函数是私有的**。(可参考[菜鸟教程-单例模式](https://www.runoob.com/design-pattern/singleton-pattern.html))

首先必须将**类的构造器的访问权限设置为private**，这样，就不能用new操作符在类的外部产生类的对象了，但在类内部仍可以产生该类的对象。因为在类的外部开始还无法得到类的对象，**只能调用该类的某个静态方法以返回类内部创建的对象**，静态方法只能访问类中的静态成员变量，所以，**指向类内部产生的该类对象的变量也必须定义成静态的**。

#### 懒汉式和饿汉式

```java
public class SingletonTest {
	public static void main(String[] args) {
		Singleton instance1=Singleton.getInstance();
		Singleton instance2=Singleton.getInstance();
		System.out.println(instance1==instance2);//true
	}
}
/*单例模式-饿汉式*/
class Singleton{
	private static Singleton instance=new Singleton();
	//内部创建类对象,指向类内部产生的该类对象的变量也必须定义成静态的
	
	private Singleton(){//构造器的访问权限必须是private
	}
	
	public static Singleton getInstance() {//提供公共的、静态的方法，返回类的对象
		return instance;
	}
}
```

```java
/*
 * 单例模式-懒汉式 
 *懒汉式暂时还存在线程安全问题，学了多线程后，可改进
 */
class Singleton {
	private static Singleton instance;
	// 声明静态的当前类的对象，不初始化——懒汉式和饿汉式的区别

	private Singleton() {// 构造器的访问权限必须是private
	}

	public static Singleton getInstance() {// 提供公共的、静态的方法，返回类的对象
		if (instance == null)instance = new Singleton();//在方法中创建对象 初始化
		return instance;
	}
}
```

饿汉——一上来就迫不及待的造好对象——加载类时就初始化

懒汉——什么时候用什么时候造——方法调用的时候

两种方式的对比：

饿汉式：	
 * 坏处：对象加载时间过长。
 * 好处：饿汉式是线程安全的


懒汉式：
 * 好处：延迟对象的创建。
 * 目前的写法坏处：线程不安全。--->到多线程内容时，再修改

#### 单例模式的优缺点

**优点**：由于单例模式只生成一个实例，**减少了系统性能开销**

- 1、在内存里只有一个实例，减少了内存的开销，尤其是频繁的创建和销毁实例（比如管理学院首页页面缓存）。
- 2、避免对资源的多重占用（比如写文件操作）。

**缺点：**没有接口，不能继承，与单一职责原则冲突，一个类应该只关心内部逻辑，而不关心外面怎么样来实例化。

#### 使用场景

举例 java.lang.Runtime就是单例模式实现的类

常见的使用场景

* 网站的计数器，一般也是单例模式实现，否则难以同步。不用每次刷新都在数据库里加一次，用单例先缓存起来。
* 应用程序的日志应用，一般都使用单例模式实现，这一般是由于共享的日志文件一直处于打开状态，因为只能有一个实例去操作，否则内容不好追加。
* 数据库连接池的设计一般也是采用单例模式，因为数据库连接是一种数据库资源。
* 项目中，读取配置文件的类，一般也只有一个对象。没有必要每次使用配置文件数据，都生成一个对象去读取。
* Application 也是单例的典型应用
* Windows的Task Manager (任务管理器)就是很典型的单例模式
* Windows的Recycle Bin (回收站)也是典型的单例应用。在整个系统运行过程中，回收站一直维护着仅有的一个实例。
* 要求生产唯一序列号。
* 创建的一个对象需要消耗的资源过多，比如 I/O 与数据库的连接等。

## 理解main方法的语法

```java
public static void main(String[] args) {
	
}
```

 * 1. main()方法作为程序的入口
 * 2. main()方法也是一个普通的静态方法
 * 3. main()方法可以作为我们与控制台交互的方式。（之前：使用Scanner）

如何将控制台获取的数据传给形参：String[] args?

![命令行参数用法](http://101.34.218.64/JavaSE.assets/%E5%91%BD%E4%BB%A4%E8%A1%8C%E5%8F%82%E6%95%B0%E7%94%A8%E6%B3%95.png)

 ```java
public class MainTest {
	public static void main(String[] args) {
		//java MainTest 小明 61 true
		System.out.println(args[0]);
		System.out.println(args[1]);
		System.out.println(args[2]);
		int i=Integer.parseInt(args[1]);
		boolean b=Boolean.parseBoolean(args[2]);
	}
}
 ```



接受的是字符串型的数组，如果需要转换成基本数据类型 用Xxxx.parseXxx(args[i]);



小结：一叶知秋
public static void main(String[] args){//方法体}

权限修饰符：private 缺省 protected pubilc ---->封装性
修饰符：static \ final \ abstract \native 可以用来修饰方法
返回值类型： 无返回值 / 有返回值 -->return
方法名：需要满足标识符命名的规则、规范；"见名知意"
形参列表：重载 vs 重写；参数的值传递机制；体现对象的多态性
方法体：来体现方法的功能



## 类的成员之四：代码块(或初始化块)

### 作用：

对Java类或对象进行初始化

（注意 子类不能继承父类的代码块）**代码块不能被继承**


### 分类：

一个类中代码块若有修饰符，则**只能被static修饰**。

tatic 修饰的代码块，称为**静态代码块**(static block)，没有使用static修饰的，为代码块。

(1) 静态代码块：用static 修饰的代码块。用于初始化类的信息

```java
static{

}
```

1. 可以有输出语句。
2. 可以对类的属性、类的声明进行初始化操作。
3. 不可以对非静态的属性初始化。即：**不可以调用非静态的属性和方法**。
4. 若有多个静态的代码块，那么按照**从上到下**的顺序依次执行。
5. 静态代码块的执行要**先于非静态代码块**。
6. 静态代码块**随着类的加载而执行，且只执行一次**。

(2) 非静态代码块：没有static修饰的代码块。用于船舰对象时对对象的属性等进行初始化

```java
{
    
}
```

1. 可以有输出语句。
2. 也可以对类的属性、类的声明进行初始化操作。对对象的属性等进行初始化
3. 除了调用非静态的结构外，还**可以调用静态的变量或方法**。
4. 若有多个非静态的代码块，那么按照**从上到下**的顺序依次执行。
5. **每次创建对象的时候，都会执行一次。且先于构造器执行**。


static代码块通常用于初始化static的属性

```java
class Person {
public static int total;
static {
total = 100;//为total赋初值
}
…… //其它属性或方法声明
}
```

> 老韩说
>
> 1)相当于另外种形式的构造器(对构造器的补充机制)，可以做初始化的操作
> 2)场景: 如果多个构造器中都有重复的语句，可以抽取到初始化块中，提高代码的重用性



### 总结：程序中成员变量赋值的执行顺序

实例化子类对象时，涉及到父类、子类中静态代码块、非静态代码块、构造器的加载顺序：**由父及子，静态先行**。先加载父类的静态代码块，再加载子类的代码块，再非静态的。。。

>作者：吃盐的鱼
>链接：https://ac.nowcoder.com/discuss/682190?type=6
>来源：牛客网
>子类不能继承父类的代码块。
>对象的初始化顺序：
>   首先执行父类静态的内容，父类静态的内容执行完毕后，接着去执行子类的静态的内容，当子类的静态内容执行完毕之后，再去看父类有没有构造代码块，如果有就执行父类的构造代码块，父类的构造代码块执行完毕，接着执行父类的构造方法；父类的构造方法执行完毕之后，它接着去看子类有没有构造代码块，如果有就执行子类的构造代码块。子类的构造代码块执行完毕再去执行子类的构造方法。

①声明成员变量的默认初始化
②显式初始化、多个初始化块依次被执行（同级别下按先后顺序执行）
③构造器再对成员进行初始化操作
④通过”对象.属性”或”对象.方法”的方式，可多次给属性赋值







## 关键字：final

final 最终的

可以用来修饰：类、 方法、 变量(成员变量和局部变量)。

修改后叫 最终类 最终方法 最终变量(常量)

### final 修饰类

final class XXX{ } 

最终类 此类不能被继承

final标记的类**不能被继承**。提高安全性，提高程序的可读性。
如String类、System类、StringBuffer类

### final修饰方法

final标记的方法**不能被子类重写**。
比如：Object类中的getClass()。

### final 修饰变量

final标记的变量(**成员变量或局部变量)**即称为**常量**。**名称大写**，且**只能被赋值一次**。

* final标记的**成员变量**必须在**声明时**或在**每个构造器中**(每个构造器中都要有，因为不可以不赋值就使用，而构造器只能调用一个)或**代码块**中显式**赋值**，然后**才能使用**。
  final double MY_PI = 3.14;

  ```java
  public class FinalTest {
  	    final int WIDTH=0;//显式初始化
  	    final int LEFT;
  	    final int RIGHT;
  	    //final int DOWN;//报错 DOWN未初始化
  	    {
  	        LEFT=1;//代码块中初始化
  	    }
  	    public FinalTest(){
  	        RIGHT=2;//构造器中初始化
  	    }
  	    public FinalTest(int n){//用构造器初始化常量属性的好处就是可以传参，初始化不同的值
  	        RIGHT=n;//可以用this();每个构造器中构造器中要有对常量的初始化 因为构造器只能调用一次仅一个。 所以必须把该初始化的的常量初始化   
  	    }
  }
  ```

* static final 修饰的**成员变量**叫**全局常量**

* 方法的**形参用final修饰** 则**方法体内不可以再修改形参**

  final修饰形参时，表明此形参是一个常量。当我们调用此方法时，给常量形参赋一个实参。一旦赋值以后，就只能在方法体内使用此形参，但不能进行重新赋值。（基本数据类型是数据值不变；引用数据类型是地址值不变）

  ```java
  public class FinalTest1 {
  	public static void main(String[] args) {
  		finalTest(0);//0
  		finalTest(2);//2 可多次调用 因为形参的声明周期就在方体结束后结束了
  	}
  	 public static int finalTest(final int a) {
  	    	//a++;//=赋值 +=...复合赋值 ++自增自减 等都不可以 
  	    	System.out.println(a);
  			return a;
  	    }
  }
  ```

  ```java
  public class Something {
  public static void main(String[] args) {
  Other o = new Other();
  new Something().addOne(o);
  }
  public void addOne(final Other o) {
  o.i++;//没问题  因为o的地址不变，它的属性还是允许更改的
  }
  }
  class Other {
  public int i;
  }
  ```

  小技巧：i%2  等价于 i&1
  i&1 – [按位与](https://so.csdn.net/so/search?q=按位与&spm=1001.2101.3001.7020)运算，取 2进制整数 i 的最低位，如果最低位是1 则得1，如果最低位是0 则得0。 奇数 i 的最低位 是1，偶数i 的最低位 是0。if(i&1==1) 表示 如果是 奇数 则。。。

  

## 关键字：abstract

abstract 抽象的 。 用来**修饰类、方法**，不能用abstract修饰变量、代码块、构造器

类的设计应该保证父类和子类能够共享特征。有时将一个父类设计得非常抽象，以至于它没有具体的实例，这样的类叫做抽象类

父类方法不确定性的问题考虑将该方法设计为抽象(abstract)方法。所谓抽象方法就是没有实现的方法。所谓没有实现就是指**没有方法体**。
当一个类中存在抽象方法时，需要将该类声明为 abstract 类。抽象类是用来被继承的，抽象类的子类必须重写父类的抽象方法，并提供方法体。

一个类只能继承一个抽象类，而一个类却可以实现多个接口。

### 抽象类 

用abstract关键字修饰的类

 * **抽象类不能实例化**。但抽象类中一定有构造器，便于子类实例化时调用（涉及：子类对象实例化的全过程）
 * 抽象类除了不能实例化对象之外，类的其它功能依然存在，成员变量、成员方法和构造方法的访问方式和普通类一样
 * 开发中，都会提供抽象类的子类，让子类对象实例化，完成相关的操作 --->抽象的使用前提：继承性

### 抽象方法

用abstract关键字修饰的方法

 * **只有方法的声明，没有方法的实现**(即**没有方法体**)，以**分号**结束

 * 包含抽象方法的类，一定是一个抽象类(**含有抽象方法的类必须被声明为抽象类**)。反之，**抽象类中可以没有抽象方法的**。

 * **若子类重写了父类中的所有的抽象方法后，此子类方可实例化**。
> 补充：Java方法重写方法体可以和父类的相同。还有 {}是空的也能算重写

 * **若子类没重写父类中的所有的抽象方法**，**则此子类也是一个抽象类**，需要使用abstract修饰。（ 因为没重写，就**继承了父类的抽象方法**，而含有抽象方法的类必须被声明为抽象类）

   ```java
   public class AbstractTest {
   	public static void main(String[] args) {
   		SubClass sub=new SubClass();
   		//SubClass2 sub2=new SubClass2();//报错 不能实例化对象
   	}
   }
   
   abstract class AbstractClass{//抽象类
   	abstract void show();//抽象方法 用abstract修饰 后面是分号；不能有主体(即{})
   	abstract void haha();
   	void xixi() {}
   	//除了抽象方法，其他的构造器 属性 代码块 非抽象方法什么的都可以有
   }
   
   class SubClass extends AbstractClass{//重写了抽象父类的所有方法 可以实例化
   	@Override
   	void show() {}
   	@Override
   	void haha() {}
   }
   abstract class SubClass2 extends AbstractClass{
   	//未全部重写方法 该子类也要声明为抽象类 继承了父类的抽象方法 而有抽象方法的类必须声明为抽象类
   	@Override
   	void show() {
   	}
   }
   ```

   

### 使用注意点：

 * 1.**abstract只能修饰类、方法，不能用abstract修饰变量、代码块、构造器**
 * 2.**abstract不能修饰私有方法(因为不能被重写)、静态方法(看似重写不是重写)、final的方法(不能被重写)、final的类(不能被继承)**

### abstract的应用举例：

举例一：

```java
public abstract class Vehicle{
public abstract double calcFuelEfficiency(); //计算燃料效率的抽象方法
public abstract double calcTripDistance(); //计算行驶距离的抽象方法
}
public class Truck extends Vehicle{
public double calcFuelEfficiency( ) { //写出计算卡车的燃料效率的具体方法
}
public double calcTripDistance( ) { //写出计算卡车行驶距离的具体方法
}
}
public class RiverBarge extends Vehicle{
public double calcFuelEfficiency( ) { //写出计算驳船的燃料效率的具体方法 }
public double calcTripDistance( ) { //写出计算驳船行驶距离的具体方法}
}
```

举例二：
```java
abstract class GeometricObject{
public abstract double findArea();
}
class Circle extends GeometricObject{
private double radius;
public double findArea(){
		return 3.14 * radius * radius;
};
}
```
举例三：IO流中设计到的抽象类：InputStream/OutputStream / Reader /Writer。在其内部定义了抽象的read()、write()方法。

### 抽象类的匿名子类

#### 匿名类

Java 中可以实现一个类中包含另外一个类，且不需要提供任何的类名直接实例化。

(Java允许直接使用一个类的子类的类体创建一个子类对象。)

主要是用于在我们需要的时候创建一个对象来执行特定的任务，可以使代码更加简洁。

匿名类是不能有名字的类，它们不能被引用，只能在创建时用 **new** 语句来声明它们。

使用匿名类时，必然是在某个类中直接用匿名类创建对象，因此匿名类一定是内部类

匿名类语法格式：

```java
class outerClass {
    // 定义一个匿名类
    object1 = new Type(parameterList) {
         // 匿名类代码（匿名类的“类体”）
    };
}
```

以上的代码创建了一个匿名类对象 object1，匿名类是表达式形式定义的，所以末尾以分号 **;** 来结束。

匿名类通常继承一个父类或实现一个接口。

#### 创建抽象类的匿名子类的对象

```java
public class AbstractTest {
	public static void main(String[] args) {
		SubClass sub=new SubClass();//非匿名类 的 非匿名对象
		method(sub);
		method(new SubClass());//非匿名类的 匿名对象 作形参
		
		//SubClass2 sub2=new SubClass2();//报错 不能实例化对象
		SubClass2 sub2=new SubClass2() {
			//在构造器和;中间加个{}括号，里面重写一下抽象方法就可以实例化对象了 
			//这时候不是SubClass2类 而是创建了SubClass2的一个“匿名子类”的对象sub2
			@Override
			void haha() {}
		};
		method(sub2);
		method(new SubClass2() {//SubClass2的一个“匿名子类”的 匿名对象 作为形参
			@Override
			void haha() {}
		});
	}
	public static void method(AbstractClass o) {
		
	}
}

abstract class AbstractClass{//抽象类
	abstract void show();//抽象方法 用abstract修饰 后面是分号；不能有主体(即{})
	abstract void haha();
	void xixi() {}
	//除了抽象方法，其他的构造器 属性 代码块 非抽象方法什么的都可以有
}

class SubClass extends AbstractClass{//重写了抽象父类的所有方法 可以实例化
	@Override
	void show() {}
	@Override
	void haha() {}
}
abstract class SubClass2 extends AbstractClass{
	//未全部重写方法 该子类也要声明为抽象类 继承了父类的抽象方法 而有抽象方法的类必须声明为抽象类
	@Override
	void show() {
	}
}
```

#### 模板方法设计模式(TemplateMethod)

属于行为型模式

**抽象类体现的就是一种模板模式的设计**，抽象类作为多个子类的通用模板，子类在抽象类的基础上进行扩展、改造，但子类总体上会保留抽象类的行为方式。

##### **解决的问题**

当功能内部一部分实现是确定的，一部分实现是不确定的。这时可以把不确定的部分暴露出去，让子类去实现。
（换句话说，在软件开发中实现一个算法时，整体步骤很固定、通用，这些步骤已经在父类中写好了。但是某些部分易变，易变部分可以抽象出来，供不同子类实现。这就是一种模板模式。）

编写一个抽象父类，父类提供了多个子类的通用方法，并把一个或多个方法留给其子类实现，就是一种模板模式

##### 代码示例

```java
public class TemplateTest{
	public static void main(String[] args) {
		SubTemplate t=new SubTemplate();
		t.spendTime();
	}
}
abstract class Template{
	//计算某段代码执行所需要花费的时间
	public void spendTime(){
		long start = System.currentTimeMillis();
		this.code();//不确定的部分、易变的部分
		long end = System.currentTimeMillis();
		System.out.println("花费的时间为：" + (end - start));
	}
	public abstract void code();
}

class SubTemplate extends Template{
	@Override
	public void code() {
		//1000内的质数
		for(int i = 2;i <= 1000;i++){
			boolean isFlag = true;
			for(int j = 2;j <= Math.sqrt(i);j++){
				if(i % j == 0){isFlag = false;break;}
			}
			if(isFlag){System.out.println(i);}
		}
	}
}
```

示例2

```java
//抽象类的应用：模板方法的设计模式
//定义一个操作中的算法的骨架，而将一些步骤延迟到子类中。该模式使得子类可以不改变一个算法的结构即可重定义该算法的某些特定步骤。
public class TemplateMethodTest {
	public static void main(String[] args) {
		BankTemplateMethod btm = new DrawMoney();
		btm.process();//不是显式的调用重写的transact，而是调用一个模板方法间接调用transact

		BankTemplateMethod btm2 = new ManageMoney();
		btm2.process();
	}
}
abstract class BankTemplateMethod {
	// 具体方法
	public void takeNumber() {
		System.out.println("取号排队");
	}
	public abstract void transact(); // 办理具体的业务 //钩子方法
	public void evaluate() {
		System.out.println("反馈评分");
	}

	// 模板方法，把基本操作组合到一起，子类一般不能重写（加了final）(是一个关键点，不允许重写此模板方法，只允许重写里面的个别方法)
	public final void process() {
		this.takeNumber();
		this.transact();// 像个钩子，具体执行时，挂哪个子类，就执行哪个子类的实现代码。这叫"钩子方法Hook Method"或"回调方法”
		this.evaluate();
	}
}

class DrawMoney extends BankTemplateMethod {
	public void transact() {
		System.out.println("我要取款！！！");
	}
}

class ManageMoney extends BankTemplateMethod {
	public void transact() {
		System.out.println("我要理财！我这里有2000万美元!!");
	}
}
```



##### 应用场景

模板方法设计模式是编程中经常用得到的模式。各个框架、类库中都有他的影子，比如常见的有：
* 数据库访问的封装
* Junit单元测试
* JavaWeb的Servlet中关于doGet/doPost方法调用
* Hibernate中模板程序
* Spring中JDBCTemlate、HibernateTemplate等

## 接口(interface)

 一方面，有时必须从几个类中“派生”出一个子类，继承它们所有的属性和方法。**java不支持多重继承，接口可以得到多重继承的效果**。
另一方面，有时必须从几个类中抽取出一些**共同的行为特征**，而它们之间又没有is-a的关系，仅仅是具有相同的行为特征而已。例如一些设备都支持USB连接，但是设备之间没有继承关系。

接口的本质是契约，标准，规范

**类只能继承(指直接继承)一个父类，但可以实现多个接口**

接口(interface)是抽象方法和常量值定义的集合。

### 如何定义接口

* 用**interface**来定义。(相当于把定义类时的class换成interface)
* 定义成员变量
  JDK7及以前：只能定义全局常量和抽象方法
  
  * 接口中的所有成员**变量**都**默认**是由**public static final**修饰的。——全局常量
  * 接口中的所有**抽象方法**都**默认**是由**public abstract**修饰的。也可以使用 protected ，但不能用 private。——抽象方法
    ```java
    public interface MyInterface{
     static final int x=0;
     int y=0;  //默认static final 
      
     public abstract void method1(); 
     abstract void method2(); 
     void method3() ; //默认 public abstract
    }
    ```

  
  JDK8中，除了定义全局常量和抽象方法之外，还可以定义静态方法、默认方法
    ```java
    //JDK8：静态方法  使用static
  //接口中的静态方法，只能使用接口名称调用
    public static void method4() {
      System.out.println("静态方法");
    }
     
    //JDK8：默认方法 使用default 注意！！不是访问权限的"缺省" 。是和抽象方法相对的普通方法
    public default void method5() {
      System.out.println("默认方法");
    }
  //继承的接口实现父接口的抽象方法需要加 dafault
    ```
  
  JDK9 ：基于 JDK8 增加了私有静态方法的声明
  ```java 
  //JDK9： private static 方法
  //接口中的 private static 方法只能在接口内调用 ；
  private static void method6(){
   System.out.println("private method6");
  }
  ```

* **接口中没有构造器**。(接口不可以实例化)
* **接口采用多继承机制**。——接口与接口之间可以继承，而且可以多继承
  
```java
  public interface Interface3 extends Interface1,interface2{ }
```

### 接口的实现类

  实现接口的类

* 使用**implements**实现 实现接口   （implement的第三人称单数v.使生效; 贯彻; 执行; 实施;）

* **一个类可以实现多个接口**

```java
class Class implements InterfaceA{ }
如果需要继承父类 先写extends，后写implements
class SubClass extends SuperClass implements InterfaceA{ }
实现多个接口
class Class  implements  implements InterfaceA,InterfaceB,InterfaceC{ }
```
* 实现接口的类中必须提供接口中**所有方法**的具体实现内容，方可实例化。    否则，仍为抽象类。



### 一些应用

（1）USB

  ```java
public class UsbTest {
	public static void main(String[] args) {
		Computer computer=new Computer();
		//1.创建了接口的非匿名实现类的非匿名对象
		Flash flash=new Flash();
		computer.transferData(flash);
		//2.创建了接口的非匿名实现类的匿名对象
		computer.transferData(new Flash());
		//3.创建了接口的匿名实现类的非匿名对象
		USB usb=new USB() {
			@Override
			public void start() {}
			@Override
			public void stop() {}
		};
		computer.transferData(usb);
		//4.创建了接口的匿名实现类的匿名对象
		computer.transferData(new USB() {
			@Override
			public void start() {}
			@Override
			public void stop() {}
		});
	}
}
  ```

  (2) 面向接口编程：我们在应用程序中，调用的结构都是JDBC中定义的接口，不会出现具体某一个数据库厂商的API。

### 一些理解

* 接口的主要用途就是被实现类实现。（**面向接口编程**）
* 与继承关系类似，接口与实现类之间存在**多态性**
* **接口和类是并列关系**，或者可以理解为一种特殊的类。从本质上讲，接口是一种**特殊的抽象类**，这种抽象类中只包含常量和方法的定义(JDK7.0及之前)，而没有变量和方法的实现。

### java8中的新规范

知识点1：**接口中定义的静态方法，只能通过接口(名)来调用。**
知识点2：通过**实现类的对象**，可以**调用接口中的默认方法**。

​      public **default** void method5() {} JDK8：默认方法 使用default 注意！！**不是访问权限**的"缺省" 。是和抽象方法相对的**普通方法**

 >如果实现类重写了接口中的默认方法，调用时，仍然调用的是重写以后的方法

知识点3：如果子类(或实现类)**继承的父类和实现的接口中声明了同名同参数的默认方法**，那么子类在**没重写此方法的情况下**，默认调**用的是父类中的**同名同参数的方法。-->**类优先原则**

	>课件上的：
	>
	>若一个接口中定义了一个默认方法，而父类中也定义了一个同名同参数的非抽象方法，则不会出现冲突问题。因为此时遵守：类优先原则。接口中具有相同名称和参数的默认方法会被忽略。

知识点4：如果**实现类实现了多个接口，而这多个接口中定义了同名同参数的默认方法**，
 	那么在实现类没重写此方法的情况下，报错。-->**接口冲突**。
 	这就需要我们**必须在实现类中重写此方法**

	>课件上的：
	>
	>若一个接口中定义了一个默认方法，而另外一个接口中也定义了一个同名同参数的方法（不管此方法是否是默认方法），在实现类同时实现了这两个接口时，会出现：接口冲突。
	>解决办法：实现类必须覆盖接口中同名同参数的方法（重写），来解决冲突。

知识点5：如何在子类(或实现类)的方法中调用父类、接口中被重写的方法.

（在实现类里的方法里 用"接口.super.默认方法" 调用接口的默认方法  虽然不常用 这也太弯弯绕了吧！！！）

```java
class SubClass extends SuperClass implements InterfaceA,InterfaceB	{
    @Override
    void method(){}
    
    public void myMethod(){
		method();//调用自己定义的重写的方法
		super.method();//调用的是父类中声明的
		//调用接口中的默认方法  接口名.super.默认方法
		InterfaceA.super.method();
		interfaceB.super.method();
	}
}
```



### 面试题

1.抽象类和接口的异同？(很重要)
相同点：不能实例化；都可以包含抽象方法的。
不同点：
1）把抽象类和接口(java7,java8,java9)的定义、内部结构解释说明
2）类：单继承性    接口：多继承
   类与接口：多实现

![抽象类和接口的区别](http://101.34.218.64/JavaSE.assets/%E6%8A%BD%E8%B1%A1%E7%B1%BB%E5%92%8C%E6%8E%A5%E5%8F%A3%E7%9A%84%E5%8C%BA%E5%88%AB.png)

2.排错

```java
interface A {int x = 0;}
class B {int x = 1;}
class C extends B implements A {
	public void pX() {System.out.println(x);}
	public static void main(String[] args) {new C().pX();}
}

//pX方法中：
////System.out.println(x);//报错 字段x有歧义
//System.out.println(super.x);
//System.out.println(A.x);//接口中是一个全局常量,用接口名去调用
```

如果父类和接口中的变量重名了，调用时未指明，会报错 字段有歧义

3.排错

```java
interface Playable {
	void play();
}
interface Bounceable {
	void play();
}
interface Rollable extends Playable, Bounceable {
	Ball ball = new Ball("PingPang");
}
class Ball implements Rollable {
	private String name;
	public String getName() {
		return name;
	}
	public Ball(String name) {
		this.name = name;
	}
	public void play() {
		ball = new Ball("Football");
		System.out.println(ball.getName());
	}
}
//错误在ball是final的 不可以在类Ball的play()方法中修改

这里play()是对接口Bounceable和Playable两个类中的play（）都重写了 不会报错
```

允许两个接口的共同的实现类中允许对两个接口中的同名方法进行 重写。（实现类必须覆盖接口中同名同参数的方法，来解决接口冲突。）

### 课后题

```java
/*
 * 定义一个接口用来实现两个对象的比较。
* interface CompareObject{
public int compareTo(Object o);
//若返回值是 0 , 代表相等; 若为正数，代表当前对象大；负数代表当前对象小
}
定义一个Circle类，声明redius属性，提供getter和setter方法
定义一个ComparableCircle类，继承Circle类并且实现CompareObject接口。
  在ComparableCircle类中给出接口中方法compareTo的实现体，用来比较两个圆的半径大小。

定义一个测试类InterfaceTest，创建两个ComparableCircle对象，调用compareTo方法比较两个类的半径大小。

 */

interface CompareObject {
	public int compareTo(Object o);
}

class Circle {
	private double redius;

	public double getRedius() {
		return redius;
	}

	public void setRedius(double redius) {
		this.redius = redius;
	}

}

class comparableCircle extends Circle implements CompareObject {

	@Override
	public int compareTo(Object o) {
		if (this == o) {
			return 0;// 同一个对象 必等
		}

//			if (this.getRedius() > circle.getRedius()) {
//				return 1;
//			} else if (this.getRedius() < circle.getRedius()) {
//				return -1;
//			} else {
//				return 0;
//			}
			//进阶 声明redius改成Double。再使用Double里的compareTO()
			//return getRedius().compareTo(circle.getRadius());
			//再进阶 不改redius类型
			return Double.valueOf(getRedius()).compareTo(circle.getRedius());
		}else {
			//return 0;// 现阶段先这样 其实应该抛异常
			throw new RuntimeException("传入的数据类型不匹配");
			
		}
		
	}
}
public class CircleTestMain{
	public static void main(String[] args) {
		comparableCircle circe1=new comparableCircle();
		comparableCircle circe2=new comparableCircle();
		circe1.setRedius(3.2);
		circe2.setRedius(2.0);
		int result = circe1.compareTo(circe2);
		if(result>0) {
			System.out.println("circe1大于circe2");
		}else if(result<0) {
			System.out.println("circe1小于circe2");
		}else {
			System.out.println("circe1等于circe2");
		}
	}
}
```



### 接口有关的设计模式

#### 代理模式Proxy

代理模式是java开发中使用较多的一种设计模式。代理模式就是为其它对象提供一种代理以控制对这个对象的访问.

在代理模式（Proxy Pattern）中，一个类代表另一个类的功能。属于结构型模式。

```java
public class ProxyTest {
	public static void main(String[] args) {
		RealServer realServer = new RealServer();
		ProxyServer proxyServer = new ProxyServer(realServer);		
		proxyServer.browse();
	}
}

interface Network{
	public void browse();
}
//被代理类
class RealServer implements Network{
	@Override
	public void browse() {
		System.out.println("真实的服务器访问网络");		
	}	
}
//代理类
class ProxyServer implements Network{
	private Network work;//声明一个接口变量
	public ProxyServer(Network work) {
		this.work=work;
	}
	public void check() {
		System.out.println("联网之前的检查工作");
	}
	
	@Override
	public void browse() {
		check();//代理类负责检查工作
		work.browse();//被代理类真实的访问
	}
}

//输出：
//联网之前的检查工作
//真实的服务器访问网络
```

例2

```java
public class StaticProxyTest {
	public static void main(String[] args) {
		Star s = new Proxy(new RealStar());
		s.confer();
		s.signContract();
		s.bookTicket();
		s.sing();
		s.collectMoney();
	}
}
interface Star {
	void confer();// 面谈
	void signContract();// 签合同
	void bookTicket();// 订票
	void sing();// 唱歌
	void collectMoney();// 收钱
}
class RealStar implements Star {
	public void confer() {
	}
	public void signContract() {
	}
	public void bookTicket() {
	}
	public void sing() {
		System.out.println("明星：歌唱~~~");
	}
	public void collectMoney() {
	}
}
class Proxy implements Star {
	private Star real;
	public Proxy(Star real) {
		this.real = real;
	}
	public void confer() {
		System.out.println("经纪人面谈");
	}
	public void signContract() {
		System.out.println("经纪人签合同");
	}
	public void bookTicket() {
		System.out.println("经纪人订票");
	}
	public void sing() {
		real.sing();
	}
	public void collectMoney() {
		System.out.println("经纪人收钱");
	}
}
```



##### 应用场景：

在直接访问对象时带来的问题，比如说：要访问的对象在远程的机器上。在面向对象系统中，有些对象由于某些原因（比如对象创建开销很大，或者某些操作需要安全控制，或者需要进程外的访问），直接访问会给使用者或者系统结构带来很多麻烦，我们可以在访问此对象时加上一个对此对象的访问层。

* 安全代理：屏蔽对真实角色的直接访问。
* 远程代理：通过代理类处理远程方法调用（RMI）
*  延迟加载：先加载轻量级的代理对象，真正需要再加载真实对象比如你要开发一个大文档查看软件，大文档中有大的图片，有可能一个图片有100MB，在打开文件时，不可能将所有的图片都显示出来，这样就可以使用代理模式，当需要查看图片时，用proxy来进行大图片的打开。

##### 分类

* 静态代理（静态定义代理类）
* 动态代理（动态生成代理类）: JDK自带的动态代理，需要反射等知识

#### 工厂相关的模式

1. 解决的问题
实现了创建者与调用者的分离，即将创建对象的具体过程屏蔽隔离起来，达到提高灵活性的目的。

2. 具体模式


工厂方法模式：用来生产同一等级结构中的固定产品。（支持增加任意产品)

>简单工厂模式（Simple Factory）看为工厂方法模式的一种特例
>
>简单工厂模式：用来生产同一等级结构中的任意产品。（对于增加新的产品，需要修改已有代码）

抽象工厂模式：用来生产不同产品族的全部产品。（对于增加新的产品，无能为力；支持增加产品族)

## 类的成员之五：内部类

内部类 Inner class

Java中允许将一个类A声明在另一个类B中，则类A就是内部类，类B称为外部类.

### 内部类的分类：

* 成员内部类（静态、非静态 ）

* 局部内部类(方法内、代码块内、构造器内) 不谈修饰符

  ```java
  public Test{}
      public Test() {	
  		//构造器内的局部内部类
  		class A{ }
  	}
  	public void method(){
  		//方法内的局部内部类
  		class A{ }
  	}
  	{	//代码块内的局部内部类
  		class A{ }
  	}
  	
  }
  ```

  

### 成员内部类

#### 成员内部类作为外部类的成员

* **调用外部类的结构**

  注意静态调静态，动态调静态或动态。

  > 非static的成员内部类中的成员不能声明为static的，只有在外部类或static的成员内部类中才可声明static成员。
  >
  > 当想要在外部类的静态成员部分使用内部类时，可以考虑内部类声明为静态的。

  成员内部类可以直接使用外部类的所有成员(相当于省略了"外部类.this.")，包括私有的。

  > 而外部类访问成员内部类的成员，需要“内部类.成员”或“内部类对象.成员”的方式

  如果内部类和外部类有同名的成员，内部类中直接调用时是指自己。

  如果有同名的变量，内部类方法中直接调用变量时在内部类的方法中、内部类中、外部类中依次往外找。——就近原则

  ```java
  class Person {	
  	int age;
  	class Dog  {
  		String name;
  		int age;
  		public void show() {
  			int age=1;
  			System.out.println("狗");
  	
  			System.out.println(age);//依次往外找 方法中有是方法的局部变量(或形参)。方法的注释掉是内部类的。内部类也注释掉是外部类的 
  			System.out.println(this.age);//内部类的属性 Person.Dog里的age
  			System.out.println(Person.this.age);//外部类的属性Person里的age
          }
      }
  }
  ```

  

  (内部类中this是指内部类，super默认是Object除非指明父类)

* **可以被static修饰**，但此时就不能再使用外层类的非static的成员变量

* 可以被**4种不同的访问权限修饰符修饰**。(而外部类只可以用缺省和public)

#### 成员内部类对内作为一个类

* 类内可以定义属性、方法、构造器等
* 可以被**final**修饰，表示此类不能被继承。言外之意，不使用final，就可以被继承
* 可以被**abstract**修饰，可以被**其它的内部类继承**
* 编译以后生成OuterClass$InnerClass.class字节码文件（也适用于局部内部类）

### 局部内部类

只能在声明它的方法或代码块中使用，而且是先声明后使用。除此之外的任何地方都不能使用该类。
但是它的对象可以通过外部方法的返回值返回使用，返回值类型只能是局部内部类的父类或父接口类型。

注意点：
在方法中的局部内部类的方法中,如果调用局部内部类所声明的方法中的局部变量的话,要求此局部变量声明为final的。（因为方法生命周期短，num是另保存了一个副本）

  ```java
public class OuterClass {
	public void method() {
		class InnerClass{
			void method1(){
				final int i = 0;
				System.out.println(i);
			}
		}
	}
}
  ```

​	jdk 7及之前版本：要求此局部变量显式的声明为final的
​	jdk 8及之后的版本：可以省略final的声明

### 重点关注的问题

内部类知道这些就”够用“

1.如何实例化成员内部类的对象

* 静态成员内部类创建对象： 外部类.内部类 变量名=new 外部类.内部类构造器();

  Person.Dog dog = new Person.Dog();

* 非静态的成员内部类创建对象：外部类.内部类 变量名=外部类的对象.new 外部类.内部类构造器();（构造器前的外部类.可省略）

  Person p = new Person();
  Person.Bird bird = p.new Bird();//p.new Person.Bird()

2.如何在成员内部类中区分调用外部类的结构

[跳转](#成员内部类作为外部类的成员)

3.开发中，局部内部类的使用

```java
//这两种方式都是在方法getComparable()中创建了一个局部内部类
//返回一个实现了Comparable接口的类的对象
	public Comparable getComparable(){

		//创建一个实现了Comparable接口的 实现类的 匿名对象
		//方式一：
//		class MyComparable implements Comparable{
//			@Override
//			public int compareTo(Object o) {
//				return 0;
//			}
//		}
//		return new MyComparable();
		
		//方式二：创建了一个实现了comparable接口的 匿名实现类的 匿名对象
		return new Comparable(){
			@Override
			public int compareTo(Object o) {
				return 0;
			}	
		};
	}
```

匿名内部类 

new 类或接口(参数列表){

}

# 第7章 异常处理



## 异常概述与异常体系结构

异常：在Java语言中，将程序执行中发生的不正常情况称为“异常”。(开发过程中的**语法错误和逻辑错误不是异常**)

Java程序在执行过程中所发生的异常事件可分为两类：Error和Exception

* Error(错误)：Java虚拟机无法解决的严重问题。如：JVM系统内部错误、资源耗尽等严重情况。比如：StackOverflowError(栈溢出)和OOM(OutofMemoryError堆溢出)。一般不编写针对性的代码进行处理。

  ```java
  public static void main(String[] args) {
  		//main(args);//java.lang.StackOverflowError
  		Integer[] arr = new Integer[1024*1024*1024];//java.lang.OutofMemoryError
  	}
  ```

* Exception(异常): 其它因编程错误或偶然的外在因素导致的一般性问题，**可以使用针对性的代码进行处理**。

  例如：空指针访问、试图读取不存在的文件、网络连接中断、数组角标越界

 重点关注Exception。狭义上，异常一般指的是Exception的。程序员通常只能处理Exception，而对Error无能为力

所有异常都发生在运行阶段的。

对于这些错误，一般有两种解决方法：一是遇到错误就终止程序的运行。另一种方法是由程序员在编写程序时，就考虑到错误的检测、错误消息的提示，以及错误的处理。

**捕获**错误最理想的是在编译期间，但有的错误只有在运行时才会发生（比如：除数为0，数组下标越界等）。分类：编译时异常和运行时异常。

>编译时异常和运行时异常，**都发生在运行阶段**。编译阶段异常是不会发生的。编译时异常因为什么而得名？
>
>因为编译时异常必须在编译（编写）阶段预先处理，如果不处理编译器报错，因此得名。
>所有异常都是运行阶段发生的。因为只有程序运行阶段才可以new对象。
>因为异常的发生都是new异常对象。
>
>版权声明：本文为CSDN博主「夢想家吖」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
>原文链接：https://blog.csdn.net/qq2632246528/article/details/114086425



(1)运行时异常 
* 是指编译器不要求强制处置的异常。一般是指编程时的逻辑错误，是程序员应该积极避免其出现的异常。**java.lang.RuntimeException类及它的子类**都是运行时异常。
* 对于这类异常，**可以不作处理**，因为这类异常很普遍，若全处理可能会对程序的可读性和运行效率产生影响。

(2)编译时异常——也发生在运行时！！
* 是指**编译器要求必须处置的异常**。即程序在运行时由于外界因素造成的一般性异常。**编译器要求Java程序必须捕获或声明所有编译时异常**。
* 对于这类异常，如果程序不处理，可能会带来意想不到的结果。

>编译时异常：必须显示处理（try……catch……），否则程序就会发生错误，无法通过编译
>
>运行时异常：无需显示处理，也可以和编译时异常一样处理
>
>在编译时异常中，不管是否会出现异常，Java都强制要求我们在代码中进行显式的声明和捕获，否则就会产生编译错误。

执行javac.exe 文件名，发现编译时异常(发生在运行阶段,编译器只是预处理)
执行java.exe 类命，发现运行时异常

异常体系结构：

```java
java.lang.Throwable
		|-----java.lang.Error(unchecked):一般不编写针对性的代码进行处理。
		|-----java.lang.Exception:可以进行异常的处理
			|-----IOException(checked、编译时异常)
					|-----FileNotFoundException
					|-----EOFException
			|-----ReflectiveOperationException
					|-----ClassNotFoundException(checked、编译时异常)
			|------RuntimeExceptio(unchecked、运行时异常)
					|-----NullPointerException
					|-----ArrayIndexOutOfBoundsException
					|-----ClassCastException
					|-----NumberFormatException
					|-----InputMismatchException
					|-----ArithmeticException
```



”**如果出现 RuntimeException 异常， 那么就一定是你的问题**”“是一条相当有道理的规则。

Java语言规范将派生于Error类或**RuntimeException类**的所有异常称为**非受检( unchecked) 异常**， 所有其他的异常称为受检（checked) 异常。(忽略Error)**可以把所有非受检异常等价于运行时异常(RuntimeException及其子类)，受检异常等价于编译时异常。**

## 常见异常

### 常见运行时异常

1)**NullPointerException 空指针异常**。 当应用程序试图在需要对象的地方使用 null 时

```java
//NullPointerException
		int[][] arr=new int[2][];
		System.out.println(arr[1][0]);//arr[1]是null
```
> 技巧：如果str.XXX("字符串") 不如写成 "字符串".XXX(str) 。防止空指针异常

2)**ArithmeticException 数学运算异常**。  当出现异常的运算条件时，抛出此异常

```java
// ArithmeticException 数学算术异常 比如除以零
		System.out.println(2 / 0);
```
3)**ArrayIndexOutOfBoundsException 数组下标越界异常**  。用非法索引访问数组时抛出的异常。如果索引为负或大于等于数组大小

```java
// ArrayIndexOutOfBoundsException
		int[][] arr = new int[2][3];
		System.out.println(arr[1][3]);
```
4)**ClassCastException 类型转换异常**。  当试图将对象强制转换为不是实例的子类时，抛出该异常

```java
//ClassCaseException  出现在向下转型时
	Object obj=new Date();
	String str=(String)obj;
```
5)**NumberFormatException 数字格式不正确异常**。当应用程序试图将字符串转换成一种数值类型，但该字符串不能转换为适当格式时

```java
// NumerFormatException 常出现在使用包装类的valueOf(string)、parseXxx(string)时
		Integer I = Integer.valueOf("123a");
		int i = Integer.parseInt("123a");
```
6)**InputMismatchException 输入不匹配异常**

```java
// InputMismatchException 输入不匹配
		Scanner sc = new Scanner(System.in);
		int score = sc.nextInt();// 输入数据不是一个整型时
		System.out.println("分数" + score);
```


### 常见编译时异常

 java.io.IOExeption 当发生某种 I/O 异常时，抛出此异常
    FileNotFoundException 当试图打开指定路径名表示的文件失败时，抛出此异常。 
    EOFException 当输入过程中意外到达文件或流的末尾时，抛出此异常。 
	java.net.UnknownHostException 无法确定主机的IP地址
	java.net.MalformedURLException出现了错误的 URL。或者在规范字符串中找不到任何合法协议，或者无法解析字符串
java.lang.ClassNotFoundException 加载类，而该类不存在时
java.lang.InterruptedException 当线程在活动之前或活动期间处于正在等待、休眠或占用状态且该线程被中断时
java.lang.IllegalArgumentException向方法传递了一个不合法或不正确的参数
java.sql.SQLException 操作数据库时 查询表可能发生异常

举例：

```java
//FileNotFoundException 韩顺平的例子
import java.io.FileInputStream;
import java.io.IOException;
public class TestFileNotFoundException {
	public static void main(String[] args) {
		try {
			FileInputStream fis;
			fis = new FileInputStream("d:\\aa.jpg");
			int len;
			while ((len = fis.read()) != -1) {
				System.out.println(len);
			}
			fis.close();
		} catch (IOException e) {
			e.printStackTrace();
		}
	}
}
```

```java
//FileNotFoundException  宋红康的例子
import java.io.File;
import java.io.FileInputStream;
public class TestFileNotFoundException2 {
	public static void main(String[] args) {
		File file=new File("hello.txt");
		FileInputStream fis= new FileInputStream(file);
			int data=fis.read();
			while (data != -1) {
				System.out.print((char)data);
				data = fis.read();
			}
			fis.close();
	}
}
```

## 异常处理机制（重要）

在编写程序时，经常要在可能出现错误的地方加上检测的代码，如进行x/y运算时，要检测分母为0，数据为空，输入的不是数据而是字符等。过多的if-else分支会导致程序的代码加长、臃肿，可读性差。因此采用异常处理机制。
Java异常处理
Java采用的异常处理机制，是将异常处理的程序代码集中在一起，与正常的程序代码分开，使得程序简洁、优雅，并易于维护。

**抓抛模型**
(1)过程一："抛"——抛出异常：程序在正常执行的过程中，一旦出现异常，就会**在异常代码处生成一个对应异常类的对象，并将此对象抛出**。（抛出：异常对象将被提交给Java运行时系统）

 * **一旦抛出对象以后，其后的代码就不再执行**。
 * 关于异常对象的产生：①虚拟机自动生成的异常对象并抛出② 手动创建对象，并抛出（throw 没有s）。

(2)过程二："抓"——捕获(catch)异常：可以理解为异常的处理方式：① try-catch-finally  ② throws

**Java异常处理的方式**：

方式一：try-catch-finally： 程序员在异常中捕获发生的异常，自行处理
方式二：throws + 异常类型：将发生的异常抛出，交给调用者(方法)处理，最顶级的处理者就是JVM 

### try-catch-finally

#### 结构示意

```java
try{
   		//可能出现异常的代码——可疑代码
}catch(异常类型1 变量名1){
   		//处理异常的方式1
}catch(异常类型2 变量名2){
   		//处理异常的方式2
}catch(异常类型3 变量名3){
   		//处理异常的方式3
}
   ..多个catch..
finally{
   		//一定会执行的代码
   }
```

![try-catch-finally处理机制示意图](http://101.34.218.64/JavaSE.assets/try-catch-finally%E5%A4%84%E7%90%86%E6%9C%BA%E5%88%B6%E7%A4%BA%E6%84%8F%E5%9B%BE.png)

#### 结构说明

(1)try：

* 使用try将**可能出现异常的代码(可疑代码)**包装起来，在执行过程中**，一旦出现异常，就会生成一个对应异常类的对象并抛出**。
* **根据此对象的类型，去catch中进行匹配**；
* 注意：**一旦抛出对象以后，try中其异常代码后的代码就不再执行**。
* 如果没有发生异常则顺序执行try中的的代码，不会进入catch，会执行finally中代码，若没写finally的情况下，继续执行结构后的代码
* **在try结构中声明的变量，再出了try结构以后，就不能再被调用**

(2)catch:

* 一旦try中的异常对象匹配到某一个catch时，就进入catch中进行异常的处理。

* 一旦处理完成，就跳出当前的try-catch结构，执行finally中代码，若没写finally的情况下，继续执行结构后的代码

* 如果catch中处理异常的代码也出现异常，则不会执行结构后的。但是有finally必执行。

* **catch中的异常类型如果满足子父类关系**，则要求**子类一定声明在父类的上面**(保证了发生异常时，只会匹配一个catch)。否则，报错。(如果没子父类关系，则谁上谁下无所谓。）
  
  > 技巧：如果明确知道产生的是何种异常，可以用该异常类作为catch的参数；也可以用其父类作为catch的参数。
> 比如可以用RuntimeException类作为参数，或者用所有异常的父类Exception类作为参数

* 常用的异常对象处理的方式：
  ① **String  getMessage()**获取异常信息，返回字符串    
  ② **void printStackTrace()**获取异常类名和异常信息，以及异常出现在程序中的位置。返回值void。

  	![输出的异常信息](http://101.34.218.64/JavaSE.assets/%E8%BE%93%E5%87%BA%E7%9A%84%E5%BC%82%E5%B8%B8%E4%BF%A1%E6%81%AF.png)

(3)finally

 * finally是**可选**的。

 * **finally中声明的是一定!一定！一定！会被执行的代码**。即使catch中又出现异常了、try中有return语句、catch中有return语句等情况。

   ```java
   	@Test
   	public void Test() {
   		System.out.println(method());
   	}
   	public  int method() {
   		try {
   			int num = Integer.parseInt("12a4");
   			return 0;
   		} catch (NumberFormatException e) {
   			//System.out.println(e.getMessage());
   			e.printStackTrace();
   			return 1;//执行到return方法，就会返回相应的值，把值存在临时栈中。只是没有立即返回，而是执行finally
   		}finally {
   			return 2;//finally返回2 告诉程序结束
   		}
   	}
   //输出：
   java.lang.NumberFormatException: For input string: "12a4"
   	at java.base/java.lang.NumberFormatException.forInputString(NumberFormatException.java:67)
   	at java.base/java.lang.Integer.parseInt(Integer.java:668)
   	at java.base/java.lang.Integer.parseInt(Integer.java:786)
   	at com.loong.exception1.trycatchtest.method(trycatchtest.java:12)
   	at com.loong.exception1.trycatchtest.Test(trycatchtest.java:8)
   .。。。。。。。。。。报错信息。。。。。。。
   2
   ```

   

 * 像数据库连接、输入输出流、网络编程Socket等资源，JVM是不能自动的回收的，我们需要自己手动的进行资源的释放。此时的**资源释放**，就需要声明在finally中。

   ```java
   package com.loong.exception1;
   import java.io.File;
   import java.io.FileInputStream;
   import java.io.FileNotFoundException;
   import java.io.IOException;
   public class trycatchtest {
   	public static void main(String[] args) {
   
   		FileInputStream fis = null;
   		try {
   			File file = new File("hello.txt");
   			fis = new FileInputStream(file);
   			
   			int data = 0;
   			data = fis.read();
   			while (data != -1) {
   				System.out.print((char) data);
   				data = fis.read();
   			}
   		} catch (FileNotFoundException e) {
   			// TODO 自动生成的 catch 块
   			e.printStackTrace();
   		}catch(IOException e) {
   			e.printStackTrace();
   		}finally {
   			try {
   				if(fis!=null)
   //				如果没文件，FileInputStream(file)会抛出FileNotFoundException 但是fis仍为null 
   //				故执行完catch后 在执行finally时，fis会是null，
   //				所以这里要判断一下，避免空指针异常
   				fis.close();
   			} catch (IOException e) {
   				// TODO 自动生成的 catch 块
   				e.printStackTrace();
   			}
   		}
   	}
   }
   //项目文件夹 右击 新建 文件 hello.txt
   ```

   

(4)其它：

* 体会1：使用try-catch-finally处理编译时异常，是得程序在编译时就不再报错，但是运行时仍可能报错。相当于我们使用try-catch-finally将一个编译时可能出现的异常，延迟到运行时出现。

 * 体会2：开发中，由于运行时异常比较常见，所以我们通常就不针对运行时异常编写try-catch-finally了。针对于编译时异常，我们说一定要考虑异常的处理。

 * try-catch-finally结构可以嵌套

* 可以进行 try-finally 配合使用(仅限于运行时异常——不用catch也行，java可以自己捕获)

  >**不捕获异常**时的情况:前面使用的异常都是**RuntimeException类或是它的子类**，这些类的异常的特点是：即使没有使用try和catch捕获，Java自己也能捕获，并且编译通过( 但运行时会发生异常使得程序运行终止 )。
  >
  >如果抛出的异常是IOException等类型的**非运行时异常，则必须捕获**，否则编译错误。也就是说，我们**必须处理编译时异常，将异常进行捕捉，转化为运行时异常**

```java
  //可以进行 try-finally 配合使用, 这种用法相当于没有捕获异常，
        //因此程序会直接崩掉/退出。应用场景，就是执行一段代码(try)，不管是否发生异常，
        //都必须执行(finally)某个业务逻辑
        try{
            int n1 = 10;
            int n2 = 0;
            System.out.println(n1 / n2);//ArithmeticException: / by zero
        }finally {
            System.out.println("执行了 finally..");//执行了
        }
        System.out.println("程序继续执行..");//未执行
```



### throws

"throws + 异常类型"写在方法的声明处。指明此方法执行时，可能会抛出的异常类型。（声明方法可能要抛出一个或多个的各种异常类）

一旦当方法体执行时，出现异常，仍会在异常代码处生成一个异常类的对象，此对象满足throws后异常类型时，就会被抛出。异常代码后续的代码，就不再执行！

* 如果一个方法(中的语句执行时)可能生成某种异常，但是并**不能确定如何处理这种异常，则此方法应显示地声明抛出异常**，表明该方法将不对这些异常进行处理，而**由该方法的调用者负责处理**。

* 在方法声明中用throws语句可以声明抛出异常的列表，throws后面的异常类型可以是方法中产生的异常类型，也可以是它的父类。

* **子类重写的方法抛出的异常类型不大于父类被重写的方法抛出的异常类型**

* 在**多态**的情况下，对methodA()方法的调用-**异常的捕获按父类声明的异常**处理。

    ```java
  import java.io.FileNotFoundException;
  import java.io.IOException;
  public class ThrowsTest2 {
  	public static void main(String[] args)  {
  		SuperClass s = new SubClass();
  		try {
  			s.method();
  		} catch (IOException e) {//在多态的情况下，异常的捕获按父类声明的异常处理 
  			//调用的是SubClass中的方法 抛出FileNotFoundException  父类的类型大，故可以接收
  			e.printStackTrace();
  		}
  	}
  }
  class SuperClass {
  	public void method() throws IOException{}
  }
  class SubClass extends SuperClass{
  	public void method()throws FileNotFoundException{}//异常类型 子<=父
  }
  ```

  

* 对于编译时异常，程序中必须处理，try--catch-finally和throws二选一

* 对于**运行时异常**，如果程序员没显式的处理异常，**默认throws**。

  

![throws处理机制图](http://101.34.218.64/JavaSE.assets/throws%E5%A4%84%E7%90%86%E6%9C%BA%E5%88%B6%E5%9B%BE.png)

```java
import java.io.File;
import java.io.FileInputStream;
import java.io.IOException;
public class ThrowsTest {
	public static void main(String[] args) throws IOException {method();}
//	public static void main(String[] args) {
//		try {
//			method();
//		} catch (IOException e) {
//			System.out.println("自己的处理");
//			e.printStackTrace();
//		}
//
//	}
	public static void method() throws IOException {method1();}
	public static void method1() throws IOException {method2();}
	public static void method2() throws IOException {
		File file = new File("1hello.txt");
		FileInputStream fis = new FileInputStream(file);//// 可能FileNotFoundException
		int data = fis.read();
		while (data != -1) {
			System.out.print((char) data);
			data = fis.read();//// 可能 IOException
		}
		fis.close();//// 可能 IOException
	}
}

```

### 对比两种处理方式

​	try-catch-finally:真正的将异常给处理掉了。

​	throws的方式只是将异常抛给了方法的调用者。并没真正将异常处理掉。  

### 开发中应该如何选择两种处理方式？

 * 如果父类中被重写的方法没throws方式处理异常，则子类重写的方法也不能使用throws，意味着如果子类重写的方法中异常，必须使用try-catch-finally方式处理。

 * 执行的方法a中，先后又调用了另外的几个方法，这几个方法是**递进**关系执行的。我们建议这**几个方法使用throws**的方式进行处理。而执行的**方法a可以考虑使用try-catch-finally**方式进行处理。

   ```java
   方法a（） {
       try{
        arg1= 方法1();
        arg2=方法2(arg1);//上一个方法的结果作为下一个方法的参数  递进关系
        方法3(arg2);
       }catch(Exception e){....}
       finally{ }
   }
   arg1 方法1（）throws XXXException{ }
   arg2 方法2（）throws XXXException{ }
   void 方法3（）throws XXXException{ }
   //每个小方法都抛给方法a 让它处理  方法A一旦有异常就停止后面的过程  因为取不到参数会影响下个方法 
   //不这样的后果：如果在每个小方法里处理掉了 比如方法1中异常处理了 方法1抛出异常终止了 而方法2仍执行，但参数没有 会出错
   ```

   

## 手动抛出异常：throw

Java异常类对象除在程序执行过程中出现异常时由系统自动生成并抛出，也可根据需要使用人工创建并抛出。

首先要生成异常类对象，然后通过throw语句实现抛出操作(提交给Java运行环境)。
IOException e = new IOException("IO错误");
throw e;
或者直接
throw IOException("IO错误");
可以抛出的异常必须是Throwable或其子类的实例

```java
public class ThrowTest {
	public static void main(String[] args) {
		Student stu = new Student();
		try {
			stu.regist(-1);
			System.out.println(stu);
		} catch (Exception e) {
			// TODO 自动生成的 catch 块
			e.printStackTrace();
		}
	}
}

class Student {
	private int id;

	public void regist(int id) {
		if (id > 0) {
			this.id = id;
		} else {

//			throw new RuntimeException("您输入的数据非法");//运行时异常 不用处理
			/*
			 * 输出：Exception in thread "main" java.lang.RuntimeException: 您输入的数据非法 at
			 * com.loong.exception1.Student.regist(ThrowTest.java:17) at
			 * com.loong.exception1.ThrowTest.main(ThrowTest.java:6)
			 */
			throw new Exception("您输入的数据非法");// 需要处理 在声明方法处声明抛出 在调用此方法的方法里处理
			/*
			 * java.lang.Exception: 您输入的数据非法 
			 * at com.loong.exception1.Student.regist(ThrowTest.java:28) 
			 * at com.loong.exception1.ThrowTest.main(ThrowTest.java:7)
			 */
		}
	}
}
```



## 用户自定义异常类

当程序中出现了某些”错误”，但该错误信息并没有在Throwable子类中描述处理，这个时候可以自己设计异常类，用于描述该错误信息。

* 一般地，用户自定义异常类都是RuntimeException的子类。
> 自定义异常类名(程序员自己写）继承Exception或RuntimeException。
> 若继承Exception为编译时异常，如果继承RuntimeExceptio为运行时异常。
> 把自定义异常做成 运行时异常，好处时，我们可以使用默认的处理机制，比较方便

* 自定义异常类通常需要编写几个重载的构造器。
* 自定义异常需要提供serialVersionUID。（串行版本标识，用于IO流中序列化标识类？后面学）
* 自定义的异常通过throw抛出。
* 自定义异常最重要的是异常类的名字，当异常出现时，可以根据名字判断异常类型。

```java
class FushuException extends Exception {
	private static final long serialVersionUID = 1L;
	public FushuException() {}
	public FushuException(String msg) {super(msg);}
}

public class ThrowTest {
	public static void main(String[] args) {
		Student stu = new Student();
		try {
			stu.regist(-1);
			System.out.println(stu);
		} catch (Exception e) {
			e.printStackTrace();
		}
	}
}
class Student {
	private int id;
	public void regist(int id) throws Exception {//如果自定义异常类继承RuntimeException，不需要声明throws
		if (id > 0) {
			this.id = id;
		} else {
			throw new FushuException("不能输入负数");
			/*
			 * com.loong.exception1.FushuException: 不能输入负数
			 * at com.loong.exception1.Student.regist(ThrowTest.java:37) 
			 * at com.loong.exception1.ThrowTest.main(ThrowTest.java:7)
			 */
		}
	}
}
```



## 一些总结

 ![异常处理的5个关键字](http://101.34.218.64/JavaSE.assets/%E5%BC%82%E5%B8%B8%E5%A4%84%E7%90%86%E7%9A%845%E4%B8%AA%E5%85%B3%E9%94%AE%E5%AD%97.png)

## 一首小诗

世界上最遥远的**距离**，是我在if里你在else里，似乎一直相伴又永远分离；
世界上最痴心的**等待**，是我当case你是switch，或许永远都选不上自己；
世界上最真情的**相依**，是你在try我在catch。无论你发神马脾气，我都默默承受，静静处理。到那时，再来期待我们的finally。

## 一些练习

```java
public class ReturnExceptionDemo {
	static void methodA() {
		try {
			System.out.println("进入方法A");
			throw new RuntimeException("制造异常");
		} finally {
			System.out.println("用A方法的finally");
		}
	}
	static void methodB() {
		try {
			System.out.println("进入方法B");
			return;
		} finally {
			System.out.println("调用B方法的finally");
		}
	}
	public static void main(String[] args) {
		try {
			methodA();
		} catch (Exception e) {
			System.out.println(e.getMessage());
		}
		methodB();
	}
}
/*
 * 注意 一定是先执行完finally再返回给调用的方法 
 * 进入方法A 用A方法的finally 制造异常 进入方法B 调用B方法的finally
 */

```

```java
/*
 * 编写应用程序EcmDef.java，接收命令行的两个参数，要求不能输入负数，计算
两数相除。
对 数 据 类 型 不 一 致 (NumberFormatException) 、 缺 少 命 令 行 参 数
(ArrayIndexOutOfBoundsException、除0(ArithmeticException)及输入负数(EcDef 自定义的异常)进行异常处理。
提示：
(1)在主类(EcmDef)中定义异常方法(ecm)完成两数相除功能。
(2)在main()方法中使用异常处理语句进行异常处理。
(3)在程序中，自定义对应输入负数的异常类(EcDef)。
(4)运行时接受参数 java EcmDef 20 10//args[0]=“20” args[1]=“10”
(5)Interger类的static方法parseInt(String s)将s转换成对应的int值。
如：int a=Interger.parseInt(“314”);//a=314;
 */
public class EcmDef {
	public static int ecm(int x, int y) throws EcDef {
		if (x < 0 || y < 0)throw new EcDef("分子或分母为负数了");
		return x / y;
	}
	public static void main(String[] args) {
		try {
			int args0 = Integer.parseInt(args[0]);
			int args1 = Integer.parseInt(args[1]);
			int result = ecm(args0, args1);
			System.out.println(result);
		} catch (NumberFormatException e) {
			System.out.println("数据类型不一致");
		} catch (ArrayIndexOutOfBoundsException e) {
			System.out.println("缺少命令行参数");
		} catch (ArithmeticException e) {
			System.out.println("除以0了");
		}
		catch (EcDef e) {
			System.out.println(e.getMessage());
		}
	}
}

class EcDef extends Exception {
	private static final long serialVersionUID = 1L;
	public EcDef() {}
	public EcDef(String msg) {super(msg);}
}
```



## 一些常见的辨析面试题


final、finally、finalize三者的区别？

类似：
throw 和 throws
	throw 表示**生成**一个异常对象,并抛出。声明在方法体内。后面跟 异常对象
	throws 属于异常处理的一种方式，声明在方法的声明处。 后面跟 异常类型

| 关键字 | 意义                     | 位置       | 后面跟的东西 |
| ------ | ------------------------ | ---------- | ------------ |
| throws | 异常处理的一种方法       | 方法声明处 | 异常类型     |
| throw  | 手动生成异常对象的关键字 | 方法体中   | 异常对象     |

Collection 和 Collections
String 、StringBuffer、StringBuilder
ArrayList 、 LinkedList
HashMap 、LinkedHashMap
重写、重载

结构不相似的：
抽象类、接口
== 、 equals()
sleep()、wait()



# 第8章 多线程

multithreading

## 基本概念：程序、进程、线程

### 程序、进程、线程

程序(program) ：为完成特定任务、用某种语言编写的一组指令的集合。即一段静态的代码，静态对象
进程(process)：正在运行的一个程序。进程作为资源分配的单位，系统在运行时会为每个进程分配不同的内存区域.

* 程序是静态的，进程是动态的

线程(thread):进程可进一步细化为线程，是一个程序内部的一条执行路径。
* 若一个进程同一时间**并行**执行多个线程，就是支持多线程的

* 线程作为**调度和执行的单位**，每个线程拥有**独立的运行栈和程序计数器(pc)**，线程切换的开销小

* 一个进程中的多个线程共享相同的内存单元/内存地址空间

  它们从同一堆中分配对象，可以访问相同的变量和对象。这就使得线程间通信更简便、高效。但多个线程操作共享的系统资源可能就会带来安全的隐患。

  >**每个线程，拥有自己独立的：栈、程序计数器**——每个线程都有一份
  >**多个线程，共享同一个进程中的结构：方法区、堆** ——每个进程一份，多个线程共享
  > ![](http://101.34.218.64/JavaSE.assets/JVM%E5%86%85%E5%AD%98%E5%8C%BA%E5%9F%9F.png)

* 一个Java应用程序java.exe，其实至少有三个线程：**main()主线程，gc()垃圾回收线程，异常处理线程**。当然如果发生异常，会影响主线程。

### 单核和多核

### 并发和并行

并行与并发
并行：多个CPU同时执行多个任务。比如：多个人同时做不同的事。
并发：一个CPU(采用时间片)同时执行多个任务。比如：秒杀、多个人做同一件事。（宏观上是同时发生的，但微观上是交替发生的）

### 使用多线程的优点

1. 提高应用程序的响应。对图形化界面更有意义，可增强用户体验。
2. 提高计算机系统CPU的利用率
3. 改善程序结构。将既长又复杂的进程分为多个线程，独立运行，利于理解和修改

### 何时需要多线程

* 程序需要同时执行两个或多个任务。
* 程序需要实现一些需要等待的任务时，如用户输入、文件读写操作、网络操作、搜索等。
* 需要一些后台运行的程序时。

## ==线程的创建和使用(重要)==
> //java.lang.Thread类
> class Thread implements Runnable
>
> 构造器：
> Thread()：创建新的Thread对象
> Thread(String threadname)：创建线程并指定线程实例名
> Thread(Runnable target)：指定创建线程的目标对象，它实现了Runnable接口中的run方法
> Thread(Runnable target, String name)：比上一个还可以设置线程名字
>
> void start() 使该线程开始执行；JVM调用该线程的 run 方法。如果线程已经启动，抛出IllegalThreadStateException -。 
>
> void run() 如果该线程是使用独立的 Runnable 运行对象构造的，则调用该 Runnable 对象的 run 方法；否则，该方法不执行任何操作并返回。 Thread 的子类应该重写该方法。 

**两种方式**
**方式一：继承Thread类，重写run方法**
**方式二：实现Runnable接口，重写run方法**(开发中更推荐使用)

### 方式一：继承Thread类的方式：

* 1. 创建一个**继承于Thread类的子类**
* 2. **重写Thread类的run()** --> 将此线程执行的操作声明在run()中
* 3. **创建Thread类的子类的对象**
* 4. 通过**线程对象调用start()**：start()作用：①启动当前线程 ② 调用当前线程的run()

> 注意：
> ①我们启动一个线程，**必须调用start()，不能调用run()的方式启动线程**(对象.run()只是调用了run(),没有启动线程)。
> 	如果自己手动调用run()方法，那么就只是普通方法，没有启动多线程模式。
> 	run()方法由JVM调用，什么时候调用，执行的过程控制都有操作系统的CPU调度决定。
> 	想要启动多线程，必须调用start方法。<img src="http://101.34.218.64/JavaSE.assets/start()%E6%96%B9%E6%B3%95.png" alt="start()方法" style="zoom:50%;" />
>
> ②如果**再启动一个**线程，必须**重新创建一个Thread子类的对象**，调用此对象的start()。
> 一个线程对象只能调用一次start()方法启动，如果重复调用了，则将抛出以上的异常“IllegalThreadStateException”。非法的进程状态异常  （因为进程已启动））

**技巧：使用Thread的匿名子类的匿名对象调用方法**

```java
new Thread(){
            @Override
            public void run() {
               //操作（自己的业务代码）
            }
        }.start();
```

代码示例：

```java
/**
 * 多线程的创建 方式一：继承于Thread类
 *
 * @author LoongKK
 * @create 2022/7/16-15:06
 */
//1.创建一个继承于Thread类的子类
class MyThread extends Thread {
    //2.重写Thread类的run() --> 将此线程执行的操作声明在run()中
    @Override
    public void run() {
        for (int i = 0; i < 100; i++) {
            for (int j = 0; j < 1000; j++) ;
            System.out.println("###[run]###");
        }
    }
}

public class ThreadTest {
    public static void main(String[] args) {
        //3. 创建Thread类的子类的对象
        MyThread myThread = new MyThread();
        //4. 通过此对象调用start()：①启动当前线程 ② 调用当前线程的run()
        myThread.start();
        for (int i = 0; i < 100; i++) {
            for (int j = 0; j < 1000; j++) ;//这句子延时 为了效果明显
            System.out.println("***[main]***");
        }
    }
}
//可以看到交替的输出run和main而不是先输出完run再输出main
```

```java
//创建两个线程，一个输出偶数 一个输出奇数——>肯定需要创建两个子类，都要重写不同的run()方法
public class ThreadDemo{
    public static void main(String[] args) {
        //比起"创建两个继承Thread的子类，再分别创建对象，然后调用start（）方法"，更推荐使用Thread的匿名子类的匿名对象调用方法
        new Thread(){
            @Override
            public void run() {
                for (int i = 0; i < 100; i++) {
                    for (int j = 0; j <1000 ; j++);
                   if(i%2==0) System.out.println(Thread.currentThread().getName()+"偶数"+i);
                }
            }
        }.start();
        new Thread(){
            @Override
            public void run() {
                for (int i = 0; i < 100; i++) {
                    for (int j = 0; j <1000 ; j++);
                    if(i%2==1) System.out.println(Thread.currentThread().getName()+":奇数"+i);
                }
            }
        }.start();
    }
}
```

小技巧：可以通过Thread.currentThread() .getXXX()获取当前线程的信息
	 static Thread currentThread()     返回对当前正在执行的线程对象的引用。 

```JAVA
//练习：创建三个窗口卖票 总票数100张
class Window  extends Thread{
    private static int ticket=100;//加了static  大致递减，还是有重复的票号！！——>存在线程安全问题
    @Override
    public void run() {
        while (true){
            if(ticket>0){
                System.out.println(getName()+"卖票，票号为："+ticket);
                ticket--;
            }
            else{
                break;
            }
        }
    }
}
public class WindowTest {
    public static void main(String[] args) {
        Window w1 = new Window();
        Window w2 = new Window();
        Window w3 = new Window();
        w1.setName("窗口1");
        w2.setName("窗口2");
        w3.setName("窗口3");
        w1.start();
        w2.start();
        w3.start();
    }
}
```

### 线程常用方法

Thread类中的常用的方法:

1. start():启动当前线程；调用当前线程的run()

2. run(): 通常需要重写Thread类中的此方法，将创建的线程要执行的操作声明在此方法中 

3. **static** Thread currentThread() 返回对当前正在执行的线程对象的引用。 
   在Thread子类中就是this，通常用于主线程和Runnable实现类

4. String getName():获取当前线程的名字

5. void setName(String name):设置当前线程的名字

6. **static** void yield():线程让步(释放当前cpu的执行权)
   暂停当前正在执行的线程，把执行机会让给优先级相同或更高的线程
   若队列中没有同优先级的线程，忽略此方法

7. join():在线程a中调用线程b的join(),此时线程a就进入阻塞状态，直到线程b完全执行完以后，线程a才结束阻塞状态。（让调用join的线程对象b先执行，a阻塞）
   当某个程序执行流中调用其他线程的 join() 方法时，调用线程将被阻塞，直到 join() 方法加入的 join 线程执行完为止。
   低优先级的线程也可以获得执行。
   需要处理InterruptedException

8. stop():已过时,不推荐使用。当执行此方法时，强制结束当前线程。
   
> ①线程完成任务后，会自动退出。
>
> ②还可以通过**使用变量**来控制run方法退出的方式停止线程，即**通知方式**
>
> ​	stop()可由**修改某些变量**以指示目标线程应该停止运行的代码来取代。目标线程应**定期检查**该变量，并且如果该变量指示它要停止运行，则**从其运行方法依次返回**。如果目标线程等待很长时间（例如基于一个条件变量），则应使用  `interrupt` 方法来中断该等待。
>
> 线程的终止示例代码
>
> <img src="http://101.34.218.64/JavaSE.assets/%E7%BA%BF%E7%A8%8B%E7%9A%84%E7%BB%88%E6%AD%A2%E7%A4%BA%E4%BE%8B%E4%BB%A3%E7%A0%81.png" alt="线程的终止示例代码" style="zoom:50%;" />

9. **static** void sleep(long millitime):让当前线程“睡眠”指定的millitime毫秒（）。在指定的millitime毫秒时间内，当前线程是阻塞状态。需要处理InterruptedException

10. boolean isAlive():判断当前线程是否存活

11. void interrupt() 中断此线程。并没有真正的结束线程 一般用于中断正在休眠的线程

12. void setPriority(int newPriority) 更改线程的优先级。在[1,10]之间的整型
    设置一个在[1,10]之间的整型的优先级：在Thread中有全局常量Thread.MIN_PRIORITY=1 Thread.MAX_PRIORITY=10 NORM_PRIORITY=5 默认优先级

13. int getPriority() 获取线程的优先级

```java
// 测试Thread类中的常用方法
class HelloThread extends Thread {
    public HelloThread() {
    }
    public HelloThread(String name) {//也可以通过此构造器 为线程设置名字
        super(name);
    }
    @Override
    public void run() {
        for (int i = 0; i < 100; i++) {
            //for (int j = 0; j < 1000; j++) ;
            try {
                sleep(15);
                if(i==90)interrupt();//会在主方法里catch一个线程中断异常 然后又继续被系统唤醒
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
           System.out.println(Thread.currentThread().getName() + ":" + i);//线程一 相当于下面这句
           //System.out.println(this.getName() + ":" + i);//线程一 this也可以省

        }
    }
}

public class ThreadMethodTest {
    public static void main(String[] args) {
        HelloThread h1 = new HelloThread();
        h1.setName("线程一");//也可以通过构造器HelloThread（"线程一"）
        //System.out.println(h1.getName());//输出线程h1的名字。run方法里则需通过Thread.currentThread()或this来调用getName
        h1.start();
        Thread.currentThread().setName("主线程main");//main主线程改名 main是静态方法，不能用this

        System.out.println(Thread.currentThread().getPriority());//获取的线程当前的的优先级 默认
        Thread.currentThread().setPriority(Thread.MIN_PRIORITY);//设置一个在[1,10]之间的整型的优先级 在Thread中有全局常量Thread.MIN_PRIORITY=1 Thread.MAX_PRIORITY=10
        System.out.println(Thread.currentThread().getPriority());//获取的线程当前的的优先级 更改后的
        for (int i = 0; i < 100; i++) {
            //for (int j = 0; j < 1000; j++) ;//用下面的sleep休眠来代替延时
            try {
                Thread.sleep(1);//单位：毫秒  主线程休眠
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
            System.out.println(Thread.currentThread().getName() + ":" + i);//main
            System.out.println("线程一的存活状态"+h1.isAlive());//线程一的存活状态
            if(i==80){
                try {
                    h1.join();//主线程中i=80时，在主线程中调用线程一的join(),此时主线程就进入阻塞状态，直到线程一完全执行完以后，线程主才结束阻塞状态。
                } catch (InterruptedException e) {//线程中断异常
                    e.printStackTrace();
                }
            }
        }
    }
}

```

### 方式二：实现Runnable接口的方式：

* 1. 创建一个实现了Runnable接口的类
* 2. 实现类去实现Runnable中的抽象方法：run()
* 3. 创建实现类的对象
* 4. 将此对象作为参数传递到Thread类的构造器中，创建Thread类的对象
* 5. 通过Thread类的对象调用start()：开启线程；调用Runnable接口实现类中的run()

     > Thread中的run():
     >
     > ```
     > @Override//也实现了Runnable接口中的run()。
     > public void run() {
     >     if (target != null) {
     >         target.run();
     >     }
     > }
     > 现在方式二直接实现Runnable接口中的run() 再把对象传进去——代理模式
     > ```

技巧：只启动一个线程时①new Thread(Runnable target).start()

new Thread(Runnable target,String name).start()

```
new Thread(new Window(),"窗口一").start();
```

②可以用Runnable接口的匿名实现类的匿名对象做Thread构造器的参数

```java
new Thread(new Runnable(){
    @Override
    public void run() {
        //操作
    }
}).start();
```

方式二代码示例：

```java
class MyThread implements Runnable {
    @Override
    public void run() {
        for (int i = 0; i < 100; i++) {
            try {
                Thread.sleep(50);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
            System.out.println(Thread.currentThread().getName());//此处不能用this.getName()了 因为MyThread不是继承的Thread，没有getName方法
        }
    }
}

public class Thread2Test {
    public static void main(String[] args) {
        MyThread myThread = new MyThread();
        Thread t1 = new Thread(myThread);//Thread(Runnable target)
        t1.setName("t1");
        t1.start();
        Thread t2 = new Thread(myThread);//创建多个(同一个run方法的)线程用可以用同一个"实现类的对象"，只要把它当构造器参数创建新的Thread类对象即可
        t2.setName("t2");
        t2.start();
        for (int i = 0; i < 100; i++) {
            try {
                Thread.sleep(50);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
            System.out.println(Thread.currentThread().getName());

        }
    }
```

```java
//练习：创建三个窗口卖票 总票数100张 使用方式二
class Window  implements Runnable{
    //同一个Runnable类对象，三个线程执行，共用此对象的属性。不用加static
    private int ticket=100;//不用加static  但还是有重复的票号！！——>线程安全问题
    @Override
    public void run() {
        while (true){
            if(ticket>0){
                System.out.println(Thread.currentThread().getName()+"卖票，票号为："+ticket);
                ticket--;
            }
            else{
                break;
            }
        }
    }
}
public class WindowTest2 {
    public static void main(String[] args) {
      Window w=new Window();
      new Thread(w,"窗口一").start();
      new Thread(w,"窗口二").start();
      new Thread(w,"窗口三").start();
    }
}

```



### 两种方式的对比：

* 开发中：优先选择**实现Runnable接口的方式**
     原因：
     * 实现的方式避免了类的单继承性的局限性（方式一继承了Thread后不能继承其它类）；
     * 实现的方式更适合来处理**多个线程共享数据**的情况
       （多个线程可以共享同一个接口实现类的对象，非常适合多个相同线程来处理同一份资源。）。
     
* 联系：public class Thread implements Runnable
* 相同点：两种方式都需要重写run(),将线程要执行的逻辑声明在run()中；
          目前两种方式，要想启动线程，都是调用的Thread类中的start()。
* 区别：
      继承Thread：线程代码存放Thread子类run方法中。
      实现Runnable：线程代码存在接口的子类(实现类)的run方法。

### 线程的调度

调度策略：①时间片②抢占式：高优先级的线程抢占CPU

java的调度方法：

* **同优先级线程**组成先进先出队列（先到先服务），使用**时间片**策略；

* 对**高优先级**，使用**优先调度的抢占式**策略

### 线程的优先级

MAX_PRIORITY：10
MIN _PRIORITY：1
NORM_PRIORITY：5  -->默认优先级

如何获取和设置当前线程的优先级：

* void setPriority(int newPriority) 更改线程的优先级。在[1,10]之间的整型
* int getPriority() 获取线程的优先级

说明：高优先级的线程要抢占低优先级线程cpu的执行权。但是**只是从概率上讲，高优先级的线程高概率的情况下被执行**。并不意味着只当高优先级的线程执行完以后，低优先级的线程才执行。

### 线程的分类

Java中的线程分为两类：一种是**守护线程**，一种是**用户线程**。
* 它们在几乎每个方面都是相同的，唯一的区别是判断JVM何时离开。
* **守护线程**是用来服务用户线程的，通过在start()方法**前**调用
*	thread.setDaemon(true)可以把一个用户线程变成一个守护线程。
* Java垃圾回收就是一个典型的守护线程。
* **若JVM中都是守护线程，当前JVM将退出**。
* 形象理解：兔死狗烹，鸟尽弓藏

## 线程的生命周期

JDK中用Thread.State类定义了线程的六种状态,可以用getState()获取

> API中内容：
>
> public static enum Thread.State
> extends Enum<Thread.State>线程状态。线程可以处于下列状态之一： 
>
> | 状态                   | 含义                                                         |
> | ---------------------- | ------------------------------------------------------------ |
> | NEW  新建              | 至今尚未启动的线程处于这种状态。                             |
> | RUNNABLE 运行          | 正在 Java 虚拟机中执行的线程处于这种状态。                   |
> | BLOCKED 阻塞           | 受阻塞并等待某个监视器锁的线程处于这种状态。                 |
> | WAITING 等待           | 无限期地等待另一个线程来执行某一特定操作的线程处于这种状态。 |
> | TIMED_WAITING 超时等待 | 等待另一个线程来执行取决于指定等待时间的操作的线程处于这种状态。 |
> | TERMINATED  终止       | 已退出的线程处于这种状态。                                   |
>
> 在给定时间点上，一个线程只能处于一种状态。这些状态是虚拟机状态，它们并没有反映所有操作系统线程状态。
>
> ![Java线程的状态](http://101.34.218.64/JavaSE.assets/Java%E7%BA%BF%E7%A8%8B%E7%9A%84%E7%8A%B6%E6%80%81.png)
>
> （图源《Java 并发编程艺术》4.1.4 节）

要想实现多线程，必须在主线程中创建新的线程对象。
Java语言使用Thread类及其子类的对象来表示线程，在它的一个完整的生命周期中通常要经历如下的五种状态：

* 新建(创建)： 当一个Thread类或其子类的对象被声明并创建时，新生的线程对象处于新建状态
* 就绪：处于新建状态的线程被start()后，将进入线程队列等待CPU时间片，此时它已具备了运行的条件，只是没分配到CPU资源
* 运行：当就绪的线程被调度并获得CPU资源时,便进入运行状态， run()方法定义了线程的操作和功能
* 阻塞：在某种特殊情况下，被人为挂起或执行输入输出操作时，让出 CPU 并临时中止自己的执行，进入阻塞状态
* 死亡(终止)：线程完成了它的全部工作或线程被提前强制性地中止或出现异常导致结束

线程的状态转换图

![线程的状态转换图_宋红康](http://101.34.218.64/JavaSE.assets/%E7%BA%BF%E7%A8%8B%E7%9A%84%E7%8A%B6%E6%80%81%E8%BD%AC%E6%8D%A2%E5%9B%BE_%E5%AE%8B%E7%BA%A2%E5%BA%B7.png)

![](http://101.34.218.64/JavaSE.assets/%E7%BA%BF%E7%A8%8B%E7%9A%84%E7%8A%B6%E6%80%81%E8%BD%AC%E6%8D%A2%E5%9B%BE_%E9%9F%A9%E9%A1%BA%E5%B9%B3.png)

说明：
1.生命周期关注两个概念：状态、相应的方法
2.关注：状态a-->状态b:哪些方法执行了（回调方法）
        某个方法主动调用：状态a-->状态b
3.阻塞：临时状态，不可以作为最终状态
  死亡：最终状态

## ==线程的同步(重要)==

### 线程安全问题

 多线程出现了安全问题(例如前面的窗口卖票问题、单例模式中的懒汉式都出现了线程安全问题)

如何找问题，即代码是否存在线程安全？
（1）明确哪些代码是多线程运行的代码
（2）明确多个线程是否有共享数据
（3）明确多线程运行代码中是否有多条语句操作共享数据

问题的原因：当多条语句在操作同一个线程共享数据时，一个线程对多条语句只执行了一部分，还没有执行完，另一个线程参与进来执行。导致共享数据的错误。

解决办法：**对多条操作共享数据的语句，只能让一个线程都执行完，在执行过程中，其他线程不可以参与执行。(即所有操作共享数据的这些语句都要放在同步范围中)**

Java对于多线程的安全问题提供了专业的解决方式：**同步机制**

### 方式一：同步代码块 synced block

​    `
​    synchronized (同步监视器){
​    // 需要被同步的代码；
​    }
​    `

synchronized  v. (使)同步

**同步代码块的锁**：自己指定，很多时候也是指定为this或类名.class
在**实现Runnable接口**创建多线程的方式中，我们可以考虑使**用this**充当同步监视器。
在**继承Thread类**创建多线程的方式中，慎用this充当同步监视器，考虑**使用当前类(synchronized(当前类类名.class){ })**充当同步监视器。

### 方式二：同步方法 synced method

如果操作共享数据的代码完整的声明在一个方法中，我们不妨将此方法声明同步的。

synchronized还可以放在方法声明中，表示整个方法为同步方法

`public synchronized void method (String name){
		…
}`

Java中的每一个对象都有一个内部锁。 如果一个方法用 synchronized 关键字声明，那么对象的锁将保护整个方法。也就是说，要调用该方法， 线程必须获得内部的对象锁。

将静态方法声明为 synchronized 也是合法的。如果调用这种方法，该方法获得相关的类对象的内部锁。例如， 如果 Bank 类有一个静态同步的方法，那么当该方法被调用时，Bank.class对象的锁被锁住

同步方法仍然涉及到同步监视器，只是不需要我们显式的声明。

*  非静态的同步方法，同步监视器是：this
*     静态的同步方法，同步监视器是：当前类本身

(也可普通方法的方法体再用同步块包起来,可以自定义锁，还可以不必为静态从而可以调用非静态)

### 两种方式的细节说明

说明：
1.**操作共享数据的代码，即为需要被同步的代码**。  -->不能包含代码多了，也不能包含代码少了。
	范围太大：没发挥多线程的功能。 范围太小：没锁住所有有安全问题的代码
2.共享数据：多个线程共同操作的变量。比如：ticket就是共享数据。
3.同步监视器，俗称：**锁**。互斥锁(有些人也叫它同步锁)。任何一个类的对象，都可以充当锁。
   要求：**使用同一个资源的多个线程必须要共用同一把锁**。必须确保使用同一个资源的多个线程共用一把锁，这个非常重要，否则就
无法保证共享资源的安全

关键字synchronized与对象的互斥锁联系，当某个对象用synchronized修饰时，表明该对象在任一时刻只能由一个线程访问。

* **同步代码块的锁**：自己指定，很多时候也是指定为this或类名.class
    在**实现Runnable接口**创建多线程的方式中，我们可以考虑使**用this**充当同步监视器。
    在**继承Thread类**创建多线程的方式中，慎用this充当同步监视器(多个线程公用一个this时可以)，考虑**使用当前类(synchronized(当前类类名.class){ })**充当同步监视器。
> 补充： 类也是对象 。`java.lang.Class<T>` 。在Java中，每个class都有一个相应的Class对象。也就是说，当我们编写一个类，编译完成后，在生成的.class文件中，就会产生一个Class对象，用于表示这个类的类型信息。A.class 其实返回的是一个类A的Class对象

* **同步方法的锁：非静态方法（this）、静态方法（类名.class）**

    **非静态的同步方法 默认锁对象为this**(当前类的 对象)
    **静态(static修饰)的同步方法 默认锁对象为当前类本身** 类名.class

### 两种方式的代码示例

```java
package com.loong.synchronized_;

import java.lang.reflect.Method;

/**
 * 三个窗口卖票 （使用同步）
 * Window1-同步代码块处理实现 Runnable 的线程安全问题
 * Window2-同步代码块处理继承 Thread 类的线程安全问题
 * Window3-同步方法处理实现 Runnable 的线程安全问题
 * Window4-同步方法处理继承 Thread 类的线程安全问题
 *
 * @author LoongKK
 * @date 2022/7/17
 */
//Window1-同步代码块处理实现 Runnable 的线程安全问题
class Window1 implements Runnable {
    private int ticket = 100;
    private Object obj = new Object();//要放在run方法外 多个线程必须要共用同一把锁
    @Override
    public void run() {
        while (true) {
            //synchronized(obj)//任何一个类的对象，都可以充当锁
            synchronized (this) {//在实现Runnable接口创建多线程的方式中，一般使用this充当同步监视器。(window1的对象w)
                if (ticket > 0) {
                    try {
                        Thread.sleep(50);
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                    System.out.println(Thread.currentThread().getName() + "卖票，票号为：" + ticket);
                    ticket--;
                } else {
                    break;
                }
            }
        }
    }
}

//Window2-同步代码块处理继承 Thread 类的线程安全问题
class Window2 extends Thread {
    private static int ticket = 100;
    private static Object obj = new Object();//静态 才能多个共享一个
    @Override
    public void run() {
        while (true) {
            //synchronized (this){//错误 不可以用this this指w1，w2，w3三个对象
            //synchronized (obj){//正确 任何一个类的对象，都可以充当锁
            synchronized (Window2.class) {// 在继承Thread类创建多线程的方式中，慎用this充当同步监视器，考虑使用当前类充当同步监视器。类名.class是Class的一个对象
                if (ticket > 0) {
                    System.out.println(getName() + "卖票，票号为：" + ticket);
                    ticket--;
                } else {
                    break;
                }
            }
        }
    }
}

//Window3-同步方法处理实现 Runnable 的线程安全问题
class Window3 implements Runnable {
    private int ticket = 100;
    @Override
    public void run() {
        while (true) {
            method();
        }
    }
    private synchronized void method() {//监视器默认this
        if (ticket > 0) {
            try {
                Thread.sleep(50);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
            System.out.println(Thread.currentThread().getName() + "卖票，票号为：" + ticket);
            ticket--;
        }
    }
}

//Window4-同步方法处理继承 Thread 类的线程安全问题
class Window4 extends Thread {
    private static int ticket = 100;
    private boolean loop=true;

    public void setLoop(boolean loop) {
        this.loop = loop;
    }
    @Override
    public void run() {
        while (loop) {
            method();
        }
    }
    //private synchronized void method() {//错误 非静态同步方法默认this  这里不唯一 w1,w2,w3
    //private static synchronized void method() {//静态同步方法默认 类名.class
        private void method() {//还可以方法中使用同步代码块把方法体包起来 这样可以使用非静态属性和方法了
            synchronized (Window4.class) {
                if (ticket > 0) {
                    try {
                        Thread.sleep(50);
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                    System.out.println(Thread.currentThread().getName() + "卖票，票号为：" + ticket);
                    ticket--;
                } else setLoop(false);
            }
        }
}

public class WindowTestSync {
    public static void main(String[] args) {

//        Window1 w = new Window1();
//        new Thread(w, "窗口一").start();
//        new Thread(w, "窗口二").start();
//        new Thread(w, "窗口三").start();

//        Window2 w1 = new Window2();
//        Window2 w2 = new Window2();
//        Window2 w3 = new Window2();
//        w1.setName("窗口1");
//        w2.setName("窗口2");
//        w3.setName("窗口3");
//        w1.start();
//        w2.start();
//        w3.start();

//        Window3 w = new Window3();
//        new Thread(w, "窗口一").start();
//        new Thread(w, "窗口二").start();
//        new Thread(w, "窗口三").start();

        Window4 w1 = new Window4();
        Window4 w2 = new Window4();
        Window4 w3 = new Window4();
        w1.setName("窗口1");
        w2.setName("窗口2");
        w3.setName("窗口3");
        w1.start();
        w2.start();
        w3.start();
    }
}
```

```java
package com.loong.synchronized_;

import com.sun.org.apache.bcel.internal.generic.NEW;

/*
 * 单例模式-懒汉式 改进版
 */
public class SingletonTest {
    public static void main(String[] args) {
        new Thread() {
            @Override
            public void run() {
                    System.out.println(this.getName() + Singleton.getInstance());
            }
        }.start();
        new Thread() {
            @Override
            public void run() {
                    System.out.println(this.getName() + Singleton.getInstance());
            }
        }.start();
        // Singleton instance=Singleton.getInstance();

    }
}

class Singleton {
    private static Singleton instance ;

    private Singleton() {
    }
//    public  static Singleton getInstance() {
//        synchronized(Singleton.class) {
//            if (instance == null) instance = new Singleton();
//        }
//        return instance;
//    }

    public static Singleton getInstance() {
        //这里在同步代码块外和同步代码块内进行了两次判空，这种懒汉式写法叫做双重检验锁（Double Check Lock）。
        //这种方式效率更高
        if (instance == null) {//相当于 立个牌子 告诉新来的线程 有对象了 勿念
            synchronized (Singleton.class) {
                if (instance == null) instance = new Singleton();
            }
        }
        return instance;
    }
//    public static synchronized Singleton getInstance() {//方式二
//        if (instance == null) {
//            try {
//                Thread.sleep(50);//休眠 延时 使线程安全问题现象明显
//            } catch (InterruptedException e) {
//                e.printStackTrace();
//            }
//            instance = new Singleton();//在方法中创建一个对象 初始化instance 如果不进行改进 多次调用会产生线程安全问题
//        }
//        return instance;
//    }
}
```

### 释放锁的操作

* 当前线程的同步方法、同步代码块执行结束。
* 当前线程在同步代码块、同步方法中遇到break、return终止了该代码块、该方法的继续执行。
* 当前线程在同步代码块、同步方法中出现了未处理的Error或Exception，导致异常结束。
* 当前线程在同步代码块、同步方法中执行了线程对象的wait()方法，当前线程暂停，并释放锁。

### 不会释放锁的操作

* 线程执行同步代码块或同步方法时，程序调用Thread.sleep()、Thread.yield()方法暂停当前线程的执行
* 线程执行同步代码块时，其他线程调用了该线程的suspend()方法将该线程挂起，该线程不会释放锁（同步监视器）。
	应尽量避免使用suspend()和resume()来控制线程,方法不推荐使用

### 线程的死锁

线程的死锁问题
妈妈：你先完成作业，才让你玩手机；小明：你先让我玩手机，我才完成作业。
**多个线程都占用了对方的锁资源，但不肯相让，导致了死锁。**
不同的线程分别占用对方需要的同步资源不放弃，都在等待对方放弃自己需要的同步资源，就形成了线程的死锁
出现死锁后，不会出现异常，不会出现提示，只是所有的线程都处于阻塞状态，无法继续

解决方法：
专门的算法、原则
尽量减少同步资源的定义
尽量避免嵌套同步
```java
//1. 如果 flag 为 T, 线程 A 就会先得到/持有 o1 对象锁, 然后尝试去获取 o2 对象锁
//2. 如果线程 A 得不到 o2 对象锁，就会 Blocked
//3. 如果 flag 为 F, 线程 B 就会先得到/持有 o2 对象锁, 然后尝试去获取 o1 对象锁
//4. 如果线程 B 得不到 o1 对象锁，就会 Blocked
run(){
  if (flag) {
	synchronized (o1) {//对象互斥锁, 下面就是同步代码
		System.out.println(Thread.currentThread().getName() + " 进入 1");
		synchronized (o2) { // 这里获得 li 对象的监视权
			System.out.println(Thread.currentThread().getName() + " 进入 2");
		}
	}
} else {
	synchronized (o2) {
		System.out.println(Thread.currentThread().getName() + " 进入 3");
		synchronized (o1) { // 这里获得 li 对象的监视权
			System.out.println(Thread.currentThread().getName() + " 进入 4");
		}
  }
 }
    //可能出现一个线程持有o1的不到o2 另一个持有o2得不到o1
```

```java
//DeadLock

class A {
	public synchronized void foo(B b) {
		System.out.println("当前线程名: " + Thread.currentThread().getName()
				+ " 进入了A实例的foo方法"); // ①
		try {
			Thread.sleep(200);
		} catch (InterruptedException ex) {
			ex.printStackTrace();
		}
		System.out.println("当前线程名: " + Thread.currentThread().getName()
				+ " 企图调用B实例的last方法"); // ③
		b.last();
	}

	public synchronized void last() {
		System.out.println("进入了A类的last方法内部");
	}
}

class B {
	public synchronized void bar(A a) {
		System.out.println("当前线程名: " + Thread.currentThread().getName()
				+ " 进入了B实例的bar方法"); // ②
		try {
			Thread.sleep(200);
		} catch (InterruptedException ex) {
			ex.printStackTrace();
		}
		System.out.println("当前线程名: " + Thread.currentThread().getName()
				+ " 企图调用A实例的last方法"); // ④
		a.last();
	}

	public synchronized void last() {
		System.out.println("进入了B类的last方法内部");
	}
}

public class DeadLock implements Runnable {
	A a = new A();
	B b = new B();

	public void init() {
		Thread.currentThread().setName("主线程");
		// 调用a对象的foo方法
		a.foo(b);
		System.out.println("进入了主线程之后");
	}

	public void run() {
		Thread.currentThread().setName("副线程");
		// 调用b对象的bar方法
		b.bar(a);
		System.out.println("进入了副线程之后");
	}

	public static void main(String[] args) {
		DeadLock dl = new DeadLock();
		new Thread(dl).start();
		dl.init();
	}
}
```

### 方式三：Lock锁  -JDK5.0新增

* 从JDK 5.0开始，Java提供了更强大的线程同步机制——通过显式定义同步锁对象来实现同步。同步锁使用Lock对象充当。

* **java.util.concurrent.locks.Lock接口是控制多个线程对共享资源进行访问的工具**。锁提供了对共享资源的独占访问，每次只能有一个线程对Lock对象加锁，线程开始访问共享资源之前应先获得Lock对象。

  • void lock( )获取这个锁；如果锁同时被另一个线程拥有则发生阻塞。
  • void unlock( )释放这个锁。

* ReentrantLock (可重入锁)类实现了 Lock ，它拥有与 synchronized 相同的并发性和内存语义，在实现线程安全的控制中，比较常用的是ReentrantLock，可以显式加锁、释放锁。

  • ReentrantLock( )构建一个可以被用来保护临界区的可重入锁。
  • ReentrantLock(boolean fair )构建一个带有公平策略的锁。一个公平锁偏爱等待时间最长的线程。 但是，这一公平
  的保证将大大降低性能。 所以， 默认情况下， 锁没有被强制为公平的。

```java
class A{
	private final ReentrantLock lock = new ReenTrantLock();
	public void m(){
		lock.lock();
		try{
			//保证线程安全的代码;
		}
		finally{
			lock.unlock();
		}
	}
    /*也可以用来同步代码块
    lock.lock();
		try{
			//保证线程安全的代码;
		}
		finally{
			lock.unlock();
		}*/
}
注意：如果同步代码有异常，要将unlock()写入finally语句块
```



```java
import java.util.concurrent.locks.ReentrantLock;

/**
 * 解决线程安全问题的方式三 Look锁
 */
class Window implements Runnable {
    private int ticket = 100;
    //①实例化RenntrantLock
    ReentrantLock lock=new ReentrantLock(true);
    @Override
    public void run() {
        while (true) {
            //②调用锁定方法lock()
            lock.lock();
            try {//try-finally结构
                //try中是同步代码
                if (ticket > 0) {
                    try {
                        Thread.sleep(10);
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                    System.out.println(Thread.currentThread().getName() + "售票，票号：" + ticket--);
                }
                else break;
            } finally {
                //调用解锁方法unlock()
                lock.unlock();
            }
        }
    }
}

public class LockTest {
    public static void main(String[] args) {
        Window w = new Window();
        new Thread(w,"窗口一").start();
        new Thread(w,"窗口二·").start();
        new Thread(w,"窗口三").start();
    }
}
```

```java
import java.util.concurrent.locks.ReentrantLock;
/**
 * 银行有一个账户。
 * 有两个储户分别向同一个账户存3000元，每次存1000，存3次。每次存完打印账户余额
 */
class Account{
    private double balance;//余额
    ReentrantLock lock = new ReentrantLock(true);
    public Account(double balance){
        this.balance=balance;
    }
    //存钱
    public void deposit(double amt){
        if(amt>0){
            lock.lock();
            try {
                balance += amt;
                try {
                    Thread.sleep(50);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
                System.out.println(Thread.currentThread().getName() + "存钱成功。余额：" + balance);
            }finally {
                lock.unlock();
            }
        }
    }
}
class Customer extends Thread{
    private Account acct;
    public Customer(Account acct) {
        this.acct = acct;
    }

    @Override
    public void run() {
        for (int i = 0; i < 3; i++) {
            acct.deposit(1000);
        }
    }
}
public class AccountTest {
    public static void main(String[] args) {
        Account acct=new Account(0);
        Customer c1=new Customer(acct);
        Customer c2=new Customer(acct);
        c1.setName("甲");
        c2.setName("乙");
        c1.start();
        c2.start();

    }
}
```



### synchronized 与 Lock的异同？

* 相同：二者都可以解决线程安全问题

* 不同：synchronized机制在执行完相应的同步代码以后，自动的释放同步监视器

  Lock需要手动的启动同步（lock()，同时结束同步也需要手动的实现（unlock()）

### 同步方式利弊：

好处：解决了线程安全问题

坏处：操作同步代码时，只能有一个线程参与，其它线程等待，**相当于是一个单线程的过程**（执行效率降低）

### 开发中使用的优先顺序：

* Lock ---> 同步代码块（已经进入了方法体，分配了相应资源 ) ---> 同步方法（在方法体之外)



## 线程的通信

1.线程通信涉及到的三个方法：

* wait():一旦执行此方法，**当前线程**就进入**阻塞**状态(直到另一线程对该对象发出 notify(或notifyAll) 为止)，**并释放同步监视器**。

* notify():一旦执行此方法，就**会唤醒被wait的(等待该对象监控权的)一个线程**。如果有多个线程被wait，就**唤醒优先级高的那个**。

  当前线程被notify后，要重新获得监控权，然后从断点处继续代码的执行

* notifyAll():一旦执行此方法，就会**唤醒所有被wait(等待该对象监控权的)的线程**。

2.说明：

* 1.wait()，notify()，notifyAll()三个方法**必须使用在同步代码块或同步方法中**。

* 2.wait()，notify()，notifyAll()三个方法的调用者**必须是同步代码块或同步方法**中的**同步监视器**。(对象名.xxx())

  这三个方法**只有在synchronized方法或synchronized代码块中才能使用**，否则会报java.lang.IllegalMonitorStateException异常。

  这三个方法**必须有锁对象调用**（调用方法的必要条件：当前线程必须具有对该对象的监控权（加锁）），而任意对象都可以作为synchronized的同步锁，因此这三个方法只能在Object类中声明

* 3.wait()，notify()，notifyAll()三个方法是定义在**java.lang.Object**类中。

例 题
使用两个线程打印 1-100。线程1, 线程2 **交替**打印

```java
/**
 * 例题 使用两个线程打印 1-100。线程1, 线程2 交替打印
 */
class Communication implements Runnable {
    int i = 1;
    public void run() {
        while (true) {
            synchronized (this) {
                notify();//唤醒另一个阻塞的线程 省略了this 如果自定义一个object来做监视器，那这里也要换
                if (i <= 100) {
                    System.out.println(Thread.currentThread().getName() +
                            ":" + i++);
                } else
                    break;
                try {
                    wait();//当前阻塞 释放同步监视器 省略了this
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }
        }
    }
}
public class WaitTest {
    public static void main(String[] args) {
        Communication c1=new Communication();
        new Thread(c1).start();
        new Thread(c1).start();
    }
}
```

生产者/消费者问题

```java
/**
 * 生产者/消费者问题
 * 生产者(Productor)将产品交给店员(Clerk)，而消费者(Customer)从店员处
 * 取走产品，店员一次只能持有固定数量的产品(比如:20），如果生产者试图
 * 生产更多的产品，店员会叫生产者停一下，如果店中有空位放产品了再通
 * 知生产者继续生产；如果店中没有产品了，店员会告诉消费者等一下，如
 * 果店中有产品了再通知消费者来取走产品。
 *
 * @author LoongKK
 * @create 2022/7/18-8:25
 */
class Productor implements Runnable {
    private Clerk clerk;
    public Productor(Clerk clerk) {
        this.clerk = clerk;
    }
    @Override
    public void run() {
        System.out.println(Thread.currentThread().getName() + ":开始生成产品。。。");
        while (true) {
            try {
                Thread.sleep((int) (Math.random() * (200 - 50 + 1) + 50));
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
            //把延时放同步块外面。放里面会导致时间太快 虽然notify唤醒了其它线程 但是监视器还是在自己手里
            synchronized (clerk) {
                if (clerk.forProductor()) {
                    produceProduct();
                    clerk.notifyAll();
                } else {
                    try {
                        clerk.wait();
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                }
            }
        }
    }

    private void produceProduct() {
        System.out.println(Thread.currentThread().getName() + "生产一件产品");
        clerk.setProductCount(clerk.getProductCount() + 1);
    }
}

class Customer implements Runnable {
    private Clerk clerk;

    public Customer(Clerk clerk) {
        this.clerk = clerk;
    }

    @Override
    public void run() {
        System.out.println(Thread.currentThread().getName() + ":开消费产品。。。");
        while (true) {
            try {
                Thread.sleep((int) (Math.random() * (200 - 50 + 1) + 50));
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
            synchronized (clerk) {
                if (clerk.forCustomer()) {
                    consumeProduct();
                    clerk.notifyAll();
                } else {
                    try {
                        clerk.wait();
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                }
            }
        }
    }
    private void consumeProduct() {
        System.out.println(Thread.currentThread().getName() + "消费一件产品");
        clerk.setProductCount(clerk.getProductCount() - 1);
    }
}

class Clerk {
    private int productCount = 0;
    public int getProductCount() {
        return productCount;
    }
    public void setProductCount(int productCount) {
        this.productCount = productCount;
    }

    //如果生产者试图 生产更多的产品，店员会叫生产者停一下，如果店中有空位放产品了再通知生产者继续生产；
    public boolean forProductor() {
        if (productCount < 20) {
            System.out.println("店员：当前产品数量:" + productCount + " " + "可以生产");
            return true;
        } else {
            System.out.println("店员：当前产品数量:" + productCount + " " + "暂停生产");
            return false;
        }
    }

    // 如果店中没有产品了，店员会告诉消费者等一下，如果店中有产品了再通知消费者来取走产品。
    public boolean forCustomer() {
        if (productCount > 0) {
            System.out.println("店员：当前产品数量:" + productCount + " " + "消费者可以取走产品");
            return true;
        } else {
            System.out.println("店员：当前产品数量:" + productCount + " " + "供货不足，敬请期待");
            return false;
        }
    }
}


public class ProductTest {
    public static void main(String[] args) {
        Clerk clerk = new Clerk();
        Productor p = new Productor(clerk);
        Customer c = new Customer(clerk);
        Customer c2 = new Customer(clerk);
        new Thread(p, "生产者1").start();
        new Thread(c, "消费者1").start();
        new Thread(c, "消费者2").start();
    }
}
```

```java
//ppt上给的
class Clerk { // 售货员
    private int product = 0;

    public synchronized void addProduct() {
        if (product >= 20) {
            try {
                wait();
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        } else {
            product++;
            System.out.println("生产者生产了第" + product + "个产品");
            notifyAll();
        }
    }
    public synchronized void getProduct() {
        if (this.product <= 0) {
            try {
                wait();
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        } else {
            System.out.println("消费者取走了第" +
                    product + "个产品");
            product--;
            notifyAll();
        }
    }
}
class Productor implements Runnable { // 生产者
    Clerk clerk;
    public Productor(Clerk clerk) {
        this.clerk = clerk;
    }
    public void run() {
        System.out.println("生产者开始生产产品");
        while (true) {
            try {
                Thread.sleep((int) Math.random() * 1000);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
            clerk.addProduct();
        }
    }
}
class Consumer implements Runnable { // 消费者
    Clerk clerk;
    public Consumer(Clerk clerk) {
        this.clerk = clerk;
    }
    public void run() {
        System.out.println("消费者开始取走产品");
        while (true) {
            try {
                Thread.sleep((int) Math.random() * 1000);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
            clerk.getProduct();
        }
    }
}
public class ProductTest1 {
    public static void main(String[] args) {
        Clerk clerk = new Clerk();
        Thread productorThread = new Thread(new Productor(clerk));
        Thread consumerThread = new Thread(new Consumer(clerk));
        productorThread.start();
        consumerThread.start();
    }
}
```



## JDK5.0新增线程创建方式

### 新增方式一：实现Callable接口，重写call()
(Runnable重写run Callabler重写call 都是前几个字母)
与使用Runnable相比， Callable功能更强大些

```java
//API中的Callable
package java.util.concurrent;
@FunctionalInterface
public interface Callable<V> {
    /**
     * Computes a result, or throws an exception if unable to do so.
     计算结果，如果无法计算结果，则抛出一个异常。
     * @return computed result 返回结果
     * @throws Exception if unable to compute a result
     */
    V call() throws Exception;//定义了一个不带任何参数的叫做 call 的方法
}
```



* 相比run()方法，**可以有返回值**

* 方法**numThread**

* **支持泛型的返回值**

* 需要**借助FutureTask类**，比如获取返回结果用get()

  > Future接口
  >
  > * 可以对具体Runnable、Callable任务的执行结果进行取消、查询是否完成、获取结果等。
  >
  > * FutrueTask是Futrue接口的唯一的实现类
  > * FutureTask **同时实现了Runnable, Future接口**。它**既可以作为Runnable被线程执行，又可以作为Future得到Callable的返回值**

步骤：

1.创建一个实现Callable的实现类
2.实现call方法，将此线程需要执行的操作声明在call()中
3.创建Callable接口实现类的对象
4.将此Callable接口实现类的对象作为传递到FutureTask构造器中，创建FutureTask的对象
5.将FutureTask的对象作为参数传递到Thread类的构造器中，创建Thread对象，并调用start()
6.获取Callable中call方法的返回值
   get(）的返回值即为FutureTask构造器参数Callable实现类重写call()的返回值。get需要处理异常

代码示例：

```java
package com.loong.thread3;
import java.util.concurrent.Callable;
import java.util.concurrent.ExecutionException;
import java.util.concurrent.FutureTask;

//1.创建一个实现Callable的实现类
class NumThread implements Callable {
    //2.实现call方法，将此线程需要执行的操作声明在call()中
    @Override
    public Object call() throws Exception {
        int sum = 0;
        for (int i = 0; i <= 100; i++) {
            if (i % 2 == 0) {
                System.out.println(i);
                sum += i;
            }
        }
        return sum;//相当于自动转型成Integer 返回给Object
    }
}

public class ThreadTest3 {
    public static void main(String[] args) {
        //3.创建Callable接口实现类的对象
        NumThread numThread = new NumThread();
        //4.将此Callable接口实现类的对象作为传递到FutureTask构造器中，创建FutureTask的对象
      //  FutureTask futureTask = new FutureTask(numThread);
        FutureTask<Integer> futureTask = new FutureTask<Integer>(numThread);//可使用泛型
        //5.将FutureTask的对象作为参数传递到Thread类的构造器中，创建Thread对象，并调用start()
        new Thread(futureTask).start();
        try {
            //6.获取Callable中call方法的返回值
            //get(）的反回值即为FutureTask构造器参数Callable实现类重写call()的返回值。get需要处理异常
           // Object sum = futureTask.get();
            Integer sum = futureTask.get();//Integer还是Object也可以，向上转型
            System.out.println("sum=" + sum);
        } catch (InterruptedException e) {
            e.printStackTrace();
        } catch (ExecutionException e) {
            e.printStackTrace();
        }
    }
}
```

如何理解实现Callable接口的方式创建多线程比实现Runnable接口创建多线程方式强大？
* 1. call()可以返回值的。
* 2. call()可以抛出异常，被外面的操作捕获，获取异常的信息
* 3. Callable是支持泛型的

### 新增方式二：使用线程池

背景：经常创建和销毁、使用量特别大的资源，比如并发情况下的线程，对性能影响很大。
思路：**提前创建好多个线程，放入线程池中**，使用时直接获取，使用完放回池中。可以避免频繁创建销毁、实现**重复利用**。类似生活中的公共交通工具。
好处：

* **提高响应速度**（减少了创建新线程的时间）

* **降低资源消耗**（重复利用线程池中线程，不需要每次都创建）

* **便于线程管理**
	corePoolSize：核心线程数 核心池的大小
	maximumPoolSize：最大线程数
	keepAliveTime：线程没有任务时最多保持多长时间后会终止
	…

线程池相关API
JDK 5.0起提供了线程池相关API：ExecutorService 和 Executors	
(1)ExecutorService：真正的线程池接口。常见子类ThreadPoolExecutor	
* void execute(Runnable command) ：执行任务/命令，没有返回值，一般用来执行Runnable
* `<T> Future<T> submit(Callable<T> task)`：执行任务，有返回值，一般用来执行Callable
* void shutdown() ：关闭连接池
> API中的内容 java.util.concurrent.ThreadPoolExecutor
> 一个 ExecutorService，它使用可能的几个池线程之一执行每个提交的任务，通常使用 Executors 工厂方法配置。 
>
> 线程池可以解决两个不同问题：由于减少了每个任务调用的开销，它们通常可以在执行大量异步任务时提供增强的性能，并且还可以提供绑定和管理资源（包括执行任务集时使用的线程）的方法。每个 ThreadPoolExecutor 还维护着一些基本的统计数据，如完成的任务数。 
>
> 为了便于跨大量上下文使用，此类提供了很多可调整的参数和扩展钩子 (hook)。但是，强烈建议程序员使用较为方便的 Executors 工厂方法 Executors.newCachedThreadPool()（无界线程池，可以进行自动线程回收）、Executors.newFixedThreadPool(int)（固定大小线程池）和 Executors.newSingleThreadExecutor()（单个后台线程），它们均为大多数使用场景预定义了设置。

(2)Executors：工具类、线程池的工厂类，用于创建并返回不同类型的线程池
* Executors.newCachedThreadPool()：创建一个可根据需要创建新线程的线程池
* Executors.newFixedThreadPool(n); 创建一个可重用固定线程数的线程池
* Executors.newSingleThreadExecutor() ：创建一个只有一个线程的线程池
* Executors.newScheduledThreadPool(n)：创建一个线程池，它可安排在给定延迟后运行命令或者定期地执行。

四种创建线程的方式开发中**最常用的是线程池**

步骤：

1.创建指定线程数量的线程池
2.执行指定的线程的操作。需要提供事项Runnable接口或Callable接口实现类的对象
3.关闭连接池


代码示例：

```java
package com.loong.thread4;

import java.util.concurrent.*;

class NumThread1 implements Runnable{
    @Override
    public void run() {
        System.out.println(Thread.currentThread().getName());
    }
}
class NumThread implements Callable<Integer> {
    @Override
    public Integer call() throws Exception {
        System.out.println(Thread.currentThread().getName());
        return 123;
    }
}
public class ThreadPool {
    public static void main(String[] args) {
        //1.提供指定线程数量的线程池
        ExecutorService pool = Executors.newFixedThreadPool(10);//pool是ExecutorService接口的实现类的的对象

        //System.out.println(pool.getClass());//java.util.concurrent.ThreadPoolExecutor。
        // 类ThreadPoolExecutor继承了抽象类AbstractExecutorService，而AbstractExecutorService实现ExecutorService
        // 那么如何设置线程池？先向下转型成为ThreadPoolExecutor
        ThreadPoolExecutor pool1 =(ThreadPoolExecutor)pool;
        pool1.setCorePoolSize(15);

        //2.执行指定的线程的操作。需要提供事项Runnable接口或Callable接口实现类的对象
        pool.execute(new NumThread1());//execute适合用于Runnable
        Future<Integer> result=pool.submit(new NumThread());//submit一般用于Callable  可用Future<T>获取返回结果对象
        //此 Future 的 get 方法所返回的结果类型
        Integer num = null;
        try {
            num = result.get();
            System.out.println("num=" + num);
        } catch (InterruptedException e) {
            e.printStackTrace();
        } catch (ExecutionException e) {
            e.printStackTrace();
        }

        //3.关闭连接池
        pool.shutdown();
    }
}

```

## 面试题

线程创建的四种方式

解决线程安全问题的方式 3种 并比较不同



面试题：synchronized 与 Lock的异同？（synchronized和Lock方式解决线程安全问题的对比）
*   相同：二者都可以解决线程安全问题
* 不同：synchronized机制在执行完相应的同步代码以后，自动的释放同步监视器

  Lock需要手动的启动同步（lock()，同时结束同步也需要手动的实现（unlock()）

面试题：sleep() 和 wait()的异同？

* 1.相同点：一旦执行方法，都可以使得当前的线程进入阻塞状态。
* 2.不同点
  1）两个方法声明的位置不同：Thread类中声明sleep() , Object类中声明wait()
  2）调用的要求不同：sleep()可以在任何需要的场景下调用。 wait()必须使用在同步代码块或同步方法中
  3）关于是否释放同步监视器：如果两个方法都使用在同步代码块或同步方法中，sleep()不会释放锁，wait()会释放锁。

# 第9章 Java常用类
## ==1.字符串相关的类==

### String类

#### String的特性

String:字符串，使用一对""引起来表示,Java 程序中的所有字符串字面值（如 `"abc"` ）都作为此类的实例实现。 。

字符串的字符使用Unicode字符编码，一个字符(不区分字母还是汉字)占两个字节

1.String声明为final类，**不可被继承**，代表**不可变**的字符序列(不可变性)
2.String实现了Serializable接口：表示字符串是**支持序列化**的。（可以串行化:可以在网络传输）
        实现了Comparable接口：表示String可**以比较大小**
3.String内部定义了final char[] value用于存储字符串数据(final的value 不能指向新的地址，但是单个字符内容是可以变化)
	注：JDK9之后是byte[] value字节数组，主要是为了节省空间。还增加了一个coder字节，表示是否包含utf-16编码
4.通过**字面量**的方式（区别于new)给一个字符串赋值，此时的字符串值声明在**字符串常量池**中)。
5.字符串常量池中是**不会存储相同内容**(使用String类的equals()比较，返回true)的字符串的。

![字符串存储在字符串常量池](http://101.34.218.64/JavaSE.assets/%E5%AD%97%E7%AC%A6%E4%B8%B2%E5%AD%98%E5%82%A8%E5%9C%A8%E5%AD%97%E7%AC%A6%E4%B8%B2%E5%B8%B8%E9%87%8F%E6%B1%A0.png)

#### **String的不可变性：**

1.当对字符串重新赋值时，需要重写指定内存区域赋值，不能使用原有的value进行赋值。
2.当对现的字符串进行连接操作时，也需要重新指定内存区域赋值，不能使用原有的value进行赋值。
3.当调用String的replace()方法修改指定字符或字符串时，也需要重新指定内存区域赋值，不能使用原有的value进行赋值。

```java
代码举例
String s1 = "abc";//字面量的定义方式
String s2 = "abc";
s1 = "hello";

System.out.println(s1 == s2);//比较s1和s2的地址值 false

System.out.println(s1);//hello
System.out.println(s2);//abc

System.out.println("*****************");

String s3 = "abc";
s3 += "def";
System.out.println(s3);//abcdef
System.out.println(s2);

System.out.println("*****************");

String s4 = "abc";
String s5 = s4.replace('a', 'm');
System.out.println(s4);//abc
System.out.println(s5);//mbc
```

#### String创建对象(实例化)的不同方式

方式一：通过字面量定义的方式  String s="Hello";

> 先从常量池查看是否有"Hello"数据空间，如果有，直接指向;如果没有则重新创建，然后指向。s最终指向的是常量池的空间地址

方式二：通过new + 构造器的方式 

> String s=new String("Hello");
>
> 先在堆中创建空间，里面维护了value属性指向常量池的"Hello"空间。
>
> 如果常量池没有"Hello",重新创建；如果有，直接通过value指向。 
>
> 最终s指向的是堆中的空间地址。

//本质上this.value = new char[0];
String s1 = new String();
//this.value = original.value;
String s2 = new String(String original);
//this.value = Arrays.copyOf(value, value.length);
String s3 = new String(char[] a);
String s4 = new String(char[] a,int startIndex,int count);

```java
代码举例
//通过字面量定义的方式：此时的s1和s2的数据javaEE声明在方法区中的字符串常量池中。
String s1 = "javaEE";//s1指向常量池中的 "javaEE"
String s2 = "javaEE";
//通过new + 构造器的方式:此时的s3和s4保存的地址值，是数据在堆空间中开辟空间以后对应的地址值。
String s3 = new String("javaEE");//s3指向堆中的对象 对象的value指向"javaEE"
String s4 = new String("javaEE");

System.out.println(s1 == s2);//true
System.out.println(s1 == s3);//false
System.out.println(s1 == s4);//false
System.out.println(s3 == s4);//false
```

![String两种方式内存分析](http://101.34.218.64/JavaSE.assets/String%E4%B8%A4%E7%A7%8D%E6%96%B9%E5%BC%8F%E5%86%85%E5%AD%98%E5%88%86%E6%9E%90.png)

![String创建对象方式示意1](http://101.34.218.64/JavaSE.assets/String%E5%88%9B%E5%BB%BA%E5%AF%B9%E8%B1%A1%E6%96%B9%E5%BC%8F%E7%A4%BA%E6%84%8F1.png)

![String创建对象方式示意2](http://101.34.218.64/JavaSE.assets/String%E5%88%9B%E5%BB%BA%E5%AF%B9%E8%B1%A1%E6%96%B9%E5%BC%8F%E7%A4%BA%E6%84%8F2.png)

面试题

String s = new String("abc");方式创建对象，在内存中创建了几个对象？
两个:一个是堆空间中new结构，另一个是char[]对应的常量池中的数据："abc"

String str1 = “abc”;与String str2 = new String(“abc”);的区别？
字符串常量存储在字符串常量池，目的是共享
字符串非常量对象存储在堆中

<img src="http://101.34.218.64/JavaSE.assets/str1%E5%92%8Cstr2%E7%9A%84%E5%8C%BA%E5%88%AB.png" alt="str1和str2的区别" style="zoom: 67%;" />

字符串的对象是如何存储的？

```java
Person p1 = new Person("Tom",12);
Person p2 = new Person("Tom",12);
System.out.println(p1.name.equals(p2.name));//true  String重写的equals 比较的是内容
System.out.println(p1.name == p2.name);//true 比较的是地址 
```

![字符串的对象是如何存储的](http://101.34.218.64/JavaSE.assets/%E5%AD%97%E7%AC%A6%E4%B8%B2%E7%9A%84%E5%AF%B9%E8%B1%A1%E6%98%AF%E5%A6%82%E4%BD%95%E5%AD%98%E5%82%A8%E7%9A%84.png)

#### 字符串拼接方式赋值的对比

* 常量与常量的拼接结果在常量池。且常量池中不会存在相同内容的常量。

* 只要其中有一个是变量，结果就在堆中。（相当于new）指向堆中new的对象，对象的value指向字符串常量池中的字符串。

  注意：当变量有final修饰时，是一个常量，按常量处理

* 如果拼接的结果调用intern()方法，返回值就在常量池中。

  > API中内容：当调用 intern 方法时，如果池已经包含一个等于此 String 对象的字符串（用 equals(Object) 方法确定），则返回池中的字符串。否则，将此 String 对象添加到池中，并返回此 String 对象的引用。 
  >
  > 它遵循以下规则：对于任意两个字符串 s 和 t，当且仅当 s.equals(t) 为 true 时，s.intern() == t.intern() 才为 true。 
  >
  > 所有字面值字符串和字符串赋值常量表达式都使用 intern 方法进行操作。字符串字面值在 Java Language Specification 的 §3.10.5 定义。 
  >
  > 返回：一个字符串，内容与此字符串相同，但一定取自具有唯一字符串的池。

```java
    @Test
    public void test3(){
        String s1="javaEE";
        String s2="hadoop";

        String s3="javaEEhadoop";
        String s4="javaEE"+"hadoop";
        String s5=s1+"hadoop";//老韩小结:底层是StringBuilder sb = new StringBuilder(; sb.append(s1);sb.append("hadoop"); sb是在堆中，并且append是在原来字符串的基础上追加的.
        String s6="javaEE"+s2;
        String s7=s1+s2;
        String s8=(s1+s2).intern();
		final String s9="javaEE";
        String s10=s9+"hadoop"
            
        System.out.println(s3 == s4);//true
        System.out.println(s3 == s5);//false
        System.out.println(s3 == s6);//false
        System.out.println(s3 == s7);//false
        System.out.println(s5 == s6);//false
        System.out.println(s5 == s7);//false
        System.out.println(s6 == s7);//false
        System.out.println(s3 == s8);//true
        System.out.println(s3 == s10);//true
        //① 字面量1连接字面量2 会被优化为 字面量1字面量2  例：String s4="javaEE"+"hadoop";被编译器优化为String s4="javaEEhadoop"
        // ②有变量参与，都相当于new  例如这里的s5，s6，s7  都是指向堆中各自new的对象 这些对象指向字符串常量池中的同一个"javaEEhadoop"   特殊情况：final  、intern()
    }
```

#### 面试题;

```java
public class StringTest1 {
    String str = new String("hsp");
    char[] ch = {'j', 'a', 'v', 'a'};
    public void change(String str, char ch[]) {
        str = "java";
        ch[0] = 'h';
    }

    public static void main(String[] args) {
        StringTest1 ex = new StringTest1();
        ex.change(ex.str, ex.ch);
        System.out.println(ex.str);
        System.out.println(ex.ch);
    }
}
//hsp
//java
```

![String面试题内存分析](http://101.34.218.64/JavaSE.assets/String%E9%9D%A2%E8%AF%95%E9%A2%98%E5%86%85%E5%AD%98%E5%88%86%E6%9E%90.png)



#### JVM中涉及字符串的内存结构

常见三种JVM:

sun公司的HotSpot——默认的

BEA公司的JRockit

IBM公司的J9 VM

常量池的位置：

jdk 1.6:字符串常量池存储在**方法区（永久代）**
jdk 1.7:字符串常量池存储在**堆**
jdk 1.8:字符串常量池存储在**堆** (这里宋红康说在元空间 讲错了)

>
>JDK1.6及之前，运行时常量池（字符串常量池也在里边）是存放在方法区，此时方法区的实现是永久带。(很多开发者习惯将方法区叫做永久代，实际上永久代只是方法区的一种实现方式。)
>JDK1.7字符串常量池被单独从方法区移到堆中，运行时常量池剩下的还在永久带（方法区）
>JDK1.8，永久带移除后，方法区的新的实现为元空间，但字符串常量池还在堆中，运行时常量池在元空间（方法区）
>
>参考https://blog.csdn.net/qq_30999361/article/details/124727031

### String常用方法

* int length()：返回字符串的长度： return value.length
* char charAt(int index)： 返回某索引处的字符return value[index]
* boolean isEmpty()：判断是否是空字符串：return value.length == 0
* String toLowerCase()：使用默认语言环境，将 String 中的所有字符转换为小写
* String toUpperCase()：使用默认语言环境，将 String 中的所有字符转换为大写
* String trim()：返回字符串的副本，忽略前导空白和尾部空白
* boolean equals(Object obj)：比较字符串的内容是否相同
* boolean equalsIgnoreCase(String anotherString)：与equals方法类似，忽略大小写
* String concat(String str)：将指定字符串连接到此字符串的结尾。 等价于用“+”
* int compareTo(String anotherString)：比较两个字符串的大小
* String substring(int beginIndex)：返回一个新的字符串，它是此字符串的从beginIndex开始截取到最后的一个子字符串。
* String substring(int beginIndex, int endIndex) ：返回一个新字符串，它是此字符串从beginIndex开始截取到endIndex(不包含)的一个子字符串。[beginIndex,endIndex)
---
* boolean endsWith(String suffix)：测试此字符串是否以指定的后缀结束
* boolean startsWith(String prefix)：测试此字符串是否以指定的前缀开始
* boolean startsWith(String prefix, int toffset)：测试此字符串从指定索引开始的子字符串是否以指定前缀开始
---
* boolean contains(CharSequence s)：当且仅当此字符串包含指定的 char 值序列时，返回 true

* int indexOf(String str)：返回指定子字符串在此字符串中第一次出现处的索引

* int indexOf(String str, int fromIndex)：返回指定子字符串在此字符串中第一次出现处的索引，从指定的索引开始

* int lastIndexOf(String str)：返回指定子字符串在此字符串中最右边出现处的索引

* int lastIndexOf(String str, int fromIndex)：返回指定子字符串在此字符串中最后一次出现处的索引，从指定的索引开始反向搜索。注：indexOf和lastIndexOf方法如果未找到都是返回-1

  什么情况下，indexOf(str)和lastIndexOf(str)返回值相等？情况一：存在唯一的str子串。情况二不存在str(返回-1)
---
替换
* String replace(char oldChar, char newChar)：返回一个新的字符串，它是通过用 newChar 替换此字符串中出现的所有 oldChar 得到的。
* String replace(CharSequence target, CharSequence replacement)：使用指定的字面值替换序列替换此字符串所有匹配字面值目标序列的子字符串。
* String replaceAll(String regex,String replacement) ： 使用给定的replacement 替换此字符串所有匹配给定的正则表达式的子字符串。
* String replaceFirst(String regex, String replacement) ： 使用给定的replacement 替换此字符串匹配给定的正则表达式的第一个子字符串。
---
匹配
* boolean matches(String regex)：告知此字符串是否匹配给定的正则表达式。
---
切片
* String[] split(String regex)：根据给定正则表达式的匹配拆分此字符串。
* String[] split(String regex, int limit)：根据匹配给定的正则表达式来拆分此字符串，最多不超过limit个，如果超过了，剩下的全部都放到最后一个元素中。

![String常用方法1.png](http://101.34.218.64/JavaSE.assets/String%E5%B8%B8%E7%94%A8%E6%96%B9%E6%B3%951.png)

![String常用方法2.png](http://101.34.218.64/JavaSE.assets/String%E5%B8%B8%E7%94%A8%E6%96%B9%E6%B3%952.png)

代码示例：

```java
package com.loong.string;

import org.junit.Test;

import java.util.Queue;

/**
 * @author LoongKK
 * @create 2022/7/20-10:27
 */
public class StringMethodTest {
    @Test
    public void test1() {
        //1. equals 前面已经讲过了. 比较内容是否相同，区分大小写
        String str1 = "hello";
        String str2 = "Hello";
        System.out.println(str1.equals(str2));//false
        // 2.equalsIgnoreCase 忽略大小写的判断内容是否相等
        System.out.println("john".equalsIgnoreCase("johN"));//true
        // 3.length 获取字符的个数，字符串的长度
        System.out.println("韩顺平".length());//3
        // 4.indexOf 获取字符在字符串对象中第一次出现的索引，索引从 0 开始，如果找不到，返回-1
        String s1 = "wer@terwe@g";
        int index = s1.indexOf('@');
        System.out.println(index);// 3
        System.out.println("weIndex=" + s1.indexOf("we"));//0
        // 5.lastIndexOf 获取字符在字符串中最后一次出现的索引，索引从 0 开始，如果找不到，返回-1
        s1 = "wer@terwe@g@";
        index = s1.lastIndexOf('@');
        System.out.println(index);//11
        System.out.println("ter 的位置=" + s1.lastIndexOf("ter"));//4
        // 6.substring 截取指定范围的子串
        String name = "hello,张三";
        //下面 name.substring(6) 从索引 6 开始截取后面所有的内容
        System.out.println(name.substring(6));//截取后面的字符
        //name.substring(0,5)表示从索引 0 开始截取，截取到索引 5-1=4 位置
        System.out.println(name.substring(0, 5));//hello
        System.out.println(name.substring(2, 5));//llo
    }
    @Test
    public void test2() {
        // 1.toUpperCase 转换成大写
        String s = "heLLo";
        System.out.println(s.toUpperCase());//HELLO
        // 2.toLowerCase
        System.out.println(s.toLowerCase());//hello
        // 3.concat 拼接字符串
        String s1 = "宝玉";
        s1 = s1.concat("林黛玉").concat("薛宝钗").concat("together");
        System.out.println(s1);//宝玉林黛玉薛宝钗together
        // 4.replace 替换字符串中的字符
        s1 = "宝玉 and 林黛玉 林黛玉 林黛玉";
        //在 s1 中，将 所有的 林黛玉 替换成薛宝钗
        //  s1.replace() 方法执行后，返回的结果才是替换过的.
        // 注意对 s1 没有任何影响
        String s11 = s1.replace("宝玉", "jack");
        System.out.println(s1);//宝玉 and 林黛玉 林黛玉 林黛玉
        System.out.println(s11);//jack and 林黛玉 林黛玉 林黛玉
        // 5.split 分割字符串, 对于某些分割字符，我们需要 转义比如 | \\等
        String poem = "锄禾日当午,汗滴禾下土,谁知盘中餐,粒粒皆辛苦";
        // 以 , 为标准对 poem 进行分割 , 返回一个数组
        String[] split = poem.split(",");
        System.out.println("==分割后内容===");
        for (int i = 0; i < split.length; i++) {
            System.out.println(split[i]);
        }
        // 在对字符串进行分割时，如果有特殊字符，需要加入 转义符 \
        poem = "E:\\aaa\\bbb";
        split = poem.split("\\\\");
        System.out.println("==分割后内容===");
        for (int i = 0; i < split.length; i++) {
            System.out.println(split[i]);
        }
        // 6.toCharArray 转换成字符数组
        s = "happy";
        char[] chs = s.toCharArray();
        for (int i = 0; i < chs.length; i++) {
            System.out.println(chs[i]);
        }
        // 7.compareTo 比较两个字符串的大小，如果前者大，
        // 则返回正数，后者大，则返回负数，如果相等，返回 0
        // 老韩解读
        // (1) 如果长度相同，并且每个字符也相同，就返回 0
        // (2) 如果长度相同或者不相同，但是在进行比较时，可以区分大小
        //就返回 if (c1 != c2) {
        //return c1 - c2;
        //}
        // (3) 如果前面的部分都相同，就返回 str1.len - str2.len
        String a = "jcck";// len = 3
        String b = "jack";// len = 4
        System.out.println(a.compareTo(b)); // 返回值是 'c' - 'a' = 2 的值
        // 8.format 格式字符串
        /* 占位符有:
         * %s 字符串 %c 字符 %d 整型 %.2f 浮点型
         *
         */
        String name = "john";
        int age = 10;
        double score = 56.857;
        char gender = '男';
        //将所有的信息都拼接在一个字符串.
        String info =
                "我的姓名是" + name + "年龄是" + age + ",成绩是" + score + "性别是" + gender + "。希望大家喜欢我！ ";
        System.out.println(info);
        //老韩解读
        //1. %s , %d , %.2f %c 称为占位符
        //2. 这些占位符由后面变量来替换
        //3. %s 表示后面由 字符串来替换
        //4. %d 是整数来替换
        //5. %.2f 表示使用小数来替换，替换后，只会保留小数点两位, 并且进行四舍五入的处理
        //6. %c 使用 char 类型来替换
        String formatStr = "我的姓名是%s 年龄是%d，成绩是%.2f 性别是%c.希望大家喜欢我！";
        String info2 = String.format(formatStr, name, age, score, gender);
        System.out.println("info2=" + info2);
    }
}

```

#### 开发中常用技巧：

```java
String str = "12hello34world5java7891mysql456";
//把字符串中的数字替换成,，如果结果中开头和结尾有，的话去掉
String string = str.replaceAll("\\d+", ",").replaceAll("^,|,$", "");
System.out.println(string);

String str = "12345";
//判断str字符串中是否全部有数字组成，即有1-n个数字组成
boolean matches = str.matches("\\d+");
System.out.println(matches);
String tel = "0571-4534289";
//判断这是否是一个杭州的固定电话
boolean result = tel.matches("0571-\\d{7,8}");
System.out.println(result);

String str = "hello|world|java";
String[] strs = str.split("\\|");
for (int i = 0; i < strs.length; i++) {
System.out.println(strs[i]);
}
System.out.println();
String str2 = "hello.world.java";
String[] strs2 = str2.split("\\.");
for (int i = 0; i < strs2.length; i++) {
System.out.println(strs2[i]);
}
```

#### 复习：String和基本数据类型或包装类之间的转换

([点这里去复习](#String和基本数据类型或包装类之间的转换))

#### Sting与字符数组char[]之间的转换

String --> char[]:调用String的toCharArray()：

> public char[] toCharArray()：将字符串中的全部字符存放在一个字符数组中的方法
> public void getChars(int srcBegin, int srcEnd, char[] dst,int dstBegin)：提供了将指定索引范围内的字符串存放到数组中的方法

char[] --> String:调用String的构造器：

> String(char[]) 和 String(char[]，int offset，intlength) 分别用字符数组中的全部字符和部分字符创建字符串对象。

```java
     String str1 = "abc123";  
    char[] charArray = str1.toCharArray();
    for (int i = 0; i < charArray.length; i++) {
        System.out.println(charArray[i]);
    }

    char[] arr = new char[]{'h','e','l','l','o'};
    String str2 = new String(arr);
    System.out.println(str2);
```



#### String与字节数组 byte[]转换

编码：String --> byte[]:调用String的getBytes()
> public byte[] getBytes() ：使用平台的默认字符集将此 String 编码为byte 序列，并将结果存储到一个新的 byte 数组中。
> public byte[] getBytes(String **charsetName**) ：使用**指定的字符集**将此 String 编码到 byte 序列，并将结果存储到新的 byte 数组。

解码：byte[] --> String:调用String的构造器
> String(byte[])：通过使用平台的默认字符集解码指定的 byte 数组，构造一个新的 String。
> String(byte[]，int offset，int length) ：用指定的字节数组的一部分，即从数组起始位置offset开始取length个字节构造一个字符串对象。
>
> String(byte[],String **charsetName**)

编码：字符串 -->字节  (看得懂 --->看不懂的二进制数据)
解码：编码的逆过程，字节 --> 字符串 （看不懂的二进制数据 ---> 看得懂

说明：解码时，要求解码使用的字符集必须与编码时使用的字符集一致，否则会出现乱码。

GBK中，中文字符占两个字节；UTF-8，中文字符占三个字节

```java
@Test
public void test3() throws UnsupportedEncodingException {
    String str1 = "abc123中国";
    byte[] bytes = str1.getBytes();//使用默认的字符集，进行编码。
    System.out.println(Arrays.toString(bytes));

    byte[] gbks = str1.getBytes("gbk");//使用gbk字符集进行编码。
    System.out.println(Arrays.toString(gbks));

    System.out.println("******************");

    String str2 = new String(bytes);//使用默认的字符集，进行解码。
    System.out.println(str2);

    String str3 = new String(gbks);
    System.out.println(str3);//出现乱码。原因：编码集和解码集不一致！


    String str4 = new String(gbks, "gbk");
    System.out.println(str4);//没出现乱码。原因：编码集和解码集一致！


}
```

```java
String str = "中";
System.out.println(str.getBytes("ISO8859-1").length);// -128~127
System.out.println(str.getBytes("GBK").length);//中文字符占两个字节
System.out.println(str.getBytes("UTF-8").length);//中午字符占三个字节
System.out.println(new String(str.getBytes("ISO8859-1"),"ISO8859-1"));// 乱码，表示不了中文
System.out.println(new String(str.getBytes("GBK"), "GBK"));
System.out.println(new String(str.getBytes("UTF-8"), "UTF-8"));
```

#### 常见算法题目

```java
package com.loong.string;
import java.util.Arrays;
public class StringQuestion {
    public static void main(String[] args) {
        System.out.println(solution1(" 1243dsh dh3 "));
        System.out.println(solution2("abcdefg",2,6));
        System.out.println(solution3("abkkcadkabkebfkabkskab", "ab"));

    }
//1.模拟一个trim方法，去除字符串两端的空格。
    public static String solution1(String str){
        return str.replaceAll("^ | $","");
    }
//2.将一个字符串进行反转。将字符串中指定部分进行反转。比如“abcdefg”反转为”abfedcg”
    public static String solution2(String str,int begin,int end){//[begin,end)
        char[] charArray=str.toCharArray();
        for (int i = begin; i < (begin+end)/2; i++) {
            char temp=charArray[i];
            charArray[i]=charArray[end-begin+1];
            charArray[end-begin+1]=temp;
        }
        return new String(charArray);
    }
    //老师的
    //方式一：
    public String reverse(String str,int startIndex,int endIndex){
        if(str==null)return null;
        char[] arr=str.toCharArray();
        for (int x = startIndex,y=endIndex; x < y; x++,y--) {
            char temp=arr[x];
            arr[x]=arr[y];
            arr[y]=temp;
        }
        return new String(arr);
    }
    //方式二：拼接
    public String reverse1(String str,int startIndex,int endIndex){
        if(str==null)return null;
        String reverseStr=str.substring(0,startIndex);//第一部分
        for (int i = endIndex; i >= startIndex ; i--) {//倒着把想要反转的子串每个字符拼接到前面
            reverseStr+=str.charAt(i);
        }
        reverseStr+=str.substring(endIndex+1);//第三部分
        return reverseStr;
    }
    //方式三 使用StringBuffer/StringBuilder 不用new很多对象 效率高
    public String reverse2(String str,int startIndex,int endIndex) {
        if (str == null) return null;
        StringBuilder builder = new StringBuilder(str.length());
        builder.append(str.substring(0, startIndex));//第一部分

        for (int i = endIndex; i >= startIndex; i--) {//倒着把想要反转的子串每个字符拼接到前面
            builder.append(str.charAt(i));
        }
        builder.append(str.substring(endIndex + 1));

        return builder.toString();
    }
//3.获取一个字符串在另一个字符串中出现的次数 比如：获取“ab”在 “abkkcadkabkebfkabkskab” 中出现的次数
    public static int solution3(String str1,String str2){
        //我的思路：用indexOf 找到 记一次  从返回的索引处开始的子串中再找
        int count=0,index = 0;
        while(index<str1.length()){
            index=str1.indexOf(str2,index);
            if(index==-1)break;
            else{
                count++;
                index+=str2.length();
            }
        }
        return count;
    }
//老师的
    public int getCount(String mainStr,String subStr){
        int mainLength=mainStr.length();
        int subLength=subStr.length();
        int count=0;
        int index= 0;
        if (mainLength<subLength){return 0;}
        else{
            while((index=mainStr.indexOf(subStr,index))!=-1){
                count++;
                index+=subLength;
            }
            return count;
        }
    }
//
//4.获取两个字符串中最大相同子串（最大公共子串）。
// 比如：str1 = "abcwerthelloyuiodef“;str2 = "cvhellobnm"
// 提示：将短的那个串进行长度依次递减的子串与较长的串比较。——滑动窗口  还有其它方法：KMP
    //老师的 只适用于只有一个最大公共子串的情况
    public String getMaxSameString(String str1,String str2){
        String maxStr=(str1.length()>=str2.length())?str1:str2;
        String minStr=(str1.length()<str2.length())?str1:str2;
        int length = minStr.length();
        if(str1==null||str2==null)return null;
        for (int i = 0; i < length; i++) {//i++控制窗口长度
            for (int x = 0,y=length-i;y<=length;x++,y++) {//x++,y++ 窗口向后滑
                String subStr = minStr.substring(x,y);
                if (maxStr.contains(minStr)){//boolean contains(CharSequence s)：当且仅当此字符串包含指定的 char 值序列时，返回 true
                    return minStr;
                }
            }
        }
        return null ;
    }
//5.对字符串中字符进行自然顺序排序。
// 提示：
// 1）字符串变成字符数组。
// 2）对数组排序，选择，冒泡，Arrays.sort();
// 3）将排序后的数组变成字符串。
    public String sortTest(String str){
        char[] arr = str.toCharArray();
        Arrays.sort(arr);
        return new String(arr);
    }
}
```



老师给的示例代码
```java
package com.atguigu.java;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
import org.junit.Test;
/*
 * 1.模拟一个trim方法，去除字符串两端的空格。
 * 
 * 2.将一个字符串进行反转。将字符串中指定部分进行反转。比如将“abcdefg”反转为”abfedcg”
 * 
 * 3.获取一个字符串在另一个字符串中出现的次数。
      比如：获取“ab”在 “cdabkkcadkabkebfkabkskab”    
      中出现的次数
4.获取两个字符串中最大相同子串。比如：
   str1 = "abcwerthelloyuiodef“;str2 = "cvhellobnm"//10
   提示：将短的那个串进行长度依次递减的子串与较长  
   的串比较。
5.对字符串中字符进行自然顺序排序。"abcwerthelloyuiodef"
提示：
1）字符串变成字符数组。
2）对数组排序，选择，冒泡，Arrays.sort(str.toCharArray());
3）将排序后的数组变成字符串。
 */
public class StringExer {
	// 第1题
	public String myTrim(String str) {
		if (str != null) {
			int start = 0;// 用于记录从前往后首次索引位置不是空格的位置的索引
			int end = str.length() - 1;// 用于记录从后往前首次索引位置不是空格的位置的索引
			while (start < end && str.charAt(start) == ' ') {
				start++;
			}
			while (start < end && str.charAt(end) == ' ') {
				end--;
			}
			if (str.charAt(start) == ' ') {
				return "";
			}
			return str.substring(start, end + 1);
		}
		return null;
	}
	// 第2题
	// 方式一：
	public String reverse1(String str, int start, int end) {// start:2,end:5
		if (str != null) {
			// 1.
			char[] charArray = str.toCharArray();
			// 2.
			for (int i = start, j = end; i < j; i++, j--) {
				char temp = charArray[i];
				charArray[i] = charArray[j];
				charArray[j] = temp;
			}
			// 3.
			return new String(charArray);
		}
		return null;
	}
	// 方式二：
	public String reverse2(String str, int start, int end) {
		// 1.
		String newStr = str.substring(0, start);// ab
		// 2.
		for (int i = end; i >= start; i--) {
			newStr += str.charAt(i);
		} // abfedc
			// 3.
		newStr += str.substring(end + 1);
		return newStr;
	}
	// 方式三：推荐 （相较于方式二做的改进）
	public String reverse3(String str, int start, int end) {// ArrayList list = new ArrayList(80);
		// 1.
		StringBuffer s = new StringBuffer(str.length());
		// 2.
		s.append(str.substring(0, start));// ab
		// 3.
		for (int i = end; i >= start; i--) {
			s.append(str.charAt(i));
		}
		// 4.
		s.append(str.substring(end + 1));
		// 5.
		return s.toString();
	}
	@Test
	public void testReverse() {
		String str = "abcdefg";
		String str1 = reverse3(str, 2, 5);
		System.out.println(str1);// abfedcg
	}
	// 第3题
	// 判断str2在str1中出现的次数
	public int getCount(String mainStr, String subStr) {
		if (mainStr.length() >= subStr.length()) {
			int count = 0;
			int index = 0;
			// while((index = mainStr.indexOf(subStr)) != -1){
			// count++;
			// mainStr = mainStr.substring(index + subStr.length());
			// }
			// 改进：
			while ((index = mainStr.indexOf(subStr, index)) != -1) {
				index += subStr.length();
				count++;
			}
			return count;
		} else {
			return 0;
		}
	}
	@Test
	public void testGetCount() {
		String str1 = "cdabkkcadkabkebfkabkskab";
		String str2 = "ab";
		int count = getCount(str1, str2);
		System.out.println(count);
	}
	@Test
	public void testMyTrim() {
		String str = "   a   ";
		// str = " ";
		String newStr = myTrim(str);
		System.out.println("---" + newStr + "---");
	}
	// 第4题
	// 如果只存在一个最大长度的相同子串
	public String getMaxSameSubString(String str1, String str2) {
		if (str1 != null && str2 != null) {
			String maxStr = (str1.length() > str2.length()) ? str1 : str2;
			String minStr = (str1.length() > str2.length()) ? str2 : str1;
			int len = minStr.length();
			for (int i = 0; i < len; i++) {// 0 1 2 3 4 此层循环决定要去几个字符
				for (int x = 0, y = len - i; y <= len; x++, y++) {
					if (maxStr.contains(minStr.substring(x, y))) {
						return minStr.substring(x, y);
					}
				}
			}
		}
		return null;
	}
	// 如果存在多个长度相同的最大相同子串
	// 此时先返回String[]，后面可以用集合中的ArrayList替换，较方便
	public String[] getMaxSameSubString1(String str1, String str2) {
		if (str1 != null && str2 != null) {
			StringBuffer sBuffer = new StringBuffer();
			String maxString = (str1.length() > str2.length()) ? str1 : str2;
			String minString = (str1.length() > str2.length()) ? str2 : str1;
			int len = minString.length();
			for (int i = 0; i < len; i++) {
				for (int x = 0, y = len - i; y <= len; x++, y++) {
					String subString = minString.substring(x, y);
					if (maxString.contains(subString)) {
						sBuffer.append(subString + ",");
					}
				}
				System.out.println(sBuffer);
				if (sBuffer.length() != 0) {
					break;
				}
			}
			String[] split = sBuffer.toString().replaceAll(",$", "").split("\\,");
			return split;
		}
		return null;
	}
	// 如果存在多个长度相同的最大相同子串：使用ArrayList
//	public List<String> getMaxSameSubString1(String str1, String str2) {
//		if (str1 != null && str2 != null) {
//			List<String> list = new ArrayList<String>();
//			String maxString = (str1.length() > str2.length()) ? str1 : str2;
//			String minString = (str1.length() > str2.length()) ? str2 : str1;
//
//			int len = minString.length();
//			for (int i = 0; i < len; i++) {
//				for (int x = 0, y = len - i; y <= len; x++, y++) {
//					String subString = minString.substring(x, y);
//					if (maxString.contains(subString)) {
//						list.add(subString);
//					}
//				}
//				if (list.size() != 0) {
//					break;
//				}
//			}
//			return list;
//		}
//
//		return null;
//	}
	@Test
	public void testGetMaxSameSubString() {
		String str1 = "abcwerthelloyuiodef";
		String str2 = "cvhellobnmiodef";
		String[] strs = getMaxSameSubString1(str1, str2);
		System.out.println(Arrays.toString(strs));
	}
	// 第5题
	@Test
	public void testSort() {
		String str = "abcwerthelloyuiodef";
		char[] arr = str.toCharArray();
		Arrays.sort(arr);
		String newStr = new String(arr);
		System.out.println(newStr);
	}
}
```




### StringBuffer、StringBuilder

String中如果多次执行改变串内容的操作，会导致大量副本字符串对象存留在内存中，降低效率。如果这样的操作放到循环中，会极大影响程序的性能。



#### StringBuffer类

 java.lang.StringBuffer代表可变的字符序列，JDK1.0中声明，可以对字符串内容进行增删，此时不会产生新的对象。

* 直接父类 是 AbstractStringBuilder,父类里面有value

*  StringBuffer 是一个 final 类，不能被继承

* StringBuffer 实现了 Serializable, 即 StringBuffer 的对象可以串行化

* char[] value**没有final声明,value可以不断扩容**。

* StringBuffer是一个容器

* 不用每次都更换地址(即不是每次创建新对象)， 所以效率高于 String

* 很多方法与String相同

* 作为参数传递时，方法内部可以改变值

* 对象必须使用构造器生成
  StringBuffer()：初始容量为16的字符串缓冲区
  StringBuffer(int size)：构造指定容量的字符串缓冲区
  StringBuffer(String str)：将内容初始化为指定字符串内容
  
* String vs StringBuffer

  String保存的是字符串常量，里面的值不能更改(final)，每次String类的更新实际上就是该地址，效率，效率较低。

  StringBuffer保存的是地府从变量，里面的值可以更改，每次StringBuffer的更新实际上可以更新内容，不用每次更新地址，效率较高。char[] value 放在堆

  ```java
  String s = new String("我喜欢学习");
  //System.out.println(s == s.concat("数学"));//false  s.concat("数学")相当于s+"数学"
  s=s+"数学";//s=s.concat("数学");
  StringBuffer buffer = new StringBuffer("我喜欢学习");
  //System.out.println(buffer == buffer.append("数学"));//true
  buffer.append("数学");
  ```

  自己画的 String对象的实体不可变final  buffer对象的实体可变

  ![StringvsStringBuffer](http://101.34.218.64/JavaSE.assets/StringvsStringBuffer.png)

#### StringBuffer类的常用方法

StringBuilder 和 StringBuffer 非常类似，均代表可变的字符序列，而且提供相关功能的方法也一样


StringBuffer append(xxx)：提供了很多的append()方法，用于进行字符串拼接 
  >  注意：根据append源码  **buffer.append(xxx) 如果xxx为null会把字符串"null"加进去**！！
  >
  >  ```java
  >  String str = null;
  >          StringBuffer sb = new StringBuffer();
  >          sb.append(str);//根据append源码  buffer.append(xxx) 如果xxx为null会把字符串"null"加进去！！
  >          System.out.println(sb.length());//4
  >          System.out.println(sb);//"null"
  >          StringBuffer sb1 = new StringBuffer(str);//此构造器源码用到了str.length() + 16，而str为null抛空指针异常
  >          System.out.println(sb1);
  >  ```

StringBuffer delete(int start,int end)：删除指定位置的内容
StringBuffer replace(int start, int end, String str)：把[start,end)位置替换为str
StringBuffer insert(int offset, xxx)：在指定位置插入xxx
StringBuffer reverse() ：把当前字符序列逆转

(当append和insert时，如果原来value数组长度不够，可扩容。)
如上这些方法支持方法链操作。
方法链的原理：
 @Override
    public synchronized StringBuffer append(String str) {
        super.append(str);
        return this;//当方法的返回值是一个对象时，这个对象还可以再调用它的方法。（可以连续的.方法.方法）
    }
 其它方法：

```java
public int indexOf(String str)
public String substring(int start,int end)
public int length()
public char charAt(int n )
public void setCharAt(int n ,char ch)
```

#### 开发中StringBuffer、StringBuilder中的常用方法(重要)

增：append(xxx)
删：delete(int start,int end)
改：setCharAt(int n ,char ch) / replace(int start, int end, String str)
查：charAt(int n )
插：insert(int offset, xxx)
长度：length();
遍历：for() + charAt() / toString()

#### 三者的异同(重要)

String、StringBuffer、StringBuilder三者的对比
String(JDK1.0):不可变的字符序列；底层使用char[]存储
StringBuffer(JDK1.0):可变的字符序列；线程安全的，效率低；底层使用char[]存储
StringBuilder:可变的字符序列；jdk5.0新增的，线程不安全的，效率高；底层使用char[]存储

注意：作为参数传递的话，方法内部String不会改变其值，StringBuffer和StringBuilder会改变其值

效率从高到低排列：StringBuilder > StringBuffer >> String

1.如果字符串存在大量的修改操作，一般使用StringBuffer或StringBuilder
   如果字符串存在大量的修改操作，并在单线程的情况，使用StringBuilder
   如果字符串存在大量的修改操作，并在多线程的情况，使用StringBuffer
2.如果我们字符串很少修改，被多个对象引用，使用String, 比如配置信息等

#### StringBuffer与StringBuilder的内存解析

 以StringBuffer为例：

String str = new String();//char[] value = new char[0];
String str1 = new String("abc");//char[] value = new char[]{'a','b','c'};

StringBuffer sb1 = new StringBuffer();//char[] value = new char[16];//**底层创建了一个长度是16的数组**。
System.out.println(sb1.length());//0  显示的是count 
sb1.append('a');//value[0] = 'a';
sb1.append('b');//value[1] = 'b';

StringBuffer sb2 = new StringBuffer("abc");//char[] value = new char["abc".length() + 16];

//问题1. System.out.println(sb2.length());//3 显示的是count 不是+16后的个数
//问题2. 扩容问题:如果要添加的数据底层数组盛不下了，那就需要扩容底层的数组。
         默认情况下，**扩容为原来容量的2倍 + 2**，同时将原数组中的元素复制到新的数组中。

指导意义：开发中建议大家使用：StringBuffer(int capacity) 或 StringBuilder(int capacity)(避免让它自己扩容，因为扩容要复制。效率低)

#### 三者之间的转换

String -->StringBuffer、StringBuilder:调用StringBuffer、StringBuilder构造器
StringBuffer、StringBuilder -->String:①调用String构造器；②StringBuffer、StringBuilder的toString()

#### 三者的效率测试

从高到低排列：**StringBuilder > StringBuffer >> String**

因为StringBuilder是线程不安全的，故比StringBuffer快一点

```java
 long startTime = 0L;
        long endTime = 0L;
        String text = "";
        StringBuffer buffer = new StringBuffer("");
        StringBuilder builder = new StringBuilder("");
//开始对比
        startTime = System.currentTimeMillis();
        for (int i = 0; i < 20000; i++) {
            buffer.append(String.valueOf(i));
        }
        endTime = System.currentTimeMillis();
        System.out.println("StringBuffer的执行时间：" + (endTime - startTime));
        startTime = System.currentTimeMillis();
        for (int i = 0; i < 20000; i++) {
            builder.append(String.valueOf(i));
        }
        endTime = System.currentTimeMillis();
        System.out.println("StringBuilder的执行时间：" + (endTime - startTime));
        startTime = System.currentTimeMillis();
        for (int i = 0; i < 20000; i++) {
            text = text + i;
        }
        endTime = System.currentTimeMillis();
        System.out.println("String的执行时间：" + (endTime - startTime));
/*某次的输出
StringBuffer的执行时间：5
StringBuilder的执行时间：3
String的执行时间：1443
*/
```



## 2.JDK 8之前的日期时间API

我们将学习：
System类中的currentTimeMillis()
java.util.Date和子类java.sql.Date
SimpleDateFormat
Calendar

![所有的时间相关API](http://101.34.218.64/JavaSE.assets/%E6%89%80%E6%9C%89%E7%9A%84%E6%97%B6%E9%97%B4%E7%9B%B8%E5%85%B3API.png)

计算世界时间的主要标准有：
UTC(Coordinated Universal Time)
GMT(Greenwich Mean Time)
CST(Central Standard Time)



### System静态方法

1.获取系统当前时间：System类中的currentTimeMillis()
long time = **System.currentTimeMillis()**;
//返回当前时间与1970年1月1日0时0分0秒之间以**毫秒**为单位的时间差。
//称为时间戳
System.out.println(time);

此方法适于计算时间差。

### Date类

 java.util.Date类
       |---java.sql.Date类
表示特定的瞬间，精确到毫秒
1.两个构造器的使用
* 构造器一：Date()：创建一个对应本地当前时间的Date对象
* 构造器二：Date(long date) 创建指定毫秒数的Date对象
2.两个方法的使用
* toString():显示当前的年、月、日、时、分、秒 
 > dow mon dd hh:mm:ss zzz yyyy 
 > 其中： dow 是一周中的某一天 (Sun, Mon, Tue,Wed, Thu, Fri, Sat)，zzz是时间标准。
* getTime():获取当前Date对象对应的毫秒数。（时间戳）

3. java.sql.Date对应着数据库中的日期类型的变量
* 如何实例化

* 如何将java.util.Date对象转换为java.sql.Date对象

   把util里带时分秒的Date转化为年月日的sql里的date 借助getTime获得毫秒数 放到sql.Date的构造器中

```java
@Test
    public  void test1(){
        Date date = new Date();
        System.out.println(date);//调用了重写的toString()   Thu Jul 21 00:38:04 CST 2022
     //   System.out.println(System.currentTimeMillis());//1658335084037 当前 调用方法时的时间 可以看出下面getTime比这里时间还早
        System.out.println(date.getTime());//1658335084026 new Date();时的时间

        Date date1 = new Date(date.getTime());//指定毫秒数 这里还是用new Date();时的时间
        System.out.println(date1.getTime());//1658335084026
        System.out.println(date1);//Thu Jul 21 00:38:04 CST 2022

        java.sql.Date date3 = new java.sql.Date(123456789L);
        System.out.println(date3);//yyyy-mm-dd

        //java.util.Date对象转换为java.sql.Date对象
        //情况一：多态的向下转型
//        Date date4 = new java.sql.Date(2343243242323L);
//        java.sql.Date date5 = (java.sql.Date) date4;
        //情况二：时间格式的转换  把util里带时分秒的Date转化为年月日的sql里的date 借助getTime获得毫秒数 放到sql.Date的构造器中
        Date date6 = new Date();
        java.sql.Date date7 = new java.sql.Date(date6.getTime());
    }
```

### SimpleDateFormat类

Date类的API不易于国际化，大部分被废弃了，java.text.SimpleDateFormat类是一个**不与语言环境有关**的方式来格式化和解析日期的具体类。

#### **SimpleDateFormat对日期Date类的格式化和解析**

* 格式化：**日期 --->字符串**
    SimpleDateFormat() ：构造器 默认的模式和语言环境创建对象
    SimpleDateFormat(String pattern)：构造器 可以用参数pattern指定的格式创建一个对象
    
    public **String format(Date date)**：SimpleDateFormat的对象调用该方法格式化时间对象date
    
* 解析：格式化的逆过程，**字符串 ---> 日期**
    public **Date parse(String source)**：从给定字符串的开始解析文本，以生成一个日期。
#### 代码示例

 ```java
 @Test
    public void test2() {
        Date date = new Date();
        SimpleDateFormat sdf = new SimpleDateFormat();
        System.out.println(sdf.format(date));//22-7-21 下午3:47  //默认的模式和语言环境
        try {
            System.out.println(sdf.parse("22-7-21 下午1:23"));//Thu Jul 21 13:23:00 CST 2022
        } catch (ParseException e) {
            e.printStackTrace();
        }
        //*************照指定的方式格式化和解析：调用带参的构造器*****************
        //SimpleDateFormat sdf1 = new SimpleDateFormat("yyyyy.MMMMM.dd GGG hh:mm aaa");//02022.七月.21 公元 03:47 下午
        //SimpleDateFormat sdf1 = new SimpleDateFormat(""yyyy年MM月dd日 EEE HH:mm:ss"");
        // SimpleDateFormat sdf1 = new SimpleDateFormat("yyyy-MM-dd hh:mm:ss aaa");//h是12小时制的时
        SimpleDateFormat sdf1 = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");//H是24小时制的时。 开发中这种格式用的多

        String format1 = sdf1.format(date);//格式化时间对象date
        System.out.println(format1);//2022-07-21 15:48:23

        Date date2 = null;
        try {
            date2 = sdf1.parse("2022-07-21 03:35:33");//解析:要求字符串必须是符合SimpleDateFormat对象sdf1识别的格式(通过构造器参数体现),否则，抛异常
        } catch (ParseException e) {
            e.printStackTrace();
        }
        System.out.println(date2);//Thu Jul 21 03:35:33 CST 2022
    }
 ```

#### 模式字母

> | 字母 | 日期或时间元素           | 表示                                 | 示例                                        |
> | ---- | ------------------------ | ------------------------------------ | ------------------------------------------- |
> | `G`  | Era 标志符               | [Text](#text)                        | `AD`                                        |
> | `y`  | 年                       | [Year](#year)                        | `1996`; `96`                                |
> | `M`  | 年中的月份               | [Month](#month)                      | `July`; `Jul`; `07`                         |
> | `w`  | 年中的周数               | [Number](#number)                    | `27`                                        |
> | `W`  | 月份中的周数             | [Number](#number)                    | `2`                                         |
> | `D`  | 年中的天数               | [Number](#number)                    | `189`                                       |
> | `d`  | 月份中的天数             | [Number](#number)                    | `10`                                        |
> | `F`  | 月份中的星期             | [Number](#number)                    | `2`                                         |
> | `E`  | 星期中的天数             | [Text](#text)                        | `Tuesday`; `Tue`                            |
> | `a`  | Am/pm 标记               | [Text](#text)                        | `PM`                                        |
> | `H`  | 一天中的小时数（0-23）   | [Number](#number)                    | `0`                                         |
> | `k`  | 一天中的小时数（1-24）   | [Number](#number)                    | `24`                                        |
> | `K`  | am/pm 中的小时数（0-11） | [Number](#number)                    | `0`                                         |
> | `h`  | am/pm 中的小时数（1-12） | [Number](#number)                    | `12`                                        |
> | `m`  | 小时中的分钟数           | [Number](#number)                    | `30`                                        |
> | `s`  | 分钟中的秒数             | [Number](#number)                    | `55`                                        |
> | `S`  | 毫秒数                   | [Number](#number)                    | `978`                                       |
> | `z`  | 时区                     | [General time zone](#timezone)       | `Pacific Standard Time`; `PST`; `GMT-08:00` |
> | `Z`  | 时区                     | [RFC 822 time zone](#rfc822timezone) | `-0800`                                     |

#### 一些练习

练习一：字符串"2020-09-08"转换为java.sql.Date

```java
@Test
public void testExer() throws ParseException {
    String birth = "2020-09-08";

    SimpleDateFormat sdf1 = new SimpleDateFormat("yyyy-MM-dd");
    Date date = sdf1.parse(birth);//将字符串解析为Date

    java.sql.Date birthDate = new java.sql.Date(date.getTime());//date.getTime获得毫秒数 放到sql.Date的构造器中
    //System.out.println(birthDate);
}
```
练习二："三天打渔两天晒网"   1990-01-01开始(是第1天)  问xxxx-xx-xx 打渔？晒网？
举例：1990-01-02 打渔 2     这里输出的2是总天数

> 思路：
> **总天数 % 5 == 1,2,3 : 打渔**
> **总天数 % 5 == 4,0 : 晒网**
> 总天数的计算？
> 方式一：**( date2.getTime() - date1.getTime()) / (1000 * 60 * 60 * 24) + 1**
> 方式二：1990-01-01  --> 2019-12-31 每整年的时间加起来(注意闰年) +  2020-01-01 -->2020-09-08(如果让算2020-09-08这一天)

### Calendar类

Calendar(JDK1.1)是一个抽象基类，主用用于完成日期字段之间相互操作的功能

获取Calendar实例的方法

* 使用类方法Calendar.getInstance()
* 调用它的子类GregorianCalendar的构造器


一个Calendar的实例是系统时间的抽象表示，一些方法

* int get(int field)方法来取得想要的时间信息。
  
  静态常量参数，比如YEAR、MONTH、DAY_OF_WEEK、HOUR(12小时制)、HOUR_OF_DAY(24小时制) 、MINUTE、SECOND
  返回值需注意:
  获取月份时：一月是0，二月是1...12月是11
  获取星期时：周日是1，周二是2 ...周六是7
  
* public void set(int field,int value) 将给定的日历字段设置为给定值。

* public void add(int field,int amount) 根据日历的规则，为给定的日历字段添加或减去指定的时间量。

* public final Date getTime()  返回一个表示此 Calendar 时间值（从历元至现在的毫秒偏移量）的 Date 对象。(日历类---> Date)

* public final void setTime(Date date)  使用给定的 `Date` 设置此 Calendar 的时间。(Date ---> 日历类)

代码示例

```java
   @Test
    public void testCalendar() {
        //1.实例化
        //方式一：创建其子类（GregorianCalendar的对象
        //方式二：调用其静态方法getInstance()
        Calendar calendar = Calendar.getInstance();
       //System.out.println(calendar.getClass());//class java.util.GregorianCalendar

        //2.常用方法
        //get()
        int days = calendar.get(Calendar.DAY_OF_MONTH);//这个月的第几天
        System.out.println(days);//21
        System.out.println(calendar.get(Calendar.DAY_OF_YEAR));//202 这一年的第几天
        //Calender 没有专门的格式化方法，需要程序员自己来组合显示
System.out.println(calendar.get(Calendar.YEAR) + "-" + (calendar.get(Calendar.MONTH) + 1) + "-" + calendar.get(Calendar.DAY_OF_MONTH) +" " + calendar.get(Calendar.HOUR_OF_DAY) + ":" + calendar.get(Calendar.MINUTE) + ":" + calendar.get(Calendar.SECOND) );//2022-7-21 17:44:58
        
        //set()
        //calendar可变性
        calendar.set(Calendar.DAY_OF_MONTH, 22);//将DAY_OF_MONTH设置为22
        days = calendar.get(Calendar.DAY_OF_MONTH);
        System.out.println(days);//22

        //add()
        calendar.add(Calendar.DAY_OF_MONTH, -3);//当前时间月份的第几天减3
        days = calendar.get(Calendar.DAY_OF_MONTH);
        System.out.println(days);//19

        //getTime():日历类---> Date
        Date date = calendar.getTime();
        System.out.println(date);//Tue Jul 19 17:23:05 CST 2022

        //setTime():Date ---> 日历类
        Date date1 = new Date();
        calendar.setTime(date1);
        days = calendar.get(Calendar.DAY_OF_MONTH);
        System.out.println(days);//21
    }
```



## 3.JDK 8中新日期时间API

第一代：jdk 1.0 Date类
第二代：jdk 1.1 Calendar类，一定程度上替换Date类
第三代：jdk 1.8 提出了新的一套API

JDK 1.0中包含了一个java.util.Date类，但是它的大多数方法已经在JDK 1.1引入Calendar类之后被弃用了。而Calendar并不比Date好多少。它们面临的问题是：
可变性：像日期和时间这样的类应该是不可变的。  Calendar可变
偏移性：Date中的年份是从1900开始的，而月份都从0开始。
格式化：格式化只对Date有用，Calendar则不行。
此外，它们也不是线程安全的；不能处理闰秒等。

第三次引入的API是成功的，并且Java 8中吸收了Joda-Tame的精华引入的API——java.time已经纠正了过去的缺陷。
java.time 中包含了所有关于本地日期LocalDate、本地时间LocalTime、本地日期时间LocalDateTime、时区ZonedDateTime和持续时间Duration的类。
Date 类新增了 toInstant() 方法，用于把 Date 转换成新的表示形式Instant。

新时间日期API:
**java.time** – 包含值对象的基础包
java.time.chrono – 提供对不同的日历系统的访问
**java.time.format** – 格式化和解析时间和日期
java.time.temporal – 包括底层框架和扩展特性
java.time.zone – 包含时区支持的类
说明：大多数开发者只会用到基础包和format包，也可能会用到temporal包。因此，尽管有68个新的公开类型，大多数开发者，大概将只会用到其中的三分之一

### LocalDate、LocalTime、LocalDateTime类

LocalDate、LocalTime、LocalDateTime 类是其中较重要的几个类(java.time包下)，它们的实例是**不可变的对象**，分别表示使用 ISO-8601日历系统的日期、时间、日期和时间。
它们提供了简单的本地日期或时间，并不包含当前的时间信息，也不包含与时区相关的信息。

> 注：ISO-8601日历系统是国际标准化组织制定的现代公民的日期和时间的表示法，也就是公历。

* LocalDate 只包含IOS格式的**日期**（2022-07-21）
* LocalTime只包含IOS格式的**时间**(19:49:24.849)
* LocalDateTime包含**日期和时间**（2022-07-21T19:49:24.849）——**最常用**的类之一

类似于Calendar，可以对比学习。

常用方法
![LocalXxx类常用方法](http://101.34.218.64/JavaSE.assets/LocalXxx%E7%B1%BB%E5%B8%B8%E7%94%A8%E6%96%B9%E6%B3%95.png)

```java
 //1.静态方法now() 获取根据当前时间创建的LocalDate、LocalTime、LocalDateTime类的对象
        LocalDate localDate = LocalDate.now();
        LocalTime localTime = LocalTime.now();
        LocalDateTime localDateTime = LocalDateTime.now();

        System.out.println(localDate);//2022-07-21  重写的toString()
        System.out.println(localTime);//19:19:08.112
        System.out.println(localDateTime);//2022-07-21T19:19:08.112

        //2.静态方法of() 返回指定根据指定的时间或日期或日期和时间创建的对象
        LocalDateTime localDateTime1 = LocalDateTime.of(2022,1,2,3,4,5);
        System.out.println(localDateTime1);//2022-01-02T03:04:05

        //3.getXxx() 获取对象的Xxx项 (年、月、日、时、分、秒等中的某一项)
        System.out.println("年=" + localDateTime1.getYear());//2022
        System.out.println("月=" + localDateTime1.getMonth());//JANUARY 英文月
        System.out.println("月=" + localDateTime1.getMonthValue());//1  阿拉伯数字月
        System.out.println("日=" + localDateTime1.getDayOfMonth());//2
        System.out.println("时=" + localDateTime1.getHour());//3
        System.out.println("分=" + localDateTime1.getMinute());//4
        System.out.println("秒=" + localDateTime1.getSecond());//5

        //4.withXxx()指定参数修改对象的Xxx项，返回一个新的对象。——不可变性！！！
        LocalDate localDate1 = localDate.withYear(2023);
        LocalDate localDate2=localDate1.withDayOfMonth(10);
        System.out.println(localDate2);//2023-07-10 //改了年和日

        //5.plus 和 minus 方法可以对当前时间进行加或者减,返回一个新的对象。——不可变性！！！
        //看看 890 天后，是什么时候 把 年月日-时分秒
        System.out.println("890 天后=" +localDateTime1.plusDays(890));
        //看看在 3456 分钟前是什么时候，把 年月日-时分秒输出
        System.out.println("3456 分钟前=" + localDateTime1.plusDays(890));
```



### Instant

java.time包中

① 时间线上的一个瞬时点。 概念上讲，它只是简单的表示自1970年1月1日0时0分0秒（UTC)开始的秒数。用来作时间戳
> 时间戳是指格林威治时间1970年01月01日00时00分00秒(北京时间1970年01月01日08时00分00秒)起至现在的总秒数。
>
> 因为java.time包是基于纳秒计算的，所以Instant的精度可以达到纳秒级
> 1秒 = 1000毫秒 =10^6微秒=10^9纳秒

② 类似于 java.util.Date类

常用方法：

* now() 静态方法，返回默认UTC时区的Instant类的对象
* ofEpochMilli(long epochMilli) 静态方法，返回在1970-01-01 00:00:00基础上加上指定毫秒数之后的Instant类的对象
* atOffset(ZoneOffset offset)结合即时的偏移来创建一个 OffsetDateTime
* toEpochMilli()返回1970-01-01 00:00:00到当前时间的毫秒数，即为时间戳

和Date的转换：
```java
//Instant——>Date
Date date=Date.from(instant);
//Date——>Instant
Instant instant=date.toInstant();
```

方法使用代码示例

```java
  @Test
    public void testInstant(){
        //now() 静态方法 获取UTC时区的的时间 本初子午线上的太阳时
        Instant instant= Instant.now();
        System.out.println(instant);//2022-07-21T12:45:11.546Z 显示的UTC时区的的时间 本初子午线上的太阳时

        //atOffset添加时间偏移量 返回一个OffsetDateTime对象
        OffsetDateTime offsetDateTime = instant.atOffset(ZoneOffset.ofHours(8));//加8小时才是北京时间
        System.out.println(offsetDateTime);//2022-07-21T20:45:11.546+08:00

        //toEpochMilli()返回1970-01-01 00:00:00到当前时间的毫秒数，即为时间戳--------->Date类中的getTime()
        long milli = instant.toEpochMilli();
        System.out.println(milli);//1658407778630

        //ofEpochMilli(long epochMilli)静态方法，返回在1970-01-01 00:00:00基础上加上指定毫秒数之后的Instant类的对象——不可变
        Instant instant1=Instant.ofEpochMilli(123456789L);
        System.out.println(instant1);//1970-01-02T10:17:36.789Z
    }
```



### DateTimeFormatter

java.time.format包中

格式化或解析日期、时间。相当于新型的SimpleDateFormat

该类提供了三种格式化方法：
* 预定义的标准格式。如：ISO_LOCAL_DATE_TIME;ISO_LOCAL_DATE;ISO_LOCAL_TIME
* 本地化相关的格式。如：ofLocalizedDateTime(FormatStyle.LONG)
* **自定义的格式。如：ofPattern(“yyyy-MM-dd hh:mm:ss”)**——开发中用到的 

```java
   @Test
    public void testFormat(){
        //方式一 预定义的标准格式。如：ISO_LOCAL_DATE_TIME;ISO_LOCAL_DATE;ISO_LOCAL_TIME
        DateTimeFormatter formatter=DateTimeFormatter.ISO_LOCAL_DATE;
        //格式化：日期——>字符串
        LocalDateTime localDateTime= LocalDateTime.now();
        String str =formatter.format(localDateTime);
        System.out.println(localDateTime);//2022-07-21T22:04:59.052
        System.out.println(str);//2022-07-21
        //解析： 字符串——>日期
        TemporalAccessor parse = formatter.parse("2025-11-11");
        System.out.println(parse);//"{},ISO resolved to 2025-11-11"

        //方式二 本地化相关的格式。
        // ：ofLocalizedDateTime(FormatStyle dateTimeStyle)
         //FormatStyle.LONG/FormatStyle.MEDIUM/FormatStyle.SHORT :适用于LocalDateTime
        DateTimeFormatter dateTimeFormatter1 = DateTimeFormatter.ofLocalizedDateTime(FormatStyle.LONG);
        DateTimeFormatter dateTimeFormatter2 = DateTimeFormatter.ofLocalizedDateTime(FormatStyle.MEDIUM);
        DateTimeFormatter dateTimeFormatter3 = DateTimeFormatter.ofLocalizedDateTime(FormatStyle.SHORT);
        //格式化
        System.out.println(dateTimeFormatter1.format(localDateTime));//2022年7月21日 下午10时36分59秒
        System.out.println(dateTimeFormatter2.format(localDateTime));//2022-7-21 22:36:59
        System.out.println(dateTimeFormatter3.format(localDateTime));//22-7-21 下午10:36

        //ofLocalizedDate(FormatStyle dateStyle)
        //FormatStyle.FULL/FormatStyle.LONG/FormatStyle.MEDIUM/FormatStyle.SHORT :适用于LocalDate
        DateTimeFormatter dateFormatter1 = DateTimeFormatter.ofLocalizedDate(FormatStyle.LONG);
        DateTimeFormatter dateFormatter2 = DateTimeFormatter.ofLocalizedDate(FormatStyle.MEDIUM);
        DateTimeFormatter dateFormatter3 = DateTimeFormatter.ofLocalizedDate(FormatStyle.SHORT);
        //格式化
        System.out.println(dateFormatter1.format(localDateTime));//2022年7月21日
        System.out.println(dateFormatter2.format(localDateTime));//2022-7-21
        System.out.println(dateFormatter3.format(localDateTime));//22-7-21

     //重点！！方式三 自定义的格式。如：ofPattern(“yyyy-MM-dd hh:mm:ss”)——重点！！！！！最常使用的方式
        DateTimeFormatter myFormatter= DateTimeFormatter.ofPattern("yyyy-MM-dd HH:mm:ss");
        //格式化：
        System.out.println(myFormatter.format(localDateTime));//2022-07-21 22:46:48
        //解析：
        TemporalAccessor parse1 = myFormatter.parse("2025-12-12 11:11:11");
        System.out.println(parse1);//"{},ISO resolved to 2025-12-12T11:11:11
    }
```



### 其它类

* ZoneId：该类中包含了所有的时区信息，一个时区的ID，如 Europe/Paris
* ZonedDateTime：一个在ISO-8601日历系统时区的日期时间，如 2007-12-03T10:15:30+01:00 Europe/Paris。
  其中每个时区都对应着ID，地区ID都为“{区域}/{城市}”的格式，例如：Asia/Shanghai等
* Clock：使用时区提供对当前即时、日期和时间的访问的时钟。
* 持续时间：Duration，用于计算两个“时间”间隔
* 日期间隔：Period，用于计算两个“日期”间隔
* TemporalAdjuster : 时间校正器。有时我们可能需要获取例如：将日期调整到“下一个工作日”等操作。
* TemporalAdjusters : 该类通过静态方法(firstDayOfXxx()/lastDayOfXxx()/nextXxx())提供了大量的常用TemporalAdjuster 的实现。

### 参考：与传统日期处理的转换

| 类                                                       | To 遗留类                             | From 遗留类                 |
| -------------------------------------------------------- | ------------------------------------- | --------------------------- |
| java.time.Instant与java.util.Date                        | Date.from(instant)                    | date.toInstant()            |
| java.time.Instant与java.sql.Timestamp                    | Timestamp.from(instant)               | timestamp.toInstant()       |
| java.time.ZonedDateTime与java.util.GregorianCalendar     | GregorianCalendar.from(zonedDateTime) | cal.toZonedDateTime()       |
| java.time.LocalDate与java.sql.Time                       | Date.valueOf(localDate)               | date.toLocalDate()          |
| java.time.LocalTime与java.sql.Time                       | Date.valueOf(localDate)               | date.toLocalTime()          |
| java.time.LocalDateTime与java.sql.Timestamp              | Timestamp.valueOf(localDateTime)      | timestamp.toLocalDateTime() |
| java.time.ZoneId与java.util.TimeZone                     | Timezone.getTimeZone(id)              | timeZone.toZoneId()         |
| java.time.format.DateTimeFormatter与java.text.DateFormat | formatter.toFormat()                  | 无                          |

## ==4.Java比较器==



`==`和`=!`可运用于比较引用数据类型的地址是否相等，但是若想比较引用数据类型的大小就需要比较器（在开发场景中，我们需要对多个对象进行排序，会用到比较对象大小）

Java实现对象排序的方式有两种：

* 自然排序：java.lang.Comparable
* 定制排序：java.util.Comparator

可以使用两个接口中的任何一个

### Comparable接口

像**String、包装类等实现了Comparable接口**，重写了compareTo(obj)方法，给出了比较两个对象大小的方式。
   String、包装类重写compareTo()方法以后，进行了**从小到大**的排列

实现Comparable接口的对象列表（和数组）可以通过 Collections.sort 或Arrays.sort进行自动排序。实现此接口的对象可以用作有序映射中的键或有序集合中的元素，无需指定比较器。（sort方法中用到了compareTo(obj)方法）

```java
		String[] arr = new String[]{"AA","CC","KK","MM","GG"};
        Arrays.sort(arr);//因为String实现了Comparable接口
        System.out.println(Arrays.toString(arr));//[AA, CC, GG, KK, MM]
        System.out.println("abc".compareTo("abcd"));
```

> Comparable 的典型实现：(**默认都是从小到大排列的**)
> * String：按照字符串中字符的Unicode值进行比较
> * Character：按照字符的Unicode值来进行比较
> * 数值类型对应的包装类以及BigInteger、BigDecimal：按照它们对应的数值大小进行比较
> * Boolean：true 对应的包装类实例大于 false 对应的包装类实例
> * Date、Time等：后面的日期时间比前面的日期时间大

**重写compareTo(obj)的规则**：
如果当前对象this大于形参对象obj，则返回正整数，
如果当前对象this小于形参对象obj，则返回负整数，
如果当前对象this等于形参对象obj，则返回零。

对于类 C 的每一个 e1 和 e2 来说，当且仅当 e1.compareTo(e2) == 0 与e1.equals(e2) 具有相同的 boolean 值时，类 C 的自然排序才叫做与 equals一致。建议（虽然不是必需的）**最好使自然排序与 equals 一致**

对于自定义类来说，如果需要排序，我们**可以让自定义类实现Comparable接口，重写compareTo(obj)方法**。在compareTo(obj)方法中指明如何排序。（和重写equals差不多）

```java
class Goods implements Comparable {
    private String name;
    private double price;

  /*
  ------省略了一些构造器、getter和setter、重写的toString----------------
  */

    //按价格从低到高排序
    @Override
    public int compareTo(Object o) {
        if(o==this)return 0;
        if (o instanceof Goods) {
            Goods goods = (Goods) o;
            //方式一
            if (this.price > goods.price) {return 1;}
            else if (this.price < goods.price) {return -1;}
            else {
                //return this.name.compareTo(goods.name); //如果按价格相等再按名称排的话
                 return 0;
                 }
            //return Double.compare(this.price,goods.price);//方式二
        }
        throw new RuntimeException("传入的数据类型不一致！");
    }
}

测试：
 @Test
    public void testCompareTo() {
        Goods[] arr = new Goods[3];
        arr[0]=new Goods("Lenovo鼠标",34.5);
        arr[1]=new Goods("Dell鼠标",43.5);
        arr[2]=new Goods("Xiaomi鼠标",30);
        Arrays.sort(arr);
        System.out.println(Arrays.toString(arr));
  //[Goods{name='Xiaomi鼠标', price=30.0}, Goods{name='Lenovo鼠标', price=34.5}, Goods{name='Dell鼠标', price=43.5}]
    }
```



### Comparator接口

当元素的类型没实现java.lang.Comparable接口而又不方便修改代码，或者实现了java.lang.Comparable接口的排序规则不适合当前的操作，那么可以考虑使用 Comparator 的对象(比较器)来排序
**重写compare(o1,o2)的规则**
compare(Object o1,Object o2)方法，比较o1和o2的大小：
如果方法返回正整数，则表示o1大于o2；
如果返回0，表示相等；
返回负整数，表示o1小于o2。

**可以将 Comparator 传递给 sort 方法**（如 Collections.sort 或 Arrays.sort），从而允许在排序顺序上实现精确控制。
```java
一般用匿名实现类
//1.接口的匿名实现类的有名对象
Comparator com = new Comparator() {
            @Override
            public int compare(Object o1, Object o2)  {/*...*/}
        };
Arrays.sort(goods,com);
Collections.sort(coll,com);
new TreeSet(com);

//2.接口Comparator的匿名实现类的匿名对象的方式
Arrays.sort(goods,new Comparator() {//
            @Override
            public int compare(Object o1, Object o2) {/*...*/}
        });
```

还可以使用 Comparator 来控制某些数据结构（如有序 set或有序映射）的顺序，或者为那些没有自然顺序的对象 collection 提供排序。

**重写代码示例**：

```java
import org.junit.Test;
import java.util.Arrays;
import java.util.Comparator;

public class ComparatorTest {
    @Test
    public void test() {
        //不用Goods里默认的按价格升序排，自定义比较器：按名称排列，若名称相同再按价格降序
        Goods[] arr = new Goods[4];
        arr[0]=new Goods("Lenovo鼠标",34.5);
        arr[1]=new Goods("Dell鼠标",42);
        arr[2]=new Goods("Dell鼠标",43.5);
        arr[3]=new Goods("Xiaomi鼠标",30);

        Arrays.sort(arr, new Comparator() {//接口Comparator的匿名实现类的匿名对象
            @Override
            public int compare(Object o1, Object o2) {
                if (o1 instanceof Goods && o2 instanceof Goods) {
                    Goods g1 = (Goods) o1;
                    Goods g2 = (Goods) o2;
                    if (g1.getName().equals(g2.getName())) {
                        return -Double.compare(g1.getPrice(), g2.getPrice());
                    } else {
                        return g1.getName().compareTo(g2.getName());
                    }
                }
                throw new RuntimeException("输入的数据类型不一致");
            }
        });

        System.out.println(Arrays.toString(arr));
        //[Goods{name='Dell鼠标', price=43.5}, Goods{name='Dell鼠标', price=42.0}, Goods{name='Lenovo鼠标', price=34.5}, Goods{name='Xiaomi鼠标', price=30.0}]
    }

    @Test
    public void test2() {
        //String 默认是从小到大的 改成从大到小
        String[] arr = new String[]{"AA", "CC", "KK", "MM", "GG"};
        Comparator com = new Comparator() {//接口的匿名实现类的有名对象
            @Override
            public int compare(Object o1, Object o2) {
                if (o1 instanceof String && o2 instanceof String) {
                    String s1 = (String) o1;
                    String s2 = (String) o2;
                    return -s1.compareTo(s2);//和原来的取反
                }
                throw new RuntimeException("输入的数据类型不一致！");
            }
        };
        Arrays.sort(arr, com);
        System.out.println(Arrays.toString(arr));
        //[MM, KK, GG, CC, AA]
    }
}
```

### 两种排序方式对比

*    Comparable接口的方式一旦一定，保证Comparable接口实现类的对象在任何位置都可以比较大小。
*    Comparator接口一般用于**临时性的比较**。

## 5.System类

System类代表系统，系统级的很多属性和控制方法都放置在该类的内部。该类位于java.lang包。
由于该类的**构造器是private的**，所以无法创建该类的对象，也就是无法实例化该类。
其**内部的成员变量和成员方法都是static的**，所以也可以很方便的进行调用。

* 成员变量：System类内部包含三个成员变量
  in 标准输入流(键盘输入)
  out 标准输出流(显示器)
  err 标准错误输出流(显示器)
* 成员方法：
  native long currentTimeMillis() 返回当前的计算机时间（毫秒）(时间戳)
  void exit(int status) 退出程序。其中status的值为0代表正常退出，非零代表异常退出。使用该方法可以在图形界面编程中实现程序的退出功能等
  void gc() 请求系统进行垃圾回收。至于系统是否立刻回收，则取决于系统中垃圾回收算法的实现以及系统执行时的情况
  String getProperty(String key) 获得系统中属性名为key的属性对应的值

> 系统中常见的属性名以及说明
> | key          | 说明                |
> | ------------ | ------------------- |
> | java.version | Java 运行时环境版本 |
> | java.home    | Java 安装目录       |
> | os.name      | 操作系统的名称      |
> | os.version   | 操作系统的版本      |
> | user.name    | 用户的账户名称      |
> | user.home    | 用户的主目录        |
> | user.dir     | 用户的当前工作目录  |
> （api中还有很多）


## 6.Math类

java.lang.Math提供了一系列**静态方法**用于科学计算。其方法的**参数和返回值类型一般为double**型。
abs 绝对值
acos,asin,atan,cos,sin,tan 三角函数
sqrt 平方根
pow(double a,doble b) a的b次幂
log 自然对数
exp e为底指数
max(double a,double b)
min(double a,double b)
random() 返回0.0到1.0的随机数
long round(double a) double型数据a转换为long型（四舍五入）
toDegrees(double angrad) 弧度—>角度
toRadians(double angdeg) 角度—>弧度

## 7.BigInteger与BigDecimal

Integer类能存储的最大整型值为231-1，Long类也是有限的，最大为263-1。再大的整数——BigInteger（可以很大）

一般的Float类和Double类可以用来做科学计算或工程计算，但在商业计算中，要求数字精度比较高，故用到java.math.BigDecimal类。(小数部分可以很长)

总结：

① java.math包的BigInteger可以表示不可变的任意精度的整数。构造器 BigInteger(String val)：根据字符串构建BigInteger对象
② 要求数字精度比较高(商业计算中)，用到java.math.BigDecimal类。BigDecimal类支持不可变的、任意精度的有符号十进制定点数。构造器public BigDecimal(double val)、public BigDecimal(String val)

# 第10章 枚举&注解

## 枚举

### 枚举类

enumeration 枚举

类的对象只有**有限个，确定的(**不需要修改)。我们称此类为枚举类。如：
星期：Monday(星期一)、......、Sunday(星期天)
性别：Man(男)、Woman(女)
季节：Spring(春节)......Winter(冬天)
支付方式：Cash（现金）、WeChatPay（微信）、Alipay(支付宝)、BankCard(银行卡)、CreditCard(信用卡)
就职状态：Busy、Free、Vocation、Dimission
订单状态：Nonpayment（未付款）、Paid（已付款）、Delivered（已发货）、Return（退货）、Checked（已确认）Fulfilled（已配货）、
线程状态：创建、就绪、运行、阻塞、死亡

**当需要定义一组常量时，强烈建议使用枚举类**

**如果枚举类中只一个对象**，则可以作为**单例模式**的实现方式。

枚举类的属性

* **枚举类对象的属性不应允许被改动**, 所以应该使用 **private final** 修饰
* 枚举类的使用 private final 修饰的属性应该**在构造器中为其赋值**
* 若枚举类显式的定义了**带参数的构造器**, 则在**列出枚举值时也必须对应的传入参数**

枚举类的实现
**JDK1.5之前需要自定义枚举类**
**JDK 1.5 新增的 enum 关键字用于定义枚举类**

### 方式一 自定义枚举类(了解)

1. **私有化(private)类的构造器**，保证不能在类的外部创建其对象
2. 在**类的内部创建枚举类的实例**。声明为：**public static final**——全局常量。注意**命名全部大写字母**
3. 对象如果有**实例变量**，应该声明为**private fina**l，**并在构造器中初始化**

总结 ：构造器private ， 对象public static final且要在类的内部创建， 属性private final且在构造器中初始化

```java
//自定义枚举类
class Season{
    //1.声明Season对象的属性:private final修饰
    private final String seasonName;
    private final String seasonDesc;
    //2.私化类的构造器,并给对象属性赋值
    private Season(String seasonName,String seasonDesc){
        this.seasonName = seasonName;
        this.seasonDesc = seasonDesc;
    }
    //3.提供当前枚举类的多个对象：public static final的
    public static final Season SPRING = new Season("春天","春暖花开");
    public static final Season SUMMER = new Season("夏天","夏日炎炎");
    public static final Season AUTUMN = new Season("秋天","秋高气爽");
    public static final Season WINTER = new Season("冬天","冰天雪地");
    //4.其他诉求：获取枚举类对象的属性 提供getter
    //5.其他诉求：提供重写的toString()
}
```

### 方式二 关键字enum定义枚举类

#### 关键字enum定义枚举类

* 使用 **enum 定义的枚举类默认继承了 java.lang.Enum类**，因此不能再继承其他类(是final的，用javap反编译class文件可看出)

* 枚举类的**构造器只能使用 private 权限修饰符**

* 枚举类的**所有实例必须在枚举类中显式列出(,分隔;结尾)**。列出的实例系统会**自动添加 public static final** 修饰

* ==**必须在枚举类的第一行声明枚举类对象**==

```java
  对象名A(参数),
  对象名B(参数),
  对象名C(参数);//枚举类中除了枚举常量 后面没别的成员 那么分号可以省略
  //如果使用无参构造器,小括号可以省略。
      对象名A，
      对象名B，
      对象名C;//枚举类中除了枚举常量 后面没没别的成员 那么分号可以省略
```

JDK1.5中可以在 **switch 表达式中使用Enum定义的枚举类的对象作为表达式**, **case 子句可以直接使用枚举值的名字**,无需添加枚举类作为限定。

```java
 //使用enum关键字枚举类
public enum SeasonEnum {
    //1.提供当前枚举类的对象，多个对象之间用","隔开，末尾对象";"结束
    SPRING("春天","春暖花开"),
    SUMMER("夏天","夏日炎炎"),
    AUTUMN("秋天","秋高气爽"),
    WINTER("冬天","冰天雪地");

    //2.声明Season对象的属性:private final修饰
    private final String seasonName;
    private final String seasonDesc;
    
    //3.私化类的构造器,并给对象属性赋值
    private SeasonEnum(String seasonName, String seasonDesc){
        this.seasonName = seasonName;
        this.seasonDesc = seasonDesc;
    }
    //4.其他诉求：getter
    public String getSeasonName() {return seasonName;}
    public String getSeasonDesc() {return seasonDesc;}
    //5.其它诉求:toString
    //若未重写toString则调用java.lang.Enum类中的toString 显示枚举类对象常量的名称
}

public class SeasonTest {
    public static void main(String[] args) {
        SeasonEnum season = SeasonEnum.SPRING;
        System.out.println(season);//SPRING 未重写toString则调用java.lang.Enum类中的toString 显示枚举类对象常量的名称
        System.out.println(SeasonEnum.class.getSuperclass());//class java.lang.Enum

        switch(season){
            case SPRING: System.out.println("春");break;
            case SUMMER: System.out.println("夏");break;
            case AUTUMN: System.out.println("秋");break;
            case WINTER: System.out.println("冬");break;
        }
    }
}

```



#### 继承于Enum类的主要方法

使用关键字 enum 定义枚举类时，会隐式继承 Enum 类, 这样我们就可以使用 Enum 类相关的方法。

主要的方法：(掌握toString、values、valueOf)

* **toString**:Enum类已经重写过了，返回的是**当前枚举类对象常量的名称**。**子类可以重写**该方法，用于返回对象的属性信息
* **values**：返回**当前枚举类中所有的对象常量数组**。该方法可以用于方便地**遍历所有的枚举值**。
* **valueOf**：**静态方法**。可以**把一个字符串转为对应的枚举类对象**(**根据名字找对象**)。要求**字符串必须是枚举类对象的“名字”**。如不是，会有运行时异常：IllegalArgumentException。（非法参数）
* compareTo：比较两个枚举常量，比较的就是编号！(枚举常量数组下标)
* name：返回当前对象名（常量名），作用同toString，子类中不能重写。建议优先使用toString
* ordinal：返回当前对象的位置号(枚举常量数组下标)，默认从 0 开始

代码示例:

```java
@Test
public void testEnumMethod(){
    SeasonEnum season = SeasonEnum.SPRING;
    //1、toString()   SeasonEnum未重写toString则调用java.lang.Enum类中的toString 显示枚举类对象常量的名称
    System.out.println(season);//SPRING
    //2、values():返回所的枚举类对象构成的数组
    SeasonEnum[] values = SeasonEnum.values();
    for(int i = 0;i < values.length;i++){
        System.out.print(values[i]+" ");//SPRING SUMMER AUTUMN WINTER
    }
    System.out.println("\n增强的for循环:");
    //增强的for循环(foreach循环) 
    for(SeasonEnum i:values){
        System.out.print(i+" ");
    }

    //3、valueOf(String objName):返回枚举类中对象名是objName的对象
    SeasonEnum oneSeason = SeasonEnum.valueOf("WINTER");
    System.out.println("\n"+oneSeason);//WINTER
    /*字符串必须为枚举常量名,否则抛异常
    SeasonEnum oneSeason2 = SeasonEnum.valueOf("WINTER111");
    抛参数非法异常：IllegalArgumentException: No enum constant com.loong.enum_.SeasonEnum.WINTER111
    */
}

```

又学到小技巧：增强的for循环(foreach循环) 
```java
for(元素数据类型 变量名x: 数组名){/* 对元素x的操作*/  }
for(SeasonEnum i:values){System.out.print(i+" ");}
```
更多Enum类的方法请见：

API中

| Modifier and Type             | Method and Description                                       |
| ----------------------------- | ------------------------------------------------------------ |
| `protected Object`            | `clone()`  抛出CloneNotSupportedException。                  |
| `int`                         | `compareTo(E o)`  将此枚举与指定的对象进行比较以进行订购。   |
| `boolean`                     | `equals(Object other)`  如果指定的对象等于此枚举常量，则返回true。 |
| `protected void`              | `finalize()`  枚举类不能有finalize方法。                     |
| `类<E>`                       | `getDeclaringClass()`  返回与此枚举常量的枚举类型相对应的Class对象。 |
| `int`                         | `hashCode()`  返回此枚举常量的哈希码。                       |
| `String`                      | `name()`  返回此枚举常量的名称，与其枚举声明中声明的完全相同。 |
| `int`                         | `ordinal()`  返回此枚举常数的序数（其枚举声明中的位置，其中初始常数的序数为零）。 |
| `String`                      | `toString()`  返回声明中包含的此枚举常量的名称。             |
| `static <T extends Enum<T>>T` | `valueOf(类<T> enumType, String name)`  返回具有指定名称的指定枚举类型的枚举常量。 |

还有一张图

![Enum类的方法](http://101.34.218.64/JavaSE.assets/Enum%E7%B1%BB%E7%9A%84%E6%96%B9%E6%B3%95.png)

#### 枚举类实现接口

因为 enum 会隐式继承 Enum，而 Java 是单继承机制，就不能再继承其它类了。

和普通 Java 类一样，枚举类可以实现一个或多个接口
* 若每个枚举值在调用实现的接口方法呈现相同的行为方式，则只要统一实现该方法即可。(一般情况)
* 若需要每个枚举值在调用实现的接口方法呈现出不同的行为方式,则可以让每个枚举值分别来实现该方法。(枚举类对象常量分别实现接口) **在枚举常量的逗号`,`或分号`;`前内部类重写方法。**（构造器内的局部内部类）

```java
interface Info{
    void show();
}
public enum SeasonEnumWithInterface implements Info{
    SPRING("春天","春暖花开"){
        @Override
        public void show() {
            System.out.println("春天到了，又到了。。。的季节");
        }
    },
    SUMMER("夏天","夏日炎炎"){
        @Override
        public void show() {
            System.out.println("夏天真热！！");
        }
    },
    AUTUMN("秋天","秋高气爽"){
        @Override
        public void show() {
            System.out.println("秋天收获");
        }
    },
    WINTER("冬天","冰天雪地"){
        @Override
        public void show() {
            System.out.println("天真冷");
        }
    };
/* 省略构造器、getter等 */
    /*//一般情况下的重写
    @Override
    public void show() {
        System.out.println("这是一个季节："+seasonName+" 天气特点：seasonDesc");
    }*/
}
```

#### 小插曲：修改项目三枚举类Status为使用关键字enum定义

```JAVA
public enum Status {
	FREE, VOCATION,BUSY //除了枚举常量 后面没东西 那么分号可以省略
	//这么简练！ 直接用父类的toString就获取了常量名 （原来代码中name和常量名一样） 不用为常量定义name属性了
	
}

//TeamService里用到了getName需要修改
 switch (p.getStatus()) {
            case BUSY    :throw new TeamException("该员工已是某团队成员");
            case VOCATION:throw new TeamException("该员正在休假，无法添加");
        }
```

## 注解(Annotation)

### 注解(Annotation)概述

从 **JDK 5.0 开始**, Java 增加了对元数据(MetaData) 的支持, 也就是Annotation(注解)

Annotation 其实就是代码里的**特殊标记**, 这些标记可以**在编译, 类加载, 运行时被读取, 并执行相应的处理**。通过使用 Annotation, 程序员可以**在不改变原有逻辑的情况下, 在源文件中嵌入一些补充信息**。代码分析工具、开发工具和部署工具可以通过这些补充信息进行验证或者进行部署。 前面的学习过的@Test、 @Override

**注解(Annotation)也被称为元数据(Metadata)**，用于**修饰包、类、方法、属性、构造器、参数、局部变量的声明**。这些信息被保存在 Annotation的 “name=value” 对中。

在JavaSE中，注解的使用目的比较简单，例如标记过时的功能，忽略警告等。
在JavaEE/Android中注解占据了更重要的角色，例如用来配置应用程序的任何切面，代替JavaEE旧版中所遗留的繁冗代码和XML配置等。
未来的开发模式都是基于注解的，JPA是基于注解的，Spring2.5以上都是基于注解的，Hibernate3.x以后也是基于注解的，现在的Struts2有一部分也是基于注解的了，注解是一种趋势，一定程度上可以说：**框架 = 注解 + 反射 + 设计模式**。

### 常见的Annotation示例

使用 Annotation 时要在其前面增加 **@ 符号**, **并把该 Annotation 当成一个修饰符使用**。用于修饰它支持的程序元素。

#### 示例一：生成文档相关的注解

@author 标明开发该类模块的作者，多个作者之间使用,分割
@version 标明该类模块的版本
@see 参考转向，也就是相关主题
@since 从哪个版本开始增加的
@param 对方法中某参数的说明，如果没有参数就不能写
@return 对方法返回值的说明，如果方法的返回值类型是void就不能写
@exception 对方法可能抛出的异常进行说明 ，如果方法没有用throws显式抛出的异常就不能写
其中
@param @return 和 @exception 这三个标记都是只用于方法的。
@param的格式要求：@param 形参名 形参类型 形参说明
@return 的格式要求：@return 返回值类型 返回值说明
@exception的格式要求：@exception 异常类型 异常说明
@param和@exception可以并列多个

```java
/**
 * @author shkstart
 * @version 1.0
 * @see Math.java
 */
public class JavadocTest {
    /**
     * 程序的主方法，程序的入口
     * @param args String[] 命令行参数
     */
    public static void main(String[] args) {
    }
    /**
     * 求圆面积的方法
     * @param radius double 半径值
     * @return double 圆的面积
     */
    public static double getArea(double radius){
        return Math.PI * radius * radius;
    }
}
```



#### 示例二：在编译时进行格式检查(JDK内置的三个基本注解)

@Override: 限定**重写**父类方法,。该注解只能用于方法
@Deprecated: 用于表示所修饰的元素(类, 方法等)**已过时**(即不推荐使用，但是仍然可以使用)。通常是因为所修饰的结构危险或存在更好的选择
@SuppressWarnings: **抑制编译器警告**（取消警告提示）

> 各自的声明周期
> @SuppressWarnings("deprecation")  //编译器警告过时（source阶段） 
> @Deprecated						//过时（Runtime阶段） 
> @Override						//重写（source阶段）

```java
public class AnnotationTest{
    public static void main(String[] args) {
        @SuppressWarnings("unused") 
        int a = 10;// 变量a未使用过 的警告被抑制  
        //IDEA中鼠标放在变量上 有黄色小灯泡 选移除局部变量"a"右边> ——指定生成的位置 对语句禁止。也可以看右边的小黄条
    }
    @Deprecated
    public void print(){
        System.out.println("过时的方法");
    }
    @Override
    public String toString() {
        return "重写的toString方法()";
    }
}
```

 >@Override 注解放在 fly 方法上，表示子类的 fly 方法时重写了父类的 fly
 >* 这里如果没有写 @Override，编译器不回去校验。重写了方法，仍构成重写；方法名等写错了不构成重写，也不会给警告。
 >
 >* 如果你写了@Override 注解，编译器就会去检查该方法是否真的重写了父类的方法(从编译层面验证)
 >如果的确重写了，则编译通过，如果没有构成重写，则编译错误
 >
 >* 看看 @Override 的定义中，
 >
 >  有@interface。 @interface和interface没有关系，@interface 表示一个 注解类，JDK5.0才引入的。
 >
 >   @Target(ElementType.METHOD)说明@Override只能修饰方法。 @Target是修饰注解的注解，是元注解。
 >
 >```java
 > import java.lang.annotation.*;
 > 
 > @Target(ElementType.METHOD)
 > @Retention(RetentionPolicy.SOURCE)
 > public @interface Override {
 > }
 >```

> .@Deprecated 修饰某个元素, 表示该元素已经过时。即不推荐使用，但是仍然可以使用。
> 查看 @Deprecated 注解类的源码
>
> ```java
> @Documented
> @Retention(RetentionPolicy.RUNTIME) //可以做到新旧版本的兼容和过渡
> @Target(value={CONSTRUCTOR, FIELD, LOCAL_VARIABLE, METHOD, PACKAGE, PARAMETER, TYPE})//可以修饰方法，类，字段, 包, 参数等等
> public @interface Deprecated {
> }
> ```

> 当我们看到一些警告的时候，可以使用 SuppressWarnings 注解来抑制警告信息。SuppressWarnings(String[] value)
> 在{""} 中，可以写入你希望抑制(不显示)警告信息。一个时可以省略大括号。
> @SuppressWarnings({"rawtypes", "unchecked", "unused"})
> @SuppressWarnings("unused")
>
> unchecked 忽略没有检查的警告 
> rawtypes 忽略没有指定泛型的警告（传参时没有指定泛型的警告错误）
> unused忽略没有使用某个变量的警告

#### 示例三：跟踪代码依赖性，实现替代配置文件功能

* Servlet3.0提供了注解(annotation),使得不再需要在web.xml文件中进行Servlet的部署。

```java
@WebServlet("/login")
public class LoginServlet extends HttpServlet {
    private static final long serialVersionUID = 1L;
    protected void doGet(HttpServletRequest request, HttpServletResponse response) throws
            ServletException, IOException { }
    protected void doPost(HttpServletRequest request, HttpServletResponse response) throws
            ServletException, IOException {
        doGet(request, response);
    } }
```

```xml
<servlet>
  <servlet-name>LoginServlet</servlet-name>
  <servlet-class>com.servlet.LoginServlet</servlet-class>
</servlet>
<servlet-mapping>
  <servlet-name>LoginServlet</servlet-name>
  <url-pattern>/login</url-pattern>
</servlet-mapping>
```

* spring框架中关于“事务”的管理

```java
    @Transactional(propagation=Propagation.REQUIRES_NEW,
            isolation=Isolation.READ_COMMITTED,readOnly=false,timeout=3)
    public void buyBook(String username, String isbn) {
//1.查询书的单价
        int price = bookShopDao.findBookPriceByIsbn(isbn);
//2. 更新库存
        bookShopDao.updateBookStock(isbn);
//3. 更新用户的余额
        bookShopDao.updateUserAccount(username, price);
    }
```

```
<!-- 配置事务属性 -->
<tx:advice transaction-manager="dataSourceTransactionManager" id="txAdvice">
	<tx:attributes>
	<!-- 配置每个方法使用的事务属性 -->
	<tx:method name="buyBook" propagation="REQUIRES_NEW"
		isolation="READ_COMMITTED" read-only="false" timeout="3" />
     </tx:attributes>
</tx:advice>
```



### 自定义Annotation

(实际开发中几乎不自定义注解)

如何自定义注解：参照@SuppressWarnings定义


 * ① 注解声明为：@interface
 * ② 内部定义成员，通常使用value表示
 * ③ 可以指定成员的默认值，使用default定义
 * ④ 如果自定义注解没成员，表明是一个标识作用。例如@Override

说明：
如果注解有成员，在使用注解时，需要指明成员的值。
自定义注解必须配上注解的信息处理流程(使用反射)才意义。
自定义注解通过都会指明两个元注解：Retention、Target

示例：

```JAVA
@Retention(RetentionPolicy.RUNTIME)
@Target(ElementType.TYPE)
@interface MyAnnotation{
   // String value();//用的时候必须给个value @MyAnnotation("hello") 或@MyAnnotation(value = "hello")
   String value() default "hello";//有默认值 用的时候不必需value，也可以给。 可以@MyAnnotation 或 @MyAnnotation()
}
```

> PPT上的内容：
>
> * 定义新的 Annotation 类型使用 @interface 关键字
> * 自定义注解**自动继承了java.lang.annotation.Annotation接口**
> * Annotation 的成员变量在 Annotation 定义中以无参数方法的形式来声明。其方法名和返回值定义了该成员的名字和类型。我们称为配置参数。
>
>   类型(返回值)只能是八种基本数据类型、String类型、Class类型、enum类型、Annotation类型、以上所有类型的数组。(void不行，二维或以上数组、其它对象等也不行)
> * 可以在定义 Annotation 的成员变量时为其指定初始值, 指定成员变量的初始值可使用 default 关键字
> * 如果只有一个参数成员，建议使用参数名为value
> * 如果定义的注解含有配置参数，那么使用时必须指定参数值，除非它有默认值。格式是“参数名 = 参数值”，如果只有一个参数成员，且名称为value，可以省略“value=”
> * 没有成员定义的 Annotation (例如@Override)称为标记; 包含成员变量的 Annotation 称为元数据 Annotation
>
> 注意：自定义注解必须配上注解的信息处理流程才有意义。

### JDK中的元注解
元注解（meta-annotation）：对现有的注解进行解释说明的注解。(修饰注解的注解)
jdk5.0的4种元注解：
* Retention：指定所修饰的 Annotation 的生命周期：SOURCE\CLASS(默认这个)\RUNTIME.（注解的生命周期）
       **只声明为RUNTIME生命周期的注解，才能通过反射获取**。
   
* Target:用于指定被修饰的 Annotation 能用于修饰哪些程序元素。(注解可以在哪些地方使用)
----------下面的两个使用频率低-------------
* Documented:表示所修饰的注解在被javadoc解析时，保留下来。（该注解是否会在 javadoc 体现）

* Inherited:被它修饰的 Annotation 将具继承性。(父类被@Inherited修饰的注解某修饰了，子类会继承父类的该注解)

--->类比：元数据的概念：String name = "Tom"; //Tom是最重要的 其它的是修饰他的



（1）@Retention: 只能用于修饰一个 Annotation 定义, 用于指定该 Annotation 的生命周期, @Retention 包含一个 RetentionPolicy 类型的成员变量`RetentionPolicy value();`使用@Rentention 时必须为该 value 成员变量指定值:
`public enum RetentionPolicy{ SOURCE,CLASS,RUNTIME}`注释保留策略

* RetentionPolicy.SOURCE:在源文件中有效（即源文件保留），编译器直接丢弃这种策略的注释
* RetentionPolicy.CLASS:在class文件中有效（即class保留） ， 当运行 Java 程序时, JVM不会保留注解。 这是默认值
 如果注释类型声明中不存在 Retention 注释，则保留策略默认为 RetentionPolicy.CLASS。
* **RetentionPolicy.RUNTIME**:在运行时有效（即运行时保留），当运行 Java 程序时, JVM 会保留注释。**程序可以通过反射获取该注释**。
![注释保留策略](http://101.34.218.64/JavaSE.assets/%E6%B3%A8%E9%87%8A%E4%BF%9D%E7%95%99%E7%AD%96%E7%95%A5.png)
> CLASS 
>           编译器将把注释记录在类文件中，但在运行时 VM 不需要保留注释。 
> RUNTIME 
>           编译器将把注释记录在类文件中，在运行时 VM 将保留注释，因此可以反射性地读取。 
> SOURCE 
>           编译器要丢弃的注释。 

（2）@Target: 用于修饰 Annotation 定义, 用于指定被修饰的 Annotation 能用于修饰哪些程序元素。
如果注释类型声明中不存在 Target 元注释，则声明的类型可以用在任一程序元素上。
  @Target 也包含一个名为 value 的成员变量：ElementType[] value();

| 取值(ElementType) | 描述                               |
| ----------------- | ---------------------------------- |
| ANNOTATION_TYPE   | 注解类型声明                       |
| CONSTRUCTOR       | 构造方法声明                       |
| FIELD             | 属性声明（包括枚举常量）           |
| LOCAL_VARIABLE    | 局部变量声明                       |
| METHOD            | 方法声明                           |
| PACKAGE           | 包声明                             |
| PARAMETER         | 参数声明                           |
| TYPE              | 类、接口（包括注释类型）或枚举声明 |
| TYPE_PARAMETER    | 参数类型声明 （自1.8）             |
| TYPE_USE          | 使用类型声明（自1.8）              |

（3）@Documented: 用于指定被该元 Annotation 修饰的 Annotation 类将被javadoc 工具提取成文档。默认情况下，javadoc是不包括注解的。
    定义为Documented的注解必须设置Retention值为RUNTIME。
（4）@Inherited: 被它修饰的 Annotation 将具有继承性。
   如果某个类使用了被@Inherited 修饰的 Annotation, 则其子类将自动具有该注解。
  比如：如果把标有@Inherited注解的自定义的注解标注在类级别上，子类则可以继承父类类级别的注解
  实际应用中，使用较少

### 利用反射获取注解信息（在反射部分涉及）

前提：要求**此注解的元注解Retention中声明的生命周期状态为：RUNTIME**.

举例

```java
@Inherited
@Retention(RetentionPolicy.RUNTIME)//RUNTIME生命周期的注解，才能通过反射获取
public @interface MyAnnotation {
   // String value();//用的时候必须给个value @MyAnnotation("hello") 或@MyAnnotation(value = "hello")
   String value() default "hello";//有默认值 用的时候不必需value，也可以给。 可以@MyAnnotation 或 @MyAnnotation()
}

@MyAnnotation
class A{ }
class B extends A{ }//子类B

 @Test
    public void testInherited(){
        Class classOfB=B.class;//反射
        Annotation[] annotations = classOfB.getAnnotations();
        for(Annotation a:annotations){
            System.out.println(a);
        }
        //@com.loong.annotation.MyAnnotation(value=hello) 即子类继承了注解MyAnnotation
       //如果数组为空 检查@MyAnnotation的@Retention是否为RetentionPolicy.RUNTIME
    }
```

### JDK 8中注解的新特性

* 可重复注解：

  ① 在MyAnnotation上声明@Repeatable，成员值为MyAnnotations.class
  ② MyAnnotation的Target和Retention等元注解与MyAnnotations相同。

```java
@Repeatable(OneAnnotationS2.class)//jdk 8 新办法
@Retention(RetentionPolicy.RUNTIME)
@Target({TYPE, FIELD, METHOD, PARAMETER, CONSTRUCTOR, LOCAL_VARIABLE})
@interface OneAnnotation {
    String value() default "hello";
}

//@OneAnnotation(value = "haha")
//@OneAnnotation(value = "xixi") 不可以放两个注解

//@OneAnnotationS({@OneAnnotation(value = "haha"),@OneAnnotation(value = "xixi")})//老办法 定义一个注解数组

@OneAnnotation(value = "haha")
@OneAnnotation(value = "xixi") //经过新办法处理，可以放多个注解了
class Boy{}

//jdk8前老办法 定义一个注解数组
@interface OneAnnotationS{//S大写便于分辨
    OneAnnotation[] value();
}

//jdk8新办法 使用@Repeatable(OneAnnotationS2.class)修饰OneAnnotation, 并将OneAnnotationS2的元注解修改和修饰OneAnnotation的元注解相同。现在可以放两个了
@Retention(RetentionPolicy.RUNTIME)
@Target({TYPE, FIELD, METHOD, PARAMETER, CONSTRUCTOR, LOCAL_VARIABLE})
@interface OneAnnotationS2{//S大写便于分辨
    OneAnnotation[] value();
}
```



* 类型注解：

  ElementType.TYPE_PARAMETER 表示该注解能写在类型变量的声明语句中（如：泛型声明。
  ElementType.TYPE_USE 表示该注解能写在使用类型的任何语句中。

  > 在Java8之前，注解只能用于声明中使用注解，比如定义类的时候、定义方法的时候或者bean中的变量上，但是没法在方法内使用。
  >
  > 在Java8中，注解可以被用到任何使用类型的地方，比如说创建实体（new）、类型转化、implements和throws。
  >
  > 其中，可以用于类型声明和类型使用的注解，被称为类型注解。TYPE_PARAMETER和TYPE_USE
  >
  > TYPE_USE ，任意使用类型的地方。
  > TYPE_PARAMETER，任何声明类型的地方。
  >
  > https://zhuanlan.zhihu.com/p/104478670

  > 类型注解只是语法而不是语义，并不会影响java的编译时间，加载时间，以及运行时间，也就是说，编译成class文件的时候并不包含类型注解。
  >
  > https://www.cnblogs.com/binghe001/p/13033447.html

# 第11章 Java集合

本章学习
层次一：选择合适的集合类去实现数据的保存，调用其内部的相关方法。
层次二：不同的集合类底层的数据结构为何？如何实现数据的操作的：增删改查等。——源码



集合、数组都是对多个数据进行存储操作的结构，简称Java**容器**。
说明：此时的存储，主要指的是内存层面的存储，不涉及到持久化的存储（.txt,.jpg,.avi，数据库中)

一方面， 面向对象语言对事物的体现都是以对象的形式，为了方便对多个对象的操作，就要*对对象进行存储*。
另一方面，使用Array存储对象方面具有一些弊端，而Java 集合就像一种容器，可以*动态地*把多个对象的引用放入容器中。

> 数组在内存存储方面的特点：
> * 数组**初始化以后，长度就确定了**。
> * 数组声明的类型，就决定了进行元素初始化时的类型。就只**能操作指定类型的数据**了  
>
> 数组在存储数据方面的弊端：
> * 数组初始化以后，长度就不可变了。**不便于扩展**
> * 数组中提供的**属性和方法少**，不便于进行添加、删除、插入等操作，**且效率不高**。
>   同时无法直接获取存储元素的个数(获取数组中**实际元素的个数,数组没有现成的属性或方法可用**)
> * 数组存储的数据是**有序的、可重复的**。---->存储数据的特点单一（对于无序、不可重复的需求，不能满足。）

Java 集合类可以用于存储数量不等的多个对象，还可用于保存具有映射关系的关联数组。(java容器类用于保存对象)
可以**动态**保存任意多个对象
提供了一系列方便的操作对象的方法 add/remove/set/get等

集合的底层 还是数组

## 一、Java集合框架概述

### 两种体系

**Java 集合可分为 Collection 和 Map 两种体系：**

* Collection接口： **单列**数据，定义了存取一组对象的方法的集合。有**两个重要的子接口 List、Set** , 他们的实现子类都是**单列**集合
  List：元素**有序、可重复**的集合
 Set：元素**无序、不可重复**的集合
* Map 接口的实现子类 是**双列**集合，保存具有映射关系“**key-value对**”(键值对)的集合

```
|----Collection接口：单列集合，用来存储一个一个的对象
         |----List接口：存储序的、可重复的数据。  -->“动态”数组
              实现类：ArrayList、LinkedList、Vector
         |----Set接口：存储无序的、不可重复的数据   -->高中讲的“集合”(无序性 确定性 互异性)
              实现类：HashSet、LinkedHashSet、TreeSet
              
|----Map:双列数据，存储key-value对的数据   ---类似于高中的函数：y = f(x)
      实现类：HashMap LinkedHashMap TreeMap Hashtable Properties
```



### Collection接口继承树

![Collection接口继承树](http://101.34.218.64/JavaSE.assets/Collection%E6%8E%A5%E5%8F%A3%E7%BB%A7%E6%89%BF%E6%A0%91.png)

（实线是继承关系，虚线是实现关系）

![Collection接口继承树_idea](http://101.34.218.64/JavaSE.assets/Collection%E6%8E%A5%E5%8F%A3%E7%BB%A7%E6%89%BF%E6%A0%91_idea.png)

### Map接口继承树

![Map接口继承树](http://101.34.218.64/JavaSE.assets/Map%E6%8E%A5%E5%8F%A3%E7%BB%A7%E6%89%BF%E6%A0%91.png)

![Map接口继承树_idea](http://101.34.218.64/JavaSE.assets/Map%E6%8E%A5%E5%8F%A3%E7%BB%A7%E6%89%BF%E6%A0%91_idea.png)

### 开发中，List和Map用的多，Set用的少

## 二、Collection接口

### (1)Collection 接口介绍

`public interface Collection<E> extends Iterable<E>`

* Collection 接口是 List、Set 和 Queue 接口的父接口，该接口里定义的方法可用于操作 Set 集合、 List 集合、Queue 集合
* JDK不提供此接口的任何直接实现(**没有直接的实现子类**)，而是**提供更具体的子接口(如：Set和List)实现**。
* 在 Java5 之前，Java 集合会丢失容器中所有对象的数据类型，把所有对象都当成 Object 类型处理；
 从 JDK 5.0 增加了泛型以后，Java 集合可以记住容器中对象的数据类型。



|----Collection接口：单列集合，用来存储一个一个的对象
         |----List接口：存储**有序的、可重复的**数据。  -->“动态”数组
              实现类：ArrayList、LinkedList、Vector
         |----Set接口：存储**无序的、不可重复的**数据   -->高中讲的“集合”(无序性 确定性 互异性)
              实现类：HashSet、LinkedHashSet、TreeSet

### (2)Collection接口方法

1、添加
  add(Object obj)
  addAll(Collection coll)
2、获取有效元素的个数
  int size()
3、清空集合
  void clear()
4、是否是空集合
  boolean isEmpty()
5、是否包含某个元素
  boolean contains(Object obj)：是否包含某个元素。是通过**元素的equals方法**来判断是否是同一个对象.
  （按元素对象的类型调重写的，没重写调父类的，父类没有就根父类Object的equals(==比地址)）
  **使用Collection集合存储对象，要求对象所属的类满足：**
  **向Collection接口的实现类的对象中添加数据obj时，要求obj所在类要重写equals().**
  boolean containsAll(Collection c)：也是调用**元素的equals方法**来比较的。拿两个集合的元素挨个比较。
6、删除
  boolean remove(Object obj) ：通过**元素的equals方法判断是否是要删除**的那个元素。**有重复的话只会删除找到的第一个元素**
  boolean removeAll(Collection coll)：取当前集合的**差集**(A-B)。移除当前集合中coll里的所有元素。即移除它们共有的元素。**重复的也都被移除**
7、取两个集合的交集
  boolean retainAll(Collection c)：把交集的结果存在当前集合中，不影响c
8、集合是否相等 。
  boolean equals(Object obj) 当前集合和形参集合的元素都相同才可返回true。 **注意List有序 Set无序**
9、转成对象数组  Object[] toArray()  返回一个**对象数组**
10、获取集合对象的哈希值
  hashCode()
11、遍历
  iterator()：返回迭代器对象（Iterator接口的实例），用于集合遍历。**每次调用都得到一个全新的迭代器对象，默认游标都在集合的第一个元素之前**

5~8需要重写对象的equals()方法

jdk1.6 API中 （可选操作应该是）

| 返回值   | 方法 |  说明   |
| ------- | ------|------- |
| boolean | **add**(E e)  | 确保此  collection 包含指定的元素（可选操作）。 |
| boolean | **addAll**(Collection<? extends E> c)   | 将指定  collection 中的所有元素都添加到此 collection 中（可选操作）。 |
| void    | **clear**() | 移除此  collection 中的所有元素（可选操作）。 |
| boolean | **contains**(Object o) |  如果此  collection 包含指定的元素，则返回 true。 |
| boolean | **containsAll**(Collection<?> c) | 如果此  collection 包含指定 collection 中的所有元素，则返回 true。 |
| boolean | **equals**(Object o)  | 比较此  collection 与指定对象是否相等。 |
| int     | **hashCode**()  | 返回此  collection 的哈希码值。 |
| boolean | **isEmpty**() | 如果此  collection 不包含元素，则返回 true。 |
| Iterator| **iterator**() | 返回在此  collection 的元素上进行迭代的迭代器。 |
| boolean | **remove**(Object o) | 从此 collection  中移除指定元素的单个实例，如果存在的话（可选操作）。 |
| boolean | **removeAll**(Collection<?> c) | 移除此  collection 中那些也包含在指定 collection 中的所有元素（可选操作）。 |
| boolean | **retainAll**(Collection<?> c) | 仅保留此  collection 中那些也包含在指定 collection 的元素（可选操作）。 |
| int     | **size**() | 返回此 collection  中的元素数。 |
| Object  | **toArray**() | 返回包含此  collection 中所有元素的数组。 |
| `<T> T[]` | **toArray**(T[] a) | 返回包含此  collection 中所有元素的数组；返回数组的运行时类型与指定数组的运行时类型相同。 |

> "可选操作" 在 Collection 接口中执行各种添加和删除操作的方法是 可选操作（optional oper-
> ations）。这意味着实现类不需要为这些方法提供功能定义。
>
> “可选操作”：简单说就是抽象类的的某些派生类实现里，或者接口的某个实现类里面，某个方法可能是无意义的，调用该方法会抛出一个异常。
> 例如在collection的某些实现类里，里面的元素可能都是只读的，那么add这个接口是无意义的，调用会抛出UnspportedOperationException异常。
> 从设计的角度说，如果一个接口的方法设计为optional，表示这个方法不是为所有的实现而设定的，而只是为某一类的实现而设定的。
> 来自：百度知道
> http://zhidao.baidu.com/question/356773669.html

代码示例：

```java
package com.loong.collection_;


import org.junit.Test;

import java.util.*;

/**
 * @author LoongKK
 * @create 2022/7/23-10:15
 */
public class CollectionTest {
    @Test
    public void test1() {
        Collection coll = new ArrayList();
        //add(Object e) 将元素e添加到集合coll中
        coll.add("AA");
        coll.add("AA");//List可重复  返回值是布尔型 是否添加成功 不可重复的集合(Set的实现类)中返回值才有用
        coll.add(123);//自动装箱 相当于coll.add(new Integer(10))
        coll.add(true);//自动装箱
        coll.add(new Date());//匿名对象
        //size():获取添加的元素个数
        int sizeOfColl = coll.size();
        System.out.println(sizeOfColl);

        //addall(Collection c) 将集合c中的元素添加到当前集合中
        Collection coll1 = new ArrayList();
        coll1.add(456);
        coll1.add("AA");
        coll.addAll(coll1);
        System.out.println(coll);//这里是调用ArrayList的toString()

        //isEnpty() 判断当前集合是否为空
        System.out.println(coll.isEmpty());//false   ArrayList中源码return size==0;

        //clear() 清空集合的元素
        coll.clear();
        System.out.println(coll.isEmpty());//true

        //contains(Object obj) 是否包含某个元素 是通过元素的equals方法来判断是否是同一个对象
        Person p = new Person("Tom");
        coll.add(p);
        String s = "string1";
        coll.add(s);
        coll.add(1111);//自动装箱
        System.out.println(coll.contains(1111));//true
        //Integer的equals方法里 return value == ((Integer)obj).intValue(); 比value内容
        System.out.println(coll.contains(new Integer("1111"))); //true
        //Person里未重写，继承的Object的equals。 比地址。若想比内容，要在Person里重写。
        System.out.println(coll.contains(p));//true
        System.out.println(coll.contains(new Person("Tom")));//false
        //String中重写了equals 比较内容
        System.out.println(coll.contains(s));//true
        System.out.println(coll.contains("string1"));//true
        System.out.println(coll.contains(new String("string1")));//true
        //containsAll(Collection c) 也是调用**元素的equals方法**来比较的 一个集合c里的元素是否都包含在集合里
        Collection c = new ArrayList();
        c.add(1111);
        c.add("string1");
        System.out.println(coll);//[Person{name='Tom', age=0}, string1, 1111]
        System.out.println(c);//[1111, string1]
        System.out.println(coll.containsAll(c));//true
/*
ArrayList的父类AbstratList中
 public boolean containsAll(Collection<?> c) {
        for (Object e : c)
            if (!contains(e))
                return false;
        return true;
    }
 */
        //remove(Object obj) ：通过元素的equals方法判断是否是要删除的那个元素。有重复的话只会删除找到的第一个元素
        System.out.println(coll);//[Person{name='Tom', age=0}, string1, 1111]
        coll.remove(1111);
        System.out.println(coll);//[Person{name='Tom', age=0}, string1]
        //removeAll(Collection c)：取当前集合的差集。移除c中的所有元素。即移除它们共有的元素。重复的也都被移除
        coll.add("string1");
        System.out.println(coll);//[Person{name='Tom', age=0}, string1, string1]
        System.out.println(c);//[1111, string1]
        coll.removeAll(c);
        System.out.println(coll);//[Person{name='Tom', age=0}]

        //boolean retainAll(Collection c)：把交集的结果存在当前集合中，不影响c
        Collection c1 = Arrays.asList(1, 2, 3, 4, 5);//Arrays数组的工具类中的方法 返回值List 返回的是Arrays的内部类ArrayList
        Collection c2 = Arrays.asList(1, 0, 3, 6);
        System.out.println(c1);
        System.out.println(c2);
       // c1.retainAll(c2);//java.lang.UnsupportedOperationException
       /* 发生问题的原因如下：
        调用Arrays.asList()生产的List的add、remove方法时报异常，这是由Arrays.asList() 返回的是Arrays的内部类ArrayList， 而不是java.util.ArrayList。Arrays的内部类ArrayList和java.util.ArrayList都是继承AbstractList，remove、add等方法AbstractList中是默认throw UnsupportedOperationException而且不作任何操作。java.util.ArrayList重新了这些方法而Arrays的内部类ArrayList没有重新，所以会抛出异常。
        https://blog.csdn.net/qq_39416311/article/details/83688591
        */
        c1=new ArrayList(c1);//解决：转换成ArrayList
        c1.retainAll(c2);
        System.out.println(c1);//[1, 3]

        //boolean equals(Object obj) 集合是否相等 。当前集合和形参集合的元素都相同才可返回true。 注意List有序 Set无序
        Collection c3 = new ArrayList();
        Collection c4 = new ArrayList();
        c3.add(1);c3.add(2);c3.add(3);
        c4.add(1);c4.add(2);c4.add(3);
        System.out.println(c3+"\n"+c4+"\n"+c3.equals(c4));//true
        c3.remove(1);c3.add(1);//变了元素1的顺序  c3 [2,3,1]  有序的List中的抽象子类AbstractList中 定义了是按顺序一个个比较
        System.out.println(c3+"\n"+c4+"\n"+c3.equals(c4));//false

        //hashCode() 返回当前对象的哈希值
        System.out.println(coll.hashCode());//721748926 一串数字

        //集合 --->数组：toArray()  返回一个对象数组
        Object[] arr = coll.toArray();
        for(int i = 0;i < arr.length;i++){
            System.out.println(arr[i]);
        }

//拓展：数组 --->集合:调用Arrays类的静态方法asList(T ... t)  里面是可变形参 可以直接传数组
        List<String> list = Arrays.asList(new String[]{"AA", "BB", "CC"});
        System.out.println(list);

        List arr1 = Arrays.asList(new int[]{123, 456});
        System.out.println(arr1.size());//1 因为把new int[]{123, 456}这个一维数组当成一个元素了 (int[]才是引用数据类型)
        //正确方式：（元素的类型Integer是引用数据类型）
        List arr2 = Arrays.asList(new Integer[]{123, 456});//传数组
        //List arr2 = Arrays.asList(new Integer(123), new Integer(456));//可变形参
       // List arr2 = Arrays.asList(123, 456); //也可以这样 自动装箱 可变形参 每个Integer
        System.out.println(arr2.size());//2

        //  iterator() 后面学
    }
}

class Person {
    private String name;
    private int age;
    public Person() {}
    public Person(String name) {this.name = name;}
    public Person(String name, int age) {this.name = name;this.age = age;}
    public String getName() {return name;}
    public void setName(String name) {this.name = name;}
    public int getAge() {return age;}
    public void setAge(int age) {this.age = age;}
    @Override
    public String toString() {
        return "Person{" + "name='" + name + '\'' + ", age=" + age + '}';
    }
}
```

#### 学到一个小技巧：Arrays.asList

```
asList
public static <T> List<T> asList(T... a)返回一个受指定数组支持的固定大小的列表。（对返回列表的更改会“直接写”到数组。）此方法同 Collection.toArray() 一起，充当了基于数组的 API 与基于 collection 的 API 之间的桥梁。返回的列表是可序列化的，并且实现了 RandomAccess。 
此方法还提供了一个创建固定长度的列表的便捷方法，该列表被初始化为包含多个元素： 

     List<String> stooges = Arrays.asList("Larry", "Moe", "Curly");
 
参数：
a - 支持列表的数组。 
返回：
指定数组的列表视图。
```

踩了一个坑

```java
   Collection c1 = Arrays.asList(1, 2, 3, 4, 5);//Arrays数组的工具类中的方法 返回值List 返回的是Arrays的内部类ArrayList
        Collection c2 = Arrays.asList(1, 0, 3, 6);
       // c1.retainAll(c2);//java.lang.UnsupportedOperationException
       /* 发生问题的原因如下：
        调用Arrays.asList()生产的List的add、remove方法时报异常，这是由Arrays.asList() 返回的是Arrays的内部类ArrayList， 而不是java.util.ArrayList。Arrays的内部类ArrayList和java.util.ArrayList都是继承AbstractList，remove、add等方法AbstractList中是默认throw UnsupportedOperationException而且不作任何操作。java.util.ArrayList重新了这些方法而Arrays的内部类ArrayList没有重新，所以会抛出异常。
        https://blog.csdn.net/qq_39416311/article/details/83688591
        */
        c1=new ArrayList(c1);//解决：转换成ArrayList
        c1.retainAll(c2);
        System.out.println(c1);//[1, 3]
```

#### 数组和集合之间的转换小结

集合 --->数组：toArray()  返回一个对象数组

```java
        //集合 --->数组：toArray()  返回一个对象数组
        Object[] arr = coll.toArray();
        for(int i = 0;i < arr.length;i++){
            System.out.println(arr[i]);
        }
```
数组 --->集合:调用Arrays类的静态方法asList(T ... t)  里面是可变形参 可以直接传数组
```java
        List<String> list = Arrays.asList(new String[]{"AA", "BB", "CC"});
        System.out.println(list);

        List arr1 = Arrays.asList(new int[]{123, 456});
        System.out.println(arr1.size());//1 因为把new int[]{123, 456}这个一维数组当成一个元素了 (int[]才是引用数据类型)
        //正确方式：（元素的类型Integer是引用数据类型）
        List arr2 = Arrays.asList(new Integer[]{123, 456});//传数组
        //List arr2 = Arrays.asList(new Integer(123), new Integer(456));//可变形参
       // List arr2 = Arrays.asList(123, 456); //也可以这样 自动装箱 可变形参 每个Integer
        System.out.println(arr2.size());//2
```



## 三、迭代器接口Iterator

遍历**Collection**的两种方式：
① 使用迭代器Iterator  ② foreach循环（或增强for循环）

### (1)迭代器接口Iterator

对 collection 进行迭代的迭代器

**Collection接口继承了Iterable接口**.(Map不能直接用， entrySet()将所有的map集合转为set集合)

java.util包下定义的迭代器接口：Iterator

> 几个接口的区分
> java.util.Iterator迭代器接口  抽象方法hasNext()、next()、remove()，jdk1.8新增默认方法forEachRemaining(Consumer<? super E> action)
>        java.util.ListIterator 接口扩展(extends)了 Iterator 接口,是 Collection API 中的接口。可以按任一方向遍历列表、迭代期间修改列表，并获得迭代器在列表中的当前位置
>
> java.lang.Iterable接口   该接口有一个iterator()方法 ，**Collection接口继承了Iterable接口**，那么所有实现了Collection接口的集合类都有一个iterator()方法，用以返回一个实现了 Iterator接口的对象(迭代器)。(**iterator()方法返回一个迭代器**)  。jdk8新增默认方法forEach(Consumer<? super T> action)
>

**Iterator对象称为迭代器**(设计模式的一种)，主要用于遍历 Collection 集合中的元素。
 GOF给迭代器模式的定义为：提供一种方法访问一个容器(container)对象中各个元素，而又不需暴露该对象的内部细节。迭代器模式，就是为容器而生。
Iterator 仅用于遍历集合，Iterator 本身并不提供承装对象的能力。如果需要创建Iterator 对象，则必须有一个被迭代的集合。
**集合对象==每次==调用iterator()方法都得到一个全新的迭代器对象，默认游标都在集合的第一个元素之前。**

**接口方法**：

* boolean **hasNext**() 
  如果仍有元素可以迭代，则返回 true 。  在调用next()方法之前调用hasNext()进行检测。若不调用，且
  下一条记录无效，直接调用next()会抛出NoSuchElementException异常。

* E **next**() 
  返回迭代中的下一个元素。  （**作用：①指针下移 ②将下移以后集合位置上的元素返回**）
  如果没有下一个元素，会抛出NoSuchElementException异常
  
* void **remove**() 
  从迭代器指向的 collection 中移**除迭代器返回的最后一个元素**（可选操作）。
  （Iterator可以删除集合的元素，但是是遍历过程中**通过迭代器对象的remove方法**，不是集合对象的remove方法。）
  ①**每次调用 next 只能调用一次此方法。**  如果尚未调用 next 方法，或者在上一次调用 next 方法之后已经调用了 remove 方法，则抛异常IllegalStateException
  ②如果进行迭代时用调用此方法之外的其他方式修改了该迭代器所指向的 collection，则迭代器的行为是不确定的。 
  
  > 这个涉及到 fast-fail 机制（快速失败），可以提前预料遍历失败情况，防止数组越界异常。
  >ArrayList中：（**迭代期间修改集合会报异常** ConcurrentModificationException）
  > 在创建迭代器之后，**除非通过迭代器自身的 remove 或 add 方法**从结构上对集合进行修改，否则在任何时间以任何方式对列表进行修改，迭代器都会抛出 ConcurrentModificationException。
  >  因此，面对并发的修改，迭代器很快就会完全失败，而不是冒着在将来某个不确定时间发生任意不确定行为的风险。

​        ③jdk1.8中，这个方法用default修饰  default void remove() {throw new supportedOperationException("remove");}

* default void forEachRemaining(Consumer<? super E> action) （自JDK1.8新增默认方法）(action - 要为每个元素执行的操作)
对每个剩余元素执行给定的操作，直到所有元素都被处理或动作引发异常。 

使用：

```java
举例：遍历集合
Iterator iterator = coll.iterator();
//hasNext():判断是否还有下一个元素
while (iterator.hasNext()) {
    //next():①指针下移 ②将下移以后集合位置上的元素返回
    System.out.println(iterator.next());
}

举例：删除集合中的对象“Tom”和456
        coll.add("Tom");//异常java.util.ConcurrentModificationException 上面有个迭代器了 迭代期间修改集合会报异常
        iterator = coll.iterator();//上次遍历结束之后 要重新获取一个迭代器。 （上面的代码也没异常了。？？）
        System.out.println(coll);
        while (iterator.hasNext()) {
            //next():①指针下移 ②将下移以后集合位置上的元素返回
            Object obj = iterator.next();//注:调用next()一次就会下移一次。每次迭代要只调用一次,可以用一个对象存起来
            //System.out.println(obj);
            if(Integer.valueOf(456).equals(obj)){
                iterator.remove();// 每次调用 next 只能调用一次remove方法。
            }
            if("Tom".equals(obj)){
                iterator.remove();// 每次调用 next 只能调用一次此方法。
            }
        }
        System.out.println(coll);
/*
[123, 456, Person{name='Tom', age=0}, Person{name='Jerry', age=0}, false, Tom]
[123, Person{name='Tom', age=0}, Person{name='Jerry', age=0}, false]
 */
/*  
//当然也可以用普通的for  开发中不推荐
for (int i = 0; i < coll.size(); i++) {
	System.out.println(iterator.next());
}*/
```



### (2)foreach循环(自JDK1.5)

又叫“增强for循环”。

```
for(元素类型 元素名：集合名或数组名){
    访问元素
}
```
IDEA使用小技巧：**集合或数组名.for 可以快速生成foreach**

* Java 5.0 提供了 foreach 循环迭代访问 **Collection**和**数组**。
* 不需获取Collection或数组的长度，无需使用索引访问元素
* foreach遍历集合类型和数组类型底层实现的不同:
  集合类型的遍历本质是使用**迭代器**实现的；(可以调试的时候查看，在for上断点，然后强制步入）（list,set,map）
  数组的遍历是通过**for循环**来实现的.
  https://www.itdaan.com/blog/2016/06/01/e334ddcc05da53d3fe8af4d028ef147f.html
代码示例：

```java
//for(集合元素的类型 局部变量 : 集合对象)
    for(Object obj : coll){
        System.out.println(obj);
    }

  //for(数组元素的类型 局部变量 : 数组对象)
    for(int a : arr){
        System.out.println(a);
    }
```
关于foreach修改集合元素
底层是迭代器 会有异常ConcurrentModificationException

关于foreach修改数组元素:——修改数组元素时 最好用普通的for
增强for循环的元素变量x，就是一个形参（局部变量），它是引用数组当前元素引用的副本，或者是基本数据类型的值的副本。——用值传递来理解
**基本类型数组，不可修改。**
**引用类型数组**（**除String类型**），不能改变引用，仅可以改变对象的属性（x.属性=xxx或x.xx()）
  String类型由于”不可变性“ 也是不可以修改的


### JDK8新特性(了解)：

①Iterator接口中定义的默认方法  forEachRemaining

```java
 default void forEachRemaining(Consumer<? super E> action) {
        Objects.requireNonNull(action);
        while (hasNext())
            action.accept(next());
    }
 action是要为每个元素执行的操作。对每个剩余元素执行给定的操作，直到所有元素都被处理或动作引发异常。 如果指定了该顺序，则按迭代的顺序执行操作。 动作抛出的异常被转发给呼叫者
```

在 Java SE 8 中， 甚至不用写循环。可以调用 forEachRemaining 方法并提供一lambda表达式（它会处理一个元素）。 将对迭代器的每一个元素调用这个 lambda 表达式，直到再没有元素为止。

使用 用迭代器调用

```java
Iterator<Integer> iterator= collection.iterator();
//调用forEachRemaining()方法遍历集合元素
iterator.forEachRemaining(ele -> System.out.println(ele));
//注意：此时iterator.hasNext()为false
```
②Iterable接口中的默认方法forEach

```java
   default void forEach(Consumer<? super T> action) {
        Objects.requireNonNull(action);
        for (T t : this) {
            action.accept(t);
        }
    }
//对Iterable的每个元素执行给定的操作，直到所有元素都被处理或动作引发异常。 除非实现类另有规定，否则按照迭代的顺序执行操作（如果指定了迭代顺序）。 动作抛出的异常被转发给呼叫者。
```
默认实现的行为： for (T t : this) action.accept(t);  ——forEach内部实现为foreach(而foreach内部还是迭代器。。。)

使用 用集合调用

```java
coll.forEach(obj-> System.out.println(obj));
或
coll.forEach(System.out::println)
```

>  二者区别
>
>  forEachRemaining是Iterator的方法，forEach是集合本身的方法。
>  forEachRemaining本质是 while(iterator.hasNext()){iterator.next()} 操作，调用了hasNext所以cursor最后超出，对于一个Iterator对象来说这是不可逆的。
>  forEach本质是 for (Type e : collection) {...} 



## 四、Collection子接口一：List

|----Collection接口：单列集合，用来存储一个一个的对象
         |----List接口：存储**有序的、可重复的**数据。  -->“动态”数组
              实现类：ArrayList、LinkedList、Vector
         |----Set接口：存储**无序的、不可重复的**数据   -->高中讲的“集合”(无序性 确定性 互异性)
              实现类：HashSet、LinkedHashSet、TreeSet

### List接口概述
java.util.List接口继承于Collection接口

* 鉴于Java中数组用来存储数据的局限性，我们**通常使用List替代数组**
* List集合类中元素**有序**、**可重复**，集合中的每个元素都有其对应的**顺序索引**。
* List容器中的元素都对应一个整数型的序号记载其在容器中的位置，**可以根据序号存取容器中的元素**。
* JDK API中**List接口的实现类常用**的有：**ArrayList、LinkedList和Vector**。

==重点！记住！==：

```
|---Collection接口：单列集合，用来存储一个一个的对象
     |----List接口：存储序的、可重复的数据。  -->“动态”数组,替换原的数组
         |----ArrayList：作为List接口的主要实现类；线程不安全的，效率高；底层使用Object[] elementData存储
         |----LinkedList：对于频繁的插入、删除操作，使用此类效率比ArrayList高；底层使用双向链表存储
         |----Vector：作为List接口的古老实现类；线程安全的，效率低；底层使用Object[] elementData存储
```

### List接口方法

List除了从Collection集合继承的方法外，List 集合里添加了一些根据索引来操作集合元素的方法。

存储的元素的要求：**添加的对象，所在的类要重写equals()方法**

==**常用的:**==

增：add(Object obj) 
删：remove(int index) 移除指定index位置的元素，并返回此元素 / remove(Object obj) Collection接口中的remove
改：set(int index, Object ele)设置指定index位置的元素为ele，**返回该位置之前的元素**
查：get(int index) 获取指定index位置的元素
插：add(int index, Object ele)在index位置插入ele元素
长度：size()
遍历：① Iterator迭代器方式
     ② 增强for循环
     ③ 普通的循环 get(index)

> * void add(int index, Object ele):在index位置插入ele元素
> * boolean addAll(int index, Collection eles):从index位置开始将eles中的所有元素添加进来
> * Object get(int index):获取指定index位置的元素
> * int indexOf(Object obj):返回obj在集合中首次出现的位置
> * int lastIndexOf(Object obj):返回obj在当前集合中末次出现的位置
> * Object remove(int index):移除指定index位置的元素，并返回此元素
> * Object set(int index, Object ele):设置指定index位置的元素为ele。**返回该位置之前的元素**
> * List subList(int fromIndex, int toIndex):返回从fromIndex到toIndex位置(**注意：[start，end）**)的子集合 **返回的是List**

### List实现类之一：ArrayList

* ArrayList 是 List 接口的典型实现类、主要实现类
* 本质上，ArrayList是对象引用的一个”变长”数组（动态数组）
*  ArrayList 中允许存放 null，而且可以多个
* ArrayList的JDK1.8之前与之后的实现区别？
  JDK1.7：ArrayList像饿汉式，**直接创建一个初始容量为10的数组**。以后若需要扩容，则扩容为原来的1.5倍
  JDK1.8：ArrayList像懒汉式，**一开始创建一个长度为0的数组，当添加第一个元素时再创建一个始容量为10的数组**。以后若需要扩容，则扩容为原来的1.5倍


> 小知识：数组工具类Arrays的asList方法的返回值
> Arrays.asList(…) 方法返回的 List 集合，既不是 ArrayList 实例，也不是Vector 实例。
> Arrays.asList(…) 返回值是一个**固定长度的** List 集合



#### JDK7 ArrayList源码分析

```java
 ArrayList list = new ArrayList();//底层创建了长度是10的Object[]数组elementData
*      list.add(123);//elementData[0] = new Integer(123);
*      ...
*      list.add("第11次添加");//如果此次的添加导致底层elementData数组容量不够，则扩容。
*      默认情况下，扩容为原来的容量的1.5倍，同时需要将原有数组中的数据复制到新的数组中。
*
*      结论：建议开发中使用带参的构造器：ArrayList list = new ArrayList(int capacity)
```



```java
 private transient Object[] elementData;//底层存储 对象数组
 private int size;//元素实际个数
 public ArrayList() { //空参构造器
        this(10);//空参构造器里调用的有参构造 创建了长度(length)(容量)是10的Object[]数组elementData
    }
 public ArrayList(int initialCapacity) {//构造器，参数是初始容量  initial初始 Capacity容量
        super();
        if (initialCapacity < 0)//如果初始化长度参数小于0，异常
            throw new IllegalArgumentException("Illegal Capacity: "+initialCapacity);
        this.elementData = new Object[initialCapacity];//创建了长度(容量)(length)是initialCapacity的Object[]数组elementData
    }
 public boolean add(E e) {//添加元素
 
        ensureCapacityInternal(size + 1); //如果再添加一个元素，确保在容量以内
        elementData[size++] = e;//
        return true;
    }
   private void ensureCapacityInternal(int minCapacity) {
        modCount++;//集合修改次数 涉及到快速失败机制,这里不分析
        // overflow-conscious code
        if (minCapacity - elementData.length > 0)//如果添加元素后的个数如果大于当前的容量，则扩容
            grow(minCapacity);
    }
       private void grow(int minCapacity) {
        // overflow-conscious code
        int oldCapacity = elementData.length;
        int newCapacity = oldCapacity + (oldCapacity >> 1);//原来容量的1.5倍 (右移一位是除以2)
        if (newCapacity - minCapacity < 0)
            newCapacity = minCapacity;
        if (newCapacity - MAX_ARRAY_SIZE > 0)
            newCapacity = hugeCapacity(minCapacity);
        // minCapacity is usually close to size, so this is a win:
        elementData = Arrays.copyOf(elementData, newCapacity);//拷贝到新数组
    }

 public ArrayList(Collection<? extends E> c) {//构造器 参数是集合 直接把集合的转化成对象数组，size直接拿过来的
        elementData = c.toArray();
        size = elementData.length;
        // c.toArray might (incorrectly) not return Object[] (see 6260652)
        if (elementData.getClass() != Object[].class)
            elementData = Arrays.copyOf(elementData, size, Object[].class);
    }
```

#### JDK8 ArrayList源码分析


1) ArrayList中维护了-个Object类型的数组elementData. [debug看源码]
transient Object[] elementData; //transient表示瞬间，短暂的，表示该属性不会被序列号
2)当创建ArrayList对象时， 如果使用的是无参构造器，则初始elementData容量为0,第1次添加，则扩容elementData为10,如需要再次扩容，则扩容elementData为1.5倍。
3)如果使用的是指定大小的构造器，则初始elementData容量为指定大小， 如果需要扩容，则直接扩容elementData为1.5倍。

扩容差异体现在创建对象时，使用的无参构造器还是指定容量参数的构造器。
无参——**初始elementData容量为0**——**第一次添加，扩容elementData为10**——后面若需扩容，为原来的1.5倍(第11次添加 扩为15 ，16次：22，23：33、、、)
有参，指定initialCapacity——初始elementData容量为initialCapacity——后面若需扩容，为原来的1.5倍（initialCapacity+1次添加 扩容为1.5*initialCapacity=y,第y+1次添加扩容为1.5y设为z）

```java
    private static final int DEFAULT_CAPACITY = 10;

    private static final Object[] EMPTY_ELEMENTDATA = {};

    private static final Object[] DEFAULTCAPACITY_EMPTY_ELEMENTDATA = {};

   //任何elementData == DEFAULTCAPACITY_EMPTY_ELEMENTDATA的空ArrayList，当第一个元素被添加时，都会被扩展为DEFAULT_CAPACITY(这里是10)
    transient Object[] elementData; // non-private to simplify nested class access

    private int size;

    /**
     * Constructs an empty list with an initial capacity of ten. 这句注释可能是忘了改了1.7里才是初始长度10，1.8一直到java17里都没改。。。https://qa.1r1g.com/sf/ask/2358212741/
     */
    public ArrayList() {
        this.elementData = DEFAULTCAPACITY_EMPTY_ELEMENTDATA;//创建了一个空的elementDate数={} (容量0)
    }


    public ArrayList(int initialCapacity) {
        if (initialCapacity > 0) {
            this.elementData = new Object[initialCapacity];
        } else if (initialCapacity == 0) {
            this.elementData = EMPTY_ELEMENTDATA;
        } else {
            throw new IllegalArgumentException("Illegal Capacity: "+initialCapacity);
        }
    }
    
	  public boolean add(E e) {
        ensureCapacityInternal(size + 1);
        elementData[size++] = e;
        return true;
    }
    
    private void ensureCapacityInternal(int minCapacity) {
        ensureExplicitCapacity(calculateCapacity(elementData, minCapacity));
    }
    
    private static int calculateCapacity(Object[] elementData, int minCapacity) {//确定minCapacity
        if (elementData == DEFAULTCAPACITY_EMPTY_ELEMENTDATA) {//是第一次添加
            return Math.max(DEFAULT_CAPACITY, minCapacity);//返回的minCapacity为DEFAULT_CAPACITY=10  第一次扩容为10
        }
        return minCapacity;//如果不是第一次扩容就把minCapacity直接返回去
    }
    
    private void ensureExplicitCapacity(int minCapacity) {
        modCount++;

        // overflow-conscious code
        if (minCapacity - elementData.length > 0)//这里第一次添加的话，比较minCapacity=10，length=0肯定是>0的 就会扩容  
            grow(minCapacity);
    }
     private static final int MAX_ARRAY_SIZE = Integer.MAX_VALUE - 8;

    private void grow(int minCapacity) {
        // overflow-conscious code
        int oldCapacity = elementData.length;
        int newCapacity = oldCapacity + (oldCapacity >> 1);//第二次及以后 为1.5倍原来的
        if (newCapacity - minCapacity < 0)
            newCapacity = minCapacity;//第一次 0-10<0  新的容量为10
        if (newCapacity - MAX_ARRAY_SIZE > 0)
            newCapacity = hugeCapacity(minCapacity);
        // minCapacity is usually close to size, so this is a win:
        elementData = Arrays.copyOf(elementData, newCapacity);//复制 并返回新数组
    }
```

### List实现类之二：LinkedList

对于频繁的插入或删除元素的操作，建议使用LinkedList类，效率较高

> 关于LinkedList在API中介绍：List 接口的链接列表实现。实现所有可选的列表操作，并且允许所有元素（包括 null）。
> 除了实现 List 接口外，LinkedList 类还为在列表的开头及结尾 get、remove 和 insert 元素提供了统一的命名方法。这些操作允许将链接列表用作堆栈、队列或双端队列。
> 此类实现 Deque 接口，为 add、poll 提供先进先出队列操作，以及其他堆栈和双端队列操作。

常见新增方法：
 void addFirst(E e) 将指定元素插入此列表的开头。 
 void addLast(E e) 将指定元素添加到此列表的结尾。 
 E getFirst()  返回此列表的第一个元素。 
 E getLast() 返回此列表的最后一个元素。 
 E removeFirst()  移除并返回此列表的第一个元素。 
 E removeLast()   移除并返回此列表的最后一个元素。 

#### 源码分析

LinkedList：**双向链表**，内部没有声明数组，而是定义了Node类型的first和last，用于记录首末元素。同时，定义内部类Node，作为LinkedList中保存数据的基本结构。Node除了保存数据，还定义了两个变量：
* prev变量记录前一个元素的位置
* next变量记录下一个元素的位置

```java
    transient int size = 0;
    transient Node<E> first;//Pointer to first node.
    transient Node<E> last;  // Pointer to last node.

   private static class Node<E> {
        E item;
        Node<E> next;
        Node<E> prev;
		//结点结构[直接前驱prev|item|直接后继next]
        Node(Node<E> prev, E element, Node<E> next) {
            this.item = element;
            this.next = next;
            this.prev = prev;
        }
    }
 
    public LinkedList() {
    }
    public LinkedList(Collection<? extends E> c) {
        this();
        addAll(c);
    }

    /**
     * Links e as last element.
     */
    void linkLast(E e) {
        final Node<E> l = last;
        final Node<E> newNode = new Node<>(l, e, null);//新Node：[之前的last|存储的对象e|null]
        last = newNode;//新node是最后一个
        if (l == null)//如果之前的last指向null 说明空表。 新node给first
            first = newNode;
        else
            l.next = newNode;// 否则 (之前last位置的next)指向newnode 
        size++;
        modCount++;
    }

 public boolean add(E e) {
        linkLast(e);
        return true;
    }
```



### List 实现类之三：Vector

Vector 是一个古老的集合，JDK1.0就有了。(jdk1.0。List、ArrayList、LinkedList都是jdk1.2)

**大多数操作与ArrayList相同**，区别之处在于**Vector是线程安全的**。(操作方法带有synchronized，是同步方法)



一些源码看小区别

通过**Vector()构造器**创建对象时，底层都创建了**长度为10的数组**。
在扩容方面，默认扩容为原来的数组长度的**2倍**。
操作方法带有synchronized，是同步方法。——**Vector是线程安全的**。

```java
jdk1.8中的源码
public Vector() {
        this(10);//像1.7时的ArrayList 初始容量10的数组
    }
    。。。。
        public synchronized boolean add(E e) {//操作方法带有synchronized 线程安全
        modCount++;
        ensureCapacityHelper(elementCount + 1);
        elementData[elementCount++] = e;
        return true;
    }
。。。。。。。。。
      private void grow(int minCapacity) {
        int oldCapacity = elementData.length;
   int newCapacity = oldCapacity + ((capacityIncrement > 0) ?capacityIncrement : oldCapacity);//2倍
        if (newCapacity - minCapacity < 0)
            newCapacity = minCapacity;
        if (newCapacity - MAX_ARRAY_SIZE > 0)
            newCapacity = hugeCapacity(minCapacity);
        elementData = Arrays.copyOf(elementData, newCapacity);
    }
```



### 面试题
(1)面试题：ArrayList、LinkedList、Vector者的异同？
 同：三个类都是实现了List接口，存储数据的特点相同：存储序的、可重复的数据
 不同：

```
|---Collection接口：单列集合，用来存储一个一个的对象
     |----List接口：存储序的、可重复的数据。  -->“动态”数组,替换原的数组
         |----ArrayList：作为List接口的主要实现类；线程不安全的，效率高；底层使用Object[] elementData存储
         |----LinkedList：对于频繁的插入、删除操作，使用此类效率比ArrayList高；底层使用双向链表存储
         |----Vector：作为List接口的古老实现类；线程安全的，效率低；底层使用Object[] elementData存储
```

还有一些源码分析的结论 底层实现、如何扩容的 

【面试题】

```java
    @Test
    public void testListRemove() {
        List list = new ArrayList();
        list.add(1);
        list.add(2);
        list.add(3);
        updateList(list);
        System.out.println(list);//[1,3]
    }
    private static void updateList(List list) {
        list.remove(2);
    }
    //考察 自动装箱和拆箱 遇上重载时
    remove(int index) 移除指定index位置的元素，并返回此元素。List接口的方法
    remove(Object obj) Collection接口中的remove
构成重载!!如果传入整数 优先调用remove(index)。若想删除这个对象2可以remove(Integer.valueOf(2))
//一个位置既能写基本数据,也能写包装类,自动装箱和自动拆箱就会失去效果 
```

面试题：请问ArrayList/LinkedList/Vector的异同？谈谈你的理解？ArrayList底层是什么？扩容机制？Vector和ArrayList的最大区别?
（1） ArrayList和LinkedList的异同

* 二者都线程不安全，相对线程安全的Vector，执行效率高。
* 此外，ArrayList是实现了基于动态数组的数据结构，LinkedList基于链表的数据结构：
**对于随机访问get和set，ArrayList觉得优于LinkedList，因为LinkedList要移动指针。**
**对于新增和删除操作add(特指插入)和remove，LinkedList比较占优势，因为ArrayList要移动数据。**

<img src="http://101.34.218.64/JavaSE.assets/ArrayList%20%E5%92%8C%20LinkedList%20%E7%9A%84%E6%AF%94%E8%BE%83.png" alt=" " style="zoom: 67%;" />

（2） ArrayList和Vector的区别
* Vector和ArrayList几乎是完全相同的,唯一的区别在于**Vector是同步类**(synchronized)，属于强同步类。因此开销就比ArrayList要大，访问要慢。
  正常情况下,大多数的Java程序员使用ArrayList而不是Vector,因为同步完全可以由程序员自己来控制。(工具类Collections里有一个`synchronizedList(List<T> list)` 返回一个线程安全的List)
* **Vector**每次扩容请求其大小的**2倍**空间，而**ArrayList是1.5倍。**
* Vector还有一个子类Stack。



在各种list中，最好把ArrayList作为缺省选择。
当插入、删除频繁时，使用LinkedList；
Vector总是比ArrayList慢，所以尽量避免使用。(很少用)。正常情况下,大多数的Java程序员使用ArrayList而不是Vector,因为同步完全可以由程序员自己来控制。(工具类Collections里有一个`synchronizedList(List<T> list)` 返回一个线程安全的List)

## 五、Collection子接口二：Set

### Set接口概述

|----Collection接口：单列集合，用来存储一个一个的对象
         |----List接口：存储**有序的、可重复的**数据。  -->“动态”数组
              实现类：ArrayList、LinkedList、Vector
         |----Set接口：存储**无序的、不可重复的**数据   -->高中讲的“集合”(无序性 确定性 互异性)
              |----HashSet：作为Set接口的主要实现类；线程不安全的；可以存储null值
                  |----LinkedHashSet：作为HashSet的子类；遍历其内部数据时，可以按照添加的顺序遍历
                 在添加数据的同时，每个数据还维护了两个引用，记录此数据前一个数据和后一个数据。 
                 对于频繁的遍历操作，LinkedHashSet效率高于HashSet.
              |----TreeSet：可以照添加对象的指定属性，进行排序。

特点：

* **无序。无序不等于随机性。**存储的数据在底层数组中并非照数组索引的顺序添加(而且Set没有索引)：如HashSet是**根据数据的哈希值决定的**，虽然不是按照添加顺序排列，但是还是排列顺序固定的。
* **不可重复**。保证添加的元素照equals()判断时，不能返回true.即：相同的元素只能添加一个。如果试把两个相同的元素加入同一个Set 集合中，则添加操作失败，返回false。（也是可以包括null的，但最多包含一个）

实现类：HashSet、LinkedHashSet、TreeSet

Set接口是Collection的子接口，**set接口没有提供额外的方法**

遍历方式：迭代器、 增强for，但是**不能使用索引的方式**

**Set 判断两个对象是否相同**不是使用 `==` 运算符，而是**根据 equals() 方法**。


> ????????存在疑问
>
> HashSet中add元素  new Person("Tom",12)和new Person("Tom",12)
>
> 未重写equals() 方法的情况下，是Object的实质上是`==`的equals()。Set调用equals，此时两个Person地址不同，认为是不同的，都可以add成功，set中有两个Person。
>
> 重写equals()方法的情况下，
>     若未重写hashCode()，还是都可以add成功，set中有两个Person。没有调用重写的equals()方法
>     若重写hashCode()方法,第一个add成功，第二个失败，set中有1个Person。
> 调用两次hashCode,再调用一次equals

==存储对象所在类的要求==：
(1)HashSet/LinkedHashSet:
要求：向Set(主要指：HashSet、LinkedHashSet)中添加的数据，其所在的类一定要重写hashCode()和equals()
重写要求：重写的hashCode()和equals()尽可能保持一致性：相等的对象必须具有相等的散列码
重写两个方法的小技巧：对象中用作 equals() 方法比较的 Field，都应该用来计算 hashCode 值。
(2)TreeSet:
1.自然排序中，比较两个对象是否相同的标准为：compareTo()返回0.不再是equals().
2.定制排序中，比较两个对象是否相同的标准为：compare()返回0.不再是equals().



### Set实现类之一：HashSet

HashSet 是 Set 接口的典型实现，大多数时候使用 Set 集合时都使用这个实现类。
HashSet 按 Hash 算法来存储集合中的元素，因此具有很好的存取、查找、删除性能。

HashSet 具有以下特点：
* 不能保证元素的排列顺序
* HashSet 不是线程安全的
* 集合元素可以是 null。因为不能重复，所以只能有一个null

HashSet 集合判断两个元素相等的标准：两个对象通过 hashCode() 方法比较相等，并且两个对象的 equals() 方法返回值也相等。
**对于存放在Set容器中的对象，对应的类一定要重写equals()和hashCode(Object obj)方法，以实现对象相等规则**。即：“==**相等的对象必须具有相等的散列码**==”。

>**在基于哈希实现的容器里，如果想使用某个类，不仅需要定义它的hashCode()方法，还需要定义equals()方法**。这两个方法一起使用，才能实现对哈希容器的正确查找。--- on java
>
>必须重写hashcode这样说并不严谨，只有**用到Set,Map这种依赖hashcode的容器**的时候，才必须要重写equals。如果你只是想简单的比较两个student类的对象是否相等，没必要重写hashcode。但是，set，map这种容器在开发中是非常常见的，如果你忽视了写equals导致报错会给后续的维护带来不便，所以在重写equals的时候，把hashcode顺带重写了是很有必要的。——网友

#### **HashSet元素添加过程**：

> PPT上的文字：向HashSet中添加元素的过程：
> * 当向 HashSet 集合中存入一个元素时，HashSet 会调用该对象的 hashCode() 方法来得到该对象的 hashCode 值，然后根据 hashCode 值，通过某种散列函数决定该对象在 HashSet 底层数组中的存储位置。（这个散列函数会与底层数组的长度相计算得到在数组中的下标，并且这种散列函数计算还尽可能保证能均匀存储元素，越是散列分布，该散列函数设计的越好）
> * 如果两个元素的hashCode()值相等，会再继续调用equals方法，如果equals方法结果为true，添加失败；如果为false，那么会保存该元素，但是该数组的位置已经有元素了，那么会通过链表的方式继续链接。
>
> 如果两个元素的 equals() 方法返回 true，但它们的 hashCode() 返回值不相等，hashSet 将会把它们存储在不同的位置，但依然可以添加成功。 （于是我们要自己重写方法 保证equals返回true时，hashCode()肯定相等）

我们向HashSet中添加元素a,首先调用元素a所在类的hashCode()方法，计算元素a的哈希值，
此哈希值接着通过某种算法（散列函数）计算出在HashSet底层数组中的存放位置（即为：索引位置)，判断数组此位置上是否已经元素：
    如果此位置上没其他元素，则元素a添加成功。 --->情况1
    如果此位置上其他元素b(或以链表形式存在的多个元素——链地址法)，则比较元素a与元素b的hash值(存的时候存的key、value、hash，b的hash是不需要重新计算的)：
        如果hash值不相同，则元素a添加成功。--->情况2
        如果hash值相同，进而需要调用元素a所在类的equals()方法：
               equals()返回true,元素a添加失败
               equals()返回false,则元素a添加成功。--->情况3

对于添加成功的情况2和情况3而言：元素a 与已经存在指定索引位置上数据以链表的方式存储。
jdk 7 :元素a放到数组中，指向原来的元素。
jdk 8 :原来的元素在数组中，指向元素a
总结：七上八下
自己画的示意图：
![](http://101.34.218.64/JavaSE.assets/Set%E4%B8%83%E4%B8%8A%E5%85%AB%E4%B8%8B.png)

HashSet底层是**HashMap**，维护了**数组+链表**的结构。（jdk7。dk8的HashMap 数组+链表，当链表>8，链表转换为红黑树，方便查询)

```java
private transient HashMap<E,Object> map;
public HashSet() {
        map = new HashMap<>();//底层也是数组，初始容量为16，当如果使用率超过0.75，（16*0.75=12）就会扩大容量为原来的2倍。（16扩容为32，依次为64,128....等）
    }

//HashMap，HashSet插入的元素其实是key
private static final Object PRESENT = new Object();//全局常量PRESENT 是固定的 共享的。 同一个value
  public boolean add(E e) {
        return map.put(e, PRESENT)==null;//
    }
```



不重写hashCode()则 Object里的hashCode()根据对象的地址随机计算，返回哈希值。 这种情况下如果对象不一样 那肯定hash基本上是不一样(极小极小可能一样)。

不重写equlas()则 Object里的equlas()用==比较对象的地址，如果对象不一样 false

> 一些拙见：
>
> hashCode()算出来的哈希值(散列码、hashcode)可能相同（即**散列码不唯一**）—— 如hashCode（）里return name.hashCode()+age；可能24+20=44  20+24=44（改进：return namehashCode()乘31+age，放大这些数的差别） 再如Object里的万一两个不同的对象随机成一样的呢—— **hash相等，对象不一定相等**。故还需要equals去判断两对象是不是真的相等。  
>
> hashCode主要是计算出来散列码**快速**的找到一个存放位置。如果不采用hashCode 直接靠equals一个个去比效率是极低的。
>
>    (**自己重写hashCode时要保证对象相等(equals返回true)，hash肯定相等**。逆否：**hash不等，对象一定不等**。因为时固定的hashCode算出来的。
>除非没重写，用的Object里的hashCode()随机出来的，才会导致对象相等，hash不等的囧态)	
> 
> 
>
> 哈希值不一样 也可能算出的“索引”位置一样——**散列冲突 （又叫哈希冲突 哈希碰撞hashcollision）** 想想 3%10=3  13%10=3
>
> HashSet添加元素过程：
>
> **hashCode**（）算出hash值————>hash值 通过散列函数算出 索引
>      数组[索引]上没有其它元素——>元素a添加
>      数组[索引]上有其它元素b(也可能是链表形式存在的多个元素)(**散列冲突**)——>比元素a和b的hash值
>             hash不相同(想想3 13)，a添加成功
>             hash相同 （ return Objects.hash(name, age);只要name和age相同 ）,再调用元素a所在类的**equlas**方法
>                  a.equals(b)返回true 则元素a不能添加，添加失败     重写equals返回true 比name和age   两个new Person("Tom",12)
>                  a.equals(b)返回false 则元素a能添加，添加成功     不重写equals时，用Object里的相当于==返回false 比地址   


#### 重写 equals() 方法的基本原则
以自定义的Customer类为例，何时需要重写equals()？
 当一个类有自己特有的“逻辑相等”概念,当改写equals()的时候，总是要改写hashCode()，根据一个类的equals方法（改写后），两个截然不同的实例有可能在逻辑上是相等的，但是，根据Object.hashCode()方法，它们仅仅是两个对象。
因此，违反了“相等的对象必须具有相等的散列码”。
结论：**复写equals方法的时候一般都需要同时复写hashCode方法。通常参与计算hashCode的对象的属性也应该参与到equals()中进行计算**
(开发中用自动生成的)


#### 重写 hashCode() 方法的基本原则

在程序运行时，同一个对象多次调用 hashCode() 方法**应该**返回相同的值。
当两个对象的 **equals() 方法比较返回 true 时**，这两个对象的 hashCode()方法的返回值(Hash值)**也应相等**。
**对象中用作 equals() 方法比较的 Field，都应该用来计算 hashCode 值。**
(开发中用自动生成的)
> 为什么用Eclipse/IDEA复写hashCode方法，有31这个数字？
>
> *选择系数的时候要选择尽量大的系数。因为如果计算出来的hash地址越大，所谓的“冲突”就越少，查找起来效率也会提高。（减少冲突）
> * 并且31只占用5bits,相乘造成数据溢出的概率较小。
> * 31可以 由i*31== (i<<5)-1来表示,现在很多虚拟机里面都有做相关优化。（提高算法效 率）
> * 31是一个素数，素数作用就是如果我用一个数字来乘以这个素数，那么最终出来的结果只能被素数本身和被乘数还有1来整除！(减少冲突)
>
> 在2，4，8，16，32，64  和左右的数里选 ，因为要素数2 7 17 31  要选大的 就31了



#### Set实现类之二：LinkedHashSet

LinkedHashSet 是 HashSet 的子类
* LinkedHashSet 也是根据元素的 hashCode 值来决定元素的存储位置，**但它同时使用双向链表维护元素的次序，这使得元素看起来是以插入顺序保存的**。

  底层是一个**LinkedHashMap**，底层维护了一个**数组(哈希表)+双向链表**。(双向链表有head和tail)

* **LinkedHashSet插入性能略低于 HashSet**，但在**迭代访问 Set 里的全部元素时有很好的性能**

  (**优点：对于频繁的遍历操作，LinkedHadhSet效率高于HashSet**)。

* LinkedHashSet 也不允许集合元素重复。

![LinkedHashSet底层机制示意](http://101.34.218.64/JavaSE.assets/LinkedHashSet%E5%BA%95%E5%B1%82%E6%9C%BA%E5%88%B6%E7%A4%BA%E6%84%8F.png)

### Set实现类之三：TreeSet

TreeSet 是 SortedSet 接口的实现类，TreeSet 可以确保集合元素**处于排序状态**。
   因为只有相同类的两个实例才会比较大小，所以==**向 TreeSet 中添加的应该是同一个类的对象（类型相同的对象）**==，否则发生ClassCastException异常。向 TreeSet 中添加元素时，只有第一个元素无须比较。
TreeSet底层使用**红黑树**结构存储数据。TreeSet和后面要讲的TreeMap采用红黑树的存储结构
 特点：**有序，查询速度比List快**
  红黑树的讲解参看http://www.cnblogs.com/yangecnu/p/Introduce-Red-Black-Tree.html

<img src="http://101.34.218.64/JavaSE.assets/%E7%BA%A2%E9%BB%91%E6%A0%91%E7%A4%BA%E6%84%8F.png" alt="红黑树示意.png" style="zoom:50%;" />

新增的方法如下： (了解)
  Comparator comparator()
  Object first()
  Object last()
  Object lower(Object e)
  Object higher(Object e)
  SortedSet subSet(fromElement, toElement)
  SortedSet headSet(toElement)
  SortedSet tailSet(fromElement)

==TreeSet 两种排序方法：自然排序和定制排序。**默认情况下，TreeSet 采用自然排序**。==

**自然排序中，比较两个对象是否相同的标准为：compareTo()返回0.不再是equals().**
**定制排序中，比较两个对象是否相同的标准为：compare()返回0.不再是equals().**

①**自然排序**：TreeSet 会调用集合元素的 **compareTo(Object obj)** 方法来比较元素之间的大小关系，然后将集合元素按**升序(默认)**排列
    如果**试图把一个对象添加到 TreeSet 时**，则**该对象的类必须实现 Comparable接**，实现 Comparable 的类必须**实现 compareTo(Object obj) 方法**，两个对象即通过compareTo(Object obj) 方法的返回值来比较大小。复习：[Comparable接口](#Comparable接口)

> 重写该对象对应的 equals() 方法时，应保证该方法与 compareTo(Object obj) 方法有一致的结果.否则，让人难以理解

②**定制排序**：如果元素所属的类没有实现Comparable接口，或不希望按照升序(默认情况)的方式排列元素，或希望按照其它属性大小进行排序，则考虑使用定制排序。
要实现定制排序，需要**将实现Comparator接口的实例==作为形参传递给TreeSet的构造器==**。复习：[Comparator接口](#Comparator接口)

```java
    @Test
    public  void testTreeSet(){
        TreeSet treeSet = new TreeSet();
        treeSet.add(123);
        treeSet.add(456);
        //因为只有相同类的两个实例才会比较大小，所以向 TreeSet 中添加的应该是同一个类的对象。
        //treeSet.add("AA");//java.lang.ClassCastException
        treeSet.add(34);
        treeSet.add(-34);
        treeSet.add(43);
        treeSet.add(11);
        treeSet.add(8);
        System.out.println(treeSet);//[-34, 8, 11, 34, 43, 123, 456] 自然排序，默认升序 Interger中的compareTo()
        System.out.println(treeSet.descendingSet());//[456, 123, 43, 34, 11, 8, -34]
        Iterator iterator = treeSet.iterator();//iterator()返回在此 set 中的元素上按升序进行迭代的迭代器。
        while(iterator.hasNext()){
            System.out.println(iterator.next());
        }
        Iterator iterator1 = treeSet.descendingIterator();//descendingIterator()返回在此 set 元素上按降序进行迭代的迭代器。
        while(iterator1.hasNext()){
            System.out.println(iterator1.next());
        }
        System.out.println("----------------定制排序---------------------");
        //定制排序
        //实在想不出场景 自己编一个吧 比如按某种自定义的规则排序 比如 按每个数离50的距离 由近到远
        Comparator com = new Comparator() {
            @Override
            public int compare(Object o1, Object o2) {
                //按年龄从小到大
                //if(o1==o2)return 0;//因为给set用 不可能有重复的 那就去了？
                if(o1 instanceof Integer && o2 instanceof Integer){
                    Integer i1=(Integer)o1;
                    Integer i2=(Integer)o2;
                    return Math.abs(i1-50)-Math.abs(i2-50);
                }else{
                    throw new RuntimeException("传入的数据类型不一致");
                }
            }
        };
        TreeSet treeSet1 = new TreeSet(com);
        treeSet1.addAll(treeSet);
        System.out.println(treeSet1);//按年龄从小到大
        //[Person{name='Tom', age=8}, Person{name='Army', age=10}, Person{name='Tom', age=12}, Person{name='Daming', age=13}]
        System.out.println(treeSet.descendingSet());
        //[Person{name='Tom', age=12}, Person{name='Tom', age=8}, Person{name='Daming', age=13}, Person{name='Army', age=10}]
        Iterator iterator2 = treeSet1.iterator();//iterator()返回在此 set 中的元素上按升序进行迭代的迭代器。
        while(iterator2.hasNext()){
            System.out.println(iterator2.next());
        }
        Iterator iterator3 = treeSet1.descendingIterator();//descendingIterator()返回在此 set 元素上按降序进行迭代的迭代器。
        while(iterator3.hasNext()){
            System.out.println(iterator3.next());
        }

    }

    @Test
    public  void testTreeSet1(){
        //自然排序
        TreeSet treeSet = new TreeSet();
        treeSet.add(new Person("Tom",12));
        treeSet.add(new Person("Army",10));
        treeSet.add(new Person("Daming",13));
        treeSet.add(new Person("Tom",8));//重名 年龄不同
        System.out.println(treeSet);
        //[Person{name='Army', age=10}, Person{name='Daming', age=13}, Person{name='Tom', age=8}, Person{name='Tom', age=12}]
        System.out.println(treeSet.descendingSet());
        //[Person{name='Tom', age=12}, Person{name='Tom', age=8}, Person{name='Daming', age=13}, Person{name='Army', age=10}]
        Iterator iterator = treeSet.iterator();//iterator()返回在此 set 中的元素上按升序进行迭代的迭代器。
        while(iterator.hasNext()){
            System.out.println(iterator.next());
        }
        Iterator iterator1 = treeSet.descendingIterator();//descendingIterator()返回在此 set 元素上按降序进行迭代的迭代器。
        while(iterator1.hasNext()){
            System.out.println(iterator1.next());
        }
        System.out.println("----------------定制排序---------------------");
        //定制排序
        Comparator com = new Comparator() {
            @Override
            public int compare(Object o1, Object o2) {
                //按年龄从小到大
                //if(o1==o2)return 0;//因为给set用 不可能有重复的 那就去了？
                if(o1 instanceof Person && o2 instanceof Person){
                    Person p1=(Person)o1;
                    Person p2=(Person)o2;
                    return p1.getAge()-p2.getAge();
                }else{
                    throw new RuntimeException("传入的数据类型不一致");
                }
            }
        };
        TreeSet treeSet1 = new TreeSet(com);
        treeSet1.addAll(treeSet);
        System.out.println(treeSet1);//按年龄从小到大
        //[Person{name='Tom', age=8}, Person{name='Army', age=10}, Person{name='Tom', age=12}, Person{name='Daming', age=13}]
        System.out.println(treeSet.descendingSet());
        //[Person{name='Tom', age=12}, Person{name='Tom', age=8}, Person{name='Daming', age=13}, Person{name='Army', age=10}]
        Iterator iterator2 = treeSet1.iterator();//iterator()返回在此 set 中的元素上按升序进行迭代的迭代器。
        while(iterator2.hasNext()){
            System.out.println(iterator2.next());
        }
        Iterator iterator3 = treeSet1.descendingIterator();//descendingIterator()返回在此 set 元素上按降序进行迭代的迭代器。
        while(iterator3.hasNext()){
            System.out.println(iterator3.next());
        }
    }


class Person implements  Comparable{
.//.....
    @Override
    public int compareTo(Object o) {//先按姓名排，若姓名相同按年龄排
        if(o==this)return 0;
        if(o instanceof Person){
            Person p=(Person) o;
            if(this.name.equals(p.name)){
                return this.age-p.age;
            }else{
                return this.name.compareTo(p.name);
            }

        }
        throw new RuntimeException("传入的数据类型不一致");
    }
}

```

### 面试题

```java
//其中Person类中重写了hashCode()和equal()方法。思考输出什么？为什么？————这个题有难度
public void test2(){
        HashSet set = new HashSet();
        Person p1 = new Person(1001,"AA");
        Person p2 = new Person(1002,"BB");
        set.add(p1);
        set.add(p2);
        p1.name = "CC";
        set.remove(p1);
        System.out.println(set);//
        set.add(new Person(1001,"CC"));
        System.out.println(set);//
        set.add(new Person(1001,"AA"));
        System.out.println(set);//
    }
   /*输出：
    [Person{id=1002, name='BB'}, Person{id=1001, name='CC'}]
[Person{id=1002, name='BB'}, Person{id=1001, name='CC'}, Person{id=1001, name='CC'}]
[Person{id=1002, name='BB'}, Person{id=1001, name='CC'}, Person{id=1001, name='CC'}, Person{id=1001, name='AA'}]

 p1.name = "CC";
  set.remove(p1);// 这一步flase 通过hashCode()属性1001,"CC"算出的hash值变了 找到的存储位置是空的 故删除失败。 对象Person{id=1001, name='CC'}还在

 set.add(new Person(1001,"CC"));//可以添加成功 因为通过属性1001,"CC"算出的hash值算出的位置是空的(已有的Person{id=1001, name='CC'}的位置是name还是”AA“时算出来的) 可以添加
 
 set.add(new Person(1001,"AA"));//可以添加成功 因为通过属性1001，"AA"算出的hash值找到的位置上虽然已经有第一个Person{id=1001, name='CC'}(没修改name前，算的hash找到的位置)，但是add过程现在需要比较现在二者的hash值，新AA的hash和第一个旧AA在add时存入的hash(是取出来的 add时存入根据属性1001,"AA"算的hash，不会重新计算！！)相同，再用equals比较，此时属性新对象"AA"和位置是已有对象的"CC"不同 故可以添加

     */

/*网上别人的分析
System.out.println(set);//[Person{id=1001, name=AA}, Person{id=1001, name=BB}]
        //1.问：这⾥set⾥⾯有⼏条数据？以及原因？
        //两条，p1和p2两个对象的哈希值不⼀样，两条数据都予以存放
        p1.name = "CC";
        set.remove(p1);
        System.out.println(set);//[Person{id=1001, name=CC}, Person{id=1001, name=BB}]
        //2.问：这⾥set⾥⾯有⼏条数据？以及原因？
        //还是两条，将p1对象的name值修改为“CC”后，但是p1对象在内存中的存放地址并未改变。当调⽤remove⽅法时，会重新计算p1对象的哈希值，再去在内存中查找该数据；此时根据name和id计算出来的哈希值
        //跟原来是不⼀样的，所以根据计算出来的哈希值在内存中对应的位置，该位置是⼀条空数据，移除的也是⼀条空数据。
        set.add(new Person(1001,"CC"));
        System.out.println(set);//[Person{id=1001, name=CC}, Person{id=1001, name=BB}, Person{id=1001, name=CC}]
        //3.问：这⾥set⾥⾯有⼏条数据？以及原因？
        //3条，上⼀问中已经提到为id=1001，name=“CC”的Person对象的哈希值，在内存中对应的地址未存放数据，则予以存放该数据。
        set.add(new Person(1001,"AA"));
        System.out.println(set);//[Person{id=1001, name=CC}, Person{id=1001, name=BB}, Person{id=1001, name=CC}, Person{id=1001, name=AA}]
        //4.问：这⾥set⾥⾯有⼏条数据？以及原因？
        //这⾥添加的new Person(1001,"AA")数据跟刚开始添加的p1对象（p1.name = "CC" 未修改之前）⼀样，
        // 两个对象的哈希值⼀样，会进⼀步调⽤equals⽅法判断两个对象是否⼀样，
        // 此时的p1对象中name已修改为“CC”，结果是根据equals⽅法判断两个对象不⼀样，还是予以存放。
*/
```

问题：集合Collection中存储的如果是自定义类的对象，需要自定义类重写哪个方法？为什么？
equals()方法。 contains() /remove()/retainsAll() ….会用到

  List：equals()方法
  Set：(HashSet、LinkedHashSet为例)：equals()、hashCode()
      (TreeSet为例)：Comparable：compareTo(Object obj)
                   Comparator：compare(Object o1,Object o2)

小练习：在List内去除重复数字值 要求尽量简单

```java
    public static List duplicateList(List list) {
        HashSet set = new HashSet();
        set.addAll(list);
        return new ArrayList(set);
    }
    public static void main(String[] args) {
        List list = new ArrayList();
        list.add(new Integer(1));
        list.add(new Integer(2));
        list.add(new Integer(2));
        list.add(new Integer(4));
        list.add(new Integer(4));
        list.add("AA");
        list.add("BB");
        List list2 = duplicateList(list);
        for (Object integer : list2) {
            System.out.print(integer+" ");
        }
    }
//AA BB 1 2 4    虽然简单 但是有缺陷 set.addAll(list);时 无序
```



## 六、Map接口

```
|----Map:双列数据，存储key-value对的数据   ---类似于高中的函数：y = f(x)  可以一对一、多对一 不能一对多
       |----HashMap:作为Map的主要实现类；线程不安全的，效率高；存储null的key和value
       		HashMap 底层： 数组+链表(JDK7及以前)  数组+链表+红黑树(JDK8)
              |----LinkedHashMap:保证在遍历map元素时，可以照添加的顺序实现遍历。
          原因：在原的HashMap底层结构基础上，添加了一对引用，指向前一个和后一个元素。(维护了一个双向链表)
                 对于频繁的遍历操作，此类执行效率高于HashMap。
       |----TreeMap:保证照添加的key-value对进行排序，实现排序遍历。此时考虑key的自然排序或定制排序
                      底层使用红黑树（红黑树是一种排序二叉树）
       |----Hashtable:作为古老的实现类；线程安全的，效率低；不能存储null的key和value
              |----Properties:常用来处理配置文件。key和value都是String类型
```

Hashtable jdk1.0  那时候还没统一规范的命名 t是小写的 后来用的人多了 也就没改。HashMap 、TreeMap 1.2，LinkedHashMap 1.4

### Map接口概述

* Map与Collection并列存在。用于保存具有**映射关系**的数据:key-value。

* Map 中的 key 和 value 都可以是任何引用类型的数据。Map 的 key 可以为 null, value 也可以为 null 。注意 key 为 null,只能有一个;value 为 null ,可以多个。

* Map 中的 **key 用Set来存放，不允许重复**，即同一个 Map 对象所对应的类，须重写hashCode()和equals()方法

* 常用String类作为Map的“键”

* key 和 value 之间存在单向一对一关系，即通过指定的 key 总能找到唯一的、确定的 value

  <img src="http://101.34.218.64/JavaSE.assets/Map%EF%BC%9Akey-value%E7%A4%BA%E6%84%8F.png" alt="Map：key-value示意.png" style="zoom:80%;" />

  put（K,V）  key放在set里(不可重复) ，values放在Collection中   一对key-vlaues实际上是一个 Entry对象 用Set存储(不可重复)  

  * Map中的key:无序的、不可重复的，使用Set存储所的key  ---> key所在的类要重写equals()和hashCode() （以HashMap为例)
  * Map中的value:无序的、可重复的，使用Collection存储所的value --->value所在的类要重写equals()
  *  一个键值对：key-value构成了一个Entry对象。
  * Map中的entry:无序的、不可重复的，使用Set存储所的entry

Map接口的常用实现类：HashMap、TreeMap、LinkedHashMap和Properties。其中，**HashMap是 Map 接口使用频率最高的实现类**

### Map 中的常用方法

添加、删除、修改操作：
* Object put(Object key,Object value)：将指定key-value添加到(或修改)当前map对象中
* void putAll(Map m):将m中的所有key-value对存放到当前map中
* Object remove(Object key)：移除指定key的key-value对，并返回value
* void clear()：清空当前map中的所有数据

元素查询的操作：
* Object get(Object key)：获取指定key对应的value
* boolean containsKey(Object key)：是否包含指定的key
* boolean containsValue(Object value)：是否包含指定的value。有重复的话， 找到一个就返回true不会继续找
* int size()：返回map中key-value对的个数
* boolean isEmpty()：判断当前map是否为空
* boolean equals(Object obj)：判断当前map和参数对象obj是否相等

元视图操作的方法：（遍历） ==重点学学==
* Set keySet()：返回所有key构成的Set集合
* Collection values()：返回所有value构成的Collection集合
* Set entrySet()：返回所有key-value对构成的Set集合

**常用的几个**

* 添加：put(Object key,Object value)
* 删除：remove(Object key)
* 修改：put(Object key,Object value)
* 查询：get(Object key)
* 长度：size()
* 遍历：keySet() / values() / entrySet()

代码示例：

```java
public class MapTest {
    @Test
    public void test1() {
        HashMap map = new HashMap();
        //        添加、删除、修改操作：
//        Object put(Object key,Object value)：将指定key-value添加到(或修改)当前map对象中
        //插入
        map.put("AA", 123);
        map.put(45, 123);
        map.put("BB", 56);
        //修改
        map.put("AA", 87);
        System.out.println(map);//{AA=87, BB=56, 45=123}

//        void putAll(Map m):将m中的所有key-value对存放到当前map中
        HashMap map1 = new HashMap();
        map1.put("CC", 123);
        map1.put("DD", 123);
        map.putAll(map1);
        System.out.println(map);//{CC=123, DD=123, AA=87, BB=56, 45=123} =的左边是key 右边是value
//        Object remove(Object key)：移除指定key的key-value对，并返回value
        Object value = map.remove("CC");
        System.out.println(value);//123   如果没有”CC“ 会返回null
        System.out.println(map);//
//        void clear()：清空当前map中的所有数据
        map.clear();//不是map=null 而是清空了元素 所有的table[i]=null  size=0
        System.out.println(map.size());//0 元素个数
    }
    @Test
    public void test2() {
        HashMap map = new HashMap();
        map.put("AA", 123);
        map.put(45, 123);
        map.put("BB", 56);
////        元素查询的操作：
//        Object get(Object key)：获取指定key对应的value
        Object value = map.get("AA");
        System.out.println(value);//123
//        boolean containsKey(Object key)：是否包含指定的key
        boolean isExist = map.containsKey("AA");
        System.out.println(isExist);//true
//        boolean containsValue(Object value)：是否包含指定的value
        isExist = map.containsValue(123);//这个map有两个value是123的元素 找到一个就返回true不会继续找
//        int size()：返回map中key-value对的个数
//        boolean isEmpty()：判断当前map是否为空
        System.out.println("元素个数：" + map.size() + " 为空：" + map.isEmpty());//元素个数：3 为空：false
        map.clear();
        System.out.println("元素个数：" + map.size() + " 为空：" + map.isEmpty());//元素个数：0 为空：true
//        boolean equals(Object obj)：判断当前map和参数对象obj是否相等
        HashMap map1 = new HashMap();
        map1.put("AA", 123);
        map1.put(45, 123);
        map1.put("BB", 56);
        HashMap map2 = new HashMap(map1);
        System.out.println(map2.equals(map1));//true
    }
    @Test
    public void test3() {
        HashMap map = new HashMap();
        map.put("AA", 123);
        map.put(45, 123);
        map.put("BB", 56);
//        元视图操作的方法：
//        Set keySet()：返回所有key构成的Set集合
        System.out.println("遍历map的所有key:");
        Set keys = map.keySet();// HashSet
        for (Object key : keys) {
            System.out.println(key + "->" + map.get(key));
        }
        //        Collection values()：返回所有value构成的Collection集合
        System.out.println("遍历map的所有的value：");
        Collection values = map.values();
        Iterator iter = values.iterator();
        while (iter.hasNext()) {
            System.out.println(iter.next());
        }
        //        Set entrySet()：返回所有key-value对构成的Set集合
        System.out.println("遍历map所有的映射关系(key-value)（每个Entry）：");
       // 映射关系的类型是Map.Entry类型，它是Map接口的内部接口
        Set mappings = map.entrySet();
        for (Object mapping : mappings) {
            Map.Entry entry = (Map.Entry) mapping;
            System.out.println("key是：" + entry.getKey() + "，value是：" + entry.getValue());
        }
   }
}

```



### HashMap(**==很重要==**)

* HashMap是 Map 接口**使用频率最高**的实现类。
* 允许使用null键和null值，与HashSet一样，不保证映射的顺序。
* 重写方法：
  所有的**key构成的集合是Set**:无序的、**不可重复**的。所以，**key所在的类要重写：equals()和hashCode()**
  所有的**value构成的集合是Collection**:无序的、**可以重复**的。所以，**value所在的类要重写：equals()**
* 一个key-value构成一个entry
* 所有的entry构成的集合是Set:无序的、不可重复的
* 判断相等的标准
  HashMap 判断两个 **key 相等的标准**是：两个 **key 通过 equals() 方法返回 true，hashCode 值也相等**。
  HashMap 判断两个 **value相等的标准**是：两个 **value 通过 equals() 方法返回 true。**

#### HashMap底层实现原理

(1) JDK7中：

HashMap map = new HashMap();
在实例化以后，底层创建了长度是16的一维数组Entry[ ] table。
...可能已经执行过多次put...
map.put (key1,value1):
首先，调用key1所在类的hashCode() 计算key1哈希值，此哈希值经过某种算法计算以后（%16，其实是&15），得到在Entry数组 中的存放位置：
    A)如果此位置上的数据为空，此时的key1-value1添加成功-----情况1
    B)如果此位置上的数据不为空，(意味着此位置上存一个或多个数据(以链表形式存在))，比较key1和已经存在的一个或多个数据的哈希值  
		a.如果key1的哈希值和已经存在的数据的key的哈希值都不同，添加成功——情况2
		b.如果key1的哈希值和已经存在的某个数据(key2-value2)的key2的哈希值都相同，继续比较：调用key1所在类的equals()方法
			(a)如果equals()返回false：此时key1-value1添加成功——情况3
			(b)如果equals()返回true，**使用value1替换value2**

注：情况2和情况3：此时key1-value1和原来的数据与链表的方式存储

默认扩容方式：**扩容为原来容量的2倍**，并把原来的数据复制过来
jdk7底层结构：**数组+链表**。

 (2)JDK8中

HashMap在jdk8中相较于jdk7在底层实现方面的不同：
1. new HashMap():底层**没有**创建一个长度为16的数组

2. jdk 8底层的数组是：**Node[]**,而非Entry[]

3. **首次调用put()方法时，底层创建长度为16的数组**

4. JDK 7及以前版本：HashMap是数组+链表 (即为链地址法)
    JDK 8版本发布以后：HashMap是**数组+链表+红黑树**实现。

  4.1 形成链表时，**七上八下**（jdk7:新的元素指向旧的元素。jdk8：旧的元素指向新的元素）
  4.2 当数组的**某一个索引位置上的元素以链表形式存在的数据个数 > 8** 且**当前数组的长度 >= 64**时，此时此索引位置上的所数据**改为使用红黑树**(一种平衡二叉查找树)存储——提高查询速度。

> PPT上：
>
> 1.HashMap map = new HashMap();//默认情况下，**先不创建长度为16的数组**
> 2.当**首次调用map.put()时**，**再创建长度为16的数组**
> 3.**数组为Node类型**，在jdk7中称为Entry类型
> 4.**形成链表结构时，新添加的key-value对在链表的尾部**（七上八下）
> 5.**当数组指定索引位置的链表长度>8时，且map中的数组的长度>= 64时**，**此索引位置上的**所有key-value对使用**红黑树**进行存储。

#### HashMap 源码分析

##### **源码中的重要常量**

```java
    static final int DEFAULT_INITIAL_CAPACITY = 1 << 4; //HashMap的默认容量，16
    static final int MAXIMUM_CAPACITY = 1 << 30;//HashMap的最大支持容量，2^30
    static final float DEFAULT_LOAD_FACTOR = 0.75f;//HashMap的默认加载因子：0.75
    static final int TREEIFY_THRESHOLD = 8;//Bucket中链表长度大于该默认值，转化为红黑树:8
    static final int UNTREEIFY_THRESHOLD = 6;//Bucket中红黑树存储的Node小于该默认值，转化为链表
    static final int MIN_TREEIFY_CAPACITY = 64;//桶中的Node被树化时最小的hash表容量:64(当桶中Node的数量大到需要变红黑树时，若hash表容量小于MIN_TREEIFY_CAPACITY时，此时应执行resize扩容操作。MIN_TREEIFY_CAPACITY的值至少是TREEIFY_THRESHOLD的4倍。)
```

##### **源码中的重要变量**

```java
    //transient Entry<K,V>[] table;  //  jdk7中 存储元素的数组 长度总是2的n次幂
    transient Node<K,V>[] table;//存储元素的数组，长度(容量)总是2的n次幂 故若初始化长度为15也会是16 
    transient Set<Map.Entry<K,V>> entrySet;//存储具体元素的集
    transient int size;//HashMap中存储的键值对的数量
    transient int modCount;//HashMap扩容和结构改变的次数。
    int threshold;//扩容的临界值 =容量*填充因子：第一次 16 * 0.75 => 12
    final float loadFactor;//填充因子

存储元素的数组长度在哈希表中被称为容量(Capacity)，在这个数组中可以存放元素的位置我们称之为“桶”(bucket)
每个bucket都有自己的索引，系统可以根据索引快速的查找bucket中的元素
```

##### **JDK7源码分析**

```JAVA
静态内部类 Entry
    static class Entry<K,V> implements Map.Entry<K,V> {
        //一个元素Entry(key,value)的内部结构
        final K key;
        V value;
        Entry<K,V> next;
        int hash;
		
        Entry(int h, K k, V v, Entry<K,V> n) {//Entry的构造器
            value = v;
            next = n;
            key = k;
            hash = h;
        }
        ...getter setter equals hashCode toString等方法，，，
    }

//（1）HashMap map=new HashMap();
//HashMap的内部存储结构其实是【数组和链表】的结合。当实例化一个HashMap时，系统会创建一个长度为Capacity的【Entry数组】，这个长度在哈希表中被称为容量(Capacity)，在这个数组中可以存放元素的位置我们称之为“桶”(bucket)，每个bucket都有自己的索引，系统可以根据索引快速的查找bucket中的元素
//每个bucket中存储一个元素，即一个Entry对象，但每一个Entry对象可以带一个引用变量，用于指向下一个元素，因此，在一个桶中，就有可能生成一个Entry链。 而且【新添加的元素作为链表的head  （七上）】
而且新添加的元素作为链表的head。
public HashMap() {
        this(DEFAULT_INITIAL_CAPACITY, DEFAULT_LOAD_FACTOR);//HashMap(16,0.75)
    }
public HashMap(int initialCapacity) {
        this(initialCapacity, DEFAULT_LOAD_FACTOR);
    }
public HashMap(int initialCapacity, float loadFactor) {
        if (initialCapacity < 0)
            throw new IllegalArgumentException("Illegal initial capacity: " +
                                               initialCapacity);
        if (initialCapacity > MAXIMUM_CAPACITY)
            initialCapacity = MAXIMUM_CAPACITY;
        if (loadFactor <= 0 || Float.isNaN(loadFactor))
            throw new IllegalArgumentException("Illegal load factor: " +
                                               loadFactor);

        // Find a power of 2 >= initialCapacity
        int capacity = 1;
        while (capacity < initialCapacity)//长度(容量)总是2的n次幂 故若指定初始化长度为15也会移位为16
            capacity <<= 1;

        this.loadFactor = loadFactor;
        threshold = (int)Math.min(capacity * loadFactor, MAXIMUM_CAPACITY + 1);
        table = new Entry[capacity];//创建一个长度为capacity(16)的Entry数组
        useAltHashing = sun.misc.VM.isBooted() &&
                (capacity >= Holder.ALTERNATIVE_HASHING_THRESHOLD);
        init();
    }


//（2）map.put(key1,value1);添加元素的过程  向HashMap中添加entry1(key，value)

    public V put(K key, V value) {
        if (key == null)
            return putForNullKey(value);
        int hash = hash(key); //需要首先计算entry1中key的哈希值(根据key所在类的hashCode()计算得到)
        int i = indexFor(hash, table.length);//哈希值经过处理以后，得到在底层Entry[]数组中要存储的位置i。
        //indexFor方法中return hash & (length-1);//相当于hash%length  hash%16用hash&15算
        for (Entry<K,V> e = table[i]; e != null; e = e.next) {
         //(B)如果位置i上已经存在entry2(或还有链表存在的entry3，entry4)即e != null，则需要通过循环的方法,依次比较entry1中key和其他的entry的key
            Object k;
            if (e.hash == hash && ((k = e.key) == key || key.equals(k))) {//b.如果hash值相同((e.hash == hash)，继续比较二者是否equals 即(k = e.key) == key || key.equals(k) 这里||左边的k==key是考虑地址相等的情况，不用调用equals直接返回true
                //（b）key.equals(k)如果返回值为true，则使用entry1的value去替换equals为true的entry的value。
                V oldValue = e.value;
                e.value = value;
                e.recordAccess(this);
                return oldValue;
            }
        }
        //(A)如果位置i上没有元素（即e == null），则entry1直接添加成功(不进入for循环)
		 //a.如果彼此hash值都不同(for循环完，都不满足if的条件e.hash == hash)，则直接添加成功
            //(a)如果遍历一遍以后，发现所有的equals返回都为false,则entry1仍可添加成功
        modCount++;
        addEntry(hash, key, value, i);//将Entry的hash，key，value添加到索引i的位置
        return null;
    }
//每个bucket中存储一个元素，即一个Entry对象，但每一个Entry对象可以带一个引用变量，用于指向下一个元素，因此，在一个桶中，就有可能生成一个Entry链。 而且【新添加的元素作为链表的head  （七上）】
     void addEntry(int hash, K key, V value, int bucketIndex) {
        if ((size >= threshold) && (null != table[bucketIndex])) {//键值对数量大于扩容的临界值 且 索引位置上有元素 (如果位置上没有元素就直接放进去元素，不扩容了) 
            resize(2 * table.length);//扩容为原来的2倍
            
            //HashMap数组扩容之后，原数组中的数据必须重新计算其在新数组中的位置
            hash = (null != key) ? hash(key) : 0;
            bucketIndex = indexFor(hash, table.length);
        }
		//Entry放table
        createEntry(hash, key, value, bucketIndex);
    }

	 void createEntry(int hash, K key, V value, int bucketIndex) {
        Entry<K,V> e = table[bucketIndex];
        table[bucketIndex] = new Entry<>(hash, key, value, e);//新添加的元素作为链表的head
        size++;
    }


扩容(了解)：
void resize(int newCapacity) {
        Entry[] oldTable = table;
        int oldCapacity = oldTable.length;
        //如果老表数组已经是最大值，则不扩容直接返回
        if (oldCapacity == MAXIMUM_CAPACITY) {
            threshold = Integer.MAX_VALUE;
            return;
        }
 
        Entry[] newTable = new Entry[newCapacity];
    //HashMap数组扩容之后，【最消耗性能的点】就出现了：原数组中的数据必须重新计算其在新数组中的位置，并放进去
        //useAltHashing默认是false
        boolean oldAltHashing = useAltHashing;
        //当我们新数组大小大于 Holder.ALTERNATIVE_HASHING_THRESHOLD，这个结果为true，则rehash为true，重新计算hash
        useAltHashing |= sun.misc.VM.isBooted() &&
                (newCapacity >= Holder.ALTERNATIVE_HASHING_THRESHOLD);
        boolean rehash = oldAltHashing ^ useAltHashing;
        //老表数据迁移到新表
        transfer(newTable, rehash);
        table = newTable;
        threshold = (int)Math.min(newCapacity * loadFactor, MAXIMUM_CAPACITY + 1);
}
```

##### **JDK8源码分析**

```java
静态内部类Node的结构
static class Node<K,V> implements Map.Entry<K,V> {
        final int hash;
        final K key;
        V value;
        Node<K,V> next;

        Node(int hash, K key, V value, Node<K,V> next) {
            this.hash = hash;
            this.key = key;
            this.value = value;
            this.next = next;
        }
        //...getKey getValue toString hashCode setValue equals...... 
    }
//(1)new HashMap（） 当实例化一个HashMap时，会初始化initialCapacity(有参的构造器时)和loadFactor
//JDK8中 HashMap的内部存储结构其实是数组+链表+树的结合
   public HashMap() {
        this.loadFactor = DEFAULT_LOAD_FACTOR; //空参构造器并未创建Node[] table, 只是初始化了loadFactor为默认加载因子0.75
    }

//(2)map.put(key1,value1);
    public V put(K key, V value) {
        return putVal(hash(key), key, value, false, true);
    }
//每个bucket中存储一个元素，即一个Node对象，但每一个Node对象可以带一个引用变量next，用于指向下一个元素，因此，在一个桶中，就有可能生成一个Node链。也可能是一个一个TreeNode对象，每一个TreeNode对象可以有两个叶子结点left和right，因此，在一个桶中，就有可能生成一个TreeNode树。而【新添加的元素作为链表的last，或树的叶子结点】
    final V putVal(int hash, K key, V value, boolean onlyIfAbsent,
                   boolean evict) {
        Node<K,V>[] tab; Node<K,V> p; int n, i;
        if ((tab = table) == null || (n = tab.length) == 0)
            n = (tab = resize()).length;//如果底层的 table 数组为 null, 或者 length =0 , 就扩容到 16。
        /*put调用putVal调用resize，resize里才创建的数组！！ 和jdk7不同
          Node<K,V>[] newTab = (Node<K,V>[])new Node[newCap];
          table = newTab;
        */
        
        if ((p = tab[i = (n - 1) & hash]) == null)
            //取出 hash 值对应的 table 的索引位置的 Node, 如果为 null（该位置上无元素）
            //就直接把加入的 k-v, 创建成一个 Node ,加入该位置即可
            tab[i] = newNode(hash, key, value, null);
        else {
            Node<K,V> e; K k;
            if (p.hash == hash &&
                ((k = p.key) == key || (key != null && key.equals(k))))
                //如果hash相同且equals返回true 则替换value。 这里先把该位置已有的p给e，下面有个if里统一进行替换
                //第一个元素就是 要替换的元素
                e = p;
            else if (p instanceof TreeNode)//如果当前的 table 的已有的 Node 是红黑树，就按照红黑树的方式处理
                e = ((TreeNode<K,V>)p).putTreeVal(this, tab, hash, key, value);
            else {
                //如果找到的结点，后面是链表(链地址法)，就循环比较
                for (int binCount = 0; ; ++binCount) {////死循环
                    if ((e = p.next) == null) {//如果next是null(说明比完了整个链表(或一开始该位置就一个已有元素)，没有和他相同),就加到该链表的最后。跳出
                        p.next = newNode(hash, key, value, null);
                        //加入后，判断当前链表的个数，是否已经到 8 个，到 8 个后就调用 treeifyBin 方法进行红黑树的转换
                        if (binCount >= TREEIFY_THRESHOLD - 1) // -1 for 1st
                            treeifyBin(tab, hash);
                        break;
                    }
                    
                    //如果在循环比较过程中，发现有相同,就 break,就只是替换 value。这里e前面的e = p.next已经改过了 
                    if (e.hash == hash &&((k = e.key) == key || (key != null && key.equals(k))))
                        break;
                    p = e;
                }
            }
            
            if (e != null) { // existing mapping for key
                V oldValue = e.value;
                if (!onlyIfAbsent || oldValue == null)
                    e.value = value;//替换key 对应 value
                afterNodeAccess(e);
                return oldValue;
            }
        }//else结束
        ++modCount//快速失败 （fail-fast）有用
        if (++size > threshold)
            resize();////计算 目前的元素含量 是否大于了 threshold（负载因子*容量） ,大于开始扩容
        afterNodeInsertion(evict);//空方法 留给LinkedHashMap操作的
        return null;
    }
//树形化
   final void treeifyBin(Node<K,V>[] tab, int hash) {
        int n, index; Node<K,V> e;
        if (tab == null || (n = tab.length) < MIN_TREEIFY_CAPACITY)//<64的话去扩容 而不是树形化
            resize();
       
        else if ((e = tab[index = (n - 1) & hash]) != null) {
            TreeNode<K,V> hd = null, tl = null;
            do {
                TreeNode<K,V> p = replacementTreeNode(e, null);
                if (tl == null)
                    hd = p;
                else {
                    p.prev = tl;
                    tl.next = p;
                }
                tl = p;
            } while ((e = e.next) != null);
            if ((tab[index] = hd) != null)
                hd.treeify(tab);
        }
    }

```

![HashMap之put](http://101.34.218.64/JavaSE.assets/HashMap%E4%B9%8Bput.png)

![](http://101.34.218.64/JavaSE.assets/HashMap%E7%9A%84%E5%AD%98%E5%82%A8%E7%BB%93%E6%9E%84.png)

![HashMap源码分析_韩顺平](http://101.34.218.64/JavaSE.assets/HashMap%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90_%E9%9F%A9%E9%A1%BA%E5%B9%B3.png)

扩容后重新计算每个元素在数组中的位置，而这是一个非常消耗性能的操作，所以如果我们已经预知HashMap中元素的个数，那么**预设元素的个数能够有效的提高HashMap的性能**。使用有参构造器

> 那么HashMap什么时候进行扩容和树形化呢？
> 当HashMap中的元素个数超过数组大小(数组总大小length,不是数组中个数size)*loadFactor 时 ， 就 会 进 行 数 组 扩 容 ， loadFactor 的 默 认 值(DEFAULT_LOAD_FACTOR)为0.75，这是一个折中的取值。也就是说，默认情况下，数组大小(DEFAULT_INITIAL_CAPACITY)为16，那么当HashMap中元素个数超过16*0.75=12（这个值就是代码中的threshold值，也叫做临界值）的时候，就把数组的大小扩展为 2*16=32，即扩大一倍，然后重新计算每个元素在数组中的位置，而这是一个非常消耗性能的操作，所以如果我们已经预知HashMap中元素的个数，那么预设元素的个数能够有效的提高HashMap的性能。
>
> 当HashMap中的其中一个链的对象个数如果达到了8个，此时如果capacity没有达到64，那么HashMap会先扩容解决，如果已经达到了64，那么这个链会变成树，结点类型由Node变成TreeNode类型。当然，如果当映射关系被移除后，下次resize方法时判断树的结点个数低于6个，也会把树再转为链表。 

关于映射关系的**key**是否可以修改？answer：**不要修改**
映射关系存储到HashMap中会存储key的hash值，这样就不用在每次查找时重新计算每一个Entry或Node（TreeNode）的hash值了，因此如果已经put到Map中的映射关系，再修改key的属性，而这个属性又参与hashcode值的计算，那么会导致匹配不上。

回头看HashSet 里面用到HashMap，HashSet插入的元素其实是key
```java
//HashSet.java中
private static final Object PRESENT = new Object();//全局常量PRESENT 是固定的 共享的。 同一个value
  public boolean add(E e) {
        return map.put(e, PRESENT)==null;//
    }
```



#### 面试题

面试题：
谈谈你对HashMap中put/get方法的认识？如果了解再谈谈HashMap的扩容机制？默认大小是多少？什么是负载因子(或填充比)？什么是吞吐临界值(或阈值、threshold)？

面试题：负载因子值的大小，对HashMap有什么影响？

* 负载因子的大小决定了HashMap的数据密度。
* 负载因子越大密度越大，发生碰撞的几率越高，数组中的链表越容易长,造成查询或插入时的比较次数增多，性能会下降。
* 负载因子越小，就越容易触发扩容，数据密度也越小，意味着发生碰撞的几率越小，数组中的链表也就越短，查询和插入时比较的次数也越小，性能会更高。但是会浪费一定的内容空间。而且经常扩容也会影响性能，建议初始化预设大一点的空间。
* 按照其他语言的参考及研究经验，会考虑将负载因子设置为0.7~0.75，此时平均检索长度接近于常数

### LinkedHashMap

LinkedHashMap 是 HashMap 的子类
在HashMap存储结构的基础上，使用了一对**双向链表来记录添加元素的顺序**
与LinkedHashSet类似，LinkedHashMap 可以维护 Map 的迭代顺序：迭代顺序与 Key-Value 对的插入顺序一致

底层实现

 ```java
  //重写的newNode方法  
  Node<K,V> newNode(int hash, K key, V value, Node<K,V> e) {
        LinkedHashMap.Entry<K,V> p = new LinkedHashMap.Entry<K,V>(hash, key, value, e);
        linkNodeLast(p);
        return p;
    }

    static class Entry<K,V> extends HashMap.Node<K,V> {
        Entry<K,V> before, after;//before和after记录了插入时的直接前驱和直接后继
        Entry(int hash, K key, V value, Node<K,V> next) {
            super(hash, key, value, next);
        }
    }
 ```



### TreeMap

//向TreeMap中添加key-value，要求key必须是由同一个类创建的对象
//因为要照key进行排序：自然排序 、定制排序

* TreeMap存储 Key-Value 对时，需要根据 key-value 对进行排序。
  TreeMap 可以保证所有的 Key-Value 对处于有序状态。
* TreeSet底层使用红黑树结构存储数据
* **所有的 Key 应该是同一个类的对象**
* TreeMap 的 Key 的排序：
  **自然排序：TreeMap 的所有的 Key 必须实现 Comparable 接口**，而且**所有的 Key 应该是同一个类的对象**，否则将会抛出 ClasssCastException
  **定制排序**：**创建 TreeMap 时，传入一个 Comparator 对象**，该对象负责对TreeMap 中的所有 key 进行排序。此时**不需要 Map 的 Key 实现Comparable 接口**。new TreeMap(com);
*  TreeMap判断两个key相等的标准：两个key通过compareTo()方法或者compare()方法返回0。



### Properties

 处理属性文件

* Properties 类是 Hashtable 的子类，该对象用于**处理属性文件**
* 由于属性文件里的 key、value 都是字符串类型，所以 **Properties 里的 key和 value 都是字符串类型**
* 存取数据时，建议使用setProperty(String key,String value)方法和getProperty(String key)方法

代码示例

```java
public class PropertiesTest {
    public static void main(String[] args) {
        Properties pros = new Properties();
        FileInputStream fis = null;
        try {
            fis = new FileInputStream("jdbc.properties");
            pros.load(fis);//从文件加载道properties
            String name = pros.getProperty("name");
            String password = pros.getProperty("password");
            System.out.println("name=" + name + ",password=" + password);
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            if (fis != null) {
                try {
                    fis.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
        }

    }

    @Test
    public void test() throws Exception {
        Properties pros = new Properties();
        //pros.load(new FileInputStream("jdbc.properties"));//FileNotFoundException  在main中可以这样
        //pros.load(new FileInputStream("D:\\IdeaProjects\\project_javase\\jdbc.properties"));//解决方式1：绝对路径
        pros.load(new FileInputStream("..\\jdbc.properties"));//解决方式2:用..\\去上一层找
        String name = pros.getProperty("name");
        String password = pros.getProperty("password");
        System.out.println("name=" + name + ",password=" + password);
    }
    //FileNotFoundException 解决:可使用绝对路径或带..的上层目录。相对路径在main方法相对于src，在@test方法中相对于module
}
```

创建jdbc.propertie

* 右击项目名——新建 可以选择新建一个File 也可新建一个Resource Bundle(资源包)
    新建File要写全名字jdbc.properties
    新建Resource Bundle(资源包)写jdbc即可，不用写扩展名  
* jdbc.properties里的内容: key=value  等号左右不能有空格，因为是字符串类型的，空格也会被认为是数据。一行一条
name=Tom哈哈
password=abc123
* 中文乱码的话，设置——Editor——FileEncodings文件编码——（建议先把Global、Project的编码改成UTF-8，）属性文件.properties默认编码改成UTF-8 在"FileEncodings transparent native-to-ascii conversion"(自动转换成Ascii但显示原生内容)打上对勾，然后删文件重新创建


### 面试题

HashMap的底层实现原理(高频面试题)

HashMap和Hashtable的异同

CurrentHashMap(ConcurrentHashMap)和Hashtable区别



## 七、Collections工具类

Collections 是一个操作 Set、List 和 Map 等集合的工具类。（操作数组的工具类：Arrays）

Collections 中提供了一系列静态的方法对集合元素进行排序、查询和修改等操作，还提供了对集合对象设置不可变、对集合对象实现同步控制等方法（均为static方法）

### 排序操作：

* reverse(List)：反转 List 中元素的顺序
* shuffle(List)：对 List 集合元素进行随机排序
* sort(List)：根据元素的自然顺序对指定 List 集合元素按升序排序
* sort(List，Comparator)：根据指定的 Comparator 产生的顺序对 List 集合元素进行排序
* swap(List，int， int)：将指定 list 集合中的 i 处元素和 j 处元素进行交换

### 查找、替换

* Object max(Collection)：根据元素的自然顺序，返回给定集合中的最大元素
* Object max(Collection，Comparator)：根据 Comparator 指定的顺序，返回给定集合中的最大元素
* Object min(Collection)
* Object min(Collection，Comparator)
* int frequency(Collection，Object)：返回指定集合中指定元素的出现次数
* void copy(List dest,List src)：将src中的内容复制到dest中
* boolean replaceAll(List list，Object oldVal，Object newVal)：使用新值替换List 对象的所有旧值

### 同步控制

Collections 类中提供了多个 synchronizedXxx() 方法，该方法可使将指定集合**包装成线程同步的集合**，从而可以解决多线程并发访问集合时的线程安全问题。

说明：ArrayList和HashMap都是线程不安全的，如果程序要求线程安全，我们可以将ArrayList、HashMap转换为线程的。使用synchronizedList(List list） 和 synchronizedMap(Map map）

| 修饰符和返回值              | 方法                                    | 说明                                                     |
| --------------------------- | --------------------------------------- | -------------------------------------------------------- |
| `static <T> Collection<T> `   | `synchronizedCollection(Collecti<T> c)` | 返回指定 collection 支持的同步（线程安全的）collection。 |
| `static <T> List<T>`         | `synchronizedList(List<T> list)`          | 返回指定列表支持的同步（线程安全的）列表。               |
| `static <K,V> Map<K,V> `      | `synchronizedMap(Map<K,V> m)`             | 返回由指定映射支持的同步（线程安全的）映射。             |
| `static <T> Set<T> `          | `synchronizedSet(Set<T> s)`               | 返回指定 set 支持的同步（线程安全的）set。               |
| `static <K,V> SortedMap<K,V>` | `synchronizedSortedMap(SortedMap<K,V> m)` | 返回指定有序映射支持的同步（线程安全的）有序映射。       |
| `static <T> SortedSet<T> `    | `synchronizedSortedSet(SortedSet<T> s)`   | 返回指定有序 set 支持的同步（线程安全的）有序 set。      |

### 代码示例

```java
public class CollextionsTest {
    @Test
    public void test(){
        List list = new ArrayList();
        list.add(123);
        list.add(43);
        list.add(765);
        list.add(-98);
        list.add(0);
        System.out.println(list);//[123, 43, 765, -98, 0]
//        排序操作：（均为static方法）
//        reverse(List)：反转 List 中元素的顺序
        Collections.reverse(list);
        System.out.println(list);//[0, -98, 765, 43, 123]
//        shuffle(List)：对 List 集合元素进行随机排序
        Collections.shuffle(list);
        System.out.println(list);//[0, 123, 43, -98, 765] 随机打乱
//        sort(List)：根据元素的自然顺序对指定 List 集合元素按升序排序
        Collections.sort(list);
        System.out.println(list);//[-98, 0, 43, 123, 765]
//        sort(List，Comparator)：根据指定的 Comparator 产生的顺序对 List 集合元素进行排序
        Collections.sort(list, new Comparator() {
            @Override
            public int compare(Object o1, Object o2) {
                if(o1 instanceof Integer && o2 instanceof Integer){
                    Integer in1=(Integer) o1;
                    Integer in2=(Integer) o2;
                    return -Integer.compare(in1,in2);//逆序
                }
                throw  new RuntimeException("数据类型不一致");
            }
        });
        System.out.println(list);//[765, 123, 43, 0, -98]
//        swap(List，int， int)：将指定 list 集合中的 i 处元素和 j 处元素进行交换
        Collections.swap(list,2,3);
        System.out.println(list);//[765, 123, 0, 43, -98]

//        int frequency(Collection，Object)：返回指定集合中指定元素的出现次数
        list.add(765);
        int count=Collections.frequency(list,765);
        System.out.println(count);//2
//        void copy(List dest,List src)：将src中的内容复制到dest中
        //List dest = new ArrayList();
        //Collections.copy(dest,list);//dese.size是0。java.lang.IndexOutOfBoundsException: Source does not fit in dest
        List dest = Arrays.asList(new Object[list.size()]);//技巧！！！：长度为list.size 元素是null的数组
        Collections.copy(dest,list);
        System.out.println(list);//[888, 123, 0, 43, -98, 765] 注意是
//        boolean replaceAll(List list，Object oldVal，Object newVal)：使用新值替换List 对象的所有旧值
        Collections.replaceAll(list,0,1); //将0换成1
        System.out.println(list);//[765, 123, 1, 43, -98, 765]

       //Collections 类中提供了多个 synchronizedXxx() 方法，该方法可使将指定集 合包装成线程同步的集合，从而可以解决多线程并发访问集合时的线程安全问题
        List newList = Collections.synchronizedList(list);
        //new List是线程安全的
    }
}

```

### 面试题

Collection和Collections的区别

### 一些经验

XXX   XXXs  XXXFatory

一般XXXs是XXX的工具类  XXXFatory是工厂用来调用返回一个XXX

## 开发中如何选择集合实现类

在开发中，选择什么集合实现类，主要取决于业务操作特点，然后根据集合实现类特性进行选择，分析如下:
1)先判断存储的类型(一组对象[单列]或一组键值对[双列])
2)一组对象[单列]: Collection接口
  允许重复: List
     增删多: LinkedList [底层维护了一个双向链表]
     改查多: ArrayList [底层维护Object类型的可变数组]
  不允许重复: Set
     无序: HashSet [底层是HashMap，维护了一个哈希表即(数组+链表+红黑树)]
     排序: TreeSet
     插入和取出顺序一致: LinkedHashSet ， 维护数组+双向链表
3)一组键值对[双列]: Map
  键无序: HashMap [底层是:哈希表jdk7: 数组+链表，jdk8: 数组+链表+红黑树]
  键排序: TreeMap 
  键插入和取出顺序一致: LinkedHashMap
  读取文件Properties

| 集合          | 描述                                                 |
| ------------- | ---------------------------------------------------- |
| ArrayList     | 一种可以动态增长和缩减的索引序列                     |
| LinkedList    | 一种可以在任何位置进行高效地插人和删除操作的有序序列 |
| HashSet       | 一种没有重复元素的无序集合                           |
| LinkedHashSet | 一种可以记住元素插人次序的集                         |
| TreeSet       | —种有序集                                            |
| HashMap       | 一种存储键 / 值关联的数据结构                        |
| LinkedHashMap | 一种可以记住键 / 值项添加次序的映射表                |
| TreeMap       | —种键值有序排列的映射表                              |
(表格节选自 java核心技术卷一)

## 一些题

(1)姓氏统计：一个文本文件中存储这所有在校生的姓名，格式如下：每行一个名字，姓与名以空格分隔
```
张 三
李 四
王 小五
```
现在想统计算有姓氏在文件中出现的次数
```java
public void test() throws IOException {
    HashMap<String, Integer> map = new HashMap<>();
    BufferedReader br = null;
        br = new BufferedReader(new FileReader(new File("e:/name.txt")));
                String value = null;//临时接收文件中的字符串变量
        StringBuffer buffer = new StringBuffer();
        flag: while ((value = br.readLine())!= null) { //开始读取文件中的字符
            char[] c = value.toCharArray();
            for (int i= 0;i < c.length; i++) {
                if(c[i]!=' '){
                buffer.append(String. valueOf(c[i]));
            } else {
                if (map.containsKey(buffer.toString())) {
                    int count = map.get(buffer.toString());
                    map.put(buffer.toString(), count + 1);
                } else {
                    map.put(buffer.toString(), 1);
                    buffer.delete(0, buffer.length());
                    continue flag;
                }
                }
            }
                }
}
```

(2)对一个Java源文件中的关键字进行计数

提示：Java源文件中的每一个单词，需要确定该单词是否是一个关键字。为了高效处理这个问题，将所有的关键字保存在一个HashSet中。用contains()来测试。若存在，count++

```java
已知代码：
File file = new File("Test.java");
Scanner scanner = new Scanner(file);
while(scanner.hasNext()){
   String word = scanner.next();
   System.out.println(word);
}
```

## 数据结构简述

1.数据结构概述
数据结构（Data Structure是一门和计算机硬件与软件都密切相关的学科，它的研究重点是在计算机的程序设计领域中探讨如何在计算机中组织和存储数据并进行高效率的运用，涉及的内容包含：数据的逻辑关系、数据的存储结构、排序算法（Algorithm）、查找（或搜索）等。

2.数据结构与算法的理解
程序能否快速而高效地完成预定的任务，取决于是否选对了数据结构，而程序是否能清楚而正确地把问题解决，则取决于算法。

所以大家认为：“Algorithms + Data Structures = Programs”（出自：Pascal之父Nicklaus Wirth）

总结：算法是为了解决实际问题而设计的，数据结构是算法需要处理的问题载体。

3.数据结构的研究对象
3.1 数据间的逻辑结构
    集合结构            
    一对一：线性结构
    一对多：树形结构
    多对多：图形结构

![](http://101.34.218.64/JavaSE.assets/%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84%E7%9A%84%E9%80%BB%E8%BE%91%E7%BB%93%E6%9E%84.png)

3.2 数据的存储结构：
线性表（顺序表、链表、栈、队列）
树
图

说明：习惯上把顺序表和链表看做基本数据结构（或真实数据结构）
      习惯上把栈、队列、树、图看做抽象数据类型，简称ADT


4. 使用详情见思维导图：
《附录：尚硅谷_宋红康_数据结构概述-Java版.xmind》

# 第12章 泛型

 generics

## 为什么要有泛型

### 泛型的引入背景

集合容器类在设计阶段/声明阶段不能确定这个容器到底实际存的是什么类型的对象，所以在JDK1.5之前只能把元素类型设计为Object，JDK1.5之后使用泛型来解决。因为这个时候除了元素的类型不确定，其他的部分是确定的，例如关于这个元素如何保存，如何管理等是确定的，因此此时把元素的类型设计成一个参数，这个类型参数叫做泛型。`Collection<E>`，`List<E>`，`ArrayList<E>`   这个<E>就是类型参数，即泛型。
### 为什么引入


那么为什么要有泛型呢，直接Object不是也可以存储数据吗？
1. 解决元素存储的安全性问题。好比商品、药品标签，不会弄错。
2. 解决获取数据元素时，需要类型强制转换的问题。好比不用每回拿商品、药品都要辨别。

![没有泛型时](http://101.34.218.64/JavaSE.assets/%E6%B2%A1%E6%9C%89%E6%B3%9B%E5%9E%8B%E6%97%B6.png)
list.add(123);也能list.add("Tom");——问题1 **类型不安全**   
 int stuScore = (Integer)score:——问题2 在获取元素后需**强转，繁琐且可能报异常**ClassCastException

![有泛型时](http://101.34.218.64/JavaSE.assets/%E6%9C%89%E6%B3%9B%E5%9E%8B%E6%97%B6.png)
Java泛型可以保证如果程序在编译时没有发出警告，运行时就不会产生ClassCastException异常。同时，代码更加简洁、健壮。
**泛型的好处**：①**编译时就会进行类型检查**，保证数据安全；②**避免了强转**，提高效率，代码简洁。使用泛型的主要优点是能够在编译时而不是在运行时检测错误。

### **泛型的概念**

所谓**泛型**，就是**允许在定义类、接口时通过一个标识表示类中某个属性的类型或者是某个方法的返回值及参数类型**。这个类型参数将在使用时（例如，继承或实现这个接口，用这个类型声明变量、创建对象时确定（即传入实际的类型参数，也称为类型实参）。

从**JDK1.5**以后，Java引入了“**参数化类型**（Parameterized type）”的概念，允许我们**在创建集合时再指定集合元素的类型**，正如：`List<String>`，这表明该List只能保存字符串类型的对象。
JDK1.5改写了集合框架中的全部接口和类，为这些**接口、类增加了泛型支持**，从而可以在声明集合变量、创建集合对象时传入类型实参。

## 集合演示如何使用泛型

### 以ArrayList为例

```java
@Test
public void test1(){
    //在集合中使用泛型:以ArrayList为例
    //public class ArrayList<E>  这个E就是类型参数(准确来说，E是类型变量、类型形参)，即泛型
    //类型变量使用大写形式， 且比较短， 这是很常见的。在 Java 库中， 使用变量 E 表示集合的元素类型， K 和 V 分别表示表的关键字与值的类型。T ( 需要时还可以用临近的 字母 U 和 S) 表示“ 任意类型”。
    ArrayList<Integer> list = new ArrayList<Integer>();//类型参数是Integer.
    // 用具体的类型(类型实参，如Integer)替换类型变量(E)就可以实例化泛型类行。注意：类型实参不能是基本数据类型
    //list.add("Tom");//报错 编译时就会进行类型检查，保证数据安全
    list.add(59);
    list.add(60);
    list.add(61);
    for(Integer score:list){
        //避免了强转
        System.out.print(score);
        if(score>=60) System.out.println("及格");
        else System.out.println("不及格");
    }
    //用迭代器
    Iterator<Integer> iterator = list.iterator();
    //泛型接口 public interface Iterator<E>
    //ArrayList中的方法返回一个泛型的接口实现类对象 public Iterator<E> iterator()
    while(iterator.hasNext()){
        Integer score=iterator.next();//避免了强转
        System.out.print(score);
        if(score>=60) System.out.println("及格");
        else System.out.println("不及格");
    }
}
```

### 以HashMap为例

```java
@Test
public void test2(){
    //在集合中使用泛型:以HashMap为例
    //public class HashMap<K,V>
    //HashMap<String,Integer> map =new HashMap<String,Integer>();
    //JDK7特性：类型推断  构造函数中可以省略泛型类型，省略的类型可以从变量的类型推断得出
    HashMap<String,Integer> map =new HashMap<>();
    map.put("Tom",87);//只能放String的key和Integer的value
    map.put("Jerry",97);
    map.put("Jack",77);

    //public Set<Map.Entry<K,V>> entrySet() 返回值Set<Map.Entry<K,V>>
    // map的内部接口interface Entry<K,V>
    Set<Map.Entry<String,Integer>> entry=map.entrySet();//  Set<Map.Entry<String,Integer>> 泛型嵌套
    //public interface Iterator<E>
    Iterator<Map.Entry<String, Integer>> iterator = entry.iterator();
    while(iterator.hasNext()){
        Map.Entry<String,Integer> e = iterator.next();
        String key=e.getKey();
        Integer value = e.getValue();
        System.out.println(key+"----"+value);
    }
}
```

```java
//如何遍历Map的key集，value集,key-value集，使用上泛型

Map<String,Integer> map = new HashMap<String,Integer>();
map.put();....
//遍历key
Set<String> keySet = map.keySet();
for(String key : keySet){
	System.out.println(key);
}

//遍历value
Collection<Integer> values = map.values();
Iterator<Integer> iterator = values.iterator();
while(iterator.hasNext()){
	System.out.println(iterator.next());
}

//遍历key-value
Set<Map.Entry<String,Integer>> entrySet = map.entrySet();
Iterator<Map.Entry<String,Integer>> iterator =  entrySet.iterator();
while(iterator.hasNext()){
	Map.Entry<String,Integer> entry = iterator.next();
	String key = entry.getKey();
	Integer value = entry.getValue();
	System.out.println(key + "--->" + value);
}
```



### 使用泛型总结：

* ① 集合接口或集合类在**jdk5.0**时都修改为带泛型的结构。

* ② 在实例化集合类时，可以指明具体的泛型类型(类型实参)

*  ③ **指明以后**，在集合类或接口中凡是定义类或接口时，**内部结构**（比如：方法、构造器、属性等）**使用到类的泛型的位置，都指定为实例化的泛型类型**(其子类类型也可以)。
    比如：add(E e)  --->实例化以后：add(Integer e)
    
* ④ 注意点：**泛型的类型必须是引用类型**(类名)，**不能是基本数据类型**。需要用到基本数据类型的位置，拿包装类替换

* ⑤ 如果实例化时，**没指明泛型的类型。默认类型为java.lang.Object**类型。

    `ArrayList list=new ArrayList(); 等价 ArrayList<Object> arrayList = new ArrayList<Object>();`

* ⑥**JDK7新特性：类型推断**。**构造函数中可以省略泛型类型**(**显式类型实参可替换为<>**)，省略的类型可以从变量的类型推断得出。

    ```java
    ArrayList<Integer> list = new ArrayList<Integer>();
    ArrayList<Integer> list = new ArrayList<>();//类型推断
    HashMap<String,Integer> map =new HashMap<String,Integer>();
    HashMap<String,Integer> map =new HashMap<>();//类型推断
    ```

## 泛型的声明和实例化

### 1.泛型的声明

`interface List<T>` 和 `class GenTest<K,V>`
其中，T,K,V不代表值，而是表示类型。这里使用任意字母都可以。常用T表示，是Type的缩写。

>类型变量使用大写形式， 且比较短， 这是很常见的。在 Java 库中， 使用变量 E 表示集合的元素类型， K 和 V 分别表示表的关键字与值的类型。T ( 需要时还可以用临近的 字母 U 和 S) 表示“ 任意类型”。——《java核心技术卷Ⅰ》
>
>T:type E:element K:key V:value

### 2.泛型的实例化：

一定要在类名后面指定类型参数的值（类型）。如：
`List<String> strList = new ArrayList<String>();`
`Iterator<Customer> iterator = customers.iterator();`
 T只能是类，不能用基本数据类型填充。但可以使用包装类填充
 把一个集合中的内容限制为一个特定的数据类型，这就是generics背后的核心思想

## 自定义泛型结构

### 自定义泛型类(重点)

1. 泛型类可能有多个参数，此时应将多个参数一起放在尖括号内。比如：<E1,E2,E3>
2. 泛型类的构造器申明：`public GenericClass(){};`//**声明构造器时不用泛型**
   而下面是错误的：`public GenericClass<E>(){}`
3. 实例化后，操作原来泛型位置的结构必须与指定的泛型类型一致。
4. 泛型不同的引用不能相互赋值。
  > 例如：尽管在编译时`ArrayList<String>`和`ArrayList<Integer>`是两种类型，但是，在运行时只有一个ArrayList被加载到JVM中——“擦除”。
  > ```java
  > ArrayList<String> list1=new ArrayList<>();
  > ArrayList<Integer> list2=new ArrayList<>();
  > System.out.println(list1.getClass()==list2.getClass());//true 都是ArrayList
  > list1=list2;//报错 不兼容的类型
  > ```
  > 泛型类型只有在静态类型检测期间才出现，在此之后，程序中的所有泛型类型都将被擦除，替换为它们的非泛型上界。例如，`List<T>` 这样的类型注解会被擦除为 List，普通的类型变量在未指定边界的情况下会被擦除为 Object.——《On java8》
  > 类型擦除 擦除（ erased) 类型变量, 并替换为限定类型 （无限定的变量用 Object)。——《java核心技术卷Ⅰ》
5. **泛型如果不指定，将被擦除，泛型对应的类型均按照Object处理**，但不等价于Object。经验：泛型要使用一路都用。要不用，一路都不要用。

6. 如果泛型结构是一个接口或抽象类，则不可创建泛型类的对象。

7. jdk1.7，泛型的简化操作：**类型推断** `ArrayList<Fruit> flist = new ArrayList<>();`

8. **泛型的指定中不能使用基本数据类型**，可以使用包装类替换。

9. 在类/接口上声明的泛型，在本类或本接口中即代表某种类型，可以作为非静态属性的类型、非静态方法的参数类型、非静态方法的返回值类型。
   但在**静态方法中不能使用类的泛型**。//静态结构加载时，没有实例化指定泛型
   public static T show(T a){return a;}//报错
   **泛型类中的静态方法不能使用类的泛型，而应该将该方法定义为泛型方法**。变成泛型方法后，泛型类型根据调用时传入的参数类型推断。调用时确定的，不是类实例化时确定的
   
10. 异常类不能是泛型的 
    `public class MyException<T> extends Exception{}`//报错  泛型类不允许扩展Exception或Throwable类
    `try{}catch(T e){}`//报错 catch块不能用泛型参数T
      `class InfoClass<T extends Exception>  {public void add(int t) throws T {this.t = t;}}`//但是在throws中允许
    参考http://www.java265.com/JavaCourse/202205/3593.html
    
    > 由于擦除的原因，catch 语句不能捕获泛型类型的异常，因为在编译期和运行时都必须知道异常的确切类型。泛型类也不能直接或间接继承自 Throwable（这将进一步阻止你去定义不能捕获的泛型异常）。但是，类型参数可能会在一个方法的 throws 子句中用到。这使得你可以编写随检查型异常类型变化的泛型代码.——《On Java8》
    
11. 不能使用new E[]。（泛型类中，**泛型参数类型的数组，不能初始化**。因为数组在 new 不能确定泛型的类型，就无法在内存开空间）
    但是可以：E[] elements = **(E[])new Object[capacity]**;
    参考：ArrayList源码中声明：Object[] elementData，而非泛型参数类型数组。

12. 父类有泛型，子类可以选择保留泛型也可以选择指定泛型类型：
    （1）子类不保留父类的泛型：按需实现
    没有类型 擦除
    具体类型
    （2）子类保留父类的泛型：泛型子类
    全部保留
    部分保留
    子类除了指定或保留父类的泛型，还可以增加自己的泛型.
    代码示例

```java
public class Father<T1,T2> { public void show(T1 t1,T2 t2){}}

// 子类不保留父类的泛型：子类不是泛型类
// 1)没有类型 擦除
class Son1 extends Father {}// 等价于class Son extends Father<Object,Object>
// 2)指明具体类型
class Son2 extends Father<Integer, String> { }

// 子类保留父类的泛型：泛型子类
// 1)全部保留
class Son3<T1, T2> extends Father<T1, T2> { }
// 2)部分保留
class Son4<T2> extends Father<Integer, T2> { }


//子类除了指定或保留父类的泛型，还可以增加自己的泛型
// 子类不保留父类的泛型
// 1)没有类型 擦除
class Son11<A, B> extends Father{}//等价于class Son extends Father<Object,Object>{}
// 2)具体类型
class Son22<A, B> extends Father<Integer, String> { }
// 子类保留父类的泛型
// 1)全部保留
class Son33<T1, T2, A, B> extends Father<T1, T2> { }
// 2)部分保留
class Son44<T2, A, B> extends Father<Integer, T2> { }
```

自定义泛型类

```java
public class Order<T> {
    String orderName;
    int orderId;
    //类的内部就可以使用类的泛型。
    //T类型定义变量
    T orderT;//成员变量orderT的类型是T，T是什么要看实例化时类名后面的类型实参

    public Order(){}
    public Order(String orderName, int orderId, T orderT) {//T类型用于构造器中
        this.orderName = orderName;
        this.orderId = orderId;
        this.orderT = orderT;
    }
    //T类型在一般方法使用： 参数、返回值、方法体内
    public T getOrderT() {
        T temp;
        return orderT;
    }
    public void setOrderT(T orderT) {
        this.orderT = orderT;
    }
}
```



### 自定义泛型接口

`interface 接口名<T>{ }`

注意点见“定义泛型类”

### 自定义泛型方法

格式：
[访问权限] **<泛型>** 返回类型 方法名([泛型标识 参数名称]) 抛出的异常

`public static <T>  T getSum(T a)`

**类型变量列表**(如`<T>`)放在**修饰符的后面**(如果有修饰符的话)，**返回值类型的前面**。——泛型方法的重要特征。（区分使用泛型的普通方法： 参数、返回值、方法体内使用泛型，仅在泛型类中定义。返回值前没有泛型类型）

泛型方法被调用时，泛型类型才被确定。编译器可以**根据传入参数的类型来推断泛型类型**，调用时一般省略<类型>。（编译器根据泛型方法的传入的泛型参数类型推断泛型类型）

泛型方法**可以声明为静态**的。因为泛型类型是调用时确定的，不是类实例化时确定的

泛型方法**可以定义在普通类中，也可以定义在泛型类中**。

泛型方法声明泛型时也可以指定上限。

```java
class ArrayAlg{
  public static <T> T getMiddle(T[] a){
    return a[a.length / 2];
  }
}

使用上限
public static <T extends Person> void test(T t){
    System.out.println(t);
} 
```

### 使用情境

泛型类和泛型方法的使用情境
DAO

```java
【DAO.java】:定义了操作数据库中的表的通用操作。   ORM思想(数据库中的表和Java中的类对应)
 //DAO:data(base) access object 数据访问对象
 //CRUD:create增 retrieve查 update改 delete删
public class DAO<T> {//表的共性操作的DAO
    //添加一条记录
    public void add(T t){ }
    //删除一条记录
    public boolean remove(int index){  return false;}
    //修改一条记录
    public void update(int index,T t){ }
    //查询一条记录
    public T getIndex(int index){ return null; }
    //查询多条记录
    public List<T> getForList(int index){   return null;  }

    //泛型方法
    //举例：获取表中一共有多少条记录？获取最大的员工入职时间？
    public <E> E getValue(){   return null;}
}

【CustomerDAO.java】:操作Customer表
public class CustomerDAO extends DAO<Customer>{//只能操作某一个表的DAO
}

【StudentDAO.java】:操作Student表
public class StudentDAO extends DAO<Student> {//只能操作某一个表的DAO
}
```

## 关于边界

重载后的关键字extends和super可以对类型变量或通配符进行限定（类型变量只有上界，通配符不仅有上界还有下界）
**extends:限定泛型的上限(上边界)** 
`<T extends Father>` T可以是Father类型或其子类(或接口Father的实现类)
`<? extends Father>` ?可以是Father类型或其子类(或接口Father的实现类)
**super:限定泛型的下限(下边界)**——超类型限定 （supertype bound)
`<? super Son>`?可以是Son类型或者其父类(不限于直接父类)

一个类型变量或通配符可以有多个限定。限定类型用“ &” 分隔， 而逗号用来分隔类型变量。
`<T extends A&B,E super C&D>`

## 泛型在继承上的体现

如果B是A的一个子类型（子类或者子接口），而G是具有泛型声明的类或接口，`G<B>`并不是`G<A>`的子类型(二者是并列关系)。
比如：String是Object的子类，但是`List<String>`并不是`List<Object>`的子类。

另一种情况：如果Son是Father的子类，那么`Son<A>`是`Father<A>`的子类。(子父类，两边同一泛型)
`Son<A>`的对象可以赋给`Father<A>`(泛型+多态)

## 通配符的使用
通配符：?

类型变量或通配符的区别https://blog.csdn.net/w903328615/article/details/122365001

### <?>无界通配符、无限定通配符
Unbounded Wildcards
<?>允许所有泛型的引用调用。任意的泛型类型都可以接受

  类A是类B的父类，`G<A>`和`G<B>`是没关系的，二者**共同的父类**是：`G<?>`
  比如：`List<?>` ，`Map<?,?>`
  `List<?>`是`List<String>`、`List<Object>`等各种泛型List的父类。

> 事实上，因为泛型参数擦除到它的第一个边界，因此` List<?>` 看起来等价于`List<Object>` ，而 List 实际上也是 `List<Object>` ——除非这些语句都不为真。`List`实际上表示 “持有任何 Object 类型的原生 List”，而` List<?>` 表示 “具有某种特定类型的非原生 List ，只是我们不知道类型是什么。”——《On java8》

代码示例
```java
  @Test
    public void test5(){
        List<Object> list1 = new ArrayList<>();
        List<String> list2 = new ArrayList<>();

        List<?> list = null;
        list = list1;
        list = list2;
        //编译通过 说明List<?>是List<Object>和List<String>的公共父类

        print(list1);
        print(list2);
    }

    public void print(List<?> list){
        Iterator<?> iterator = list.iterator();//public interface Iterator<E> E是元素类型
        while(iterator.hasNext()){
            Object obj = iterator.next();//用Object接收
            System.out.println(obj);
        }
    }
```

### 涉及通配符的集合的数据的写入和读取

* **写入**list中的元素时，编译报错。因为我们不知道c的元素类型，我们不能向其中添加对象。**唯一的例外是null，它是所有类型的成员**。
  将任意元素加入到其中**不是类型安全的**。唯一的例外的是null，它是所有类型的成员。
```java
  Collection<?> c = new ArrayList<String>();
  c.add(new Object()); // 编译时错误
```

  因为我们不知道c的元素类型，我们不能向其中添加对象。add方法有类型参数E作为集合的元素类型。我们传给add的任何参数都必须是一个未知类型的子类。因为我们不知道那是什么类型，所以我们无法传任何东西进去。
* **读取**`List<?>`的对象list中的元素时，永远是安全的，因为不管list的真实类型是什么，它包含的都是Object。
  我们可以调用get()方法并使用其返回值。返回值是一个**未知的类型，但是我们知道，它总是一个Object**。

```java
  @Test
    public void test6(){
        List<?> list = null;
        List<String> list3 = new ArrayList<>();
        list3.add("AA");
        list3.add("BB");
        list3.add("CC");
        list = list3;
        //添加(写入)：对于List<?>就不能向其内部添加数据。
        //除了添加null之外。
//        list.add("DD");//报错 类型不匹配
//        list.add('?');//报错

        list.add(null);//允许  可以是null

        //获取(读取)：允许读取数据，读取的数据类型为Object。
        Object o = list.get(0);
        System.out.println(o);
    }
```

### 通配符的使用：注意点
通配符只能用于引用参数中（变量引用、形参）。
通配符不允许出现在泛型定义中（泛型类、泛型接口、泛型方法的`< >`里）
泛型方法的显式类型说明也不可以使用通配符。
> 但是可以用在泛型类或泛型方法的{ }里还有泛型方法的形参上，配合占位符，甚至可以使用? extends T或者? super T这种形式来用作引用。

在new泛型类的时候也不可以使用通配符，比如new ArrayList<?>()。
```JAVA
//注意点：编译错误：不能用在泛型方法声明上，返回值类型前面<>不能使用?
//泛型方法的显式类型说明也不可以使用通配符。test(ArrayList<?> list)
public static <?> void test(ArrayList<?> list){  }
//注意点：编译错误：不能用在泛型类的声明上
class GenericTypeClass<?>{ }

//注意点：编译错误：不能用在创建对象上，右边属于创建集合对象
ArrayList<?> list2 = new ArrayList<?>();
```

### 有限制条件的通配符的使用
举例：
`<? extends Number>`(无穷小 , Number]只允许泛型为Number及Number子类的引用调用
`<? super Number>` [Number , 无穷大)只允许泛型为Number及Number父类的引用调用
`<? extends Comparable>`只允许泛型为实现Comparable接口的实现类的引用调用

`G<? extends A> `可以作为`G<A>`和`G<B>`的父类，其中B是A的子类（？可以是A及其子类）
`G<? super A>` 可以作为`G<A>`和`G<B>`的父类，其中B是A的父类（？可以是A及其父类 不仅是直接父类）

```java
public static void printCollection3(Collection<? extends Person> coll) {
//Iterator只能用Iterator<?>或Iterator<? extends Person>.why?
	Iterator<?> iterator = coll.iterator();
	while (iterator.hasNext()) {
		System.out.println(iterator.next());
	}
}
public static void printCollection4(Collection<? super Person> coll) {
//Iterator只能用Iterator<?>或Iterator<? super Person>.why?
	Iterator<?> iterator = coll.iterator();
	while (iterator.hasNext()) {
		System.out.println(iterator.next());
	}
}
```

思考：为什么如下操作会报错

![体会泛型中通配符的使用](http://101.34.218.64/JavaSE.assets/%E4%BD%93%E4%BC%9A%E6%B3%9B%E5%9E%8B%E4%B8%AD%E9%80%9A%E9%85%8D%E7%AC%A6%E7%9A%84%E4%BD%BF%E7%94%A8.png)

## 泛型应用举例

(1)泛型嵌套

```java
 public static void main(String[] args) {
        HashMap<String, ArrayList<Citizen>> map = new HashMap<String, ArrayList<Citizen>>();
        ArrayList<Citizen> list = new ArrayList<Citizen>();
        list.add(new Citizen("刘恺威"));
        list.add(new Citizen("杨幂"));
        list.add(new Citizen("小糯米"));
        map.put("刘恺威", list);
        Set<Entry<String, ArrayList<Citizen>>> entrySet = map.entrySet();
        Iterator<Entry<String, ArrayList<Citizen>>> iterator = entrySet.iterator();
        while (iterator.hasNext()) {
            Entry<String, ArrayList<Citizen>> entry = iterator.next();
            String key = entry.getKey();
            ArrayList<Citizen> value = entry.getValue();
            System.out.println("户主：" + key);
            System.out.println("家庭成员：" + value);
        }
    }
```



(2)用户在设计类的时候往往会使用类的关联关系，例如，一个人中可以定义一个信息的属性，但是一个人可能有各种各样的信息（如联系方式、基本信息等），所以此信息属性的类型就可以通过泛型进行声明，然后只要设计相应的信息类即可

```java
interface Info{		// 只有此接口的子类才是表示人的信息
}
class Contact implements Info{	// 表示联系方式
	private String address ;	// 联系地址
	private String telephone ;	// 联系方式
	private String zipcode ;	// 邮政编码
	public Contact(String address,String telephone,String zipcode){
		this.address = address;
		this.telephone = telephone;
		this.zipcode = zipcode;
	}
	public void setAddress(String address){
		this.address = address ;
	}
	public void setTelephone(String telephone){
		this.telephone = telephone ;
	}
	public void setZipcode(String zipcode){
		this.zipcode = zipcode;
	}
	public String getAddress(){
		return this.address ;
	}
	public String getTelephone(){
		return this.telephone ;
	}
	public String getZipcode(){
		return this.zipcode;
	}
	@Override
	public String toString() {
		return "Contact [address=" + address + ", telephone=" + telephone
				+ ", zipcode=" + zipcode + "]";
	}
}
class Introduction implements Info{//基本信息
	private String name ;		// 姓名
	private String sex ;		// 性别
	private int age ;			// 年龄
	public Introduction(String name,String sex,int age){
		this.name = name;
		this.sex = sex;
		this.age = age;
	}
	public void setName(String name){
		this.name = name ;
	}
	public void setSex(String sex){
		this.sex = sex ;
	}
	public void setAge(int age){
		this.age = age ;
	}
	public String getName(){
		return this.name ;
	}
	public String getSex(){
		return this.sex ;
	}
	public int getAge(){
		return this.age ;
	}
	@Override
	public String toString() {
		return "Introduction [name=" + name + ", sex=" + sex + ", age=" + age
				+ "]";
	}
}
class Person<T extends Info>{
	private T info ;
	public Person(T info){		// 通过构造器设置信息属性内容
		this.info = info;
	}
	public void setInfo(T info){
		this.info = info ;
	}
	public T getInfo(){
		return info ;
	}
	@Override
	public String toString() {
		return "Person [info=" + info + "]";
	}
	
}
public class GenericPerson{
	public static void main(String args[]){
		Person<Contact> per = null ;		// 声明Person对象
		per = new Person<Contact>(new Contact("北京市","01088888888","102206")) ;
		System.out.println(per);
		
		Person<Introduction> per2 = null ;		// 声明Person对象
		per2 = new Person<Introduction>(new Introduction("李雷","男",24));
		System.out.println(per2) ;
	}
}
```

## 一个练习

```java
/定义个泛型类 `DAO<T>`，在其中定义一个 Map 成员变量，Map 的键 为 String 类型，值为 T 类型。
public class DAO<T> {//表的共性操作的DAO
    private Map<String,T> map;
    public DAO() {
        this.map = new HashMap<>();//初始化map 不然NullPointerException
    }

    //public void save(String id,T entity)： 保存 T 类型的对象到 Map 成员 变量中
    public void save(String id,T entity){
        map.put(id,entity);
    }
    //public T get(String id)：从 map 中获取 id 对应的对象
    public T get(String id){
        return map.get(id);
    }
    //public void update(String id,T entity)：替换 map 中 key 为 id 的内容,改为 entity 对象
    public void update(String id,T entity){
        //map.put(id,entity);//弊端 如果没有key为id的元素 则直接添加 不是更改
        //改进 如果有id这个key
        if (map.get(id) != null || map.containsKey(id)) {//有不是null的value 则一定有key；如果value是null再看看是不是有key 。短路 快
            map.put(id,entity);
        }
        //map.replace(id,entity);//JDK1.8版直接使用replace方法
    }
    //public List<T> list()：返回 map 中存放的所有 T 对象
    public List<T> list(){
         Collection<T> values = map.values();//values()返回的是Collection
//        return (List<T>) values;//虽然不报错，但是错了。values是无序的  list是有序的，不能强转成List。
//        // values instanceof List<T>是false的。不属于子类对象->父类引用->强转为子类类型
        //正确的
        ArrayList<T> list = new ArrayList<>();
        //方式1
        for(T t:values){
            list.add(t);
        }
        //方式2
        //list.addAll(values);
        return list;
    }
    //public void delete(String id)：删除指定 id 对象
    public void delete(String id){
        map.remove(id);
    }
}
```

```java
//定义一个 User 类：
//该类包含：private 成员变量（int 类型） id，age；（String 类型）name。
public class User {
    private int id,age;
    private String name;
    public User() {}
    public User(int id, int age, String name) {
        this.id = id;
        this.age = age;
        this.name = name;
    }
//getter setter toString...
    @Override
    public boolean equals(Object o) {//T是User 故map的value是User类型 value是Collection 需要重写equals
        if (this == o) return true;
        if (o == null || getClass() != o.getClass()) return false;
        User usr = (User) o;
        if (id != usr.id) return false;
        if (age != usr.age) return false;
        return name != null ? name.equals(usr.name) : usr.name == null;
    }
}
```

```java
//定义一个测试类：
//创建 DAO 类的对象， 分别调用其 save、get、update、list、delete 方法来操作 User 对象，
//使用 Junit 单元测试类进行测试
public class DAOTest {
    @Test
    public void test1(){
        DAO<User> dao = new DAO<>();
        dao.save("1001",new User(01,18,"小明"));
        dao.save("1002",new User(02,17,"小红"));
        dao.save("1003",new User(03,10,"小光"));
        dao.update("1003",new User(04,23,"李华"));
        dao.delete("1002");
        List<User> list = dao.list();
        //System.out.println(list);
        list.forEach(System.out::println);
    }
}
```

## ==使用上泛型如何遍历Map==的key集，value集,key-value集

```java
Map<String,Integer> map = new HashMap<String,Integer>();
map.put();....
//遍历key
Set<String> keySet = map.keySet();
for(String key : keySet){
	System.out.println(key);
}

//遍历value
Collection<Integer> values = map.values();
Iterator<Integer> iterator = values.iterator();
while(iterator.hasNext()){
	System.out.println(iterator.next());
}

//遍历key-value
Set<Map.Entry<String,Integer>> entrySet = map.entrySet();
Iterator<Map.Entry<String,Integer>> iterator =  entrySet.iterator();
while(iterator.hasNext()){
	Map.Entry<String,Integer> entry = iterator.next();
	String key = entry.getKey();
	Integer value = entry.getValue();
	System.out.println(key + "--->" + value);
}
```



# 第13章 IO流

## File类

### File类介绍
* java.io.File类：**文件和文件目录路径**的抽象表示形式，与平台无关
* File 能新建、删除、重命名文件和目录,修改时间、文件大小等，但 **File 不能访问文件内容本身**。
  如果**需要访问文件内容本身，则需要使用输入/输出流**。
* 想要在Java程序中表示一个真实存在的文件或目录，那么必须有一个File对象，但是Java程序中的一个File对象，可能没有一个真实存在的文件或目录。
* File对象**可以作为参数传递给流的构造器**，指明读取或写入的”终点“
* File 类的实例是不可变的.

### 常用构造器

* public File(String pathname)
  以pathname为路径创建File对象，可以是绝对路径或者相对路径，如果pathname是相对路径，则默认的当前路径在系统属性user.dir中存储。
   绝对路径：是一个固定的路径,从盘符开始
   相对路径：是相对于某个位置开始
  
  > 说明：
  > IDEA中：
  > 如果大家开发使用JUnit中的单元测试方法测试，相对路径即为当前Module下。
  > 如果大家使用main()测试，相对路径即为当前的Project下。
  >
  > Eclipse中：不管使用单元测试方法还是使用main()测试，相对路径都是当前的Project下
  
* public File(String parent,String child)
  以parent为父路径，child为子路径创建File对象。
  
* public File(File parent,String child)
  根据一个父File对象和子文件路径创建File对象
  
* 不怎么用的 File(URI uri) 通过将给定的 file: URI 转换为一个抽象路径名来创建一个新的 File 实例。

```java
  @Test
    public void test1(){
        //构造器使用
        //注意 file可以是文件也可以是目录
        //public File(String pathname)
        File file = new File("hello.txt");//相对路径
        File filedir = new File("D:\\IdeaProjects");//一个目录
        File file1 = new File("D:\\IdeaProjects\\project_javase\\Module20220731_IO\\hello.txt");//绝对路径

        System.out.println(file);//hello.txt 输出路径，即使这个文件不存在
        System.out.println(new File(""));//"" 输出路径，即使路径为空

        //public File(String parent,String child)
        File file2 = new File("D:\\IdeaProjects\\project_javase","Module20220731_IO");

        //public File(File parent,String child)
        File file3 = new File(file2,"haha.txt");
    }
```

### 路径分隔符
路径中的每级目录之间用一个路径分隔符隔开。

路径分隔符和系统有关：
windows和DOS系统默认使用“\”来表示。
UNIX和URL使用“/”来表示。（masOS基于UNIX）

（新发现 好像在win下也可以用/分割路径，/为根时，是项目所在硬盘/相当于D:\\）

java支持跨平台运行，为了解决这个隐患，File类提供了一个常量
public static final String separator。根据操作系统，动态的提供分隔符

File file1 = new File("d:\\atguigu\\info.txt");//windows和DOS系统
File file3 = new File("d:/atguigu");//UNIX和URL
File file2 = new File("d:" + File.separator + "atguigu" + File.separator + "info.txt");//使用separator

### 常用方法（==常用==）

#### (1) File类的获取功能

* public String **getAbsolutePath**()：获取绝对路径
* public String getPath() ：获取路径
* public String getName() ：获取名称
* public String **getParent**()：获取上层文件目录路径。若无，返回null
* public long length() ：获取文件长度(即文件大小)（即：字节数Byte）。不能获取目录的长度。
* public long lastModified() ：获取最后一次的修改时间，毫秒值

下面的两个方法只适用于文件目录
* public String[] list() ：获取指定目录下的所有文件或者文件目录的名称数组
* public File[] listFiles() ：获取指定目录下的所有文件或者文件目录的File数组

不存在的文件的输出：除了路径(AbsolutePath和Path)和name，其它都是默认的
![File内存分析.png](http://101.34.218.64/JavaSE.assets/File%E5%86%85%E5%AD%98%E5%88%86%E6%9E%90.png)


```java
    @Test
    public void testFileGet(){
        //(1) File类的获取功能
        File file = new File("hello.txt");
        //file= new File("不存在的文件.txt");
        System.out.println("绝对路径:"+file.getAbsolutePath());
        System.out.println("路径:" + file.getPath());
        System.out.println("名称:" + file.getName());
        System.out.println("上层文件路径:" + file.getParent());//若无上层路径，返回null
        System.out.println("文件长度:" + file.length() + "字节");//返回long型 单位是字节Byte
        System.out.println("最后一次的修改时间:" + new Date(file.lastModified()));//lastModified()获取的是时间戳(long型)
                /*输出：
绝对路径:D:\IdeaProjects\project_javase\Module20220731_IO\hello.txt
路径:hello.txt
名称:hello.txt
上层文件路径:null
文件长度:5字节
最后一次的修改时间:Sun Jul 31 09:22:38 CST 2022

不存在的文件的输出：除了路径(AbsolutePath和Path)和name，其它都是默认的
绝对路径:D:\IdeaProjects\project_javase\Module20220731_IO\不存在的文件.txt
路径:不存在的文件.txt
名称:不存在的文件.txt
上层文件路径:null
文件长度:0字节
最后一次的修改时间:Thu Jan 01 08:00:00 CST 1970
                 */

        File file1=new File("d:\\ideaProjects\\project_javase");
        //public String[] list() ：获取指定目录下的所有文件或者文件目录的名称数组
        System.out.println("-----list()-------");
        String[] names=file1.list();
        for(String name:names){
            System.out.println(name);
        }
        //public File[] listFiles() ：获取指定目录下的所有文件或者文件目录的File数组
        System.out.println("--------listFiles()--------");
        File[] files = file1.listFiles();
        for (File eachFile:files) {
            System.out.println(eachFile);//输出的是每个File的路径名
        }
    }
```



#### (2) File类的重命名功能

* public boolean renameTo(File dest):把文件重命名为指定的文件路径

```java
        File file1=new File("hello.txt");
        File file2=new File("hi.txt");
        file1.renameTo(file2);//注意 参数是一个File
        //要保证返回true，需要在硬盘中，file1存在，且file2不存在
        System.out.println(file1);//hello.txt
```

#### (3) File类的判断功能

* public boolean **isDirectory**()：判断是否是文件目录
* public boolean **isFile**() ：判断是否是文件
* public boolean **exists**() ：判断是否存在
* public boolean canRead() ：判断是否可读
* public boolean canWrite() ：判断是否可写
* public boolean isHidden() ：判断是否隐藏

```java
    @Test
    public void testTest(){
     //File类的判断功能
        File file = new File("hi.txt");
        System.out.println("判断是否是文件目录:" + file.isDirectory());
        System.out.println("判断是否是文件:" + file.isFile());
        System.out.println("判断是否存在:" + file.exists());//一般先判断存在
        System.out.println("判断是否可读:" + file.canRead());
        System.out.println("判断是否可写:" + file.canWrite());
        System.out.println("判断是否隐藏:" + file.isHidden());
    }
    //输出：(注意，如果file是不存在的文件，则都是false)
    //判断是否是文件目录:false
    //判断是否是文件:true
    //判断是否存在:true
    //判断是否可读:true
    //判断是否可写:true
    //判断是否隐藏:false
```



#### (4) File类的创建功能

注意事项：如果你创建文件或者文件目录没有写盘符路径，那么，默认在项目路径下。

* public boolean **createNewFile**() ：创建文件。若文件存在，则不创建，返回false.(目录不存在等，会抛IO异常)
* public boolean mkdir() ：创建文件目录。如果此文件目录存在，就不创建了。如果此文件目录的上层目录不存在，也不创建。
* public boolean **mkdirs**() ：创建文件目录。如果上层文件目录不存在，一并创建。

#### (5) File类的删除功能

* public boolean **delete**()：删除文件或者文件夹
删除注意事项：
①Java中的删除**不走回收站**。
②**要删除一个文件目录**，请注意该文件目录**内不能包含文件或者文件目录**

```java
   @Test
    public void testCreate() {
        //File类的创建功能
        // 注意事项：如果你创建文件或者文件目录使用相对路径，在项目路径下（idea是在module下）开始
        //文件的创建
        //* public boolean createNewFile() ：创建文件。若文件存在，则不创建，返回false。目录不存在会抛IO异常
        File file = new File("newfile1.txt");
        //file = new File("newfile1.txt");//D:\IdeaProjects\project_javase\Module20220731_IO\newfile1.txt  在项目路径下
        if (!file.exists()) {
            try {
                file.createNewFile();
                System.out.println("创建成功");
            } catch (IOException e) {
                e.printStackTrace();
            }
        } else {
            file.delete();
            System.out.println("删除成功");
        }

        //文件目录的创建
        //* public boolean mkdir() ：创建文件目录。如果此文件目录存在，就不创建了。如果此文件目录的上层目录不存在，也不创建。
        //* public boolean mkdirs() ：创建文件目录。如果上层文件目录不存在，一并创建。
        File dir1 = new File("io/io1");
        boolean isMkdir=dir1.mkdir();
        System.out.println(isMkdir);

        File dir2 = new File("io/io2");
        boolean isMkdirs=dir2.mkdirs();
        System.out.println(isMkdirs);

        File dir = new File("io");
        boolean isDeleteDir= dir.delete();
        System.out.println(isDeleteDir);//false 因为包含文件夹io1 io2故io不能被删除
        deleteDir(dir);//自己写的递归方法

    }
    public static void deleteDir(File dir){
        File[] files=dir.listFiles();
        for(File f:files){//目录中的文件或文件夹
            if(f.isDirectory()){//是文件夹的话再递归
                deleteDir(f);
            }else{//文件的话直接删
                f.delete();
            }
        }
        dir.delete();
    }
```

```java
        File dir1 = new File("D:/IOTest/dir1");
        if (!dir1.exists()) { // 如果D:/IOTest/dir1不存在，就创建为目录
            dir1.mkdir();
        }
// 创建以dir1为父目录,名为"dir2"的File对象
        File dir2 = new File(dir1, "dir2");
        if (!dir2.exists()) { // 如果还不存在，就创建为目录
            dir2.mkdirs();
        }
        File dir4 = new File(dir1, "dir3/dir4");
        if (!dir4.exists()) {
            dir4.mkdirs();
        }
// 创建以dir2为父目录,名为"test.txt"的File对象
        File file = new File(dir2, "test.txt");
        if (!file.exists()) { // 如果还不存在，就创建为文件
            file.createNewFile();
        }
```

### 一些练习

1. 利用File构造器，new 一个文件目录file
    1)在其中创建多个文件和目录
    2)编写方法，实现删除file中指定文件的操作

2. 判断指定目录下是否有后缀名为.jpg的文件，如果有，就输出该文件名称

   ```java
       @Test
       public void exer2() {
           File dir = new File("D:\\");
           String[] list = dir.list();
           for (String s : list) {
               if (s.endsWith(".jpg")) System.out.println(s);
           }
       }
   ```
```java
public class FindJPGFileTest {
//老师写的
	@Test
	public void test1(){
		File srcFile = new File("d:\\code");
		
		String[] fileNames = srcFile.list();
		for(String fileName : fileNames){
			if(fileName.endsWith(".jpg")){
				System.out.println(fileName);
			}
		}
	}
	@Test
	public void test2(){
		File srcFile = new File("d:\\code");
		
		File[] listFiles = srcFile.listFiles();
		for(File file : listFiles){
			if(file.getName().endsWith(".jpg")){
				System.out.println(file.getAbsolutePath());
			}
		}
	}
	/*
	 * File类提供了文件过滤器方法
	 * public String[] list(FilenameFilter filter)
	 * public File[] listFiles(FileFilter filter)
	 * public File[] listFiles(FilenameFilter filter) 
	 */
	@Test
	public void test3(){
		File srcFile = new File("d:\\code");
		File[] subFiles = srcFile.listFiles(new FilenameFilter() {
			@Override
			public boolean accept(File dir, String name) {
				return name.endsWith(".jpg");
			}
		});
        
		for(File file : subFiles){
			System.out.println(file.getAbsolutePath());
		}
	}
	
}
```

3. 遍历指定目录所有文件名称，包括子文件目录中的文件。
    拓展1：并计算指定目录占用空间的大小
    拓展2：删除指定文件目录及其下的所有文件

  ```java
  import java.io.File;
  
  public class ListFilesTest {
  
  	public static void main(String[] args) {
  		// 递归:文件目录
  		/** 打印出指定目录所有文件名称，包括子文件目录中的文件 */
  
  		// 1.创建目录对象
  		File dir = new File("E:\\teach\\01_javaSE\\_尚硅谷Java编程语言\\3_软件");
  
  		// 2.打印目录的子文件
  		printSubFile(dir);
  	}
  
  	public static void printSubFile(File dir) {
  		// 打印目录的子文件
  		File[] subfiles = dir.listFiles();
  
  		for (File f : subfiles) {
  			if (f.isDirectory()) {// 文件目录
  				printSubFile(f);
  			} else {// 文件
  				System.out.println(f.getAbsolutePath());
  			}
  
  		}
  	}
  
  	// 方式二：循环实现
  	// 列出file目录的下级内容，仅列出一级的话
  	// 使用File类的String[] list()比较简单
  	public void listSubFiles(File file) {
  		if (file.isDirectory()) {
  			String[] all = file.list();
  			for (String s : all) {
  				System.out.println(s);
  			}
  		} else {
  			System.out.println(file + "是文件！");
  		}
  	}
  
  	// 列出file目录的下级，如果它的下级还是目录，接着列出下级的下级，依次类推
  	// 建议使用File类的File[] listFiles()
  	public void listAllSubFiles(File file) {
  		if (file.isFile()) {
  			System.out.println(file);
  		} else {
  			File[] all = file.listFiles();
  			// 如果all[i]是文件，直接打印
  			// 如果all[i]是目录，接着再获取它的下一级
  			for (File f : all) {
  				listAllSubFiles(f);// 递归调用：自己调用自己就叫递归
  			}
  		}
  	}
  
  	// 拓展1：求指定目录所在空间的大小
  	// 求任意一个目录的总大小
  	public long getDirectorySize(File file) {
  		// file是文件，那么直接返回file.length()
  		// file是目录，把它的下一级的所有大小加起来就是它的总大小
  		long size = 0;
  		if (file.isFile()) {
  			size += file.length();
  		} else {
  			File[] all = file.listFiles();// 获取file的下一级
  			// 累加all[i]的大小
  			for (File f : all) {
  				size += getDirectorySize(f);// f的大小;
  			}
  		}
  		return size;
  	}
  
  	// 拓展2：删除指定的目录
  	public void deleteDirectory(File file) {
  		// 如果file是文件，直接delete
  		// 如果file是目录，先把它的下一级干掉，然后删除自己
  		if (file.isDirectory()) {
  			File[] all = file.listFiles();
  			// 循环删除的是file的下一级
  			for (File f : all) {// f代表file的每一个下级
  				deleteDirectory(f);
  			}
  		}
  		// 删除自己
  		file.delete();
  	}
  }
  ```

  

## IO流原理及流的分类

### Java IO原理
* I/O是Input/Output的缩写， I/O技术是非常实用的技术，用于处理设备之间的数据传输。如读/写文件，网络通讯等。
  > 输入input：读取外部数据（磁盘、光盘等存储设备的数据）到程序（内存）中。
  > 输出output：将程序（内存）数据输出到磁盘、光盘等存储设备中。
  > 站位是相对的，程序员站在程序的角度(内存的角度)
* Java程序中，对于数据的输入/输出操作以“**流(stream)**” 的方式进行。
* java.io包下提供了各种“流”类和接口，用以获取不同种类的数据，并通过标准的方法输入或输出数据


### 流的分类
* 按**操作数据单位：字节流(8 bit,Byte)，字符流(16 bit,char)**
* 按**数据流的流向：输入流，输出流**
* 按**流的角色：节点流，处理流(处理流又叫过滤流、包装流)**

表格 四个抽象基类(==**记好**==)

| (抽象基类) | 字节流       | 字符流 |
| ---------- | ------------ | ------ |
| 输入流     | InputStream  | Reader |
| 输出流     | OutputStream | Writer |
Java的IO流共涉及40多个类，实际上非常规则，**都是从以上这4个抽象基类派生**的.
由这四个类派生出来的子类名称都是**以其父类名作为子类名后缀(小技巧)**
表格：IO流体系 (蓝色的流需要重点关注，尤其是访问文件的四个——”文件流“)
![IO流体系.png](http://101.34.218.64/JavaSE.assets/IO%E6%B5%81%E4%BD%93%E7%B3%BB.png)

#### (1)节点流和处理流
* 节点流：**直接从数据源或目的地读写数据**。
  ![节点流](http://101.34.218.64/JavaSE.assets/%E8%8A%82%E7%82%B9%E6%B5%81.png)

* 处理流：又叫过滤流，包装流。**不直接连接到数据源或目的地**，而是**“连接”在已存在的流**（节点流或处理流）之上，通过对数据的处理为程序提供更为强大的读写功能。
  ![处理流](http://101.34.218.64/JavaSE.assets/%E5%A4%84%E7%90%86%E6%B5%81.png)

处理流对节点流进行包装，使用了修饰器模式(或叫装饰器模式)。关闭处理流时，只需要关闭外层流。

#### (2)输入流 基类InputStream、Reader

* InputStream 和 Reader 是所有输入流的基类。
* InputStream（典型实现：FileInputStream）
    int read()
    **int read(byte[] b)**
    int read(byte[] b, int off, int len)
* Reader（典型实现：FileReader）
    int read()
    **int read(char [] c)**
    int read(char [] c, int off, int len)
* 程序中打开的文件 **IO 资源不属于内存里的资源，垃圾回收机制无法回收该资源**，所以应该**显式关闭文件 IO 资源**。
* FileInputStream 从文件系统中的某个文件中获得输入字节。FileInputStream用于读取非文本数据之类的原始字节流。要读取字符流，需要使用 FileReader

常见方法：

InputStream
* int read() 从输入流中读取数据的下一个字节。返回 0 到 255 范围内的 int 字节值。如果因为已经到达流末尾而没有可用的字节，则返回值 -1。
* **int read(byte[] b)** 从此输入流中将最多 b.length 个字节的数据读入一个 byte 数组中。如果因为已经到达流末尾而没有可用的字节，则返回值 -1。否则**以整数形式返回实际读取的字节数**。
* int read(byte[] b, int off,int len) 将输入流中最多 len 个数据字节读入 byte 数组。尝试读取 len 个字节，但读取的字节也可能小于该值。以整数形式返回实际读取的字节数。如果因为流位于文件末尾而没有可用的字节，则返回值 -1。
* public void close() throws IOException 关闭此输入流并释放与该流关联的所有系统资源。

Reader
* int read() 读取单个字符。作为整数读取的字符，范围在 0 到 65535 之间 (0x00-0xffff)（2个字节的Unicode码），如果已到达流的末尾，则返回 -1
* **int read(char[] cbuf)** 将字符读入数组。如果已到达流的末尾，则返回 -1。否则**返回本次读取的字符数**。
* int read(char[] cbuf,int off,int len) 将字符读入数组的某一部分。存到数组cbuf中，从off处开始存储，最多读len个字符。如果已到达流的末尾，则返回 -1。否则返回本次读取的字符数。
* public void close() throws IOException 关闭此输入流并释放与该流关联的所有系统资源。

#### (3)输出流 基类OutputStream、Writer

* OutputStream 和 Writer 也非常相似：
    void write(int b/int c);
    void write(byte[] b/char[] cbuf);
    void write(byte[] b/char[] buff, int off, int len);
    void flush();
    void close(); 需要先刷新，再关闭此流
* 因为字符流直接以字符作为操作单位，所以 **Writer 可以用字符串来替换字符数组**，即以 String 对象作为参数
    void write(String str);
    void write(String str, int off, int len);
* FileOutputStream 从文件系统中的某个文件中获得输出字节。FileOutputStream用于写出非文本数据之类的原始字节流。要写出字符流，需要使用 FileWriter

常见方法：

OutputStream
* void write(int b) 将指定的字节写入此输出流。write 的常规协定是：向输出流写入一个字节。要写入的字节是参数 b 的八个低位。b 的 24 个高位将被忽略。 即写入0~255范围的。
* void write(byte[] b) 将 b.length 个字节从指定的 byte 数组写入此输出流。write(b) 的常规协定是：应该与调用 write(b, 0, b.length) 的效果完全相同。
* void write(byte[] b,int off,int len) 将指定 byte 数组中从偏移量 off 开始的 len 个字节写入此输出流。
* public void flush()throws IOException 刷新此输出流并强制写出所有缓冲的输出字节，调用此方法指示应将这些字节立即写入它们预期的目标。
* public void close() throws IOException  关闭此输出流并释放与该流关联的所有系统资源。

Writer
* void write(int c)写入单个字符。要写入的字符包含在给定整数值的 16 个低位中，16 高位被忽略。 即写入0 到 65535 之间的Unicode码。
* void write(char[] cbuf) 写入字符数组。
* void write(char[] cbuf,int off,int len) 写入字符数组的某一部分。从off开始，写入len个字符
* void write(String str) 写入字符串。
* void write(String str,int off,int len) 写入字符串的某一部分。
* void flush() 刷新该流的缓冲，则立即将它们写入预期目标。
* public void close() throws IOException关闭此输出流并释放与该流关联的所有系统资源。

#### 输入、输出的标准化过程(==熟悉==)

输入过程
   ① 创建File类的对象，指明读取的数据的来源。（要求此文件一定要存在）
   ② 创建相应的输入流，将File类的对象作为参数，传入流的构造器中
   ③ 具体的读入过程：创建相应的byte[] 或 char[]。
   ④ 关闭流资源
   说明：程序中出现的异常需要使用try-catch-finally处理。

输出过程
   ① 创建File类的对象，指明写出的数据的位置。（不要求此文件一定要存在）
   ② 创建相应的输出流，将File类的对象作为参数，传入流的构造器中
   ③ 具体的写出过程：write(char[]/byte[] buffer,0,len)
   ④ 关闭流资源
   说明：程序中出现的异常需要使用try-catch-finally处理

重点学习

![典型的节点流和处理流.jpg](http://101.34.218.64/JavaSE.assets/%E5%85%B8%E5%9E%8B%E7%9A%84%E8%8A%82%E7%82%B9%E6%B5%81%E5%92%8C%E5%A4%84%E7%90%86%E6%B5%81.png)



## 文件流——典型的节点流

文件流：FileReader/FileWriter，FileInputStream/FileOutputStream
FileReader/FileWriter属于字符流，FileInputStream/FileOutputStream属于字节流

### 注意点

* **读取时，文件一定要存在，否则就会报异常**FileNotFoundException

* 注意两个read的返回值
  read()的理解：返回读入的**一个字符**。如果达到文件末尾，返回-1
  read(char[] cbuf):返回每次读入cbuf数组中的字符的**个数**。如果达到文件末尾，返回-1
  
* **输出时，文件可以不存在，不会报异常**。
  File对应的硬盘中的文件如果**不存在**，在输出的过程中，会**自动创建**此文件。
  File对应的硬盘中的文件如果存在(同目录下的同名文件)：
      ①如果流使用的构造器是：FileWriter(file,**false**) / FileWriter(**file**):对原文件内容**覆盖**
      ②如果流使用的构造器是：FileWriter(file,**true**):不会对原文件覆盖，而是在原文件内容末尾**追加**内容(true，则将字节写入文件末尾处，而不是写入文件开始处)
  
* 根据文件类型选择字符流还是字节流
  字符流操作字符，对于**文本文件**(常见的如.txt，.java，.c，.cpp 等语言的源代码)，使用**字符流**处理
  字节流操作字节，对于**非文本文件**(如.jpg,.mp3，.avi，.rmvb，mp4，**.doc，.excel,.ppt**,...)，使用**字节流**处理。(尤其注意.**doc,excel,ppt这些不是文本文件**)
  
  > 如果用处理字节流的FileInputStream处理字符流，控制台输出时，英文字母可以，中文会乱码(复制文件就不会)
  >
  > UTF-8里一个字母是ASCII用的是1个字节 汉字是3个字节(GBK每个汉字两个字节,UTF-8每个汉字三个字节),如果定义的byte数组长度不能刚好读到每个汉字的最后一个字节的话，就会出现乱码
  >  解决的思路：
  >  第一个是定义一个足够大的byte数组，能把所有的内容都包含进去。（不建议，只适合小文件）
  >  第二个是使用字符流FileReader，通过字符输出能保证每个汉字都不乱码。（适合普通文本）
  >  第三是使用**转换流**把FileInputStream转换为FileReader。
  >
  > https://blog.csdn.net/Nortom/article/details/119063702
  
* 异常处理时，为了保证流资源一定可以执行关闭操作，用try-catch-finally处理。（**close放finally中，记得判断空指针**）

* 其实 这四个文件流都 **有个构造器可以直接放path**，构造器内部new File。比如new FileInputStream("一张图片")

### 代码示例

#### 读取文本文件

```java
    @Test
    public void testFileReader() {//使用read()
        FileReader fr = null;
        try {
            //1.实例化File类
            File file = new File("hello.txt");
            //2.提供具体的流
            fr = new FileReader(file);//可能FileNotFound异常

            //3.数据读入
            //read()//读入单个字符.返回作为整数读取的字符。如果已到达流的末尾，则返回 -1
            int data;
            while ((data = fr.read()) != -1) {//可能IO异常
                System.out.println((char) data);
            }
        } catch (FileNotFoundException e) {
            e.printStackTrace();
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            if (fr != null)//如果fr赋值前出现异常 fr会是空指针(运行时异常，需要避免)
                try {
                    //流的关闭操作
                    fr.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
        }
    }

    @Test
    public void testFileReader1() {//使用read(char[] cbuf)
        //使用read(char[] cbuff)
        FileReader fr = null;
        try {
            //1.实例化File类
            File file = new File("hello.txt");
            //2.提供具体的流
            fr = new FileReader(file);//可能FileNotFound异常
            //3.数据读入
            char[] cbuf = new char[5];//自己定义的数组长度是5则每次最多读5个
            int len;//记录读入的个数或-1
            //len=fr.read(cbuf);//将字符读入数组。返回每次读入的个数，如果到了文件末尾返回-1
            while ((len=fr.read(cbuf))!=-1){
                //方式一 循环
//                for (int i = 0; i < len;i++) {//要用len。不能用cbuf.length因为最后读的可能不够length的个数个(13个则5，5，3不足5,会导致个数少没覆盖原来的数据)。
//                    System.out.print(cbuf[i]);
//                }
                //方式二 转换成字符串
                String str = new String(cbuf,0,len);//要用String(cbuf,0,len)，不能String(cbuf)，原因同上
                System.out.print(str);

            }
        } catch (FileNotFoundException e) {
            e.printStackTrace();
        } catch (IOException e) {
            e.printStackTrace();
            //更具体System.out.println("read-Exception :" + e.getMessage());
        }finally {
            if(fr!=null) {
                try {
                    //3.资源关闭
                    fr.close();
                } catch (IOException e) {
                    e.printStackTrace();
                    //更具体System.out.println("close-Exception :" + e.getMessage());
                }
            }
        }
    }
```

#### 写入文本文件

```java
    @Test
    public void testFileWriter()  {
        FileWriter fw = null;
        try {
            File file = new File("hello1.txt");
            //fw = new FileWriter(file);
            //fw = new FileWriter(file,false);
            fw = new FileWriter(file,true);
            fw.write("hello world");
            fw.write("\n哈哈哈哈");
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            if(fw!=null) {
                try {
                    fw.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
        }
//内容：
//hello world
//哈哈哈哈
    }
```

#### 文件复制(文本文件)

```java
    // 以文本文件为例使用FileReader和FileWriter
    @Test
    public void testFileReaderWriter() {
        FileReader fr = null;
        FileWriter fw = null;
        try {
            File srcFile = new File("hello.txt");
            File desFile = new File("hello2.txt");

            fr = new FileReader(srcFile);
            fw = new FileWriter(desFile, true);

            char[] cbuf = new char[5];
            int len;
            while ((len = fr.read(cbuf)) != -1) {
                //fw.write(cbuf);错误写法
                fw.write(cbuf, 0, len);
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {//fr和fw先close哪个都可以 ，最好是从后往前——好习惯

            if (fw != null) {
                try {
                    fw.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }

            if (fr != null) {
                try {
                    fr.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
//也可以将close的操作放在fw的finally中，一样的
//            if (fw != null) {
//                try {
//                    fw.close();
//                } catch (IOException e) {
//                    e.printStackTrace();
//                } finally {
//                    if (fr != null) {
//                        try {
//                            fr.close();
//                        } catch (IOException e) {
//                            e.printStackTrace();
//                        }
//                    }
//                }
//            }
            
        }

    }
```

#### 文件复制 使用字节流

(其实复制文本文件也是可以的)

```java
//复制图片    
@Test
    public void testFileInputOutputStream() {
        FileInputStream fis = null;
        FileOutputStream fos = null;
        try {
            File srcfile = new File("一张图片.jpg");
            File destfile = new File("一张图片1.jpg");

            fis = new FileInputStream(srcfile);
            fos = new FileOutputStream(destfile);
            byte[] buffer = new byte[5];
            int len;
            while ((len = fis.read(buffer)) != -1) {
                fos.write(buffer, 0, len);
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            if (fos != null) {
                try {
                    fos.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
            if (fis != null) {
                try {
                    fis.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
        }
        System.out.println("图片复制完毕");
    }
```
可以改成一个通用的方法
```java
    public void copyFile(String srcPath, String destPath) {
        FileInputStream fis = null;
        FileOutputStream fos = null;
        try {
            File srcfile = new File(srcPath);
            File destfile = new File(destPath);

            fis = new FileInputStream(srcfile);
            fos = new FileOutputStream(destfile);
            byte[] buffer = new byte[1024];//一般可以1024(1KB)  其实更多用缓冲流
            int len;
            while ((len = fis.read(buffer)) != -1) {
                fos.write(buffer, 0, len);
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            if (fos != null) {
                try {
                    fos.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
            if (fis != null) {
                try {
                    fis.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
        }
        System.out.println("文件复制完毕");
    }

  @Test
    public void testCopyFile() {
        long start = System.currentTimeMillis();
        copyFile("测试.pptx","测试1.pptx");
        long end = System.currentTimeMillis();
        System.out.println("复制操作花费时间："+(end-start)+"毫秒");
    }
```



## 缓冲流——典型的处理流

开发中更常用缓冲流来包装文件流使用，而不是单纯使用文件流

### 注意点：

* **为了提高数据读写的速度**，Java API提供了带缓冲功能的流类，在使用这些流类时，会创建一个**内部缓冲区数组**，缺省使用8192个字节(8KB)的缓冲区。(对于BufferedReader 和 BufferedWriter是8192个字符 )

  ```java
  BufferedReader 和 BufferedWriter：
  private static int defaultCharBufferSize = 8192;//8192个字符 
  构造器中cb = new char[sz];//sz是defaultCharBufferSize
  
  BufferedReader 和 BufferedWriter：
  private static int DEFAULT_BUFFER_SIZE = 8192;//8192个字节  默认8KB
  构造器中buf = new byte[size];
  ```

* 缓冲流要“套接”在相应的节点流之上，根据数据操作单位可以把缓冲流分为
  **字节流 BufferedInputStream 和 BufferedOutputStream**
  **字符流BufferedReader 和 BufferedWriter**
  
* 当读取数据时，数据按块读入缓冲区，其后的读操作则直接访问缓冲区

  ①当使用BufferedInputStream读取字节文件时，BufferedInputStream会一次性从文件中读取8192个(8Kb)，存在缓冲区中，直到缓冲区装满了，才重新从文件中读取下一个8192个字节数组。

  ②向流中写入字节时，不会直接写到文件，先写到缓冲区中直到缓冲区写满，BufferedOutputStream才会把缓冲区中的数据一次性写到文件里。使用方法**flush()可以强制将缓冲区的内容全部写入输出流**

* 关闭流的顺序和打开流的顺序相反。**只要关闭最外层流即可，关闭最外层流也会自动关闭相应的内层节点流**

* flush()方法的使用：手动将buffer中内容写入文件

* 如果是**带缓冲区的流对象的close()方法，不但会关闭流，还会在关闭流之前刷新缓冲区**，关闭后不能再写出

* BufferedReader的增加了一个readLine方法 具体看代码示例

### 代码示例

#### BufferedInputStream&BufferedOutputStream

```java
public void copyFileWithBuffered(String srcPath,String destPath){
    BufferedInputStream bis = null;
    BufferedOutputStream bos = null;
    try {
        File srcFile =new File(srcPath);
        File destFile = new File(destPath);

        FileInputStream fis = new FileInputStream(srcFile);//缓冲流是处理流，套在节点流上
        FileOutputStream fos = new FileOutputStream(destFile);

        bis = new BufferedInputStream(fis);
        bos = new BufferedOutputStream(fos);

        byte[] buffer = new byte[1024];
        int len;
        while ((len=bis.read(buffer))!=-1){
            bos.write(buffer,0,len);
        }
    } catch (IOException e) {
        e.printStackTrace();
    } finally {
        //先关闭外层的流 再关闭内层的流。但是只要close()关闭最外层流即可，关闭最外层流也会自动关闭相应的内层节点流
        if(bos!=null) {
            try {
                bos.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
        if(bis!=null) {
            try {
                bis.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }
}

@Test
public void testCopyFileWithBuffered(){
    long start = System.currentTimeMillis();
    copyFileWithBuffered("E:\\java学习\\软件安装\\jdk-8u321-windows-x64.exe","jdk-8u321-2.exe");
    long end = System.currentTimeMillis();
    System.out.println("复制操作花费时间："+(end-start)+"毫秒");//275 快了差不多四倍
}
```

#### BufferedReader&BufferedWriter

```java
    public void copyBufferedReaderBufferedWriter(String srcPath,String destPath){
        BufferedReader br = null;
        BufferedWriter bw = null;
        try {
            File srcFile = new File(srcPath);
            File destFile = new File(destPath);

            FileReader fr = new FileReader(srcFile);
            FileWriter fw = new FileWriter(destFile);

            br = new BufferedReader(fr);
            bw = new BufferedWriter(fw);
            //方式一
            char[] cbuf = new char[1024];
            int len;
            while ((len=br.read(cbuf))!=-1){
                bw.write(cbuf,0,len);
            }
            //方式二 使用String 和 注意是null哦readLine()
            //public String readLine() throws IOException
            //读取一个文本行。通过下列字符之一即可认为某行已终止：换行 ('\n')、回车 ('\r') 或回车后直接跟着换行。
            //返回：包含该行内容的字符串，不包含任何行终止符，如果已到达流末尾，则返回 null
            String data;
            while((data= br.readLine())!=null){//注意是null哦
                //因为返回的字符串不包含换行和回车 需要自己添加一个
                //bw.write(data+"\n");//这样也可以
                bw.write(data);
                bw.newLine();//相当于一个回车
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            if(bw!=null) {
                try {
                    bw.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
            if(br!=null) {
                try {
                    br.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
        }
    }
@Test
public void testCopyBufferedReaderBufferedWriter(){
    long start = System.currentTimeMillis();
    copyBufferedReaderBufferedWriter("nertc_log_engine.txt","log.txt");
    long end = System.currentTimeMillis();
    System.out.println("复制操作花费时间："+(end-start)+"毫秒");
}
```

### 练习

1.实现图片加密\解密操作。

```java
@Test
public void encrypt(){//图片加密 提示 buffer[i]^5  
    BufferedInputStream bis = null;
    BufferedOutputStream bos = null;
    try {
        bis = new BufferedInputStream(new FileInputStream("一张图片.jpg"));
        bos = new BufferedOutputStream(new FileOutputStream("一张图片加密后.jpg"));

        byte[] buffer = new byte[1024];
        int len;
        while((len=bis.read(buffer))!=-1){
            //对字节数组进行修改 实现加密
            for (int i = 0; i < len; i++) {
                buffer[i]= (byte) (buffer[i]^5);
            }
            bos.write(buffer,0,len);
        }
    } catch (IOException e) {
        e.printStackTrace();
    } finally {
        if(bos!=null) {
            try {
                bos.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
        if(bis!=null) {
            try {
                bis.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }
}


@Test
public void decrypt(){//图片解密 提示 buffer[i]^5  和加密一样的，只改了path。m^n^n=m
    BufferedInputStream bis = null;
    BufferedOutputStream bos = null;
    try {
        bis = new BufferedInputStream(new FileInputStream("一张图片加密后.jpg"));
        bos = new BufferedOutputStream(new FileOutputStream("一张图片解密后.jpg"));

        byte[] buffer = new byte[1024];
        int len;
        while((len=bis.read(buffer))!=-1){
            //对字节数组进行修改 实现加密
            for (int i = 0; i < len; i++) {
                buffer[i]= (byte) (buffer[i]^5);
            }
            bos.write(buffer,0,len);
        }
    } catch (IOException e) {
        e.printStackTrace();
    } finally {
        if(bos!=null) {
            try {
                bos.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
        if(bis!=null) {
            try {
                bis.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }
}
```

2.获取文本上每个字符出现的次数
提示：遍历文本的每一个字符；字符及出现的次数保存在Map中；将Map中数据写入文件

```java
//自己写的
    public void wordCount(String srcPath, String destPath) {
        BufferedReader br = null;
        BufferedWriter bw = null;
        try {
            br = new BufferedReader(new FileReader(srcPath));
            bw = new BufferedWriter(new FileWriter(destPath));

            HashMap<Integer, Integer> map = new HashMap<>();
            int c;
            while ((c = br.read()) != -1) {
                if (map.containsKey(c))
                    map.put(c, map.get(c) + 1);
                else
                    map.put(c, 1);
            }
            Set<Map.Entry<Integer, Integer>> enterSet = map.entrySet();//Set<Map.Entry<Character, Integer>>也可以 key是(char)c

            for (Map.Entry<Integer, Integer> enter : enterSet) {
                //System.out.println(enter.getKey() + " " + enter.getValue());
                int key = enter.getKey();
                int value = enter.getValue();
                if ((char) key == '\r') {//或key==13 \r  13  回车
                    bw.write("回车 " + value + "\n");
                } else if ((char) key == '\n') {//或key==10 \n 10 换行
                    bw.write("换行 " + value + "\n");
                } else if ((char) key == ' ') {//或key==32 空格 32
                    bw.write("空格 " + value + "\n");
                }else if ((char) key == '\t') {//或key==9 制表符 9
                    bw.write("制表符 " + value + "\n");
                }else if ((char) key == '\u200B') {//zwsp 宽零空格
                    bw.write("宽零空格 " + value + "\n");
                }else {
                    bw.write((char) key + " " + value + "\n");
                }

            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            if (bw != null) {
                try {
                    bw.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
            if (br != null) {
                try {
                    br.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
        }

    }

    @Test
    public void testWordCount() {
        wordCount("E:\\java学习\\JavaSE.md", "WordCound.txt");
    }
```

```java
//老师的 感觉他写的不太好。。。
public class WordCount {
    @Test
    public void testWordCount() {
        FileReader fr = null;
        BufferedWriter bw = null;
        try {
            //1.创建Map集合
            Map<Character, Integer> map = new HashMap<Character, Integer>();

            //2.遍历每一个字符,每一个字符出现的次数放到map中
            fr = new FileReader("dbcp.txt");
            int c = 0;
            while ((c = fr.read()) != -1) {
                //int 还原 char
                char ch = (char) c;
                // 判断char是否在map中第一次出现
                if (map.get(ch) == null) {
                    map.put(ch, 1);
                } else {
                    map.put(ch, map.get(ch) + 1);
                }
            }

            //3.把map中数据存在文件count.txt
            //3.1 创建Writer
            bw = new BufferedWriter(new FileWriter("wordcount.txt"));

            //3.2 遍历map,再写入数据
            Set<Map.Entry<Character, Integer>> entrySet = map.entrySet();
            for (Map.Entry<Character, Integer> entry : entrySet) {
                switch (entry.getKey()) {
                    case ' ':
                        bw.write("空格=" + entry.getValue());
                        break;
                    case '\t'://\t表示tab 键字符
                        bw.write("tab键=" + entry.getValue());
                        break;
                    case '\r'://
                        bw.write("回车=" + entry.getValue());
                        break;
                    case '\n'://
                        bw.write("换行=" + entry.getValue());
                        break;
                    default:
                        bw.write(entry.getKey() + "=" + entry.getValue());
                        break;
                }
                bw.newLine();
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            //4.关流
            if (fr != null) {
                try {
                    fr.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }

            }
            if (bw != null) {
                try {
                    bw.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }

            }
        }

    }
}
```



## 转换流

处理流之二：转换流

转换流提供了在字节流和字符流之间的转换——类似"桥"

> 学英语：transform  vt 使转换

* Java API提供了两个转换流：
    **InputStreamReader：将InputStream转换为Reader**——解码
    **OutputStreamWriter：将Writer转换为OutputStream**——编码

    **记好了套哪个流**：InputStreamReader(InputStream)——程序——OutputStreamWriter(OutputStream)
    
* 字节流中的数据都是字符时，转成字符流操作更高效。

* 很多时候我们使用转换流来处理文件乱码问题。实现编码和解码的功能。

![转换流](http://101.34.218.64/JavaSE.assets/%E8%BD%AC%E6%8D%A2%E6%B5%81.png)

### InputStreamReader

* 实现将**字节的输入流**按指定字符集**转换为字符的输入流**。
* 需要**和InputStream“套接”**。
* 构造器
  public InputStreamReader(InputStream in)//使用系统默认字符集
  public InputSreamReader(InputStream in,String charsetName)
  如： Reader isr = new InputStreamReader(System.in,”gbk”);
* 文件编码的方式决定了解析时使用的字符集。(文件是什么编码的，读的时候就按什么转化)

### OutputStreamWriter

* 实现将**字符的输出流**按指定字符集**转换为字节的输出流**。
* 需要**和OutputStream“套接”**。
* 构造器
  public OutputStreamWriter(OutputStream out)
  public OutputSreamWriter(OutputStream out,String charsetName)

### 代码示例

```java
/**
 * *InputStreamReader：将InputStream转换为Reader
 * *OutputStreamWriter：将Writer转换为OutputStream
 */
public class TransformTest {
    @Test
    public void testTransform() {
        InputStreamReader isr = null;
        OutputStreamWriter osw = null;
        try {
            FileInputStream fis = new FileInputStream("D:\\test_utf-8.txt");
            FileOutputStream fos = new FileOutputStream("D:\\test_gbk.txt");

            //InputStreamReader isr = new InputStreamReader(fis);//使用默认的字符集
            isr = new InputStreamReader(fis, "utf-8");//确定的。文件编码的方式决定了解析时使用的字符集。因为文件test_utf-8.txt是utf-8的
            osw = new OutputStreamWriter(fos, "gbk");//可变的。根据需要来，想保存成什么编码的

            //转化后当Reader和Writer用就好了
            char[] cbuf = new char[20];
            int len;
            while ((len = isr.read(cbuf)) != -1) {
                            String str = new String(cbuf,0,len);
                            System.out.println(str);
                //            osw.write(str);
                osw.write(cbuf, 0, len);
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            if (osw != null) {
                try {
                    osw.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
            if (isr != null) {
                try {
                    isr.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
        }
    }
}
```

### 常见字符集(了解)

ASCII：美国标准信息交换码。用一个字节的7位可以表示。
ISO8859-1：拉丁码表。欧洲码表。用一个字节的8位表示。
GB2312：中国的中文编码表。最多两个字节编码所有字符
GBK：中国的中文编码表升级，融合了更多的中文文字符号。最多两个字节编码
    GBK2312和GBK 两个字节,首位0则这两个字节各表示两个字符,首位1则两个字节一起表示一个字符
UTF-8：变长的编码方式，可用1-4个字节来表示一个字符。
Unicode：国际标准码，融合了目前人类使用的所字符。为每个字符分配唯一的字符码。所有的文字都用两个字节来表示。

一些说明：
ANSI编码，通常指的是平台的默认编码，例如英文操作系统中是ISO-8859-1，中文系统是GBK
GBK2312,GBK,UTF-8都**兼容ASCII，可以用ASCII码表示一个英文字母**  一个字节就够
Unicode只是定义了一个庞大的、全球通用的字符集，并为每个字符规定了唯一确定的编号，具体存储成什么样的字节流，取决于字符码方案。推荐的Unicode编码是UTF-8和UTF-16。
    Unicode字符集只是定义了字符的集合和唯一编号，
    Unicode编码，则是对UTF-8、UCS-2/UTF-16等具体编码方案的统称而已，并不是具体的编码方案。
    UTF-8就是每次8个位传输数据，而UTF-16就是每次16个位
    UTF-8如何1-4个字节表示(超出多语言范围的字符用4个字节，修正的UTF-8编码中需要6个)：
    0XXXXXXX 一个字节 兼容ASCII
    110XXXXX 1OXXXXXX 见到110开头就是2个字节 10开头的是跟着的
    1110xxxx 1OXXXXXX 1OXXXXXX 见到1110就是3个字节
    11110xxx 1OXXXXXX 1OXXXXXX 1OXXXXXX 见到11110就是4个字节
    中文字符在UTF-8中3个字节
    ![UTF-8表示汉字.png](http://101.34.218.64/JavaSE.assets/UTF-8%E8%A1%A8%E7%A4%BA%E6%B1%89%E5%AD%97.png)

对后面学习的启示：
客户端/浏览器端    <---->  后台(java,GO,Python,Node.js,php)   <----> 数据库
**要求前前后后使用的字符集都要统一：UTF-8.**

中文字符在UTF-8中3个字节

## 标准输入、输出流(了解)

处理流之三
static InputStream in “标准”输入流。 
static PrintStream out   “标准”输出流 
static PrintStream err “标准”错误输出流。 

* System.in和System.out分别代表了系统标准的输入和输出设备
* 默认输入设备是：键盘，输出设备是：显示器(控制台)
* System.in的类型是InputStream
* System.out的类型是PrintStream，其是OutputStream的子类FilterOutputStream 的子类
* 重定向：通过System类的setIn，setOut方法对默认设备进行改变。
  public static void setIn(InputStream in)
  public static void setOut(PrintStream out)

代码示例

```java
//从键盘一行一行输入字符串，要求将读取到的整行字符串转成大写输出。
//然后继续进行输入操作，直至当输入“e”或者“exit”时，退出程序。
       //方法一 使用Scanner 调用next() 判断字符串
        //方法二 使用System.in ——>BufferedReader的readLine
    @Test
    public void testInOut(){
        BufferedReader br = null;
        String data=null;
        try {
            InputStreamReader isr=new InputStreamReader(System.in);
            br = new BufferedReader(isr);
            System.out.println("请输入(输入e或者exit退出):");
            while((data = br.readLine()) != null){
                if("e".equalsIgnoreCase(data)||"exit".equalsIgnoreCase(data)){
                    System.out.println("程序结束");
                    break;
                }
                String upperCase = data.toUpperCase();
                System.out.println(upperCase);
                System.out.println("输入e或者exit退出:");
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            if(br!=null) {
                try {
                    br.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
        }
    }

```

Create a program named MyInput.java: Contain the methods for reading int,double, float, boolean, short, byte and String values from the keyboard.

```java
public class MyInput {//模拟一个Scanner
    public static String readString() {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String string = "";
        try {
            string = br.readLine();
        } catch (IOException ex) {
            System.out.println(ex);
        }
        return string;
    }
    public static int readInt() {return Integer.parseInt(readString());}
    public static double readDouble() {return Double.parseDouble(readString());}
    public static double readByte() {return Byte.parseByte(readString());}
    public static double readShort() {return Short.parseShort(readString());}
    public static double readLong() {return Long.parseLong(readString());}
    public static double readFloat() {return Float.parseFloat(readString());}
}
```

## 打印流(了解)

处理流之四

打印流：PrintStream和PrintWriter 都是输出流

将**基本数据类型**的数据格式转化为**字符串**输出

* 提供了一系列重载的print()和println()方法，用于多种数据类型的输出
* PrintStream和PrintWriter的输出不会抛出IOException异常
* PrintStream和PrintWriter有自动flush功能
* PrintStream 打印的所有字符都使用平台的默认字符编码转换为字节。
    在需要写入字符而不是写入字节的情况下，应该使用 PrintWriter 类。
* System.out返回的是PrintStream的实例

## 数据流(了解)

处理流之五

 为了方便地操作Java语言的基本数据类型和String的数据，可以使用数据流。
 数据流有两个类：DataInputStream 和 DataOutputStream 
(用于读取和写出基本数据类型、String类的数据）——实体化
分别“套接”在 InputStream 和 OutputStream 子类的流上

 DataInputStream中的方法
    boolean readBoolean()
    byte readByte()
    char readChar()
    float readFloat()
    double readDouble()
    short readShort()
    long readLong()
    int readInt()
    String readUTF() void readFully(byte[] b)
 DataOutputStream中的方法 将上述的方法的read改为相应的write即可。

```java
@Test
public void testDataOutputStream() {
    DataOutputStream dos = null;
    try { // 创建连接到指定文件的数据输出流对象
        dos = new DataOutputStream(new FileOutputStream("destData.dat"));
        dos.writeUTF("我爱北京天安门"); // 写UTF字符串
        dos.writeBoolean(false); // 写入布尔值
        dos.writeLong(1234567890L); // 写入长整数
        System.out.println("写文件成功!");
    } catch (IOException e) {
        e.printStackTrace();
    } finally {
        try {
            if (dos != null) {
                dos.close();
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}

@Test
public void testDataInputStream() {
    DataInputStream dis = null;
    try {
        dis = new DataInputStream(new FileInputStream("destData.dat"));
        //读取顺序要和写入顺序一样
        String info = dis.readUTF();
        boolean flag = dis.readBoolean();
        long time = dis.readLong();
        System.out.println(info);
        System.out.println(flag);
        System.out.println(time);
    } catch (Exception e) {
        e.printStackTrace();
    } finally {
        if (dis != null) {
            try {
                dis.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }
}
```

## 对象流(主要是理解序列化**)

处理流之六：对象流(对象流用的不多 ， 开发中会用json传输。**这节主要是理解序列化**)

**ObjectInputStream和OjbectOutputSteam**
用于**存储和读取基本数据类型数据或对象的处理流**。它的强大之处就是**可以把Java中的对象写入到数据源中(序列化)，也能把对象从数据源中还原回来。(反序列化)**
    **序列化：用ObjectOutputStream类保存**基本类型数据或对象的机制。内存中的对象--->存储中的文件、通过网络传输出去
    **反序列化：用ObjectInputStream类读取**基本类型数据或对象的机制。存储中的文件、通过网络接收过来 --->内存中的对象
注意： ObjectOutputStream和ObjectInputStream**不能序列化static和transient修饰的成员变量**

### 对象的序列化

**对象序列化机制允许把内存中的Java对象转换成平台无关的二进制流，从而允许把这种二进制流持久地保存在磁盘上，或通过网络将这种二进制流传输到另一个网络节点(序列化)。当其它程序获取了这种二进制流，就可以恢复成原来的Java对象（反序列化）**——(面试可能问。)

> 序列化的好处在于可将任何实现了Serializable接口的对象转化为**字节数据**，使其在保存和传输时可被还原。
> 序列化是 RMI（Remote Method Invoke – 远程方法调用）过程的参数和返回值都必须实现的机制，而 RMI 是 JavaEE 的基础。因此序列化机制是JavaEE 平台的基础。

* 如果需要让某个对象支持序列化机制，则**必须让对象所属的类及其属性是可序列化的**，**为了让某个类是可序列化的，该类必须实现如下两个接口之一**。（否则，会抛出NotSerializableException异常）
  **Serializable**//这是一个标识接口(标记接口) 没有方法。  英语翻译 可串行化的
  Externalizable //该接口有方法需要实现，因此我们一般实现上面的Serializable接口

### serialVersionUID 

序列版本号

* 凡是实现Serializable接口的类都有一个表示序列化版本标识符的静态变量：
  private static final long serialVersionUID;
  serialVersionUID用来表明类的不同版本间的兼容性。简言之，其目的是**以序列化对象进行版本控制，有关各版本反序列化时是否兼容**。
  **如果类没有显示定义这个静态常量时，它的值是Java运行时环境根据类的内部细节自动生成的。若类的实例变量做了修改，serialVersionUID 可能发生变化。故建议，显式声明。**
 简单来说，Java的序列化机制是通过在运行时判断类的serialVersionUID来验证版本一致性的。**在进行反序列化时，JVM会把传来的字节流中的serialVersionUID与本地相应实体类的serialVersionUID进行比较，如果相同就认为是一致的，可以进行反序列化**，否则就会出现序列化版本不一致的异常。(InvalidCastException)

### 总结: 自定义类可序列化(熟悉)

1.需要实现接口：Serializable
2.当前类提供一个全局常量：serialVersionUID
3.除了当前Person类需要实现Serializable接口之外，还必须保证其内部所属性也必须是可序列化的。（默认情况下，基本数据类型可序列化）

补充：ObjectOutputStream和ObjectInputStream不能序列化static和transient修饰的成员变量

### 使用对象流序列化对象

#### 序列化

**前提：对象是可序列化的**。（类实现了 Serializable 接口，该类的对象就是可序列化的）
    注意：如果某个类的**属性**不是基本数据类型或 String 类型，而**是另一个引用类型**，那么**这个引用类型必须是可序列化**的，否则拥有该类型的Field 的类也不能序列化

* 创建一个 **ObjectOutputStream**
* 调用 ObjectOutputStream 对象的 ==**writeObject(对象)**== 方法输出可序列化对象
* 注意**写出一次，操作flush()一次**

#### 反序列化

* 创建一个 **ObjectInputStream**
* 调用 **==readObject==()** 方法读取流中的对象

#### 代码示例

```java
class Account implements Serializable{//Person内部属性是引用变量 所属的类应该也是可序列化的
    static final long serialVersionUID = 12345678901L;
    private double balance;
    public Account(double balance) {
        this.balance = balance;
    }
    @Override
    public String toString() {
        return "Account{" + "balance=" + balance + '}';
    }
}
class Person implements Serializable{
    public static final long serialVersionUID = 1234567890L;//最好显式声明。可随便写一个。前面自定义异常类见过。
    private String name;//String类是可序列化的
    private int age;
    private transient int t;
    private static int s;
    private Account acc;

    public Person(String name, int age, int t, Account acc) {
        this.name = name;
        this.age = age;
        this.t = t;
        this.acc = acc;
    }
//getter setter tostring..
}
public class ObjectStreamTest {
    @Test
    public void testObjectOutputStream(){
        ObjectOutputStream oos = null;
        try {
            oos = new ObjectOutputStream(new FileOutputStream("object.dat"));
            oos.writeObject(new String("你好"));//String是可序列化的
            oos.flush();//写一个，刷新一次
            Person p = new Person("小明",20,11,new Account(500.0));
            Person.setS(1);
            oos.writeObject(p);//自定义的Person 是可序列化的(实现Serializable)
            oos.flush();//写一个，刷新一次
            p.setAge(21);//后面改的话 不影响已保存的 还是20
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            if(oos!=null){
                try {
                    oos.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
        }
    }

    @Test
    public void testObjectInputStream(){
        ObjectInputStream ois= null;
        try {
            ois = null;
            ois=new ObjectInputStream(new FileInputStream("object.dat"));
            //readObject()方法返回的是一个Object 需要向下转型。按序列化(保存)时的顺序反序列化(读取)
            String str=(String) ois.readObject();
            System.out.println(str);
            Person p = (Person) ois.readObject();
            System.out.println(p);
           System.out.println(Person.getS());
        } catch (IOException e) {
            e.printStackTrace();
        } catch (ClassNotFoundException e) {
            e.printStackTrace();
        } finally {
            try {
                ois.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
        //你好
        //Person{name='小明, age=20, t=0, acc=Account{balance=500.0}}  //t=0  transient的属性不可被序列化
        //0  //static的属性s不可被实例化
    }
```

#### 面试题

谈谈你对java.io.Serializable接口的理解，我们知道它用于序列化，是空方法接口，还有其它认识吗？
* 实现了Serializable接口的对象，可将它们转换成一系列字节，并可在以后完全恢复回原来的样子。这一过程亦可通过网络进行。这意味着序列化机制能自动补偿操作系统间的差异。换句话说，可以先在Windows机器上创建一个对象，对其序列化，然后通过网络发给一台Unix机器，然后在那里准确无误地重新“装配”。不必关心数据在不同机器上如何表示，也不必关心字节的顺序或者其他任何细节。
* 由于大部分作为参数的类如String、Integer等都实现了java.io.Serializable的接口，也可以利用多态的性质，作为参数使接口更灵活。

## 随机存取文件流(了解)

RandomAccessFile 类
* RandomAccessFile 声明在java.io包下，但直接继承于java.lang.Object类。
  并且它实现了DataInput、DataOutput这两个接口，也就意味着这个类**既可以读也可以写**。（**既可以作为一个输入流，又可以作为一个输出流**）（作为**输出流时会对原文件内容进行覆盖**。默认情况下，从头覆盖）

* RandomAccessFile 类支持 “**随机访问**” 的方式，程序可**以直接跳到文件的任意地方来读、写文件**
  
    支持只访问文件的部分内容
    
    可以向已存在的文件后追加内容
    
* RandomAccessFile 对象包含一个**记录指针**，用以标示当前读写处的位置。
  RandomAccessFile 类对象**可以自由移动记录指针**：
    long **getFilePointer**()：获取文件记录指针的当前位置
    void **seek**(long pos)：将文件记录指针定位到 pos 位置

* 构造器
    public RandomAccessFile(File file, String mode)
    public RandomAccessFile(String name, String mode)
    
* 创建 RandomAccessFile 类实例需要指定一个 mode 参数，该参数**指定 RandomAccessFile 的访问模式**：
    **r**: 以只读方式打开
    **rw**：打开以便读取和写入
    rwd:打开以便读取和写入；同步文件内容的更新(write数据时，rw不会立即写入硬盘。rwd立即写入硬盘。如果写数据过程中发生异常，rwd模式中已被write的数据会被保存到硬盘，而rw则全部丢失)
    rws:打开以便读取和写入；同步文件内容和元数据的更新
    如果模式为**只读r。则不会创建文件**，而是会去读取一个已经存在的文件，如果**读取的文件不存在则会出现异常**。
    如果模式为**rw读写。如果文件不存在则会去创建文件**，如果存在则不会创建。

### 代码示例
#### 读取、写入文件

```java
@Test
public void testRandomAccessFile(){
    RandomAccessFile raf1 = null;
    RandomAccessFile raf2 = null;
    try {
        //虽然既可以读也可以写，但是要new两个对象
        raf1 = new RandomAccessFile(new File("一张图片.jpg"),"r");
        //RandomAccessFile raf1 = new RandomAccessFile("一张图片.jpg","r");//构造器RandomAccessFile(String name, String mode)
        raf2 = new RandomAccessFile(new File("一张图片2.jpg"),"rw");

        byte[] buffer =new byte[1024];
        int len;
        while((len=raf1.read(buffer))!=-1){
            raf2.write(buffer,0,len);
        }
    } catch (IOException e) {
        e.printStackTrace();
    } finally {
        if(raf1!=null) {
            try {
                raf1.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
        if(raf2!=null) {
            try {
                raf2.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }
}
```

#### seek()的使用

```java
@Test
public void testSeeK()  {
    RandomAccessFile raf1 = null;//helloworld
    try {
        raf1 = new RandomAccessFile("hello.txt","rw");
        System.out.println(raf1.getFilePointer());//0
        raf1.seek(3);//pos - 从文件开头以字节为单位测量的偏移量位置 也就是字节数组下表位置
        System.out.println(raf1.getFilePointer());//3
        raf1.write("xyz".getBytes());
        System.out.println(raf1.getFilePointer());//6
    } catch (IOException e) {
        e.printStackTrace();
    } finally {
        try {
            raf1.close();
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
    //helxyzorld
}
```
#### 模拟插入效果

实现RandomAccessFile模拟word的“插入”数据的效果。用seek(int pos) 
在abcdefg 中插入xyz 变成abxyzcdefg

```java
@Test
public void Insert() {
    //实现RandomAccessFile模拟word的“插入”数据的效果。用seek(int pos)   在abcdefg 中插入xyz 变成abxyzcdefg
    RandomAccessFile raf = null;
    try {
        raf = new RandomAccessFile("hello.txt","rw");
        raf.seek(2);//调文件指针到3
        //把从3到后面的内容存到StringBuilder里
        StringBuilder sb = new StringBuilder((int) new File("hello.txt").length());//指定一个长度为文件大小(字节)的 StringBuilder底层char[]的长度
        byte[] buffer = new byte[1024];
        int len;
        while((len=raf.read(buffer))!=-1){
            sb.append(new String(buffer,0,len));
        }//sb里cdefg
        raf.seek(2);//移回来
        raf.write("xyz".getBytes());//要插入的内容写入  文件里：abxyzfg

        raf.write(sb.toString().getBytes());//后面的内容在StringBuilder中的数据再写入  文件里：abxyzcdefg
    } catch (IOException e) {
        e.printStackTrace();
    } finally {
        if(raf!=null) {
            try {
                raf.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }
}
```

#### 断点下载 (思路

我们可以用RandomAccessFile这个类，来实现一个多线程断点下载的功能，
下载前都会建立两个临时文件，一个是与被下载文件大小相同的空文件，另一个是记录文件指针的位置文件，每次暂停的时候，都会保存上一次的指针，然后断点下载的时候，会继续从上一次的地方下载，从而实现断点下载或上传的功能

## 字节数组流

 ByteArrayOutputStream 字节数组输出流  可以避免出现乱码

### 一种节点流

```java
public class ByteArrayOutputStreamTest {
	@Test
	public void test1() throws Exception {
		FileInputStream fis = new FileInputStream("abc.txt");
		String info = readStringFromInputStream(fis);
		System.out.println(info);
	}

	private String readStringFromInputStream(FileInputStream fis) throws IOException {
		// 方式一：可能出现乱码
		// String content = "";
		// byte[] buffer = new byte[1024];
		// int len;
		// while((len = fis.read(buffer)) != -1){
		// content += new String(buffer);
		// }
		// return content;

		// 方式二：BufferedReader
		BufferedReader reader = new BufferedReader(new InputStreamReader(fis));
		char[] buf = new char[10];
		int len;
		String str = "";
		while ((len = reader.read(buf)) != -1) {
			str += new String(buf, 0, len);
		}
		return str;

		// 方式三：可以避免出现乱码
		// ByteArrayOutputStream baos = new ByteArrayOutputStream();
		// byte[] buffer = new byte[10];
		// int len;
		// while ((len = fis.read(buffer)) != -1) {
		// baos.write(buffer, 0, len);
		// }
		//
		// return baos.toString();
	}
}
```

## NIO.2

(==也很重要 面试高频 这里不细讲 后面项目用到的时候再讲==)

### NIO.2概述
Java NIO (New IO，Non-Blocking IO)是从Java 1.4版本开始引入的一套新的IO API，可以替代标准的Java IO API。
NIO与原来的IO有同样的作用和目的，但是使用的方式完全不同，NIO支持面向缓冲区的(IO是面向流的)、基于通道的IO操作。NIO将以**更加高效**的方式进行文件的读写操作。

Java API中提供了两套NIO，一套是针对标准输入输出NIO，另一套就是网络编程NIO。
java.nio.channels包下
Channel接口
|-----FileChannel:处理本地文件
|-----SocketChannel：TCP网络编程的客户端的Channel
|-----ServerSocketChannel:TCP网络编程的服务器端的Channel
|-----DatagramChannel：UDP网络编程中发送端和接收端的Channel


NIO. 2
随着 **JDK 7** 的发布，Java对NIO进行了极大的扩展，增强了对文件处理和文件系统特性的支持，以至于我们称他们为 **NIO.2**


### NIO.2中Path、Paths、Files类的使用
#### Path接口
早期的Java只提供了一个File类来访问文件系统，但File类的功能比较有限，所提供的方法性能也不高。而且，大多数方法在出错时仅返回失败，并不会提供异常信息。

NIO. 2为了弥补这种不足，引入了Path接口（jdk1.7），代表一个平台无关的平台路径，描述了目录结构中文件的位置。Path可以看成是File类的升级版本，实际引用的资源也可以不存在。
```java
在以前IO操作都是这样写的:
import java.io.File;
File file = new File("index.html");
但在Java7 中，我们可以这样写：
import java.nio.file.Path;
import java.nio.file.Paths;
Path path = Paths.get("index.html");
```

#### Files、Paths工具类
NIO.2在java.nio.file包下还提供了Paths、Files工具类：
1.Paths包含了两个返回Path的静态工厂方法。
* static Path get(String first, String … more) : 用于将多个字符串串连成路径
* static Path get(URI uri): 返回指定uri对应的Path路径
  

2.Files是用于操作文件或目录的工具类。Files包含了大量静态的工具方法来操作文件。Files常用方法：
(1)操作文件和目录

* Path copy(Path src, Path dest, CopyOption … how) : 文件的复制
* Path **createDirectory**(Path path, FileAttribute<?> … attr) : 创建一个目录
* Path **createFile**(Path path, FileAttribute<?> … arr) : 创建一个文件
* void delete(Path path) : 删除一个文件/目录，如果不存在，执行报错
* void **deleteIfExists**(Path path) : Path对应的文件/目录如果存在，执行删除
* Path move(Path src, Path dest, CopyOption…how) : 将 src 移动到 dest 位置
* long **size**(Path path) : 返回 path 指定文件的大小

(2)用于判断
* boolean exists(Path path, LinkOption … opts) : 判断文件是否存在
* boolean isDirectory(Path path, LinkOption … opts) : 判断是否是目录
* boolean isRegularFile(Path path, LinkOption … opts) : 判断是否是文件
* boolean isHidden(Path path) : 判断是否是隐藏文件
* boolean isReadable(Path path) : 判断文件是否可读
* boolean isWritable(Path path) : 判断文件是否可写
* boolean notExists(Path path, LinkOption … opts) : 判断文件是否不存在

(3)用于操作内容
* SeekableByteChannel newByteChannel(Path path, OpenOption…how) : 获取与指定文件的连接，how 指定打开方式。
* DirectoryStream\<Path\> newDirectoryStream(Path path) : 打开 path 指定的目录
* InputStream newInputStream(Path path, OpenOption…how):获取 InputStream 对象
* OutputStream newOutputStream(Path path, OpenOption…how) : 获取 OutputStream 对象

#### 代码示例Path

```java
package com.atguigu.java1;
import java.io.File;
import java.nio.file.Path;
import java.nio.file.Paths;
import org.junit.Test;

public class PathTest {

    //如何使用Paths实例化Path
    @Test
    public void test1() {
        Path path1 = Paths.get("d:\\nio\\hello.txt");//new File(String filepath)

        Path path2 = Paths.get("d:\\", "nio\\hello.txt");//new File(String parent,String filename);

        System.out.println(path1);
        System.out.println(path2);

        Path path3 = Paths.get("d:\\", "nio");
        System.out.println(path3);
    }

    //Path中的常用方法
    @Test
    public void test2() {
        Path path1 = Paths.get("d:\\", "nio\\nio1\\nio2\\hello.txt");
        Path path2 = Paths.get("hello.txt");

//		String toString() ： 返回调用 Path 对象的字符串表示形式
        System.out.println(path1);

//		boolean startsWith(String path) : 判断是否以 path 路径开始
        System.out.println(path1.startsWith("d:\\nio"));
//		boolean endsWith(String path) : 判断是否以 path 路径结束
        System.out.println(path1.endsWith("hello.txt"));
//		boolean isAbsolute() : 判断是否是绝对路径
        System.out.println(path1.isAbsolute() + "~");
        System.out.println(path2.isAbsolute() + "~");
//		Path getParent() ：返回Path对象包含整个路径，不包含 Path 对象指定的文件路径
        System.out.println(path1.getParent());
        System.out.println(path2.getParent());
//		Path getRoot() ：返回调用 Path 对象的根路径
        System.out.println(path1.getRoot());
        System.out.println(path2.getRoot());
//		Path getFileName() : 返回与调用 Path 对象关联的文件名
        System.out.println(path1.getFileName() + "~");
        System.out.println(path2.getFileName() + "~");
//		int getNameCount() : 返回Path 根目录后面元素的数量
//		Path getName(int idx) : 返回指定索引位置 idx 的路径名称
        for (int i = 0; i < path1.getNameCount(); i++) {
            System.out.println(path1.getName(i) + "*****");
        }

//		Path toAbsolutePath() : 作为绝对路径返回调用 Path 对象
        System.out.println(path1.toAbsolutePath());
        System.out.println(path2.toAbsolutePath());
//		Path resolve(Path p) :合并两个路径，返回合并后的路径对应的Path对象
        Path path3 = Paths.get("d:\\", "nio");
        Path path4 = Paths.get("nioo\\hi.txt");
        path3 = path3.resolve(path4);
        System.out.println(path3);

//		File toFile(): 将Path转化为File类的对象
        File file = path1.toFile();//Path--->File的转换

        Path newPath = file.toPath();//File--->Path的转换
    }
}

```

#### 代码示例Files

```java
package com.atguigu.java1;

import java.io.IOException;
import java.io.InputStream;
import java.io.OutputStream;
import java.nio.channels.SeekableByteChannel;
import java.nio.file.DirectoryStream;
import java.nio.file.Files;
import java.nio.file.LinkOption;
import java.nio.file.Path;
import java.nio.file.Paths;
import java.nio.file.StandardCopyOption;
import java.nio.file.StandardOpenOption;
import java.util.Iterator;

import org.junit.Test;

/**
 * Files工具类的使用：操作文件或目录的工具类
 */
public class FilesTest {

	@Test
	public void test1() throws IOException{
		Path path1 = Paths.get("d:\\nio", "hello.txt");
		Path path2 = Paths.get("atguigu.txt");
		
//		Path copy(Path src, Path dest, CopyOption … how) : 文件的复制
		//要想复制成功，要求path1对应的物理上的文件存在。path1对应的文件没有要求。
//		Files.copy(path1, path2, StandardCopyOption.REPLACE_EXISTING);
		
//		Path createDirectory(Path path, FileAttribute<?> … attr) : 创建一个目录
		//要想执行成功，要求path对应的物理上的文件目录不存在。一旦存在，抛出异常。
		Path path3 = Paths.get("d:\\nio\\nio1");
//		Files.createDirectory(path3);
		
//		Path createFile(Path path, FileAttribute<?> … arr) : 创建一个文件
		//要想执行成功，要求path对应的物理上的文件不存在。一旦存在，抛出异常。
		Path path4 = Paths.get("d:\\nio\\hi.txt");
//		Files.createFile(path4);
		
//		void delete(Path path) : 删除一个文件/目录，如果不存在，执行报错
//		Files.delete(path4);
		
//		void deleteIfExists(Path path) : Path对应的文件/目录如果存在，执行删除.如果不存在，正常执行结束
		Files.deleteIfExists(path3);
		
//		Path move(Path src, Path dest, CopyOption…how) : 将 src 移动到 dest 位置
		//要想执行成功，src对应的物理上的文件需要存在，dest对应的文件没有要求。
//		Files.move(path1, path2, StandardCopyOption.ATOMIC_MOVE);
		
//		long size(Path path) : 返回 path 指定文件的大小
		long size = Files.size(path2);
		System.out.println(size);

	}

	@Test
	public void test2() throws IOException{
		Path path1 = Paths.get("d:\\nio", "hello.txt");
		Path path2 = Paths.get("atguigu.txt");
//		boolean exists(Path path, LinkOption … opts) : 判断文件是否存在
		System.out.println(Files.exists(path2, LinkOption.NOFOLLOW_LINKS));

//		boolean isDirectory(Path path, LinkOption … opts) : 判断是否是目录
		//不要求此path对应的物理文件存在。
		System.out.println(Files.isDirectory(path1, LinkOption.NOFOLLOW_LINKS));

//		boolean isRegularFile(Path path, LinkOption … opts) : 判断是否是文件

//		boolean isHidden(Path path) : 判断是否是隐藏文件
		//要求此path对应的物理上的文件需要存在。才可判断是否隐藏。否则，抛异常。
//		System.out.println(Files.isHidden(path1));

//		boolean isReadable(Path path) : 判断文件是否可读
		System.out.println(Files.isReadable(path1));
//		boolean isWritable(Path path) : 判断文件是否可写
		System.out.println(Files.isWritable(path1));
//		boolean notExists(Path path, LinkOption … opts) : 判断文件是否不存在
		System.out.println(Files.notExists(path1, LinkOption.NOFOLLOW_LINKS));
	}

	/**
	 * StandardOpenOption.READ:表示对应的Channel是可读的。
	 * StandardOpenOption.WRITE：表示对应的Channel是可写的。
	 * StandardOpenOption.CREATE：如果要写出的文件不存在，则创建。如果存在，忽略
	 * StandardOpenOption.CREATE_NEW：如果要写出的文件不存在，则创建。如果存在，抛异常
	 *
	 * @author shkstart 邮箱：shkstart@126.com
	 * @throws IOException
	 */
	@Test
	public void test3() throws IOException{
		Path path1 = Paths.get("d:\\nio", "hello.txt");

//		InputStream newInputStream(Path path, OpenOption…how):获取 InputStream 对象
		InputStream inputStream = Files.newInputStream(path1, StandardOpenOption.READ);

//		OutputStream newOutputStream(Path path, OpenOption…how) : 获取 OutputStream 对象
		OutputStream outputStream = Files.newOutputStream(path1, StandardOpenOption.WRITE,StandardOpenOption.CREATE);


//		SeekableByteChannel newByteChannel(Path path, OpenOption…how) : 获取与指定文件的连接，how 指定打开方式。
		SeekableByteChannel channel = Files.newByteChannel(path1, StandardOpenOption.READ,StandardOpenOption.WRITE,StandardOpenOption.CREATE);

//		DirectoryStream<Path>  newDirectoryStream(Path path) : 打开 path 指定的目录
		Path path2 = Paths.get("e:\\teach");
		DirectoryStream<Path> directoryStream = Files.newDirectoryStream(path2);
		Iterator<Path> iterator = directoryStream.iterator();
		while(iterator.hasNext()){
			System.out.println(iterator.next());
		}
	}
}

```

## 使用第三方jar包实现文件读写

(开发中常用)

apache-common包

在Module目录右击，文件夹libs，将commons-io-2.5.jar复制进来，现在还不能用。

还需要右键jar包，Add as Library(添加为库)	，确定

```java
package com.loong.commons_io;
import org.apache.commons.io.FileUtils;
import java.io.File;
import java.io.IOException;
public class FileUtilsTest {
    public static void main(String[] args) {
        try {
            FileUtils.copyFile(new File("hello.txt"), new File("hellocopy.txt"));
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

# 第14章 网络编程

## 网络编程概述

Java提供的网络类库，可以实现无痛的网络连接，联网的底层细节被隐藏在 Java 的本机安装系统里，由 JVM 进行控制。并且 Java 实现了一个跨平台的网络库，程序员面对的是一个统一的网络编程环境。

前置知识《计算机网络》：网络的概念和分类，IP地址的表示和分类、域名、url和HTTP协议、端口号（记住常见的端口号） 、网络通信协议以及对应的哪一层、TCP和UDP 等

网络编程的目的：直接或间接地通过网络协议与其它计算机实现数据交换，进行通讯。


网络编程中有两个主要的问题：
* 如何准确地定位网络上一台或多台主机（IP）；定位主机上的特定的应用(端口)
* 找到主机后如何可靠高效地进行数据传输（网络通信协议）


网络通信要素： ①IP和端口号；②网络通信协议

## 通信要素1：IP和端口号

### IP

唯一的标识 Internet 上的计算机（通信实体）

 (略) ip分类 私有地址 回环地址127.0.0.1 主机名localhost、

ip不易记忆  域名

**在Java中使用InetAddress类代表IP**

### 端口号

端口号标识正在计算机上运行的进程（程序）
* 不同的进程有不同的端口号
* 被规定为一个 16 位的整数 0~65535。
* 端口分类：
 公认端口：0~1023。被预先定义的服务通信占用
（如：**HTTP占用端口80，https 443，FTP占用端口21，ssh 22**，Telnet占用端口23，smtp 25）
 注册端口：1024~49151。分配给用户进程或应用程序。
（如：**Tomcat占用端口8080，MySQL占用端口3306，Oracle占用端口1521，sqlserber占用1433**等）。
 动态/私有端口：49152~65535。


* **端口号与IP地址的组合得出一个网络套接字：Socket。**

### InetAddress类
在Java中使用InetAddress类代表IP，此类的一个对象就代表着一个具体的IP地址

实例化：getByName(String host) 、 getLocalHost()
常用方法：getHostName() / getHostAddress()

代码示例
```java
  public static void main(String[] args) {
        try {
            InetAddress inet1 = InetAddress.getByName("192.168.1.1");
            System.out.println(inet1);
            InetAddress inet2 = InetAddress.getByName("localhost");
            System.out.println(inet2);
            InetAddress inet3 = InetAddress.getLocalHost();//返回本地主机
            System.out.println(inet3);
            InetAddress inet4 = InetAddress.getByName("www.baidu.com");
            System.out.println(inet4);
            System.out.println("hostname:"+inet4.getHostName()+" hostaddress:"+ inet1.getHostAddress());
        } catch (UnknownHostException e) {//未知主机异常
            e.printStackTrace();
        }
        /*输出:
        /192.168.1.1
        localhost/127.0.0.1
        DESKTOP-2T3P0TO/192.168.192.1
        www.baidu.com/180.101.49.11
        hostname:www.baidu.com hostaddress:192.168.1.1
         */
    }
```


## 通信要素2：网络协议

![各层对应的协议.png](http://101.34.218.64/JavaSE.assets/%E5%90%84%E5%B1%82%E5%AF%B9%E5%BA%94%E7%9A%84%E5%8D%8F%E8%AE%AE.png)

### TCP 和 UDP的区别：

* TCP协议：传输控制协议
 使用TCP协议前，须先建立TCP连接，形成传输数据通道
 传输前，采用“三次握手”方式，点对点通信，**是可靠的**
 TCP协议进行通信的两个应用进程：客户端、服务端。
 在连接中可进行**大数据量的传输**
 传输完毕，需**释放已建立的连接，效率低**
* UDP协议：用户数据报协议
 将数据、源、目的封装成数据包，**不需要建立连接**
 每个数据报的大小限制在64K内
 发送不管对方是否准备好，接收方收到也不确认，故是不可靠的
 可以广播发送
 发送数据结束时**无需释放资源，开销小，速度快**

### TCP三次握手 建立连接

![TCP三次握手](http://101.34.218.64/JavaSE.assets/TCP%E4%B8%89%E6%AC%A1%E6%8F%A1%E6%89%8B.png)

### TCP四次挥手 释放连接

![TCP四次挥手](http://101.34.218.64/JavaSE.assets/TCP%E5%9B%9B%E6%AC%A1%E6%8C%A5%E6%89%8B.png)

## 套接字Socket和Socket类(重要)

网络编程 也叫Socket通信，Socket编程

### 套接字(Socket)
* 利用套接字(Socket)开发网络应用程序早已被广泛的采用，以至于成为事实上的标准。
* 网络上具有唯一标识的IP地址和端口号组合在一起才能构成唯一能识别的标识符套接字。
* 通信的两端都要有Socket，是两台机器间通信的端点。
* 网络通信其实就是Socket间的通信。
* Socket允许程序把网络连接当成一个流，数据在两个Socket间通过IO传输。
* 一般主动发起通信的应用程序属客户端，等待通信请求的为服务端。

* Socket分类：
    **流套接字（stream socket）：使用TCP提供可依赖的字节流服务**
    **数据报套接字（datagram socket）：使用UDP提供“尽力而为”的数据报服务**

### Socket类

常用构造器：
* public Socket(InetAddress address,int port)创建一个流套接字并将其连接到指定 IP 地址的指定端口号。
* public Socket(String host,int port)创建一个流套接字并将其连接到指定主机上的指定端口号。

常用方法：
* public InputStream getInputStream()返回此套接字的输入流。可以用于接收网络消息
* public OutputStream getOutputStream()返回此套接字的输出流。可以用于发送网络消息
* public InetAddress getInetAddress()此套接字连接到的远程 IP 地址；如果套接字是未连接的，则返回 null。
* public InetAddress getLocalAddress()获取套接字绑定的本地地址。 即本端的IP地址
* public int getPort()此套接字连接到的远程端口号；如果尚未连接套接字，则返回 0。
* public int getLocalPort()返回此套接字绑定到的本地端口。 如果尚未绑定套接字，则返回 -1。即本端的端口号。
* public void close()关闭此套接字。套接字被关闭后，便不可在以后的网络连接中使用（即无法重新连接或重新绑定）。需要创建新的套接字对象。 关闭此套接字也将会关闭该套接字的 InputStream 和OutputStream。
* public void shutdownInput()如果在套接字上调用 shutdownInput() 后从套接字输入流读取内容，则流将返回 EOF（文件结束符）。 即不能在从此套接字的输入流中接收任何数据。
* public void shutdownOutput()禁用此套接字的输出流。对于 TCP 套接字，任何以前写入的数据都将被发送，并且后跟 TCP 的正常连接终止序列。 如果在套接字上调用 shutdownOutput() 后写入套接字输出流，则该流将抛出 IOException。 即不能通过此套接字的输出流发送任何数据。

## TCP网络编程

Java语言的基于套接字编程分为服务端编程和客户端编程。

基于Socket的TCP编程 通信模型

![基于TCP的Socket通信](http://101.34.218.64/JavaSE.assets/%E5%9F%BA%E4%BA%8ETCP%E7%9A%84Socket%E9%80%9A%E4%BF%A1.png)



### 使用Socket类实现

![网络编程](http://101.34.218.64/JavaSE.assets/%E7%BD%91%E7%BB%9C%E7%BC%96%E7%A8%8B.png)

### 例1 发送消息c->s

```java
//TCP网络编程
    //示例 客户端发送信息给服务端 服务的将数据显示在控制台
    //先运行server()(会侦听连接，阻塞) ，再运行client()，然后在server的控制台看输出
public class TCPTest {
    @Test
    public void client(){//客户端
        Socket socket = null;
        OutputStream os = null;
        try {
          //1.创建Socket 对象 指明服务器端的ip和端口
            //构造器Socket(InetAddress address,int port)
            //InetAddress inet = InetAddress.getByName("127.0.0.1");//服务端的。 这里用本机演示
            //Socket socket = new Socket(inet,8899);

            //构造器Socket(String host,int port)
            socket = new Socket("127.0.0.1",8899);
            //2.获取一个输出流，用于输出数据
            os = socket.getOutputStream();//返回此套接字的输出流。可以用于发送网络消息
            //3.写出数据
            os.write("你好，我是客户端mm".getBytes());
              //这里发送完直接关闭流和套接字了，就没用上socket.shutdownOutput();
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            //4.关闭资源
            if(os!=null) {
                try {
                    os.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
            if(socket!=null) {
                try {
                    socket.close();//socket也需要关流
                    //关闭socket,不再和服务器通信  
                    //可以只关socket, socket.getXXX到的相应的InputStream、OutputStream也自动关闭了
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
        }

    }

    @Test
    public void server(){
        ServerSocket ss= null;//ServerSocket 此类实现服务器套接字
        Socket socket= null;
        InputStream is = null;
        ByteArrayOutputStream baos = null;
        try {
            //1.创建ServerSocket 指明自己的端口号
            ss = new ServerSocket(8899);
            //2.调用accept()接收来自客户端的socket
            socket = ss.accept();//侦听并接受到此套接字的连接。此方法在连接传入之前一直阻塞。（ 返回来自客户端连接的套接字）
            //3.获取输入流
            is = socket.getInputStream();
            //4.读取输入流中的数据
            //会乱码 不建议
//        byte[] buffer = new byte[1024];
//        int len;
//        while((len=is.read(buffer))!=-1){
//            String str = new String(buffer,0,len);
//            System.out.println(str);
//        }
            baos = new ByteArrayOutputStream();
            byte[] buffer = new byte[5];
            int len;
            while((len=is.read(buffer))!=-1){
                baos.write(buffer,0,len);
            }
            System.out.println("收到了来自于"+socket.getInetAddress().getHostAddress()+"的数据:");
            System.out.println(baos.toString());
			
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            //5.关闭资源
            if (baos != null) {
                try {
                    baos.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
            if (is != null) {
                try {
                    is.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
            if (socket != null) {
                try {
                    socket.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
            if (ss != null) {
                try {
                    ss.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
        }
        /*
        收到了来自于127.0.0.1的消息:
        你好，我是客户端mm
         */
    }
}
```

### 例2 发送文件c->s

```java
//示例2：客户端发送文件给服务端，服务端将文件保存在本地。
//(应该用try-catch-finally处理异常，这里简单写写)
public class TCPTest2 {
    @Test
    public void client() throws IOException {
        Socket socket = new Socket("127.0.0.1", 9090);
        FileInputStream fis = new FileInputStream("E:\\java学习\\面向对象.png");//最好用缓冲流包一下
        OutputStream os = socket.getOutputStream();
        byte[] buffer = new byte[1024];
        int len;
        while ((len = fis.read(buffer)) != -1) {
            os.write(buffer, 0, len);
        }
          //这里发送完直接关闭流和套接字了，就没用上socket.shutdownOutput();
        if (os != null) os.close();
        if (fis != null) fis.close();
        if (socket != null) socket.close();
        
    }
    @Test
    public void server() throws IOException {
        ServerSocket ss = new ServerSocket(9090);
        Socket socket= ss.accept();
        InputStream is = socket.getInputStream();

        FileOutputStream fos = new FileOutputStream("面向对象.jpg");
        byte[] buffer = new byte[1024];
        int len;
        while ((len=is.read(buffer))!=-1){
            fos.write(buffer,0,len);
        }

        if(fos!=null)fos.close();
        if(is!=null) is.close();
        if(socket!=null) socket.close();
        if(ss!=null) ss.close();
    }
}
```

### 例3 发送文件c->s,返回消息s->c

> 半关闭 (half-close) 提供了这样一种能力：套接字连接的一端可以终止其输出 ， 同时仍旧可以接收来自另一端的数据。
> 这是一种很典型的情况 ， 例如我们在向服务器传输数据， 但是一开始并不知道要传输多少数据。 在向文件写数据时 ， 我们只需在数据写入后关闭文件即可。 但是 ， 如果关闭一个套接字 ， 那么与服务器的连接将立刻断开 ， 因而也就无法读取服务器的响应了。
> 使用**半关闭**的方法就可以解决上述问题 。 可以通过**关闭一个套接字的输出流来表示发送给服务器的请求数据已经结束 ， 但是必须保持输入流处于打开状态**。
>
> 服务器端将读取输入信息， 直至到达输入流的结尾 ， 然后它再发送响应。
> 当然 ，该协议只适用于一站式 (one-shot) 的服务 ， 例如 HTTP 服务 ， 在这种服务中 ， 客户端连接服务器 ， 发送一个诮求 ， 捕获响应信息 ， 然后断开连接。
> • void shutdownOutput () 1. 3
> 将输出流设为“流结束" 。
> •void shutdownlnput() 1. 3
> 将输入流设为“流结束" 。
> • boolean i sOutputShutdown () 1. 4
> 如果输出已被关闭 ， 则返同 true。
> • boolean is Input Shutdown () 1. 4
> 如果输入已被关闭 ， 则返回 true 。
>
> (《java核心技术Ⅱ》)

```java
//从客户端发送文件给服务端，服务端保存到本地。并返回“发送成功”给客户端。并关闭相应的连接
public class TCPTest3 {
    @Test
    public void client() throws IOException {
        Socket socket = new Socket("127.0.0.1", 9090);
        FileInputStream fis = new FileInputStream("E:\\java学习\\面向对象.png");//最好用缓冲流包一下
        OutputStream os = socket.getOutputStream();
        byte[] buffer = new byte[1024];
        int len;
        while ((len = fis.read(buffer)) != -1) {
            os.write(buffer, 0, len);
        }
        //----------------------
        //没有下面这句，服务器的read()会阻塞。读不到末尾，不能返回-1.
        // read()是一个阻塞方法 在输入数据可用、检测到流末尾或者抛出异常前，此方法一直阻塞。
        //前面两个例子因为关闭了流和套接字 导致输入数据不可用，故read未阻塞
        socket.shutdownOutput();//将输出流设为”流的末尾“。这样服务器read()就不会堵塞了 可以读到-1
        //接收服务器的消息
        InputStream is = socket.getInputStream();
        ByteArrayOutputStream baos = new ByteArrayOutputStream();
        while ((len = is.read(buffer)) != -1) {
            baos.write(buffer, 0, len);
        }
        System.out.print(baos.toString());//发送成功

        if (baos!=null)baos.close();
        if(is!=null)is.close();
        //--------------------
        if (os != null) os.close();
        if (fis != null) fis.close();
        if (socket != null) socket.close();
    }
    @Test
    public void server() throws IOException {
        ServerSocket ss = new ServerSocket(9090);
        Socket socket= ss.accept();
        InputStream is = socket.getInputStream();

        FileOutputStream fos = new FileOutputStream("面向对象.jpg");
        byte[] buffer = new byte[1024];
        int len;
        while ((len=is.read(buffer))!=-1){
            fos.write(buffer,0,len);
        }
        System.out.println("图片接收完成");
        //-------------------
        //返回客户端消息”发送成功“
        OutputStream os = socket.getOutputStream();
        os.write("发送成功".getBytes());

        if(os!=null)os.close();
        //----------------------
        if(fos!=null)fos.close();
        if(is!=null) is.close();
        if(socket!=null) socket.close();
        if(ss!=null) ss.close();
    }
    //服务端控制台：图片接收完成
    //客户端控制台：发送完成
}
```

### 访问Tomcat服务器

* 客户端：
浏览器或自定义一个客户端
* 服务端：
Tomcat等服务器或自定义一个服务器

cs架构数据访问体系示意图:

![cs架构数据访问体系](http://101.34.218.64/JavaSE.assets/cs%E6%9E%B6%E6%9E%84%E6%95%B0%E6%8D%AE%E8%AE%BF%E9%97%AE%E4%BD%93%E7%B3%BB.png)

apache-tomcat装好 见“尚硅谷\_宋红康\_Tomcat快速部署.pdf"

”catalina run 运行
访问http://localhost:8080

资源放在webapps。 在examples放hello.txt内容"你好"保存utf-8
访问http://localhost:8080/examples/hello.txt可以读取

后面学web会深入学习

## UDP网络编程(了解)

（Socket类也可以实现UDP，但是其中关于UDP的方法已过时。 使用 DatagramSocket 取代 UDP 传输。）

类 DatagramSocket 和 DatagramPacket 实现了基于 UDP 协议网络程序。
* UDP数据报通过数据报套接字 DatagramSocket 发送和接收，系统不保证UDP数据报一定能够安全送到目的地，也不能确定什么时候可以抵达。
* DatagramPacket 对象封装了UDP数据报，在数据报中包含了发送端的IP地址和端口号以及接收端的IP地址和端口号。

* UDP协议中**每个数据报都给出了完整的地址信息**，因此**无须建立发送方和接收方的连接**。如同发快递包裹一样。(**发送端与接收端是两个独立的运行程序**)

### DatagramSocket 类的常用方法
构造方法
* public DatagramSocket(int port)创建数据报套接字并将其绑定到本地主机上的指定端口。套接字将被绑定到通配符地址，IP 地址由内核来选择。
* public DatagramSocket(int port,InetAddress laddr)创建数据报套接字，将其绑定到指定的本地地址。本地端口必须在 0 到 65535 之间（包括两者）。如果 IP 地址为 0.0.0.0，套接字将被绑定到通配符地址，IP 地址由内核选择。

普通方法
* public void close()关闭此数据报套接字。
* public void **send(DatagramPacket p)**从此套接字发送数据报包。DatagramPacket 包含的信息指示：将要发送的数据、其长度、远程主机的 IP 地址和远程主机的端口号。
* public void **receive(DatagramPacket p)**从此套接字接收数据报包。当此方法返回时，DatagramPacket的缓冲区填充了接收的数据。数据报包也包含发送方的 IP 地址和发送方机器上的端口号。 此方法在接收到数据报前一直阻塞。数据报包对象的 length 字段包含所接收信息的长度。如果信息比包的长度长，该信息将被截短。
* public InetAddress getLocalAddress()获取套接字绑定的本地地址。
* public int getLocalPort()返回此套接字绑定的本地主机上的端口号。
* public InetAddress getInetAddress()返回此套接字连接的地址。如果套接字未连接，则返回 null。
* public int getPort()返回此套接字的端口。如果套接字未连接，则返回 -1。

### DatagramPacket类的常用方法
* public DatagramPacket(byte[] buf,int length)构造 DatagramPacket，用来接收长度为 length 的数据包。 length 参数必须小于等于 buf.length。
* public **DatagramPacket**(byte[] buf,int length,InetAddress address,int port)构造数据报包，用来将长度为 length 的包发送到指定主机上的指定端口号。length参数必须小于等于 buf.length。
* public InetAddress getAddress()返回某台机器的 IP 地址，此数据报将要发往该机器或者是从该机器接收到的。
* public int getPort()返回某台远程主机的端口号，此数据报将要发往该主机或者是从该主机接收到的。
* public byte[] **getData**()返回数据缓冲区。接收到的或将要发送的数据从缓冲区中的偏移量 offset 处开始，持续 length 长度。
* public int **getLength**()返回将要发送或接收到的数据的长度。

### 流 程：

1. DatagramSocket与DatagramPacket
2. 建立发送端，接收端
3. 建立数据包
4. 调用Socket的发送、接收方法
5. 关闭Socket

### 代码示例

```java
//先receiver再sender。
//TCP如果接收端(服务端)没运行，发送端连接失败。connection refused (握手失败)
//UDP如果接收端没运行，发送端仍然可以正常发送。只是没人接受而已
public class UDPTest1 {
    @Test
    public void sender() {
        DatagramSocket ds = null;
        try {
            ds = new DatagramSocket();
            String str = "你好";
            byte[] data = str.getBytes();
            InetAddress inet = InetAddress.getByName("127.0.0.1");//对方的地址
            //构造器DatagramPacket(byte buf[], int offset, int length, InetAddress address, int port)
            DatagramPacket dp = new DatagramPacket(data, 0, data.length, inet, 9900);//数据报包

            ds.send(dp);//发送数据
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            if (ds != null) ds.close();
        }
    }

    @Test
    public void receiver() {
        DatagramSocket socket = null;
        try {
            socket = new DatagramSocket(9900);//在接收端，要指定监听的端口!!
            byte[] buffer = new byte[100];
            DatagramPacket packet = new DatagramPacket(buffer, 0, buffer.length);
            socket.receive(packet);//接收
            System.out.println(new String(packet.getData(), 0, packet.getLength()));
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            if (socket != null) socket.close();
        }
    }
}
```

```java
public class UDPTest2 {
    @Test
    public void sender(){
        DatagramSocket ds = null;
        try {
            ds = new DatagramSocket();
            byte[] by = "hello,atguigu.com".getBytes();
            DatagramPacket dp = new DatagramPacket(by, 0, by.length,
                    InetAddress.getByName("127.0.0.1"), 10000);
            ds.send(dp);
        } catch (Exception e) {
            e.printStackTrace();
        } finally {
            if (ds != null)
                ds.close();
        }
    }

    @Test
    public void receiver(){
        DatagramSocket ds = null;
        try {
            ds = new DatagramSocket(10000);
            byte[] by = new byte[1024];
            DatagramPacket dp = new DatagramPacket(by, by.length);
            ds.receive(dp);
            String str = new String(dp.getData(), 0, dp.getLength());
            System.out.println(str + "--" + dp.getAddress());
        } catch (Exception e) {
            e.printStackTrace();
        } finally {
            if (ds != null)
                ds.close();
        }
    }
}
```

## URL编程(了解 web部分细讲)

URL(Uniform Resource Locator)：统一资源定位符，它表示 Internet 上某一资源的地址。

**==URL的基本结构由5部分组成==**：
<传输协议>://<主机名>:<端口号>/<文件名>#片段名?参数列表

* 例如:
`http://192.168.1.100:8080/helloworld/index.jsp#a?username=shkstart&password=123`
`#片段名`：即锚点，例如看小说，直接定位到章节
`参数列表格式`：参数名=参数值&参数名=参数值....

### URL类
为了表示URL，java.net 中实现了类 URL。
构造器（注意：URL类的构造器都声明抛出非运行时异常，必须要对这一异常进行处理，通常是用 try-catch 语句进行捕获。）

* public **URL (String spec)**：通过一个表示URL地址的字符串可以构造一个URL对象。
例如：URL url = new URL ("http://www. atguigu.com/");
* public **URL(URL context, String spec)**：通过基 URL 和相对 URL 构造一个 URL 对象。
例如：URL downloadUrl = new URL(url, “download.html")
* public URL(String protocol, String host, String file); 
例如：new URL("http","www.atguigu.com", "download. html");
* public URL(String protocol, String host, int port, String file); 
例如: URL gamelan = new URL("http", "www.atguigu.com", 80, “download.html");

常用方法
一个URL对象生成后，其**属性是不能被改变**的，但可以通过它给定的方法来获取这些属性：
* public String getProtocol( ) 获取该URL的协议名
* public String getHost( )获取该URL的主机名
* public String getPort( )获取该URL的端口号
* public String **getPath**( )获取该URL的文件路径
* public String getFile( )获取该URL的文件名
* public String **getQuery**( ) 获取该URL的查询名（参数列表）

```java
    URL url = null;
    try {
        url = new URL("http://localhost:8080/examples/myTest.txt?username=Tom");
    } catch (MalformedURLException e) {
        e.printStackTrace();
    }
    System.out.println(url.getProtocol());//http
    System.out.println(url.getHost());//localhost
    System.out.println(url.getPort());//8080
    System.out.println(url.getPath());// /examples/myTest.txt
    System.out.println(url.getFile());// /examples/myTest.txt
    System.out.println(url.getQuery());//username=Tom  如果没有，返回null
```


### 针对HTTP协议的URLConnection类
URL的方法 openStream()：能从网络上读取数据 。若希望输出数据，例如向服务器端的 CGI （公共网关接口-Common GatewayInterface-的简称，是用户浏览器和服务器端的应用程序进行连接的接口）程序发送一些数据，则必须先与URL建立连接，然后才能对其进行读写，此时需要使用URLConnection 。

URLConnection：表示到URL所引用的远程对象的连接。当与一个URL建立连接时，首先要在一个 URL 对象上通过方法 openConnection() 生成对应的 URLConnection对象。如果连接过程失败，将产生IOException.
```
URL netchinaren = new URL ("http://www.atguigu.com/index.shtml");
URLConnectonn u = netchinaren.openConnection( );
```
通过URLConnection对象获取的输入流和输出流，即可以与现有的CGI
程序进行交互。
public Object getContent( ) throws IOException
public int getContentLength( )
public String getContentType( )
public long getDate( )
public long getLastModified( )
public InputStream **getInputStream**( )throws IOException
public OutputSteram getOutputStream( )throws IOException


> URI、URL和URN的区别
> URI，是uniform resource identifier，统一资源标识符，用来唯一的标识一个资源。
> URL是uniform resource locator，统一资源定位符，它是一种具体的URI，即URL可以用来标识一个资源，而且还指明了如何locate这个资源。
> URN，uniform resource name，统一资源命名，是通过名字来标识资源，比如mailto:java-net@java.sun.com。
>
> 也就是说，URI是以一种抽象的，高层次概念定义统一资源标识，而URL和URN则是具体的资源标识的方式。URL和URN都是一种URI。
>
> 在Java的URI中，一个URI实例可以代表绝对的，也可以是相对的，只要它符合URI的语法规则。
> 而URL类则不仅符合语义，还包含了定位该资源的信息，因此它不能是相对的。

### 代码示例

```java
//可以读取、下载对应的url资源：
public static void main(String[] args) {
    HttpURLConnection urlConnection = null;
    InputStream is = null;
    FileOutputStream fos = null;
    try {
        URL url = new URL("http://localhost:8080/examples/beauty.jpg");
        urlConnection = (HttpURLConnection) url.openConnection();
        urlConnection.connect();
        is = urlConnection.getInputStream();
        fos = new FileOutputStream("day10\\beauty3.jpg");

        byte[] buffer = new byte[1024];
        int len;
        while((len = is.read(buffer)) != -1){
            fos.write(buffer,0,len);
        }

        System.out.println("下载完成");
    } catch (IOException e) {
        e.printStackTrace();
    } finally {
        //关闭资源
        if(is != null){
            try {
                is.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
        if(fos != null){
            try {
                fos.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
        if(urlConnection != null){
            urlConnection.disconnect();
        }
    }
}
```

# 第15章 反射(重要)

reflection

（本章“获取Class实例”、“创建运行时类的对象”、“调用运行时类的指定结构” 要会写代码 特别是调用运行时类的指定结构。）

反射 在框架底层和设计模式中经常用到。**框架 = 反射 + 注解 + 设计模式**。

## Java反射机制概述

Java Reflection
* Reflection（反射）是被视为**动态语言的关键**。反射机制允许程序**在执行期**借助于Reflection API**取得任何类的内部信息**，**并能直接操作任意对象的内部属性及方法**。
> 补充：动态语言 vs 静态语言
> 1、动态语言
> 是一类在运行时可以改变其结构的语言：例如新的函数、对象、甚至代码可以被引进，已有的函数可以被删除或是其他结构上的变化。通俗点说就是在运行时代码可以根据某些条件改变自身结构。
> 主要动态语言：Object-C、C#、JavaScript、PHP、Python、Erlang。
> 2、静态语言
> 与动态语言相对应的，运行时结构不可变的语言就是静态语言。如Java、C、C++。
>
> **Java是静态语言**不是动态语言，但Java可以称之为“准动态语言”。即Java有一定的动态性，我们可以利用反射机制、字节码操作获得**类似动态语言的特性**。Java的动态性让编程的时候更加灵活！

* 加载完类之后，在堆内存的方法区中就产生了一个**Class类型的对象（一个类只有一个Class对象）**，这个对象就包含了完整的类的结构信息。我们**可以通过这个对象看到类的结构**。这个对象就像一面镜子，透过这个镜子看到类的结构，所以，形象的称之为：**反射**。

  例：正常方式：引入需要的”包类”名称——》通过new实例化——》取得实例化对象
  反射方式：实例化对象——》getClass()方法——》得到完整的“包类”名称

### Java反射机制提供的功能

* 在运行时判断任意一个对象所属的类
* 在运行时构造任意一个类的对象
* 在运行时判断任意一个类所具有的成员变量和方法
* 在运行时获取泛型信息
* 在运行时调用任意一个对象的成员变量和方法
* 在运行时处理注解
* 生成动态代理

### 反射相关的主要API
**java.lang.Class**:代表一个类。**反射的源头**。(**Class类的对象(一个类)叫做“运行实例”**)  
java.lang.reflect.Method:代表类的方法
java.lang.reflect.Field:代表类的成员变量
java.lang.reflect.Constructor:代表类的构造器
更多。。。

> Class在lang包下，不用import。 其它的在子包下，仍需导入

### 先看一个示例

```java
public class  ReflectionTest {
    @Test
    public void testReflection() throws NoSuchMethodException, InvocationTargetException, InstantiationException, IllegalAccessException, NoSuchFieldException {
        //1.通过反射 创建对象
        Class clazz = Person.class;// 现在的Person类 叫做”运行实例“
        //冷知识：变量名“clazz”不是写错了，这是常见的一种习惯。是被用来代替"class“(class是一个保留字用来定义类)。源码里也有很多这么命名的。说英语的人(那些同时读英国英语和美国英语的人)习惯于把's‘和'z’调换一下。常用clazz或cls命名
        Constructor cons = clazz.getConstructor(String.class, int.class);//获取构造器
        Object obj = cons.newInstance("Tom", 12);
        Person p = (Person) obj;
        System.out.println(p);

        //2.通过反射，调用对象指定的属性和方法
        Field age = clazz.getDeclaredField("age");
        age.set(p, 10);
        System.out.println(p);

        Method show = clazz.getDeclaredMethod("show");//空参方法，写方法名。非空参的还可以加参数类型，可以获取重载方法。如(show,String.class,int.class)获取show(String,int)
        show.invoke(p);

        //3.使用反射，可以调用内部私有结构————特别之处！
        //比如 私有的构造器、方法、属性
        Constructor cons1 = clazz.getDeclaredConstructor(String.class);//获取private Person(String name )
        cons1.setAccessible(true);//为反射对象 构造器cons1设置可访问标志
        // void setAccessible(boolean flag)为反射对象设置可访问标志。 flag 为 true 表明屏蔽 Java 语言的访问检查，使得对象的私有属性也可以被査询和设置。
        Person p1 = (Person) cons1.newInstance("Jerry"); //调用private Person(String name )
        System.out.println(p1);

        Method showNation = clazz.getDeclaredMethod("showNation",String.class);//获取private String showNation(String nation)
        showNation.setAccessible(true);//为反射对象 方法showName设置可访问标志
        showNation.invoke(p1, "China");
        String nation = (String) showNation.invoke(p1,"China");//invoke的返回值是Object 要强转成showNation的1返回值类型String
        System.out.println(nation);

        Field name = clazz.getDeclaredField("name");//获取private String name;
        name.setAccessible(true);//为反射对象 属性name设置可访问标志
        name.set(p1, "Army");
        System.out.println(p1);
    }
    //输出：
    //Person{name='Tom', age=12}
    //Person{name='Tom', age=10}
    //你好，我是一个人
    //Person{name='Jerry', age=0}
    //我的国籍是：China
    //我的国籍是：China
    //Person{name='Army', age=0}
}

public class Person {
    private String name;//私有的属性
    public int age;

    public Person() {}
    private Person(String name ) {this.name = name;}//私有的构造器
    public Person(String name, int age) {this.name = name;this.age = age;}

    public void show(){System.out.println("你好，我是一个人");}

    private String showNation(String nation){//私有方法 带返回值
        System.out.println("我的国籍是：" + nation);
        return nation;
    }
//getter setter toString...
}
```

> 如何看待反射和封装性两个技术的应用
>
> 开发中一般还是用普通方式。而反射具有动态性，运行时和前端交互时会用到。

## 理解Class类 获取Class实例（重要）

> 在Object类中定义了方法`public final Class getClass()`，此方法将被所有子类继承，方法返回值的类型是一个Class类。Class类是Java反射的源头。
> 实际上所谓反射从程序的运行结果来看也很好理解，即：可以通过对象反射求出类的名称。

`java.lang.Class<T> `  (虽然是个泛型类，在大多数实际问题中， 可以忽略类型参数， 而使用原始的 Class 类)

> `Class` 类的实例表示正在运行的 Java 应用程序中的类和接口。枚举是一种类，注释是一种接口。每个数组属于被映射为  Class 对象的一个类，所有具有相同元素类型和维数的数组都共享该 `Class` 对象。基本的 Java  类型（`boolean`、`byte`、`char`、`short`、`int`、`long`、`float`  和 `double`）和关键字 `void` 也表示为 `Class` 对象。 
> 
> `Class` 没有公共构造方法。`Class` 对象是在加载类时由 Java 虚拟机以及通过调用类加载器中的  `defineClass` 方法自动构造的。 

对于每个类而言，JRE 都为其保留一个不变的 Class 类型的对象。一个 Class 对象包含了特定某个结构(class/interface/enum/annotation/primitive type/void/[])的有关信息。

### 对于Class类的理解

* Class本身也是一个类。”**描述类的类**“

* Class 对象只能由系统建立对象。（不是new出来的，是系统创建的）
  
> `Class` 没有公共构造方法。`Class` 对象是在加载类时由 Java 虚拟机以及通过调用类加载器中的  `defineClass` 方法自动构造的。 ——API文档

* **一个加载的类在 JVM 中只会有一个Class实例**（一个类只有一个Class对象。因为类只加载一次。接口、数组也属于类）

* **一个Class对象对应的是一个加载到JVM中的一个.class文件**
 > 类的加载过程：(宋红康总结)
 > 程序经过javac.exe命令以后，会生成一个或多个字节码文件(.class结尾)。
 > 使用java.exe命令对某个字节码文件进行解释运行。相当于将某个字节码文件加载到内存中。此过程就称为类的加载。
 > 加载到内存中的类，我们就称为运行时类，此运行时类，就作为Class的一个实例。
 >
 > 换句话说，**Class的实例就对应着一个运行时类。**
 > 加载到内存中的运行时类，会缓存一定的时间。在此时间之内，我们可以通过不同的方式来获取此运行时类。

* 每个类的实例都会记得自己是由哪个 Class 实例所生成  。（故可以 对象.getClass
* 通过Class可以完整地得到一个类中的所有被加载的结构
* Class类是Reflection的**根源**，针对任何你想动态加载、运行的类，唯有先获得相应的Class对象

### ==获取Class类的实例的方式==(四种）

1）前提：若已知具体的类，通过类的class属性获取，该方法最为安全可靠，程序性能最高
实例：Class clazz = String.class;
2）前提：已知某个类的实例，调用该实例的getClass()方法获取Class对象
实例：Class clazz = “www.atguigu.com”.getClass();
3）前提：已知一个类的全类名，且该类在类路径下，可通过Class类的静态方法forName()获取，可能抛出ClassNotFoundException
实例：Class clazz = Class.forName(“java.lang.String”);
4）其他方式(不做要求)
ClassLoader cl = this.getClass().getClassLoader();
Class clazz4 = cl.loadClass(“类的全类名”);

#### ==代码示例==

```java
    //获取Class实例的四种方式 需掌握前三种
    @Test
    public void howToGetClass() throws ClassNotFoundException {
        //方式1 调用运行时类的属性 前提：已知具体的类。 
        Class clazz1= Person.class;

        //方式2 通过运行时类的对象，调用getClass() 前提：已知某个类的实例
        Person P1 = new Person();//前提
        Class clazz2= P1.getClass();
        Class clazz22= "字符串".getClass();

        //方式3 Class类的静态方法forName("全类名")  前提：已知类的全类名(完全限定名)  即 包名.类名  ——这种方式更好的体现了动态性
        //static Class forName(String className)    返回指定类名className的 Class对象。可能抛出ClassNotFoundException
        Class clazz3 = Class.forName("com.loong.refiectiontest.Person");//IDEA里，这个方法""里敲Person会自动给出全类名 牛啊！
        Class clazz33 = Class.forName("java.lang.String");//""打String也会自动给出全类名

        //方式4 使用类的加载器Classloader (这种方式仅了解)
        ClassLoader cl = this.getClass().getClassLoader();
        Class clazz4 = cl.loadClass("com.loong.refiectiontest.Person");

        System.out.println(clazz1==clazz2 && clazz1==clazz3 && clazz1==clazz4);//true 这四种方式获取到的是同一个实例
        System.out.println(clazz1);//class com.loong.refiectiontest.Person
    }
```

#### 体会反射的动态性

```java
//体会反射的动态性
@Test
public void test() {

    for (int i = 0; i < 100; i++) {
        int num = new Random().nextInt(3);//0,1,2
        String classPath = "";
        switch (num) {
            case 0:
                classPath = "java.util.Date";
                break;
            case 1:
                classPath = "java.lang.Object";
                break;
            case 2:
                classPath = "com.loong.refiectiontest.Person";
                break;
        }

        try {
            Object obj = Class.forName(classPath).newInstance();
            System.out.println(obj);
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

#### 总结：创建类的对象的方式?

方式一：new + 构造器
方式二：要创建Xxx类的对象，可以考虑：Xxx、Xxxs、XxxFactory、XxxBuilder类中查看是否有静态方法的存在。可以调用其静态方法，创建Xxx对象。
方式三：通过反射

### Class实例可以是哪些结构

> `Class` 类的实例表示正在运行的 Java 应用程序中的类和接口。枚举是一种类。注释是一种接口。每个数组属于被映射为  Class 对象的一个类，所有具有相同元素类型和维数的数组都共享该 `Class` 对象。基本的 Java  类型（`boolean`、`byte`、`char`、`short`、`int`、`long`、`float`  和 `double`）和关键字 `void` 也表示为 `Class` 对象。 ——API文档

对于每个类(或接口)而言，JRE 都为其保留一个不变的 Class 类型的对象。一个 Class 对象包含了特定某个结构(**class/interface/enum/annotation/primitive type/void/[]**)的有关信息。

（1）class：外部类，成员(成员内部类，静态内部类)，局部内部类，匿名内部类
（2）interface：接口
（3）[]：数组
（4）enum：枚举
（5）annotation：注解@interface
（6）primitive type：基本数据类型
（7）void

```java
  Class c1 = Object.class;
  Class c2 = Comparable.class;
  Class c3 = String[].class;
  Class c4 = int[][].class;
  Class c5 = ElementType.class;//枚举
  Class c6 = Override.class;//注解
  Class c7 = int.class;
  Class c8 = void.class;
  Class c9 = Class.class;//Class也是一个类

  int[] a = new int[10];
  int[] b = new int[100];
  Class c10 = a.getClass();
  Class c11 = b.getClass();
// 只要元素类型与维度一样，就是同一个Class
  System.out.println(c10 == c11);//true
```

> 拓展 基本数据类型和void为什么有class这个属性 
>
>  java虚拟机会自动创建9个预先定义好的Class对象代表8个基本类型和void， 这些class和基本类型有相同的名字boolean, byte, char, short, int, long, float, double. 这8个基本类型的Class对象可以通过java.lang.Boolean.TYPE,java.lang.Integer.TYPE等来访问,同样可以通过int.class,boolean.class等来访问.
>
> https://bbs.csdn.net/topics/398350235/close

### Class类的常用方法

| 方法名                                            | 功能说明                                                     |
| ------------------------------------------------- | ------------------------------------------------------------ |
| static Class forName(String name)                 | 返回指定类名 name 的  Class 对象                             |
| Object newInstance()                              | 调用缺省构造函数，返回该Class对象的一个实例                  |
| getName()                                         | 返回此Class对象所表示的实体（类、接口、数组类、基本类型或void）名称 |
| Class getSuperClass()                             | 返回当前Class对象的父类的Class对象                           |
| Class [] getInterfaces()                          | 获取当前Class对象的接口                                      |
| ClassLoader getClassLoader()                      | 返回该类的类加载器                                           |
| Class getSuperclass()                             | 返回表示此Class所表示的实体的超类的Class                     |
| Constructor[] getConstructors()                   | 返回一个包含某些Constructor对象的数组                        |
| Field[] getDeclaredFields()                       | 返回Field对象的一个数组                                      |
| Method getMethod(String name,Class …  paramTypes) | 返回一个Method对象，此对象的形参类型为paramType              |

## 类的加载与ClassLoader的理解(了解)

仅了解 详见ppt

类的加载过程 三步

![类的加载过程.png](http://101.34.218.64/JavaSE.assets/%E7%B1%BB%E7%9A%84%E5%8A%A0%E8%BD%BD%E8%BF%87%E7%A8%8B.png)

![类的加载详解.png](http://101.34.218.64/JavaSE.assets/%E7%B1%BB%E7%9A%84%E5%8A%A0%E8%BD%BD%E8%AF%A6%E8%A7%A3.png)

![类加载器作用.png](http://101.34.218.64/JavaSE.assets/%E7%B1%BB%E5%8A%A0%E8%BD%BD%E5%99%A8%E4%BD%9C%E7%94%A8.png)

![类加载器的种类](http://101.34.218.64/JavaSE.assets/%E7%B1%BB%E5%8A%A0%E8%BD%BD%E5%99%A8%E7%9A%84%E7%A7%8D%E7%B1%BB.png)

```java
@Test
public void testClassLoader() throws ClassNotFoundException {
    //1.获取一个系统类加载器
    ClassLoader classloader = ClassLoader.getSystemClassLoader();
    System.out.println(classloader);//sun.misc.Launcher$AppClassLoader@18b4aac2
    //2.获取系统类加载器的父类加载器，即扩展类加载器
    classloader = classloader.getParent();
    System.out.println(classloader);//sun.misc.Launcher$ExtClassLoader@28a418fc
    //3.获取扩展类加载器的父类加载器，即引导类加载器
    classloader = classloader.getParent();
    System.out.println(classloader);//null
    //如果调用扩展类加载器的额getParent()是无法获取引导类加载器的。
    //引导类加载器主要负责加载java的核心类库，无法加载自定义类库

    //4.测试自定义类的类加载器 用的系统类加载器
    classloader = Class.forName("com.loong.refiectiontest.ReflectionTest").getClassLoader();
    classloader = ReflectionTest.class.getClassLoader();//这种更常见
    classloader = com.loong.refiectiontest.ReflectionTest.class.getClassLoader();//写全了
    System.out.println(classloader);//sun.misc.Launcher$AppClassLoader@18b4aac2
    //5.测试JDK提供的Object类由哪个类加载器加载 用的引导类加载器，获取不到
    classloader = Class.forName("java.lang.Object").getClassLoader();
    System.out.println(classloader);//null

    //*关于类加载器的一个主要方法：getResourceAsStream(String str):获取类路径下的指定文件的输入流
    InputStream in = null;
    in = this.getClass().getClassLoader().getResourceAsStream("exer2\\test.properties");
    System.out.println(in);
}
```

### getResourceAsStream方法(需掌握)

类加载器的一个主要方法：getResourceAsStream(String str):获取类路径下的指定文件的输入流  默认在Module的src下 

```java
    @Test
    public void testGetResourceAsStream() throws IOException {
        Properties pros = new Properties();

        //以前读properties的方式
//        FileInputStream fis = new FileInputStream("jdbc.properties");//jdbc.properties文件在module下
//        FileInputStream fis = new FileInputStream("ser\\jdbc1.properties");//jdbc1.properties文件在module下的src下
//        pros.load(fis);

        //现在的方式 使用类加载器的一个方法：getResourceAsStream(String str):获取类路径下的指定文件的输入流
        //默认properties文件在当前module的src下
        ClassLoader cl = ReflectionTest.class.getClassLoader();
        //InputStream is = cl.getResourceAsStream("jdbc.properties");//NullPointerException 读的是Module下的，而此方法默认在src下
        InputStream is = cl.getResourceAsStream("jdbc1.properties");//jdbc1.properties在src下
        pros.load(is);


        String user = pros.getProperty("user");
        String password = pros.getProperty("password");
        System.out.println("user="+user+" password="+password);
        ////开发中，properties文件在module下的src下
    }
```

启示：开发中，properties文件在module下的src下

## ==创建运行时类的对象==

### 方式一：**Class类对象调用newInstance()方法**

 (是**Class类中**的newInstance()方法，是空参的)
newInstance():调用此方法，创建对应的运行时类的对象。内部调用了运行时类的空参的构造器。
要想此方法正常的创建运行时类的对象，要求：**必须有 public 的无参构造**
1.**运行时类必须提供空参的构造器**。否则，InstantiationException
2.**空参的构造器的访问权限足够**。通常，设置为public。权限不够IllegalAccessException

```java
Class clazz = Person.class;
Object obj = clazz.newInstance();
Person p = (Person) obj;
```

### 方式二： **获取构造器实例**，通过**构造器实例调用newInstance(参数...)方法**

（是**Constructor类中的**newInstance(参数...)方法）
①通过Class类的**getDeclaredConstructor**(Class … parameterTypes)取得本类的指定形参类型的构造器
`Constructor<T> getDeclaredConstructor(Class<?>... parameterTypes)`
“指定形参类型”是可变形参，也可以用数组。指定形参类型用”xxx.class“。若0个参数则获取的是空参构造器。
如果没有这个构造器则NoSuchMethodException

②通过**Constructor实例调用newInstance**(Object ... initargs)创建对象 （是Constructor类中的newInstance(参数...)）
`public T newInstance(Object ... initargs)`
这个方法可以根据构造器传实参。构造器实例若是空参的则newInstance()，有参的就传实参

```java
Class clazz = Person.class;
Constructor cons1 = clazz.getDeclaredConstructor();//获取空参构造器
Constructor cons = clazz.getDeclaredConstructor(String.class, int.class);//获取构造器Person(String name, int age)

Object obj1 = cons1.newInstance();//相当于调用了Person()
Object obj = cons.newInstance("Tom", 12);//调用了Person(String name, int age)
Person p1 = (Person) obj;
Person p = (Person) obj;
```
注意：
1.在jdk1.9中因为Class类中的newInstance()方法会提示被弃用的方法。
替代方法getDeclatedConstructor().newInstance()即方式二。以后还是多用方式二吧！！
2.可以用`Class<T>`避免强转(看代码演示)，但是一般不用泛型

本节得到的启示：在javabean中要求提供一个public的空参构造器。原因：
1.便于通过反射，创建运行时类的对象
2.便于子类继承此运行时类时，默认调用super()时，保证父类此构造器

### 完整代码

```java
public class NewInstanceTest {
	//方式一
    @Test
    public void test1() throws InstantiationException, IllegalAccessException {
        Class clazz = Person.class;
        //方式一：Class类对象调用newInstance()方法  (是Class类中的newInstance()方法，是空参的)
        //newInstance():调用此方法，创建对应的运行时类的对象。内部调用了运行时类的空参的构造器。
        //要想此方法正常的创建运行时类的对象，要求：
        //1.运行时类必须提供空参的构造器。否则，InstantiationException
        //2.空参的构造器的访问权限足够。通常，设置为public。权限不够IllegalAccessException
        Object obj = clazz.newInstance();//newInstance()在1.9会提示被弃用的方法。替代方法getDeclatedConstructor().newInstance() 在jdk8里也可以用。见下面的方式二
        Person p = (Person) obj;
        System.out.println(p);

        Class<Person> clazz1 = Person.class;
        Person p1 = clazz1.newInstance();//Class的泛型 决定了newInstance的返回值 避免强转
        System.out.println(p);
    }
    //方式二
    @Test
    public void test2() throws NoSuchMethodException, InvocationTargetException, InstantiationException, IllegalAccessException {
        Class clazz = Person.class;
        //方式二 获取构造器实例，通过构造器调用newInstance(Object ... initargs)创建对象
        // ①通过Class类的getDeclaredConstructor(Class … parameterTypes)取得本类的指定形参类型的构造器
        //Constructor<T> getDeclaredConstructor(Class<?>... parameterTypes)
        //“指定形参类型”是可变形参，也可以用数组。指定形参类型用”xxx.class“。若0个参数则获取的是空参构造器。
        //如果没有这个构造器则NoSuchMethodException
        Constructor cons1 = clazz.getDeclaredConstructor();//获取空参构造器
        Constructor cons = clazz.getDeclaredConstructor(String.class, int.class);//获取构造器Person(String name, int age)
        //②通过Constructor实例调用newInstance(Object ... initargs)创建对象 （是Constructor类中的newInstance(参数...)）
        //public T newInstance(Object ... initargs)
        //这个方法
        Object obj1 = cons1.newInstance();//相当于调用了Person()
        Object obj = cons.newInstance("Tom", 12);//调用了Person(String name, int age)
        Person p = (Person) obj;
        System.out.println(p);

        //可以将①②合起来
        Object obj2=clazz.getDeclaredConstructor(String.class, int.class).newInstance("Tom",12);
    }
 }
```



## 获取运行时类的完整结构信息

当前运行时类的某一结构的全部。Field、Method、Constructor、Superclass、Interface、Annotation

还有包Package

本节了解 主要开发中常用到"获取运行时类的带泛型的父类 的泛型"、"获取运行时类实现的接口"

### **测试前的准备** 

```
com.loong.refiectiontest1包中有个结构丰富的Person类——用于测试
com.loong.refiectiontest2包的是测试方法
```

```java
package com.loong.refiectiontest1;
 //结构更加丰富的Person 有父类 有实现的接口 有注解 还有重写的方法 权限不同的属性、构造器、方法
@MyAnnotation(value = "Person的注解")
public class Person extends Creature<String> implements Comparable<String>,MyInterface{
    private String name;//私有的属性
    int age;//包权限
     public int id = 0;

    public Person() {}
     @MyAnnotation(value = "构造器Person(name)的注解")
    private Person(String name ) {this.name = name;}//私有的构造器
    Person(String name, int age) {this.name = name;this.age = age;}

     @MyAnnotation(value = "show方法的注解")
    private String show(String nation){System.out.println("我的国籍是：" + nation);return nation;}
    public String display(String interests){return interests;}

    public String getName() {return name;}
    public void setName(String name) {this.name = name;}
    public int getAge() {return age;}
    public void setAge(int age) {this.age = age;}
    @Override
    public String toString() {return "Person{" + "name='" + name + '\'' + ", age=" + age + '}';}
     @Override
     public void info() {System.out.println("我是一个人");}
     @Override
     public int compareTo(String o) {return 0;}
 }
```

```java
package com.loong.refiectiontest1;
import java.io.Serializable;
public class Creature<T> implements Serializable {
    private char gender;//性别
    public double weight;//体重
    private void breath(){System.out.println("生物呼吸");}
    public void eat(){System.out.println("生物吃东西");}
}
```

```java
package com.loong.refiectiontest1;
@Target({TYPE, FIELD, METHOD, PARAMETER, CONSTRUCTOR, LOCAL_VARIABLE})
@Retention(RetentionPolicy.RUNTIME)
public @interface MyAnnotation {
    String value() default "hello";
}
```

```java
package com.loong.refiectiontest1;
public interface MyInterface {
    void info();
}
```

### 获取当前运行时类的属性结构，以及Field类中方法介绍

全部的Field
* public Field[] getFields()返回此Class对象所表示的类或接口的public的Field。（包括父类的）
* public Field[] getDeclaredFields()返回此Class对象所表示的类或接口的(声明的)全部Field。（这个类中声明的。不包含父类中声明的方法

Field方法中：
* public int getModifiers() 以整数形式返回此Field的修饰符
* public Class<?> getType() 得到Field的属性类型
* public String getName() 返回Field的名称。

```java
//获取当前运行时类的属性结构
public class FieldTest {
    @Test
    public void test1(){//所有的属性
        Class clazz = Person.class;

        //getFields():获取当前运行时类及其父类中声明为public访问权限的属性
        Field[] fields=clazz.getFields();
        for (Field field:fields ) {
            System.out.println(field);
        }
        //输出： 权限  数据类型 变量名
        //public int com.loong.refiectiontest1.Person.id
        //public double com.loong.refiectiontest1.Creature.weight

        //getDeclaredFields():获取当前运行时类中声明的所属性。（不包含父类中声明的属性
        Field[] declaredFields = clazz.getDeclaredFields();
        for (Field field:declaredFields ) {
            System.out.println(field);
        }
        //输出
        //private java.lang.String com.loong.refiectiontest1.Person.name
        //int com.loong.refiectiontest1.Person.age
        //public int com.loong.refiectiontest1.Person.id
    }

    @Test
    public void testField(){//Field类中的方法
        Class clazz = Person.class;
        Field[] declaredFields = clazz.getDeclaredFields();
        for(Field f:declaredFields){
            //①取得修饰符: public int getModifiers();
            int modifiers = f.getModifiers();//返回一个表示修饰符的常量之和的整数。比如public final 返回PUBLIC+FINAL=1+16=17
            // 0是缺省，1是public,2是private... 在java.lang.reflect.Modifier中定义的常量。
            //可以调用Modifier中的静态方法toString(int mod) 转换成相应的字符串。如Modifier.toString(17)返回"public final"，Modifier.toString(0)返回""
            System.out.println(Modifier.toString(modifiers));
            //②取得数据类型public Class<?> getType()
            Class type = f.getType();//返回“class 包名.类名”或基本数据类型。 可使用getName()返回“包名.类名”或基本数据类型
            System.out.println(type.getName());
            //③取得变量名 public String getName()
            String name = f.getName();
            System.out.println(name);
            System.out.println("-------------");
        }
        /*输出：
        private
        java.lang.String
        name
        -------------

        int
        age
        -------------
        public
        int
        id
         */
    }
```



### 获取当前运行类的方法结构，以及Method类方法介绍

全部的方法
* public Method[] getDeclaredMethods()返回此Class对象所表示的类或接口的全部方法
* public Method[] getMethods()返回此Class对象所表示的类或接口的public的方法

Method类中：
* public Class<?> getReturnType()取得全部的返回值
* public Class<?>[] getParameterTypes()取得全部的参数
* public int getModifiers()取得修饰符
* public Class<?>[] getExceptionTypes()取得异常信息

```java
package com.loong.refiectiontest2
import com.loong.refiectiontest1.Person;

public class MethodTest {
    @Test
    public void test1(){
        Class clazz = Person.class;

        //getMethods():获取当前运行时类及其所父类中声明为public权限的方法
        Method[] methods = clazz.getMethods();
        for(Method m : methods){
            System.out.println(m);
        }
        System.out.println();
        //getDeclaredMethods():获取当前运行时类中声明的所有方法。（不包含父类中声明的方法
        Method[] declaredMethods = clazz.getDeclaredMethods();
        for(Method m : declaredMethods){
            System.out.println(m);
        }
        //权限修饰符 返回值类型 方法名(参数类型) throws 异常XxxException
    }

    @Test
    public void testMethod(){//Method中的方法
        Class clazz = Person.class;
        Method[] declaredMethods = clazz.getDeclaredMethods();
        for(Method m : declaredMethods){
            System.out.println("------"+m.getName()+"--------");
            //①获取方法的注解 (注意 只能获取生命周期RUNTIME的注解)
            System.out.println("注解：");
            Annotation[] annotations = m.getAnnotations();//源码还是调用getDeclaredAnnotations()
            for (Annotation anno : annotations) {
                System.out.println(anno);//@com.loong.refiectiontest1.MyAnnotation(value=show方法的注解)
            }
            //②获取方法的修饰符
            System.out.println("修饰符"+Modifier.toString(m.getModifiers()));
            //③获取方法的返回值类型
            System.out.println("返回值类型"+m.getReturnType().getName());
            //④获取方法的方法名
            System.out.println("方法名"+m.getName());
            //④获取方法的参数类型
            System.out.println("参数类型：");
            Class[] parameterTypes = m.getParameterTypes();//如果空参，返回长度为 0 的数组
            if(parameterTypes.length!=0){
                for (Class parameterType : parameterTypes) {
                    //System.out.println(parameterType);//class 包名.类名
                    System.out.println(parameterType.getName());//包名.类名
                }
            }
            //⑤获取方法的声明的异常
            System.out.println("异常：");
            Class[] exceptionTypes = m.getExceptionTypes();//若此方法没有在其 throws 子句中声明异常，则返回长度为 0 的数组
            for (Class exceptionType : exceptionTypes) {
                //System.out.println(exceptionType);//class 包名.类名
                System.out.println(exceptionType.getName());//包名.类名
            }
        }
    }
}
```

### 获取当前运行时类的构造器结构，以及Constructor类方法

全部的构造器
* public Constructor\<T\>[] getConstructors()返回此 Class 对象所表示的类的所有public构造方法。
* public Constructor\<T\>[] getDeclaredConstructors()返回此 Class 对象表示的类声明的所有构造方法。

Constructor类中：
* 取得修饰符: public int getModifiers();
* 取得方法名称: public String getName();
* 取得参数的类型：public Class<?>[] getParameterTypes();

```java
package com.loong.refiectiontest2;
import com.loong.refiectiontest1.Person;

public class ConstructorTest {
    @Test
    public void test() {
        Class clazz = Person.class;
        //getConstructors():获取当前运行时类中声明为public的构造器
        Constructor[] constructors = clazz.getConstructors();
        for (Constructor c : constructors) {
            System.out.println(c);
        }

        System.out.println();
        //getDeclaredConstructors():获取当前运行时类中声明的所有的构造器
        Constructor[] declaredConstructors = clazz.getDeclaredConstructors();
        for (Constructor c : declaredConstructors) {
            System.out.println(c);
        }
    }
}
//构造器也是方法，Constructor类中有和Method类中相同的方法可以获取注解、修饰符、方法名称、参数的类型。(没有throws异常)
```

### 获取运行时类的父类

* public Class<? Super T> getSuperclass()返回表示此 Class 所表示的实体（类、接口、基本类型）的父类的Class。

```java
package com.loong.refiectiontest2;
import com.loong.refiectiontest1.Person;

public class SuperClassTest {
    @Test
    public void testSuper(){
        Class clazz = Person.class;
        //获取运行时类的父类
        Class superclass = clazz.getSuperclass();
        System.out.println(superclass);//class com.loong.refiectiontest1.Creature
        System.out.println("----------------");
        //获取运行时类的带泛型的父类
        Type genericSuperclass = clazz.getGenericSuperclass();
        System.out.println(genericSuperclass);//com.loong.refiectiontest1.Creature<java.lang.String>
        System.out.println("-----------------");
        //获取运行时类的带泛型的父类 的泛型——应用场景举例 在学泛型时举例DAO的CustomerDAO里会有这样的需求
        ParameterizedType paramType = (ParameterizedType) genericSuperclass;//ParameterizedType 表示参数化类型，如 Collection<String>。
        Type[] actualTypeArguments = paramType.getActualTypeArguments();//获取泛型类型的参数类型数组
        for (Type actualTypeArgument : actualTypeArguments) {
            //System.out.println(actualTypeArgument+" ");//class 包名.类名
            //System.out.println(actualTypeArgument.getTypeName()+" ");//包名.类名
            System.out.println(((Class)actualTypeArgument).getName()+" ");//包名.类名
        }
        /*输出
        class com.loong.refiectiontest1.Creature
        ----------------
        com.loong.refiectiontest1.Creature<java.lang.String>
        -----------------
        java.lang.String
         */
    }
}
```

> 感悟： 逻辑性代码  vs 功能性代码
> 逻辑性代码  先做什么后做什么——经验
> 功能性代码  固定的，拿来就用，会用就行——工具

### 获取接口、所在包、注解

public Class<?>[] getInterfaces() 确定此对象所表示的类或接口实现的接口。

```java
@Test
public void test(){
    Class clazz = Person.class;
    //获取运行时类实现的接口
    Class[] interfaces = clazz.getInterfaces();//也是返回的Class[]
    for (Class anInterface : interfaces) {
        System.out.println(anInterface);
    }
    System.out.println("---------------------");
    //获取运行时类的父类实现的接口
    Class[] interfaces1 = clazz.getSuperclass().getInterfaces();
    for (Class anInterface : interfaces1) {
        System.out.println(anInterface);//interface 包名.接口名
    }
    //获取所在包
    Package pack = clazz.getPackage();
    System.out.println(pack);//package 包名
    //获取注解
    Annotation[] annotations = clazz.getAnnotations();
    for (Annotation annotation : annotations) {
        System.out.println(annotation);
    }
    //输出：@com.loong.refiectiontest1.MyAnnotation(value=Person的注解)
    //主要就是通过反射拿到注解的value
}
```

### ==本节重点==

"获取运行时类的带泛型的父类 的泛型"
```java
Class clazz = Person.class;
//获取运行时类的父类
Class superclass = clazz.getSuperclass();//class com.loong.refiectiontest1.Creature
//获取运行时类的带泛型的父类
Type genericSuperclass = clazz.getGenericSuperclass();//com.loong.refiectiontest1.Creature<java.lang.String>
//获取运行时类的带泛型的父类 的泛型——应用场景举例 在学泛型时举例DAO的CustomerDAO里会有这样的需求
ParameterizedType paramType = (ParameterizedType) genericSuperclass;//ParameterizedType 表示参数化类型，如Collection<String>。
Type[] actualTypeArguments = paramType.getActualTypeArguments();//获取泛型类型的参数类型数组
for (Type actualTypeArgument : actualTypeArguments) {
    //System.out.println(actualTypeArgument+" ");//class 包名.类名
    //System.out.println(actualTypeArgument.getTypeName()+" ");//包名.类名
    System.out.println(((Class)actualTypeArgument).getName()+" ");//包名.类名
}
```

"获取运行时类实现的接口"——动态代理中会用到
```java
Class clazz = Person.class;
//获取运行时类实现的接口
Class[] interfaces = clazz.getInterfaces();//也是返回的Class[]
for (Class anInterface : interfaces) {
    System.out.println(anInterface);
}
System.out.println("---------------------");
//获取运行时类的父类实现的接口
Class[] interfaces1 = clazz.getSuperclass().getInterfaces();
for (Class anInterface : interfaces1) {
    System.out.println(anInterface);//interface 包名.接口名
}
```

## ==调用运行时类的指定结构信息==

### ==调用指定方法==

通过反射，调用类中的方法，通过Method类完成。步骤：
1.通过Class类的getMethod(String name,Class…parameterTypes)方法取得一个Method对象，并设置此方法操作时所需要的参数类型。
2.之后使用Method类中的方法Object invoke(Object obj, Object... args)进行调用，并向方法中传递要设置的obj对象的参数信息。

Object invoke(Object obj, Object … args)
说明：
1.返回值类型Object对应底层方法的返回值。底层方法返回基本类型，则会包装在Object；底层方法返回类型为 void，则该调用返回 null
2.若底层方法若为静态方法，此时形参Object obj会被忽略，也可以设为 null。
3.若底层方法形参列表为空，则Object[] args为null或一个长度0的数组
4.若底层方法声明为private,则需要在调用此invoke()方法前，显式调用方法对象的setAccessible(true)方法，将可访问private的方法。

```java
//调用运行时类的指定方法——需要掌握
/*以调用Person里的show(String nation)方法为例
 @MyAnnotation(value = "show方法的注解")
private String show(String nation){System.out.println("我的国籍是：" + nation);return nation;}
 */
@Test
public void testMethod() throws NoSuchMethodException, InvocationTargetException, InstantiationException, IllegalAccessException {
    Class clazz = Person.class;
    Person p = (Person) clazz.getDeclaredConstructor().newInstance();
    //获取运行时类型的方法
    //Class类中方法Method getDeclaredMethod(String name, Class<?>... parameterTypes) 参数：（方法名，该方法的形参类型列表）形参类型用”xxx.class“表示
    Method show = clazz.getDeclaredMethod("show", String.class);
    //为反射对象设置可访问标志,禁用java语言访问检查
    show.setAccessible(true);
    //调用方法
    // Method类中方法Object invoke(Object obj, Object... args) 参数：（调用该方法的运行时类的对象，该方法的参数列表）
    String nation = (String) show.invoke(p, "中国");
    System.out.println("返回值nation" + nation);
    /*输出：
    我的国籍是：中国  (show方法内的输出)
    返回值nation中国 (返回值)
     */

    //-----调用静态方法------
    //以private static void showDesc(){System.out.println("调用了静态方法showDesc");}为例 静态 空参的
    Method methodStatic = clazz.getDeclaredMethod("showDesc");
    methodStatic.setAccessible(true);
    //Object retrunVal= methodStatic.invoke(p);//可以给一个obj,但不起作用
    Object retrunVal = methodStatic.invoke(null);//obj可以设为null
    System.out.println(retrunVal);//底层方法返回值是void时，invoke方法返回null

    //-------调用空参方法----
    //获取有三种方式
    Method methodNotArg = clazz.getDeclaredMethod("info");//只给出方法名。底层方法参数类型参数 是个参数列表，个数可0
    //clazz.getDeclaredMethod("info",new Class[0]);//也可以是长度为0的Class数组
    //clazz.getDeclaredMethod("info",null);//或者为null
    methodNotArg.setAccessible(true);
    methodNotArg.invoke(p);
}
```

### 关于setAccessible方法的使用

public void setAccessible(boolean flag) throws SecurityException
将此对象的 accessible 标志设置为指示的布尔值。值为 true 则指示反射的对象在使用时应该取消 Java 语言访问检查。值为 false 则指示反射的对象应该实施 Java 语言访问检查。

* Method、Field、Constructor对象都有setAccessible()方法。
  (Method、Field、Constructor都继承了java.lang.reflect.AccessibleObject类中的此方法)
* setAccessible启动和禁用访问安全检查的开关。
* 参数值为true则指示反射的对象在使用时应该取消Java语言访问检查。
  ①提高反射的效率。如果代码中必须用反射，而该句代码需要频繁的被调用，那么请设置为true。
  ②使得原本无法访问的私有成员也可以访问
* 参数值为false则指示反射的对象应该实施Java语言访问检查。

### 调用指定属性

在反射机制中，可以直接通过Field类操作类中的属性，通过Field类提供的set()和get()方法就可以完成设置和取得属性内容的操作。

* public Field getField(String name) 返回此Class对象表示的类或接口的指定的public的Field。
* public Field getDeclaredField(String name)返回此Class对象表示的类或接口的指定的Field。

在Field中：
* public Object get(Object obj) 取得指定对象obj上此Field的属性内容

* public void set(Object obj,Object value) 设置指定对象obj上此Field的属性内容

  如果底层字段是静态字段，则忽略 obj 变量；它可以为 null。 (如count.set(p,2)中任意的p会被忽略，不起作用。或者设为null如count.set(null,2);)

  如果属性权限问题（非public），不能get和set，需setAccessible(true)

```java
//调用指定的属性
@Test
public void testField() throws NoSuchFieldException, NoSuchMethodException, InvocationTargetException, InstantiationException, IllegalAccessException {
    Class clazz = Person.class;
    Person p = (Person) clazz.getDeclaredConstructor().newInstance();
    //调用指定的属性
    // 方法1 Field getField(String name) 返回名为name的属性。（只能获取public的）  方法一不推荐。getXxx不推荐，一般用getDeclaredXxx
    Field id = clazz.getField("id");
    //设置该属性的值set(Object obj,Object value) 返回指定对象上此 Field 表示的字段的值。如果该值是一个基本类型值，则自动将其包装在一个对象中。
    id.set(p, 100);//set(运行类的对象，属性值)
    //获取该属性的值 Object get(Object obj)
    int pid = (int) id.get(p);
    System.out.println(pid);//100

    //方法2 ①Field getDeclaredField(String name) 获取运行时类中声明的名为name的属性(所有权限的都可以)
    Field name = clazz.getDeclaredField("name");//private String name 私有
    Field age = clazz.getDeclaredField("age");//int age 默认
    //②为反射对象设置可访问标志,禁用java语言访问检查  （然后非public的才能使用set和get。否则抛异常IllegalAccessException）（public的这步有没有都可）
    name.setAccessible(true);
    age.setAccessible(true);
    //③通过set设置和get获取该属性的值
    name.set(p, "小明");
    age.set(p, 18);
    String pname = (String) name.get(p);
    int page = (int) age.get(p);
    System.out.println(pname + page);

    //Person加一个静态属性public static int count;
    Field count = clazz.getDeclaredField("count");
    count.setAccessible(true);
    count.set(p, 1);//静态的属性 对象p被忽略，不起作用
    count.set(null, 1);
}
```

### 调用指定构造器

```java
//调用运行时类中指定的构造器
@Test
public void testConstructor() throws NoSuchMethodException, InvocationTargetException, InstantiationException, IllegalAccessException {
    Class clazz = Person.class;
    Constructor constructor = clazz.getDeclaredConstructor(String.class);//构造器名和类名是一样的，故只有构造器的参数类型列表
    constructor.setAccessible(true);
    Person person = (Person) constructor.newInstance("Tom");
}
```

## 反射的应用：动态代理

### 代理模式
代理设计模式的原理:使用一个代理将对象包装起来, 然后用该代理对象取代原始对象。任何对原始对象的调用都要通过代理。代理对象决定是否以及何时将方法调用转到原始对象上。

之前为大家讲解过代理机制的操作，属于静态代理，特征是代理类和目标对象的类都是在编译期间确定下来，不利于程序的扩展。同时，每一个代理类只能为一个接口服务，这样一来程序开发中必然产生过多的代理。最好可以通过一个代理类完成全部的代理功能。
    静态代理（静态定义代理类）
    动态代理（动态生成代理类）: JDK自带的动态代理，需要反射等知识

```java
//静态代理举例
//特点：代理类和被代理类在编译期间就确定下来
    
interface ClothFactory{
    void produceCloth();
}
//代理类
 class ProxyClothFactory implements ClothFactory{
    private ClothFactory factory;//被代理类对象进行实例化

     public ProxyClothFactory(ClothFactory factory) {
         this.factory = factory;
     }

     @Override
    public void produceCloth() {
         System.out.println("代理工厂做一些准备");
         factory.produceCloth();
         System.out.println("代理工厂做一些后续工作");
    }
}
//被代理类
class NikeClothFactory implements ClothFactory{

    @Override
    public void produceCloth() {
        System.out.println("Nike工厂生产一批运动服");
    }
}
public class StaticProxyTest{
    public static void main(String[] args) {
        NikeClothFactory nikeClothFactory = new NikeClothFactory();//创建代理类的对象
        ProxyClothFactory proxyClothFactory = new ProxyClothFactory(nikeClothFactory);//创建代理类的对象
        proxyClothFactory.produceCloth();
    }
}
```


### 动态代理
动态代理是指客户通过代理类来调用其它对象的方法，并且是在程序运行时根据需要动态创建目标类的代理对象。需要动态创建目标类的代理对象。
动态代理使用场合:①调试②远程方法调用
动态代理相比于静态代理的优点：抽象角色中（接口）声明的所有方法都被转移到调用处理器一个集中的方法中处理，这样，我们可以更加灵活和统一的处理众多的方法。

#### Java动态代理相关API
Proxy ：专门完成代理的操作类，是所有动态代理类的父类。通过此类为一个或多个接口动态地生成实现类。
提供用于创建动态代理类和动态代理对象的静态方法
* static Class<?> getProxyClass(ClassLoader loader, Class<?>... interfaces) 创建一个动态代理类所对应的Class对象
* static Object **newProxyInstance(ClassLoader loader, Class<?>[] interfaces,InvocationHandler h)** 直接创建一个动态代理对象
参数：类加载器,被代理类实现的全部接口,InvocationHandler接口的实现类实例

#### 步骤
0.创建被代理的类以及接口。(一般操作)
1.创建一个实现接口InvocationHandler的类，它必须实现invoke方法，以完成代理的具体操作
  在实现类中，①创建一个被代理类对象obj②实现 invoke方法
  java.lang.reflect.InvocationHandler接口中唯一的方法：
  Object invoke(Object proxy, Method method, Object[] args)在代理实例上处理方法调用并返回结果。
    参数：（代理类的对象,要调用的方法,方法调用时所需要的参数）
    此invoke方法中，使用传过来的参数method和args调用Method类中invoke方法。method.invoke(obj,args)；
2.通过Proxy的静态方法**newProxyInstance(ClassLoader loader, Class[] interfaces, InvocationHandler h)** 创建一个接口代理
RealSubject target = new RealSubject();
// Create a proxy to wrap the original implementation
DebugProxy proxy = new DebugProxy(target);
// Get a reference to the proxy through the Subject interface
Subject sub = (Subject) Proxy.newProxyInstance(
Subject.class.getClassLoader(),new Class[] { Subject.class }, proxy);//下面的代码示例中是封装getProxyInstance方法中了
3.通过接口代理调用被代理类的方法

#### 代码示例

```java
package com.loong.proxy;

import java.lang.reflect.InvocationHandler;
import java.lang.reflect.Method;
import java.lang.reflect.Proxy;

//动态代理代码示例

interface Human{
    String getBelief();
    void eat(String food);
}

//被代理类
class SuperMan implements Human{
    @Override
    public String getBelief() {return "I believe I can fly!";}
    @Override
    public void eat(String food) {System.out.println("吃" + food);}
}
//-------------------------------------------
/*
想要事项动态代理 需要解决问题：
一 如何根据加载到内存中的被代理类，动态的创建一个代理类及其对象
二 当通过代理类的对象调用方法时，如何动态的去调用被代理类的同名方法
 */
//代理类
class ProxyFactory{
    //调用此方法 返回一个代理类对象。解决问题一
    public static Object getProxyInstance(Object obj){//参数obj：//被代理类的对象
        MyInvocationHandler handler = new MyInvocationHandler();
        handler.bind(obj);
        //java.lang.reflect.Proxy中静态方法static Object newProxyInstance(ClassLoader loader,Class<?>[] interfaces,InvocationHandler h)
        //参数：(类加载器,被代理类实现的全部接口,InvocationHandler接口的实现类实例)
        //返回一个指定接口的代理类实例，该接口可以将方法调用指派到指定的调用处理程序。
        return Proxy.newProxyInstance(obj.getClass().getClassLoader(),obj.getClass().getInterfaces(),handler);//用到了反射
    }
}

//java.lang.reflect.InvocationHandler接口的实现类
class MyInvocationHandler implements InvocationHandler{
    private Object obj;//需要使用被代理类的对象进行赋值
    public void bind(Object obj){this.obj=obj;}

    //Object invoke(Object proxy, Method method, Object[] args)在代理实例上处理方法调用并返回结果。
    //参数：（代理类的对象,要调用的方法,方法调用时所需要的参数）
    //通过代理类调用方法a时，就会自动的调用如下的invoke()——就是通过handler里的invoke来调用obj里的方法
    //将被代理类要执行的方法a的功能声明在invoke()中。invoke（obj，a,"参数"）
    @Override
    public Object invoke(Object proxy, Method method, Object[] args) throws Throwable {
        //method是代理类对象调用的方法，此方法也就作为了被代理类调用的方法——解决问题二
        Object returnValue=method.invoke(obj,args);
        return returnValue;
    }
}

public class DynamicProxyTest {
    public static void main(String[] args) {
        SuperMan superMan = new SuperMan();//被代理类对象
        //ProxyFactory proxyInstance = (ProxyFactory) ProxyFactory.getProxyInstance(superMan);//代理类的对象
        Human proxyInstance = (Human) ProxyFactory.getProxyInstance(superMan);//代理类的对象
        //当通过代理类对象调用方法时，会自动的调用被代理类中同名的方法
        System.out.println(proxyInstance.getBelief());
        proxyInstance.eat("麻辣烫");

        //这里把静态代理举例中的被代理类也用动态代理试一下
        NikeClothFactory nikeClothFactory = new NikeClothFactory();
        ClothFactory proxyInstance1= (ClothFactory) ProxyFactory.getProxyInstance(nikeClothFactory);
        proxyInstance1.produceCloth();
    }
}
```

#### 动态代理与AOP

AOP（Aspect Orient Programming,面向切面编程)。 一种思想。
> AOP主要应用了动态代理，动态代理是AOP的实现手段
> https://www.cnblogs.com/zwb7926/p/3580845.html
>
> 使用Proxy生成一个动态代理时，往往并不会凭空产生一个动态代理，这样没有太大的意义。
>
> 通常都是为指定的目标对象生成动态代理。这种动态代理在AOP中被称为AOP代理，AOP代理可代替目标对象，AOP代理
> 包含了目标对象的全部方法。但AOP代理中的方法与目标对象的方法存在差异：
> **AOP代理里的方法可以在执行目标方法之前、之后插入一些通用处理**

以前：几段代码中有相同代码段，抽离出来一个方法。但是方法是固定的。
有了动态代理以后，这个抽离出的方法可以是变动的。

```java
class HumanUtrl{
    public static void method1(){System.out.println("通用方法1");}
    public static void method2(){System.out.println("通用方法2");}
}

class MyInvocationHandler implements InvocationHandler {
    private Object obj;
    public void bind(Object obj){this.obj=obj;}

    @Override
    public Object invoke(Object proxy, Method method, Object[] args) throws Throwable {
        HumanUtrl.method1();//
        Object returnValue=method.invoke(obj,args);
        HumanUtrl.method2();//这样在method1和method2之间的方法是变动的
        return returnValue;
    }
}
```

# 第16章 java8其它新特性

Java8中有两大最为重要的改变。第一个是 Lambda 表达式；另外一个则是Java SE 8的流库 Stream API。

## 新特性概述

Java 8 是oracle公司于2014年3月发布，可以看成是自Java 5 以来最具革命性的版本。Java 8为Java语言、编译器、类库、开发工具与JVM带来了大量新特性。

* 速度更快

* 代码更少(增加了新的语法：Lambda 表达式)

* 强大的 Stream API

* 便于并行

  并行流就是把一个内容分成多个数据块，并用不同的线程分别处理每个数据块的流。相比较串行的流，并行的流可以很大程度上提高程序的执行效率。
  Java 8 中将并行进行了优化，我们可以很容易的对数据进行并行操作。Stream API 可以声明性地通过 parallel() 与 sequential() 在并行流与顺序流之间进行切换

* 最大化减少空指针异常：Optional

* Nashorn引擎，允许在JVM上运行JS应用

  jdk目录bin下jjs.exe

  jjs func.js

  ```javascript
  function f(){
  	return 1;
  };
  
  print(f() + 1);
  ```

  

![](http://101.34.218.64/JavaSE.assets/java8%E6%96%B0%E7%89%B9%E6%80%A7.png)

[What's New in JDK 8](http://www.oracle.com/technetwork/java/javase/8-whats-new-2157071.html)

之前讲过的：
接口可定义默认方法、静态方法，
新时间api(java.time包下)
注解 可重复注解、类型注解
集合 源码改动 一些集合延迟了数组的创建、HashMap底层用到了红黑树
Iterator接口中定义的默认方法  forEachRemaining
Iterable接口中的默认方法forEach

## Lambda表达式

Lambda 是一个**匿名函数**，我们可以把 Lambda 表达式理解为是一段**可以传递的代码**（将代码像数据一样进行传递）。使用它可以写出更简洁、更灵活的代码。作为一种更紧凑的代码风格，使Java的语言表达能力得到了提升。

举例：从匿名类到 Lambda 的转换

```java
@Test
public void test1(){
    Runnable r1 = new Runnable() {
        @Override
        public void run() {
            System.out.println("我爱北京天安门");
        }
    };
    r1.run();

    //-------------------------
    Runnable r2 = () -> System.out.println("我爱北京天安门");
    r2.run();
    //"->"叫做lambda操作符或箭头操作符
}

@Test
public void test2(){
    Comparator<Integer> com1= new Comparator<Integer>() {
        @Override
        public int compare(Integer o1, Integer o2) {
            return Integer.compare(o1,o2);
        }
    };
    System.out.println( com1.compare(12,21));
    //-----------Lambda表达式---------------------
    Comparator<Integer> com2= (o1, o2) -> Integer.compare(o1,o2);
    //有泛型 参数类型省略；Comparator也仅有一个抽象方法且有返回值，方法名声明省略
    System.out.println( com2.compare(12,21));
    //-----------方法引用-------------------
    Comparator<Integer> com3= Integer::compare;
    System.out.println( com3.compare(12,21));
}
```

### 语法

Lambda 表达式在Java 8 语言中引入的一种新的语法元素和操作符。
`->` 该操作符被称为 **Lambda 操作符**或**箭头操作符**。它将 Lambda 分为两个部分：
左侧：指定了 Lambda 表达式需要的**参数列表**。(其实就是接口中的抽象方法的形参列表)
右侧：指定了 **Lambda 体**，是抽象方法的实现逻辑，也即Lambda 表达式要执行的功能。(其实就是就是重写的抽象方法的方法体)

**语法规则：**
**`->`左边：lambda形参列表的参数类型可以省略(类型推断)；如果lambda形参列表只一个参数且类型可推断，其一对()也可以省略**
**`->`右边：lambda体应该使用一对{}包裹；如果lambda体只一条执行语句,可以省略{}（可能是一条return语句，可省略这一对{}和return关键字,但必须是同时省略，不能只省略一个）**

```java
public class LambdaTest1 {
    @Test
    public void test() {
        // 情景一：无参，无返回值
        Runnable r1 = () -> {System.out.println("你好");};
        Runnable r2 = () -> System.out.println("你好");//lambda体只有一条语句 大括号以及后面冒号{};可以省
        Runnable r3 =()-> {
            System.out.println("第一句");
            System.out.println("第二句");
        };

        //情景二：Lambda需要一个参数，无返回值
        //以前：
        Consumer<String> con = new Consumer<String>() {
            @Override
            public void accept(String s) {//消费一个指定泛型的数据(这里是String s)，如何消费在方法体内自定义
                System.out.println(s);
            }
        };
        //使用lambda表达式：
        Consumer<String> con1 =(String s)-> System.out.println(s);
        Consumer<String> con2 = (s) -> System.out.println(s);//类型推断 类型可以省略。
        Consumer con3 = s -> System.out.println(s);// 只需要一个参数并且该参数类型可以推断出来，小括号也可以省略。

        //情景三：多个参数，有返回值
        //以前
        Comparator<Integer> com = new Comparator<Integer>() {
            @Override
            public int compare(Integer x, Integer y) {
                return Integer.compare(x,y);
            }
        };
        //使用lambda表达式
        //无需指定 lambda 表达式的返回类型。 lambda 表达式的返回类型总是会由上下文推导得出。
        Comparator<Integer> com1= (x,y) -> {return Integer.compare(x,y);};
        Comparator<Integer> com2= (x,y) -> Integer.compare(x,y);//只有一条return语句时，可省略return和大括号;
        //Comparator<Integer> com3= (x,y) -> return Integer.compare(x,y);//错误 不能只省{};
        //Comparator<Integer> com4= (x,y) -> {Integer.compare(x,y)};//错误 不能只省return
    }
}
```

#### 摘自 java核心技术卷Ⅰ

> **即使 lambda 表达式没有参数， 仍然要提供空括号**，就像无参数方法一样：
> `0 -> { for (inti = 100;i >= 0;i ) System.out.println(i); }`
> **如果可以推导出一个 lambda 表达式的参数类型，则可以忽略其类型**。例如：
>
> ```java
> Comparator<String> comp
> 	= (first, second) // Same as (String first, String second)
> 		-> first.length() - second.length();
> ```
>
> 在这里， 编译器可以推导出 first 和 second 必然是字符串， 因为这个 lambda 表达式将赋给一个字符串比较器。（下一节会更详细地分析这个赋值。）
>
> **如果方法只有一参数， 而且这个参数的类型可以推导得出，那么甚至还可以省略小括号**：
>
> ```java
> ActionListener listener = event ->
> 	System.out.println("The time is " + new Date()");
> 	// Instead of (event) -> . . . or (ActionEvent event) -> . . .
> ```
>
> **无需指定 lambda 表达式的返回类型。 lambda 表达式的返回类型总是会由上下文推导得出。**例如，下面的表达式
> `(String first, String second) -> first.length() - second.length()`
> 可以在需要 int类型结果的上下文中使用。

> lambda表达式的重要特征:
>
> - **可选类型声明：**不需要声明参数类型，编译器可以统一识别参数值。
> - **可选的参数圆括号：**一个参数无需定义圆括号，但多个参数需要定义圆括号。
> - **可选的大括号：**如果主体包含了一个语句，就不需要使用大括号。
> - **可选的返回关键字：**如果主体只有一个表达式返回值则编译器会自动返回值，大括号需要指定表达式返回了一个数值。
>
> ——菜鸟教程

## 函数式(Functional)接口

对于只有一个抽象方法的接口， 需要这种接口的对象时， 就可以提供一个 lambda 表达 式。 这种接口称为函数式接口 （functional interface )。**Lambda表达式的本质 作为函数式接口的实例**。
 典型的Runnable、Comparator等就是函数式接口

在java.util.function包下定义了Java 8 的丰富的函数式接口。

**只包含一个抽象方法的接口，称为函数式接口。**

* 你可以**通过 Lambda 表达式来创建该接口的对象**。（若 Lambda 表达式抛出一个受检异常(即：非运行时异常)，那么该异常需要在目标接口的抽象方法上进行声明）。(“new 匿名实现类”用Lambda表达式来表示)
* 我们可以在**一个接口上使用 @FunctionalInterface 注解，这样做可以检查它是否是一个函数式接口**。同时 javadoc 也会包含一条声明，说明这个接口是一个函数式接口。
* 在java.util.function包下定义了Java 8 的丰富的函数式接口


> 如何理解函数式接口
> Java从诞生日起就是一直倡导“一切皆对象”，在Java里面面向对象(OOP)编程是一切。但是随着python、scala等语言的兴起和新技术的挑战，Java不得不做出调整以便支持更加广泛的技术要求，也即**java不但可以支持OOP还可以支持OOF（面向函数编程）**
> 在函数式编程语言当中，函数被当做一等公民对待。在将函数作为一等公民的编程语言中，Lambda表达式的类型是函数。但是在Java8中，有所不同。在Java8中，**Lambda表达式是对象，而不是函数，**它们**必须依附于**一类特别的对象类型——**函数式接口**。
> 简单的说，在Java8中，**Lambda表达式就是一个函数式接口的实例**。这就是Lambda表达式和函数式接口的关系。也就是说，只要一个对象是函数式接口的实例，那么该对象就可以用Lambda表达式来表示。
> 所以**以前用匿名实现类表示的现在都可以用Lambda表达式来写。**

### 自定义函数式接口

可以在**一个接口上使用 @FunctionalInterface 注解，这样做可以检查它是否是一个函数式接口**。同时 javadoc 也会包含一条声明，说明这个接口是一个函数式接口。

```java
//自定义函数式接口
//@FunctionalInterface
//interface MyNumber{
//    public double getValue();
//}
@FunctionalInterface//使用注解
interface MyFun<T>{//使用上泛型
    public T getValue(T t);
}

public class MyFunctionTest {
    public String toUpperString(MyFun<String> myFun,String str){
        return myFun.getValue(str);
    }

    @Test
    public void test(){
        String newStr=toUpperString(str-> str.toUpperCase(),"abcde");
        System.out.println(newStr);
    }
}
//作为参数传递 Lambda 表达式：为了将 Lambda 表达式作为参数传递，接收Lambda表达式的参数类型必须是与该 Lambda 表达式兼容的函数式接口的类型。
```

### 内置的函数式接口

在java.util.function包下定义了Java 8 的丰富的函数式接口。

Java 内置四大核心函数式接口：

| 函数式接口   | 参数类型 | 返回类型 | 用途 |
| ----- | ------- | ------ | ----------- |
| Consumer\<T>消费型接口 | T | void     | 对类型为T的对象应用操作，包含方法：void accept(T t) |
| Supplier\<T>供给型接口  | 无 | T | 返回类型为T的对象，包含方法：T  get()  |
| Function<T, R>函数型接口 | T | R | 对类型为T的对象应用操作，并返回结果。结果是R类型的对象。包含方法：R apply(T t) |
| Predicate\<T>断定型接口 | T  | boolean  | 确定类型为T的对象是否满足某约束，并返回boolean 值。包含方法：boolean test(T t) |

使用示例

```java
@Test
public void test1(){
    happyTime(500, new Consumer<Double>() {
        @Override
        public void accept(Double money) {
            System.out.println("买了一杯水，花了"+money);
        }
    });
    //---------------使用lambda表达式-------------
    happyTime(500,money-> System.out.println("买了一杯水，花了"+money));
}
public void happyTime(double money, Consumer<Double> consumer){
    consumer.accept(money);
}

    @Test
    public void test2() {
        List<String> list = Arrays.asList("北京", "天津", "南京", "东京", "普京");
        List<String> filterStrs = filterString(list, new Predicate<String>() {
            @Override
            public boolean test(String s) {
                return s.contains("京");
            }
        });
        //------------------使用Lambda表达式------
        List<String> filterStrs2 = filterString(list, s -> s.contains("京"));
    }
    public List<String> filterString(List<String> list, Predicate<String> pre) {//过滤字符串
        ArrayList<String> filterList = new ArrayList<>();
        for (String s : filterList) {
            if (pre.test(s)) {//根据test(s)的规则过滤字符串s
                filterList.add(s);
            }
        }
        return filterList;
    }
```

其它：

![其它内置函数式接口.png](http://101.34.218.64/JavaSE.assets/%E5%85%B6%E5%AE%83%E5%86%85%E7%BD%AE%E5%87%BD%E6%95%B0%E5%BC%8F%E6%8E%A5%E5%8F%A3.png)

### 总结

1. 何时使用lambda表达式？
当需要对一个函数式接口实例化的时候，可以使用lambda表达式。
2. 何时使用给定的函数式接口？
如果我们开发中需要定义一个函数式接口，首先看看在已有的jdk提供的函数式接口是否提供了能满足需求的函数式接口。如果有，则直接调用即可，不需要自己再自定义了

## 方法引用与构造器引用

### 方法引用

method references

**当要传递给Lambda体的操作，已经有实现的方法了，可以使用方法引用**！

* 方法引用可以看做是Lambda表达式深层次的表达。换句话说，方法引用就是**Lambda表达式**，也就是函数式接口的一个实例，**通过方法的名字来指向一个方法**，可以认为是Lambda表达式的一个语法糖。

* 要求：**实现接口的抽象方法的参数列表和返回值类型，必须与方法引用的方法的参数列表和返回值类型保持一致！**

* 格式：使用操作符 `::` 将类(或对象) 与 方法名分隔开来。

  `类(或对象) :: 方法名`

* 如下三种主要使用情况：
  ① 对象::实例方法名
  ② 类::静态方法名
  ③ 类::实例方法名
  
  > 要求接口中的抽象方法的形参列表和返回值类型与方法引用的方法的形参列表和返回值类型相同！（针对于情况1和情况2）
  > 当函数式接口方法的第一个参数是需要引用方法的调用者，并且第二个参数是需要引用方法的参数(或无参数)时：ClassName::methodName（针对于情况3）

如果给函数式接口提供实例，恰好满足方法引用的使用情境，大家就可以考虑使用方法引用给函数式接口提供实例。如果大家不熟悉方法引用，那么还可以使用lambda表达式。

```java
public class MethodRefTest {
    
   // 情况一：对象 :: 实例方法
   //Consumer中的void accept(T t)
   //PrintStream中的void println(T t)
   @Test
   public void test1() {
      Consumer<String> con =str -> System.out.println(str);
      PrintStream ps = System.out;//静态常量
      Consumer<String> con2 = ps::println;
      Consumer<String> con3 = System.out::println;
      con3.accept("test1");
   }

   //Supplier中的T get()
   //Employee中的String getName()
   @Test
   public void test2() {
      List<Employee> employees = EmployeeData.getEmployees();
      Employee employee = employees.get(2);
      Supplier<String> sup= ()-> {return employee.getName();};
      Supplier<String> sup1= ()-> employee.getName();
      Supplier<String> sup2=employee::getName;
        System.out.println(sup2.get());
    }

   // 情况二：类 :: 静态方法
   //Comparator中的int compare(T t1,T t2)
   //Integer中的int compare(T t1,T t2)

   private static int compare(Employee o1, Employee o2) {
      return Integer.compare(o1.getAge(), o2.getAge());
   }
   @Test
   public void test3() {
        List<Employee> employees = EmployeeData.getEmployees();
        Collections.sort(employees, new Comparator<Employee>() {
            @Override
            public int compare(Employee o1, Employee o2) {
                return Integer.compare(o1.getAge(),o2.getAge());//年龄从小到大排序
            }
        });
      Collections.sort(employees,(o1,o2)->Integer.compare(o1.getAge(),o2.getAge()));//lambda表达式
      Collections.sort(employees, MethodRefTest::compare);//方法引用

      for (Employee employee : employees) {
         System.out.println(employee);
      }

      //——————————————每两个比————————
      Comparator<Integer> com= (t1,t2)-> Integer.compare(t1,t2);
      Comparator<Integer> com1= Integer::compare;
      System.out.println(com1.compare(12,21));
    }

   //Function中的R apply(T t)
   //Math中的Long round(Double d)
   @Test
   public void test4() {
      Function<Double,Long> func=new Function<Double, Long>() {
         @Override
         public Long apply(Double d) {
            return Math.round(d);
         }
      };
      Function<Double,Long> func1=d->Math.round(d);
      Function<Double,Long> func2= Math::round;
      Long ans=func2.apply(2.5);
   }

   // 情况三：类 :: 实例方法
   // Comparator中的int comapre(T t1,T t2)
   // String中的int t1.compareTo(t2)
   @Test
   public void test5() {
      Comparator<String> com = new Comparator<String>() {
         @Override
         public int compare(String o1, String o2) {
            return o1.compareTo(o2);
         }
      };
      Comparator<String> com1=(o1,o2)->o1.compareTo(o2);
      Comparator<String> com2= String::compareTo;
      int result=com2.compare("abc","abb");
   }

   //BiPredicate中的boolean test(T t1, T t2);
   //String中的boolean t1.equals(t2)
   @Test
   public void test6() {
      BiPredicate<String,String> bip=new BiPredicate<String, String>() {
         @Override
         public boolean test(String s, String s2) {
            return s.equals(s2);
         }
      };
      BiPredicate<String,String> bip1= (s,s2) -> s.equals(s2);
      BiPredicate<String,String> bip2= String::equals;
      boolean result = bip2.test("haha", "haha");
   }

   // Function中的R apply(T t)
   // Employee中的String getName();
   @Test
   public void test7() {
      Function<Employee,String> fun = new Function<Employee, String>() {
         @Override
         public String apply(Employee employee) {
            return employee.getName();
         }
      };
      Function<Employee,String> fun1=(e)->e.getName();
      Function<Employee,String> fun2=Employee::getName;
      String name=fun2.apply(new Employee(1100,"小明"));
   }
```

### 构造器引用

构造器引用与方法引用很类似，只不过方法名为 new。`类名::new`

和方法引用类似，函数式接口的**抽象方法**的形参列表和构造器的形参列表一致。抽象方法的返回值类型即为构造器所属的类的类型

可以用数组类型建立构造器引用。`数据类型[ ]:new`

> Java 有一个限制，无法构造泛型类型 T 的数组。数组构造器引用对于克服这个限制很有用。——见《java核心技术卷Ⅰ》

```java
//构造器引用
   //Supplier中的T get()
   @Test
   public void test1(){
       Supplier<Employee> sup = new Supplier<Employee>() {
           @Override
           public Employee get() {
               return new Employee();
           }
       };

       Supplier<Employee> sup1= ()->new Employee();

       Supplier<Employee> sup2= Employee::new;
       Employee employee = sup2.get();

   }

//Function中的R apply(T t)
   @Test
   public void test2(){
       Function<Integer,Employee> fun= new Function<Integer,Employee>() {
           @Override
           public Employee apply(Integer id) {
               return new Employee(1234);
           }
       };
       Function<Integer,Employee> fun1=(id)->new Employee(id);
       Function<Integer,Employee> fun2=Employee::new;
       Employee employee = fun2.apply(1234);
}

//BiFunction中的R apply(T t,U u)
   @Test
   public void test3(){
       BiFunction<Integer,String,Employee> biF=new BiFunction<Integer,String,Employee>() {
           @Override
           public Employee apply(Integer id, String name) {
               return new Employee(id,name);
           }
       };
       BiFunction<Integer,String,Employee> biF1= (id,name)->new Employee(id,name);
       BiFunction<Integer,String,Employee> biF2= Employee::new;
       Employee employee = biF2.apply(123,"小明");

}

//数组引用
   //Function中的R apply(T t)
   @Test
   public void test4(){
       int[] arr=new int[5];
       Integer[] arrr=new Integer[5];
       Function<Integer,Integer[]> fun=new Function<Integer, Integer[]>() {
           @Override
           public Integer[] apply(Integer n) {
               return new Integer[n];
           }
       };
       Function<Integer,Integer[]> fun1=(n)->new Integer[n];
       Function<Integer,Integer[]> fun2=Integer[]::new;
       Integer[] arr2=fun2.apply(5);
}
```

## 强大的Stream API

Stream API ( java.util.stream) 把真正的函数式编程风格引入到Java中。这是目前为止对Java类库最好的补充，因为Stream API可以极大提供Java程序员的生产力，让程序员写出高效率、干净、简洁的代码。
Stream 是 Java8 中处理集合的关键抽象概念，它可以指定你希望对集合进行的操作，可以执行非常复杂的查找、过滤和映射数据等操作。 使用Stream API 对集合数据进行操作，就类似于使用 SQL 执行的数据库查询。也可以使用 Stream API 来并行执行操作。简言之，**Stream API 提供了一种高效且易于使用的处理数据的方式。**

### 为什么要使用Stream API

实际开发中，项目中多数数据源都来自于Mysql，Oracle等。但现在数据源可以更多了，有MongDB，Radis等，而这些NoSQL的数据就需要Java层面去处理。
 Collection 集合和 Stream 的区别：Collection 是一种静态的内存数据结构，而 Stream 是有关计算的。前者是主要面向内存，存储在内存中，后者主要是面向 CPU，通过 CPU 实现计算。——（**Stream关注的是对数据的运算，与CPU打交道；集合关注的是数据的存储，与内存打交道**）
 java8提供了一套api,使用这套api可以对内存中的数据进行过滤、排序、映射、归约等操作。类似于sql对数据库中表的相关操作。

### 什么是 Stream

是数据渠道，用于操作数据源（集合、数组等）所生成的元素序列。
**注意**：
①Stream 自己**不会存储元素**。
②Stream **不会改变源对象**。相反，他们会返回一个持有结果的新Stream。
③Stream **操作是延迟执行的**。这意味着他们会等到**需要结果的时候才执行**。

### Stream 的操作三个步骤

① 创建 Stream(Stream的实例化)
  一个数据源（如：集合、数组），获取一个流
② 中间操作
  一个**中间操作链**，对数据源的数据进行处理(过滤、映射、...)
③ 终止操作(终端操作)
  **一旦执行终止操作，就执行中间操作链，并产生结果**。**之后，不会再被使用**(stream已经**执行终止操作**了，会抛异常，**stream已被关闭，不能再用了。要重新创建一个**)。

![stream示意.png](http://101.34.218.64/JavaSE.assets/stream%E7%A4%BA%E6%84%8F.png)

### 创建 Stream的方式

#### 方式一：通过集合

Java8 中的 Collection 接口(java.util.Collection)被扩展，提供了两个获取流的方法：
* default Stream\<E> stream() : 返回一个顺序流
* default Stream\<E> parallelStream() : 返回一个并行流
```java
List<Employee> employees = EmployeeData.getEmployees();
Stream<Employee> stream = employees.stream();//操作时按集合顺序去取
Stream<Employee> stream1 = employees.parallelStream();//并行流
```

#### 方式二：通过数组
Java8 中的 Arrays 的静态方法 stream() 可以获取数组流：
 static \<T> Stream\<T> stream(T[] array): 返回一个流
 重载形式，能够处理对应基本类型的数组：
 public static IntStream stream(int[] array)
 public static LongStream stream(long[] array)
 public static DoubleStream stream(double[] array)
```java
String[] strarr = {"hello","world","!"};
Stream<String> stream = Arrays.stream(strarr);//返回带泛型的流

int[] arr = new int[]{1,2,3,4,5,6};
IntStream intstream = Arrays.stream(arr);//返回基本数据类型的流
```

#### 方式三：通过Stream的of()
Stream类静态方法 of(), 通过显示值创建一个流。它可以接收任意数量的参数。
public static\<T> Stream\<T> of(T... values) : 返回一个流
```java
Stream<Integer> integerStream = Stream.of(1, 2, 3, 4, 5, 6);
```

#### 方式四：创建无限流(不常用，了解)

Stream类静态方法 iterate() 和 generate(),创建无限流。
* 迭代
public static\<T> Stream\<T> iterate(final T seed, final UnaryOperator\<T> f)
* 生成
public static\<T> Stream\<T> generate(Supplier\<T> s)
```java
//举例：遍历前十个偶数
Stream<Integer> stream = Stream.iterate(0, x -> x + 2);
stream.limit(10).forEach(System.out::println);//如果没有limit 将会是无限的

//举例：生成10个随机数
Stream<Double> stream1 = Stream.generate(Math::random);
stream1.limit(10).forEach(System.out::println);
```

### Stream 的中间操作
多个中间操作可以连接起来形成一个流水线，**除非流水线上触发终止操作，否则中间操作不会执行任何的处理！**
而在终止操作时一次性全部处理，称为“**惰性求值**”。
返回值是还流。

#### 筛选与切片
* filter(Predicate p)	接收 Lambda ， 从流中排除某些元素——过滤
* distinct()	筛选，通过流所生成元素的 hashCode() 和 equals() 去除重复元素——去重
* limit(long maxSize)	截断流，使其元素不超过给定数量
* skip(long n)	跳过元素，返回一个扔掉了前 n 个元素的流。若流中元素不足 n 个，则返回一个空流。与 limit(n) 互补

```java
List<Employee> list=EmployeeData.getEmployees();
//①filter(Predicate p)	接收 Lambda ， 从流中排除某些元素——过滤
//Predicate<T>中方法boolean test(T o)
Stream<Employee> stream = list.stream();
Stream<Employee> employeeStream = stream.filter(employee -> employee.getAge() > 35);//筛选大于35岁的员工
employeeStream.forEach(System.out::println);//终止操作。输出了大于35岁的员工
//可和终止操作写成一句
//stream.filter(employee -> employee.getAge() > 35).forEach(System.out::println);
//注意：上面stream已经执行终止操作了，会抛异常，stream已被关闭，不能再用了。要重新创建一个

//②distinct()	筛选，通过流所生成元素的 hashCode() 和 equals() 去除重复元素——去重
list.add(new Employee(1008, "扎克伯格", 35, 2500.32));//添加重复元素供测试
list.add(new Employee(1008, "扎克伯格", 35, 2500.32));
 Stream<Employee> stream1 = list.stream();
 stream1.distinct().forEach(System.out::println);//去重
 
//③limit(long maxSize)	截断流，使其元素不超过给定数量
//④skip(long n)	跳过元素，返回一个扔掉了前 n 个元素的流。若流中元素不足 n 个，则返回一个空流。可与 limit(n) 互补
Stream<Integer> integerStream = Stream.of(1, 2, 3, 4, 5, 6,7);
//integerStream.limit(2).forEach(System.out::println);//1 2 取前两个
//integerStream.skip(4).forEach(System.out::println);//5 6 7 跳过了前四个元素
//integerStream.skip(4).limit(2).forEach(System.out::println);//5,6 跳过了前四个元素后 取前两个
integerStream.limit(2).skip(1).forEach(System.out::println);//2 取前两个后 跳过一个
```

#### 映射
* **map(Function f)**	接收一个函数作为参数，该函数会被应用到每个元素上，并将其映射成一个新的元素。
* mapToDouble(ToDoubleFunction f)	接收一个函数作为参数，该函数会被应用到每个元素上，产生一个新的 DoubleStream。
* mapToInt(ToIntFunction f)	接收一个函数作为参数，该函数会被应用到每个元素上，产生一个新的 IntStream。
* mapToLong(ToLongFunction f)	接收一个函数作为参数，该函数会被应用到每个元素上，产生一个新的 LongStream。
* **flatMap(Function f)**	接收一个函数作为参数，将流中的每个值都换成另一个流，然后把所有流连接成一个流
```java
 @Test
    public void test2(){
       //map(Function f)	接收一个函数作为参数，该函数会被应用到每个元素上，并将其映射成一个新的元素。
        // Function<T, R>中方法R apply(T t)
        List<String> list = Arrays.asList("aa","bb","cc","dd","ee");
        list.stream().map(str->str.toUpperCase()).forEach(System.out::println);

        //练习：获取员工姓名长度大于3的 员工的姓名
        List<Employee> employees = EmployeeData.getEmployees();
        Stream<String> namesStream = employees.stream().map(Employee::getName);//Stream<Employee>映射成 Stream<String>
        namesStream.filter(name->name.length()>3).forEach(System.out::println);

        //flatMap(Function f)	接收一个函数作为参数，将流中的每个值都换成另一个流，然后把所有流连接成一个流
// map之于flatMap相当于add之于addAll。list1.add(list2);把list2作为一个元素，而list1.addAll(list2);把list2中的元素添加到list1
        Stream<Stream<Character>> streamStream = list.stream().map(StreamAPITest1::fromStringToStream);//是Stream的Stream
        streamStream.forEach(s-> s.forEach(System.out::println)); //嵌套forEach

        Stream<Character> characterStream = list.stream().flatMap(StreamAPITest1::fromStringToStream);//是Character的Stream
        characterStream.forEach(System.out::println);
    }
    //将字符串中多个字符构成的集合转换为对应的Stream实例
    public static Stream<Character> fromStringToStream(String str){
        ArrayList<Character> list = new ArrayList<>();
        for (Character c : str.toCharArray()) {
            list.add(c);
        }
        return list.stream();
    }
```

#### 排序
* sorted()	产生一个新流，其中按自然顺序排序
* sorted(Comparator com)	产生一个新流，其中按比较器顺序排序
```java
//sorted()	产生一个新流，其中按自然顺序排序
 List<Integer> integers = Arrays.asList(4545, 4854, 48, 54, 848, 87, 5);
 integers.stream().sorted().forEach(System.out::println);
 //sorted(Comparator com)	产生一个新流，其中按比较器顺序排序
 EmployeeData.getEmployees().stream().sorted((e1,e2)->e1.getAge()-e2.getAge()).forEach(System.out::println);
```

### Stream 的终止操作
* 终端操作会从流的流水线生成结果。其结果可以是任何不是流的值，例如：List、Integer，甚至是 void 。
* 流进行了终止操作后，不能再次使用

#### 匹配与查找
* allMatch(Predicate p)	检查是否匹配所有元素
* anyMatch(Predicate p)	检查是否至少匹配一个元素
* noneMatch(Predicate p)	检查是否没有匹配所有元素

* findFirst()	返回第一个元素
* findAny()	返回当前流中的任意元素
* count()	返回流中元素总数
* max(Comparator c)	返回流中最大值
* min(Comparator c)	返回流中最小值
* forEach(Consumer c)	内部迭代(使用 Collection 接口需要用户去做迭代，称为外部迭代。相反，Stream API 使用内部迭代——它帮你把迭代做了)
```java
List<Employee> employees = EmployeeData.getEmployees();

//allMatch(Predicate p)	检查是否匹配所有元素
//练习：是否所有员工的年龄都大于18岁
boolean allMatch = employees.stream().allMatch(e -> e.getAge() > 18);
System.out.println(allMatch);

//anyMatch(Predicate p)	检查是否至少匹配一个元素
//练习 是否存在员工的工资大于9000
boolean anyMatch = employees.stream().anyMatch(e -> e.getSalary() > 9000);
System.out.println(anyMatch);

//noneMatch(Predicate p)	检查是否 没有匹配所有元素
//是否存在员工姓雷
//boolean noneMatch = employees.stream().noneMatch(e -> e.getName().charAt(0) == '雷');
boolean noneMatch = employees.stream().noneMatch(e -> e.getName().startsWith("雷"));
System.out.println(noneMatch);//false 说明有匹配的元素

//findFirst()	返回第一个元素
Optional<Employee> first = employees.stream().findFirst();
System.out.println(first);//Optional[Employee{id=1001, name='马化腾', age=34, salary=6000.38}]
System.out.println("-------");

//findAny()	返回当前流中的任意元素
for (int i=0;i<100;i++){
    System.out.println(employees.stream().findAny());//多次还是一样的。。
    //System.out.println(employees.parallelStream().findAny());//多次会有不同，不稳定
}
//count()	返回流中元素总数
long count = employees.stream().filter(e->e.getSalary()>5000).count();//工资大于5000的员工数量

//max(Comparator c)	返回流中最大值
//min(Comparator c)	返回流中最小值
Optional<Employee> max = employees.stream().max((e1, e2) -> Double.compare(e1.getSalary(), e2.getSalary()));
Optional<Employee> min = employees.stream().min((e1, e2) -> Double.compare(e1.getSalary(), e2.getSalary()));

//forEach(Consumer c)	内部迭代
employees.stream().forEach(System.out::println);//Stream的forEach
employees.forEach(System.out::println);//List继承了接口Iterable的forEach
```

#### 规约
* reduce(T iden, BinaryOperator b) 可以将流中元素反复结合起来，得到一个值。返回 T
* reduce(BinaryOperator b) 可以将流中元素反复结合起来，得到一个值。返回 Optional\<T>

> 注：映射map 和 规约reduce 的连接通常称为 map-reduce 模式，因 Google用它来进行网络搜索而出名。

```java
//reduce(T identity, BinaryOperator<T> accumulator) 可以将流中元素反复结合起来，得到一个值。返回 T
//BinaryOperator<T> extends BiFunction<T,T,T> 所以R apply(T t, U u);变成了T apply(T t, T u);
//练习 计算1-10的自然数的和
List<Integer> list = Arrays.asList(1,2,3,4,5,6,7,8,9,10);
//Integer reduce = list.stream().reduce(0, (x, y) -> x + y);//x+y返回x，再加下一个数y
Integer reduce = list.stream().reduce(0, Integer::sum);//方法引用
System.out.println(reduce);//55

//reduce(BinaryOperator b) 可以将流中元素反复结合起来，得到一个值。返回 Optional<T>
//计算公司所有员工工资总和
List<Employee> employees = EmployeeData.getEmployees();
//Optional<Double> reduce1 = employees.stream().map(e -> e.getSalary()).reduce((x, y) -> x + y);
Optional<Double> reduce1 = employees.stream().map(Employee::getSalary).reduce(Double::sum);
System.out.println(reduce1);//Optional[48424.08]
```

#### 收集
* collect(Collector c)	将流转换为其他形式。接收一个 Collector接口的实现(收集器)，用于给Stream中元素做汇总的方法

Collector 接口中方法的实现决定了如何对流执行收集的操作(如收集到 List、Set、Map)。——收集器

```java
//练习：查找工资大于6000的员工，结果返回一个list或set
List<Employee> employees = EmployeeData.getEmployees();
//返回list
List<Employee> employeeList = employees.stream().filter(e -> e.getSalary() > 6000).collect(Collectors.toList());
employeeList.forEach(System.out::println);//集合的forEach
//返回set
Set<Employee> employeeSet = employees.stream().filter(e -> e.getSalary() > 6000).collect(Collectors.toSet());
employeeSet.forEach(System.out::println);//集合的forEach
```
##### Collectors工具类
Collectors 实用类提供了很多静态方法，可以方便地创建常见收集器实例
* toList	把流中元素收集到List。返回List\<T>
  `List<Employee> emps= list.stream().collect(Collectors.toList());`
* toSet	把流中元素收集到Set。返回Set\<T>
  `Set<Employee> emps= list.stream().collect(Collectors.toSet());`
* toCollection	把流中元素收集到创建的集合。返回Collection\<T>
  `Collection<Employee> emps =list.stream().collect(Collectors.toCollection(ArrayList::new));`

其它

![Collectors工具类.png](http://101.34.218.64/JavaSE.assets/Collectors%E5%B7%A5%E5%85%B7%E7%B1%BB.png)



## Optional类

到目前为止，臭名昭著的空指针异常是导致Java应用程序失败的最常见原因。以前，**为了解决空指针异常，Google公司著名的Guava项目引入了Optional类**，Guava通过使用检查空值的方式来防止代码污染，它鼓励程序员写更干净的代码。受到Google Guava的启发，**Optional类已经成为Java 8类库的一部分。**

**Optional\<T> 类(java.util.Optional) 是一个容器类，它可以保存类型T的值，代表这个值存在。或者仅仅保存null，表示这个值不存在。原来用 null 表示一个值不存在，现在 Optional 可以更好的表达这个概念。并且可以避免空指针异常。**

Optional类的Javadoc描述如下：这是一个可以为null的容器对象。如果值存在则isPresent()方法会返回true，调用get()方法会返回该对象。

Optional提供很多有用的方法，这样我们就不用显式进行空值检测。
① 创建Optional类对象的方法：
* Optional.of(T t) : 创建一个 Optional 实例，t必须非空；
* Optional.empty() : 创建一个空的 Optional 实例
* Optional.ofNullable(T t)：t可以为null

```java
Girl girl = new Girl();
Optional<Girl> girl1 = Optional.of(girl);
girl=null;
//Optional.of(girl);//异常 NullPointerException
Optional<Girl> girl2 = Optional.ofNullable(girl);//可以为null
System.out.println(girl2);//Optional.empty
//Optional类中toString() {return value != null? String.format("Optional[%s]", value) : "Optional.empty";}
```

② 判断Optional容器中是否包含对象：
* boolean isPresent() : 判断是否包含对象
* void ifPresent(Consumer<? super T> consumer) ：如果有值，就执行Consumer接口的实现代码，并且该值会作为参数传给它。

③ 获取Optional容器的对象：
* T get(): 如果调用对象包含值，返回该值，否则抛异常。**调用get前用isPresent判断一下**
* T orElse(T other) ：如果有值则将其返回，否则返回指定的other对象。(**为null则返回指定的对象**）
* T orElseGet(Supplier<? extends T> other) ：如果有值则将其返回，否则返回由Supplier接口实现提供的对象。
* T orElseThrow(Supplier<? extends X> exceptionSupplier) ：如果有值则将其返回，否则抛出由Supplier接口实现提供的异常。

```java
public class OptionalTest {
    @Test
    public void test1(){
        Girl girl = new Girl();
        Optional<Girl> girl1 = Optional.of(girl);
        girl=null;
        //Optional.of(girl);//异常 NullPointerException
        Optional<Girl> girl2 = Optional.ofNullable(girl);//可以为null
        System.out.println(girl2);//Optional.empty
        //Optional类中toString() {return value != null? String.format("Optional[%s]", value) : "Optional.empty";}
    }

    public String getGirlName(Boy boy){
        return  boy.getGirlfriend().getName();//boy和boy.getGirlfriend()都可能为null，造成空指针
    }
    public String getGirlName1(Boy boy){//优化：加了判断bull
        if(boy!=null){
            Girl girlfriend = boy.getGirlfriend();
            if(girlfriend!=null)return girlfriend.getName();
        }
        return  null;
    }
    public String getGirlName2(Boy boy){//优化：使用Optional
        Optional<Boy> boyOptional = Optional.ofNullable(boy);
        //此时的boy1一定非空
        Boy boy1 = boyOptional.orElse(new Boy(new Girl("迪丽热巴")));

        Girl girl = boy1.getGirlfriend();

        Optional<Girl> girlOptional = Optional.ofNullable(girl);
        //girl1一定非空
        Girl girl1 = girlOptional.orElse(new Girl("古力娜扎"));

        return girl1.getName();
    }
    @Test
    public void test2(){
        Boy boy = null;
        boy = new Boy();
        System.out.println(getGirlName2(null));//迪丽热巴  boy为null
        System.out.println(getGirlName2(boy));//古力娜扎 boy.getGirlfirend（）为null
    }
}
class Girl {
    private String name;
    public Girl(String name){this.name=name;}
    public Girl() {}
    public String getName() {return name;}
    public void setName(String name) {this.name = name;}
    @Override
    public String toString() {return "Girl{" + "name='" + name + '\'' + '}';}
}

class Boy {
    private Girl girlfriend;
    public Boy() {}
    public Boy(Girl girlfriend) {this.girlfriend = girlfriend;}
    public Girl getGirlfriend() {return girlfriend;}
    public void setGirlfriend(Girl girlfriend) {this.girlfriend = girlfriend;}
    @Override
    public String toString() {return "Boy{" + "girlfriend=" + girlfriend + '}';
    }
}
```

# 附:Java 9及以后版本的新特性

网上提供的切换java版本的方法 .bat

```java
@echo off
set JAVA_HOME=C:\Program Files\Java\jdk-16
set Path=%JAVA_HOME%\bin;%Path%
echo Java 16 activated.
```



# 附：软件使用

## IDEA使用

关于版本：并不是月份  是xx年发布的第几个版本的迭代版本。年份.版本.小版本

仅运行的话，软件自带了jre 。开发的话需要装jdk

➢ 工程下的 src 类似于 Eclipse 下的 src 目录，用于存放代码。
➢ 工程下的.idea 和 project01.iml 文件都是 IDEA 工程特有的。类似于 Eclipse 工程下的.settings、.classpath、.project 等。（可以靠这个分辨是一个idea工程还是eclipse工程）

同一个窗口管理 n 个项目，这在IntelliJ IDEA 是无法做到的。一个 Project 打开一个 Window 窗口，可以打开多个项目窗口。(现在可以了?，file-projectstructure，可以在一个窗口导入多个project)

删除模块先remove 再delete

但是可以多模块(module) 右击项目 创建模块 之后写代码在模块里的src 然后项目里的src没用了可以删除了。

新建项目 java（java EE是web的，Sprong是框架的）

不管是创建类还是接口、枚举都选创建类

在 IDEA 里要说的是，写完代码，不用点击保存。IDEA 会自动保存代码

psvm或main 快速打出main方法

sout打出System.out.println   到so就可以回车了

内容.sout  可以System.out.println(内容)

new XXX().var 可以快速生成局部遍历

集合或数组名.for 可以快速生成foreach

iter遍历可迭代对象或数组

代码提示不区分大小写 编辑器 常规 代码完成 区分大小写(Match case)的√去掉

shift F6批量重命名变量

快捷键 注意 ctrl + d不是删除 是复制到下一行  删除一行是ctrl +Y

鼠标放在爆红位置 万能解错/生成返回值变量   alt + enter

环绕 选中代码 ctrl alt T

生成构造器 set get等 alt+insert

ctrl p 提醒方法参数  

ctrl q 显示文档提示

alt +7 左侧的Structrue = **Ctrl＋F12** 可以显示当前文件的结构

看一个类的层级关系 ctrl + H[学习继承后，非常有用]

中一个类，按**CTRL+ALT+U**，即可生成当前类的继承关系图 也可以右键Diagrams(图表)——Show Diagram(显示图)。Ctrl+ALT+B显示实现，Ctrl+ALT+P显示父级

将光标放在一个方法上，输入 ctrl + B , 可以定位到方法 [学继承后，非常有用]
***********
鼠标放在 方法或变量等 Ctrl + B , 或者Ctrl + 鼠标左键    Go to declaration转到定义(声明)处
Ctrl + Alt + B  Go to implementation(s)转到实现         
也可以右击——转到—— 声明 或实现

**********
自动的分配变量名 , 通过 在后面假 .var

Ctrl + N   Go to class
Ctrl + Shift + N   Go to file
Ctrl + Alt + Shift + N   Go to symbol
Alt + Right/Left   Go to next / previous editor tab

IDEA导入Eclipse项目为一个模块：

* Eclipse中，右击项目名——显示位置——资源管理器，找到项目文件夹，ctrl+c

  ![](http://101.34.218.64/JavaSE.assets/eclipse%E5%A4%8D%E5%88%B6%E9%A1%B9%E7%9B%AE%E6%96%87%E4%BB%B6%E5%A4%B9.png)

* IDEA中，右击项目名——show in...（打开于）——Explorer(资源管理器) ，找到项目文件夹——点进去，处于与其它模块共同的层次的目录下，ctrl+v

  ![](http://101.34.218.64/JavaSE.assets/idea%E7%B2%98%E8%B4%B4%E6%A8%A1%E5%9D%97.png)

* 文件——项目结构(快捷键CTRL+ALT+ SHIFT+S)
* Module（模块）——“+”——导入模块——选中刚粘贴的那个文件夹——从外部模型导入模块——Eclipse——然后一直下一步 如果报错jdk版本不对，在“依赖”那里选择一下jdk版本



使用单元测试方法 无法在控制台输入：在IDEA中点击help->Edit Custom Vm Options…，进入，在最后一行加入：（最后记得重启idea）  -Deditable.java.test.console=true

## Eclipse的使用

运行 Ctrl+F11

1.Alt+/ 代码提示 敲完main 按Alt+/ ，敲完sysout按Alt+/   syso就行

2.自动的代码提示

Window --> Preferences->Java --> 打开Editor --> 点击Content Assist（内容辅助）->Auto activition triggers for Java（java的自动激活触发器） 的值为 .abcdefghijklmnopqrstuvwxyz

有的版本区分大小写.abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ

再在上面插入”Disable insertion triggers except 'Enter'“的地方打对勾,防止按个别的键空格、等号等也给补全。

3.Ctrl+Shift+F不起作用，和输入法的简繁切换冲突，禁用了输入法的即可

4.设置文档注释后，在方法、类等前面按`/**`再回车
见"Eclipse的使用配置.pdf"

5.导包 ctrl shift O      查看类型层次结构ctrl shift T

6.光标在语句中，按shift+回车 下起一空行 ；ctrl shift 回车 上起一行

7.在标签栏源码那里可以自动生成构造器和getter setter    按ALT +SHIFT +S

8.导入现有的项目后 改完包名还有x号是需要保存一下

9.

```java
customerList.getAllCustomers(这里)这里;这里
    鼠标光标放在这三个中一个地方按ctrl 1
将语句指定给新的局部变量
   Customer[] 自定义 =  customerList.getAllCustomers();
```

10.窗口——首选项——java——编辑器——Code Minings(代码挖掘)  在show method parameter names（显示方法参数名称）打对号 形参

11.光标选中指定的类，查看继承树结构：ctrl + t   IDEA里是Ctrl H

12.Eclipse Debug

双击行号前加断点 右击代码 调试方式

![](http://101.34.218.64/JavaSE.assets/eclipse%E8%B0%83%E8%AF%95%E5%8A%9F%E8%83%BD.png)

step into 单步跳入(f5) 进入当前行所调用的**方法**中
step over 单步跳过(f6) 执行完当前行的**语句**，进入下一行
step return 单步跳回(f7)执行完当前行所在的**方法**，进入下一行

drop to frame 回到当前行所在方法的第一行
resume 恢复执行完当前行所在断点的所有代码，进入下一个断点，如果没有就结束
Terminate 终止停止 JVM, 后面的程序不会再执行

若step into 单步跳入方法不起作用 则因为使用的不是jdk里的jre。右击 ——Debug Configurations——JRE——修改Alternate JRE为jdk1.8.0xxx而不是jre1.8.0xxx(先remove再add)

 13.传参 右击 ——run as——Argument——Program arguments

14.选中名字  ctrl+t 查看类型层次结构

15.源码——包围方式——try-catch  快捷键alt shift z

常用快捷键

>

>1.补全代码的声明：alt + /
>* 2.快速修复: ctrl + 1
>* 3.批量导包：ctrl + shift + o
>* 4.使用单行注释：ctrl + /
>* 5.使用多行注释： ctrl + shift + /
>* 6.取消多行注释：ctrl + shift + \
>* 7.复制指定行的代码：ctrl + alt + down 或 ctrl + alt + up
>* 8.删除指定行的代码：ctrl + d
>* 9.上下移动代码：alt + up 或 alt + down
>* 10.切换到下一行代码空位：shift + enter
>* 11.切换到上一行代码空位：ctrl + shift + enter
>* 12.如何查看源码：ctrl + 选中指定的结构 或 ctrl + shift + t
>* 13.退回到前一个编辑的页面：alt + left
>* 14.进入到下一个编辑的页面(针对于上面那条来说的)：alt + right
>* 15.光标选中指定的类，查看继承树结构：ctrl + t
>* 16.复制代码： ctrl + c
>* 17.撤销： ctrl + z
>* 18.反撤销： ctrl + y
>* 19.剪切：ctrl + x
>* 20.粘贴：ctrl + v
>* 21.保存： ctrl + s
>Eclipse 的使用配置-宋红康
>* 22.全选：ctrl + a
>* 23.格式化代码： ctrl + shift + f
>* 24.选中数行，整体往后移动：tab
>* 25.选中数行，整体往前移动：shift + tab
>* 26.在当前类中，显示类结构，并支持搜索指定的方法、属性等：ctrl + o
>* 27.批量修改指定的变量名、方法名、类名等：alt + shift + r
>* 28.选中的结构的大小写的切换：变成大写： ctrl + shift + x
>* 29.选中的结构的大小写的切换：变成小写：ctrl + shift + y
>* 30.调出生成 getter/setter/构造器等结构： alt + shift + s
>* 31.显示当前选择资源(工程 or 文件)的属性：alt + enter
>* 32.快速查找：参照选中的 Word 快速定位到下一个 ：ctrl + k
>* 33.关闭当前窗口：ctrl + w
>* 34.关闭所有的窗口：ctrl + shift + w
>* 35.查看指定的结构使用过的地方：ctrl + alt + g
>* 36.查找与替换：ctrl + f
>* 37.最大化当前的 View：ctrl + m
>* 38.直接定位到当前行的首位：home
>* 39.直接定位到当前行的末位：end

IDEA的使用

Ctrl Alt T     快捷进行try + catch 等操作

## Typora

`[点击我跳转](#标题名)`注意#后直接跟标题名

>[**typora 出现空行 段落**](https://blog.csdn.net/minervalingxian/article/details/111814053)*千次阅读*
>
>2020-12-27 15:57:31
>
>**问题**：在 typora 中按回车，实际会自动产生一个空白行。
>
>**解释**：在markdown的源代码中，段落由两个或两个以上的空行分隔开。在Typora中，你只需要一个空行（按一次`回车`键）就可以创建一个新的段落。
>
>按下 shift + 回车 创建一个简单换行符。大多数其他的markdown语法分析程序会无视简单换行符。 为了让其他的markdown语法分析程序也能识别你的换行符，你可以在段落末尾留下两个空格或者插入<br/>。
>
>**解决方案**：行尾加 两个空格 再 按下 shift + 回车

插入音乐 可以贴外链播放器

折叠：

```html
<details>
    <summary>标题</summary>
    内容
</details>
```

<details>     <summary>标题</summary>      内容  </details>
```

```

## 宋红康老师小相声

《深圳の艳遇》https://www.bilibili.com/video/BV1Kb411W75N?p=547&t=787.6