# Title (replace with your title)

In this article, we will explore how to use regular expressions to match IP addresses. An IP address is a numerical label assigned to each device connected to a computer network that uses the Internet Protocol for communication. An IP address consists of four numbers (each ranging from 0 to 255) separated by periods.

## Summary

We will be explaining a regular expression that matches IPv4 addresses. The regex is:
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
This regex uses various regex components such as anchors, quantifiers, OR operator, character classes, and grouping and capturing to match the desired pattern.
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
| Character Class | Meaning |
| ----------- | ----------- |
| `a-z` | Match any letter within the range of lowercase a to lowercase z. |
| `0-9` | Match any number from 0 to 9. |
| `_` | Match literal underscores. |
| `\.` | Match literals dot (`.`).  Dots have special functions in regular expression.  The backslash (`\`) is used to escape the character. |
| `-` | Match literal hyphens. |
| `\d` | Match any digit from 0 to 9.  Effectively the same as using `0-9`. |
| `@` | Match literal at signs.  Found following the first parenthetical group in our email RegEx. |
### Anchors

The `^` and `$` anchors are used to match the start and end of the string respectively. In our regex, we want to ensure that the entire string matches the IP address pattern.

### Quantifiers

The `.` character matches any character except for newline. We use the `.` character followed by the quantifier `{3}` to match any three characters. 

### OR Operator

The `|` character is used as an OR operator to match different patterns. In our regex, we use it to match the range of values for each segment of the IP address.

### Character Classes

The `[0-9]` character class matches any single digit. We use this class to match each of the digits in an IP address.


### Grouping and Capturing

The `()` parentheses are used to group patterns together. We use them in our regex to group the different segments of the IP address. The `?:` is a non-capturing group that groups patterns together without capturing the matched text.

### Bracket Expressions

The `[]` brackets are used to match any single character in the specified range. We use this to match the range of values for each segment of the IP address.

### Greedy and Lazy Match

By default, regex matching is greedy, meaning it will match as much as possible. We use the `?` quantifier to make the matching lazy, meaning it will match as little as possible.

### Boundaries

In our regex, we use the `\b` boundary to ensure that the IP address is not part of a larger word.

### Back-references

Back-references are used to match the same text that was previously matched by a capturing group. We do not use back-references in our regex.

### Look-ahead and Look-behind

Look-ahead and look-behind assertions are used to match text based on what comes before or after it. We do not use look-ahead or look-behind assertions in our regex.

## Author

I'm Bulkacity, a software engineer and you can find more of my projects on [my GitHub profile](https://github.com/bulkacity).
