# Hex Value RegEx Tutorial

A brief explanation of regex (regular expression) for hex values

## Summary

For starters, what is a hexadecimal code (hex code)? A hexadecimal code is actually a number system made up of 16 symbols. Those 16 symbols sometimes go by the name, base-16. These codes are very popular and one way that they can be used is in web development! CSS can utilize the power of hex codes to render the color of your choosing with numbers and letters (symbols), rather than typing out the name of the color completely. The shortened number of values needed really make hex codes easy and efficient to use.

So what goes makes a hex value? Well they start with these basic components:

1. "#" symbol at the beginning
2. Next are any letters a-f, A-F, and/or digits 0-9.
3. There needs to be only 6 or 3 letters and/or numbers in this type of code.

Here's an example of the regex for a hex value:

`/^#?([a-fA-F0-9]{6}|[a-fA-F0-9]{3})$/`

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

Components in regex are all of the symbols that make up that epression. We'll be breaking down the hex regex from above.

### Anchors

Here'a the expression again: `/^#?([a-fA-F0-9]{6}|[a-fA-F0-9]{3})$/`

The anchors are `/^` & `$/`. These characters must be at the beginning and end of a string as you see it and cannot change their posititions in the hex expression.

The `^` is an assertion . That assertion basically says, "Whatever comes after me is final!". Any wrong declaration after the `^` will give an incorrect result of whatever it is you’re trying to match. In the hex regex the `/^` is requiring a `#` to follow it.

The next anchor, `$/`, has the assertion `$`. This requires whatever is placed before it. That means that the required symbol before `$/` is `)` in our hex regex snippet.

### Quantifiers

A quantifier lets us know how many characters can be used in the expression. In our hex regex snippet, `{}` are the qauntifiers and the value inside is the parameter that needs to be met. `[a-fA-F0-9]{6}`means 6 characters are required or `[a-fA-F0-9]{3}`means 3 characters are required.

### Character Classes

Character classes are represented by `a-f0-9`. This means that at least 1 character will need to be any letter between a and f or any digit between 0 and 9.

### OR Operator

The `|` is an OR Operator that determines the character classes and grouping constructs within Bracket Expressions.

The hex regex snippet, `/^#?([a-fA-F0-9]{6}|[a-fA-F0-9]{3})$/`, will allow either 6 OR 3 characters to match `[a-fA-F0-9]`, after the`#`. (ex: #dA5)

### Bracket Expressions

Bracket Expressions are these `[]`. Bracket expressions contain the allowed characters, character classes, and/or expressions to help match whatever the hex expression is looking for. This means that `[a-fA-F0-9]` is looking for a secific combination of the following `[abcdefABCDEF0123456789]`

### Grouping and Capturing

The `()` are a grouping construct that captures whatever it is we're trying to match within it. It makes the values one unit so that the match is exact.

### Flags

Flags can be used to limit the functionality of a regex. Here are example of some flags: `d, g, i, m, s, u, y`

## Author

Hi, I'm Christa, an aspiring email an UI developer making my way through learning backend frameworks like MySQL and MongoDB 😅, while deepening my love for HTML and CSS. Check out my projects here: https://github.com/cnewing
