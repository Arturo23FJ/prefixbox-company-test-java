# Prefixbox Test

## Short questions

- What is a package? How do you define a package?
- A package in Java is used to group related classes. Think of it as a folder in a file directory. We use packages to avoid name conflicts, and to write a better maintainable code.

- What is a constructor? When is it executed?
- A constructor in Java is a special method that is used to initialize objects. The constructor is called when an object of a class is created.

- How do you implement inheritance in Java?
- To inherit from a class, use the extends keyword.

- How do you prevent someone to inherit from a class?
- If you don't want other classes to inherit from a class, use the final keyword.

- What is a final variable? Where you can assign value to final variables?
- A non-access modifier used for classes, attributes and methods, which makes them non-changeable.
- In Java, non-static final variables can be assigned a value either in constructor or with the declaration. But, static final variables cannot be assigned value in constructor; they must be assigned a value with their declaration.

- Specify the available access modifiers in Java and briefly explain them
private - visible to the class only
protected - visible to the package and all subclasses
public - visible to the world

- Briefly explain the mechanism of exception handling
- The Exception Handling in Java is one of the powerful mechanism to handle the runtime errors so that normal flow of the application can be maintained.

- What is the difference between an abstract class and an interface?
- A class can have a state which can be modified by non-abstract methods but an interface cannot have the state because they can't have instance variables. The second difference is that an interface cannot have a constructor even in Java 8 but abstract class always has a constructor in Java.
- What is the difference between Comparator and Comparable?
- A Comparable object is capable of comparing itself with another object of same type. A Comparator object is capable of comparing two objects of another class.
- How Iterable and Iterator interface works? What methods need to exist in a class that implements them? What is their relation to for loops?
- An Iterable is a simple representation of a series of elements that can be iterated over. It does not have any iteration state such as a "current element". Instead, it has one method that produces an Iterator. An Iterator is the object with iteration state. It lets you check if it has more elements using hasNext() and move to the next element (if any) using next(). Every class that implements Iterable interface appropriately, can be used in the enhanced For loop (for-each loop).
## Programming tasks

You can write your solutions in any language, you can even write pseudo code or
using only your own words.
The point is not to make a perfectly running application, the point is the way
you think!
Don't worry if you miss a semicolon or some parantheses.
You might use the Java stream API for your solutions but none of the exercises
require them

### Palindrom

Write a function which decides whether a text is palindrom(It's the same whether
you read it forwards or backwards). E.g.: abba, rotator, stats.
You might assume that the input string is not null, the length is greater than
1 and less than one million. **Strive for the low memory complexity!**

Example:

```java
public boolean isPalindrom(String input) {

}

isPalindrom("alma"); //false
isPalindrom("görög"); //true
```

### Find The Duplicate

You have an array that contains strings. Every item in the array is
unique except one which is present in the array exactly twice.
Write a function which finds the string that is present twice in the array.
You might assume that the input array is not null, the length is greater
or equal to 2 and less than one million. **Strive for the low time complexity!**

Example:

```java
public String findTheDuplicate(String[] input) {

}

String[] fruitBasket = new String[] { "apple", "banana", "coconut", "durian",
"banana", "elderberry", "fig", "grapefruit" };
findTheDuplicate(fruitBasket); //should return banana
```

### Count The Words

You have a long string that has some meaning on a real language. For example a
whole novel in a single string.
Write a function that counts the occurence of each word inside the string and
writes them to the output in the following format: `word: number of occurences`
You might assume that the input is not null and not empty. The order of the
words on the ouput does not matter.
The solution might be case insensitive, you don't have to differentiate
bwetween capital and non-capital letters.
The punctuation marks and line endings are not part of the words!

Example:

```java
public void countTheWords(String crazyLongString) {

}

String boci = "Boci, boci tarka, se füle, se farka.";
countTheWords(boci);

//Output:
//boci:2
//tarka:1
//se:2
//füle:1
//farka:1
```

### What Is The Output

What is the output of the following Java application? Explain your solution!

```java
package com.mycompany.myproject;

public class Person {
    public String firstName;
    public String lastName;

    public Person(String firstName, String lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }  

    @Override
    public String toString() {return this.firstName + " " + this.lastName;}
}

public class Main {
    public static void main(String[] args) {
        int i = 0;
        String s = "apple";
        Person p = new Person("Jonh", "Doe");

        doSomething(i, s, p);

        System.out.println(i);
        System.out.println(s);
        System.out.println(p);
    }

    public static void doSomething(int i, String s, Person p)
    {
        i = 5;
        s += "banana";
        p.lastName = "Rambo";
    }
}

```

## SQL

- What is the PRIMARY KEY?
- What is the difference between CLUSTERED INDEX and NONCLUSTERED INDEX?
- There is a table called `Employees`. Let's assume that the columns exist
and they have the right data type.
What is going to happen if we execute the script and we destroy
the database connection during the execution? What are the possible problems
that might occure?

```sql
BEGIN TRANSACTION

UPDATE Employees
SET Salary = Salary * 1.1
WHERE
    Salary < 250000
    AND IsActiveEmployee = 1
```

## Web and HTTP

- Specify the existing HTTP request methods and describe their usage!
- What are the groups of HTTP response status codes? Write an example for each group!
