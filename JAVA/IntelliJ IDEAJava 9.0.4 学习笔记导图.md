# 	IntelliJ IDEAJava 9.0.4 学习笔记导图

笔记以 idea 中创建项目的形式书写，该文档类似一个目录。

JVM + 核心类库 = JRE

JRE + java开发工具（javac.exe/jar.exe) = JDK

# 该文件包含 Java 最基础的语法

## 文件名： JavaBasicGrammar

#### 循环： 

while	do while	for	for嵌套	for each增强循环	switch	

#### 判断：

if else

#### String类：

String类简单字符串

.length()	方法介绍

String在数组中的应用：char 数组转换 String 字符串	创建 String 类型的数组（一维和多维）

import java.util.Arrays;   Arrays类（导包）中的方法，输出多维数组和一维数组。

#### Scanner的介绍：

import java.util.Scanner

Java 方法 Math.max()介绍

#### 三元运算符 ：

条件运算符也被称为三元运算符。该运算符有3个操作数，并且需要判断布尔表达式的值。该运算符的主要是决定哪个值应该赋值给变量。

```java
variable x = (expression) ? value if true : value if false
```

#### 方法

方法只能在方法中调用不能呢个在类里调用

**重载 ：方法名相同，方法参数的类型和个数不同。**

#### 传参注意事项：

方法传递数组

引用类型参数的传递，调用方的变量，和接收方的参数变量，指向的是同一个对象。双方任意一方对这个对象的修改，都会影响对方（因为指向同一个对象嘛）,解决该问题可以使用深拷贝，内容不变地址改变。



------

# 该文件包含 Java oop 面向对象

面向过程POP：

- 把要解决的问题梳理出来，**线性顺序**的去解决问题，适用于解决单个对象问题（因为每个人都有自己独特的问题）。
- 集体服务于个人。
- 普遍人认为集体是为个人而存在的，而且集体的福利和力量的发挥是为了个人的利益的。

面向对象OOP：

- 把要解决的问题全部汇总，**解决共性问题**，特性问题单独解决，适用于解决多个对象的问题。
- 个人服务于集体。
- 毛认为个人存在于集体之中，并为集体而存在，而 且个人是在集体中才能获得幸福和才华的发挥。



OOP三大特性：封装 encapsulation	继承 inheritance	多态



## 文件名：dogManagerOOPOne

通过记录狗状态来介绍面向对象

类 class 构造对象的模板和蓝图。

对象 object(根据所需属性，引用的类, 的抽象说法)

属性(类当中的变量和方法的总称)：属性是类的重要组成部分

成员变量（属性中的变量）	行为 behavior(属性中的方法)	

实例 instance（根据所需属性，  引用的类， 的现实体现）	

你可以说一个实例是一个对象，但你不能说一个对象是一个实例。因为定义对象时只是把自身的规则和逻辑定义好，实例可以通过输入不同的数据使得自己和其他实例不同。

创建实例	调用属性

空指针介绍



## 文件名：dogManagerOOPTwo

public	private

#### OOP的封装

封装的思想

to String()	方法

## 文件名：dogManagerOOPThree

构造方法：写构造方法不需要返回值，不是空返回值因此是没有类型的，通常情况下需要一个无参数的构造，来满足初始化时不填参数。

构造方法的使用：初始化

使用构造方法后封装失效的问题

垃圾回收的问题

## 文件名：aboutStaticOOPUpFour

static（静态的修饰词）介绍：静态属性基于类。

静态变量

静态方法 ：类层面的方法，可由类之接调用。

静态代码块：和类一起完成初始化，只加载一次。

单例设计模式 ：再外部只能调用该类内部事先创建好的对象，不能在外部创建新的该类对象。

## 文件名：animalManagerOOPDownOne	

#### 继承 extends:

构造方法不能直接被子类继承，如果强行继承可用super。

多层继承

覆写/重写：

- 继承父类的方法，虽然方法名没变，但是子类需要根据子类的实际需求作出革新。

- Override和Overload不同的是，如果方法签名不同，就是Overload，Overload方法是一个新方法；如果方法签名相同，并且返回值也相同，就是Override。

   注意：方法名相同，方法参数相同，但方法返回值不同，也是不同的方法。在Java程序中，出现这种情况，编译器会报错。

super：在子类中虽然重写了但还要用父类的属性，这时用 super 来修饰该属性。

final：可修饰：类、方法、常量。类不可继承，方法可继承但不能重写，常量可继承但不能修改。

## 文件名：animalManagerOOPDownTwo

Abstract 修饰抽象

抽象类：无法实例对象（没法new 对象）

抽象方法：没有方法体，被继承后必须重写

## 文件名：humanOOPDownThree

### 接口：

- 一个类可实现多个接口，接口中的属性：行为都是抽象方法，公共的静态常量。接口之间可继承。

- 接口是对动作的抽象，而抽象类是对根源(具体的事物)的抽象。

### 匿名内部类：

- 本质是一个继承或实现，类或接口，的子类的一个实例对象，只不过这个对象是匿名的。
- 场景：常用于该方法只会被调用当下这一次

## 文件名：huaMuLanOOPDownFour

### 多态：

同一个行为具有多个不同表现形式或形态的能力。

#### 多态存在的三个必要条件：

* 继承
* 重写
* 创建对象时父类 new 子类`(有逼格的说法是：父类引用指向子类对象)`没有向上转型的子类对象无法实现向下转型



- 向上转型：子类引用的对象转换为父类类型称为向上转型。通俗地说就是是将子类对象转为父类对象。此处父类对象可以是接口。转型后，只能使用父类的属性（子类自己的特性用不了），如果父类是接口使用的还是子类的属性(接口中的行为没方法体)。父类 名=new子类对象
- 向下转型：是建立再向上转型的基础上，父类引用的对象，转换为子类类型称为向下转型。（需要强转）子类 名 =（强转子类）向上转型的对象名 



## 外加

### 类之间的关系

- 依赖 dependence ("use - a")即：一个类的放方法操作或使用，需要另一个类的对象。
- 聚合 aggregation ("has - a")即：一个类的对象包含另一个类的对象。
- 继承  inheritance ("is - a")即：一个类不但包含另一个类的方法在这基础上还有其新的特色属性。



### 访问器方法  accessor method

- 只访问对象但不修改对象的方法
- 例如：`LocaDate.getYear(); `



### 主力类 workhouse class 

- 通常这些类没有`main`方法，但是有自己的属性。



### 关键字 this

当主力类中的行为，用于操作实例并且还要对这个实例字段进行修改存取操作时，为了更清晰的分清是使用主力类的字段还是实例的字段，会在需要区分的字段前写上`this.`，以表示调用我们真正需要用的字段的实例。

