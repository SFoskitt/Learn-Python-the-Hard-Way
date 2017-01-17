#Exercise 22#

This is what we're told to do in this exercise:

_First, go back through every exercise you have done so far and write down every word and symbol (another name for "character") that you have used. Make sure your list of symbols is complete._

_Next to each word or symbol, write its name and what it does. If you can't find a name for a symbol in this book, then look for it online. If you do not know what a word or symbol does, then read about it again and try using it in some code._


enter `python` in the terminal to open the Python shell

enter `quit()` to exit the Python shell

enter `python <filename>.py` to run a Python script

`ls` in the terminal to list the files in the directory

`cd` in the terminal to change the directory

Atom is a recommended text editor (but I really like Sublime)

`print` in the script produces output in the terminal (at this point we only give it strings)

octothorpe character `#` prefixes a commented line

Math symbols
============

    `+` plus -- in a math expression, this adds (in strings this concatenates)
    `-` minus -- subtract
    `/` slash -- division
    `*` asterisk -- multiplication
    `%` percent -- in a math expression, this is modulus (returns the remainder value of an expression)
    `<` less-than -- for comparison expressions
    `>` greater-than -- for comparison expressions
    `<=` less-than-equal -- for comparison expressions
    `>=` greater-than-equal -- for comparison expressions
    

comma `,` separator used after the print expression to follow it with something else that will be printed

`Traceback` is the start of most errors - this points to the place in the script where an error occurred

any number that contains a decimal of any length is called a "floating point" - otherwise numbers are type "integer"

`%s` `%r` `%d` are string formatters - these act like variables to stand in place of a list of replacement values at the end of a string -- `%r` is best for debugging, where the "r" here stands for (roughly) raw
```
print "If I add %d, %d, and %d I get %d." % (
    my_age, my_height, my_weight, my_age + my_height + my_weight)
```

`print "." * 10` will print the period character ten times in a row

`round()` will round a floating point number

string formatters can reside in a variable (DRY) to be used later, ex:
```
formatter = "%r %r %r %r"

print formatter % (1, 2, 3, 4)
print formatter % ("one", "two", "three", "four")
```

`True` and `False` are boolean values, not strings, so these are expressed without quotation marks

`\n` prints a new line 

`"""` or  `'''` (triple quotes - single or double) at the beginning and end of a block of text to make a long string 

`\` is the back slash - outside of a math expression, this is used in strings as an escape character which tells Python to ignore the character which follows - there are a number of escape sequences

_This table is lifted directly from the book and is not my original work_

| Escape sequence | What it does                |
|-----------------|-----------------------------|
|`\\`             | escape the backslash        |
| `\'`            | escape the single quote     |
| `\"`            | escape the double quote     |
| `\a`            | ASCII bell (BEL)            |  <--- I don't know what this one is yet
| `\b`            | ASCII backspace (BS)        |
| `\f`            | ASCII form feed (FF)        |
| `\n`            | ASCII line feed (LF)        |
| `\N{name}`      | Named for unicode database  | <--- I don't know what this one is yet
| `\r`            | Carriage return (CR)        |
| `\t`            | Tab (TAB)                   |
| `\uxxxx`        | Character with 16-bit value |
| `\uxxxxxxxx`    | Character with 32-bit value |
| `\v`            | ASCII vertical tab (VT)     |
| `\ooo`          | Char with octal value ooo   |
| `\xhh`          | Char with hex value         |
_________________________________________________


