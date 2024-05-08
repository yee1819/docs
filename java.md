---
title: java的学习
categories: 笔记
tag: java
description: 好久之前的java一些笔记
abbrlink: d7d7fe33
toc: true
toc_number: true
aside: true
---





# JAVA的学习

[toc]



:mi-two-tone check_circle green:



:fa fa-home fa-fw:


## 计算机相关知识

### 计算机硬件

- 总线
- - 中央处理器(CPU)
  - 内存（主存）
  - 存储设备（如硬盘，u盘，光盘）
  - 输入设备（键盘，鼠标等）
  - 输出设备（显示器，打印机）
  - 通信设备（调制解调器，网卡）

---



#### 中央处理器

英文缩写cpu，是计算机的大脑，从内存中获取指令，然后执行这些命令。

其中有控制单元：用于控制和协调其他组件的动作
算数/逻辑单元：用于完成数值运算（`+-*/`）和逻辑运算（><=）

计算机内有个内部时钟，以固定速度发射电子脉冲。时钟速度越快，在固定时间段内的执行指令就越多，速度的计量单位是赫兹（hz），一赫兹相当于每秒一个脉冲，目前的单位是以千兆赫(Ghz)来表述,电脑的频率一般为千兆赫GHZ

1khz=1024hz
1mhz=1024khz
1ghz=1024mhz



cpu的核是实现指令读取和执行的部分，一个多核cpu是以一个具有俩个或者更多独立核的组件。可提高cpu的处理能力

+++



#### 存储设备

内存：内存的数据断电缺失

永久存储数据

磁盘驱动器：即磁盘/硬盘，光驱（CD，DVD），USB闪存驱动器（即U盘，通用串行总线），软驱AB盘

+++





### 冯诺依曼体系结构

五大结构

- 运算器

  完成数据加工处理的加工器

- 控制器

  控制程序执行的控制器

- 存储器

  记忆程序和数据的存储器

- 输入设备

  输入数据和程序的输入设备

- 输出设备

  输出处理结果的输出设备

![冯诺依曼](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/%5Cmarkdown%E5%86%AF%E8%AF%BA%E4%BE%9D%E6%9B%BC.webp)

+++



#### 内存

计算机是一系列电路开关，0是关，1是开

一个0或者一个1是一个比特（bit），是计算机最小的存储单位。

计算机最基本的存储单元是字节（byte），每个字节由8个比特构成。单位是B
千字节(KB)=1024B
兆字节(MB)=1024KB
千兆字节(GB)=1024MB
万兆字节(TB)=1024GB

八个比特存储二进制的最高数是1024 ，所以存储单位进制是1024

内存（RAM） 由一个有序字节序列组成，用于存储程序及程序所需 的数据

cpu如果要调用硬盘 里的数据要优先让内存读取硬盘的数据，再有内存交付给cpu（目的是加快工作效率，硬盘慢CPU快，内存读取速度比硬盘快约10倍）

内存是带点存储，断电消失，容量有限，长期存储还得靠硬盘

内存在这一步起到的作用：
1. 保存从硬盘读取的数据，提供给cpu使用
1. 保存cpu的一些临时处理结果，以便下次使用或保存到硬盘

RAM最多，速度越快，但是有上限

+++



#### 输入输出设备

鼠标、键盘

显示器、打印机

+++



#### 通信设备

拨号调制解调器、DSL（数字用户线）、无线网络、网络接口卡、电缆调制解调器

+++



### 操作系统

管理和控制计算机的活动

```ascii
 |----------------------|
 V						V
用户<---->应用程序<--->操作系统<------>硬件
```

操作系统的主要任务：

- 控制和监视系统的活动
- 分配和调配系统资源
- 调度操作

+++

### 万维网

world wide web分为web客户端和web服务器程序。

www可以让web客户端（浏览器）访问web服务器的页面（网页）

URL统一资源定位符

URI统一资源标识符

超文本传输协议（Hypetext Transfer Protocol）**http协议，https协议是具有安全性的ssl加密传输协议**

万维网包含于因特网，因特网包含于互联网

架构：
B/S
browser server  （通过浏览器访问服务器）

C/S
client  server（通过客户端访问服务器） 

+++

## 常用DOS命令

用win+R输出cmd调出命令提示符

切换盘

```dos
C:\Users\Yee>d:

D:\>
```

dir：列出当前目录下的所有文件及文件夹

md：创建目录

rd：删除目录

cd：进入指定目录

cd..：返回上一级目录

cd\：返回根目录

del：删除文件

exit： 退出dos命令行

+++

#### 创建目录/移动目录/列出目录实例

