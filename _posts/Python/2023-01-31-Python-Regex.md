---
title:  "Python Regex"
date:   2023-01-15 22:10:00 +0545
categories: [Python]
tags: [Regex]
---

RegEx Module  
Python has a built-in package called re, which can be used to work with Regular Expressions.

Import the re module:

```python
import re
```

## regex functions

The re module offers a set of functions that allows us to search a string for a match:

Function | Description
--- | ---
findall | Returns a list containing all matches
split | Returns a list where the string has been split at each match
search | Returns a Match object if there is a match anywhere in the string
sub | Replaces one or many matches with a string
--- | ---

## The findall() Function

The findall() function returns a list containing all matches.

Example  
Print a list of all matches:

```python
import re

txt = "We are the 'Vikings' from the north."
x = re.findall("the", txt)
print(x)
```

## The search() Function

The search() function searches the string for a match, and returns a Match object if there is a match.

If there is more than one match, only the first occurrence of the match will be returned:

Example  
Search for the position in the string:

```python
import re

txt = "We are the 'Vikings' from the north."
x = re.search("\'V", txt)
print("The position of the search string is:", x.start())
```

## The split() Function

The split() function returns a list where the string has been split at each match:

Example  
Split at each white-space character:

```python
import re

txt = "We are the 'Vikings' from the north."
x = re.split("\s", txt)
print(x)
```

## The sub() Function

The sub() function replaces the matches with the text of your choice:

Example  
Replace every white-space character with "_":

```python
import re

txt = "We are the 'Vikings' from the north."
x = re.sub("\s", "_", txt)
print(x)
```

## Meta Characters

Metacharacters are characters with a special meaning:

Character | Description
--- | ---
[] | A set of characters
\ | Signals a special sequence (can also be used to escape special characters)
. | Any character (except newline character)
^ | Starts with
$ | Ends with
\* | Zero or more occurrences
\+ | One or more occurrences
{} | Exactly the specified number of occurrences
\| | Either or
() | Capture and group

## Special Sequences

A special sequence is a \ followed by one of the characters in the list below, and has a special meaning:

Character | Description
--- | ---
\A | Returns a match if the specified characters are at the beginning of the string
\b | Returns a match where the specified characters are at the beginning or at the end of a word
\B | Returns a match where the specified characters are present, but NOT at the beginning (or at the end) of a word
\d | Returns a match where the string contains digits (numbers from 0-9)
\D | Returns a match where the string DOES NOT contain digits
\s | Returns a match where the string contains a white space character
\S | Returns a match where the string DOES NOT contain a white space character
\w | Returns a match where the string contains any word characters (characters from a to Z, digits from 0-9, and the underscore _ character)
\W | Returns a match where the string DOES NOT contain any word characters
\Z | Returns a match if the specified characters are at the end of the string

## Sets

A set is a set of characters inside a pair of square brackets [] with a special meaning:

Set | Description
--- | ---
[arn] | Returns a match where one of the specified characters (a, r, or n) are present
[a-n] | Returns a match for any lower case character, alphabetically between a and n
[^arn] | Returns a match for any character EXCEPT a, r, and n
[a-zA-Z] | Returns a match for any character alphabetically between a and z, lower case OR upper case
[+] | In sets, +, *, ., |, (), $,{} has no special meaning, so [+] means: return a match for any + character in the string
[0123] | Returns a match where any of the specified digits (0, 1, 2, or 3) are present
[0-9] | Returns a match for any digit between 0 and 9
\[0-5][0-9] | Returns a match for any two-digit numbers from 00 and 59
