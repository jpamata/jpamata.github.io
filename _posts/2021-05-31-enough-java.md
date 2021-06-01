---
layout: post
title: "Enough Java"
description: The very basics
category: articles
tags: [java]
comments: true
---

The very basics one needs to get started with writing Java programs

<!-- more -->

Java is nice, a platform independent language. When you compile a program with java, the compiler turns it into a platform independent code (which is standard) called the java bytecode, which runs on jvm platforms.


A basic program in Java

```java
//this is a comment, this line of code is not executed
//comments are used for readability, notes, and even TODOs

public class Program{ //we declare a class called Program 
	/*
	this is a multi-line comment
	*/
	//main function is where the program execution begins
    public static void main(Strin[]args){ 
	//the next function prints the string "Hello world" to the console
	System.out.println("Hello world");
    }
}
```

Every code in java is part of a class. It's a collection of classes. Unlike in languages like python which every program can just be a collection of python.

<code>public</code> is used so that the method can be accessed everywhere. As it's the main method, it has to be public for JVM to run it.

<code>static</code> methods can be called without creating objects. As it's the main method, it has to be static as JVM just wants to call the main and not create objects of the class to run it.

<code>void</code> is a return type. In Java, main method has to be void unlike in a language like C++ where the return type is usually of type int.

<code>(String[]args)</code> are arguments for the main, which is basically an array of strings. The <u>args</u> is just a name of the array and can be renamed anyway you want, can be rewritten as <code>String[]x</code> if you're lazy. String[]args is used as the parameter for the main function, as we can easily send a set of strings to test the main from our terminal

<code>System.out.println();</code> prints a string to the console. <code>System</code> is a class in the java.lang package, <code>out</code> is an object in that System class and is of type PrintStream and is used to print something to the standard output, and <code>println</code> is a method of the PrintStream class.


Here's a new java program 

```java

public class Program{
    public static void main(String[]args){
		int integerNum = 420;
		String sentence = "java program";
		double doubleNum = 420.69;
		float floatNum = 69.96f;
		System.out.println(integerNum + " " + sentence + " " + doubleNum + " " + floatNum);
    }
}

```

We have to specify the data types (and thus memory) for a variable in languages like Java and C++ for the compiler. These types of languages are called statically typed languages. Different from dynamically typed languages like Python where you dont have to specify the data type and at runtime, is decided how much memory is allocated for variables - this also makes it slower than statically typed languages.

Data types in the above code are: int, String, double, float

