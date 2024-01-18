# Title Password Validation Regex

Welcome to the world of regular expressions, or simply, regex! If you've ever felt the need to find, replace, or validate text patterns, regex is your go-to tool. This tutorial is your friendly guide to understanding a regex example to validate password inputs.

## Summary

Today we will be breaking down what looks to be a complicated regular express for validating a password. This regular expression checks the user supplied password for at least one digit, at least one lowercase character, at least on uppercase character, at least on special character, and at least 8 characters of length, but no more that 144.

Our password validation regular express(regex):
> /^(?=.*[a-z])(?=.*[A-Z])(?=.*[0-9])(?=.*[*.!@$%^&()]).{8,144}$/g

Here is an example of a password that would satisfy the above regular express(regex):
> Abcdefg1*

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

### Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
