# How 2 Regex

Howdy, Pardner. Do you know what Regex is? No? Well that's okay, because you're gonna learn today, hombre. Let's get it!

## Summary

Regex expressions are a text processing system that use a special pattern system for notation. This gives programmers the means to easily process and validate strings using the Don't Repeat Yourself principle. Regex can be used for many different languages.

For this tutoria we will be using a regular expression to match a Hex Value

Our example is:
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

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
The Anchors are used to start and end a string or expression. These set where the search parameters begin and end.

Caret `^` begins the expression and the Dollar sign `$` ends the expression

So in our example we would be looking at `/^`#?([a-f0-9]{6}|[a-f0-9]{3})`$/`

### Quantifiers

/^#`?`([a-f0-9]`{6}`|[a-f0-9]`{3}`)$/

Quantifiers are used in regex to determine how many characters are expected. They specify how many instances of a character, group or character class must be present in the input for the match to be found. Quantifiers are greedy by default, so they will match as many characters as possible. In the context of this hex value matcher, it uses `{6}` to find the full Hex format such as (#00A3E0) or the shorthand form with `{3}` where it would read something like (#09F)

### OR Operator

/^#?([a-f0-9]{6}`|`[a-f0-9]{3})$/

OR operators are operators within the expression that is defined with `|`. The OR operator is essentially a boolean so in 

The OR operator behaves simlarly to a boolean. In our sample regex, it's essentially saying the hex value could be 6 characters with `[a-f0-9]{6}` or 3 characters with `[a-f0-9]{3}`

### Character Classes

Character classes is where you tell the engine to match out of several characters by closing them in brackets so for an example we want the option of `map` or `mop` to match so you would use m[ao]p to make them both match. 

### Flags

Flags are used to change how the expression is interpreted. 
Regex is not implemented in the sample code we are using but to cover this we will break down the flags that a `/`

 * `/i` is  for ignoring the case

 * `/g` is Global search which allows for matching all the instances within a string that follow the guidelines set

 * `/m` would be for multiline which will search line by line rather than searching through a string as a whole


### Grouping and Capturing
To show off grouping and capturing we'll be using an expression for matching an email:
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

The usage of 
### Bracket Expressions

/^#?(`[a-f0-9]`{6}|`[a-f0-9]`{3})$/

Bracket expressions signified by`[]` are used as guidelines for matching.This means in our expression any letter from `a` to `f` and numbers from `0` to `9` are valid to use for matching. 



### Greedy and Lazy Match

/^#`?`([a-f0-9]{6}|[a-f0-9]{3})$/

Greedy and lazy matches that are meant to make matches with different approaches. Greedy matches are a match that attempt to match an element as many times as possible. Lazy matches on the other hand are used to find the shortest possible string

In the context of our sample expression, a greedy match is used to match as many of the characters in the hex value as possible. Normally expressions are greedy by default but can be made lazy with the `?` character


### Boundaries
`\b` makes it so you match on a word boundary. Which means 

### Back-references

Back-references match the text that's been previously matched by a capturing group. 

### Look-ahead and Look-behind

Collectively referred to as "lookaround," Look-Ahead and Look-behind are zero-length assertions that made positive or negative

    *`(?=ABC123)` is an example of postive lookahead meaning it matches a group after the main expression without it including the result

    *`(?!ABC)` is a negative lookahead

    *(?<=ABC>) is an example of postive lookbehind 

    *(?<!ABC) is a negative lookbehind 
## Author
Ryan Jackson

Github: https://github.com/JimothyThunderguns