```dos
C:\Users\Yee>dir
 驱动器 C 中的卷是 OS
 卷的序列号是 4805-CB1A

 C:\Users\Yee 的目录

2022/08/01  17:41    <DIR>          .
2022/08/01  17:41    <DIR>          ..
2022/05/05  12:33    <DIR>          .anaconda
2022/05/25  22:09    <DIR>          .android
2022/04/21  12:31    <DIR>          .cache
2022/05/14  01:59    <DIR>          .conda
2022/05/05  12:35                25 .condarc
2022/05/05  12:32    <DIR>          .continuum
2022/04/21  12:31    <DIR>          .eclipse
2022/05/14  01:44    <DIR>          .idlerc
2022/05/05  12:49    <DIR>          .ipython
2022/05/05  12:49    <DIR>          .matplotlib
2022/03/25  20:04    <DIR>          .Origin
2022/04/24  23:12    <DIR>          .p2
2022/05/14  02:08                27 .python_history
2022/03/25  20:04    <DIR>          .QtWebEngineProcess
2022/04/23  17:45    <DIR>          .redhat
2022/05/14  01:58    <DIR>          .spyder-py3
2022/01/11  13:22    <DIR>          .vscode
2021/10/15  20:36    <DIR>          3D Objects
2021/10/17  14:14    <DIR>          ansel
2021/10/15  20:36    <DIR>          Contacts
2022/04/14  13:25    <DIR>          Creative Cloud Files
2022/07/30  15:36    <DIR>          Desktop
2022/07/27  01:54    <DIR>          Documents
2022/05/28  19:50    <DIR>          Downloads
2022/04/21  12:23    <DIR>          eclipse
2021/10/15  20:36    <DIR>          Favorites
2022/05/05  12:50    <DIR>          Jedi
2021/10/15  20:36    <DIR>          Links
2021/10/15  20:36    <DIR>          Music
2022/08/01  17:45    <DIR>          OneDrive
2022/04/25  00:24    <DIR>          Pictures
2021/10/15  20:36    <DIR>          Saved Games
2021/10/15  20:38    <DIR>          Searches
2021/10/22  14:53    <DIR>          source
2022/08/01  17:41    <DIR>          Videos
2022/05/11  16:14    <DIR>          编程
               2 个文件             52 字节
              36 个目录 30,808,530,944 可用字节

C:\Users\Yee>md java

C:\Users\Yee>cd java

C:\Users\Yee\java>md hello.java

C:\Users\Yee\java>md class1

C:\Users\Yee\java>md class2

C:\Users\Yee\java>cd class2

C:\Users\Yee\java\class2>cd ..

C:\Users\Yee\java>cd\

C:\>
```

![image-20220801224825370](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/%5Cmarkdownimage-20220801224825370.png)

![image-20220801224845030](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/%5Cmarkdownimage-20220801224845030.png)

+++

#### 创建文件

```dos
C:\Users\Yee>cd java

C:\Users\Yee\java>echo hello,my name is 66>1.txt
```

![image-20220801225749867](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/%5Cmarkdownimage-20220801225749867.png)

```dos
C:\Users\Yee\java>echo hello,my name is xingtong>1.txt

C:\Users\Yee\java>

```

![image-20220801225845111](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/%5Cmarkdownimage-20220801225845111.png)

echo指令是替代文件内容到某个文件，若无文件则创建，若存在则替代

+++

```dos
C:\Users\Yee>cd java

C:\Users\Yee\java>del 1.txt

C:\Users\Yee\java>

```

![image-20220801230251871](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/%5Cmarkdownimage-20220801230251871.png)



+++

#### 删除文件

使用del可以删除文件

如果想批量删除一个格式的文件,如图所示有很多txt格式的文件

![image-20220801230502053](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/%5Cmarkdownimage-20220801230502053.png)

```
C:\Users\Yee\java>del *.txt
//*类似sql的*
```

![image-20220801230552004](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/%5Cmarkdownimage-20220801230552004.png)

+++

#### 删除目录

```dos
C:\Users\Yee\java>rd hello.java

```



![image-20220801231123355](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/%5Cmarkdownimage-20220801231123355.png)

<font size=5 color=red >当目录不为空，不允许删除</font>

```dos
C:\Users\Yee\java>cd..

C:\Users\Yee>rd java
目录不是空的。

```

<font size=5 color=red>当文件夹不为空又想删除时，在上一级目录使用del进行删除所有文件，再删除目录</font>

```
C:\Users\Yee>cd java

C:\Users\Yee\java>cd class1

C:\Users\Yee\java\class1>echo hello,world>1.docx

C:\Users\Yee\java\class1>

```

