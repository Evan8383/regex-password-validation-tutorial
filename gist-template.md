# Password Validation using Regex

Welcome to the world of regular expressions, or simply, regex! If you've ever felt the need to find, replace, or validate text patterns, regex is your go-to tool. This tutorial is your friendly guide to understanding a regex example to validate password inputs.

## Summary

Today we will be breaking down what looks to be a complicated regular express for validating a password. This regular expression checks the user supplied password for at least one digit, at least one lowercase character, at least on uppercase character, at least on special character, and at least 8 characters of length, but no more that 144.

Our password validation regular express(regex):
> /^(?=.*[a-z])(?=.*[A-Z])(?=.*[0-9])(?=.*[*.!@\$%^&()]).{8,144}$/g

Here is an example of a password that would satisfy the above regular express(regex):
> Abcdefg1*

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Character Classes](#character-classes)
- [Flags](#flags)

## Regex Components
Within our example we have the following components:
- Positive lookahead
- Dot
- Quantifier
- Character set
- Opening and Closing brackets
- Beginning and End anchors
- Flags

### Anchors
There are two anchors in our example expression.

In regular expressions, anchors are special characters that specify a position in the string where a match must occur. They do not consume characters in the string, but rather assert something about a position. There are two main types of anchors:

- ^ - The caret symbol ^ is the start-of-string anchor. It asserts that the following pattern must start at the beginning of the string. For example, the regex ^abc will match any string that starts with "abc".

- \$ - The dollar sign \$ is the end-of-string anchor. It states that the pattern must be at the end of the string to match. For example, the regex abc$ will match any string that ends with "abc".

Anchors are a powerful tool in regex, allowing you to specify not just what you want to match, but where within the string you want to match it.

### Quantifiers
Quantifiers in regex determine how many instances of a character, group, or character class must be included in the input for the string to match. Here are the main types of quantifiers found in our example:

- . - The Dot matches any character excluding line breaks.

- \* - The asterisk is used to specify "zero or more" of the next element. For example, in our example, .*[A-Z] would match "A", "AAA", etc., and even an empty string.

- ? - The question is used to specify "zero or one" of the next element. It makes the preceding element optional. For example, a? would match "a" and an empty string.

- {n} - Curly brackets are used to specify a specific number of occurrences. For example, a{3} would match exactly "aaa".

- {n,} - A number followed by a comma in curly brackets means "n or more" of the preceding element. For example, a{2,} would match "aa", "aaa", "aaaa", etc.

- {n,m} - Two numbers separated by a comma in curly brackets specify a range of occurrences. For example, a{2,3} would match "aa" and "aaa", but not "a" or "aaaa".

  This is what is used in our example. Our usage of the curly braces and two numbers separated by a comma indicates, the password must be at least 8 characters long, but not longer than 144 characters.

Quantifiers can be used with any character, character class, or grouping. They are a powerful tool in regex, allowing you to specify complex patterns with a simple syntax.

### Grouping Constructs

In our example, the grouping constructs are the parts within parentheses (). They are used here mainly for lookahead assertions. Let's break them down:

- (?=.[a-z]) - This is a positive lookahead assertion. It checks if there is at least one lowercase letter somewhere in the string. The . matches any character, and [a-z] matches any lowercase letter. So, (?=.[a-z]) ensures that the string contains at least one lowercase letter.

- (?=.[A-Z]) - This is another positive lookahead assertion. It checks if there is at least one uppercase letter somewhere in the string. Similarly, (?=.[A-Z]) ensures that the string contains at least one uppercase letter.

- (?=.[0-9]) - This positive lookahead assertion checks if there is at least one digit somewhere in the string. [0-9] matches any digit from 0 to 9. So, (?=.[0-9]) ensures that the string contains at least one digit.

- (?=.[*.!@\$%^&()]) - This positive lookahead assertion checks if there is at least one special character somewhere in the string. The characters *.!@\$%^&() inside the square brackets represent a set of special characters. So, (?=.[*.!@$%^&()]) ensures that the string contains at least one of these special characters.

The grouping constructs in this regex are used to assert that the string contains at least one lowercase letter, one uppercase letter, one digit, and one special character. The {8,144} outside the parentheses is a quantifier that asserts the string must be between 8 and 144 characters long. The ^ and $ are anchors that assert the start and end of the string, respectively. The /g at the end is a flag that allows the regex to match multiple occurrences of the pattern within the string.

### Character Classes

In regular expressions, character classes are defined inside square brackets [] and match any one character from the class.

In our example there are several character classes:

- [a-z] - This is a character class that matches any lowercase letter from 'a' to 'z'. It's used in the lookahead assertion (?=.[a-z]) to check that the string contains at least one lowercase letter.

- [A-Z] - This is a character class that matches any uppercase letter from 'A' to 'Z'. It's used in the lookahead assertion (?=.[A-Z]) to check that the string contains at least one uppercase letter.

- [0-9] - This is a character class that matches any digit from '0' to '9'. It's used in the lookahead assertion (?=.[0-9]) to check that the string contains at least one digit.

- [*.!@\$%^&()] - This is a character class that matches any of the special characters *.!@\$%^&(). It's used in the lookahead assertion (?=.[*.!@\$%^&()]) to check that the string contains at least one of these special characters.

So, in this regex, character classes are used to define sets of characters that the string must contain at least one of.

### Flags

In regular expressions, flags are single-letter codes that modify the behavior of the entire pattern. They are placed after the closing slash / of the pattern.

In our example there is one flag:

- g - This is the "global" flag. It means that the pattern will be tested against all possible matches in a string. Without the g flag, the regex will stop after the first match is found.

There are several other flags that can be used with Regular Express. However, this example with only cover the global flag (g)

In this regex, the g flag is used to ensure that the pattern is tested against the entire string, not just the first part of the string that matches the pattern.

## Author


Thank you for taking the time to read a little about password validation using Regular Expressions!

My name is Evan and im a networking engineer. Regular expressions have proven to be help in my day to day job along with helping me solve problems during my journey to learn how to code.

I hope this guide was helpful in understanding why certain sections of a regular expression are used!