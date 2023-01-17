# Title (replace with your title)
Regex Matching an E-mail Address

## Summary
A regular expression, or regex, for matching email addresses is a pattern used to search for and match specific sequences of characters in a string.

A common regex for matching email addresses is one that checks for the presence of the following elements:

A word character or digit, which begins the local part of the email address, followed by any number of word characters, digits, dots, or dashes
The at symbol (@)
A word character, which begins the domain part of the email address, followed by any number of word characters or dots
A dot (.)
A word character, which specifies the top-level domain (TLD) of the email address, such as .com, .edu, .gov, etc.
The regex will look like /^[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}$/



## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Special Characters](#special-characters)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components
A regular expression for matching email addresses typically includes several different components, which are used to search for and match specific sequences of characters in a string. These components include:

Character classes
Quantifiers
Special characters
Anchors
Grouping Constructs
The OR operator
Flags
Character Escapes

An example of a regex that uses many of these components to match email address: /^[A-Z0-9._%+-]+@[A-Z0-9.-]+\.(com|edu|gov)$/i

### Anchors
Two common anchors used in a regex for matching email addresses are the ^ (caret) and $ (dollar sign) characters.

The ^ character, when placed at the beginning of a regex, is called the "start of line" anchor. It matches the position at the beginning of the string being searched. This anchor is used to ensure that the email address starts at the beginning of the string and does not have any leading whitespace or other characters.

The $ character, when placed at the end of a regex, is called the "end of line" anchor. It matches the position at the end of the string being searched. This anchor is used to ensure that the email address ends at the end of the string and does not have any trailing whitespace or other characters.

For example, in the regex /^[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}$/i the ^ and $ are used to indicate that the email must start at the beginning of the line and end at the end of the line, respectively.

### Quantifiers
These are used to specify how many times a character or group of characters can be matched. For example, + means one or more times. This can be used to match one or more characters from a character class.

### Special characters
These are used to specify certain types of characters that can be matched. For example, @ is used to match the at symbol that separates the local part from the domain part of the email address. Similarly, . (dot) is used to match the dot that separates the domain name from the top-level domain (TLD) of the email address.

### Grouping Constructs
These are used to group different parts of the regex together. For example, ( ) (parentheses) are used to group characters together and apply a quantifier to the entire group.

### Bracket Expressions
 These are also known as character classes. They are used to specify a set of characters that can be matched.

For example, in the regex /^[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}$/i, the brackets [] enclose a set of characters that can be matched in the local part of the email address, which is the part before the @ symbol. The character class [A-Z0-9._%+-] matches any uppercase letter, digit, dot, underscore, percent, plus, or hyphen.

Similarly, in the same regex, the character class [A-Z0-9.-] matches any uppercase letter, digit, dot, or hyphen in the domain part of the email address, which is the part after the @ symbol.

Bracket expressions can also be used to specify a range of characters to match. For example, [a-z] matches any lowercase letter, and [0-9] matches any digit.

It's important to note that bracket expressions are case sensitive, so [a-z] matches only lowercase letters and [A-Z] matches only uppercase letters. To match both case, you can use [a-zA-Z]


### Character Classes
These are used to specify a set of characters that can be matched. In a regex for matching email addresses, character classes are often used to specify the characters that can be used in the local part and domain part of the email address. For example, [A-Z0-9._%+-] matches any uppercase letter, digit, dot, underscore, percent, plus, or hyphen.

### The OR Operator
This is used to match one of several different patterns. For example, | (pipe) is used to match one of several different top-level domains (TLDs) such as .com, .edu, .gov.

### Flags
The most common flag used in an email matching regex is:

i (ignore case): This flag makes the regex case-insensitive. It allows the regex to match both uppercase and lowercase letters without having to specify both in the character class. So, for example, the character class [A-Z] would match both uppercase "A" and lowercase "a" when the i flag is used.

### Character Escapes
In regular expressions, certain characters have special meaning and need to be escaped in order to match them literally. The most common characters that are escaped in an email matching regex are:

. (dot): The dot is a special character that matches any character except a newline. In an email matching regex, the dot is used to match the dot that separates the domain name from the top-level domain (TLD) of the email address. If you want to match a literal dot, you must escape it with a backslash \.

+ (plus): The plus is a special character that matches one or more of the preceding character. It's used in the local part of the email address, to match one or more of the characters specified in the character class.

* (asterisk): The asterisk is a special character that matches zero or more of the preceding character. It's not used in the usual email matching regex.

? (question mark): The question mark is a special character that matches zero or one of the preceding character. It's not used in the usual email matching regex.

$ (dollar sign): The dollar sign is a special character that matches the end of the line. It's used as an anchor in the email matching regex to match the end of the line.

^ (caret): The caret is a special character that matches the start of the line. It's used as an anchor in the email matching regex to match the start of the line.

{} (curly brackets): The curly brackets are special characters that specify a range of possible repetitions of the preceding character or group. It's used in the TLD part of the email address to match the TLD with a specific length.

[] (square brackets): The square brackets are special characters that specify a set of characters that can be matched. It's used in the local and domain parts of the email address to match specific set of characters.

() (parentheses): The parentheses are special characters that group characters together and apply a quantifier to the entire group. It's not used in the usual email matching regex.

\ (backslash): The backslash is used to escape special characters so that they are treated as literal characters. For example, \. matches a literal dot, instead of any character.

An example of a regex that uses many of these characters: /^[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}$/i

## Author
Michael Corbo is the author of this particular tutorial.
Github = http://github.com/mrcorbo
Email = michaelrcorbo@gmail.com