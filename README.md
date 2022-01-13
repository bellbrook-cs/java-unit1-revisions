# Lesson 1-3 Revisions

## Problem Statement

We are going back to the beginning to review code from lessons 1-3. Please use the 4 day weekend to review, and figure out and master the content from these 3 lessons.

There are 4 parts to this assignment, parts 1-3 correspond to lessons 1-3. However part 4 is an actual task you should be able to figure out. You need to submit this after completing part 4.

Use your best judgement in deciding whether or not to complete parts 1-3. You know better than anyone else what you are struggling with.

### Part 1

Modify your program to match the following code snippet:

```java
public class Main {
   public static void main(String[] args) {
      System.out.println("Hello World!");
   }
}
```

notice that when you run it you see the following:

```
Hello World!
```

The output of your program is not in quotes, however the **string literal** you typed in your code is in quotes.

The portion of your code that says `System.out.println` is the method that you are calling, it is like a command for the computer.

The parentheses are required to call a method, they contain **parameters** that can change how our method acts. In this case what gets printed to the console.

Some methods allow you to leave the parentheses empty, if you leave the `System.out.println` parentheses empty a blank line will be printed.

The quotes contain a **string literal**, we have now discussed **string variables** in class, **literals** are the actual literal value in your code. **variables** are like nicknames for values, the value they correspond to can change throughout your program.

Try making the following changes to our code:

```java
public class Main {
   public static void main(String[] args) {
      System.out.print("Hello!")
      System.out.println("Hello again!");
      System.out.println("Goodbye!");
   }
}
```

When you run this, you should see the following:

```
Hello!Hello again!
Goodbye!
```

Think about the difference between `System.out.println` and `System.out.print`, what is different about the lines of code you wrote? and what is different about the display?

`System.out.print` will not add a newline after it prints it's **parameter**.

- `System.out.println` is like asking the computer to type something and then hit the enter key.
- `System.out.print` is like asking the computer to type something and move on, the cursor stays on the same line.

### Part 2

There are 3 different types of variables introduced in this lesson:

- String
- int
- double

The capitalization does matter, and you need to notice that only `String` starts with a capital letter.

This is because `int` and `double` are what's called **primitive types** and `String` is an **object**.

Try looking at, and running the following code snippets:

```java
String s = "Hello cruel world";
System.out.println(s);
```

```java
int age = 59;
System.out.println(age);
```

```java
double d = -137.8036;
System.out.println(d);

d = 1.547776E23;
System.out.println(d);
```

looking at the lines above you should notice a patter like this:

```
{variable type} {variable name} = {literal value};
```

this is what it looks like to **declare** and **initialize** a variable.

you can write the following code as well:

```java
String s;
```

which only **declares** a variable s.

looking at the sample code snippets you should see the line:

```java
d = 1.547776E23;
```

This is what it looks like to **initialize** but not **declare** the variable.

You will also need to notice the special syntax containing the letter `E` (can also be a lowercase `e`). This means it is in scientic notation. This is a **double literal** that is equal to the number to the left of `E` multiplied by 10 to the power of the number to the right of `E`. In this case 1.547776 * 10^23.

It is important to note that you cannot use `^` to do exponentiation in java, if you try it will compile, however you will see an unexpected answer.

try the following:

```
System.out.println(10^6);
```

intuitively you may think it should be `1000000` however, we see this instead: `12`

This is because `^` means XOR in java, which is not an operation you need to worry about for the time being.

### Part 3

This section is mostly about manipulating strings. The first thing you should pay special attention to in the chapter is what an **index** is. Each character in a `String` has an **index** or location. **indexing starts at 0 in java**

```
"Hopper Gee"
 0123456789
```

In the above example you should notice that the first character `'H'` is at index 0, and the space also counts as a character in counting the index.

When you are printing things in java, you may notice more complicated print statements appearing in this lesson. You can print just about anything inside a `System.out.println` statement. **However** you can only print 1 thing in each statement.

The following works because you are **concatenating** the strings together. This combines the two Strings into 1 string that gets printed:

```java
String s1 = "Hello";
String s2 = "There";
System.out.println(s1 + s2);
```

The following also combines the **variables** with a **literal** to make the output more readable.

```java
String s1 = "Hello";
String s2 = "There";
System.out.println(s1 + " " + s2);
```

Try running the above snippets as well so you understand the difference in output.

`substring` was a tricky method that many seemed to struggle with. Given the following `String` as an example.

```java
String s = "The quick brown fox jumps over the lazy dog";
```

we can perform some examples.

```java
String s = "The quick brown fox jumps over the lazy dog";
System.out.println(s.substring(5)); // prints: uick brown fox jumps over the lazy dog
```

`substring` is called on a specific string like this: `{String variable}.substring({paramters});`, you need a specific string **variable** or **literal** to call the **method** on.

in this case the **parameter** is 5. this means the **method** **returns** a new string containing the same characters as the string `s` starting at and including the 5th indexed character. 

We can use 2 parameters in a substring as well:

```java
String s = "The quick brown fox jumps over the lazy dog";
System.out.println(s.substring(5,11)); // prints: uick b
```

In this case the **parameters** are 5 and 11. This means get the characters starting at and including the 5th indexed character up to but not including the 11th indexed character.

There was not as much confusion surrounding the other concepts in this lesson, but I encourage you to run all the code snippets in lesson 3 and examine the output yourself.

### Part 4

Read through the code provided. There are sections marked that you should not modify, and sections marked that you are allowed to modify. Please only modify the specified sections to complete this assignment.

Your goal is to get the output of the program to match the expected output below.

There are certain restrictions that go along with each line of output, so read very carefully.

#### Starter code

this is the starter code you should copy into your Main.java file:

```java
/*
 * Program Title: 
 * Author: 
 * Date:
 * Purpose: 
 */

public class Main {
  public static void main(String[] args) {

    /* DO NOT MODIFY THE FOLLOWING LINES */

    int num1 = 1;
    int num2 = 2;
    double num3;
    double num4 = 10.0;
    String s1 = "The quick brown fox jumps over the lazy dog";
    String s2 = "Hello world";
    String s3;

    /* ONLY MODIFY THE FOLLOWING LINES */

    // You may not use any string literals in your solution to `output1`
    String output1 = s1;

    // You may not use any string literals in your solution to `output2`
    String output2 = s2;

    // Please modify this line without restriction
    s3 = "";

    // Please modify this line without restriction
    num4 = 1;

    // You may not use any string literals in your solution to `output3`
    String output3 = s2;

    // Please modify this line to not use any numeric literals or variables.
    int output4 = num1;

    // Please modify the following lines without restriction
    num1 = 0;
    num2 = 1;

    /* DO NOT MODIFY THE FOLLOWING LINES */

    System.out.println(output1);

    System.out.println(output2 + output3);

    System.out.println(output2 + s3);

    System.out.println(num4);

    System.out.println("The length of \"" + s3 + "\" is " + output4);

    System.out.println(output1.substring(num1, num2));
  }
}
```

#### Expected Output

```
THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG
Hello fox
Hello john
197620.5
The length of "john" is 4
BROWN
```

## Submission

Please submit the following to google classroom:

1. `Main.java`
    * Hover over `Main.java`.
    * Click the three dots to the right of the file name.
    * Click `Download`.
    * Upload the downloaded file to google classroom.
2. A link to your replit project