关于`this`介绍延伸出两种参数：

- 隐式参数 implicit parameter ：`this`所代表的参数（也可以说我们需要的目标参数）
- 显示参数 expilcit paramenter ：直接使用，没有特指是那个 实际的参数



------

# 该文件包含 Java API 和进阶功能（不包含新特性）

### Object 是所有类的父类

#### Objects 类 继承于 Oboject

此类提供很多静态方法用于在对象上操作的实用方法或在操作之前检查某些条件。  这些实用程序包括用于计算对象的哈希码，返回对象的字符串，比较两个对象以及检查索引或子范围值是否超出范围的`null`或`null`  - `null`方法。

```java
Objects.requireNonNull(T obj)  // 关于判断对象是否为null, 如果为 null 直接报异常NullPointerException
Objects.requireNonNull(T obj, String exceptionMessage) // 同上，但如果为 null 可自定义异常信息
    
Objects.requireNonNullElse(T obj, T defaultObj) // 判断对象是否为 null ，如果为 null 返回第二个参数   
    
    
```



------



## 文件名：javaApiOne

### scanner类：

一个简单的文本扫描器，可以使用正则表达式解析原始类型和字符串。 

------



### number：是抽象类（abstract），所有包装类的父类。

包装类优势：面向对象的方式把基础类型包装成对象，再调用相应类中的计算方法去完成计算。省去了我们调用基础内置数据类型自己写计算函数。

内置数据类型：byte、int、long、double 等。

包装类：Integer、Long、Byte、Double、Float、Short、BigInteger、BigDecimal

包装类比较对象中的元素要用 equals()；方法，不能用 ==（比较地址），因为能出现地址不同，元素内容相同.

**但是**在 BigDeciaml 中需要比较到元素数据的数学性质时，要注意不能使用 equals(); 要使用 compareTo(); 方法，因为元素的小数位数的不同会导致元素的内容不同，但在数学上：18.00 = 18 ，不能因为小数内容干扰是否相等的判断。



#### 装箱与拆箱：

装箱：内置数据类型被当作对象使用的时候（装箱），就可以调用方法了。

拆箱：把对象，像内置类那样，直接使用符号进行运算。



#### 不可变类：

一旦实例被创建，不可能改变其成员变量的值。

所有包装类和 String 都是不可变类。

不可变类的对象是不可改变的，因此需要拷贝该内容时可以不复制其本身，只要复制地址储存地址就可，这样提高效率优化内存，同时在多线程下不会被其他线程篡改，省掉同步锁。正因如此，给此类型的类的对象赋新值时，并不是改变对象本身而是创建新的对象，如频繁用到，会产生很多无用拉级，建议使用可代替的可变类如：String 和 StringBuffer



------

### 数学有关的类

Math类：包含执行基本数字运算的方法，如基本指数，对数，平方根和三角函数。 

StrictMath类：方法同于 Math 类，解决不同平台（X86 ARM）之间浮点计算误差不相同问题,但速度不如 Math 类。



------

### 随机数有关的类

Random类：生成伪随机数。可设定生成随机数的界限以及宽度（数字的总位数）。

SecureRandom类：提供了一个密码强的随机数生成器，继承于 random 类。

**ThreadLocalRandom**：继承于 random 类 ，最主要的作用 解决 random 类中一些 方法无法设置两边边界的问题。该方法是个静态方法不能直接创建对象（单例设计模式） 但可以调用该类中 current(); 去使用该类的其他方法。



------

### 时间有关的类

Date 类：分配当前的时间，或给定一个linux时间戳去分配（因为以毫秒不是秒计算，使用时别忘*1000否则会在1970年）。

DateForamt 类：是一个用于日期/时间格式化子类的抽象类，它以语言无关的方式格式化和分析日期或时间。

SimpleDateFormat 类：继承于 DateFormat 类，用于以区域设置敏感的方式格式化和解析日期，该类提供很多常量用于格式化 。

Calendar 类：可以为在某一特定时刻和一组之间的转换的方法，提供大量关于时间的字段用于操纵该日历字段 。这是个抽象类，但他提供静态方法供使用。

GregorianCalendar 类：继承Calendar类，提供了世界上大多数国家使用的标准日历系统。

LocalDate 类：一个不可变的日期时间对象，表示日期，通常被视为年月日。 也可以访问其他日期字段，例如日期，星期几和星期。  例如，值“2007年10月2日”可以存储在`LocalDate` 。 

LocalDateTime 类：是一个不变的日期时间对象，代表日期时间，通常被视为年 - 月 - 日 - 小时 -  秒。 也可以访问其他日期和时间字段，例如日期，星期几和星期。 时间表示为纳秒精度。  例如，值“2007年10月2日在13：45.30.123456789”可以存储在`LocalDateTime`  。

------

### maven库和junit单元测试框架在企业中的用途

junit单元测试框架：又称模块测试。



------

### 字符串

String类：字符串类，提供方法操作字符串。Java程序中的所有字符串文字（例如`"abc"` ）都被实现为此类的实例。

```java
String.format - 使用指定的格式字符串和参数返回格式化的字符串。(可解决在 仅限格式化输出时 小数的位数)
```

**注意:**字符串不变; 它们的值在创建后不能被更改。 字符串缓冲区支持可变字符串。  因为String对象是不可变的，它们可以被共享。因此再使用String类时，往字符串中追加字符串，实际上是又新建一个和源对象名字相同的新对象，但旧对象还是存在的，如大量操作会损失大量的性能。

StringBuilder类：为字符串插入和追加解决上述问题，该类在多线程中无法同步，但速度快。

StringBuffer类：解决StringBuilder，线程同步问题。

```bash
# 需要说明的是，CharSequence就是字符序列(还是个接口String类实现了它)，String, StringBuilder和StringBuffer本质上都是通过字符数组实现的！

# 源码中 String 类的 equals 的方法继承于 Object 类,Object 类中的 equals 方法只对比对象的地址,String 类的 equals 的方法虽然重写但仅支持 String 类的对象去对比其内容字符串是否相同


```

 

------

### 异常

Throwable类：是Java语言中所有错误和异常的超类。

Error类：错误类，是Throwable的直接子类。

Exception类：异常类，是Throwable的直接子类。

