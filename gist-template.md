# Interpreting a regex Email Match

The purpose of this tutorial is to help developers understand and implement Regex into their applications. Regex is a generally universal language that is used to help determine whether an input is acceptable for use within the application. In this example we will go over the regex for a simple email.

## Summary

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

This regex is used by developers to determine whether an email is valid or not!

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

In the regex example above, the anchors used are the '^' and '$'.

- The '^' represents the beggining of the string in question.
- The '$' represents the end of the string in question.

They are used to contain what is trying to get matched.

### Quantifiers

In the regex example above, the first quantifier is the '+' and the second set of quanifiers are {2,6}.

The '+' is used to say that the previous set must match at least one of the included tokens.
{2,6} is used to show how many characters are used in the previous set.
In this example, the previous token can have between 2 and 6 characters.

### OR Operator

There are no OR operators in this example. or is represented by a '|' in cases where it is used.

### Character Classes

The regex example above has many different character classes.
In [a-z0-9_\.-]

- 'a-z' represents that the input matches any letter a to z. It is case sensitive.
- '0-9' represents that the input matches any number from 0 to 9
- '_' represents that _ is accepted as a match
- '\.' represents that . is accepted as a match. It has \ before it because it is used specifically later in the regex espression.
- '-' represents that - is accepted as a match.

In [\da-z\.-]

- '\d' represents that any digit can be used as a match. Similar to '0-9'.

* 'a-z' represents that the input matches any letter a to z. It is case sensitive.
* '\.' represents that . is accepted as a match. It has \ before it because it is used specifically later in the regex espression.
* '-' represents that - is accepted as a match.

### Flags

There are no flags in this regex expression.

### Grouping and Capturing

Groups are determined by '()'
In the regex example above ([a-z0-9_\.-]+)

- '+' show that at least one of the previous tokens must be present to be valid
- '[a-z0-9_\.-]' show all of the different character classes or tokens that will make this valid for use.

### Bracket Expressions

Bracket expressions group tokens together in order to validate the expression provided.

For example: In ryan42buck@gmail.com

- The first bracket '[a-z0-9_\.-]' is used to decypher if 'ryan42buck' is a valid input.
- The '@' is used literally in this expression so it does not need to be in a set of brackets.
- The second braket '[\da-z\.-]' is used to determine if gmail is a valid input.

* '\.' or an escaped . is used literally in this expression so it does not need to be in a set of brackets
* The third bracket [a-z\.] is used to determine if com is a valid input

### Greedy and Lazy Match

There are no lazy matches in this expression. Lazy matches are used by using '?'.
In this case it is a greedy match which means that it matches as many of the characters as it can.

### Boundaries

There are no boundaries in this expression. Boundaries are represented by the '\b' anchor.

### Back-references

There are no Back references in this expression. Back references are used by '\1' to refer back to a previous section of the expression to use in a later part in the expression.

### Look-ahead and Look-behind

Neither look ahead or look behind is used in this expression. Look ahead is used to find characters previous to a key character. Look behind is used to find characters after a key character.

## Author

My name is Ryan Buckley and I am currently a student learning JavaScript though Case Western Reserve University.

https://github.com/Ryan-Buckley1