![image-20220801231706768](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/%5Cmarkdownimage-20220801231706768.png)

此时我的class1目录下的文件不为空

```dos
C:\Users\Yee\java\class1>cd..

C:\Users\Yee\java>rd class1
目录不是空的。
```

提示我不能删除

```dos

C:\Users\Yee>cd java

C:\Users\Yee\java>del class1
C:\Users\Yee\java\class1\*, 是否确认(Y/N)? Y

C:\Users\Yee\java>rd class1

C:\Users\Yee\java>
```

![image-20220801232037632](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/%5Cmarkdownimage-20220801232037632.png)





就能删除了



+++

## 浅识JAVA

  人机交互方式

图形化界面（GUI）、命令行方式（CLI）

JAVASE   标准版   支持面向桌面型应用

JAVAEE   企业版    开发企业环境下的应用程序解决方案针对Web应用程序开发

JAVAME  小型版    支持JAVA移动端的平台

JAVA Card    支持java小程序

+++

### 面向对象

三大特征：封装，多态，继承

基本概念：类，对象

+++

###  健壮性

吸收C/C++的特点，去掉C/C++的一些容易弄错的点，例如指针、内存申请与释放，多继承等等，提供一个相对安全的内存管理和访问机制

+++

### 跨平台性

由于java程序的特点，使用虚拟机（JVM）运行，可以在多个平台（windows，linux等等）上运行同一个java程序。

+++

### 核心机制

java虚拟机：JVM

垃圾收集机制

+++

### JDK

java开发工具包，其中包括JAVA开发工具和jre，开发工具包含：编译工具（javac.exe）和打包工具(jar.exe)等

+++

### JRE

包括java虚拟机(JVM)和JAVA程序的核心类库，想运行JAVA程序只需要有JRE就好

+++

### JVM

java运行的环境，虚拟机

+++

### 用命令行运行java程序

用记事本写好一个java程序，修改后缀为java

![image-20220802192446930](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/%5Cmarkdownimage-20220802192446930.png)



在cmd里实现

```java
//编译
C:\Users\Yee\java\class2>javac hello.java
//运行
C:\Users\Yee\java\class2>java hello
hello,world

```

+++

###  注释

与c/c++一样

```java
//单行注释
/*
多
行
注
释
*/


/**
这是文档注释
会被java内置的jdk提供的javadoc解析，生成一套以网页形式体现的该程序的说明文档
*/
```

以下是大概的使用方法概述

首先先写一个java程序，里面包含文档注释

```java
/**
 @author yxq
 @version v1.0
 测试文档的用法
 */
public  class hello{
    public static void main(String[]  args){
        System.out.println("hello,world");
    }
}
```

需要设置环境变量jdk才能通过命令行打开javadoc

小技巧，在需要打开cmd的路径前加上cmd和空格点回车打开的cmd就是当前目录下的cmd

或者直接在目录上输入cmd打开的cmd也是目录下的cmd

![image-20220803151328647](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/%5Cmarkdownimage-20220803151328647.png)

```java
 //命令行语句（尚硅谷讲的是）
javadoc -d  建立一个新文件夹的文件夹名  -author -version java文件名
//csdn查的资料是
javadoc -encoding UTF-8 -charset UTF-8 Doc.java
```

+++

也可以用idea等编译器生成文档

这里是idea的生成文档使用方法

![image-20220803152220242](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/%5Cmarkdownimage-20220803152220242.png)

![image-20220803152356217](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/%5Cmarkdownimage-20220803152356217.png)

遇到了几个问题javadoc:错误 - 无法读取 Input lenght=1 

不能生成文档，是因为不能存在中文路径名。换成英文就可以了。

![image-20220803153330401](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/%5Cmarkdownimage-20220803153330401.png)

这样就能生成使用文档了

+++

### java     api   文档

api 是接口

讲解了各个类名使用方法

+++

### 程序编写注意事项

一个java文件中，可以有多个class

但是只能有一个public class 

并且public class 后面的类名与文件名相同

程序的入口是main()方法格式 是固定的

```java
public  class hello{
    public static void main(String[]  args){
        System.out.println("hello,world");
    }
}
//args 是一个单词的缩写arguments 参数  可变
//即
public  class hello{
    public static void main(String[]  a){
        System.out.println("hello,world");
    }
}
//可运行
//中括号可以变
public  class hello{
    public static void main(String  a[]){
        System.out.println("hello,world");
    }
}
//也可运行
```

+++

编译后会生成一个或多个字节码文件，文件名与数量与java文件的class名字数量相同。

+++