```bash
# Error类的使用场景：  
是指程序无法处理的错误，表示应用程序运行时出现的重大错误。(很难通过完善代码修复)例如jvm运行时出现的, OutOfMemoryError以及Socket编程时出现的端口占用等程序无法处理的错误。

# Exception类的使用场景:
 * 异常可分为运行时异常跟编译异常
 * <1> 运行时异常：即RuntimeException及其之类的异常。这类异常在代码编写的时候不会被编译器所检测出来，是可以不需要被捕获，
 * 但是程序员也可以根据需要进行捕获抛出。常见的RUNTimeException有：NullPointException（空指针异常），
 * ClassCastException（类型转换异常），IndexOutOfBoundsException（数组越界异常）等。
 *
 * <2> 编译异常：RuntimeException以外的异常。这类异常在编译时编译器会提示需要捕获，如果不进行捕获则编译错误。
 * 常见编译异常有：IOException（流传输异常），SQLException（数据库操作异常）等。
 *
 * 注意：异常和错误的区别：异常能被程序本身可以处理，错误是无法处理。
```

RuntimeException类：继承于Exception类，各种运行时异常的超类，多出现语法没有错误（代码可编译）但运行时出错。

ReflectiveOperationException类：继承于Exception类，各种反射异常的超类（java的反射是指程序在运行期间可以拿到对象的的所有信息）。

![](E:\learnt\JAVA\异常跟错误都继承于Throwable类.png)



#### 异常处理

```java
// 异常处理两种办法：

// try catch finally -捕获异常 ->使用场景：捕获异常并个人处理彻底解决问题，其他使用者使用没问题。
try() {
    // 有异常的程序代码
} catch(异常类型 异常变量名) {
	// 调用异常方法，或根据需求要写的代码    
} finally{
    /* 
    finally 代码块无论是否捕获成功异常都会执行，即使在 catch 代码块中添加 return 关键字，并捕获异常成功也会先执行 catch 代码块中其他内容，再执行 finally 代码块的内容，最后执行 returen ，如果 finally 代码块中恰好也有return ，那 catch 里的 returen 毛用没有。
    因此，finally 代码块适合运行清理等善后代码。
    */
}

// throws throw -抛出异常并声明异常 ->使用场景：抛出异常并提示所有使用者，并让 JVM 自行解决。
public void demo() throws 异常类型，可多个{
    throw new 异常类型对象
}
```

存在多个 catch 时，注意 catch 的顺序，异常类的子类要在异常类的父类之前，以避免想要捕获的异常丢失的问题。

自己编写的类继承各种异常类，可自定义异常。

IllegalArgumentException：非法或不正确的参数异常



------

###  

### 文件	&	输入输出流(File 	&	I/O Stream)

#### 文件

文件(file) 	文件夹(folder) 	文件路径(file path) 	目录(directory)

绝对路径  (absolut path)	相对路径  (relative path)

Windows10 的文件路径的书写方式与 Linux 的不同：

- UNIX根目录的磁盘驱动器说明符"/"
- Windows UNC路径名的"\\"

File 类：文件和目录路径名的抽象表示。 并提供一些方法进行操作。



#### 输入输出流

##### 介绍

Java.io 包几乎包含了所有操作输入、输出需要的类。

I/O 流表示输入源或输出目标。一个流可以表示许多不同类型的源和目标，包括磁盘文件、设备、其他程序和内存阵列。

Input : 输入       Output: 输出

判断输入还是输出要站在操作目标的角度上。

因我们操作的目标是 Java program(程序)：

- 从一个数据源读取数据 ———— 输入流： InputStream
- 向一个目标写入数据 ———— 输出流： OutputStream

![](E:\learnt\JAVA\IOStream\Reading information into a program.gif)

读取输入(例：查阅文件)



![](E:\learnt\JAVA\IOStream\Writing information from a program.gif)

写入输出(例：保存文件)



##### 类介绍

byteStreams : 字节流
程序使用字节流来执行 8 位字节的输入和输出。

字符流在 AIP 中属于 IO 包，但不在 InputStream 和 OutputStream 抽象类中.
字符流只能使用文字类的文件。

字符流和字节流是可以互相转换的使用：InputStreamReader 和 OutputStreamWriter ,
这两个类是没有缓冲区的，建议用 Buffered 类 包装一下再去使用。

缓存区：普通字节流或字符流读取一个字符的字节编码，进行操作，将多个字符的字节编码打包成数组存入缓存，当数组存满时在一起操作。

Java 提供带缓存区的类(带Buffered)：

* 装饰设计模式：（普通套餐的升级）
* 使用装饰设计模式的类，需要有这种类的基础类。（这种类算是基础类的 VIP 版本）
* 有四个缓冲流类用于包装非缓冲流：
* BufferedInputStream并 BufferedOutputStream创建缓冲字节流，而 BufferedReader BufferedWriter 创建缓冲字符流。



![](E:\learnt\JAVA\IOStream\IOStream.png)

PrintStream：装饰类一种负责格式化输出，构造可传入输出流，以及文件名字(并可以指定字符集)，该类中的方法不会抛出I / O异常。

PrintWriter：PrintStream 类的“字符流”版本，当然对字符的输出格式更多。

#### **注意：输出时如果不是追加内容将会覆盖源文件。**

------



### JAVA 的多线程

多线程编程：当一个程序中多个线程对同一个共享的资源，进行抢占并操作。

- 多线程模型是 JAVA 最基础的并发模型。
- 读写网络数据，数据库，Web开发,都要依赖 JAVA 多线程模型



#### 并发与并行

##### 并发 Concurrency

可以在同一段时间内做不同的事情，**不同任务交替工作。**

##### 并行 Parallelism

可以在同一时刻做不同的事情，**不同任务同时工作。**



#### 进程与线程 

**线程存在于进程中，一个进程中必须要有一个线程。**

##### 进程  Process

- 一个进程有一个独立的执行环境。
- 一个进程通常有一套完整的、私有的基本运行时资源；特别是，每个进程都有自己的内存空间；因而使得多进程之间的通讯效率低于多线程。
- 进程通常被视为程序或应用程序的同义词。然而，用户所看到的单个应用程序实际上可能是一组协作进程。
- JVM 的大多数实现都作为单个进程运行。Java 应用程序可以使用 ProcessBuilder对象创建其他进程。
- 多进程应用程序，是健硕的在安全情况下，一个进程的崩溃不会导致整个应用或其他进程崩溃。



##### 线程 Thread

* 线程有时被称为轻量级进程。进程和线程都提供了一个执行环境，但是创建一个新线程比创建一个新进程需要更少的资源。
* 线程存在于进程中每个进程至少有一个。线程共享进程的资源，包括内存和打开的文件。这有助于高效但可能存在问题的沟通。
* 一个 JAVA 程序实际上是一个 JVM 的进程，JVM 的进程中又有一个主线程来执行，这个就是我们 main 方法。
* 在主线程中我们可启动多个子线程，就可以执行多个任务。
* 当然 JVM 进程除了主线程外还有一些工作线程(又称用户线程(就是是你自己写的线程这又相当于主线程的子线程))为进程服务，主线程停掉不会影响子线程工作。



##### 线程的调度

