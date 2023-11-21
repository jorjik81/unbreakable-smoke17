# Title 
Matching an Email – /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Regular expressions, or regex, are tools in programming to find and manipulate text patterns, making tasks like validation and search efficient. They're crucial for text-related operations, enhancing precision and effectiveness in coding.

## Summary

 /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/.

Regular expression above is used to validate email addresses. It checks for the standard email format, ensuring that it begins with a combination of lowercase letters, numbers, underscores, dots, or  hyphens, followed by the "@" symbol. The domain part includes alphanumeric characters, dots, or hyphens, followed by a period and a top-level domain (TLD) with 2 to 6 letters.

Example within the code: 

const emailRegex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;

const isValidEmail = (email) => {
  return emailRegex.test(email);
};

// Example usage
const userEmail = "example@email.com";
if (isValidEmail(userEmail)) {
  console.log("Email is valid!");
} else {
  console.log("Invalid email format.");
}

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)



## Regex Components

### Anchors
'^': Asserts the start of the string.
'$': Asserts the end of the string.

### Quantifiers
'+': Matches one or more occurrences.

### Character Classes
\ - The backslash () is an escape character.It indicates that the dot should be treated as a literal character and not as a metacharacter. 
/ - The forward slashes at the beginning and end of the regex  mark the start and end of the regular expression pattern
([]) represents a range of characters we are matching, regardles the length of the string.
(-) used between alphanumeric characters (letters and numbers) and shows range of those possible characters
'[a-z0-9_\.-]: Matches any lowercase letter, digit, underscore, dot, or hyphen. Matching example: john_doe-123
([]+): + matches one or more occurrences of the characters within the square brackets.
'[\da-z\.-]: Matches any digit, lowercase letter, dot, or hyphen.
\d—Matches any Arabic numeral digit. example: e.9xample-mail
'[a-z\.]: Matches any lowercase letter or dot.
([a-z\.]{2,6}): The top-level domain (TLD) is limited to 2 to 6 lowercase letters. example: com.mm
the email with all allowed characters would look like this: john_doe-123@e.9xample-mail.com.mm"

### Grouping and Capturing
'(...)': Capturing groups for specific parts of the email address.

### Bracket Expressions
'[]': Bracket expression is a way to specify a set of characters. It's enclosed within square brackets

### Greedy and Lazy Match
'+': Greedy quantifier, matching one or more occurrences.

### Boundaries
'^': Asserts the start of the string.
' ': Asserts the end of the string.

## Author

Giorgi Jorjadze
Skills: JS, Express, Node, MySql, MongoDB, HTML, CSS

GitHub profile: https://github.com/jorjik81