There's more data types as well. I'm lazy so just google what those are (or [here](https://www.w3schools.com/java/java_data_types.asp))or run the program I wrote above and play with it. Create a file with the same name as the class, then on terminal enter <code>$ javac Program.java</code> to compile then afterwards, <code>$ java Program</code> to run

Naming convetion for variable names in Java: 

constants: all capital, has a <code>final</code> keyword preceding the data type, and every word is separated by underscores. For example

```java
final double TETHER_TO_DOLLAR = 1.0;
```

Other variables:  lowercase for the first letter, then every subsequent first letter of a word would be uppercased. For example

```java
double priceOfBitcoinTodayInDollars = 57,816.94;
```

Most of these are called primitive data types. String is the exception as it's non-primitive. Non-primitive data types are objects of classes which can be user defined classes or predefined classes. An example of such data type is an Array, so whenever you create one, you create objects. I'm not really sure why String is non-primitive, perhaps it's because as the intro to Strings section of the book "How to Design Program" says (and we talked about in [Day 16](/articles/2021/04/28/diy-bootcamp-016)), a string is just an array of characters (or in the book, called 1String)

we create non-primitive variables with the new keyword which we'll see below

non-primitives when not initialised, have a default value. Meanwhile primitive types dont. Thus you cant just do something like the following

```java
int anInteger;
System.out.println(anInteger);
```

The above, anInteger being a primitive data type,  will throw an error message saying: <code>variable anInteger might not have been initialized</code>

But if we do that to a non-primitive...

```java
class Testing{
	//anInteger is a member (called element) of class Testing
    int anInteger;
}

public class Program {
    public static void main(String[]args){
	//next line  means we create a new object called "a" of the class "Testing" 
        Testing a = new Testing();
        System.out.println(a.anInteger);
    }
}
```

The above outputs the default for a non-primitive integer, which is 0.

Perhaps the biggest difference to know, is that non-primitives are pretty much just references. By reference we mean it just holds a reference to the object's memory location.

Let's take a look at a new program below

```java
class Number{
    int x;
}

public class Program{
    public static void main(String[]args){
        //new keyword is used to create variables of non primitive
        //see my notes on it sourced from thinking in java, below
        Number num = new Number();
        //access members of a non-primitive var with "."
        //we assign to to num.x
        num.x = 420;
        System.out.println(num.x);
        //output: 420
        Number num2 = num;
        System.out.println(num2.x);
        //output: 420
        num.x = 69;
        System.out.println(num2.x + " " + num.x);
        //output: 69 69
    }
}
```

Any data type from the class Number, the one we created, is a non-primitive.

Like for example num2 variable, is a non-primitive and thus holds just reference. Which is why when we "assigned" it to the value of num, once we changed num.x to 69, the value of the other variable that is a reference to it, which is num2, also changed to 69. Thus resulting to the 69 69 output seen above

In java, non-primitives are stored in the heap memory, while the primitives are stored in the stack memory. Thus when we do the <code>Number num;</code> instead of the one above which is <code>Number num = new Number();</code>, a new keyword, no memory is allocated in the heap, we just have a reference variable.

<code>Number num2 = num;</code> then is just making a reference variable to the memory of num.

Now in Java, one can have non-primitives for every primitive data type through wrapper classes like <code>Character</code> is a wrapper class for <code>char</code>. Another is <code>Integer</code> as wrapper class for <code>int</code>.

Accordign to the javadoc

```
java.lang public final class Integer
extends Number
implements Comparable<Integer>

The Integer class wraps a value of the primitive type int in an object. 
An object of type Integer contains a single field whose type is int.
```

It's pretty useful for generics where you pass data types as arguments to create objects of its data types. An example are java collections. We have to use non-primitives for them. We cant just send ints data type for a hashmap like the following

```java
import java.util.HashMap;

public class Test {
    public static void main(String[]args){
        HashMap<int, int> map=new HashMap<>();
    }
}
```

It will give us the following compiler errror 

```
Error:(5, 17) java: unexpected type
  required: reference
  found:    int
Error:(5, 22) java: unexpected type
  required: reference
  found:    int
```

Instead we have to use wrapper classes for int

```java
import java.util.HashMap;

public class Test {
    public static void main(String[]args){
        HashMap<Integer, Integer> map=new HashMap<>();
    }
}
```

Notice that the wrappr non-primitives have an uppercase first letter. It's a naming convention for classes in Java

Type conversion

We can automatically convert primitive data types in java either through <u>Implicit Conversion</u>. An implicit is where you can assign a variable of a smaller data type to that of a larger data type, like for example an <code>int</code> can be automatically converted to a <code>long</code> or <code>float</code> or <code>double</code>.

```java
int x = 1;
double y = x; //implicit
```

this is the ranking, from lowest to largest data type 

- byte

- short

- char

- int

- long

- float

- double

For converting a larger data type to that of a smaller data type, we have to perform <u>Explicit conversion</u> so we wont lose information during the conversion we have to state explicitly type out the type inside a set of parenthesis to tell the compiler the type we will convert that variable to. In the following, we tell the compiler that we'll have to convert a <code>double</code> y to type <code>int</code>.

```java
int x = 1;
double y = x; //implicit
int z = (int) y; //explicit
```

Now suppose we do the following, what happens?

```java
int num1 = 420;
Integer num2 = num1;
int num3 = num2;
```

In Java, we dont need some type conversion when we assign a primitive type (int) variable to a non-primitive (Integer) type variable. What happened here is called <a href="https://docs.oracle.com/javase/tutorial/java/data/autoboxing.html">Autoboxing</a>, where the primitive type variable "automatically" becomes its corresponding type of non-primitive, or vice versa.

I've been looking at solutions for competition programming problems in Java and plenty of them are using Bufferedreader, as it's faster they said.

Thus, time to learn reading input with bufferedreader

```java
//importing these 3 are essential for buffered reader
import java.io.BufferedReader;
import java.io.IOException; //exception for readLine
import java.io.InputStreamReader;
//or we could just import the whole java.io package 
//import.java.io.*:

public class Test {
    public static void main(String[]args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        //reads a user's input
        String input = br.readLine();
    }
}
```

<code>System.in</code> takes an input stream of bytes from the standard input device, which is the keyboard. <code>InputStreamReader</code> converts the streams into characters. <code>BufferedReader</code> then reads these converted characters.

More info at [https://www.cs.princeton.edu/courses/archive/spr96/cs333/java/tutorial/java/nutsandbolts/input.html](https://www.cs.princeton.edu/courses/archive/spr96/cs333/java/tutorial/java/nutsandbolts/input.html)

> System.in implements the standard input stream. The standard input stream is a C library concept that has been assimilated into the Java language. Simply put, a stream is a flowing buffer of characters; the standard input stream is a stream that reads characters from the keyboard. The standard input stream is a convenient place for an old-fashioned text-based application to get input from the user.


we use <code>.readLine()</code> to read input. but as [Oracle's java docs says (I quoted below)](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/io/BufferedReader.html#readLine()), we have to handle this exception by either importing java.io.IOException and declare the method to throw an exception with <code>throws IOExceptio</code>. Or we could have a try-catch for it.

> public String readLine() throws IOException
>
>Reads a line of text. A line is considered to be terminated by any one of a line feed ('\n'), a carriage return ('\r'), a carriage return followed immediately by a line feed, or by reaching the end-of-file (EOF).
>
>Returns:
>
>A String containing the contents of the line, not including any line-termination characters, or null if the end of the stream has been reached without reading any characters
>
>Throws:
>
>IOException - If an I/O error occurs