- 线程的调度，是由操作系统系统决定的，JVM 也是操作系统中的进程之一。
- 因此在 JAVA 中使用代码调整优先级(priority)并不一定能使高优先级的线程先的任务先执行。
- 尤其是在低任务或高性能处理器面前，确实是设置高优先级，但处理速度太快，就像没设置一样。
- 综上，如果有优先级调度的需求建议使用线程通信(线程之间：唤醒与等待与插队)，而别以来优先级调度。



##### 扩展：

一个应用程序，在进程和线程中可有多种搭配实现：

- 多进程模式（多个进程每个进程只有一个线程）
- 多线程模式（一个进程但里面有多个线程）
- 多进程加多线程组合



#### JAVA 中创建线程

##### 要用到类和接口介绍

java.lang 包下的 Thread 类，该类继承于 Object 实现  Runnable 接口

- Thread 类负责提供控制线程的方法和变量。
- Runnable 接口负责提供一个名为 run() 的抽象方法，用于该接口被实现后写入线程要执行的内容。
- Thread 类中提供了传入 实现了 Runnable 接口的类的构造

简单控制线程的方法(Thread Api中的一些方法)：

- start() 方法打开线程 (不要 run() 方法，那只是单纯调用方法)
- sleep(long millis) 方法暂停线程执行绪设定暂停时间 
- setPriority(int newPriority) 更改此线程的优先级。 JVM 1~10 等级默认5。除了1~10常量还有字符定义的三个常量，分别为：MAX_PRIORITY = 10，MIN_PRIORITY = 1，NORM_PRIORITY = 5。main 线程为5。



##### 创建方法

根据 Runnable 接口 和 Thread 类的关系得出：

- 当线程内容不需要继承其他类的时候可以让写线程内容的类直接继承 Thread  类并复写 run() ，使用时直接实例我们自己写类，并调用 Thrad 类 的方法即可。
- 当线程内容需要继承其他类的时候，由于 JAVA 单继承的特性，写线程内容的类不能继承 Thread 了，就先实现 Runnable 接口 ，把线程的执行内容写完。在使用时实例 Tread类，并在其对象内传入，写线程内容的类的对象。

```java
Thread thread = new Thread(new MyThread);
thread.start();
```



#### Daemon Thread守护线程

守护线程是一个奇特的线程，他为主线程以及子线程服务，在主线程或子线程结束后，自动结束，并与主线程一起销毁。

- 守护线程当进程不存在或主线程停止，守护线程也会被停止。
- 当所有的非守护线程结束时，程序也就终止了，同时会杀死进程中的所有守护线程
- 例：gc线程 （线程不定时回收垃圾）属于守护线程。
- 在守护线程中产生的新线程也是守护线程。
-  不要认为所有的应用都可以分配给守护线程来进行服务，比如读写操作或者计算逻辑。



可以自己创建守护线程

- 名字要易识别
- 调用 Thread 类中的 setDeamon(true) 方法 
- **注意：**必须在调用线程的 start() 方法之前设置，否则会抛出IllegalThreadStateException异常。
- isDaemon() 方法可测试该线程是否是守护线程， 返回 bollean 值。





#### 线程的执行状态

##### 自然状态

 多线程的执行顺序**在没有控制需求的情况下**就像地铁上的乘客一样，主线程(main)是地铁，子线程时乘客。

- 当在主线程中开启子线程时，子线程开始执行，与此同时主线线程也会同步执行，直到各自执行完各自的内容，或出现突发情况终止。
- 就像这趟地铁(主线程)只会沿着既定线路行驶，但车上的乘车(开启的子线程)会去往自己需要地方，因此地铁和乘客都在同时执行自己的事情。

##### 实际状态

但为了满足实际需要我们肯定需要控制线程，当我们控制线程时，这些线程会有不同的状态：

1. New ：新创建的线程，还没有开始执行
2. Runnable：正在执行的线程，执行 run(); 方法中的 JAVA 代码
3. Blocked：正在执行的线程，但因需同步共同的变量信息或其他操作，所阻塞而被挂起
4. Waiting：正在执行的线程，但因要配合其他线程的执行，完成线程的通信而等待中，只能被唤醒。
5. Timed Waiting：和 Waiting 状态类似但，该状态是通过计时等待，计时结束自动唤醒。
6. Terminated：线程终止，线程执行结束或出现异常被迫结束

线程的执行可在在上述 2 3 4 5 这几个状态中进行切换以满足线程之间通信来实现用户的具体需求。

实现以上状态需要用到 Api 来自不同的类，下面分状态介绍。



#### 同步 锁 Block

##### 共享与抢占带来的问题

线程主要通过 对字段和 对象引用字段 的共享访问来进行通信。这种通信形式非常高效，但线程运作是抢占式的，会导致两种错误：线程干扰和内存一致性错误。

- 线程干扰反例：当一些严格操作的业务场景时，不同的的执行功能会出现干扰，例如账户中0元，线程A：存入500，线程B：取出200，B线程抢占到了取出200，0元账户取出200 能 ？
- 内存一致性反例：网上抢鞋子就剩最后一双，A线程去抢，B线程也去抢，A先抢到，内存不一致B也能抢到？

因此我们需要一把“锁”，规范线程的执行不受干扰，同步线程内存使其一致。



##### 锁是否公平

Java 中的锁总共可分为两类：公平锁和非公平锁。

- **公平锁：**每个线程获取锁的顺序是按照线程访问锁的先后顺序获取的，最前面的线程总是最先获取到锁。
- **非公平锁：**每个线程获取锁的顺序是随机的，并不会遵循先来先得的规则，所有线程会竞争获取锁。
- **举个例子：**公平锁就像开车经过收费站一样，所有的车都会排队等待通过，先来的车先通过，



##### 使用同步锁所需的类与方法

###### synchronized  同步锁

- 写代码时发现 synchronized 是关键字，他基于 JVM 层面（随着版本更迭可能性能会变强）。
- 使用时需要新建并传入 Object 对象。(相当于一个判断机制)
- 同步代码块：线程 run() 方法中需要上锁的内容。
- 同步方法：synchronized 修饰的方法
- 非公平锁

```java
public class ThradA implements Runnable {
    Object lock = new Object();
	@override
	run(){
		synchronized(lock){
 			// 上锁内容       
    	}
	}
}  
```



###### 同步语句

- ReentrantLock 类中的方法完成同步,还有关于锁设置以及查验等操作的方法。
- lock() 方法上锁， unlock() 方法解锁，千万别忘了解锁，否则会出现死锁的情况。
- 死锁是一种持久型的状态。多个线程同时被阻塞,它们中的一个或者全部都在等待某个资源被释放。程序和线程都处于等待状态。
- 默认构造非公平锁。
- ReentrantLock(boolean fair) 该构造可创建公平锁。
- 该类实现于 Lock  和 Serializable 接口。

