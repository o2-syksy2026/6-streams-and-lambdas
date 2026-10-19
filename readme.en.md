# Streams and lambdas

![A stream as a conveyor belt: values pass through filter and map stages into a list](img/chapters/streams.svg)

In this repository, you get familiar with Java's Stream API and lambda expressions. The exercise is divided into parts, each with a Java class whose unfinished methods you complete with streams and lambdas according to their comments and hints. The package has no main program; instead, each part has its own unit tests.

Recommended self-study materials:

* [The Stream API (dev.java)](https://dev.java/learn/api/streams/)
* [Lambda Expressions in Java (Coding with John, YouTube)](https://youtu.be/tj5sLSFjVj4)
* [Optionals In Java (Coding with John, YouTube)](https://youtu.be/vKVzRbsMnTQ)
* [The Java 8 Stream API Tutorial (baeldung.com)](https://www.baeldung.com/java-8-streams)

## Starting the exercise

First fork this repository into your own GitHub repository with GitHub's **Fork** button, and only then clone your fork to your computer:

```sh
git clone https://github.com/<your-github-username>/6-streams-and-lambdas.git
```

Open the cloned project in your code editor.

## Testing

The parts of the exercise have ready-made [JUnit](https://junit.org/) unit tests in the [src/test/java](./src/test/java/) directory. Each part tells which test class grades it. You can run the tests with your code editor's testing tool ([VS Code](https://code.visualstudio.com/docs/java/java-testing), [Eclipse](https://www.vogella.com/tutorials/JUnitEclipse/article.html)) or with [Gradle](https://docs.gradle.org/current/userguide/java_testing.html), for example:

```
./gradlew test --tests IntegerStreamsTest        # unix
.\gradlew.bat test --tests IntegerStreamsTest    # windows
```

Add `--info` to the end of the command for more details about failing tests. You do not need to study how the tests are implemented, and you can also try your solution with your own `main` method. You may write more tests of your own, but do not change or remove the given tests.

Do not change the names, parameters or return types of the given classes, methods and constructors, because the tests will then not compile. You get the original version of a file back with `git restore <path to file>` or with the **Palauta lähtökoodi** (restore starter code) function of the course system.

## Submitting and points

Each part of the exercise has its own page in the course system (https://jtjuslin.kapsi.fi/java), and its code fields contain the part's starter code. Copy your solution into the code fields or write it there directly. **Testaa ilman palautusta** (test without submitting) runs the part's tests without saving points, and **Lähetä** (submit) submits your solution. Each test class is accepted only if all of its tests pass, and the points are divided according to the accepted test classes.

**Points in two stages**

1. When your solution passes in the course system, you get **half of the points** for the part.
2. Finally, push everything to your public GitHub repository. Then press the **Lähetä tarkistettavaksi** (submit for checking) button on the part's page. When the tests pass, you get **full points** for the part. The repository may remain public.

There is no grading YAML workflow (GitHub Actions) on GitHub, and `git push` does not start any grading. When you press **Lähetä tarkistettavaksi**, the course system's bot fetches your code from your repository and checks it with the same tests. Both stages must be completed before the chapter deadline. You can submit as many times as you need, and your best result is kept.


## Part 1: IntegerStreams *(basics, 10 %)*

You learn to use the ready-made methods of the [IntStream class](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/stream/IntStream.html) that perform common calculations on streams of integers. Complete the methods of the [IntegerStreams](./src/main/java/part01/IntegerStreams.java) class.

Graded with the test class [IntegerStreamsTest](./src/test/java/part01/IntegerStreamsTest.java).


## Part 2: OptionalValues *(basics, 10 %)*

You learn to handle situations where a stream may not contain any values, which must be taken into account when calculating an average or extreme values, for example. In such situations, Java uses "optional" objects: [Optional](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Optional.html), [OptionalDouble](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/OptionalDouble.html) and [OptionalInt](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/OptionalInt.html). Complete the methods of the [OptionalValues](./src/main/java/part02/OptionalValues.java) class.

Graded with the test class [OptionalValuesTest](./src/test/java/part02/OptionalValuesTest.java).


## Part 3: ListsAndStreams *(basics, 10 %)*

You learn to create streams from lists and lists from streams. Complete the methods of the [ListsAndStreams](./src/main/java/part03/ListsAndStreams.java) class.

Graded with the test class [ListsAndStreamsTest](./src/test/java/part03/ListsAndStreamsTest.java).


## Part 4: MappingStreams *(basics, 10 %)*

You learn to create new streams by transforming the values of an existing stream. The transformations are typically written as lambda expressions. Complete the methods of the [MappingStreams](./src/main/java/part04/MappingStreams.java) class.

Graded with the test class [MappingStreamsTest](./src/test/java/part04/MappingStreamsTest.java).


## Part 5: FilteringStreams *(basics, 10 %)*

Filtering data is a very common use of streams. You learn to select only the values that meet certain conditions into a new stream. Complete the methods of the [FilteringStreams](./src/main/java/part05/FilteringStreams.java) class.

Graded with the test class [FilteringStreamsTest](./src/test/java/part05/FilteringStreamsTest.java).


## Part 6: PredicatesWithStreams *(basics, 10 %)*

You learn to check conditions that concern the whole stream. Complete the methods of the [PredicatesWithStreams](./src/main/java/part06/PredicatesWithStreams.java) class.

Graded with the test class [PredicatesWithStreamsTest](./src/test/java/part06/PredicatesWithStreamsTest.java).


## Part 7: ObjectStreams *(applying, 10 %)*

You apply streams to your own [Person](./src/main/java/person/Person.java) class and notice that handling your own classes with streams is very similar to handling Java's built-in types. Complete the methods of the [ObjectStreams](./src/main/java/part07/ObjectStreams.java) class.

Graded with the test class [ObjectStreamsTest](./src/test/java/part07/ObjectStreamsTest.java).


## Part 8: PersonStreams *(applying, 10 %)*

You convert strings into [Person](./src/main/java/person/Person.java) objects and back, and perform applied operations, such as increasing the age of every person in the stream by one year. Complete the methods of the [PersonStreams](./src/main/java/part08/PersonStreams.java) class.

Graded with the test class [PersonStreamsTest](./src/test/java/part08/PersonStreamsTest.java).


## Part 9: PizzaStreams *(advanced, 20 %)*

You handle [pizzas](./src/main/java/pizza/Pizza.java) and their toppings with streams. We focus especially on pineapple, a particularly controversial topping, and practice applied operations, such as sorting streams. Complete the methods of the [PizzaStreams](./src/main/java/part09/PizzaStreams.java) class.

Graded with the test class [PizzaStreamsTest](./src/test/java/part09/PizzaStreamsTest.java).


## License and authors

This exercise was developed by Teemu Havulinna and Jukka Juslin, and it is licensed under the [Creative Commons BY-NC-SA license](https://creativecommons.org/licenses/by-nc-sa/4.0/). ChatGPT 3.5 and GitHub Copilot were used in creating the assignment, the source code and the tests.
