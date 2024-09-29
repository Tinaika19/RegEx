# Title (Matching an Email)

This tutorial breaks down a regular expression (regex) used to match email addresses. Regex is a powerful tool for validating text, and this pattern ensures the input follows the correct format for a valid email address.


## Summary

This regular expression is used to validate email addresses. It ensures that the input follows the correct format for a valid email address, including a local part (before the @), a domain name (after the @), and a domain extension (like .com or .org).

## Table of Contents

- [Anchors](#anchors)
- [Local Part](#LocalPart)
- [Domain name](#Domainname)
- [The @ symbol](#The@symbol)
- [Dot and Domain Extension](#DotandDomainExtension)
- [Valid Examples](#ValidExamples)
- [Author](#Author)



## Regex Components

### Anchors
- ^: This is the start anchor, meaning that the pattern should match from the very beginning of the string. It ensures that nothing comes before the start of the email.
- $: This is the end anchor, which ensures that the match goes all the way to the end of the string. Nothing can appear after the email address.
Together, ^ and $ ensure that the entire string is evaluated as an email address and prevent extra characters from being included before or after.

### Local Part
The local part is the section of the email address before the @ symbol. This regex pattern handles typical characters allowed in an email's local part:
  - `[a-z0-9_\.-]+`: Matches the local part of the email (the part before the `@`).
  - `[a-z0-9]`: Matches any lowercase letter (`a-z`) or digit (`0-9`).
  - `_`: Matches an underscore (`_`).
  - `\.`: Matches a literal dot (`.`).
  - `-`: Matches a hyphen (`-`).
  - The `+` quantifier ensures one or more characters from this set.

### Domain name
The domain name is the section of the email address after the @ symbol and before the domain extension (e.g., example in example.com). This pattern allows domain names with valid characters:
   - `[\da-z\.-]+`: Matches the domain part after the `@`.
   - `\d`: Matches any digit (`0-9`).
   - `[a-z]`: Matches any lowercase letter (`a-z`).
   - `\.`: Matches a literal dot (`.`).
   - `-`: Matches a hyphen (`-`).
### The @ symbol
This is the literal at-symbol (@), which separates the local part of the email from the domain part. Every valid email must contain exactly one @ symbol.

### Dot and Domain Extension
 - `\.` matches the literal dot before the domain extension.
 - `[a-z\.]{2,6}` matches the domain extension, ensuring it has between 2 and 6 characters (e.g., `.com`, `.org`, `.co.uk`).


### Valid Examples:

- `john.doe@example.com`
- `user_name123@mail-server.net`
- `jane-doe@123mail.co.uk`

### Full Pattern Examples
Consider the email address john.doe@example.com:

- **Local Part:** john.doe
- **Lowercase letters** (john), a dot (.), and lowercase letters (doe).
- **@ Symbol:** Separates the local part and the domain part.
- **Domain Part:** example
- **Lowercase letters** (example).
- **Dot:** A literal dot (.).
- **Domain Extension:** com
- **Lowercase letters** (com), and the length (3 characters) is valid.
This email matches the regex fully.

## Author

This tutorial was created by Tinaika Pereira. I am passionate about web development and enjoy creating content on regex. You can find more of my work on my [GitHub profile](https://github.com/Tinaika19).