```java
public class ThradB implements Runnable {
    // 创建一个公平锁
	ReentrantLock reentrantLock = new ReentrantLock (ture);
	@override
	run(){
         // 上锁
        try{
            reentrantLock.lock();
            // 上锁内容
        }catch (Exception e){
            e.printStackTrace();
            System.out.println(Thread.currentThrad().getName() + "线程上锁出现异常！");
        }finally{
            // 解锁
            try{
                reentrantLock.unlock();
            }catch (Exception e){
                e.printStackTrace();
                System.out.println(Thread.currentThread().getName() + "线程开锁出现异常");
            }
        }
	}
}  
```



#### 线程的通信

##### 同一类型多线程之间通信（线程调度）

可使用 Thread 类中的方法进行通信

###### join

```java
/* 线程插队（属于线程调度）
 * join()
 * join(long millis)
 * join(long millis, int nanos)
 * 调用该方法后，后面还未执行的代码（子线程调用等），都必须等，
 * 等到使用 join() 方法的线程执行完毕才能继续执行。
 * join() 方法中的参数，是使用 join() 方法的线程执行的时间限制，
 * 超过设置的时间限制，直接执行后面的代码。（这种方法叫 超时等待 或 即使等待）
 * millis - 以毫秒为单位等待的时间
 * nanos - 0-999999等待的额外纳秒
 * 换算进率为1000
 * 1 毫秒 = 1000000 纳秒
 * 1 秒 = 1000 毫秒
 * 1 毫秒 = 1000 微秒
 * 1 微秒 = 1000 纳秒
 */
```



###### sleep

```java
/* 静态方法：线程休眠 （属于线程调度）
 * sleep(long millis)
 * sleep(long millis, int nanos)
 * 导致正在执行的线程以指定的毫秒数加上指定的纳秒数来暂停（临时停止执行），
 * 这取决于系统定时器和调度器的精度和准确性。 线程不会丢失任何显示器的所有权。
 * 该方法需要抛出异常，并需要 Try Catch 包裹。
 */
```



###### yield

```java
/* 静态方法：线程让步 （属于线程调度）
 *  yield() 对调度程序的一个暗示，即当前线程愿意产生当前使用的处理器。
 * 它让掉当前线程 CPU 的时间片，使正在运行中的线程重新变成就绪状态，并重新竞争 CPU 的调度权。
 * 它可能会获取到，也有可能被其他线程获取到。
 * 因此无法保证yield()真的能达到让步目的，因为让步的线程还有可能被线程调度程序再次选中。
 */
```



##### 不同类型线程之间的通信(等待唤醒机制)

可使用 Object 类中的方法

###### wait

```java
/*
* void wait()
* 导致当前线程等待，直到另一个线程调用该对象的 notify()方法或 notifyAll()方法。
* void wait(long timeout)
* 导致当前线程等待，直到另一个线程调用该对象的 notify()方法或 notifyAll()方法，或指定的时间已过。
* void wait(long timeout, int nanos)
* 导致当前线程等待，直到另一个线程调用该对象的 notify()方法或 notifyAll()方法，或者某些其他线程中断当前线程，
* 或者已经过了一定量的实时时间。
* 使用该方法有异常：
* IllegalMonitorStateException - 如果当前线程不是对象监视器的所有者。
* InterruptedException - 如果任何线程在当前线程等待通知之前或当前线程中断当前线程。
* 当抛出此异常时，当前线程的中断状态将被清除。
*/
```



###### notify notifyAll

```java
    /*
     * void notify()
     * 唤醒正在等待对象监视器的单个线程。 如果任何线程正在等待这个对象，其中一个被选择被唤醒。
     * 选择是任意的，并且由实施的判断发生。 线程通过调用wait方法之一等待对象的监视器。
     *
     * 唤醒的线程将无法继续，直到当前线程放弃此对象上的锁定为止。
     * 唤醒的线程将以通常的方式与任何其他线程竞争，这些线程可能正在积极地竞争在该对象上进行同步;
     * 例如，唤醒的线程在下一个锁定该对象的线程中没有可靠的权限或缺点。
     *
     * 该方法只能由作为该对象监视器的所有者的线程调用。 线程以三种方式之一成为对象监视器的所有者：
     * 通过执行该对象的同步实例方法。
     * 通过执行在对象上同步的synchronized语句的主体。
     * 对于类型为Class,的对象，通过执行该类的同步静态方法。
     * 一次只能有一个线程可以拥有一个对象的显示器。
     *
     * notifyAll()
     * 唤醒正在等待对象监视器的所有线程。 线程通过调用其中一个wait方法等待对象的监视器。
     *
     */
```



------



### 集合 

数组可以存基础类型也可以存储对象，但有一下致命缺陷催生了集合诞生这也是集合最直观的优势：

- 数组初始化后大小不可变，但集合可以自动扩容。
- 数组只能按照索引顺序存取，但集合可以通过其自身的方法(当然使用索引也可以)不借助索引完成存取操作。

#### 集合家族结构 `Collection` `Map`

Java标准库自带的`java.util`包提供了集合类：`Collection`，它是除`Map`外所有其他集合类的根接口。Java的`java.util`包主要提供了以下三种类型的集合：

- `List`：一种有序列表的集合，例如：按索引排列的`Student`的`List`；
- `Set`：一种保证没有重复元素的集合，例如：所有无重复名称的`Student`的`Set`；
- `Map`：一种通过键值（key-value）查找的映射表集合，例如：根据`Student`的`name`查找对应`Student`的`Map`。

![](E:\learnt\JAVA\Collections  Framework\Collection.png)



![](E:\learnt\JAVA\Collections  Framework\Map.png)



Java 集合设计有两大特点：

- 接口与实现类分离，结构脉络有条理。
- 引入泛型，可规定类型。



由于Java的集合设计非常久远，中间经历过大规模改进，我们要注意到有一小部分集合类是遗留类，不应该继续使用：

- `Hashtable`：一种线程安全的`Map`实现(里面有很多同步方法，单线程情况下比`HashMap`要慢很多),被 Jdk1.5提供的 **`ConcurrentHashMap`**(支持检索的完全并发性和更新的高预期并发性的哈希表。 该类符合与`Hashtable`)相同的功能规范，并包括与`Hashtable`每种方法对应的方法的`Hashtable`  。)所替代 ；(ps：之前有傻逼面试官我问过我`HashMap`与`Hashtable`的区别，我当时一口咬定没有`Hashtable` 这种东西，之前毕竟第一遍学`Java`。这种淘汰掉东西，我压根没看，哈哈哈。一个合格的开发者不应该用`Hashtable`这种淘汰货，既然用不到那比啥？)
- `Vector`：一种线程安全的`List`实现,但是大多数情况下不使用Vector，因为操作Vector效率比较低；
- `Stack`：基于`Vector`实现的`LIFO`的栈。

