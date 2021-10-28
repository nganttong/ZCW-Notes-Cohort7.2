# Fundamental Programming Structures in Java
* A simple Java Program

    ```java
    public class FirstSample {
        public static void main(String[] args) {
            System.out.println("We will not use 'Hello, World!'");
        }
    }
    ```
* 2 scopes here, class scope and method scope. 
    * Methods are `MEMBERS` of the class. 

* Nullary Method
    *   A method that takes no arguments

* Java is case sensitive
* Class names must begin with a letter, and after that, they can have any combination of letters, digits, and underscores.
* If you put anything other than a LETTER or a reserved word at the beginning of your class name, it will fail to compile.
* You need to make the name for the source the SAME as the name for the public class.
* Whitespace is irrelevant to the Java compiler
* Any scope is going to be named after what it is the scope of (about equiv. of context)
* If you do not type "public" before class, it maeans it is package protected, means things with the same package have access to this

```java
public class ClassName {
    public static void main(String[] args) {
        program statements
    }
}
``` 

* A Class defines all of Java code
* In Java, (pretty much) everything is an Object
* `main` is merely a special method (a function defined in a class) that is exxecuted when the program runs
* `main` doesn't return anything, thus the `void` return keyword
* `main` doesnt operate on an object, thus the `static` keyword
    * `static` means occuring or existing independant of the state of an object

## Object Stuff
* Since almost everything in Java is an object, remeber that:
    * Static Methods are called on a `Class`, not on objects themselves
        * `SomeObject.someMethod()`
    * Instance methis are called on instances of the objects

    ```java
    SomeObject so = new SomeObject();
    so.someInstanceMethod();
    ```
 * Note the construction of `so`

