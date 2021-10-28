## Reviewing 'Fundamental Programming Structures in Java' from lecture 102621
* Class names and the file name NEED to follow same case upper/lower
    * One and top most class shares name of file
* Space and indentation doesn't matter in Java, but pay attention to formatting

```java
public class ClassName {
    public static void main(String[] args) {
        program statements
    }
}
``` 
* Class defines all Java code, and `main` is just a special method.
* You can have multiple mains, just depends on ordering when called on.

    * Static methods are kind of class methods
    * Instance methods are things that we write
* Don't forget everytime you change your java code, you need to compile it.

* We want to use comments when we are fleshing out the code
    * Comments
        1. `//` for single line comment
        2. `/*` and `*/` for multiline comments
        3. using `/**` to start and `*/` to end will be used to generate documentation automatically

* **You CAN NOT nest `/* */` comments in Java**

### Data Types
* Java is a strongly declared typed language and every veriable must have a declared type.

* There are 8 primitive types in Java
    1. int
    2. short
    3. long
    4. byte
    5. float
    6. double
    7. char
    8. boolean
        * these are data types  

!!Declaration is **VERY** important idea!!

Know the diff between declaring a variable, initializing it, and using it.

* You can in fact declare multiple variables in a line.

```java
    int i, j; // both are integers
```

**PLEASE** initialize your variables
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

  ## Constants are really important
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
* Denoted by `final`

-- These notes are not on the full lecture.



Watch Redux video [Here](https://drive.google.com/file/d/1T9Hrluz23WVggsZkCkMyawJe3FqZWtFb/view?usp=sharing)