还有一小部分接口是遗留接口，也不应该继续使用：

- `Enumeration<E>`：已被`Iterator<E>`取代。

Java集合使用统一的`Iterator`遍历，尽量不要使用遗留接口。因此 `Collection`接口 继承于`Iterable` 接口。



#### Collection List

有序列表集合的根接口，本质上是更加灵活的数组。

**元素存储特色：** 

- 元素有特定顺序
- 元素可以重复，实际对象层面而非地址层面。
- 元素可以是`null`,而且可重复
- 元素插入时可指定位置，但不能超过整个集合的宽度
- 元素可以通过整数索引访问并搜索。

**注意：**`List` 自己提供了一个 `List.of()` 这个静态方法让你可以使用这借口创建集合，但无论在性能方面还是规范方面都不建议使用该接口。



##### ArrayList

集合界的扛把子使用特频。除了实现`List`接口之外，该类还提供了一些方法来处理内部用于存储列表的数组的大小。  （这个类大致相当于`Vector` ，除了`ArrayList`是不同步的。） 

###### 常用方法

```java
boolean add(E e); // 将指定的元素追加到此集合列表的末尾。元素的类型可以根据自己设定的类型添加
void add(int index,  E e); // 在此集合列表中的指定位置插入指定的元素。
void clear(); // 从列表中删除所有元素。 此呼叫返回后，列表将为空。
boolean contains(Object o); // 如果此列表包含指定的元素，则返回true 。
get(int index); // 返回此列表中指定索引位置的元素。
set(int index, E e); // 用指定的元素替换此列表中指定位置的元素。
int indexOf(Object o); // 返回此列表中指定元素的第一次出现的索引，如果此列表不包含元素，则返回-1。
boolean isEmpty(); // 如果此列表不包含元素，则返回 true ,反之 false。
remove(int index); // 删除该列表中指定位置的元素,该方法在使用在 Integer 类型上，会出现索引和元素之间混乱，会自动识别为索引而不是元素。
boolean removeAll(Collection<?> c); // 从此列表中删除指定集合中包含的所有元素
boolean retainAll(Collection<?> c); // 从此列表中删除其中不包含在指定集合中的所有元素。
int size(); // 返回此列表中的元素数, 形式和数组宽度的 length 关键字相同，但是 size() 是方法。
List<E> subList(int fromIndex,int toIndex); // 返回指定的fromIndex 和 toIndex 之间的列表部分的元素。fromIndex - 子列表的低端点（包含）toIndex - 子列表的高端点（不包含）
toArray(); // 以正确的顺序（从第一个到最后一个元素）返回一个包含此列表中所有元素的数组。如果想接收返回后的数组需要创建一个合集泛型相同类型的数组，去接收集合转化后的数组。设置数组的宽度可以用 size() 方法解决。

```



##### LinkedList

`LinkedList` 链表实现了两个接口：`List` 与  `Deque`两个接口。该实现类不同步

- `Deque` 接口(双端队列->两端都可进出->支持两端元素插入和移除的线性集合。)注意：该接口不能存null，但元素可重复。
- 因此当`LinkedList`作为列表时可存Null，以及满足`List`的**部分**特性 。反之当作为队列或堆栈时要满足`Deque`特性。

###### 特色花活链表：

链表：储存的元素在链表中是一个节点的形式储存，而这个**节点:**不但储存元素还存储指向前一元素和后一个元素的地址信息。

- 单向链表：节点中只存储后一元素指向的地址。
- 双向链表：节点储存前一和后一元素指向的地址。**`LinkedList`使用双线链表**
- ![](E:\learnt\JAVA\Collections  Framework\链表分为单向和双向 linkedList 双向.png)

正因`LinkedList`舍弃了元素索引使用链表，使得其对元素的增删效率高于`ArrayList`，同时也因索引，使其查改效率不如`ArrayList`。

**注意：linkedList.add(int index, Object item) 这个方法中的`int index`并不是链表的索引而是：一个逻辑索引 -> 实际上是从头开始迭代到达该节点之前需要迭代的次数，并不能提供搜索索引的能力。**

![](E:\learnt\JAVA\Collections  Framework\arrayList  和linkedList 差异.png)

ArrayDeque: 基于数组实现的线性双向队列，通常作为栈或队列使用，但是栈的效率不如LinkedList高。
LinkedList: 基于链表实现的链式双向队列，通常作为栈或队列使用，但是队列的效率不如ArrayQueue高 。



###### 常用方法

```java
void addFirst(E e); // 向队头插入元素。
void addLast(E e);  // 将指定的元素追加到此列表的末尾。此方法相当于add(E) 。
E element(); // 检索但不删除此列表的头（第一个元素）。NoSuchElementException - 如果此列表为空
E void getFirst();// 返回此列表中的第一个元素。NoSuchElementException - 如果此列表为空
E void getLast(); // 返回此列表中的最后一个元素。NoSuchElementException - 如果此列表为空
boolean offerFirst(E e); // 向队头插入元素，如果插入成功返回true，否则返回false
boolean offerLast(E e); // 向队尾插入元素，如果插入成功返回true，否则返回false
// 检索的意思：找到并索取资料->在这里意思时查找元素找到并返回。
E peek(); // 检索但不删除此列表的头（第一个元素）并返回。如果此列表为空则为null。
E peekFirst(); // 检索但不删除此列表的第一个元素，并返回。如果此列表为空，则返回 null 。
E peekLast(); // 检索但不删除此列表的最后一个元素，并返回。如果此列表为空，则返回 null 。
E poll(); // 检索并删除此列表的头（第一个元素）。如果此列表为空则为null。
E pollFirst(); // 检索并删除此列表的第一个元素，如果此列表为空，则返回 null 。
E pollLast(); // 检索并删除此列表的最后一个元素，如果此列表为空，则返回 null 。
E pop(); // 从此列表表示的堆栈中弹出一个元素。 换句话说，删除并返回此列表的第一个元素。此方法相当于removeFirst() 。NoSuchElementException - 如果此列表为空
void push(E e); // 将元素推送到由此列表表示的堆栈上。 换句话说，在该列表的前面插入元素。此方法相当于addFirst(E) 
E removeFirst(); // 从此列表中删除并返回第一个元素。
E removeLast(); // 从此列表中删除并返回最后一个元素。
boolean removeFirstOccurrence(Object o); // 删除此列表中指定元素的第一个出现（从头到尾遍历列表时）。 如果列表不包含该元素，则它不会更改。
boolean removeLastOccurrence(Object o); // 删除此列表中指定元素的最后一次出现（从头到尾遍历列表时）。 如果列表不包含该元素，则它不会更改。


```