* Methods are functions defined in the contect of a class (side note: it's similar to a function on js)
    * Java does not support functions because they are independant in the existance of an object, we use methods because they are within the scope of a Class

## Java Environment
* Codeis compiled with `javac`
* `javac Example.java`
* Code is compiled to a thing called bytecode and saved in class files
* The bytecode is then run in the JVM (Java Virtual Machine) 
    * This means that the bytecode can be run on any machine that has the JVM
* `java Example`
    * just `java` and the name of the file i.e. `Example`

### Comments
1. `//` for single line comment
2. `/*` and `*/` for multiline comments
3. using `/**` to start and `*/` to end will be used to generate documentation automatically

```java
/**
 * This is the first sample program in Core Java Chapter 3
 * @version 1.01 1997-03-22
 * @author Gary Cornell
 */
public class FirstSample {
    public static void main(String[] args) {
        System.out.println("We will not use 'Hello, World!'");
    }
}
```

* CAUTION: `/* */` does not nest in Java.

## Data Types
* Java is a strongly typed language in every variable must have a declared type.

### Define these Important words
* Declaration -- (from google) In computer programming, a declaration is a language construct that specifies properties of an identifier: it declares what a word (identifier) "means". ... Java uses the term "declaration", though Java does not require separate declarations and definitions.
* Initialization -- (from google) Initialization: Initialization is when we put a value in a variable, this happens while we declare a variable. Example: int x = 7; , String myName = "Emi"; , Boolean myCondition = false; Assignment: Assignment is when we already declared or initialized a variable, and we are changing the value.
* Assignment -- (from google) Assignment in Java is the process of giving a value to a primitive-type variable or giving an object reference to an object-type variable. The equals sign acts as assignment operator in Java, followed by the value to assign.

## There are 8 primitive types in Java
1. int
2. short
3. long
4. byte
5. float
6. double
7. char
8. boolean
* these are data types

### Integer Types
* The integer types are for numbers without fractional part
![](https://i.gyazo.com/cb4ffb8c1cd6c1d5004ac48597d0ad12.png)

### Floating-Point Types
* The floatinf-point tpyes denote numbers with fractinal parts 
![](https://i.gyazo.com/14d2b949879cd04fe46ab92298c00b39.png)

Due to repeating decimals and the amount of significant digits in floating point types you can get incorrect values due to roundoff error. For example ` 2.0 - 1.1` does not return `0.9`. It returns `0.8999999999`

### The Char Type
* Literal values of type of char are enclosed in single quotes
* Values of type char can be expressed as hexadecimal values that run from \u0000 to \uFFFF

![](https://i.gyazo.com/bca9a1067c7ff33b7392079e67cc9ee3.png)

### The Boolean Type
* The boolean type has two values, false and true.

### BIG NUMBERS
* If the precision of the basic integer and floating-point types is not sufficient, you can turn to a couple of handy classes in the java.math package: BigInteger and BigDecimal.

```java
BigInteger a = BigInteger.valueOf(100);
```
* you cannot use the familiar mathematical operators such as + and * to combine big numbers

```
BigInteger c = a.add(b); // c = a + b
BigInteger d = c.multiply(b.add(BigInteger.valueOf(2))); // d = c * (b + 2)
```

### Variables
* In Java, every variable has a type. You declare a variable by placing the type first, followed by the name of the variable. 

```
double salary;
int vacationDays;
long earthPopulation;
boolean done;
```
* Must have a semicolon because a declaration is a cmplete Java Statement

* You can declare multiple variables on a single line:

```java
    int i, j; // both are integers
```
### Initializing Variables

* After you declare a variable, you must explicitly initialize it by means of an assignment statement you can never use the value of an uninitialized variable.

```java
int vacationDays;
System.out.println(vacationDays); // ERROR--variable not initialized
```

```java
int vacationDays;
vacationDays = 12;
```

*You can both declare and initialize a variable all on the same line, for example:

  ```java
  int vacationDays = 12;
  ```

 ### Constants
 * The Keyword final indicates that you can assign to the variable ONCE, and then its value is set once and for all. Also known as a constant.
  
  ```java
 public class Constants {
    public static void main(String[] args) {
        final double CM_PER_INCH = 2.54;
        double paperWidth = 8.5;
        double paperHeight = 11;
				System.out.println("Paper size in centimeters: "
          + paperWidth * CM_PER_INCH + " by " + paperHeight * CM_PER_INCH);
    }
}
```

  * Its probably more in common in Java to create a constant so that its available to multiple methods inside a single class. These are usually called class constants
  
  ```java
  public class Constants2 {
    public static final double CM_PER_INCH = 2.54;

    public static void main(String[] args) {
        double paperWidth = 8.5;
        double paperHeight = 11; System.out.println("Paper size in centimeters: "
            + paperWidth * CM_PER_INCH + " by " + paperHeight * CM_PER_INCH);
    }
}
```

  ### Operator
  * The usual arithmatic operators
  ![](https://i.gyazo.com/08422109e1ac4354e5ab1ae5248fd72f.png)

  * The / operator denotes integer division if both arguments are integers, and floating point division otherwise

  ### Mathematical Methods and Constants
  * The Math class contains in an assortment of mathematical funtios that you may occasionally need
 ```java
 double x = 4;
double y = Math.sqrt(x);
System.out.println(y); // prints 2.0

double y = Math.pow(x, a);
```

* The Math class supplies the usual trigonometric functions:
    * Math.sin
    * Math.cos
    * Math.tan
    * Math.atan
    * Math.atan2

  ### Converstions Between Numeric Types
  * 19 Specific conversions on primitive types are called the widening primitive conversions:
    * byte to short, int, long, float, or double
    * short to int, long, float, or double
    * char to int, long, float, or double
    * int to long, float, or double
    * long to float or double
    * float to double

**Sidenote:** Pretty much in easy terms, you can put little things into a bigger one, bu tnot vice versa. <-- Also know as widening.

* A Widening primitive conversion does not lose information about the overall magnitude of numeric value.

```java
int n = 123456789;
float f = n; // f is 1.23456792E8
```

### Casts
* Then two values are combined with the binary operator (such as n + f where n is an integer and f is a floating-pont value), both operands are converted to a common type befre the operation is carried out.
    * If either of the operands is of type double, the other one will be converted to a double.
    * Otherwise else, if either of the operands is of type float, the other one will be converted to a float.
    * Otherwise else, if either of the operands is of type long, the other one will be converted to a long.
    * Otherwise, both operands will be converted to an int.

* Converstions in which loss of information is possible (will cut off digits, see code block 2) are done by means of casts

```java
double x = 9.997;
int nx = (int) x;
```
```java
double x = 9.997;
int nx = (int) Math.round(x);
```


### Conbining Assignment With Operators
* `x+=4` is equivalent to ` x = x + 4;`

### Increment and Decrement Operator
* n++ adds 1 to the current value of the variable n, and n– subtracts 1 from it

```java
int n = 12; n++;
```
```java
int m = 7;
int n = 7;

int a = 2 * ++m; // now a is 16, m is 8
int b = 2 * n++; // now b is 14, n is 8
```
**Note** about above code block-- do not use '++m' always use 'm++' Just always have variable then operator sign.

### Relational and Boolean Operators
* To test for equality, use a double equal sign, ==.
```java
3==7 // is false.
```
**single = is already used for assignment**

* Use a != for inequality.
```java
3!=7 // is true.
```
![](https://i.gyazo.com/12208709f24cadd1dcd889da39f52734.png)

* `=` is always 2nd when doing relation operators i.e >= or <=

```java
Java uses && for the logical “and” operator and || for the logical “or” operator.
``` 
* The exclamation point ! is the logical negation operator.

```java
The && and || operators are evaluated in “short circuit” fashion
```
* The second argument is not evaluated if the first argument already determines the value

```java
expression1 && expression2
```
```java
x != 0 && 1 / x > x + y //no division by 0
```
* The value of expression1 || expression2 is automatically true if the first expression is true, without evaluating the second expression.

### Ternary Operators
* Java supports the ternary ?: operator

* Ternary Operators are equivalent to `if else` statements

```java
condition ? expression1 : expression2
```

```java
x < y ? x : y //gives the smaller of x and y
```

** Sidenote:** "If x is less than y then x returns y" is how the above clode black is said.

### Bitwuse Operators

```java
& (“and”)	(“or”) ^ (“xor”) ~ (“not”)
```
```java
>> and « operators which shift a bit pattern to the right or left.

>>> operator fills the top bits with zero, unlike » which extends the sign bit into the top bits. There is no «< operator.
```

### Parentheses and Operator Hierarchy

```java
a && b || c
```
means
```java
(a && b) || c
```
Since += associates right to left, the expression
```java
a += b += c
```
means
```java
a += (b += c)
```

 ### Enumerated Types
 
 * You can define your own enumerated type

 ```java
 enum Size { SMALL, MEDIUM, LARGE, EXTRA_LARGE };
 ```
 * Now you can declare variables of this type:
 ```java
 Size s = Size.MEDIUM;
 ```