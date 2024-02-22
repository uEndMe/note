todo cbs 

143 String的实例化与连接操作

# 第11章 常用类和基础api 5.java比较器


# JavaEE

[API 文档](https://docs.oracle.com/en/java/javase/17/docs/api/index.html)		[oracle 官网](http://www.oracle.com)        [bilibili](https://www.bilibili.com/video/BV1PY411e7J6/)        [github中文笔记](https://zq99299.github.io/java-tutorial/java/)

```
面向对象的高级编程语言。
```

```
体系：
	javaSE		标准版		桌面应用
	javaEE		企业版		web应用
	javaME		微型版		嵌入式设备，移动设备，等其他设备
	
版本：
	java				1995.05
	java 5.0		2004.09
	java 8.0		2014.03
	java 17.0		2021.09
	
跨平台：
	通过再各个操作系统上安装JVM虚拟机，让java在JVM中运行。
```

```
神书：《Java核心技术》 《Effective Java》 《Java编程思想》
```

````
优质笔记：https://github.com/zq99299/repository-summary
面试笔记：https://github.com/CyC2018/CS-Notes
````



# 安装配置

```
windows 全局环境配置。
```



### JDK8

[JDK8 下载](https://www.oracle.com/java/technologies/downloads/#java8)

#### 安装

```
account: 695381719@qq.com
password: abcd1234.A
```

```
安装步骤：下一步/更改路径/下一步/安装.../更改路径/下一步/安装.../关闭
```

```
JDK:		集成开发工具包。JRE + javac + java + javadoc ...
  JRE:		运行环境。JVM + java核心类库
    JVM:		虚拟机
```



#### 环境变量

```
电脑/右键/属性/高级系统设置/高级/环境变量(N).../系统变量
```

```
1. 删除默认java环境变量：
	系统变量/path/选择/
	C:\Program Files(x86)\Common Files\Oracle\Java\javapath
	
2. 新建变量：
	变量名： JAVA_HOME
	变量值： H:\ProgramFiles\JDK\a
	
3. 添加path:
	系统变量/path/添加/
	%JAVA_HOME%\bin
	
4. 测试
	cmd/java/回车
	cmd/javac/回车
```

* 使用

```java
目录下CMD/回车/
编译：javac HelloWorld.java  // 生成类名文件
运行：java HelloWorld	// 执行类文件
```



### IDEA

```
集成开发工具
```

[官网](https://www.jetbrains.com/zh-cn/idea/)    [破解文档](https://oaugj4oxm5m.feishu.cn/docx/RVfdda7uKoKcyJxiCXmcpBMEnGd)



#### 起步

```
破解版		ideaIU-2023.2.4.exe
```

* 安装

```
下载/安装/完成/开启/关闭/
```

* 破解

```
解压idea.zip/双击/IDEA激活.vbs/success/完成
```



#### 新建项目

```
新建项目/
	名称：JavaSECode
	位置：D:\_\db\20231028_my_db\javaProject
		v 创建 Git 仓库
	语言：Java
	构建：IntelliJ
	JDK: 17
	v 添加示例代码
		v 使用入门提示生成代码
创建/
```

#### JDK 设置

```
文件/项目结构/项目设置/项目/

Name							项目名称
SDK								JDK版本
Language level		限制编辑语言版本规范
Compiler output		编译目录 out
```



#### 详细设置

```
文件/设置/
```



##### 系统设置

```
// 取消自动更新
设置/外观与行为/系统设置/更新
 x IDE更新
 v 插件更新
 V 显示新功能
```



##### 项目文件编码

```
/编辑器/文件编码/
	全局编码		UTF-8
	项目编码		UTF-8
	
	属性文件		UTF-8
		v 自动转换
	创建UTF-8	 不含 BOM
```



##### 控制台编码

```
/编辑器/常规/控制台/
	默认编码		UTF-8
```



##### 文档注释

```
/编辑器/文件和代码模板/Include/File Header
```

```

/**
*
* @author chenbaoshui ${YEAR}-${MONTH}-${DAY} ${TIME}:00
*/
```



##### 自动编译

```
/构建,执行,部署/编译器/
 v 自动构建项目
 v 并行编译独立模块
```



#### ----



#### 工程与模块管理

```
// 层级结构
工程 > 模块 > 包 > 类
project > module > package > class
```

```
// 清除根代码
删除/src

// 新建模块
/项目名/右键/新建/模块/
	名称：		part001-module
新建/
```

```
// 包名
src/
	// 一般以公司网址倒序为包名：如： 
	com.srm.user-module // 顶级域名.公司名.模块名
```

```
// 删除模块
模块/右键/移除/
模块/右键/删除/
```



#### 代码模板

```
// 后缀补全
/编辑器/常规/后缀补全/
	v 启用后缀补全
	
// 实时模板
/编辑器/实时模板/
```

```
// 自定义实时模板
/编辑器/实时模板/+/新增组/xxx/
/新增模板/
	略缩名称  描述
	代码片段
	应用语言范围
```



#### 快捷键

```
本地文档：/db/book/IDEA快捷键.md
```



#### DEBUG

```
设置/按字母顺序排序值
打断点/调试/

步过：下一步
步入：进入方法
强制步入：进入系统方法
步出：退出
跳转：跳转到光标处

恢复
结束
查看断点
禁用断点
```



#### 插件

```
// 版本控制忽略文件
.ignore (3.2.3.193)

// 阿里规范
Alibaba Java Coding Guidelines

// 正则大全
any-rule

// 驼峰转换
CamelCase
alt + shift + u 转下划线

// 代码预言
Codota AI Autocomplete for Java and JavaScript (4.2.10)

// 彩虹日志 
Grep Console
颜色配置：
fatal	CD201F	FFFFFF
error	FFF2F0	FF4D4F
warn	FFFBE6	FAAD14
info	-	9EAEFF
debug	-	96D996
trace	-	ADADAD

// 实体工具支持
Lombok

// Mybatis 跳转
MyBatisX

// 驼峰翻译
Translation (2.9.4-193)

// ---- ---- ---- 未使用 ---- ---- ----

// 国际语言支持
i18n support

// web 工程转换
JBLJavaToWeb (1.4.3)

// github 阅读器？
Sourcegraph

// boot 创建向导
Spring Assistant (0.12.0)
```



#### 版本控制

```
详见：git章节
```

# ----



# 基本语法



### 起步

```java
// UserController.java
public class UserController {
  public static void main(String[] args) {
    System.out.println("打印字符~~");
  }
}
```

```
javac UserController.java
java UserController
```



#### 注释

```java
// 单行注释
/* 多行注释 */
/**
	@name 文档注释
	@describe 通过javadoc生成文档注释信息
*/
```



#### 关键字

[官方地址](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/_keywords.html)

> 本地文档：/db/book/【了解】尚硅谷_Java关键字汇总说明.pdf

```
特殊意义的单词。
```

```java
// 数据类型
void
class interface enum
byte short int long float double char boolean

// 流程控制
if else
switch case break
while do for continue return
  
// 默认流程语句，默认抽象方法，默认注解值
default
  
// 权限修饰符
public protected 缺省 private
    
// 类关系
class extends implements
  
// 实例
new this super instanceof
  
// 异常
try catch finally throw throws
  
// 包
package import
  
// 字面量
true false null
  
// 其他修饰符
static					静态 // 变量，方法，代码块，内部类
native					原生方法 // 方法
final						常量 // 类，变量，方法，局部变量
abstract				抽象 // 类，方法
synchronized		同步 // 方法，代码块
volatile				原子 // 变量
strictfp				严格浮点 // 类，接口，方法
transient				临时 // 变量 // 不会序列化
  
// 断言
assert
  
// 保留字
const goto
```



#### 标识符

```
用于命名的单词。
类，变量，方法，包等命名的字符序列。
```

```
命名规则：
	1. 允许字符：a-Z0-9_$ 
	2. 非法字符：关键字保留字特殊值
	3. 非法开头：0-9
	（不含空格，严格大小写）
	
命名规范：
	1. 见名知意
	2. 类，接口：首字母大写
	3. 变量，方法：小驼峰
	4. 包：xx.yy.zz
	5. 常量：XXX_YYY
```



#### 变量

```java
// 对值的具名引用
int x = 1;
```

```
// 概念
* 内存中的一个存储区域，该区域的数据可以在同一类型范围内不断变化
* 变量的构成包含三个要素：数据类型、变量名、存储的值
* Java中变量声明的格式：数据类型 变量名 = 变量值
```



#### 语句

```java
* 语句
    
  * 声明				// int xx;
  	* 声明一个当前方法栈的变量
  
  * 表达式			 // 变量运算/方法调用
  	* 经过计算，返回一个结果

  * 流程控制		 // if/switch/while/for...
  	* 条件，if，基于调节或范围
  	* 枚举，switch，基于值
  	* 循环，持续执行，直到条件满足
  	* 迭代，迭代一系列的值
  
  * 块 				// { xx(); xxx(); }
  	* 语句集合，将其视为一条语句
```



#### 包

```
类和接口的分组。提供访问保护，命名空间管理
```

```
com.atguigu.test
一级域名.项目名.模块名
```

```java
package com.atguigu.test; // 声明包 （类）

import java.util.Scanner; // 导入包 （类）
import java.util.*; // 导入包下所有类

public class Test1 {
    public static void main(String[] args) {
        // ...
    }
}
```



### 运算符


```java
// 比较相等
== !=					判断相等
instanceof		判断实例所属类
  
// 特殊
.						访问属性
=						赋值
()					转换类型 // 大转具体
->					Lambda
```



#### 布尔运算

```java
// 逻辑运算
! ^	& |					逻辑：非，异，与，或
&& ||						短路：与，或 // 推荐短路逻辑
  
// 条件
?:						条件判断 // x ? 1 : 0
```



#### 数学运算

```java
// 自增 // 计算中，形成操作数栈。
++a --a				前自增 // 先自增，在入栈
a++ a——				后自增 // 先入栈，再自增
~							按位非 // 二进制，全反
!							逻辑非 // 取反
()						括号，提升优先级 // a+(b+c), 先算a,再算b+c

// 比较/关系
< > <= >=		判断大小
== !=				判断相等
  
// 算术
+ - * / %			算术

// 位运算
~						按位非 // 二进制，全反
^						按位异 // 二进制，异
&						按位与 // 二进制，与
| 					按位或 // 二进制，或
<<					左移 // 放大n个二进制	*2^n
>>					右移 // 缩小n个二进制	/2^n(舍去小数)
>>>					无符号右移 // 同右移（强制取正）

// 赋值
= *= /= %=		赋值，乘除赋值  // short,byte 自带强制转换
+= -= <<= >>=	加减赋值，位移赋值
>>>= &= ^= |=	按位赋值
```



#### 运算顺序

```
1. 根据优先级分割因数
2. 从左向右进行计算  // 条件，赋值除外？
		a. 计算中，每个因数依次入栈，然后进行计算
```

```
后缀：.() [] {}

算术：++ -- ~ ！+ - * / %
位移：<< >> >>>

关系：> >= < <= instanceof == !=
逻辑：& ^ | && ||

条件： ?:
赋值： = *= %= /= += -= >>= <<= >>>=
```



#### 类型转换

```java
// 自动类型转换
byte -> short -> int -> long-> float-> double
				 char -> int
```

```
* 有变量时；整型默认int，浮点默认double
* 该运算不会自动转换类型？
+= -= 等赋值运算
```

* 强制类型转换

```java
// 数据类型 变量名 = （数据类型）被强转数据值；
int n = (int)3.14;
```



### 流程控制

```
用于控制语句的执行顺序
三种流程：顺序结构，分支结构，循环结构
```

#### 分支结构

```java
// 条件语句
if() {...}else if() {...} else {...}
switch() { case 1: xx; break; case 2: xx; break; default:xx; }
xx ? a : b;
```

```
* switch 支持变量：byte,short,int,char,enum,String
```

```java
* JDK 12 
  
// 支持多个case合写 （case合并，不穿透）
switch(month){
	case 3,4,5 -> System.out.println("春季");
  default -> System.out.println("默认季节");
}

// 返回值
String res = switch(month){
    case 3,4,5 -> "春季";
    default -> "未知季节";
}
System.out.println(res); // 春季
```



#### 循环结构

```java
// 循环语句
while() {...}
do {...} while ();
for(int i = 1; i == 2; i++){...} // for(初始化;判断;更新){}
for(int x: arr){...}

// 跳转语句
break; // 跳出整个循环及switch
continue; // 跳转到下一个循环 
	// 跳转点：for 更新语句， while/do while 判断语句
```



> * while 循环
>
> ```
> 0.初始化
> while (1.循环条件){
> 	2.循环体 （循环操作）
> 	3.循环变量 （迭代）
> }
> ```
>
> ```
> 01 -> 231 231 231 ...
> ```



> * do while 循环
>
> ```
> 0.初始化
> do{
> 	1.循环体（循环操作）
> 	2.循环变量 （迭代）
> } while (3.循环条件);
> ```
>
> ```
> 0123 -> 123 123 123 ...
> ```
>
> ```
> * 适用于 循环条件依赖循环操作 （如判断重复，需要输入）
> ```



> * for 循环
>
> ```
> for(0.初始化;1.循环条件;3.循环变量){
> 	2.循环体
> }
> ```
>
> ```
> 0123 -> 123 123 123 ...
> ```
>
> ```
> * 适用于：循环次数固定
> ```



> * 循环嵌套
>
> ```
> 循环内部嵌套另一个循环。
> 二层循环：平方面积
> 三层循环：立方体积
> ```
>
> ```
> 生产环境：可控性，安全性 // 循环变量不要跳跃，不要多次修改
> ```



> 一重循环实现双重循环公式
>
> ```
> y = (X^2+X - n)/2
> x = [-1 ± √(1 + 8y + 4n)]/2
> 
> x:边
> y:面积
> n:起始点 （三角形转梯形，顶部宽）
> 
> 1+4y必须是>=0的，否则无解
> ```
>
> ```
> for(int i = 1; i <= 5 * 5; i++) {
> System.out.print("*");
> // [-1 ± √(1 + 8y + 4n)]/2 == 1,2,3...
> if (i % 5 == 0) System.out.println();
> }
> ```





### 基本类型

```
值存储，副本传递，栈存储
```

```
类型			字节		范围
byte			1			-128  ~  127
short			2			-3,2768  ~  3,2767
int				4			-2^31  ~  -2^31-1		(直接量默认) // 2.14E9
long			8			-2^63  ~ 2^63-1			(L)				 // 9.22E19

float			4			6 ~ 7位							 (F)
double		8			15 ~ 16位						 (直接量默认)

boolean		1			false,true

char			2			\u0000~\uffff				( 0~65535 )
```



> * 扩展
>
> ```
> 进制：
> 	计算机中只有二进制，使用二进制存储运算数据。	
> 	// 进制表示：ob10,010,0x10
> 	
> 补码：
> 	如： -1
> 	原码： 1000 0001		// 略
> 	反码： 1111 1110		// 符号位不变，按位取反
> 	补码：	1111 1111		// 反码 +1
> ```
>
> ```
> ASCII编码表：	// 128位，大小写差值32
> 	0		48
> 	A		65
> 	a		97
> 	
> \u0000 等控制字符会破坏后尾字符？
> ```
>
> ```
> 8 bit			= 1 Byte
> 1024 Byte	= 1 KB
> 1024 KB		= 1 MB
> 1024 MB		= 1 GB
> 1024 GB		= 1 TB
> ```
>
> ```
> 转义符：\n \t \" \' \b \r
> ```



### 引用类型

```
字符串，数组，类，接口，枚举，注解，记录
"", [], class, interface, enum, @interface, record
```



#### String

```
多个字符的有序集合。
```

```java
// 声明 // 支持 unicode 写法
String s = "这是字符串";
```

```java
// 转义序列
	\b  空格
  \t	制表
  \n	换行
  \f	换页
  \r	回车
  
// 原本含义
  \"
  \'
  \\
```

```
* 详见：常用类与API/字符串/String
```



#### 数组

```
值的有序集合。 // 用于存储固定大小的同类元素
```

```java
// 动态声明 （元素未定）
int[] arr = new int[3];

// 静态声明 （编译时已知数据）
int[] arr = {0,1,2}; // 类型推断 仅支持初始化
int[] arr = new int[]{0,1,2}; // 赋值
```

```
* 数组使用需要开辟内存空间，给出长度和类型。
* 数组定长：分配内存空间时，必须定长度，长度不变
```

```
// 内存分析
虚拟机栈：存放方法中声明的变量，如数组的引用
堆内存：存放对象，如数组中的元素
```



> * C 风格
>
> ```
> // 动态声明
> int arr[] = new int[5]; // 动态声明数组
> // 静态声明
> int arr[] = {1,2,3,4}; // 静态声明 （仅支持初始化）
> int arr[] = new int[]{1,2,3}; // 静态声明
> ```





##### 二维数组

* 声明

```java
// 动态声明 (元素未定)
int[][] arr = new int[5][3]; // 同时给出一维二维长度
int[][] arr = new int[5][]; // 给出一维长度（外层）

// 静态声明
int[][] arr = {{1,2},{3,4}}; // 类型推断 仅支持初始化
int[][] arr = new int[][]{{1,2},{3,4}}; // 赋值
```



> * C 风格
>
> ```
> // []乱放，不推荐
> int[] arr[] = {1,2};
> int arr[][] = {1,2};
> ```
>
> ```
> int x, y[]; //x是int，y是数组
> int[] x, y[]; //x是一维数组，y是二维数组
> ```



##### 算法

```java
// 二分查找
public static int dichotomy(int[] arr, int v){
  // 参数：命中区间，开始，结束
  int s = 0;
  int e = arr.length - 1;

  // 合法区间
  while(s <= e) {

    // 二分，命中
    int mid = (s + e) / 2;
    if(v == arr[mid]) {
      return mid;
    }

    // 更新区间：右边，左边
    if(v > arr[mid]){
      s = mid + 1;
    } else {
      e = mid - 1;
    }

  }
  return -1;
}
```



[十大经典算法](https://www.cnblogs.com/guoyaohua/p/8600214.html)

<img src="db\img\十大经典排序算法.png" alt="十大经典排序算法" style="zoom:50%;" />

```java
// 冒泡排序
public static int[] bubble(int[] arr) {
  
  // 列：0 ~ length - 2
  for (int i = 0; i < arr.length - 1; i++) {
    
    // 行：(0 ~ (length - 2)) - 列
    for (int j = 0; j < arr.length - 1 - i; j++) {
      
      // 冒泡
      if (arr[j] > arr[j + 1]) {
        int tmp = arr[j + 1];
        arr[j + 1] = arr[j];
        arr[j] = tmp;
      }
    }
  }
  return arr;
}

// 快速排序
public static int[] quick(int[] arr) {
    return quick(arr, 0, arr.length - 1);
}
private static int[] quick(int[] arr, int start, int end) {
    if (start >= end) {
        return arr;
    }

  	// 标记：左一为中位数
    // base/l -------- r
    int base = arr[start];
    int l = start;
    int r = end;

    // ---->> base/l/r <<----
    while (l < r) {

      	// 位移：从右到左，找到小值，移动到左空
        // base/l <<<<---- r
        while (l < r) {
            if (arr[r] < base) {
                arr[l] = arr[r];
                l++;
                break;
            }
            r--;
        }

      	// 位移：从左到右，找到大值，移动到右空
        // base/l ---->>>> r
        while (l < r) {
            if (arr[l] > base) {
                arr[r] = arr[l];
                r--;
                break;
            }
            l++;
        }
    }

  	// 位移：将中位值插入到分界点
    // ---- base/l/r ----
    if (l != start) {
        arr[l] = base;
    }

  	// 递归：按中位值分界，左递归，右递归
    // l1 ---- r1 base l2 ---- r2
    quick(arr, start, l - 1);
    quick(arr, l + 1, end);
    return arr;
}
```



#### class

```
类：实例对象的模板，属性和行为的规范。
```

```
实体类：存放实体数据
工具类：操作数据的工具
```

```java
package com.atguigu.test; // 包位置
 
public class Student{
  // 成员变量
  String name;
  int age;
  
  // 成员方法
  void sayHellow(){
    System.out.println("你好");
    return ; // 返回 // 结束方法
  }
}
```

```java
package com.atguigu.test; // 包位置
public class Test1{
  public static void main(String[] args) {
    // 实例化
    Student tom = new Student();
    
    // 调用属性
    tom.name = "tom";
    tom.age = 20;
    
    // 调用方法
    tom.sayHello();
  }
}
```


#### interface

  ```
类规范。所有实现类必须拥有的属性/方法
  ```

```java
public interface Person {
	String NAME = "tom"; // 属性：公开静态常量
	public void say(); // 方法：公开抽象
  	// JDK 1.8 开始
	public default void start() {} // 默认方法
	public static void show() {} // 静态方法
}
```

```java
// 实现类
public class Teacher implements Person {
  @Override
	public void say() { } // 必须实现抽象方法
}
```


> ```
> 面向接口编程：所有引用位置使用接口。
> ```




* 单继承多实现

```
一个继承 + N个接口
```



#### enum

```
一组预定义的常量，隐式继承 Enum
```

```java
public enum Season { // 枚举 // 一诺
  SPRING("春"),SUMMER("夏"),AUTUMN("秋"),WINTER("冬");
  private String info;
  Season(String info) { // 构造方法：私有
    this.info = info;
  }
  @Override
  public String toString() {
    return info;
  }
  public static Season get(int i) {
    return values()[i];
  }
}
```

* 枚举方法

```
1.toString(): 属性名
2.name():属性名
3.ordinal():索引
4.values():枚举的数组
5.valueOf(String name)：属性名 -> 枚举元素
```



> ```
> // JDK1.5之前的枚举
> public class Seacon {
> // 枚举对象
> public static final Season A = new Season("春");
> public static final Season B = new Season("夏");
> public static final Season C = new Season("秋");
> public static final Season D = new Season("冬");
> // 属性
> 	private String info;
> 	// 私有所有构造方法
> 	private Season(String info) {
> 		this.info = info;
> 	}
> }
> ```





####  annotation 

```
一种元数据形式，提供了一个不属于程序本身的程序数据
（运行时注解，会编译进.class文件）
```



###### 基本注解

```java
@Override											// 重写检测
@Deprecated										// 弃用标记
@SuppressWarnings("unused")		// 抑制警告 // 类型
```

> ```
> * 抑制类型：all, unchedked, unuesd ...
> ```



###### 元注解

```java
用于修饰注解 			// 注解的注解
```

```java
@Target				// 生效范围
		ElementType // 枚举值
    		TYPE,METHOD,CONSTRUCTRO,PACKAGE...
    
@Retention		// 生命周期 （滞留阶段）
		RetentionPolicy
        SOURCE	// 源代码。仅存在于.java源代码中，不编译入.class
        CLASS		// 字节码。仅存在于类上,对象创建出来就消失了。
        RUNTIME // 运行时。编译进.class文件。

@Documented		// javadoc记录
@Inherited		// 可继承，允许子类继承父类中的注解
```

```java
@Target(ElementType.METHOD)
@Retention(RetentionPolicy.SOURCE)
public @interface Test{
	String a(); // 注解的变量属性
  String b();
}
```

```java
@Test(a = "参数", b = "参数")
public void method(){}
```

> * 简写
>
> ```java
> @Target(ElementType.METHOD)
> @Retention(RetentionPolicy.SOURCE)
> public @interface Test{
> 	String value(); // 仅有一个value时，简写
> }
> ```
>

> ```java
> @Test("参数") // 注解变量简写
> public void method(){}
> ```
>



###### 文档注释

```
/**
 * 注释说明
 *
 * @author		作者
 * @version		版本
 * @see				参考
 * @since			启用版本
 * @param			形参名 形参类型 形参说明
 * @return		返回值类型 返回值说明
 * @throws		异常类型 异常说明
 * @exception	异常类型 异常说明
 */
```



###### 自定义注解

```
1. 必须有处理流程
1. 只能使用反射读取
3. 必须是 RetentionPolicy.RUNTIME
```



#### record

```
Java 16 新特性：record类
```

```java
public record Person(
  String name,
  String sex,
  int age) {
  
}
```

```
* final类
* 自动实现equals、hashCode、toString函数
* 成员变量均为public属性
```



# 面向对象

```
从宏观上，整体上，设计程序的编程风格。
```

```
面向过程(POP)：分步骤解决问题。
面向对象(OOP)：调用对象方法解决问题。
```

> ```
> 将系统按照功能/特征/模块进行拆分，封装为对象
> 通过调用对象解决问题，关注系统的结构
> ```



### 类和对象

```
面向对象三大特性：封装，继承，多态
```

```
* 类：对象的模板，属性和行为的规范。
* 对象：符合类要求的实例。
* 属性：状态信息
* 行为：动作能力
```

```java
public class FileName{
  public static void main(String[] args) {
    // 使用对象
    Person jack = new Person();		// 实例化
    jack.name = "jack"; 					// 调用属性（属性赋值）
    jack.sya(); 									// 调用方法；
  }
}

// 声明类
class Person {
  String name;  					// 属性
  public void say() {}  	// 方法
  public Person() {}  		// 构造方法
}
```



#### 变量类型

```java
package com.atguigu.test; // 包位置
public class Student{
  // 成员变量
  String name;
  
  // 类变量
  static String school;
  
  void sayHellow(){
    // 局部变量
    String hellow = "你好";
    return hellow;
  }
}
```

```java
局部变量： 
	声明：方法，构造方法，语句块。 
	// 声明，初始化，销毁都在该方法中。
	
成员变量：
	声明：类中，方法体之外。  
	// 对象实例化时，创建。 
	// 访问：类中方法、构造方法，特定类的语句块
	
类变量： （静态）
	声明：类中，方法体之外。 
	// 必须为 static 类型
```



#### 修饰符

* 权限修饰符

```
public				公共。任何
protected			保护。本包，子包访问
缺省 					 普通。本包访问
private				私有。仅本类访问
```

* 特殊修饰符

```java
static
	类的属性和方法
final
	不能重写，不能修改 [1]
	* 修饰类：不能被继承
native
	原生，方法体为C语言
abstract
	抽象类
synchronized
	同步方法
	
// 其他修饰符
native					原生方法 // 方法
volatile				原子 // 变量
strictfp				严格浮点 // 类，接口，方法
transient				临时 // 变量 // 不会序列化
```

```
[1] 常量：
	成员：未赋值，需在构造前赋值
	局部：未赋值，需在调用前赋值
```



#### 面对对象

```
// 完成面对对象的三步骤
1. 类的定义
2. 对象的创建
3. 对象调用属性或方法
```



#### 匿名对象

```
创建后直接调用,不保存引用地址
```

```java
// 匿名对象
new Persion().say()
```



#### 匿名类

```java
// 匿名类创建对象，一般用于继承并重写方法，可直接调用方法
new Thread() {
    @Override
    public void run() {
        System.out.println("~~");
    }
}.start();
```



### 成员变量

```java
class Person {
  
  /** [修饰符...] 数据类型 变量名 [ = 初始值 ] */
  private String name;

}
```

```
* 修饰符：权限，静态，常量，原子，临时
```



### 成员方法

```
重载，参数传递,重写
```

```java
class Person {
  /*
  修饰符 返回类型 方法名 (参数类型 形参) {
		方法体
  }
  */
  public void set(String str) {
    return str + "xxx";
  }
}
```



#### 组成

```
常规部分：	访问修饰符，返回类型，方法名，参数组，方法体
非常规：特殊修饰区, 抛出异常区
```

```
* 访问修饰符
	public,protected,缺省,private
	
* 返回类型
	数据类型，void
	
* 方法名
	小驼峰命名
	
* 参数组
	定义时：形参 // (类型 参数名) // 形参无值，形式上的参数
	调用时：实参 // 按需传参：类型，要求，顺序
	
* 方法体
	{} // 大括号中
```

> ```
> * 参数传递机制：值传递
> 	* 基本类型：数据值
> 	* 引用类型：地址值
> ```
>
> ```
> * 其他修饰符：
> 静态，原生，常量，抽象，同步，严格浮点
> ```



#### 可变参数

```java
// 变长参数组
public static void method(int... nums) {
  for(int n: nums) {}
}
```

> ```
> // 可变参数模拟
> method(new int[]{0,1,2,3});
> ```



#### 方法重载

```
方法重载：同名方法，参数组不同（类型，个数，顺序）
```

```java
public class Person {
  void method() { }
  void method(int i) { } // 方法重载
}
```

```
* 当重载为子类/父类时，优先本态，兼容多态
```



#### 方法重写

```
子类方法与父类重名
```

```
修饰符：
	* 不能权限降级
	* static 不能重写，缺省 挎包不能重写
	
返回类型：
	* 基本类型 必须一致
	* 引用类型 可以是衍生类
```

> ```
> @Override // 检查方法重写是否规范
> ```



#### 递归

```
方法自己调用自己
```



### 构造器

```
用创建对象，并初始化属性。
```

```
Constructor // 构造器
特点：与类同名，没有返回类型
使用：仅在创建对象时调用，且必须调用
```

```
加载顺序：
	预编译 > 静态属性 > 静态代码块 >
	super > 属性 > 代码块 > 构造方法体
	this...
```

```java
public class Student {
  private String name;
  private int age;
  
  public Student(String name, int age) { // 构造器
    super();// 首行调用父类 // 默认
    this.name = name;
    this.age = age;
  }
}
```

```java
Student lisi = new Student("李四", 20);
```



> ```
> 标准JavaBean
> * 类必须是具体和公共的
> * 必须有无参数的构造方法
> * 成员变量私有化，并提供set和get方法
> ```

> ```
> 没有显示构造方法时，自动配备默认构造方法
> ```
>
> ```
> Student()
> 	实例化整个类
> 	super() -> 属性/方法 -> 代码块 -> 构造函数
> ```
>
> ```
> super() 
> 	会实例化整个父类,创建一个被继承对象：
> 	属性/方法 -> 代码块 -> 构造函数
> ```
>
> ```
> 类初始化时
> 类变量，类方法，会进行预编译 （类似变量提升）
> ```



#### this

```
当前对象
```



#### super

```
父类对象，用于访问继承的父类属性
```

```
构造函数中，首行调用（隐式调用）
```

```java
public class Pet {
  public Pet(String name, int age, String gender) {
    this.name = name;
    this.age = age;
    this.gender = gender;
  }
}
```

```java
public class Dog extends Pet{
  // 构造方法
  public Dog() {
    // 父类首行调用 // 显示调用
    super("旺财",3,"公");
  }
}
```



### 代码块

```
普通代码块：创建对象
静态代码块：类加载 // 用于静态属性赋值
```

```java
public Person {
	{ } // 普通代码块
	static{ } // 静态代码块
}
```



> ```java
> // 执行顺序
> public Person {
> 
> Person() {
>  // super() // 首行调用默认supper
>  // init // 初始化属性
>  // {} // 调用代码块
>  System.out.print(111);// 调用构造器主体
> }
> 
> }
> ```



### 内部类

```
一个类声明在类体中
```

```java
public class Outer {
	class Inner { } // 成员内部类
  static class Inner2 { } // 静态内部类
  public void method() {
    class Inner1 { } // 局部内部类
  }
}
```



#### 静态内部类

* 外部类

```java
内部声明：静态成员，普通成员
外部访问：静态成员
```

* 其他类，使用

```java
// 其他类 // 类外使用
public class Run {
  public static void main(String[] args) {
    // 其他类使用静态内部类
    Outer.Inner inner = new Outer.Inner();
  }
}
```



#### 成员内部类

* 外部类

```java
内部声明：普通成员
外部访问：静态成员，普通成员
```

* 其他类，使用

```java
// 其他类 // 类外使用
public class Run {
  public static void main(String[] args) {
    Outer outer = new Outer(); // 实例化外部类方式
    // 其他类使用成员内部类
    Outer.Inner1 inner1 = outer.new Inner1();
  }
}
```

> ```
> // 匿名外部类方式
> Outer.Inner1 inner2 = new Outer().new Inner1();
> ```



#### 局部内部类

* 方法内

```java
不是类的成员，没有修饰符。
内部声明：普通成员
外部访问：静态成员，普通成员
使用顺序：先声明，后使用
```

* 其他类，使用

```java
// 其他类 // 类外使用
public class Run {
  public static void main(String[] args) {
    // 其他类使用静态内部类
    Outer.Inner inner = new Outer.Inner();
  }
}
```



#### 匿名内部类

```java
局部内部类的一个子分类
```

```java
public class Run {
  public static void main(String[] args) {
    // 匿名内部类，作为接口的实现类
    Interface inter = new Interface(){
      @Override
      public void method() {} // 实现方法
    };
  }
}
```

> ```
> // 匿名对象方式·一
> new Interface(){
> @Override
> public void method() {} // 实现方法
> }.method();
> ```
>
> ```
> // 匿名对象方式·二
> fn(new Interface(){
> @Override
> public void method() {} // 实现方法
> });
> ```

### ----



### 封装

```
将类的内部信息隐藏在内部，仅提供可操作的对外接口。
高内聚，低耦合的体现
```



#### 数据封装

```
// 权限修饰符
public				公共。任何
protected			保护。本包及子包
缺省 					 普通。本包
private				私有。本类
```



#### 封装实现

```java
// 私有化属性
public class Student {
  private String name;

  public getName() {
    return name
  }
  public setName(String name) {
    this.name = name
  }
}
```

> ```
> Alt + Insert /生成/getter和setter/
> ```



### 继承

```
* 继承父类所有属性，方法
* 构造器需要手动调用super
```

```java
public class Pet {
  String name;
  int age;
}
```

```java
public class Dog extends Pet{
	private String type;
}
```



> ```
> * 单继承
> * 默认继承Object
> ```
>
> ```
> * 提高代码复用性
> * 提高代码扩展性
> * 多态的基础
> ```



### 多态

```
引用父类对象时，传入子类对象。
编译时声明宽松的父类型，运行时传入具体的子类型，调用方法。
```

```
实现：
	* 继承实现父子类
	* 子类重写方法
	* 父类引用子类对象
```

```java
public class Pet {
  public void play() {}
}

public class Cat extends Pet {
  public void play() {
    System.out.print("撸猫");
  }
}

// 继承
public class Dog extends Pet {
  // 重写
  public void play() {
    System.out.print("遛狗");
  }
}
```

```java
Dog dog = new Dog(); // 本态 // 优先
Pet dog = new Dog(); // 多态 // 只能访问 Pet 属性
```



> ```
> 子类对象赋值为父类引用时。
> 视为父类类型，只能访问父类属性。
> * 子类重写的方法具有多态性。
> ```



#### 向上转型

```java
Pet pet = new Dog(); // 向上转型（自动完成）
```



#### 向下转型

```java
Dog dog = (Dog)pet; // 向下转型（手动完成）
```

```
多态时，子类独有属性不可访问
通过向下转型，访问独有属性
```

#### instanceof

```java
obj instatnceof Object; // 类型检测
```

#### Object

```
根父类，所有引用类型的超类
```



  ### 抽象类

```
为了更好的实现多态
```

```
* 抽象类不能实例化
* 抽象方法没有方法体
```

```java
public abstract class Pet{
	public abstract play();	
}

// 实现类
public class Dog extends Pet {
  // 实现方法
  public void play() {
    System.out.print("遛狗");
  }
}
```



#### 虚方法调用

```
编译阶段不能确定方法的调用入口地址，运行时确定（被重写的方法）
```



### ----





### 内存解析

```
堆（Heap）：所有的对象实例。
栈（Stack）：指虚拟机栈。存储局部变量等。
方法区（Method Area）：用于存储已被虚拟机加载的类信息、常量、静态变量、即时编译器编译后的代码等数据。
```



#### 属性内存

![普通属性和静态数据的内存空间](db\img\普通属性和静态数据的内存空间.png)



```java
加载类： // 方法区
  1. 普通属性签名
  2. 分配静态属性空间
  3. 方法签名
  
实例化：// 堆
	1. 分配属性内存空间
```

```
* 签名：保留变量信息，暂时不开辟内存空间
```

> ```
> 类的加载时机：
> 	默认类，预加载
> 	首次实例化时，从顶层父类开始加载
> 	之后实例化时，加载过的类无需加载，从未加载的顶层父类开始加载
> ```



#### 方法内存

![方法压栈](db\img\方法压栈.png)

```
方法调用：
	1. 方法压栈 // 在栈空间分配内存，于底部
	2. 子方法压栈 // 于顶部入栈，分配空间
	3. 子方法出栈 // 顶部出栈，回收空间
	4. 方法出栈
```

```
* 静态方法：类名/对象调用
* 普通方法：只能对象调用
```



#### 包装类

| 序号 | 基本数据类型 | 包装类（java.lang包） |
| ---- | ------------ | --------------------- |
| 1    | byte         | Byte                  |
| 2    | short        | Short                 |
| 3    | int          | **Integer**           |
| 4    | long         | Long                  |
| 5    | float        | Float                 |
| 6    | double       | Double                |
| 7    | char         | **Character**         |
| 8    | boolean      | Boolean               |
| 9    | void         | Void                  |

* 装箱与拆箱

```
装箱：基础 -> 对象
拆箱：对象 -> 基础
```

```java
// 装箱
Integer n1 = new Integer(100);
Integer n2 = Integer.valueOf(100);
// 拆箱
int n3 = n1.intValue();
```

> ```
> jdk 1.5 开始 自动装箱拆箱
> ```



### UML 类图

```
// 含义
+ 			public 类型
#				protected 类型
-				private 类型
斜体		 抽象类/方法
```

```
User
____________________
- name : String
- age: Integer
____________________
+ getNmae() : String
+ setName(String) : void
# eat() : void
```

> ```
> // idea 快捷键
> Ctrl + Alt + U: 弹窗类图
> Ctrl + Shift + Alt + U: 标签类图
> ```



### ----



----

```

```







### 



# 常用类与API

>本地文档：\db\book\JDK_API_1.6_zh_中文.CHM



### 基本

#### Object

```
根父类，所有引用类型的超类
```

* 方法

```java
Object.toString(Object);	// 转String
Object.equals(Object);		// 判断相等
```



#### Integer

* 方法

```java
Integer.parseInt(String);		// 转int
```



#### Double

* 方法

```java
Double.parseDouble(String);	// 转double
```





#### Arrays

```java
java.util.Arrays			// 数组工具
```

* 静态

```java
// 操作
fill();				// 填充 // arr,val
fill();				// 填充范围 // arr,s,e,val
sort();				// 排序 升序
sort();				// 排序 部分 a,s,e

// 运算

binarySearch();		// 二分查找 // arr,val
binarySearch();		// 二分查找范围 // arr,s,e,val
equals();					// 相等 // arr1,arr2
deepEquals();			// 深度相等 // arr1,arr2
  
// 收集
copyOf();					// 复制 // arr,len
copuOfRange();		// 复制范围 // arr,s,e
asList();					// 换列表（包装类数组）// arr
asList();					// 换列表（散列） // el...
toString();				// 转字符 // arr
deepToStreing();	// 深度转字符 // arr
```



#### ----



#### System

```
java.lang.System
```

* 静态

```java
in;								// 输入流（键盘）
out;							// 输出流（显示器）
	out.print();				// 打印
  out.println();			// 打印换行
err;							// 错误输出流（显示器）

currentTimeMillis(); 	// 时间戳
nanoTime();						// 纳秒 （仅测量时长）
arraycopy(); 					// 数组复制 // a,0,b,0,len
exit(0); 							// 退出系统
gc(); 								// 运行垃圾回收器
getProperty(); 				// 系统属性
```

```java
// 系统属性
	java.version		// java 运行时环境版本
  java.home				// java 安装目录
  os.name					// 操作系统名称
  os.version			// 操作系统版本
  user.name				// 用户名
  user.home				// 用户目录
  user.dir				// 当前工作目录
```



#### Runtime

* 静态

```java
getRuntime();				// 运行时对象
```

* 方法

```java
totalMemory();			// 总内存
freeMemory();				// 空闲内存
```



#### Scanner

```
java.util.Scanner
```

```java
import java.util.Scanner; // 引入扫描仪
public class FileName{
  public static void main(String[] args){
    // 实例化扫描仪
    Scanner input = new(System.in);
    
    // 接收数据
    boolean bo = input.nextBoolean(); // boolean
    byte b = input.nextByte(); // byte
    short s = input.nextShort(); // short
    int i = input.nextInt(); // int
    long l = input.nextLong(); // long
    float f = input.nextFloat(); // float
    double d = input.nextDouble(); // double
    String str = input.next(); // String // 不支持空格
    char ch = input.next().charAt(0); // char
  }
}
```

> ```
> // 实例化扫描仪
> java.util.Scanner input = 
> 	new java.util.Scanner(System.in);
> ```
>
> ```
> // 接收字符串 // 不推荐
> String line = input.nextLine();
> ```



#### ----



### 字符串

#### String

```
// 类特性
* final						// 不可被继承
* Serializable		// 可序列化 // 用于网络传输
* Comparable			// 可比较
* char[] value		// 底层存储容器 // jdk9+ 改为 byte[]
```

```
// 存储位置
* 存储在字符串常量池 // StringTable
* 不存在相同常量字符串
* 存放于方法区 // jdk7+ 改为 堆空间
```



##### 编码解码

```java
// String -> String
new String();
new String(String s);

// Char -> String （解码）
new String(char[] c);
new String(char[] c, int start, int leng); // 起始，长度

// Byte -> String （解码）
new String(byte[] b);
new String(byte[] b, String charset); // 字符集("UTF-8") // java.nio.charset.StandardCharsets.UTF_8

// X -> String （解码）
String.valueOf(T t);
```

```java
// string -> char[] （编码）
.toCharArray();

// string -> byte[] （编码）
.getBytes();
.getBytes(String charset); // 字符集("UTF-8") 

// ...
```



##### 常用方法

```java
length();					// 字符数
trim();						// 修剪
intern();					// 常量池引用地址

int indexOf(String s);						// 查找, 匹配首位
int lastIndexOf(String s);				// 末尾查找, 匹配首位
String substring(int s, int e);		// 截取, 起点/终点(不含)
char charAt(int index);						// 提取

contains();							// 包含判断
endsWith();							// 结尾判断
startsWith();						// 开头判断
equals();								// 等值判断
equalsIgnoreCase(); 		// 等值判断，忽略大小写
compareTo();						// 比较，正数为 >
compareToIgnoreCase(); 	// 比较，忽略大小写

toUpperCase();		// 转大写
toLowerCase();		// 转小写
replace();				// 替换字符
```



##### 正则

```java
replaceAll(String reg, String rep);			// 替换所有
replaceFirst(String reg, String rep);		// 替换首个
```

```java
// 替换字符串
"xx.txt(2)".replaceAll("[\\(\\d\\)]", "");  // xx.txt
"abc".replaceFirst("([A-Z])", "_$1"); 			// _abc
```

```java
// 复用正则
Pattern reg = Pattern.compile("[\\(\\d\\)]");
String s = "xx.txt(2)";
reg.matcher(s).replaceAll(""); // xx.txt

// 复用正则
Pattern reg = Pattern.compile("([A-Z])");
String s = "abc";
reg.matcher(s).replaceAll(""); // _abc
```





##### 内存分析

```java
String s = "xx";	// 常量池
String s = new String("xx"); // 堆

// 1. 常量：常量池
// 2. 变量：堆
// 3. intern()：返回常量池
```

```java
// 字符串拼接问题
String s = "xx" + "xx"; // 常量池
String x = s + "xx" // 堆
  
// * s 字面量赋值时，结果在常量池
// * s 作为表达式变量时，结果x在堆
```





#### StringBuilder

```
速度快，线程不安全 * 推荐
```

```java
new StringBuilder(String str); // 实例化
```

```java
append();				// 追加
toString();			// 转字符

insert();				// 插入 // index,val
delete();				// 删除 // start,end
deleteCharAt();	// 删除 // index
setCharAt();		// 替换 // index,val
reverse();			// 反转
setLength();		// 定长 // length
replace();			// 替换 // strat,end,val
indexOf();			// 索引 // val
lastIndexOf();	// 索引 // val
substring();		// 截取 // start,end
```



#### StringBuffer

```
旧类，线程安全
* 方法同上
```





### 时间

```java
// 时间包
java.time 					// 包含值对象的基础包
java.time.temporal 	// 包括底层框架和扩展特性
java.time.zone 			// 包含时区支持的类  
java.time.format 		// 格式化和解析时间和日期
java.time.chrono 		// 提供对不同的日历系统的访问
```

```java
// 设计原则
* 明确，null参数，报空指针
* 流式，链式调用，不含空值
* 不可变，新对象必须为副本
* 扩展，可拓展
```

```java
// 时间体系
	java.time
		* Date // 日期时间
		
	java.util
		* 机器时间
			* Instant // 瞬时，基于时间戳
    
		* 人类时间
			* LocalDateTime 	// 本日日期时间，不含时区
			* LocalDate 			// 本地日期，不含时区
			* LocalTime 			// 本地时间，不含时区
			
			* ZonedDateTime 	// 时区日期时间
    	* OffsetDateTime  // 时差日期时间
    
    	* Duration 		// 持续，时间时长（时分秒）
    	* Period 			// 周期，日期时长（年月日）
    
    	* Clock // 时钟
```



#### Date (弃用)

```java
// 实例化
new Date();					// 当前
new Date(Long long);				// 解析，时间戳
Date.from(Instant instant);	// 解析，瞬时

// 查询
date.getTime();							// 时间戳（毫秒）
System.currentTimeMillis(); // 时间戳

// 转换
toInstant();			// 转瞬时
```



* SimpleDateFormat

```java
java.text.SimpleDateFormat // 格式化
```

```java
SimpleDateFormat f = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");

f.parse("2021-12-16 14:42:18"); // Date
f.format(new Date()); 					// 2021-12-16 14:42:18
```

```java
SSS		// 毫秒 // 999
E			// 星期 // 星期一
Z			// 时区 // +0800
```



* Calendar  (JDK1.1)

```java
java.util.Calendar	// 时间，修改时间
```

```java
Calendar cal = Calendar.getInstance(); // 创建
cal.getTime(); // 转Date
cal.get(Calendar.YEAR); // 获取年
cal.add(Calendar.YEAR,10); // 修改时间
```



* Timestamp

```java
long now = System.currentTimeMillis();

//  实例化
Tiemstamp s = new Timestamp(now); 			// 实例化
Timestamp.valueOf(String s); 						// "1900-1-1 0:0:0" // 解析
Timestamp.valueOf(LocalDateTime date);	// 解析
Timestamp.from(Instant i); 							// 解析

// 查询
getTime();						// 时间戳

// 转换
toString();						// "1900-01-01 00:00:00.0"
toLocalDateTime();		// 转日期时间
toInstant();					// 转瞬间
```



#### 接口

```java
TemporalAccessor	// 时间访问
	* TemporalField		// 时间单位
	* TemporalQuery		// 时间属性
	
Temporal					// 时间操作
	* TemporalAdjuster // 时间调节器

TemporalAmount		// 时长
	* TemporalUnit			// 时长单位
```



##### TemporalAccessor

```
时间查询接口，用于查询时间属性明细
```

```java
isSupported(TemporalField field);   // 单位 - 是否支持查询
range(TemporalField field);         // 单位 - 可选范围
get(TemporalField field);           // 单位 - 值
getLong(TemporalField field);       // 单位 - long值

query(TemporalQuery query);					// 查询 - 内容
```



###### TemporalField

```
时间点单位，如：年月日，时分秒（非时长）
```

```java
// 接口方法
略...
```

```java
// 年月日
ChronoField.YEAR;
ChronoField.MONTH_OF_YEAR;
ChronoField.DAY_OF_MONTH;
// 周
ChronoField.DAY_OF_WEEK;
// 时分秒
ChronoField.HOUR_OF_DAY;
ChronoField.MINUTE_OF_HOUR;
ChronoField.SECOND_OF_MINUTE;
```

```java
// 获取小时
LocalDateTime now = LocalDateTime.now();
int hour = now.get(ChronoField.HOUR_OF_DAY);
```



###### TemporalQuery

```
时间查询器，如：日期，时间，精度
```

```java
// 查询时间
R queryFrom(Temporal);
```

```java
// 参数：时间，时间查询器
LocalDateTime now = LocalDateTime.now();
TemporalQuery<LocalDate> query = TemporalQueries.localDate();

// 调用方法一 // 日期
LocalDate date = query.queryFrom(now);

// 调用方法二 // 日期（推荐）
LocalDate date = now.query(query);
```



* 实现类

```java
// 实现类 // 枚举 TemporalQueries.*
zoneId();      // 时区
chronology();  // 纪元
precision();   // 精度
zone();        // 宽松时区
offset();      // 时差
localDate();   // 日期
localTime();   // 时间
```



##### Temporal

```
时间操作接口，用于时间调节及计算 // 配合时长参数
```

```java
isSupported(TemporalUnit unit);		// 单位 - 是否支持加减

// 调节时间
with(TemporalAdjuster adjuster);	// 调节时间
with(TemporalField field, long newVal); // 调节时间，单位，值

// 计算加减
plus(TemporalAmount amount); // 加减时间，时长
plus(long v, TemporalUnit unit); // 加减，值，时长单位

minus(TemporalAmount amount);
minus(long v, TemporalUnit unit);

// 计算时长 // 等价：DAYS.between(s, e)
long unitl(Temporal e, TemporalUnit u); // 间隔，目标，单位
```


###### TemporalAdjuster

```
时间调节器，如：下周一
```

```java
// 调节时间
temporal adjustInfo(temporal);
```

```java
// 参数：时间，时间调节器
LocalDateTime now = LocalDateTime.now();
TemporalAdjuster nextWeekOne = TemporalAdjusters.next(DayOfWeek.MONDAY);

// 调用方法一 // 下周一（推荐）
LocalDateTime t = now.with(nextWeekOne);

// 调用方法二 // 下周一
LocalDateTime t = nextWeekOne.adjustIno(now);
```

> ```
> // 调节时间，单位，值
> with(TemporalField field, long newVal);
> ```



* 实现类

```java
// 实现类 // 枚举 TemporalAdjusters.*
ofDateAdjuster(localDate -> localDate); // 自定义调节器
firstDayOfMonth(); // 当月首日
lastDayOfMonth(); // 当月尾日
firstDayOfNextMonth(); // 次月首日
firstDayOfYear(); // 当年首日
lastDayOfYear(); // 当年尾日
firstDayOfNextYear(); // 次年首日

firstInMonth(DayOfWeek.MONDAY); // 当月首个周几
lastInMonth(DayOfWeek.MONDAY); // 当月末个周几
dayOfWeekInMonth(2, DayOfWeek.MONDAY); // 当月第二个周几
next(DayOfWeek.MONDAY); // 下周几
nextOrSame(DayOfWeek.MONDAY); // 下周几(含今日)
previous(DayOfWeek.MONDAY); // 上周几
previousOrSame(DayOfWeek.MONDAY); // 上周几(含今日)
```



##### TemporalAmount

```
时长接口，时间计算的必要参数
```

```java
// 单位 - 值
long get(TemporalUnit unit);

// 所有单位，从大到小，如：年月日
List<TemporalUnit> getUnits();

// 添加到指定日期，并返回 // temporal.plus(amount)
Temporal addTo(Temporal temporal);

// 减去到指定日期，并返回 // temporal.minus(amount)
Temporal subtractFrom(Temporal temporal);
```



* 实现类

```
Duration // 时长
Period // 时期
```



###### TemporalUnit

```
时长单位， 如：年月日，时分秒（非时间点）
```

```java
// 接口方法
between();		// 总时长 // 如总天数
略...
```

```java
// 年月日
ChronoUnit.YEARS;
ChronoUnit.MONTHS;
ChronoUnit.DAYS;
// 周
ChronoUnit.WEEKS;
// 时分秒
ChronoUnit.HOURS;
ChronoUnit.MINUTES;
ChronoUnit.SECONDS;
```

```java
// 明天
LocalDateTime now = LocalDateTime.now();
LocalDateTime next = now.plus(1, ChronoUnit.DAYS);
```






#### ----

#### 方法约定

```java
// 方法命名约定
static of();			// 精准实例化。严格验证每个子元素 // 如时、分、秒
static from();		// 转换实例化。仅获取有效信息，丢弃冗余信息 // 精确时间，如 LocalDateTime
static parse();		// 解析实例化。跨系统解析文本，兼容性稳定性 // 文本

get();			// 状态值
is();				// 状态

with();			// 计算为副本
plus();			// 加的副本
minus();		// 减的副本

to();				// 转换
at();				// 组合
format();		// 格式化输出字符
```



##### 实例化

```java
// 实例化
XX.now();						// 当前
XX.ofEpochMilli();	// 时间戳/毫秒
XX.from();					// 时间/TemporalAccessor
XX.parse();					// "2011-12-03T10:15:30Z"/...

// 查询
isSupported();		// 是否支持该单位 // Field,Unit
rang();						// 单位范围 // Field
get();						// 单位值 // Field
getLong();				// 单位值 // Field

// 判断
compareTo();
isAfter();
isBefore();
equals();
```



##### 调节

```java
// 调节 // 将指定时间单位设为指定值
with(adjuster);		// 时间调节器
with(field, v);		// 自定义调节器 // 单位，值
truncatedTo();		// 截断精度 // ChronoUnit.SECONDS
```



##### 计算

```java
// 计算
plus(amount); 				// + 时长
plus(l, unit);				// + 自定义时长 // 值，单位
plusXX();							// + XX

minus(amount);				// - 时长
minus(l, unit);				// - 自定义时长 // 值，单位
minusXX();						// - X

until(end, unit);			// 计算时长 // DAYS.between(s, e)
```




#### 机器时间

```java
* Instant		// 瞬时，基于时间戳，同 Date, 表示一个瞬间的毫米级时间点
```

```java
// 实例化
Instant.now();						// 当前
Instant.ofEpochMilli();		// 时间戳/毫秒
Instant.from();						// 转换
Instant.parse();					// "2011-12-03T10:15:30Z"

// 查询
toEpochMilli();		// 时间戳/毫秒
getEpochSecond();	// 秒
getNano();				// 纳秒部分 100 000 000

// 转换
atZone();							// 组合：时区 // ZonedDateTime
atOffset();						// 组合：时差 // OffsetDateTime

// 查询，判断，调节，计算
略，详见方法约定
```



#### 人类时间

```java
* LocalDateTime		// 本地日期时间，不含时区的通用日期时间
* LocalDate				// 本地日期，不含时区的通用日期
* LocalTime				// 本地时间，不含时区的通用时间
* ZonedDateTime		// 时区日期时间，指定时区
* OffsetDateTime  // 时差日期时间，指定时差
```

```java
// 实例化
X.now();				// 当前
X.of();					// 精准时间 // 年月日时分秒
X.ofInstant();	// 瞬时, 时区
X.from();				// 转换
X.parse();			// "2011-12-03T10:15:30"

// 转换
toLocalDate();				// 日期
toLocalTime();				// 时间
atOffset();						// 组合：时差
atZone();							// 组合：时区 // ZonedDateTime

// 查询，判断，调节，计算
略，详见方法约定
```



#### 时长

```java
* Duration		// 时长，基于时间的时间量（时分秒）
* Period			// 周期，基于日期的日期量（年月日）
```

```java
// 实例化
X.of();					// 时长 // 长度，单位
X.from();				// 转换 // TemporalAmoun
X.parse();			// 解析 // "PT24H0M0S"

// 查询
abd();					// 绝对值

// 查询，判断，调节，计算
略，详见方法约定
```



#### ----



#### Clock 

```
时钟，用于国际化
```

```java
Clock.systemUTC // UTC时钟
Clock.offset() // 指定偏移量时钟
```



#### DateTimeFormatter

[格式化占位符文档](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#patterns)

```
时间格式化程序
```

```java
DateTimeFormatter f = DateTimeFormatter.ofPattern("yyyy-MM-dd HH:mm:ss");

LocalDateTime.parse("2021-12-16 14:42:18", f); 	// LocalDateTime
f.format(LocalDateTime.now()); 									// 2021-12-16 14:42:18
```



> ```
> // 解析为本地日期时间
> LocalDateTime.parse("2021-12-16 14:42:18", f);
> 
> // 等同于
> f.parse("2018-05-08 16:03:55").query(LocalDateTime::from);
> ```



#### ----



### 正则

```java
// 声明：正则：/a*b/
Pattern p = Pattern.compile("a*b");
// 匹配字符串
Matcher m = p.matcher("aaaaab");
// 匹配结果
boolean b = m.matches();
```

```
* 原子语法需要双反斜杠，字符串转义，正则转义。如："\\d" 
```



#### Pattern

```
正则模式
```

```java
// 静态属性
CANON_EQ                         // 启用规范等效性。
CASE_INSENSITIVE            (?i) // 忽略大小写。
COMMENTS                    (?x) // 空格，及注释
DOTALL                      (?s) // 点模式
LITERAL                     \Q\E // 文本引用
MULTILINE                   (?m) // 多行模式

UNIX_LINES                  (?d) // Unix 线路模式 // 多行模式下，仅\n视为行分隔  
UNICODE_CASE                (?u) // 忽略 Unicode 大小写 // 能匹配到特殊字符的大小写
UNICODE_CHARACTER_CLASS     (?U) // 启用预定义字符类和 POSIX 字符类的 Unicode 版本。
```

```java
// 实例化
Pattern.compile();		// 正则模式

// 查询
flags();							// 匹配表示
pattern();						// 正则表达式

// 转换
matcher();						// 匹配器
asMatchPredicate();		// 匹配判断器
asPredicate();				// 查找判断器

split();							// 拆分，将正则作为分隔符
splitAsStream();			// 拆分流

// 工具
Pattern.matches();		// 直接匹配
Pattern.quote();			// 文本引用 // \Qxx\E
```

> ```
> // 输入多个匹配表示
> Pattern.compile("xx", Pattern.MULTILINE | Pattern.UNIX_LINES);
> ```
Removes from the underlying collection the last element returned by this iterator (optional operation).



#### Matcher

```
匹配器
```

```java
// 替换
replaceFirst();     // 替换首个
replaceAll();       // 替换所有

// 工具
quoteReplacement();     // 文本引用 // 转义[转义符]，屏蔽反向引用等
```

```java
// 匹配
matches();          // 全量匹配
lookingAt();        // 局部匹配 // 包含即可
find();             // 依次匹配 // 依次查找每个子序列

// 匹配结果
group();            // 匹配内容 // [整个, 捕获组n...]
start();            // 匹配开始位
end();              // 匹配开始位

// 未匹配结果（仅依次查找）
appendReplacement(sb, i);       // sb += 未匹配部分 + i
appendTail(sb);                 // sb += 剩余未匹配部分
```


#### 匹配规则

```js
// 术语
字面量字符			- 字面含义字符
元字符					- 特殊含义字符	（ 如： . ^ $ | \ \* + ? () [] {} ）
转义符					- 元字符的匹配方法 反斜杠 \
```



##### 1.  原子

```js
// 字符类
[abc]               a, b, c      
[^abc]              非(a, b, c)     
[a-zA-Z]            a-z, A-Z          
[a-d[A-Z]]          并集，同上          
[a-z&&[def]]        交集，a-z中，仅def   
[a-z&&[^bc]]        交集，a-z中，排除bc   
[a-z&&[^m-p]]       交集，a-z中，排除m-p  

// 逻辑
ab			连接符：和			ab	
|				选择符：或			a|bb -> a 或 bb

// 模式单元
()			- 组匹配/捕获组（捕获组不支持 g 全局模式）
  	()			- 组匹配		(app)+ -> appapp
  	()			- 捕获组		a(b)(c) -> ['abc','b','c']
(?:)		- 非捕获组		a(?:b)(?:c) -> ['abc']
(?<)		- 独立获组		a(?>\\w+)c -> 无 // 会占有，导致失败
\n			- 正向引用		(a)\1 -> aa
$n			- 反向引用		replace(/【([^]+?)】/,'[$1]')

(?<a>)	- 具名组匹配		(?<a>xx) 读取：res.groups.a
\k<a>		- 具名组引用		/(?<a>xx)\k<a>/ -> xxxx

/*
* 组匹配：视为整体，提升优先级
* 捕获组：暂存内存，额外捕获到匹配组
		- 不支持全局匹配，可用循环exec()捕获
		- 用于捕获，引用
* 非捕获组：取消额外捕获
* 独立捕获：取消额外捕获，且进行占有匹配
* 正向引用：\n 从1开始，依次引用匹配组。
		- 用于匹配重复格式
* 反向引用：$1 从1开始，依次引用匹配组，替换时，可以引用
		- 用于替换双引号等
		
* 具名组匹配：方便读取
		- (?<name>aa) -> baab...
		- 读取：res.groups.name  // 'aa'
*/
```



##### 2. 原子修饰

```js
// 位置修饰
^ 		开始
$			结束
\b		词边界
\B		非词边界
\G		上次结尾，连续匹配

\A		输入开始
\z		输入结束
\Z		最后的终止符

// 断言
x(?=值)		先行断言			x(?=y) -> xy			匹配值：x
x(?!值)		先行否定断言		x(?!y) -> x略		匹配值：x
(?<=值)x		后行断言			(?<=y)x -> yx			匹配值：x
(?<!值)x		后行否定断言		(?<!y)x -> 略x		匹配值：x

// 引用
\Q...\E		引用字符 // 不转义，直接使用
```

```js
// 数量修饰
{n}			n
{n,}		n~
{n,m}		n-m
 
?				0-1		{0,1}
*				0~		{0,}
+				1~		{1,}

// 贪婪匹配 // aaab -> \w*
+				占有匹配：尽量多，且占有		 // \w*+b -> 无		 // \w* 吞字符，导致失败
				贪婪匹配：尽量多 						// \w* -> aaab 		// 默认
?				克制匹配：尽量少						// \w*? -> a

// 标识匹配
(?i)			全局修饰，开启大小写敏感
(?-i)			全局修饰，关闭大小写名
(?i:X)		组内修饰，开启大小写敏感

  i：大小写不敏感（CASE_INSENSITIVE）
  d：Unix 行模式（UNIX_LINES）
  m：多行模式（MULTILINE）
  s：点匹配所有字符模式（DOTALL）
  u：Unicode 字符类模式（UNICODE_CHARACTER_CLASS）
  x：忽略空白模式（COMMENTS）
  U：启用 Unix 行模式（UNIX_LINES）
```

> ```
> * 匹配任意字符：	[^]
> * 阻止贪婪匹配： {}?  ??  *?  +?
> ```



##### 3. 特殊字符

```js
// 预定义模式
.			点字符：一个字符		. -> 任意（除外：回车换行，\r\t）
\d		[0-9]							digit 数字
\w		[A-Za-z0-9_]			word 单词
\s		[ \t\n\f\r\x0B]		space 空格（含垂直制表符）
       
\D    [^\d]   非数字
\W    [^\w]   非单词
\S		[^\s]   非空格
       
\R		任何换行
\X		任何合法字符
       
\v		垂直制表符
\h		水平制表符

// 特殊字符
\\          反斜杠
\t          制表
\n          换行
\r          回车
\f          换页
\cX         ctrl + X // 控制字符

// 中文 // https://www.tamasoft.co.jp/en/general-info/unicode.html
[\u2e80-\u2eff] // [⺀-\u2eff] 部首字 // 128 字
[\u4E00-\u9FA5] // [一-龥] 基本字 // 20902 字
[\u9FA6-\u9FFF] // [龦-鿿] 偏僻字 // 90 字
[\uDB40DC00-\uDB7FDFFF] // 四字节暂无法匹配
```



### 比较器

```java
// 排序方式
	* 自然排序 // java.lang.Comparable
	* 定制排序 // java.util.Comparator
```



#### Comparable 

```java
自然排序 // Object 接口
```

```java
// 重写排序方法
@Ovriride
public int compareTo(Object o) {
  if (o instanceof Person){
    Person b = (Persion) o;
    return this.xx - b.xx;
  }
  return 0;
}
```



#### Comparator

```java
定制排序 // .stream().sorted() 参数
```

```java
// 实例化
X.comparing(Function k); 								// 取键器，并排序
X.comparing(Function k, Comparator c);	// 取键器，并定制排序
X.comparingXX(Function k); 							// xx取键器，并排序

X.naturalOrder();						// 比较器，自然排序
X.reverseOrder();						// 比较器，自然倒序
X.nullsFirst(Compartor c);	// 比较器，空值优先
X.nullsLast(Compartor c);		// 比较器，空值置后

// 再次排序
reversed();				// 反转
thenComparing(Function k);  // 相等后比较
thenComparing(Function k, Comparator c);
thenComparingXX(Function k);

// 比较
compare(a, b);		// 比较顺序
```



### 数学

#### BigInteger

```java
java.math.BigInteger  // 大整形计算
```

* 使用

```java
BigInteger a = new BigInteger("123");
BigInteger b = new BigInteger("123");
a.add(b);				// +
a.subtract(b);	// -
a.multiply(b);	// *
a.divide(b);		// /
a.remainder(b);	// %
```



> ```
> RoundingMode 枚举类 // 取整模式
> CEILING			// 无穷大
> DOWN				// 零
> FLOOR				// 无穷小
> HALF_DOWN		// 
> HALF_EVEN		// 
> HALF_UP			// 四舍五入
> UNNECESSARY	// 
> UP					// 远离零
> ```



#### BigDecimal

```java
java.math.BigDecimal  // 大精度计算
```

* 使用

```java
// 初始化
BigDecimal a = new BigDecimal("0.123");
BigDecimal b = new BigDecimal("0.123");

// 四则运算
a.add(b);							// +
a.subtract(b);						// -
a.multiply(b);						// *
a.divide(b,2,RoundingMode.UP);		// / // 位数，取值

a.remainder(b);						// %

// 近似取值
a.setScale(2,RoundingMode.UP);		// 向上取2位
```



#### Math

```
java.lang.Math
```

* 静态方法

```java
random();			// 随机数 0 ~ 0.999
abs();				// 绝对值
floor();			// 向下取整
ceil();				// 向上取整
round();			// 四舍五入
max();				// 最大
min();				// 最小

pow();				// 幂运算
sqrt();				// 平方根
```



#### Random

```java
java.util.Random		// 随机数 （种子发生器）
```

* 普通方法

```java
// 随机种子
new Random(System.nanoTime())
    
// 获取一个随机数
boolean nextBoolean();
void nextBytes(byte[] bytes);
double nextDouble();
float nextFloat();
double nextGaussian();
int nextInt();
int nextInt(int n);			// 0 ~ （n-1）
long nextLong();
```



### ----




# 集合框架

```
将多个元素组成一个单元，用于存储，检索，操作，聚合
```

```java
// 集合
- Iterable 		// 迭代
			- Collection	// 集合
          - Set				// 散列
              - SortedSet			// 升序散列
          		* HashSet				// 散列
          		* TreeSet				// 树
          		* LinkedHashSet	// 链式散列
  
          - List			// 序列
  						* ArrayList		// 动态数组
  						* LinkedList	// 双向链表
  
          - Queue			// 队列
              - Deque				// 双向队列
              	* ArrayDeque		// 双向队列
  						* LinkedList	// 双向链表

// 映射组
- Map
		- SortedMap			// 升序哈希表
  	* HashMap				// 哈希表
		* TreeMap				// 有序哈希表
		* LinkedHashMap	// 链式哈希表
```

```java
// 并发集合
- Set
  	* CopyOnWriteArraySet		// 副本散列，写时复制
- List
  	* CopyOnWriteArrayList	// 副本序列，写时复制
- Map
  	* ConcurrentHashMap			// 并发图，锁分段技术
```



### Iterable

```
遍历
```

```java
// 遍历
forEach();			// 迭代

// 转换
iterator();			// 迭代器 // Iterator
spliterator();	// 并行迭代器 // Spliterator
```



> * Iterator
> 
> ```
> 迭代器
> ```
> 
> ```
> // 手动迭代
> hasNext();		// 是否有下一个元素
> next();				// 查询元素
> remove();			// 删除元素
> 
> // 自动迭代
> forEachRemaining(i -> i);		// 迭代
> ```
> 
> ```
> // 使用
> Iterator i = collection.iterator();
> while(i.hasNext()) { // 下一个
>  	i.next(); // 读取
>  	i.remove(); // 删除 // 迭代期间，禁止操作集合 // 仅允许 remove();
> }
> 
> // fail-fast 快速失败机制
> 1. 每次操作集合计数 modCount
> 2. 迭代开始时，保存该值
> 3. 迭代中，一旦该值改变，立即抛出异常
> ```
>
>
>
>
> * Spliterator
> 
> ```
> 并行迭代器
> ```
> 
> ```
> tryAdvance();						// 是否有剩余元素
> estimateSize();					// 剩余元素数量
> characteristics();			// 元素类型
> trySplit();							// 尝试拆分 // 返回前半部分，保留后半部分
> forEachRemaining();			// 迭代
> 
> ...
> ```



### Collection

```
集合，一组对象
```

```java
// 查询
size();					// 数量
isEmpty();			// 为空
contains();			// 含有
containsAll();	// 含有所有

// 操作
add();					// 添加
addAll();				// 添加集合

remove();				// 删除
removeAll();		// 删除集合
removeIf();			// 条件删除
retainAll();		// 交集，保留指定

clear();				// 清空

// 转换
strem();						// 流
parallelStream();		// 并行流

toArray(new Integer[0]);	// 转数组
```



### ----



### List

```
序列，有序集合
```

```java
// 查询
indexOf();			// 由元素，查索引
lastIndexOf();	// 由元素，查索引，从尾查找

get();					// 按索引，元素

// 操作
add();			// 按索引，添加
addAll();		// 按索引，添加集合
set();			// 按索引，替换
remove();		// 按索引，删除

sort();			// 排序
subList();	// 截取
  
// 转换
listIterator();		// 有序迭代器

// 工具
List.copyof();		// 集合转序列
List.of();				// 元素转序列
```




> * ListIterator
>
> ```
> 有序迭代器
> ```
>
> 
> ```
> // 手动迭代
> hasPrevious();		// 是否有上一个元素
> previous();				// 上一个
> 
> nextIndex();			// 下一个索引
> previousIndex();	// 上一个索引
> 
> add();						// 添加元素
> set();						// 替换元素
> ```




### Set

```
散列，不重复集合
```

```java
// 方法
同集合
  
// 工具
List.copyof();		// 集合转序列
Set.of();					// 元素转散列
```



#### SortedSet

```
有序的不重复集合，有序键集合
```






### Queue

```
队列，集合的修改接口
```

```java
// 查询
element();		// 查询
peek();				// 尝试查询

// 操作
add();				// 插入
offer();			// 尝试插入
remover();		// 删除
poll();				// 尝试插入
```

```
* 当元素不存在时报错，尝试时不会报错
```



#### Deque

```
双端队列，集合的修改接口（两端）
```



### ----



### Map

```
映射组，键值对映射的对象
```



#### SortedMap

```
有序的映射组，有序的键值对映射对象
```



### ----



### Collections 

```
集合工具类
```



### Arrays

```
数组工具类
```





### ----



# 泛型



# 反射机制



# ----



# 异常处理

```java
运行时错误。
```

```java
// 抛出机制
1. 在错误行，创建异常对象
2. 向上依次抛出，直到调用方法
3. 调用方法抛出到JVM，虚拟机终止运行
```



### 体系

```java
Throwable 		// 出错
	* Error					// 错误 // 无法处理
  		* VirtualMachineError				// 虚拟机错误
    		* ...
	* Exception			// 异常 // 尽量避免，处理
    		* 受捡异常			// 编译时异常
			* 非受检异常			// 运行时异常
```

![异常分类](db\img\异常分类.png)



### 分类

* 受捡（checked）异常

```
异常必须处理，否则报编译错误
```

```java
IOException											// 输出输入异常
	* EOFException
	* FileNotFoundException
	* MalformedURLException
	* UnknownHostException
  * ...
	ClassNotFoundException					// 类加载失败
	CloneNotSupportedException			// 克隆方法未实现
```

> ```
> * 编译时异常进行处理时，可以编译。运行时抛出
> ```



* 非受检（unchecked）异常

```
异常不强制处理，但是会终止进程
```

```java
RuntimeException
	* ArithmeitcException						// 数学异常
	* ClassCastException						// 强转失败
	* IllegalArgumentException			// 非法参数
	* IllegalStateException					// 非法状态？
	* IndexOutOfBoundsException			// 数组越界
	* NoSuchElementException				// 请求元素不存在，枚举？
	* NullPointerException					// 空指针
  * ...
```



### 自定义异常

```java
// 自定义受检异常 // 编译器编译时报错
public class DividerException extends Exception {
  public DividerException(String info) {
    super(info); // 错误信息
  }
}
```

```java
// 使用
public class Test {
  public static void main(String[] args) {
    try{ // 监视
      method();
    }catch (DividerExceptions e){ // 捕获
      e.printStackTrace(); // 打印堆栈异常信息
    }
    
  }
  
  public void method()throws { // 向调用点，抛出异常
    // 抛出异常
    throw new DividerException("[异常] 这是一个异常");
  }
}
```

> ```
> * 自定义受检异常：适用于编译时报错
> * 自定义非受检异常：适用于运行时报错
> 根据场景选择继承 Exception || RuntimeException
> ```



### 捕获

```
try,catch,finally,throw,throws
```



try  catch

```java
try{ // 监控异常，通知 catch // 不能独立存在
	
} catch(Exception ex) { // 捕获异常

}
```

> ```
> // 多重catch
> try{
> 
> }catch (ArithmeitcException ex) {
> 
> }catch (NullPointerException ex) {
> 
> }
> ```



try  finally

```java
try{ // 监控异常，通知 finally // 不能独立存在
	
} finally { // 必定执行，释放资源 // 继续向外传递异常

}
```

```
* finally: 不会捕获异常，仍然需要catch捕获
```



try  catch  finally

```java
try{ // 监控异常，通知 finally // 不能独立存在
	
} catch(Exception ex) { // 捕获异常

} finally { // 必定执行（无视return）

}
```



### 抛出

throw

```
抛出，手动创建异常对象
```

```java
throw new RuntimeException("手动抛出错误");
```



throws

```
声明此方法不处理该异常。
调用此方法必须处理该异常。
```

```java
// throws 继续向上抛出异常，调用点需要处理。
// Exception 声明的异常，本方法不处理（多个异常使用[,]隔开）
public void method()throws Exception {

}
```



# 多线程

* 使用场景

```
用于同时执行不同的事件。 
```

* 并行与并发

```
* 并行：同个时间，多个进程同时进行
* 并发：多个进程在同一个时间段发生
```

* 线程与进程

```
* 线程：进程的一个执行单元，程序执行的最小单位
* 进程：内存中的一个应用程序，有独立的内存空间
* 程序：一组指令的集合，可以完成指定任务/功能
* 软件：一个多个应用程序及资源组成的软件系统
```

> ```
> 线程：最小单位，可以同时运行多个独立功能
> 进程：一个程序最少需要一个进程，如虚拟机
> ```

* 线程调度

```
* 分时调度
		轮流使用CPU,平均分配时间。
		
* 抢占式调用
		按优先级分配使用，同级抢占使用
```



### 开启线程

```java
方式：
1. 自定义线程类 继承 Thread		// 子线程
2. 自定义程序类 实现 Runnable	// 子程序
```

```java
// 简写
new Thread(() -> {
	System.out.println("启动线程~~~");
}).start();
```



#### 继承 Thread

```
继承Thread，并重写 run() 方法，创建线程，并启动
```

```java
// 自定义线程类继承 Thread
public class MyThread extends Thread {
   // 开启子线程，运行的代码写入run方法
	@Override
  public void run(){ // 子线程代码
		System.out.println("子线程代码")
  }
}
```

```java
// 一个线程对象只能开启一个子线程，运行一次start
MyThread thread = new MyThread();
thread.stat();
```



> * 简写
>
> ```
> new Thread() {
>     @Override
>     public void run() {
>         System.out.println("子线程代码");
>     }
> }.start();
> ```



#### 实现 Runnable

```
创建 Runnable 对象，传入并创建线程对象，并启动。
```

```java
// 自定义线程类实现 Runnable
public class MyRun implements Runnable {
   // 开启子线程，运行的代码写入run方法
	@Override
  public void run(){ // 子线程代码
		System.out.println("子线程代码")
  }
}
```

```java
// 一个线程对象只能开启一个子线程，运行一次start
Thread thread = new Thread(new MyRun);
thread.stat(); // 开启子线程，调用 run 方法
```



> * 简写
>
> ```
> new Thread(() -> 
> 	System.out.println("子线程代码")).start();
> ```



#### 实现 Callable

```
创建 Callable 调用对象，传入并创建任务对象。
创建 FutureTask 任务对象，传入并创建线程，并启动。
调用 task.get() 获取子线程的结果
```

```java
// 自定义线程实现 Callable
public class MyCallable implements Callable<String> {
	@Override
  public String call() throws Exception {
    System.out.println("子线程代码");
    return "结果";
  }
}
```

```java
// 一个线程对象只能开启一个子线程，运行一次start
FutureTask<String> task = new FutureTask<>(new MyCallable());
new Thread(task).start();

// 阻塞当前进程，等待task线程的结果，恢复当前线程
String res = task.get();
```



> * 简写
>
> ```
> // 声明任务
> FutureTask<String> task = new FutureTask<>(() -> {
>     System.out.println("子线程代码");
>     return "结果";
> });
> 
> // 启动任务
> new Thread(task).start();
> 
> // 获取结果
> try {
>     String s = task.get();
> } catch (ExecutionException e) {
>     throw new RuntimeException(e);
> }
> ```



#### 线程池 Executors

```
// 优势
提高响应速度 // 提前创建线程
降低资源消耗 // 复用线程
便于线程管理 // 核心大小，最大线程数，空闲存活时间
```

```java
// 初始化线程，并指定线程数量
ExecutorService executor = Executors.newFixedThreadPool(10);

// 实现：Runnable 接口 // 无返回值
executor.execute(() -> System.out.println(111));
// 实现：Callable 接口 // 有返回值 // get() 获取
executor.submit(() -> 111);

// 关闭连接池
executor.shutdown();
```



### Thread类

* 构造方法

```java
public Thread();// 分配一个线程
public Thread(String name);// 分配，并命名
public Thread(Runnable target);// 自定子程序
public Thread(Runnable target, String name);// 自定子程序，并命名
```

* 类方法

```java
Thread.currentThread();			// 当前线程
Thread.sleep(long ms);			// 休眠毫秒
Thread.yield();							// 放掉一次，重新抢
```

* 普通方法

```java
getName();							// 获取线程名
setName(String name);		// 设置线程名
isAlive();							// 是否存活（未结束）
getPriority();					// 获取优先级
setPriority(int i);			// 设置优先级

start();								// 激活,只能一次
join();									// 连接（需要在运行中线程调用，接管控制权）
join(long ms);					// 连接（限时）
join(long ms, int ns); 	// 连接（限时）

stop();									// 强迫程序停止。不安全，已弃用
suspend()/resume();			// 暂停/恢复。容易死锁，已弃用
```

> * 优先级
>
> ```
> Thread.MAX_PRIORITY		// 最高 10
> Thread.MIN_PRIORITY		// 最低 1
> Thread.NORM_PRIORITY	// 标准 5 // 默认
> ```
>
> * join();
>
> ```
> 连接已开始的线程 t.join(), 当前线程阻塞，
> 等待连接线程执行完毕，当前线程恢复运行。
> 
> 作用：一般用于等待已执行的较慢线程，如联网获取外部数据
> ```
>
> * 守护线程
>
> ```
> 随线程启动，随线程结束。
> 如：垃圾回收线程
> ```



### 线程安全

```
多个线程访问同一资源，进行读写操作，读取的结果被篡改
```

```
 解决线程安全方式:
 1. 同步代码块
 2. 同步方法
 3. 锁机制
```

> ```
> * 使用 volatile 保证变量的对主内存的可见性
> * 使用 synchronized 保证线程操作的原子性
> ```



#### 同步代码块

```java
// 此代码期间，其他线程无法执行
// () 唯一锁对象，只有拿到锁对象才能进入执行
synchronized(this) {
	System.out.pirntln("同步代码块，强占CPU控制权");
}
```

> ```
> 用于强占CPU
> 锁结束前，其他线程无权抢夺
> ```



```java
// 锁对象：
synchronized(this){}			// this
synchronized(类.class){}		// 当前类的class对象
```

> ```
> synchronized(lock){}			// new Object
> synchronized("lock"){}		// 字符串
> ```



#### 同步方法

```java
// 此代码期间，其他线程无法执行
// 锁对象：this/类.class
public synchronized void fn() {
	System.out.pirntln("同步代码块，强占CPU控制权");
}
```



### 线程通信

```java
// 由 synchronized 中的同步监视器调用 // 同一个锁内的通讯
wait();					// 等待
notify();				// 随机唤醒一个
notifyAll();		// 唤醒所有
```

> ```
> [1] 等待：
> 	* 进入阻塞状态，并释放同步监视器锁，直到被其他线程唤醒
> 	* 等待期间，进行的判断可能被更改，需要重新判断
> ```



### 生命周期

* 五状态说法 JDK 1.5

```java
New					// 新建
Runnable		// 就绪，等待cpu调度
Running			// 运行
Blocked			// 阻塞
Dead				// 死亡
```

* 六状态说法 JDK 1.5+

```java
Thread.State.NEW              // 新建
Thread.State.RUNNABLE         // 就绪/运行
Thread.State.BLOCKED          // 锁阻塞，等待获取锁
Thread.State.WAITING          // 计时等待
Thread.State.TIMED_WAITING    // 无限等待
Thread.State.TERMINATED       // 死亡
```



### 单例模式

```java
// 单例模式的线程安全问题
public static class LazyOne {
    private LazyOne() {}
  
    // 1. volatile 保证原子性
    private static volatile LazyOne singleton;
  
    public static LazyOne getInstance() {
      
        // 2. 轻量判断，快速读取
        if (singleton != null) {
            return singleton;
        }
      
        // 3. 加锁再次判断，保证一致性
        synchronized (LazyOne.class) {
            if (singleton != null) {
                return singleton;
            }
            return singleton = new LazyOne();
        }
      
    }
}
```



### 死锁

```
不同的线程分别锁住对方需要的同步监视器对象不释放，
都在等待对方先放弃时就形成了线程的死锁
```



# 数据结构

* 逻辑关系

```
集合结构：同属一个集合，无逻辑关系
线性结构：一对一，存在唯一的首尾元素
树形结构：一对多
图形结构：多对多
```



* 存储结构

```
线性结构：一组连续的存储单元
	* 优点：结构单一仅需保持数据本身，下标访问，随机访问
	* 缺点：静态分配连续空间，空间利用低，插入删除耗时多
	
链式结构：一组不连续的节点，节点存数据及之下个地址
	* 优点：不连续存储空间利用高，动态长度，插入删除快速
	* 缺点：需要额外空间存储指针，不支持下标，不支持随机访问
	
索引结构：

散列结构：
```



# File类与IO流

#### I/O 数据流

```
用于设备之间的数据传输
```

```java
// 特点
* 处理设备的数据传输
* 数据的操作方式
* 含有操作流的对象
```

```java
// 流的分类
流向：输入inpu，输出output		// 读取，写入
数据：字节流 ，字符流					 // 超文本，文本
角色：节点流，处理流					 // 基础读写类，封装读写类
```

```
* 需要 try catch 处理异常
```

* 路径

```
绝对路径： "D:\\file\\test.txt"

相对路径：
	main			- 当前工程
	method		- 当前模块
```



###### File类

```java
java.io.File				// 文件/目录
```

```java
// 构造器
File(String path); // 文件
File(String parent, String child) // 目录,名称
File(File parent, String child) // 目录对象,名称
```

```java
// 读取
exists();				// 存在  // 一可Zs 特s
getName();			// 文件名
length();				// 字节  // long
lastModified();	// 最后修改时间

getPath();					// 路径 （创建时路径）
getAbsolutePaht();	// 绝对路径
getAbsoluteFile();	// 绝对路径 File

getParent();				// 目录
getParentFile();		// 目录 File
```

```java
// 操作
createNewFile();	// 创建文件
renameTo();				// 重命名	// 参 File 返 boolean  
delete();					// 删除
deleteOnExit();		// 存在则删除

mkdir();					// 创建目录 （只能创建一级目录）
mkdirs();					// 创建多级目录

list();						// 文件名 // String[]
listFiles();			// File // File[]
```

```java
// 判断
isFile();					// 文件
isDirectory();		// 目录

isHidden();				// 隐藏
canRead();				// 只读
canWrite();				// 只写
```

> ```
> * 创建目录/文件，返回 结果（boolean）
> ```





> * 递归多级目录
>
> ```
> 
> ```





###### 抽象基类

* IO流体系

<img src="H:/20211121--java/1221-io/imgs/IO流体系.png" alt="IO流体系" style="zoom:80%;" />

```java
// 抽象基类
字节流：InputStream, OutputSteam // 操作二进制，适用于复制文件
字符流：Reader, Writer // 操作字符

// 节点流 // 文件流
字节型： FileInputStream, FileOutputStream,
字符型： FileReader, FileWriter

// 处理流
缓存流：BufferedInputStream, BufferedOutputStream, BufferedReader, BufferedWriter
转换流：InputStreamReader, OutputStreamWriter
对象流：ObjectIInputStream, ObjectOutputStream
```



* 常用方法

```java
// InputStream 输入流 读取字节
read();
read(byte[] b); 
read(byte[] b, int off, int len);

// OutputStrearm 输出流 写入字节
write();
write(byte[] b); 
write(byte[] b, int off, int len);

// Reader 阅读流 读取字符
read(); // char[] 如上

// Writer 书写流 书写字符
write(); // char[] 如上
write(String s);
```



###### 字节流

```
* 读写非文本文件，如 jpg,mp3,mp4
```



FileInputStream 输入流

```java
File file = new File("a.mp3");  // 文件
FileInputStream fis = new FileInputStream(file);  // 输入流

// 读取
byte[] data = new byte[0]; // 容器
for(byte[] container = new byte[1024 * 8];;) {
  int len = fis.read(container); // 读取一段
  if(len == -1) break; // 读完
  byte[] newData = new byte[data.length + len]; // 新容器
  System.arraycopy(data,0,newData,0, data.length); // 扩容
  System.arraycopy(container,0, newData, data.length, len); // 追加数据
  data = newData; // 容器更新
}

// 输出
String txt = new String(data);
System.out.println("[读取结果]\t" + txt);

// 释放
fis.close();
```

> ```
> fis.read(); // 无参读取，返回单个字节
> ```



FileOutputStream 输出流

```java
File file = new File("a.mp3");		// 文件
if(!file.exists)file.createNewFile();  // 创建文件
FileOutputStream fos = new FileOutputStream(file,true);  // 输出流 追加模式
String data = "这是写入文字"; // 数据

// 写入输出流
byte[] dataTemp = data.getBytes();
int i = 0; // 写入段数
int SIZE = 1024 * 8; // 每次写入大小
while ((i + 1) * SIZE <= dataTemp.length) {
  fos.write(dataTemp, i * SIZE, SIZE); // 写入每段
  i++;
}
fos.write(dataTemp, i * SIZE, dataTemp.length % SIZE); // 写入余数

// 释放
fos.close()
```



文件复制

```java
File srcFile = new File("a.mp3"); // 源文件
File copyFile = new File("a（副本）.mp3"); // 副本
if(!copyFile.exists) copyFile.createNewFile(); // 创建副本

FileInputStream fis = new FileInputStream(srcFile); // 输入流
FileOutputStream fos = new FileOutputStream(copyFile); // 输出流

// 循环复制
for(byte[] container = new byte[1024 * 8];;) { // 分段
  int len = fis.read(container);// 读取
  if(len == -1) break; // 读完
  fos.write(container,0,len); // 写入
}

fis.close();
fos.close();
```



###### 字符流

```
* 读写文本文件，如 txt,java,c,
```

FileReader 输入流

```java
File file = new File("a.txt");
FileReader fr = new FileReader(file); // 输入流

for(char[] container = new char[1024 * 8];;){ // 容器
  int len = fr.read(container); // 读取
  if(len == -1) break; // 读完
  System.out.print( new String(container,0,len) ); // 打印
}

fr.close(); // 关闭
```

> ```
> fr.read(); // 无参读取，返回单个字符
> ```



FileWriter 输出流

```java
File file = new File("a.txt");
FileWriter fw = new FileWriter(file, true); // 输出流 追加

String s = "这是需要写入的文字";
fw.write(s); // 写入文字
```

> ```
> * write(); // 没有文件则进行创建
> ```



###### 缓冲流

```
* 提高流的读写速度
* 原理：内部提供一个缓冲区，可以一次性读取大量数据。
```

```java
// 输出完毕需要释放缓冲区
bos.flush(); // 刷新缓存区
bw.flush(); // 刷新缓存区
```



字节型

```
BufferedInputStream			- 输入流
BufferedOutputStream		- 输出流
```

* 复制文件

```java
File srcFile = new File("a.mp3"); // 源文件
File copyFile = new File("a（副本）.mp3"); // 副本
if(!copyFile.exists) copyFile.createNewFile(); // 创建副本

BufferedInputStream bis = // 缓冲输入流
  new BufferedInputStream(new FileInputStream(srcFile));
BufferedOutputStream bos =  // 缓冲输出流
  new BufferedOutputStream(new FileOutputStream(copyFile));

// 循环复制
while(true) {
  byte[] contain = new byte[1024 * 8]; // 分段
  int len = bis.read(contain); // 读取
  if(len == -1) break; // 读完
  bos.write(contain,0,len); // 写入
}
bos.flush(); // 刷新缓存区

// 关闭
bis.close();
bos.close();
```



字符型

```
BufferedReader		- 输入流
BufferedWriter		- 输出流
```

* 复制文件

```java
BufferedReader br = // 缓冲输入流
  new BufferedReader(new FileReader("a.txt"));
BufferedWriter bw =  // 缓冲输出流
  new BufferedWriter(new FileWriter("a(副本).txt"));

// 方式一 
while(true) {
  char[] contain = new char[1024 * 8];// 分段
  int len = br.read(contain);// 读取
  if(len == -1) break; // 读完
  bw.write(contain,0,len); // 写入
}
bw.flush(); // 刷新缓存区

// 方式二
while(true) {
  String data = br.readLine(); // 读取
  if(data == null)break; // 读完
  bw.write(data); // 写入一行
  bw.newLine(); // 换行
}
bw.flush(); // 刷新缓存区

// 关闭
br.close();
bw.close();
```

```

```







###### 转换流

```
// 属于字符流
InputStreamReander		- 字节输入 -> 字符输入 // 解码读取
OutputStreamWriter		- 字符输出 -> 字节输出 // 编码写入
```

```
作用：提供字节流，字符流之间的转换
解码： byte -> 字符
编码： 字符 -> byte
```



解码

```java
FileInputStream fis = new FileInputStream("test.test");
InputStreamReader isr = // 实例化 // 编码类型
  new InputeStreamReader(fis,"UTF-8");

while(true) {
  char[] container = new char[1024 * 8]; // 容器
  int len = isr.read(container); // 读取
  System.out.print(new String(container,0,len)); // 打印
}

isr.close(); // 关闭
```



编码

```java
FileOutputStream fos = new FileOutputStream("test.txt");
OutputStreamWriter osw = // 实例化 // 编码类型
  new OutputStreamWriter(fos,"gbk");

String s = "这是写入内容";
osw.write(s); // 写入

osw.close(); // 关闭
```



字符集

```
ASCII				- 美国标准信息交换码，一字节7位
UTF-8				- 可变长编码方式，1-4字节
GBK					- 中文编码表升级，最多2个字节

ISO8859-1		- 拉丁码表，欧洲码表，一字节8位
GB2312			- 中文编码表，最多2个字节
Unicode			- 国际标准码，所有字节2个字节
```



###### ----



###### 数据流

```
作用：用于读写基本类型的变量，字符串
```

```
DataInputStream				- 输入流  读取
DataOutputStream			- 输出流  写入
```



###### 对象流

```
作用：用于读写基本类型或对象的变量，字符串
```

```
ObjectOutputStream		- 序列化
ObjectInputStream			- 反序列化
* 只能读写单个对象？
```

* Serializable

```
* 实现可序列接口 // jvm虚拟机自动实现 // 标签型接口(自动实现)
```

* 序列化

```java
ObjectOutputStream oos = // 实例化 // 输出流
	new ObjectOutputStream(new FileOutputStream("a.txt"));
Person p = new Person("张三",23,"男");

oos.writeObject(p); // 写入对象
oos.flush();
oos.close();
```

* 反序列化

```java
ObjectInputStream ois = // 实例化 // 输入流
	new ObjectInputStream(new FileInputStream("a.txt"));

Person p = (Person)ois.readObject();
oos.writeObject(p); // 写入对象
oos.close();
```



###### 打印流

```
方便的打印功能
```

```
PrintStream			- 字节输出
PrintWriter			- 字符输出
```



###### 序列化

```
实现接口 Serializable 
```

```
将java对象转为二进制流
可以进行保存，传输
```

```
// 使用对象流的方法
ObjectOutputStream		- 序列化
ObjectInputStream			- 反序列化
```



###### 系统类

* 标准输入，输出流

```
System.in				- 标准输出流
System.out			- 标准输出流
```

```
默认设备
  输入	- 键盘
  输出	- 显示器
```

> ```
> NIO.2 用于直接操作缓冲流
> ```



# 网络编程



# JDK8-17新特性

# ----



# 

# 

# 










```

```