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
Quantifiers are used to specify how many instances of a character, group, or character class must be present for the input to be matched. In our example regex, the ``` + ``` quantifier is used. This quantifier matches the preceding string one or more times. In this case, the regex engine will match strings containing one or more of the characters that match the criteria listed inside of the [bracket expressions](#bracket-expressions). The other quantifier used in our regex is ```{2,6}```. This will match a user specified range of characters that align with the search criteria. The first number is the minimum number of matches, and the second is the maximum. In our example, the minimum is set to 2 and the maximum is 6, so the regex engine will match 2 to 6 characters.

### OR Operator
OR Operators are used to match strings that contain one of the elements inside. 

### Character Classes
Character classes are used to tell the regex engine to match one of several possible characters. This is similar to listing a range of numbers or letters inside square brackets. In our example, we have the ```\d``` character class. This will find a single character in the string that is a digit. Other options are ```\w``` that will match a word, and ```\s``` which will match a whiteapce character.

### Flags

### Grouping and Capturing
Using parentheses will create a group that will capture the value inside the parentheses. Our example has placed three groups in parentheses to look for the beginning of an email address the domain name, and the ".com" or other ending to an email address. The first two groups are separated by a "@" because that will be in every email address, and the second two groups are separated by a "." for the same reason.

### Bracket Expressions
Inside of our groups are characters contained by square brackets. These are bracket expressions. They are a list of characters/character classes that will be matched by the regex engine. Let's break down the first bracket expression in our example:
```
[a-z0-9_\.-]
```
We can see a few criteria listed inside the brackets, but what do they mean? These are ranges of characters that will be matched by the regex engine. "a-z" will ask the engine to look for lowercase letters from a to z. Similarly, "0-9" will search for a number character between 0 and 9. On top of looking for a character within a range of characters, you can also look for specific characters. In our example, we are looking specifically for "_" or "-", as we have them listed inside the bracket.

### Greedy and Lazy Match
When using regular expressions, you can specify whether your quantifiers will make "greedy" matches or "lazy" matches. Greedy essentially means to match the longest possible string. Lazy, on the other hand, will match the shortest string possible. Our quantifier "+" is greedy, and will therefore look for characters until it cannot find any more that fit the search criteria. Adding a "?" after a quantifier will make it lazy. If we used "+?" it will look for characters that match each of the criteria once, and then it will not look for any more to match.

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
