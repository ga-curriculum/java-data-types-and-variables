<h1>
  <span class="headline">Java Data Types and Variables</span>
  <span class="subhead">The <code>String</code> Data Type</span>
</h1>

**Learning objective**: By the end of this lesson, students will be able to employ the String data type effectively in Java, leveraging its unique behaviors to solve common programming challenges.

<div class="activity guided-walkthrough">
  <h2 class="title">Creating and working with the <code>String</code> type</h2>
  <span class="minutes">15 min</span>
</div>

The `String` type is unique for a few reasons. The first of these is that it's one of the few object types with a literal representation: letters surrounded by double quotes - `"This is a string!"`.

<blockquote class="knowledge-check">
  ❓ How is this different from the <code>char</code> data type?
</blockquote>

What this means is that you can instantiate (create an instance) of a `String` like this:

```java
/* 
  String variables can be created with the same syntax
  we use to create primitive variables
*/
String myStr = "I'm a string.";
```

This contrasts with how the data for many other object data types is typically created - by using the `new` keyword to instantiate a new object of the specified data type:

```java
// Variable assigned like an object using a constructor
String myOtherStr = new String("I'm a string too!");
```

We can create strings using either of these methods, but you'll typically use the literal notation.

> 🧠 There are subtle differences in strings created using these two methods - check out [this article](https://codehs.com/tutorial/david/understand-the-java-string-pool) for some of the details behind this if you're curious.

### `null`

A `null` value is an empty value. It is specifically signifies a **lack of value**.

Strings, like all other object types, are given a value of `null` when they are declared but not initialized:

```java
String myUninitializedString;
System.out.println(myUninitializedString);
// This will cause an error - you cannot use an uninitialized variable.
```

### `String` helper methods

Because a string is an object, it has predefined methods we can use.

#### `length()`

Used to find the length of a string:

```java
System.out.println("Hello!".length());
// Prints: 6
```

#### `charAt()`

To get the first letter of a string:

```java
System.out.println("Hey".charAt(0));
// Prints: "H"
```

#### `replace()`

To replace part of a string:

```java
System.out.println("Hello, world".replace("world", "friend"));
// Prints: "Hello, friend"
```

#### `toUpperCase()`

To make a string uppercase:

```java
System.out.println("hello!".toUpperCase());
// Prints: "HELLO!"
```

#### `concat()`

To concatenate two strings together:

```java
System.out.println("hello".concat(" world"));
// Prints: "hello world"
```

You can also add strings together using `+`:

```java
String twoStringsTogether = "Hello" + " World";
System.out.println(twoStringsTogether);
// Prints: "hello world"
```

#### These are just the beginning

Check out the **Method Summary** section of the [Java String class docs](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/String.html) for even more.

## String mutation

Note that none of the above methods mutate an existing string. Instead, they return a new string without modifying the original. For example:

```java
String greeting = "Hello"
String greetingsFriend = string.concat(", friend")
System.out.println(greeting);
// Prints: "Hello"
System.out.println(greetingsFriend);
// Prints: "Hello, friend"
```

Strings cannot be mutated in Java.

## Equality among strings

What if you want to compare one string to another?

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

Why isn't `withSigns` `true` when the output looks the same? Remember, `bl` and `ue` hold `String` data, which is an object type, and object types **hold a reference, not a value**.

The `==` operator compares the location where the object is stored in memory to see whether or not they're the same. `blue` contains a reference to where it's stored on the computer, and that's different from where `bl + ue` is stored.

Put another way, the `==` operator compares **identity**.

The `equals()` method, on the other hand, can be called on an instance of a `String` object  compares whether or not the characters in each `String` are the same, not whether or not the references are the same.

Or in another way, the `equals()` method compares **value**.

In short, when comparing object types, you will most often want to compare **value**, not **identity**. Therefore you will use the `equals()` method when comparing strings, and almost any other object type.

<div class="activity knowledge-check">
  <h2 class="title">Comparing data types</h2>
  <span class="minutes"></span>
</div>

Why can we call methods on a variable with a `String` data type but not an `int`?
