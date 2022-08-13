# Match An Email - A regular Expression Tutorial

This regex tutorial will explain the use to match emails using the expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. 

## Summary

This tutorial hopes to help you walkthrough Email Matching Regular Expression. A regular expression or in short regex refer to encdoded strings created to match patterns with exact strings created.These regex patterns can be as simple as finding an exact match for a string or even as complex as looking for a string following a certain ruleset. To understand Email Matching is to understand the parts of an email. An email is seperated by two parts the info in the 1st half seperated by an @ symbol. The second half is the domain name, this can be .com, .net, .org. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

Some of the anchors in this expression are '^', the Caret Anchor matches the beginning of the text. The '$' is the classified as the Dollar Anchor, which matches the end of the text. The '^' and '$' are used in single line mode, In the single line mode these anchors watch for matches in the beginning and the end of a string. To enable multiline mode, you need to use the 'm' flag. Now in multiline mode you can now use the caret and dollar sign anchors to match on multiple lines.

Example:
let str = 'JavaScript';
console.log(/^J/.test(str));
This will output true because of the caret anchor checking to see if the beginning of the string is a J following the caret anchor.

let str = 'JavaScript';
console.log(/t$/.test(str));
This will output true because the dollar anchor sign is watching the end of string which in this case is the character T.

let str = `1st line
2nd line
3rd line`;
let re = /^\d/g;
let matches = str.match(re);
console.log(matches);
This example will return the 1st digit of the multiline string.
### Quantifiers
Quantifiers in this regex use the '+' operator which you will use to connect the user's email info and domain. Another quantifier is the {n,n} you can use this operator to match n or more times.
### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
