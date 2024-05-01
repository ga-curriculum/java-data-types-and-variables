# ![[tktk Module Name] - tktk Microlesson Name](./assets/primitives-vs-objectes.png)

**Learning objective:** By the end of this lesson, students will be able to examine how to call methods on a variable with a `String` data type. 

## Introduction: Primitives vs. Objects (10 min)

Before we get into `String`s, let's take a step back. Have you noticed that all of the data types we've used so far begin with a lowercase letter? What about the `String` data type? Did you pick up that it begins with a capital letter?

This is a naming convention used to distinguish between primitive and object data types. Primitive types always start with a lowercase letter (e.g., `int`, `double`, `boolean`), while objects start with an uppercase letter (e.g., `String`, `Integer`).

**Primitive data types** are **pass by value**. Using a primitive as a parameter is like writing a number on a Post-it note and handing it off. `int a = 1;` is a **copy** of the numeric data, not a reference to where the data is stored.

**Object data types** contain attributes and methods and start with a capital letter. These are **pass by reference**.

In other words, using an object is like using a Dewey Decimal System in the library. A variable assigned to an object is given a number that references where a book can be found in the computer's library but is not a copy of the book itself. `Person a = new Person(Nancy, Drew);` is a reference to the data object that contains all information and methods in the class of that object.

#### Java Naming Convention Tips

Classes and objects should start with a capital letter (e.g., `String`, `Integer`), primitives always start with a lowercase letter (e.g., `int`, `boolean`), variables and method names start with a lowercase letter (e.g., `main()`), and multi-word names are camel case (e.g., `vannaWhite`). Class constants (i.e., `final` instance and static variables) are generally all capitalized with words separated by underscores (e.g., `private final Object MY_MUTEX`).

> **Discuss with the person next to you**: What does a primitive contain? What does an object contain? What's one easy way to tell the difference between an object and a primitive data type? Be ready to share your answers.

#### Words: `char` and `String`

With that basic introduction to primitives and objects, let's talk about words:

* A `char` is a primitive data type. What's an example of a `char`?

* A `String` begins with a capital letter because a `String` is an object.

> **Discuss with the person next to you**: What's an object? Be ready to share your answer.

`String`s are collections of letters and symbols known as **characters**, and we use them to deal with words and text.

A `String` is actually an array of `char` data:

``` java
String str = "abc";
// is actually
char data[] = {'a', 'b', 'c'};
```

-----

## Demo: Creating a New `String` (15 min)

`String`s are a special type of object.

Try this with me. You can instantiate (or create an instance) of a `String` like this:

``` java
// Variable can be assigned like a primitive
String a = "I'm a string.";
```

This is short for:

``` java
// Variable assigned like an object
String a = new String("I'm a string too!");
```

#### `String` Helper Methods

Because a `String` is an object, it has predefined methods we can use.

To find the length of a `String`, use its `length` property:

```java
"hello".length();
=> 5
```

To get the first letter of a `String`:

```java
"hello".charAt(0);
=> "h"
```

To replace part of a `String`:

```java
"hello world".replace("hello", "goodbye");
=> "goodbye world"
```

To make a `String` uppercase:

```java
"hello".toUpperCase();
=> "HELLO"
```

To add two `String`s together:

```java
"hello".concat(" world");
=> "hello world"
```

Or, to concatenate (add together) using `+`:

```java
String twoStringsTogether = "Hello" + " World";
=> "Hello World"
```

##### A Special Note on Equality Among `String`s

What if you want to compare two `String`s?

```java
String blue = "blue";
boolean withSign = (blue == "blue");            //=> true
boolean withWords = (blue).equals("blue");      //=> true
```

Do you know which one of these would be preferred? Let's walk through another example to show you which and why:

```java
String blue = "blue";
String bl = "bl";
String ue = "ue";
System.out.println(bl+ue);                      //=> blue
boolean withSigns = (bl+ue == blue);            //=> false
boolean withWords = (bl+ue).equals(blue);       //=> true
```

Why isn't `withSigns` `true` when the output looks the same? Remember, `String` is actually an object, and objects are **passed by reference.**

`==` compares the place where the object was stored on the computer to see whether or not they're the same. `String blue` contains a reference to where it's stored on the computer, and that's different from where `String bl` is stored. `equals()`, on the other hand, is a method that can be called on an instance of a `String` object and compares whether or not the `char` arrays in each `String` are the same, not whether or not the references are the same.

In short, use `equals` when comparing `String`s.

> **Knowledge Check**: Why can we call methods on a variable with a `String` data type but not on an `int`?

_Created by Kristen Tonga_