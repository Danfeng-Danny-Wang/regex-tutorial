# A Simple Regex Tutorial

Regex - regular expression - is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input.

## Summary

In this tutorial, I will be explaining this following regular expression that can be used to verify the input is a valid URL address.

```
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

```
/
```

The regex pattern is wrapped in slash characters (/).

### Anchors

```
^
```

The ^ anchor signifies a string that begins with the characters that follow it.

In our example, the string must start with http.

```
$
```

The $ anchor signifies a string that ends with the characters that precede it.

In our example, the string must end with an optional slash (\/?).

### Quantifiers

Quantifiers set the limits of the string that your regex matches (or an individual section of the string).

```
?
```

? matches the pattern zero or one time. So, in our example:

```
https?
```

This matches both 'http' and 'https'. In other words, the string can have an optional 's' after 'http'.

```
+
```

\+ matches the pattern one or more times. So, in our example:

```
[\da-z\.-]+
```

This matches the string that has at least 1 number, lowercase character a to z, a period, or a hyphen.

```
*
```

\* matches the pattern zero or more times. So, in out example:

```
[\/\w \.-]*
```

The string can have any number of '/', any words (\w), period, or hyphen.

```
{}
```

- { n } matches the pattern exactly n number of times
- { n, } matches the pattern at least n number of times
- { n, x } matches the pattern from a minimum of n number of times to a maximum of x number of times

In our example:

```
{2,6}
```

This means the preceding string pattern should happen a minimum of 2 times and a maximum of 6 times.

### Character Classes

A character class in a regex defines a set of characters.

```
\d
```

Matches any Arabic numeral digit. This class is equivalent to the bracket expression [0-9]

```
\w
```

Matches any alphanumeric character from the basic Latin alphabet, including the underscore (_). This class is equivalent to the bracket expression [A-Za-z0-9_].

### Grouping and Capturing

```
()
```

You can use parentheses (()) to group a section of a regex. Each section within parentheses is known as a subexpression. Unlike bracket expressions, subexpressions will look for an exact match unless they are told to do otherwise.

### Bracket Expressions

```
[]
```

Bracket expression represents a range of characters that we want to match. The string should match any of the requirements in the bracket expression. It does not need to match all of the requirements.

A hyphen (-) is often used between alphanumeric characters to represent a range of those possible characters.

```
[\da-z\.-]
```

In our example, this bracket expression represents any numbers (\d), character lowercase a to z (a-z), a period (\.), or a hyphen.

### Look-ahead and Look-behind

These regex concepts were not included in this tutorial:

- Flags
- Boundaries
- Greedy and Lazy match
- Back-references

## Author

Hey, my name is Danny. I'm a very rookie full-stack web developer.

My GitHub link is here: [Danfeng-Danny-Wang](https://github.com/Danfeng-Danny-Wang)
