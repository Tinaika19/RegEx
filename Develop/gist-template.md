# Title (Matching an Email)

This tutorial breaks down a regular expression (regex) used to match email addresses. Regex is a powerful tool for validating text, and this pattern ensures the input follows the correct format for a valid email address.


## Summary

This regular expression is used to validate email addresses. It ensures that the input follows the correct format for a valid email address, including a local part (before the @), a domain name (after the @), and a domain extension (like .com or .org).

## Table of Contents

- [Anchors](#anchors)
- [Local Part](#LocalPart)
- [Domain name](#Domainname)
- [Dot and Domain Extension](#DotandDomainExtension)
- [Valid Examples](#ValidExamples)
- [Author](#Author)



## Regex Components

### Anchors
 - `^` asserts the start of the string.
 - `$` asserts the end of the string.
   These ensure that the entire string is an email address without any extra characters before or after.

### Local Part
  - `[a-z0-9_\.-]+`: Matches the local part of the email (the part before the `@`).
  - `[a-z0-9]`: Matches any lowercase letter (`a-z`) or digit (`0-9`).
  - `_`: Matches an underscore (`_`).
  - `\.`: Matches a literal dot (`.`).
  - `-`: Matches a hyphen (`-`).
  - The `+` quantifier ensures one or more characters from this set.

### Domain name
   - `[\da-z\.-]+`: Matches the domain part after the `@`.
   - `\d`: Matches any digit (`0-9`).
   - `[a-z]`: Matches any lowercase letter (`a-z`).
   - `\.`: Matches a literal dot (`.`).
   - `-`: Matches a hyphen (`-`).

### Dot and Domain Extension
 - `\.` matches the literal dot before the domain extension.
 - `[a-z\.]{2,6}` matches the domain extension, ensuring it has between 2 and 6 characters (e.g., `.com`, `.org`, `.co.uk`).


### Valid Examples:

- `john.doe@example.com`
- `user_name123@mail-server.net`
- `jane-doe@123mail.co.uk`

## Author

This tutorial was created by Tinaika Pereira. I am passionate about web development and enjoy creating content on regex. You can find more of my work on my [GitHub profile](https://github.com/Tinaika19).
