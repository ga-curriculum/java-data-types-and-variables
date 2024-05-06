# ![[tktk Module Name] - tktk Microlesson Name](./assets/data-types-and-variables-practice.png)

**Learning objective:** By the end of this lesson, students will be able to manipulate and edit data types and variables.

## Setup - Data Types and Variables Practice

Open IntelliJ IDEA Community Edition and create a new Java project. Select the following setting for this lab:

- **Named**: `inheritance-and-abstraction-lab`
- **Location**: `~/labs` - This can be anywhere, but I suggest this location for consistency
- **Build System**: IntelliJ
- **JDK**: 17 - This should be already downloaded on your machine

Once you have selected the settings, click `Finish`.

Remove the starter code from the `Main.java` file and complete the exercises.

### Running your Work

When you are at a point to run your work, you can either:

1. Right-click on the `Main` class and select `Run 'Main.main()'`.
2. Click the green play button next to the `Main` class.
3. Use the terminal to compile and run the program.

## Exercise - Data Types and Variables Practice

Inside of the `main` method, complete the following exercises:

Copy the following code into your `main` method and replace the `___` with the appropriate data type:

```java
___ oldYear = 1950;
___ nowYear = 2016;

___ averageFamilyIncome1950 = 3_300;
___ medianHomePrice1950 = 7_354;
___ tuitionYale1950 = 600;
___ roomAndBoardYale1950 = 456;
___ otherExpensesYale1950 = 376;

___ averageFamilyIncome2015 = 51_017;
___ medianHomePrice2015 = 188_900;
___ medianHomePriceManhattan2013 = 855_000;
___ tuitionYale2015 = 45_800;
___ roomAndBoardYale2015 = 14_000;
___ otherExpensesYale2015 = 5_552;

___ intro = "To understand how purchasing power has changed in the past 65 years, it is useful to compare the family income to the cost of goods and services, such as housing and education.";
```

Copy the following code into your `main` method below the previous code. Examine the code and find the mistake:

```java
if (intro == "A long time ago in a galaxy far, far away") {
    System.out.println("May the force be with you.");
}
else {
    System.out.println(intro);
}
```

Under the previous code and using the variables from the first exercise, complete the following mathematical calculations:

- Divide the median home price by annual income and print each result to the command line. Make three variables: `homeRatio1950`, `homeRatio2015`, and `homeRatioNYC2015`.
- Find the total cost of university education for 1950 and 2015 and print the result to the command line. Then, divide university cost by annual income for `educationRatio1950`, & `educationRation2015`. Print the results to the command line.

Under the previous code, convert the following `String` into a number:

```java
String averageDebt1950 = "2000";
```

Under the previous code, complete the following variable declarations, find the typo, and replace the `/*something*/`'s in the `String` with the proper variables:

```java
___ creditCardDebt2010 = 15_355;
___ totalDebt2010 = 129,579;
String debt = "Debt is an unwelcome guest at the table in many American households. In the late 1940s and early 1950s, the average American consumer had less than $/*something*/ in total personal debt. Today, the average U.S. household with debt carries $/*something*/ in credit card debt and $/*something*/ in total debt.";
```

Using the string `debt`, determine if the following string contains the word "table". Print the result to the command line.

## Bonus

Still using the variables from the previous exercises, answer the following question:

- How has the debt-to-income ratio changed in the past 60 years?
- Round the answer to two decimal places.

### Sources

The numbers for this exercise were taken from the following sources:

- [Cost of Living 2014 - Inflation 1950 vs. 2014 Data: Housing, Cars, College](http://www.mybudget360.com/cost-of-living-2014-inflation-1950-vs-2014-data-housing-cars-college/)
- [1701-1976 Yale Book of Numbers](http://oir.yale.edu/1701-1976-yale-book-numbers)
- [Yale Financial Aid Information](http://www.yale.edu/tuba/finaid/finaid-information/1516/1516EA_FYYE.pdf)
- [Manhattan Real Estate Ten-Year Review](http://www.forbes.com/sites/erincarlyle/2014/01/30/manhattan-real-estate-ten-year-review-neighborhoods-where-prices-have-gone-up-the-most/)
- [Americans' Personal Debt Skyrockets](https://www.mainstreet.com/article/americans-personal-debt-skyrockets)
- [Average Credit Card Debt per Household](http://www.nerdwallet.com/blog/credit-card-data/average-credit-card-debt-household/)

## Conclusion (5 min)

- Identify the different types of data.
- What type of data is passed as a web request?