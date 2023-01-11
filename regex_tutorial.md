# Regex Tutorial - Matching an Email

## Summary

A regular expression is a pattern used to match character combinations in text. The regex for matching an email address consists of several parts: the local part, which appears before the @ symbol and can contain uppercase letters, digits, period, underscore, percent sign, plus sign, or hyphen; the @ symbol; the domain part, which appears after the @ symbol and can contain uppercase letters, digits, period, or hyphen; and the top-level domain, which appears after the last period and can contain two or more uppercase letters.

## Table of Contents

- [Introduction](#introduction)
- [Matching the local part](#matching-the-local-part)
- [Matching the domain part](#matching-the-domain-part)
- [Putting it all together](#putting-it-all-together)
- [Conclusion](#conclusion)

## Introduction

The most basic form of an email address consists of a local part (the part before the @ symbol) and a domain part (the part after the @ symbol).

The below will be the regex that we shall explore further along this tutorial.

<img src="https://user-images.githubusercontent.com/108771904/211237699-bcc38da0-1739-4136-9232-9ba1e2837a54.png" width="630" height="170"/>

## Matching the local part

The local part of an email address can not only contain letters (upper and lower case), digits, and certain special characters (e.g. !, #, $, %, etc.) but can also contain dots (.), however, these cannot be consecutive or appear at the beginning or end of the local part.

Here is a regex that will match a local part:

<img src="https://user-images.githubusercontent.com/108771904/211238792-6d9df6d4-f767-4c12-9477-39b71dffc798.png" width="630" height="170"/>

This regex uses the following elements:

- [a-zA-Z0-9.!#$%&'*+/=?^_{|}~-]`: This character set includes all letters (upper and lower case), digits, and certain special characters.
- \*: The asterisk indicates that the preceding character or character set can be matched zero or more times.

## Matching the domain part

Similar to the local part, each label in the domain part can contain letters (upper and lower case), digits, hyphens (but not at the beginning or end) but not certain special characters.

The domain part must end with a top-level domain (TLD) such as .com, .net, .org, etc.

Here is a regex that will match a domain part:

<img src="https://user-images.githubusercontent.com/108771904/211238793-7b6e8920-1315-46a0-bd44-43b6aa9cccd0.png" width="630" height="170"/>

This regex uses the following elements:

- [a-zA-Z0-9]: This character set includes all letters (upper and lower case) and digits.
- (?:[a-zA-Z0-9]: This is a non-capturing group that matches a label. The label can contain letters (upper and lower case), digits, and hyphens, but the hyphen cannot appear at the beginning or end.

## Putting it all together

Now that we have regex patterns for matching the local part and the domain part of an email address, we can combine them to create a regex that will match a complete email address.

## Conclusion

We learned about the different parts of an email address and how to match each part using a regex.

We also learned about some common regex elements, such as anchors, character sets, and special characters.

I hope you found this tutorial helpful and please see below for my contact information.

## Author

Author: Gareth Kwan

Github: [Link Here ](https://github.com/Gareth-Kwan)

Github Repo: [Link Here ](https://github.com/Gareth-Kwan/regex-tutorial)

Github Gist: [Link Here ](https://gist.github.com/Gareth-Kwan/fed53d9f71c772e3cdb07ff89f58946e)