## 开始

+++

### 关键字保留字

关键字：由java语言赋予特殊功能的单词或者字符串

保留字：现版本Java未使用，但以后的版本可能会使用，尽量避开使用例如goto、const

+++

### 标识符

对变量、方法、类，接口，包命名时使用的字符序列称为标识符（只要是能命名的都是标识符）

定义规则：由26个字母大小写，0-9  十个数字，_下划线,$，组成

注意：

- 数字不可以开头
- 不能使用关键字和保留字，可以包含关键字例如int是关键字不能使用，int_1可以使用
- java区分大小写，长度无限制
- 标识符不能包含空格

- 标识符可以为中文，但是尽量不用，以免造成编码不一致等等问题

+++

命名规范（不是强制要求，只是建议，增强代码可读性）

- 包名多单词组成时全小写，不同单词用__链接例如:     java_start_day1
- 类名、接口名：多单词组成时，首字母大写:   JavaStartDay1
- 变量名、方法名：多单词组成，第一个单词小写首字母，后面的单词首字母大写 ：javaStartDay1
- 常量名:所有字母大写，用下划线连接：JAVA_START_DAY1

+++

### 变量

变量存在于内存中一个存储区域

该区域的数据在同一类型范围内不断变化

变量是程序中最基本的存储单元，包含变量类型、变量名、存储的值

变量用于在内存中保存数据

变量必须先声明后使用

用变量名访问这块区域的数据

变量的作用域一般为所定义的{}内

变量在作用域中才可生效

同一个作用域中，不可以定义重名的变量 

+++

### 变量类型

+++

基本数据类型

整形：byte、short、int、long

浮点型：float、double

字符型：char

布尔型：boolean

+++

引用数据类型

类（class）、接口（interface）、数组（array）

+++

#### 整型

| 类型 | 长度 | 取值范围 |
| ---- | ---- | -------- |
|      byte|  8bit位(1byte)    | `-128~127`即-2^7^`~`2^7^-1         |
|short   |16bit位(2byte)|`-32768~32767`即-2^15^~2^15^-1|
|int |32bit(4byte)|`-2147483648~2147483647`即-2^31^~2^31^-1|
|long |64bit(8byte)|`-9223372036854775808~9223372036854775807`即-2^63^~2^63^-1|
|char |16bit|`'\u0000'~'\uffff'`即0~65535|

赋值long的时候需要在末尾加一个L或l

```
long a=23123213L;
long b=231232131l;                                                                                       
int c=2313;
```

+++

#### 浮点型

单精度float,精确到小数点后7位数

双精度double，精度是float的俩倍

浮点型由两种表达方式

十进制：4.23      42.33f     3.00

科学计数法：2.19e4   4.44E5   100e-2

| 类型   | 长度  | 取值范围             |
| ------ | ----- | -------------------- |
| float  | 4byte | -3.403E38~3.403E38   |
| double | 8byte | -1.798E308~1.798E308 |

java定义浮点型默认为double，声名float型常量则需要在后面加==f或F==

```java
float a=5.32f;
float b=4.55F;
double c=3.45;
```

+++

#### 字符型

char  1字符=2字节

```java
//定义char型变量，用''；
char c='a';
//一个char只能存储一个字符
char cc='ab';//错误
//可以输入中文或者数字或者其他国家语言
char ccc='啊';
char c2='1';
//也可以存储一个符号,包括转义子符
char c3='&';
char c4='\n';
//可以用unicode
char c5 = '\u0043';//是C

```

+++

#### 转义字符

| 字符   | 含义                    |
| ------ | ----------------------- |
| \ddd   | 1~3位八进制数表示的字符 |
| \uxxxx | 1~4位十六进制表示的字符 |
| `\'`   | 单引号’                 |
| `\"`   | 双引号”                 |
| `\\`   | 反斜杠\                 |
| `\r`   | 回车                    |
| `\n`   | 换行                    |
| `\f`   | 走纸换页                |
| `\b`   | 退格                    |
| `\t`   | 水平制表符tab键         |

+++

#### 布尔型

boolean只有两个值==true和false==,即真与否

```java
boolean a=true;
boolean b=flase;
```

+++

#### 类型转换



自动类型提升

范围小的和范围大的相运算，应用范围大的类型接收结果。

```java
byte a=12;
int b=223;
byte c=a+b;//错误
int c=a+b;//正确
long c=a+b;//正确
double c=a+b;
c=235.0
//而整型与浮点型运算都自动提升到浮点型
//char 与整型运算
int a=1;
char c='a';
int a1=a+c;//a1=98
//当char   byte    short   三个类型进行运算时，自动转化为int型
byte aa=12;
short a2=32;
char c='a';
//无论byte、short、char三种运算最后的结果由byte、short、char接收都不会成功
byte、char、short->int ->long->float->double
//高等级转化到低等级会出错
```

