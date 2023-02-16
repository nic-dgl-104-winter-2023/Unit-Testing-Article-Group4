# Unit-Testing-Article-Group4
## Introduction
 In software development, testing is an extensive topic of discussion. Before a software product reaches the hands of users, it will likely to have gone through several tests to ensure that the applications behaviour is as expected from the end user's perspective without any defects or bugs.( [Unit testing- datacamp](https://www.datacamp.com/tutorial/pytest-tutorial-a-hands-on-guide-tit-testino-ung) )

 There are two primary approaches used while testing software: Functional Testing and Non-functional Testing. Functional testing focuses on the functionality of a software product. It helps to understand whether the software is performing as needed. Each functionality is tested by providing the input, calculating the output, and comparing the actual result to the anticipated value. While non-functional testing is a sort of software testing used to evaluate the software's non-functional characteristics such as reliability, performance, and accountability. Testing, both functional and non-functional, is necessary for newly produced software. While non-functional testing examines an application's capacity to operate in an external environment, functional testing examines the accuracy of internal functions. ( [Unit testing- Javatpoint](https://www.javatpoint.com/types-of-software-testing) )

 In this article, we are concentrating on unit testing, a type of functional testing.
 ## What is Unit testing? 

Unit testing is a form of software testing that focuses on validating individual units or components of a software application and confirming that each unit functions as intended. It is considered the first phase of functional testing in the software development life cycle. It ensures that it has no impact on any other parts of your code than the component or unit under test by isolating them from the rest of your code. As a result, it isolates a single functional component, guarantees correctness, and confirms that there are no errors, enabling speedy bug fixes before merging them into the main code. It is a type of "white box" testing. It is frequently accomplished by writing test cases that test specific functions, methods, and classes. Test cases can be written in plain English, even though they are usually written in pseudocode (implemented in a language like Java or JavaScript).

The procedure for conducting unit tests consists of four steps:
- Creating test cases: Write several test cases for each component of a web application.
- Review and rewrite: Examine the written test cases and, if necessary, rewrite them if there are any mistakes.
- Baseline: Verify that each line of code is structured in a certain way.
or not.
- Execution: Choose an online Selenium grid to conduct test execution.

Unit tests are executed frequently and quickly, either individually or collectively. Even if they have complex logic or a lot of variables, they should be written in a straightforward, easy-to-read, and understandable manner. Unit testing is conducted before integration testing, so it can save a significant amount of time and money if done accurately. It can be done manually or automatically using different testing tools. ( [Unit testing- lambdatest]( https://www.lambdatest.com/learning-hub/unit-testing) )

Unit testing can be further classified into three different types of testing:

1. Whitebox testing- It is also known as glass box testing, structural testing, clear box testing, open box testing and transparent box testing. When performing this testing, the tester is familiar of the applications internal functionality and can test it against the design and requirements. It examines a software's internal code and infrastructure with a focus on comparing inputs that have been predefined to the desired and expected results. However, it is unknown what the internal structure of a component or function of an application is.

2. Black-box testing: In this kind of unit testing, the user interface, input, and output of the software application are all validated. To put it another way, black box testing is the process of evaluating an application's functioning in view of client requirements. This testing is known as black-box testing since the source code is hidden throughout it.
3. Gray-box testing: It is sometimes referred to as semi-transparent testing, is a combination of white-box and black-box testing. In this kind of testing, the testers are only partially familiar with the internal workings, functionality, and design specifications of the application. Gray-box testing encompasses a variety of test types, including regression, matrix, pattern, and orthogonal pattern testing.


## Why unit testing is important?
Unit testing is important because it helps ensure that individual components of a software system are working as intended. By running tests on individual units, developers can quickly identify and fix issues, improving the overall quality and reliability of the system. Unit testing also promotes good coding practices by encouraging developers to write modular, testable code. This can make it easier to maintain and extend the codebase over time. Additionally, unit testing can improve collaboration between team members by providing a clear, automated way to validate changes to the code. Overall, unit testing is an essential tool for building robust and high-quality software systems.

 https://brightsec.com/blog/unit-testing-best-practices/

Unit testing helps to catch bugs early in the development cycle, reducing the cost and time required to fix them. It also helps to ensure that changes to the code do not break existing functionality, by serving as a safety net as the codebase grows and evolves.

Unit testing also helps to improve the overall design of the code, encouraging the creation of modular, testable components. This leads to code that is easier to maintain and understand, as well as a development process that is faster and more efficient.

https://learn.microsoft.com/en-us/dotnet/core/testing/unit-testing-best-practices

 By writing and executing unit tests, developers can ensure that the code they write behaves as expected and is free from bugs and other defects. This helps to improve the overall quality and reliability of the system, reducing the risk of issues arising later in the development cycle. Finally, unit testing provides a clear, automated way to validate changes to the code, improving collaboration between team members and streamlining the development process. Overall, unit testing is a critical component of modern software development and helps to ensure that software systems are reliable, efficient, and maintainable.

https://www.simform.com/blog/unit-testing-best-practices/ 
## How unit testing is done?
 - Software testing methods like unit testing are essential for assuring the dependability and quality of a program. Early bug detection and correction can save time and money in the long run because it is a cost-effective method.
- The ability to independently test particular pieces of code rather than having to test the complete application is one of the main advantages of unit testing. 
- This improves in spotting issues early on in the development process, before they escalate in complexity and cost to resolve. Unit tests also offer a safety net for upcoming code revisions, making it simpler to make sure that changes to one section of the code do not unintentionally break another.
- Additionally, unit testing encourages a more flexible and reusable code architecture. Developers are compelled to consider the different parts of their code in isolation and how they interact with one another when they design unit tests. As a result, the codebase is better planned and easier to maintain.

# Example of unit test code

## Example code for temperature check test cases- 1
```java
 # is (input, expected result, comment)
is( FtoC(32),0,'Freezing point is F32, C 0');
is( FtoC(212),100,'Boiling point is F212, C 100');
is( FtoC(59038),32767, 'Upper limit of C is 32767'); 
is( FtoC(59039),undefined, 'One past upper limit is error');
``` 
[Why is unit testing is imortent to developers](https://www.techtarget.com/searchsoftwarequality/answer/Is-unit-testing-an-important-aspect-of-software-development)

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

## Example for calculating the area of a rectangle-3
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
        double area = rectangle.CalculateArea(5, 10);
        Assert.AreEqual(50, area);

        area = rectangle.CalculateArea(0, 10);
        Assert.AreEqual(-1, area);

        area = rectangle.CalculateArea(5, -10);
        Assert.AreEqual(-1, area);
    }
}
```

