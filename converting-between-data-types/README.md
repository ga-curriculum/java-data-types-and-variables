# ![[tktk Module Name] - tktk Microlesson Name](./assets/coverting-between-data-types.png)

**Learning objective:** By the end of this lesson, students will be able to describe the difference between `NaN` and `null`. 

## Demo: Converting Between Data Types (10 min)

Sometimes, it's necessary to convert between data types. User input is **always** a `String`, such as when you enter your email address, age, income, and more. If you'd like to operate on those numbers, however, you'll have to convert it to a numeric data type.

Remember how we talked about the size of primitive data types? A `float` is smaller than a `double`, and a `double` is smaller than a `long`.

When converting from smaller types to larger types — for example, `int` (4 bytes) to `double` (8 bytes) — conversion is done automatically. This is called **implicit casting**:

```java
int a = 100;
double b = a;
System.out.println(b);
```

If, on the other hand, you're converting from a bigger data type to a smaller data type — for example, `double` (8 bytes) to `int` (4 bytes) — the change in data type must be clearly marked. This is called **explicit casting**:

```java
double a = 100.7;
int b = (int) a;
System.out.println(b);
```

While that's useful for numbers, to cast successfully, a variable must be an **instance** of the second object.

What do you think would happen if you tried to cast a `String` to an `int`? There's a different way to convert `String`s into numbers.

Did you notice there's both an `int` and an `Integer` data type? The `Integer` data type is a wrapper around an `int` that provides certain methods.

For example, to convert a `String` to an `Integer`, you can use:

```java
String strValue = "42";
int intValue = Integer.valueOf(strValue);
```

Similar methods exist for all of the wrappers.

#### `NaN`

If a `String` is converted to a number but contains an invalid character, the result of the conversion will be **`NaN`**, which stands for "Not a Number."

`NaN` is toxic, and if a calculation is attempted on that variable or a method called subsequently, your program will break.

Use `isNaN()` to test for `NaN`.

#### `null`

A `null` value is an empty value. According to a StackOverflow post:

```
"Zero" is a value. It is the unique, known quantity of zero, which is meaningful in arithmetic and other math.

"Null" is a non-value. It is a "placeholder" for a data value that is not known or not specified.
```

> **Knowledge Check**: When might you get `NaN` value? What is a `null` value?

_Created by Kristen Tonga_