+++

强制类型转换

byte、short、char运算时该怎么办呢

```java
byte a=12;
short b=33;
short c=a+b;//错误
short c= (short) (a+b);//正确
//强制转换会造成精度损失
//浮点型变为整数型损失小数部分
double a=12.3;
int b=(int)a;//b=12
//超过数的精度时
int i=128;
byte b=(byte)i;b=-128//与二进制存储有关
```

+++

当long型定义时忘记写L时，会认为定义是int型，自动提升为long型

```java
long l1=123213;
long l2=22312312312312312111;//会报错，int型不允许这么长的变量存在，所以也就没了转化为long型的可能性
//同理，float型也是
float f1=12.3;//错误，默认为double，向下转换类型时失败，不允许向下自转
```

+++

整型常量默认int，浮点型默认double

```java
byte b=12;
byte b1=b+1;//编译出错，因为，1默认int型，导致b自动提升为int型，不能自动转化会byte，导致出错
float a=1.23f;
float b=a+1.1;//出错，理由同上。
```

+++

#### String字符串

引用数据类型，不算基本数据类型

```java
//声明String
String ch="1231232你好那";
//使用双引号，字符串。
//String可以和八种基本类型做运算，即连接运算
int a=99999;
String b="你好，";
String c=a+b;//c="你好，99999"
//其他逻辑、浮点型，布尔型等等都可以连接,以String型接收

//注意
char ch='a';
int num=10;
String str="hello";

System.out.println(ch+num+str);//107hello
System.out.println(ch+str+num);//ahello10
System.out.println(ch+(num+str));//ahello10
System.out.println((ch+num)+str);//107hello
System.out.println(str+num+ch);//hello10a
//string和多种数据类型计算时是根据左到右的顺序计算
//只要遇到string，后面的都是string连接了


//'a'+'b'+'c'和"a"+'b'+'c'不一样,字符型加号是做运算，字符串加号是连接

//String 转化为int型的方法为
int num1 =  Integer.parseInt(str1);
```

+++

#### 进制

计算机常用八进制，二进制，十六进制，十进制。

二进制   0b   0B   开头

八进制   0o   0O 开头

十六进制  0x   0X   开头   

```java
int a1 = 0b1100;//二进制
int a2 = 1100; //十进制
int a3 = 0o127;//八进制
int a4 = 0x1100;//十六进制
```

计算机内最高位    0正数    1负数

计算机底层以补码的方式存储数据！

二进制转八进制，三位二进制数看成一位八进制数范围0-7，八进制转二进制，每一个数字转为三位二进制数字拼接

二进制于十六进制转换也是如此

```java
二进制 000 101 111
八进制  0   5   7
```



+++

### 运算符



#### 算术运算符

```java
+
1+1=2
   
-
2-1=1
    
*
4*5=20
/
40/8=5
41/8=5//自动转int取整    
double a=41/8;//a=5.0
double a=41/(double)8;//5.125
double a=41.0/8;//5.125
%
41%8=1
-41%8=-1
41%-8=1
-41%-8=-1
//被模数符号决定了    
++
i=1;
x=++i;//x=2
y=i++；//y=1
运算符在前面的先运算在赋值
运算符在后面则先赋值再运算
--
i=1;
x=--i;//x=0
y=i--；//y=1
//自增自减的时候不会自动转化为int型，即不改变变量本身数据类型

```

+++

#### 赋值运算符

| 符号 | 效果              |
| ---- | ----------------- |
| `=`  | `赋值,a=3,c=b=6;` |
| `+=` | `a+=4同a=a+4`     |
| `-=` | `a-=4同a=a-4`     |
| `/=` | `a/=4同a=a/4`     |
| `%=` | `a%=4同a=a%4`     |
| `*=` | `a*=4同a=a*4`     |
|      |                   |

注意，a+=5与a=a+5,不同点，前者不会改变数据类型

```java
//即
short a=5;
a+=5;//不会出错
a=a+5;//a会先转int型，导致不能转化更小级别的short，出错
```





+++

#### 比较运算符

| 运算符       | 运算                                                 |
| ------------ | ---------------------------------------------------- |
| `==`         | 等于                                                 |
| `!=`         | 不等于                                               |
| `>`          | 大于                                                 |
| `<`          | 小于                                                 |
| `>=`         | 大于等于                                             |
| `<=`         | 小于等于                                             |
| `instanceof` | 检查是否属于对象"hello" instanceof String   返回true |

