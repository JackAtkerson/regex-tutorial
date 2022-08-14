# How to Match an Email Using Regular Expressions

Regular expressions (Regex for short) are a powerful tool at the disposal of software developers. Despite appearing complicated, regular expressions are easy to use and understand when they are broken down into their base components.

## Summary

In this article, we will be breaking down a regular expression that can be used to extract email addresses from a document. Here is the regular expression we will be using:
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
 We will start by breaking the expression into components, and then we will explain the funtion of each component.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
Anchors are used to match strings that start or begin with certain elements. The ``` ^ ``` anchor denotes what the string will start with, and the ``` $ ``` anchor denotes the end of the string. As you can see in our example regex, we have a ``` ^ ``` at the beginning, and a ``` $ ``` to denote the end.
### Quantifiers
Quantifiers are used to specify how many instances of a character, group, or character class must be present for the input to be matched. In our example regex, the ``` + ``` quantifier is used. This quantifier matches the preceding string one or more times.
### OR Operator
OR Operators are used to match strings that contain one of the elements inside. 
### Character Classes

### Flags

### Grouping and Capturing
Using parentheses will create a group that will capture the value inside the parentheses
### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
