<h1>
  <span class="headline">Java Data Types and Variables</span>
  <span class="subhead">Instructor Guide</span>
</h1>

## Lecture tips

Students will set up a more advanced file structure for this work - don't rush through the setup steps, but there are screenshots included to help students that fall a little behind.

In the [Data Types in Java](../primitive-data-types/README.md) microlesson, consider using a whiteboard to draw a table of data types. The table should include a **Data type** and **Example** column. Write the data types on the board in the **Data type** column and ask students to provide a couple of examples of that data type for you to write in the **Example** column.

Here's an example to get you started:

| Data type | Example                             |
|-----------|-------------------------------------|
| `boolean` |                                     |
| `int`     |                                     |
| `double`  |                                     |
| `byte`    |                                     |
| `short`   |                                     |
| `long`    |                                     |
| `float`   |                                     |
| `char`    |                                     |

As you go through the [Working With Numbers](../working-with-numbers/README.md) microlesson, code the examples, and ask students what they think the answer to each question will be before you run the code. If they guess correctly, ask them to explain why. The lecture prompts you to do this by default so you won't need to think about this in the moment.

The **Where does `Math` come from?** knowledge check in the [Working With Numbers](../working-with-numbers/README.md) microlesson provides a great opportunity to demo the [Java docs](https://docs.oracle.com/en/java/javase/17/docs/api/index.html)

It's easy to get in-the-weeds in the pass by value topic in [Primitive vs. Object Types](../primitive-vs-object-types/README.md) - feel free to touch on it briefly and return to to the topic more later when you're able to create more informed examples.

Here is a solution to the [Data Types and Variables Practice](../data-types-and-variables-practice/README.md):

```java
public class Main {
    public static void main(String[] args) {
        // TODO: Fix the following variable declarations by providing the correct type in place of the ___.

        int yearMoonLanding = 1969;
        int yearCurrent = Year.now().getValue();

        int distanceToMoonKM = 384_400;
        int averageHeightEverestMeters = 8_848;

        double averageRainfallInches2023 = 35.5;
        double highestTemperatureRecordedCelsius = 56.7;
        double lowestTemperatureRecordedCelsius = -89.25;

        String intro = "Exploring natural wonders and scientific discoveries helps us understand the world around us.";

        // TODO: Complete the following mathematical calculations.

        // Calculate the time difference between yearMoonLanding and yearCurrent, and print the result.

        System.out.println(yearCurrent - yearMoonLanding);

        // Divide distanceToMoonKM by the average speed of light (299,792 km/s) to find how long it takes for light to travel from the Moon to Earth. Print the result.

        System.out.println((double) distanceToMoonKM / 299_792d);

        // TODO: Convert the following String into a number.

        String population2011 = "7_000_000_000";

        long intPopulation2011 = Long.parseLong(population2011.replace("_", ""));

        System.out.println(intPopulation2011);

        // TODO: Complete the following variable declarations, find the typo, and replace the /*something*/s in the String with the proper variables, then print the result.

        int averageHumanLifespanYears = 72;
        int numberOfContinents = 7;
        String earthStats = "The average human lifespan is " + averageHumanLifespanYears + " years, and our planet has " + numberOfContinents + " continents.";

        System.out.println(earthStats);

        // TODO: Using one line of code, determine if the `earthStats` string contains the word "wonders". Print the result to the command line.

        System.out.println(earthStats.contains("wonders"));

        // TODO: Calculate the average temperature between the highest recorded temperature and the lowest recorded temperature.

        double averageOfExtremes = (highestTemperatureRecordedCelsius + lowestTemperatureRecordedCelsius) / 2;

        System.out.println(averageOfExtremes);

        // EXTRA: Round the answer above to two decimal places.

        System.out.println(Math.round(averageOfExtremes * 100) / 100.0);

    }
}
```