运算结果均为布尔型



+++

#### 逻辑运算符

| 符号 | 作用   |
| ---- | ------ |
| `&`  | 逻辑与 |
| `&&` | 短路与 |
| `|`  | 逻辑或 |
| `||` | 短路或 |
| `^`  | 异或   |
| `!`  | 非     |

```java
//&与&& 的区别


public  class hello{
    public static void main(String[]  arg){
        boolean a1=false,a2=false;
        int num1=10,num2=10;
        if(a1&(num1++>0)){

        }
        if(a2&&(num2++>0)){

        }
        System.out.println("num1 = "+num1);
        System.out.println("num2 = "+num2);
    }
}

//输出结果为
//num1 = 11
//num2 = 10

//逻辑与和短路与的区别就在这里，当前面的判断有一个为false时，短路与  后面的语句不会运算，逻辑与   会继续运算
```



```java
//  |   与   ||   的区别
public  class hello{
    public static void main(String[]  arg){
        boolean a1=true,a2=true;
        int num1=10,num2=10;
        if(a1|(num1++>0)){

        }
        if(a2||(num2++>0)){

        }
        System.out.println("num1 = "+num1);
        System.out.println("num2 = "+num2);
    }
}

//num1 = 11
//num2 = 10

//短路或在获得一个true条件时，不会继续后面的运算，而逻辑或会继续运算
```

短路与和短路或效率稍微高一些



| a     | b     | a&b   | a&&b  | `a|b` | `a||b` | `!a`  | `b^a` |
| ----- | ----- | ----- | ----- | ----- | ------ | ----- | ----- |
| true  | true  | true  | true  | true  | true   | false | false |
| true  | false | false | false | true  | true   | false | true  |
| false | true  | false | false | true  | true   | true  | true  |
| false | false | false | false | false | false  | true  | false |

异或：先取反，在判断是否或





+++

#### 位运算符



| 位运算符 | 作用                                                         |
| :------: | :----------------------------------------------------------- |
|   `^`    | 异或，两个二进制数中位数相同为0，不相同为1                   |
|   `|`    | 或，返回两位数都为0的值，否则返回1                           |
|   `~`    | 取反，把二进制数的0变为1，1变为0                             |
|   `>>`   | 右移，a>>n,把a的二进制数向右移动n位，相当于a=a//2^n^，可以做除法,当a>>1的时候相当于a//2 |
|   `<<`   | 左移，a<<n,把a的二进制数向左移动n位，相当于a=a`*`2^n^，可以做除法,当a<<1的时候相当于a`*`2 |
|   `&`    | 与，返回两位二进制数都为1 的部分，可以判断奇偶，例3&1=1，2&1=0，1的二进制是01，2是10，3是11，1&3即01与11都为1 的数是个位的1，2&1没有相同位数上的1，即为0，通过这样的方式判断奇偶 |

这里是异或的示例

<img src="https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/markdown/位运算的异或.png"/>

这里是或的示例

<img src="https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/markdown/位运算的或.png"/>

这里是取反示例

![位运算取反](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/markdown/%E4%BD%8D%E8%BF%90%E7%AE%97%E5%8F%96%E5%8F%8D.png)

这里是左移与右移

![位运算左移右移](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/markdown/%E4%BD%8D%E8%BF%90%E7%AE%97%E5%B7%A6%E7%A7%BB%E5%8F%B3%E7%A7%BB.png)

这里是与的示例

![位运算的与&](https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/markdown/%E4%BD%8D%E8%BF%90%E7%AE%97%E7%9A%84%E4%B8%8E&.png)



> 补充：右移时，如果是负数，用1补左边，正数用0补前面
>
> `>>>`无符号右移，无论正数负数都是左边补0

```java
//位运算的一些小用法

//1 交换值
int num1=1,num2=2;
num1 = num1 ^ num2;
num2 = num1 ^ num2;
num1 = num1 ^ num2;
```



+++

#### 三目运算符

 格式：条件表达式 ?  表达式1:表达式2

符合条件表达式进入表达式1，否则进入表达式2

类似： if (条件表达式){
	表达式1
}else{
	表达式2
}

```java
public  class hello{
    public static void main(String[]  arg){
        int num1=99;
        String str = (num1+1>=100)?"yes":"no";
        System.out.println(str);
    }
}
//输出yes

//同
public  class hello{
    public static void main(String[]  arg){
        int num1=99;
        String str ;
        if(num1+1>=100){
            str = "yes";
        }else{
            str = "no";
        }
        System.out.println(str);
    }
}
```

