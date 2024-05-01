# ![[tktk Module Name] - tktk Microlesson Name](./assets/using-special-number-operators.png)

**Learning objective:** By the end of this lesson, students will be able to examine how class methods can manipulate data in the `Math` class. 

## Demo: Let's Start With Numbers (15 min)

#### Decimals vs. Integers

<!-- **Instructor Note**: As you code the following examples, ask the students the questions below. If they guess correctly, ask them to explain why.-->

First off, let's talk about numeric data types.

What do you expect to be printed to the console?

```java
int num1 = 5;
System.out.println(num1);
=> 5
```

How about here?

```java
int num2 = 5 / 2;
System.out.println(num2);
=> 2
```

But why is `num2` not 2.5? In low-level languages (unlike JavaScript, Ruby, or PHP), numbers are strictly typed, and a type is either an integer or a decimal. An `int` stores an integer, not a decimal, as demonstrated in the previous function.

So, what data type would we use if we wanted to assign a variable to a decimal?

How about `float`?

```java
float num3 = 5 / 2;
System.out.println(num3);
=> 2
```

> **Knowledge Check**: That didn't work quite as expected. Can anyone guess why?

Because both `5` and `2` are automatically assigned the `int` data type, when the calculation is done, the answer is also an `int`. We must tell the computer that both the dividend and divisor are of a decimal type, not an integer type:

```java
float num4 = 5f / 2f;
System.out.println(num4);
=> 2.5
```

```java
double num5 = 5d / 2d;
System.out.println(num5);
=> 2.5
```

Note: In the previous example, we used both a `float` and a `double` data type to save decimal numbers.

> **Knowledge Check**: What is the difference between `float` and `double`, and when should we use each one?

#### Numeric Data Types and Bits

To answer the previous question, it's helpful to understand that a data type defines not only the type of data, but also the methods that can be used to manipulate that data. **Primitive** data types in Java also have a certain preassigned size in memory. This is represented in a number of bits:

| Name  | Width in Bits | Range    |
|-------|---------------|----------|
| `float`   | 32          | 3.4e–038 to 3.4e+038 |
| `double`  | 64          | 1.7e–308 to 1.7e+308 |

More memory means more information can fit into a variable. A `double` data type is much larger than a `float` data type.

What does that mean for working with decimals? `float` data types are more memory efficient, while `double` provides more accuracy (it's recommended for currency).

There's also a `BigDecimal` class, which is used when even more decimal points are needed.

The same data type differentiation exists in integers, between `short`, `int`, and `long`:

| Name  | Width in Bits | Range    |
|-------|---------------|----------|
| `short` | 16           | -32,768 to 32,767                  |
| `int`   | 32           | -(2^31) to (2^31)-1 (approx. 2 billion) |
| `long`  | 64           | -(2^63) to (2^63)-1                    |

`int` will cover almost all of your integer needs.

> **Knowledge Check**: What's the most common data type for decimals? What's the most common data type for integers?

#### Using Standard Arithmetic Operators

Now that we understand a bit more about the numeric data types, let's look at what we can do with them.

Here are the standard arithmetic operators (those you've been learning since grade school):

<!-- **Instructor Note**: Depending on time and student understanding, this can be breezed over (it will have been covered during the JS unit). Be sure to mention modulo, as it's an odd one. When going through each example, ask students to calculate what will be printed to the console.-->

``` java
System.out.println(2 + 2);
System.out.println(2 - 2);
System.out.println(2 / 2);
System.out.println(2 * 2);
System.out.println(2 % 2); // What does this do?
```

----

## Demo: Using Special Number Operators (10 min)

Coding languages can at times be limiting in terms of the number of operations they allow you to perform. For example, how do you square or cube a number?

Java provides a special `Math` object with some useful methods.

Taking a number to a power? Use `Math.pow(num1,num2)`:

``` java
// 3^2 becomes
System.out.println( Math.pow(3,2) );
=> 9
```

Taking a square root? Use `Math.sqrt(num1)`:

``` java
// √(4) becomes
Math.sqrt(4);
=> 2
```

Need a random number? Use `Math.random()`:

``` java
// Returns double value with positive sign greater than or equal to 0.0 and less than 1.0.
Math.random()
=> ?
// Returns random number in range.
int range = Math.abs(max - min) + 1;
(Math.random() * range) + min;
```

> **Knowledge Check**: Who provides the `Math` object? Where do you think you might be able to find more information? ([Oracle Math Documentation](https://docs.oracle.com/javase/7/docs/api/java/lang/Math.html)).

_Created by Kristen Tonga_