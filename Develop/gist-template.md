# Title (Breaking Down A Hex Value Regex)

This guide will help clarify the regex pattern used to validate hexadecimal color code values. The regex '/^#?([a-f0-9]{6}|[a-f0-9]{3})$/' is used in web design applications to assist with styling. After reviewing this regex tutorial you'll understand the patterns role in web development. 

## Summary

We will break down the the regex pattern to reveal how the expression distinguishes six-digit and three-digit hex codes, which is essential in website aesthetics. Here is the expression: '/^#?([a-f0-9]{6}|[a-f0-9]{3})$/'. 

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

- The '^' anchor is placed at the very beginning of the regex pattern.
- Its role is to assert that any match must begin at the start of the string.
- This means that the regex engine will not look for a match in the middle or at the end of the string; it will only consider a match valid if it starts from the beginning.

### Quantifiers

- '?','{6}', & '{3}' these are the quantifiers.
- '?' this is applied to the '#' character which means that the '#' can appear or not appear in the beginning of the hex code. 
- '{6}' & '{3}' the preceding hexadecimal characters must appear exactly 6 or 3 times. 

### OR Operator

- '|' this is a pipe which acts as an OR operator. 
- This makes the pattern versatile in the since that it allows the regex to match either six or three hexadecimal characters. 

### Character Classes

- The character classes are defined in the square brackets '[]'. 
- '[a-f0-9]' this is the chracter class that is used. When the combined they math any single hexadecimal character. 
- 'a-f' is the range of lowercase letters. 'a' represents 10 in decimal and 'f' represents 15 in decimal, which covers the whole range of possible values in a single hexadecimal digit. 
- '0-9' is the range of numbers from '0' to '9'. This will cover the numerical portion of the hexadecimal digits. 

### Flags

- There are no flags in this regex, however that means that this expression operates in a case-sensitive mode matching only the lower-case characters 'a-f'. 
- This also means that the anchors are the start and end of the expression not individual lines.

### Grouping and Capturing

- The parentheses '()' creates a group within the regex and captures the part of the string that matches the group for later use. 
- Grouping is useful when applying quantifiers to a sequence of characters or when using alternation, which is '|' in this case, to match more than one pattern. 
- The parenthesis capture the matched hex value being either 6 or 3 hexadecimal characters. 

### Bracket Expressions

- The bracket expression in my regex is explained in my (#character-classes) section. 
- Going into further details, on my bracket expression in the regex, it is used in an efficient manner to include all valid characters for a hexadecimal digit. 
- These bracket expressions are used to provide felxibility in specifying a range of characters to match. 
- This is crucial for accurately validating hexadecimal numbers. 

### Greedy and Lazy Match

- Greedy matches try to match as much of the string as possible while still conforming to the regex pattern. 
- Lazy matches match as little of the string as possible. 
- This regex pattern does not apply a greedy or lazy match neccesarily. 

### Boundaries

- The anchor characters are the boundaries for the regex. It defines both the beginning and the end of the expression. 
- The start of the string anchor '^' asserts that the match must start at the beginning of the string. 
- The end of the string anchor '$' asserts that the match must occur at the end of the string. 

### Back-references

- There are no back references in this regex pattern. 
- However, the use of back references reuse part of the match from an earlier capturing group, and can help identify repeated or mirrored patterns within a string. 

### Look-ahead and Look-behind

- There is no use for look-ahead and look-behind assertions in this regex.
- If we were to add a look-ahead assertion to the pattern it might be used to match a hex value only if it's followed by a specified pattern or character, without including the pattern/character in the match. 
- A look-behind assertion may be used if the hax value needed to be perceded dy a specific pattern for the match to be validated. 

## Author

I am currently new to the world of programming, and figured that one of the best ways to learn an expression is to try and teach it, so thank you for viewing this gist and see more of my projects at https://github.com/J-Ross01. 

## Sources
- https://stackoverflow.com/questions/9221362/regular-expression-for-a-hexadecimal-number
- https://medium.com/@harmoniacodes/using-regular-expressions-to-check-for-valid-hex-values-672eb089b5b0
- https://www.geeksforgeeks.org/how-to-validate-hexadecimal-color-code-using-regular-expression/
- https://www.youtube.com/watch?v=7DG3kCDx53c