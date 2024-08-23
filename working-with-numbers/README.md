<h1>
  <span class="headline">Java Data Types and Variables</span>
  <span class="subhead">Working With Numbers</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to differentiate decimal and integer numbers and carry out special operations on numbers using the `Math` class.

<div class="timed-section">
  <h2>Decimals and integers</h2>
  <span class="minutes">10 min</span>
</div>

Let's talk about numeric data types. I'll write some code, but before I run it, we'll discuss what we expect the output to be and why. I'll run the code, and then we can discuss the results. Let's start!

What do you expect to be printed to the console?

```java
int num1 = 5;
System.out.println(num1);
```

How about here?

```java
int num2 = 5 / 2;
System.out.println(num2);
```

Why did we get the result we did? Remember that different types of numbers are strictly typed. As demonstrated in the previous function, because an `int` stores an integer, not a decimal, `num2` can only ever hold a whole number.

So, what data type would we use to assign a variable to a decimal?

How about `float`?

```java
float num3 = 5 / 2;
System.out.println(num3);
```

Because `5` and `2` are automatically assigned the `int` data type, the result is also the `int` type after the calculation. To get the answer we're looking for, both the dividend and divisor must be a decimal type, not an integer type:

```java
float num4 = 5f / 2f;
System.out.println(num4);
```

```java
double num5 = 5d / 2d;
System.out.println(num5);
```

In the previous examples, we used a `float` and a `double` data type to save decimal numbers and got the same result.

<div class="activity knowledge-check">
  <h2 class="title"><code>float</code> vs. <code>double</code></h2>
  <span class="minutes"></span>
</div>

What is the difference between `float` and `double`, and when should we use each?

### Numeric data types and bits

To answer that question, it may be helpful to understand that a data type defines not only the type of data but also the methods that can be used to manipulate that data. **Primitive** data types in Java also have a certain preassigned size in memory. This is represented in a number of bits:

| Name     | Width in Bits | Range                |
|----------|---------------|----------------------|
| `float`  | 32            | 3.4e–038 to 3.4e+038 |
| `double` | 64            | 1.7e–308 to 1.7e+308 |

More memory consumed by a data type means more information can fit into a variable. A `double` data type is much larger than a `float` data type.

What does that mean when working with decimals? In short, `float` data types are more memory efficient, while `double` provides more accuracy. The data needs of many modern applications will call for the accuracy of `double` over the relatively slight performance improvements of a `float`.

<blockquote class="warning">
  🚨 Never use the <code>float</code> or <code>double</code> data types to work with numbers that require a high degree of precision, such as currency calculations. The <code>BigDecimal</code> class is better suited for these tasks.
</blockquote>

The same data type differentiation exists in integers between `byte`, `short`, `int`, and `long`:

| Name    | Width in Bits | Range                                   |
|---------|---------------|-----------------------------------------|
| `byte`  | 8             | -128 to 127                             |
| `short` | 16            | -32,768 to 32,767                       |
| `int`   | 32            | -(2^31) to (2^31)-1 (approx. 2 billion) |
| `long`  | 64            | -(2^63) to (2^63)-1                     |

`int` will cover almost all of your integer needs.

<div class="activity knowledge-check">
  <h2 class="title">Common numeric data types</h2>
  <span class="minutes"></span>
</div>

What's the most common data type for decimals? What's the most common data type for integers?

## Standard arithmetic operators

Now that we understand more about the numeric data types let's look at what we can do with them.

Here are the standard arithmetic operators (those you've been learning since grade school):

``` java
System.out.println(2 + 2);
System.out.println(2 - 2);
System.out.println(2 / 2);
System.out.println(2 * 2);
System.out.println(2 % 2); // What does this do?
```

<div class="timed-section">
  <h2>Special number operators</h2>
  <span class="minutes">5 min</span>
</div>

Programming languages can be limiting in terms of the number of operations they allow you to perform. For example, how do you square or cube a number?

Java provides a special `Math` object with some useful methods.

Taking a number to a power? Use `Math.pow(num1,num2)`:

```java
// 3^2 becomes
System.out.println( Math.pow(3,2) );
// Prints: 9
```

Taking a square root? Use `Math.sqrt(num1)`:

```java
// √(4) becomes
System.out.println( Math.sqrt(4) );
// Prints: 2
```

### `NaN`

Be careful not to produce non-real or imaginary numbers when carrying out arithmetic, for example:

```java
System.out.println( Math.sqrt(-2) );
// Prints: NaN 
// (there is no square root of negative numbers)
System.out.println(5 / 0);
// Prints: NaN
// (any number divided by 0 is undefined)
```

`NaN` is toxic, and if a calculation is attempted on that variable or a method called subsequently, your program will break.

Use `isNaN()` to test for `NaN`. Do not use `NaN == NaN` - this will always be false.

### Random Numbers

Need a random number? Use `Math.random()`. It returns a positive double greater than or equal to 0.0 and less than 1.0.

```java
System.out.println( Math.random() );
=> ? // A double greater than or equal to 0.0 and less than 1.0

// To get a number within a range
int max = 10;
int min = 1;
int range = Math.abs(max - min);

// Returns a random number between 1 and 10.
System.out.println( (Math.random() * range) + min);
```

Getting a random number might feel cumbersome, but this is a solved problem that you can always find a solution for online - look up this code when you need it!

<blockquote class="warning">
  🚨 Never use <code>Math.random()</code> to generate numbers for processes that should be cryptographically secure. While the numbers it generate may appear random, they will follow a set pattern which compromises their security.
</blockquote>

<div class="activity knowledge-check">
  <h2 class="title">Where does <code>Math</code> come from?</h2>
  <span class="minutes">5 min</span>
</div>

Who provides the `Math` object? Where do you think you might be able to find more information? ([Oracle Math Documentation](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/Math.html)).
