# ![[tktk Module Name] - tktk Microlesson Name](./assets/data-types-in-java.png)

**Learning objective:** By the end of this lesson, students will be able to predict what data falls into data type categories with ideated examples.

## Opening (5 min)

In programming, we need a way of storing information while our programs are running. This could be anything from names and numbers to dates and many other things, which are all known as **data types**. These data types are stored in **variables**, just like in algebra class. Today, we'll be exploring how data types and variables form the basic building blocks of programming and how we use them to store information in our programs.

----

## Introduction: Data Types in Java (10 min)

In computer science and computer programming, a data type — or simply, type — is a classification identifying one of various types of data that determines:
- The possible values for that type.
- The operations that can be done on values of that type.
- The meaning of the data.
- The way values of that type can be stored.

Data types are similar across different languages, including English.

<!-- **Instructor Note**: Put the categories on the board and ask students to provide the data type or in some other way create a list on the board that includes the data types below. Include both lowercase primitive and capitalized object types. This chart will be referenced later.-->

|Category    | Data Type                     | Description          | Example |
|------------|------------------------------|----------------------|---------|
|True or False  | `boolean`, `Boolean`                   | Represents either true or false.                               |`true`, `false`|
|Integers    | `short`, `int`, `Integer`, `long`, `Long`    | Whole numbers; can optionally have underscores to make large numbers easier to read.	| `42`, `1024`, `1_000_000` |
|Decimals    | `float`, `Float`, `double`, `Double`       | Decimals.                                   | `42.123`, `2.5` |
|Characters  | `char`                               | A single character surrounded by single quotation marks.                 | `'a'`, `'A'`|
|Strings     | `String`                             | Single words or sentences surrounded by double quotation marks.        | `"lots of kittens"`, `"a lazy lizard"`    |                                                                | `true`, `false`

There are also a few odd ones:
- **Byte**, which is one bit of data. You don't need to worry about it right now.
- **Collections** (we'll talk more about these soon).

We'll elaborate on all of the categories on the board and show you some helper methods to manipulate them.

> **Knowledge Check**: Come up with a few examples of data. Predict what type it falls into.

_Created by Kristen Tonga_