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
Quantifiers in this regex use the '+' operator which you will use to connect the user's email info and domain. Another quantifier is the {n,n} you can use this operator to match n or more times. in the above quantifier on line 3 will allow a match range of 2-6 characters for [a-z\.].

Example:
let str = 'ECMAScript 2020';
let re = /\d{4}/;
let result = str.match(re);
console.log(result);
This will output ["2020"] this is the same as /\d\d\d\d/
### Grouping Constructs
Capturing groups are a way to treat multiple characters as a single unit. The first grouping in this regex is ([a-z0-9_\.-]+). This matches the user's info. The second grouping in the above regex is ([\da-z\.-]+) which is whatever email platform you wish to use so its watching for a digit 0-9 and the characters a-z. The last grouping is ([a-z\.]{2,6}) to match the 
### Bracket Expressions
Bracket expressions for email matching include the characters [a-z0-9_\.-]. What this expression is doing is matching any letter from a-z and matches any number from 0-9, this is case sensitive and will only detect lowercase letters. The [\da-z\.-] is matching a single digit that is 0-9 and the character set a-z that is lowercase. The last bracket is [a-z\.] which is watch for the domain name, such as .net, .com, or .org.
### Character Classes
The character class in this regex is \d, which matches a single character digit from [0-9]. It will only pick up single digits and not multiple digits such as '17', '186', '1234515' only '1'.
## Author
My name is Tyler Zeman I am a 23 year old Full Stack developement student taking classes with the UofM's Full Stack Flex Web devlopment for the summer. The bootcamp has opened my eyes to what it takes to build a full-stack app. I have built a few so far and look forward to building many more and adding to my knowledge to making it more robust. If interested here's a link to my github: https://github.com/tylerzeman