#### Iterator

`iterator`迭代器接口，在`Iterable` 接口中被引用， `Collection`接口 继承于`Iterable` 接口。

负责遍历集合中的元素。(遍历中也可提供修改)解决 `for i`循环书写复杂，`for each`循环无法修改集合元素问题。

##### 使用迭代器：

- 需要用到 public interface Iterator<E> 这是一个接口，只可引用没法给对象。
- 因此 一个Enumeration（举例，枚举）可以被转换成一个Iterator通过使用Enumeration.asIterator()方法。
- **使用迭代器修改元素内容时要注意：修改元素的泛型是包装类的情况下，集合中的元素不得有null否则会出现空指针异常。**

##### 方法介绍

```java
// 迭代器的方法一共四个直接介绍了
default void forEachRemaining(Consumer<? super E> action);// 对每个剩余元素执行给定的操作，直到所有元素都被处理或动作引发异常。

boolean hasNext(); // 如果迭代具有更多元素，则返回true 。换句话说，如果true将返回一个元素而不是抛出异常，则返回true。

E next(); // 返回迭代中的下一个元素。 NoSuchElementException - 如果迭代没有更多的元素

default void remove(); 
/*     
* 从底层集合中删除此迭代器返回的最后一个元素（可选操作）。
* 这种方法只能在每次调用next()时调用一次。
* 异常
* UnsupportedOperationException - 如果此迭代器不支持 remove操作
* IllegalStateException - 如果 next方法尚未被调用，
* 或 remove方法在最后一次调用 next方法之后已经被调用
* 使用迭代器需要方法 hasNext() 和 next() 配合使用，
* 因此不建议 for 循环中 嵌套 迭代器 使用，会出现异常（空指针问题）。
*/
```



##### `for I`、for each`、`iterator`的区别、注意事项和分别用途：

 * `for I` 适合数据的读取与修改
 * `for each` 适合数据的读取（上升到对象引入也可修改）
 * `Iterator` 适合数据的读取与修改
 * `for each` 已经是一个小型的迭代器了，如果一定要修改集合的话可以使用迭代器，但不建议在`for each`中使用对象引用去修改元素。
 * 如果是 `ArrayList` ，用三种方式遍历的速度是 `for>Iterator>forEach`，速度级别基本一致，一般都会用`for`或者`for each`，因为`Iterator`写法相对复杂一些
 * 如果是 `LinkedList`，则三种方式遍历的差距很大了,数据量大时越明显，`Iterator>forEach>>>for`，推荐使用`foreach`或者`Iterator`，但 `Iterator` 更灵活，`forEach` 有限制。



##### 案例

```java
public class IteratorApiTest {
	public void TestOne() {
        // 简单使用迭代器，并指定输出的元素在迭代输出对应时删除。
        ArrayList<String> nameList = new ArrayList<>();
        nameList.add("Tim");
        nameList.add("Jack");
        nameList.add("Sam");
        nameList.add("Jerry");
        nameList.add("Bob");
        nameList.add("Morty");
        nameList.add("Rick");
        System.out.println(nameList);

        // 创建迭代器
        Iterator<String> it = nameList.iterator();
        // 遍历，并删除指定元素
        while (it.hasNext()) {
            String value = it.next();
            if (value != "Sam") {
                System.out.println(value);
            } else {
                it.remove();
            }
        }
        System.out.println(nameList);
	}
}
```



#### Collection Set

`Set` 集合通过 `java.util.Set` 接口在集合框架中实现。同样他继承 `collection `接口，因此也可以使用迭代器 `iterator`

`Set`接口，由哈希表（实际为`HashMap`实例）支持,因此有以下特点：

- 使用哈希表储存，就如同给每个元素上了身份证号(哈希码)，使得元素不依靠索引储存本身也没有链表或队列的关系，也就输出无序可言。
- 也正因为每个元素都有自己的哈希码也使得，`HashSet`里存储的元素不可重复。
- 更重要的是`Set`虽然继承`Collection`但底层使用`Map`实现，因此`Map`中的部分类可以转化`Set`中的对应的类来使用迭代器功能。
-  `Set`  没有替换指定位置元素的方法，要修改元素需删除重新添加。

`Set` 常用的实现类 `HashSet` 和 `LinkedHashSet` 。



##### HashSet

`HashSet` 类用于创建使用哈希表进行存储的集合。