表达式有数据类型要求，字符串和整型不能同时满足

故三元运算可以转化 if-else  结构  但是   if_else 结构 不一定可以转化三元运算

```java
int m,n;
(n>m)?"m大":55;//编译错误
```

三元运算可以嵌套使用

```java
String in = ( n > m)  ? "n大" : ( ( n < m) ? "m大" : "一样大" ) ;
```

+++

三元运算、单目运算，赋值运算是从右往左运算的，其他都是从左往右运算

+++

### 流程控制

流程控制 大体可以分为  顺序结构，分支结构和循环结构



+++

#### 顺序结构

顺序结构 即按照顺序从上往下一步一步地执行语句





+++

#### 分支结构

##### if-else分支

```java
if(判断语句){
    若为  true 执行语句
}

Boolean a  =  true;
if(判断语句){
    若为  true 执行语句
}else{
    若为 false 执行语句
}


//分支可以嵌套

if(判断语句){
    若为  true 执行语句
        if(判断语句2){
            若为  true 执行语句
        }
    	if(判断语句3){
            若为  true 执行语句
        }else{
            若为  false 执行语句
        }
}else if(判断语句5){
    若为 false 执行语句
        if(判断语句4){
            若为  true 执行语句
        }else{
            若为  false 执行语句
        }
}else if(判断语句6){
    
}else{
    
}

```

+++

##### switch分支

```java
switch(表达式){
    case 常量:
        结构;
        break;
    case 常量:
        结构;
        break;
    default:
        结构;
        break;
}
//其中default可以省略，作为不满足所有case条件的补充
//再有，case条件内若无break，执行完结构语句则玩下继续执行下一个内容
switch(表达式){
    case 1:
        结构1;
       
    case 2:
        结构2;
        break;
    default:
        结构;
        break;
}
//即表达式是1，进入case1，执行结构1，此时无case，继续执行结构2，遇到break，退出

switch(表达式){
    case 1:
        结构1;
        break;
    case 2:
        结构2;
        break;
    default:
        结构;
        break;
}//若为这个情况，表达式值为1，则执行结构1遇到则退出
```

switch结构表达式的值为   int 、byte 、 short 、 char 、 枚举类型（jdk1.5新增）、 String（jdk1.7新增）

default可以不放在末尾，运行会查看满不满足case，不满族进入default，运算后检测若无break，则继续往下运行。

+++

##### 另一种switch结构

在写代码的过程中使用switch结构，当忘记了break的书写，稍稍不留心就会出大茬子，在jdk12之中引入了一种新的switch结构，可以不需要break就可以实现结束switch结构

```java
import java.util.*;


public  class Hello{
    public static void main(String[]  arg){
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        switch(n){
            case 1 -> System.out.println(n*100);
            case 2 -> System.out.println(n);
            default -> System.out.println("不是1也不是2");

        }
    }
}
>>1
100
>>2
2
>>3
不是1也不是2    

//注意，当case里有许多语句时，需要用括号括起来，不加括号会报错
public  class Hello{
    public static void main(String[]  arg){
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        switch(n){
            case 1 -> System.out.println(n*100);
            case 2 -> {
                System.out.println(n);
                System.out.println("这是2" );
            }
            default -> System.out.println("不是1也不是2");

        }


    }
}


//新的switch语法可以返回值
public  class Hello{
    public static void main(String[]  arg){
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        int x=switch(n){
            case 1 -> n*10;
            case 2 -> n+10;
            default -> 0;
        };//注意这里需要分号结尾
        System.out.println("x="+x);
    }
}
//这里的x接收了switch返回的值。
```



+++

#### 循环结构



+++

##### for循环

```java
for(初始表达式[可省略，放置循环体外]:迭代条件[不可省略，为布尔值，为true运行，false退出循环]:迭代表达式[可省略，放置循环体内]){
    循环语句;
}
与c语言相同
//迭代条件可以为空，可以省略，会导致死循环，需要设置break。    
```



+++

##### while循环

```java
while(循环条件[布尔值，true进入循环，false退出]){
    循环体;
}
```



+++

##### do....while循环

```java
do{
	循环体;    
}while(循环条件[布尔值，true进入循环，false退出]);
//do...while 循环与while循环的差距是while循环进入时判断条件是否为true，是进入循环，false则退出循环。
//do...while循环不论条件是否为false，都会进行一次循环，再判断条件是否成立选择退出还是继续循环

```

+++

- 循环语句的条件判断可以是true

- 在循环语句里设置break可以跳出循环，可以搭配if条件选择使用。
- 循环可以嵌套使用，多使用一层循环会导致计算时间大幅度上升，慎用多级嵌套
- 







