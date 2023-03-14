# Unit-Testing-Article-Group4
## Introduction
Software testing is an important aspect of software development. It involves various types of testing, such as integration, system, and acceptance testing, to ensure that the application functions as intended by the end user. The term used to describe this type of testing method is behavior-driven development (BDD). Lately, there has been a rising trend among developers towards the test-driven development (TDD) methodology, where they write unit tests prior and then modify the code until the tests are successfully passed.
 ([Unit testing- datacamp]( https://www.datacamp.com/tutorial/pytest-tutorial-a-hands-on-guide-to-unit-testing))
 
 
In this article, we are focusing on unit test.

 
 ## What is Unit testing? 

Unit testing is a testing method designed to evaluate individual units or components of a software system separately to ensure that any errors or issues are confined to the specific unit being tested and do not impact the rest of the code. This approach enables developers to identify and fix bugs quickly, thereby reducing the risk of introducing problems into a larger codebase when integrating changes. ( [Unit testing- lambdatest]( https://www.lambdatest.com/learning-hub/unit-testing))

Unit testing is a form of white-box testing that involves developers writing test cases to evaluate the performance of individual functions, methods, and classes. The tests are created in either pseudocode, which is then implemented in a programming language like Java or JavaScript, or in plain English, depending on the programming language used in the development process. ( [Unit testing- lambdatest]( https://www.lambdatest.com/learning-hub/unit-testing))

Unit testing is also considered as automated test since the test plan is carried out by scripts instead of being performed manually by a human being.
([Unit testing- datacamp]( https://www.datacamp.com/tutorial/pytest-tutorial-a-hands-on-guide-to-unit-testing))

The following stages are involved in running unit tests:

1. Creating test cases: This involves creating a set of test cases that cover different scenarios and using those test cases for each component of an application that needs to be tested.

2. Review and re-write: After writing the test cases, it is necessary to examine them and make any necessary revisions or corrections if there are any errors.
3. Baseline: Checking each line of code is written correctly.
4. Execution: Conduct the test execution. The process includes validating the functionality of each feature in a software application by testing it under various scenarios to ensure that it performs as expected.
( [Unit testing- lambdatest]( https://www.lambdatest.com/learning-hub/unit-testing))


## Why unit testing is important?
Unit testing is important because it helps ensure that individual components of a software system are working as intended. By running tests on individual units, developers can quickly identify and fix issues, improving the overall quality and reliability of the system. Unit testing also promotes good coding practices by encouraging developers to write modular, testable code. This can make it easier to maintain and extend the codebase over time. Additionally, unit testing can improve collaboration between team members by providing a clear, automated way to validate changes to the code. Overall, unit testing is an essential tool for building robust and high-quality software systems. ([Unit testing- brightsec](https://brightsec.com/blog/unit-testing-best-practices/))

Unit testing helps to catch bugs early in the development cycle, reducing the cost and time required to fix them. It also helps to ensure that changes to the code do not break existing functionality, by serving as a safety net as the codebase grows and evolves.Unit testing also helps to improve the overall design of the code, encouraging the creation of modular, testable components. This leads to code that is easier to maintain and understand, as well as a development process that is faster and more efficient. ([Unit testing- microsoft](https://learn.microsoft.com/en-us/dotnet/core/testing/unit-testing-best-practices))

 By writing and executing unit tests, developers can ensure that the code they write behaves as expected and is free from bugs and other defects. This helps to improve the overall quality and reliability of the system, reducing the risk of issues arising later in the development cycle. Finally, unit testing provides a clear, automated way to validate changes to the code, improving collaboration between team members and streamlining the development process. Overall, unit testing is a critical component of modern software development and helps to ensure that software systems are reliable, efficient, and maintainable. ([Unit testing- simform](https://www.simform.com/blog/unit-testing-best-practices/))
 
## How unit testing is done?
 - Software testing methods like unit testing are essential for assuring the dependability and quality of a program. Early bug detection and correction can save time and money in the long run because it is a cost-effective method.
- The ability to independently test particular pieces of code rather than having to test the complete application is one of the main advantages of unit testing. 
- This improves in spotting issues early on in the development process, before they escalate in complexity and cost to resolve. Unit tests also offer a safety net for upcoming code revisions, making it simpler to make sure that changes to one section of the code do not unintentionally break another.
- Additionally, unit testing encourages a more flexible and reusable code architecture. Developers are compelled to consider the different parts of their code in isolation and how they interact with one another when they design unit tests. As a result, the codebase is better planned and easier to maintain.


Unit testing can be done in one of two ways:


- Manual unit testing entails carrying out each test phase by hand. Without the use of an automation tool, manual testing is time-consuming and laborious, especially for repetitive test cases, and it takes more work to create and execute test cases.
Automated unit testing is the process of employing automated testing technologies to automate routine manual processes. You can record, preserve, and replay your tests using automated testing technologies to avoid manual effort.
- However, many usability problems may go unnoticed during a website's testing. For instance, certain features of your website function properly on Chrome 99 (Windows 11), but not in Firefox 97. (Windows 11). Cross-browser testing is therefore crucial to resolving such usability issues before your customers do.


- Automated browser and user interface testing can be carried out using a variety of unit testing frameworks. You can automate your browser and app testing across 3000+ real browsers, devices, and operating system combinations with a cloud-based testing tool like LambdaTest. It also provides parallel testing, which can drastically reduce the time it takes to run all of your tests.
([How to perform Unit Testing](https://www.lambdatest.com/learning-hub/unit-testing#i)).

# Examples of unit test 

## Example code for temperature check test cases
```java
 # is (input, expected result, comment)
is( FtoC(32),0,'Freezing point is F32, C 0');
is( FtoC(212),100,'Boiling point is F212, C 100');
is( FtoC(59038),32767, 'Upper limit of C is 32767'); 
is( FtoC(59039),undefined, 'One past upper limit is error');
``` 
[Why is unit testing is important to developers](https://www.techtarget.com/searchsoftwarequality/answer/Is-unit-testing-an-important-aspect-of-software-development)

## Example-2
```java
public class FakeDateTimeProvider : IDateTimeProvider
{
    public DateTime ReturnValue { get; set; }

    public DateTime GetDateTime() { return ReturnValue; }

    public FakeDateTimeProvider(DateTime returnValue) { ReturnValue = returnValue; }
}
```
### Test case
```java
[TestMethod]
void ActuateLights_MotionDetected_SavesTimeOfMotion()
{
    // Arrange
    var controller = new SmartHomeController(new FakeDateTimeProvider(new DateTime(2015, 12, 31, 23, 59, 59)));

    // Act
    controller.ActuateLights(true);

    // Assert
    Assert.AreEqual(new DateTime(2015, 12, 31, 23, 59, 59), controller.LastMotionTime);
}
```
[Unit testing and coding : best practices](https://www.toptal.com/qa/how-to-write-testable-code-and-why-it-matters#:~:text=A%20typical%20unit%20test%20contains,it%20observes%20the%20resulting%20behavior)

## Example for calculating the area of a rectangle in C# - 3
```c#
// A class with a method to calculate the area of a rectangle
public class Rectangle {
    public double CalculateArea(double length, double width) {
        if (length <= 0 || width <= 0) {
            return -1;
        } else {
            return length * width;
        }
    }
}

// A test class to check if the Rectangle class is working as expected
[TestClass]
public class RectangleTest {
    [TestMethod]
    public void TestCalculateArea() {
        Rectangle rectangle = new Rectangle();
        double area = rectangle.CalculateArea(20, 30);
        Assert.AreEqual(50, area);

        area = rectangle.CalculateArea(0, 50);
        Assert.AreEqual(-1, area);

        area = rectangle.CalculateArea(10, -50);
        Assert.AreEqual(-1, area);
    }
}
```

The code includes a Rectangle class with a CalculateArea method that calculates the area of a rectangle using length and width parameters, but returns -1 if either parameter is less than or equal to zero. The RectangleTest class has a TestCalculateArea method that creates an instance of the Rectangle class and tests the CalculateArea method with various inputs, checking for expected output using the Assert.AreEqual method. The tests include a valid input, an input with length 0, and an input with negative width, to verify that invalid inputs are handled properly.([Example code for calculating rectangle area](https://dotnettutorials.net/lesson/area-of-rectangle-in-csharp/))

### General test case Example

```java
package demo.tests;
import static org.junit.Assert.*;
import org.junit.After;
import org.junit.Before;
import org.junit.Test;
public class JUnitProgram {
    @Test
    public void test_JUnit() {
        System.out.println("This is the testcase in this class");
        String str1="This is the testcase in this class";
        assertEquals("This is the testcase in this class", str1);
    }
}
```
[Hou to write general test cases with example](https://www.softwaretestinghelp.com/junit-tests-examples/).

## Conclusion
In summary, unit testing is an essential step in the development of software that focuses on ensuring the functionality of individual application components. It encourages excellent coding methods, helps in the early detection of defects, and raises the system's overall quality and dependability. Developers can quickly find problems and solve them while reducing time and expense by separating and testing individual parts. Ultimately, unit testing is a crucial technique for creating reliable, high-quality software systems, and every software development process should include it.

## References
- [Unit testing- datacamp](https://www.datacamp.com/tutorial/pytest-tutorial-a-hands-on-guide-tit-testino-ung)

- [Unit testing best practices-brightsec](https://brightsec.com/blog/unit-testing-best-practices/)
- [Unit testing best practices-microsoft](https://learn.microsoft.com/en-us/dotnet/core/testing/unit-testing-best-practices)
- [Unit testing best practices-simform](https://www.simform.com/blog/unit-testing-best-practices/)
- [How to perform Unit Testing](https://www.lambdatest.com/learning-hub/unit-testing#i).
- [Example code for calculating rectangle area](https://dotnettutorials.net/lesson/area-of-rectangle-in-csharp/)
- [Unit testing and coding : best practices](https://www.toptal.com/qa/how-to-write-testable-code-and-why-it-matters#:~:text=A%20typical%20unit%20test%20contains,it%20observes%20the%20resulting%20behavior)
- [Unit testing- lambdatest]( https://www.lambdatest.com/learning-hub/unit-testing)
- [Hou to write general test cases with example](https://www.softwaretestinghelp.com/junit-tests-examples/).
