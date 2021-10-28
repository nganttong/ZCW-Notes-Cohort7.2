# Control Flow
* Block Scope
* Conditional Statements
* Loops
* Switch Statements

## Control Flow
* Java, like any programming language, supports both conditional statements and loops to determine control flow

## Block Scope
* Before learning about control structures, you need to know more about blocks. A block or compound statement consists of a number of Java statements, surrounded by a pair of braces. Blocks define the scope of your variables.

* Blocks can be nested, doesn't matter how many times.
* **Sidenote:** For scopes, variables declared in scopes that are nested, the variables on the outer scope are applicable inwards but not the opposite.

```java
public static void main(String[] args)
{
    int n;
    ...
    {
        int k;
        ...
    } // k is only defined up to here
}
```
* **You may not declare a variable if it exists in the outter scope.**

```java
public static void main(String[] args)
{
    int n;
    ...
    {
        int k;
        int n; // Error--can't redefine n in inner block ...
    }
}
```
## Conditional Statements
* The conditional statement in Java has the form
    * if statements can be nested within one another
    * **Side note:** open curly bracket after a condition you can read it as "then"

```java
if(condition) statement {
    statement1
    statement2
    ...
}
```
* if/else statement
    * to use else, you much have a preexisting `if` that it couples to
    

```java
if (condition) {
    statement1
}
else {
    statement2
}
```
* if/else if
    * to use if, it does not need to be coupled with an `else` clause
    * you can not say `else`, then `else if`
```java
if (condition) {
    statement1
}
else if (condition2) {
    statement2
}
else {
    statement3
}
```

* Control structure code created `branches`, or different paths that the code can take.
    * For example:

```java
if(condition) {
  // do something
} else {
  // do something else
}
```
Above has two branches. One code path when the condition succeeds and one for when it fails.

## Loops
* The while loop executes a statement (which may be a block statement) while a condition is true

```java
while(condition) statement
```
* The while loop will never execute if the condition is false at the outset

* If you want to make sure a block is executed at least once, you need to move the test to the bottom, using the do/while loop.

```java
do statement while (condition);
```

## Determinate Loops
* The for loop is a general construct to support iteration controlled by a counter or similar variable that is updated after every iteration.
* Don't use while loops with teh intent to count.. just use a determinate loop, in Intellij, the shortcut is `fori`

```java
for (int i = 1; i <= 10; i++)
    System.out.println(i);
```
## Nested Loops
* You can have loops within loops, but be aware of variable scoping:

```java
for(int i = 0; i < 5; i++) {
  for(int j = 0; j < 5; j++) {
    System.out.println(j);
  }
}
```

## Multiple Selections - The switch Statement
```java
switch (choice)
{
    case 1:
        ...
        break;
    case 2:
        ...
        break;
    case 3:
        ...
        break;
    default:
        // bad input ...
        break;
}
```

* Switch statements without breaks can have code “fall through” to the next one.

```java
switch (choice)
{
    case 1:
        ...
        // notice no break
    case 2:
        ...
        break;
    case 3:
        ...
        break;
    default:
        // bad input ...
        break;
}
```
## Case Label
* A case label can be
    * A constant expression of type char, byte, short, or int
    * An enumerated constant
    * Starting with Java SE 7, a string literal

```java
public static void nestedWhileLoop {
    outerLoop:
    while(true) {
        do {
            if(true) {
                break outerLoop;

            }
        } white(true);
    }
}
```

## Statements That Break Control Flow
* The same break statement that you use to exit a switch can also be used to break out of a loop

```java
while (years <= 100) {
    balance += payment;
    double interest = balance * interestRate / 100; balance += interest;
    if (balance >= goal) break;
    years++;
}
```
* The continue statement transfers control to the header of the innermost enclosing loop

```java
Scanner in = new Scanner(System.in);
while (sum < goal)
{
    System.out.print("Enter a number: ");
    n = in.nextInt();
    if (n < 0) continue;
    sum += n; // not executed if n < 0
}
```