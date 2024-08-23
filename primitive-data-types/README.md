<h1>
  <span class="headline">Java Data Types and Variables</span>
  <span class="subhead">Primitive Data Types</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to apply Java's primitive data types and recognize their literal representations.

<div class="timed-section">
  <h2>What is a data type?</h2>
  <span class="minutes">5 min</span>
</div>

In Java, data is stored in variables so that we can access and manipulate that data throughout our apps. Each variable has a data type associated with it, and the variable can only hold that type of data.

When we create variables, we must assign the variable a data type. The data type of that variable cannot be changed from that point.

> 🧠 These qualities mean that Java is designed to enforce type safety. People also describe Java as statically typed - meaning that once a variable is assigned a data type, the type cannot change.

Throughout this lesson, we'll explore how data types and variables form the basic building blocks of programming a Java application and how we use them to store information in our programs.

<div class="timed-section">
  <h2>Primitive data types in Java</h2>
  <span class="minutes">10 min</span>
</div>

In computer science and computer programming, a data type — or simply, type — is a classification identifying one of the various types of data that determines:

- The possible values for that type.
- The operations that can be done on values of that type.
- The meaning of the data.
- The way values of that type can be stored.

Data types are often similar across different languages, including English. Java has eight primitive data types, all described below. We'll start with the most common, then briefly touch on some less common ones.

| Category       | Data type | Description                                                                               | Example                                |
| -------------- | --------- | ----------------------------------------------------------------------------------------- | -------------------------------------- |
| True or False  | `boolean` | Represents either true or false.                                                          | `true`, `false`                        |
| Integer        | `int`     | Whole numbers ranging from -2,147,483,648 to 2,147,483,647.                               | `-9000`,  `1024`, `1_000_000`          |
| Floating-point | `double`  | Positive or negative decimal numbers with about 16 digits of precision after the decimal. | `3.14159265359`, `1.0`, `-98.9`, `56D` |

By default, an integer literal will be of type `int`, and a floating-point literal will be of type `double`. You can also specify a number as a `double` by adding a `d` or `D` to the end of it.

Numeric literals can optionally include underscores to make large numbers easier to read. For example, the int `1_000_000` above will be interpreted as `1000000`. The underscores purely make the literal more readable. There are a few rules for using this pattern. For example, never start or end a number with `_`.

The following primitives are less common but do have use cases:

| Category       | Data type | Description                                                                              | Example                             |
| -------------- | --------- | ---------------------------------------------------------------------------------------- | ----------------------------------- |
| Integer        | `byte`    | Whole numbers ranging from -128 to 127.                                                  | `4`, `8`, `15`, `16`, `42`          |
| Integer        | `short`   | Whole numbers ranging from -32,768 to 32,767.                                            | `-20`, `9001`, `16384`              |
| Integer        | `long`    | Whole numbers ranging from ~-9 quintillion to ~9 quintillion.                            | `9_223_372_036_854_775_807L`, `16L` |
| Floating-point | `float`   | Positive or negative decimal numbers with about 7 digits of precision after the decimal. | `3.14159F`, `1.0F`, `-80.80F`       |
| Character      | `char`    | A single character surrounded by single quotation marks. The building block of strings.  | `'a'`, `'A'`, `'7'`, `'@'`          |

The `byte`, `short`, and `float` types can be useful in memory-constrained environments. Floating-point literals that end in an `f` or `F` will be of type `float`.

The `long` type can represent a larger range of numbers than the `int` data type. Integer literals that end in an `l` or `L` will be of type `long`.  When implementing these, the capital `L` is preferred over `l` because of how similar `l` can look to the `1` digit.

The `float` type implements the [single-precision 32-bit IEEE 754 floating point format](https://en.wikipedia.org/wiki/Single-precision_floating-point_format) standard, and the `double` type implements the [double-precision 64-bit IEEE 754 floating point format](https://en.wikipedia.org/wiki/Double-precision_floating-point_format) standard.

The IEEE 754 standard is complex, and its intricacies are largely out of the scope of this lecture. That said, we will scratch the surface as we explore these data types more.

It is important to know that you should not use `float` or `double` data types to represent floating-point numbers where exact precision is required, such as currency calculations.

As we continue through this lesson we'll elaborate on the types above and show you some helper methods to manipulate them.

<div class="activity knowledge-check">
  <h2 class="title">Video game data</h2>
  <span class="minutes">5 min</span>
</div>

Let's go around the room and come up with a few examples of data for a video game. Predict what type each piece of data would be.