++++

### 输入输出

从输入设备输入数据是需要使用Scanner对象

```java
//导入包
import java.util.Scanner;//也可以使用    import  java.util.*     使用所有java的util包
public class Scannertest{
    public static void main(String[] args){
        
        //Scanner对象实例化
        Scanner oo = new Scanner(System.in);//oo即为实例化的Scanner对象
        //Scanner对象的方法
        int num = oo.nextInt();//nextInt 是指接收数字
        System.out.println(num);
    }
}

Scanner in = new Scanner(System.in);

String name = in.next();
String name2 = in.nextLine();
int age = in.nextInt();
double weight = in.nextDouble();
Boolean panduan = in.nextBoolean();

Scanner未定义接收char型，可以使用next()接收一个字符串再取第一个字符的方式接收char型
String sex = in.next();
char sex_1 = sex.charAt(0);//此处为0指取出在索引零位存储位置的字符
//这样我们就能输入char字符型变量了


//输入格式与接收格式需要一致，若不一致如果不能向上提升数据类型会报错。

```

+++

输出格式

```java
System.out.print();//输出一行内容，不换行
System.out.println();//相对于上面的格式会输出完自动换行
System.out.printf();//格式化输出，具体同c语言

int num = 36;
String name = "小明";

System.out.println(name+"今年"+num+"岁了");
//小明今年36岁了
int num_2 = 12;
System.out.println(num+num_2+name);
//48小明
System.out.println(name+num+num_2);
//小明3612



System.out.printf("%s今年%d岁了",name,num);
//小明今年36岁了


//format格式化输出



```

+++

format输出

字符串中用format函数进行精度输出

```python
>>>print("我的名字是{}，小名是{}".format("kiko","suki"))
我的名字是kiko，小名是suki
>>>print("我的名字是{1}，小名是{0}".format("kiko","suki"))
我的名字是suki，小名是kiko
>>> print("我的名字是{0}，小名是{1}".format("kiko","suki"))
我的名字是kiko，小名是suki
>>> print("我的名字是{0}，小名是{1}".format("kiko",6666))
我的名字是kiko，小名是6666
#以上是简单的位置输出格式

```

format是一个使用起来十分强大的格式控制

<img src="https://yee-1312555989.cos.ap-guangzhou.myqcloud.com/markdown/py输出.png"/>

```python
#冒号前面的数字是后面的字符串数字
#例子
>>> a="{:_^25}".format("张三")
>>> print(a)
___________张三____________
#其中25 是总共输出的长度，而25前的‘^’是对其方式，在填充方式前的是当输出内容少 ，不足以填满长度而填充的字符
#如果不指明填充的字符，则默认空格
#千分位例子
>>> print("{0:*>25,}".format(9876543210))
************9,876,543,210
#每隔三个数字添加一个‘，’
>>> print("{0:0>25,}".format(9876543210))
0000000000009,876,543,210
#精度例子
#如果要求保留俩位小数
>>> qq=0.12333
>>> print("{:.2}".format(qq))
0.12
#不过在整数部分变成非零后我不知道为什么会变成科学计数法
>>> qq=231.123214
>>> print("{:.2}".format(qq))
2.3e+02
#修改输出类型
#和c语言差不多的，b表示二进制，c表示字符，d表示整数型，o表示八进制，x表示十六进制
#X是十六进制X大写，E和e是科学计数法表示浮点数的大小写e，f是标准浮点数输出
#%表示百分比输出浮点数
>>> a=100
>>> print("{:b}".format(a))
1100100
>>> print("{:c}".format(a))
d
>>> print("{:d}".format(a))
100
>>> print("{:o}".format(a))
144
>>> print("{:x}".format(a))
64
>>> print("{:X}".format(a))
64
>>> a=31202
>>> print("{:X}".format(a))
79E2
>>> print("{:x}".format(a))
79e2
#以下是浮点数
>>> a=2.4223
>>> print("{:e}".format(a))
2.422300e+00
>>> print("{:E}".format(a))
2.422300E+00
>>> print("{:f}".format(a))
2.422300
>>> print("{:%}".format(a))
242.230000%
```

format函数的另外一个输出方法

```python
#这是f-string输出方法
>>>name="张三"
>>>age=18
>>>print(f"我是 {name} ，我今年 {age} 岁")
我是 张三 ，我今年 18 岁
>>> print(f"{name:-^25}")
-----------张三------------
#输出的方式余format差不多，唯一的区别是f-string的方法不需要在后面使用format函数。
#直接在输出时候填入变量，控制格式即可
```