- 该类不同步。
- 该类允许`null`值。
- 可以自动扩容，初始容量为 16 ，扩容临界值为容量 0.75 ，也就是当储存 12  的位置时，自动扩容为原容量双倍，同时临界值也是新容量 0.75。
- 初始容量是可以更改的详见构造：HashSet(int initialCapacity, float loadFactor）

```java
HashSet(int initialCapacity, float loadFactor）
/* 参数：
         initialCapacity - 初始容量
         loadFactor - 负载因子（使用总容量的多少时扩容，总容量为一所占百分比转化小数）*/
        
boolean add(E e); // 将指定元素添加到此集合 如果此集合尚未包含指定的元素 返回 ture 如果此集合包含指定的元素（源码使用Objects.equals(e, e2)），不会有任何改变并返回 false

void clear(); // 从此集合中删除所有元素。 此呼叫返回后，该组将为空。
Object clone(); // 返回此 HashSet实例的浅拷贝：元素本身不被克隆。这个集合的浅拷贝
boolean contains(Object o); // 如果此集合包含指定的元素，则返回true 。更正式地说，返回true当且仅当此set包含的元素e这样Objects.equals(o, e) 。
boolean isEmpty(); // 如果此集合不包含元素（里面一个元素都没有），则返回 true 反之false。
Iterator<E> iterator(); // 返回此集合中元素的迭代器。 元素没有特定的顺序返回。
boolean remove(Object o); // 用于从该集合中删除指定的元素（如果存在）。一旦调用返回ture，此集合将不包含该元素。）
int size(); // 返回此集合中的元素数（其基数）。

```



##### LinkedHashSet

`LinkedHashSet`类是`HashSet`有序版本，引入双向链表。迭代有序，该类不同步。



##### TreeSet

Java TreeSet 类实现了使用树进行存储的 Set 接口。它继承了 AbstractSet 类并实现了 NavigableSet 接口。TreeSet 类的对象按升序存储。NavigableSet实现基于TreeMap

特点：

 - 只包含唯一元素，如 HashSet。

 - 访问和检索时间非常快。

 - 不允许空元素。

 - 非同步的。

 - TreeSet 是使用二叉搜索树实现的，它像红黑树一样是自平衡的。

 - 只能允许那些可比较的泛型类型，这里的比较是通过 调用`Comparable<T>`接口的`compareTo()；`方法实现。

   如果有特殊泛型需求：可实现`Comparable<T>`接口重写`comparaTo()`方法完成自定义操作，比较时大于为1 小于为-1 等于为0

 - 元素有序且默认升序存储(自然排序)，这里的排序顺序是通过`Comparator<T>`接口的`compare()；`方法实现。

   如有特殊排序需求：需自定义一个比较器，可实现`Comparator<T>`接口，重写`compare();`方法

`public interface Comparable<T>` 每个类的对象强加一个整体排序。 这个排序被称为类的**自然排序**  ，类的`compareTo`方法被称为其**自然比较方法** 。(自然：更准些的说是对元素之间直接比较大小)

`public interface Comparator<T>` 比较功能，对一些对象的集合施加了一个整体排序 。(更具有功能性的比较，例如元素之间长度谁长，谁能被5整除等)

 

###### 独有方法

说明：

- TreeSet是有序的Set集合，因此支持add、remove、get等方法。
- 和NavigableSet一样，TreeSet的导航方法大致可以区分为两类，一类时提供元素项的导航方法，返回某个元素；另一类时提供集合的导航方法，返回某个集合。
- lower、floor、ceiling 和 higher 分别返回小于、小于等于、大于等于、大于给定元素的元素，如果不存在这样的元素，则返回 null。

```java
// 自定义排序以及泛型的构造
TreeSet(Collection<? extends E> c) // 构造一个包含指定集合中的元素的新树集，根据其元素的 自然排序进行排序 。 
TreeSet(Comparator<? super E> comparator)  // 构造一个新的，空的树集，根据指定的比较器进行排序。
 // 方法
E ceiling(E e); // 返回比给定元素大的那一堆元素里最小的那个元素，如果集合中有与给定元素相同的元素那么返回与给定相同元素，综上都没有返回 null。
E higher(E e); // 返回这个集合中的最小元素严格大于给定的元素，如果没有这样的元素，则 null 。(和ceiling方法形容相同但没有等于的情况)

E floor(E e); // 返回比给定元素小的那一堆元素里最大的那个元素，如果集合中有与给定元素相同的元素那么返回与给定相同元素，综上都没有返回 null。
E lower(E e); // 返回该集合中最大的元素严格小于给定的元素，如果没有这样的元素，则 null 。(和floor方法形容相同但没有等于的情况)  

Iterator<E> descendingIterator() // 以降序返回该集合中的元素的迭代器。

E first();  // 返回此集合中当前的第一个（最低）元素。
E last(); // 返回此集合中当前的最后（最高）元素。 

E pollFirst(); // 检索并删除第一个（最低）元素，如果此集合为空，则返回 null 。  
E pollLast(); // 检索并删除最后一个（最高）元素，如果此集合为空，则返回 null 。
```



#### Map

`Interface Map<K,V>`：

- `Map` 映射接口是单独一个家族，与  `Collection` 列表集合有本质区别。
- 映射的一个 对象/元素 由两部分组成：键值（Key） 和 对应键的值（Value）。
- 用来实现`Key`和`Vaule`是`Interface Map.Entry<K,V>`,该接口来自`java.util.Map.Entry`，因此`Entry` 是 `Map` 的内部接口。
- 在映射中，基于 `key` 来对储存的元素进行 删改查(RUD) 是很有用的。
- `Map` 不允许重复的`key`，但`vaule`可以有重复的值。
- `Map` 不能被遍历，所以需要使用`keySet()`将`map`中的`key`转化，或`entrySet()`将`map`中`key+vaule`转化，的方法将其转换为 `Set`。



##### HashMap

`HashMap` 是 `Map` 主要实现类之一。

`HashMap` 存储一个元素需要：一个键（Key） 和 对应的键的值（Value），说白了就算是你要存的东西（Value），要给配一个ID（Key）。

`HashMap` 不是同步类。`Java HashMap` 类的初始默认容量为 16，负载因子为 0.75。可在构造中修改。

依赖哈希码来储存因此：

* `HashMap` 中每一个 `Key` 是唯一的（不能重复），一个集合中 `Key` 只允许有一个Null值。
* `HashMap` 中 `Value` 可以为 `Null`。
* `HashMap` 是无序的。

###### 方法介绍

```java
V put(K key,V value); // 将指定的值与此映射中的指定键相关联。 （插入元素）如果插入的元素的 Key 和以储存元素的 Key 相同，那么以储存的元素将会被新插入的元素替代。修改键映射有专门的方法（不推荐这种方式）。
void putAll(Map<? extends K,? extends V> m); // 指定一个 Map 复制到到调用方法的 Map。注意，如果两个 Map 的 Key 有相同的，将会被指定的 Map 替换。
void putIfAbsent(); // 会先判断指定的键（key）是否存在，不存在则将键/值对插入到 HashMap 中。(value 的 Null 在这里判定为不存在，可以插)。

V remove(Object key); // 从该 HashMap 中删除指定键的映射（如果key不存在返回 null，存在返回被删除的value）。
boolean remove(Object key,Object value); //仅当指定的密钥当前映射到指定的值时删除该条目。
void clear(); // 从这该集合中删除所有的映射。 此呼叫返回后，集合将为空。

V get(Object key); // 指定键映射到的值，如果此映射不包含键的映射， null。
V getOrDefault(Object key,V defaultValue); // 返回指定键映射到的值，如果此映射不包含键的映射，则返回 defaultValue(自己设置字段) 。

V replace(K key,V value); // 替换指定键的条目,并返回被修改之前的value,键不存在或没有改变返回null。
boolean replace(K key,V oldValue,V newValue); // 替换指定键的条目,修改成功返回true。

// 转化Collection集合和set集合
Collection<V> values(); // 虽然转化成 Collection 集合，但不支持add或addAll操作。
Collection<String> collection = hashMap.values(); // 转化案例

Set<K> keySet(); // 返回此HashMap中包含的键的Set视图。
Set<Integer> keySet = hashMap.keySet(); // 转化案例

Set<Map.Entry<K,V>> entrySet(); // 返回此HashMap中包含的映射的Set视图。
Set<Map.Entry<Integer,String>> entrySet = hashMap.entrySet(); // 转化案例
Iterator<Map.Entry<Integer,String>> iterator = hashMap.entrySet().iterator; // 只想遍历的写法

```



##### LinkedHashMap

`HashMap` 的有序版本，双向链表实现有序。不同步。



##### TreeMap

底层红黑树实现的`Map`，注意是`Map`,有序但不同步，默认自然排序，修改排序顺序活排序元素参考上面介绍的`TreeSet`。

默认的自然排序：只根据`key`来排序。

