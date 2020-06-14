- [1.Java 基础语法]()
  - [1.1.第一个Java程序](#1.1 第一个Java程序)
  - [1.2.Java程序基本结构](#1.2 Java程序基本结构)
  - 变量和数据类型
  - 整数运算

## 1.Java 基础语法

### 1.1 第一个Java程序

打开文本编辑器，输入以下代码：

```java
public class Hello {
	public static void main(String[] args) {
		System.out.println("Hello, world!");
	}
}
```

在一个Java程序中，你总能找到一个类似：

```java
public class Hello {
	...
}
```

的定义，这个定义被称为class（类），这里的类名是`Hello`，大小写敏感，`class`用来定义一个类，`public`表示这个类是公开的，`public`、`class`都是Java的关键字，必须小写，`Hello`是类的名字，按照习惯，首字母`H`要大写。而花括号`{}`中间则是类的定义。

注意到类的定义中，我们定义了一个名为`main`的方法：

```java
public static void main(String[] args) {
	...
}
```

方法是可执行的代码块，一个方法除了方法名`main`，还有用`()`括起来的方法参数，这里的`main`方法有一个参数，参数类型是`String[]`，参数名是`args`，`public`、`static`用来修饰方法，这里表示它是一个公开的静态方法，`void`是方法的返回类型，而花括号`{}`中间的就是方法的代码。

方法的代码每一行用`;`结束，这里只有一行代码，就是：

```java
System.out.println("Hello, world!");
```

它用来打印一个字符串到屏幕上。

Java规定，某个类定义的`public static void main(String[] args)`是Java程序的固定入口方法，因此，Java程序总是从`main`方法开始执行。

注意到Java源码的缩进不是必须的，但是用缩进后，格式好看，很容易看出代码块的开始和结束，缩进一般是4个空格或者一个tab。

最后，当我们把代码保存为文件时，文件名必须是`Hello.java`，而且文件名也要注意大小写，因为要和我们定义的类名`Hello`完全保持一致。

##  1.2 Java程序基本结构

我们先剖析一个完整的Java程序，它的基本结构是什么：

```java
/**
 * @Author: zhanghan
 * @Date: 2020/6/14 16:17
 * @Description: 可以用来自动创建文档的注释
 */
public class Hello {
	public static void main(String[] args) {
	// 向屏幕输出文本:
	System.out.println("Hello, world!");
	/* 多行注释开始
        注释内容
        注释结束 */
	}
	// class定义结束
}
```

因为Java是面向对象的语言，一个程序的基本单位就是`class`，`class`是关键字，这里定义的`class`名字就是`Hello`：

```java
public class Hello {	// 类名是Hello
  // ...
  // class定义结束
}
```

类名要求：

- 类名必须以英文字母开头，后接字母，数字和下划线的组合
- 习惯以大写字母开头

要注意遵守命名习惯，好的类命名：

- Hello
- NoteBook
- VRPlayer

不好的类命名：

- hello
- Good123
- Note_Book
- _World

注意到`public`是访问修饰符，表示该`class`是公开的。

不写`public`，也能正确编译，但是这个类将无法从命令行执行。

在`class`内部，可以定义若干方法（method）：
