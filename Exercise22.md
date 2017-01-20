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
    

comma `,` separator used after the `print` expression to follow it with something else that will be printed - use this to `print` the things on the same line - otherwise use a new call to `print` to accomplish on new line

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


`raw_input()` pauses the Python script to accept user input, and passes the entered value to any assigned value

wrap the `raw_input()` call as an argument to `int()` to parse the input into integer - this is safer alternative to `input()` method which is insecure because it will attempt to run the input text as Python script

passing a string to `raw_input()` method will use the string as the prompt - this is a shortcut method to use instead of prefixing `raw_input()` with a `print` call

`pydoc` followed by the name of a Python built-in method (for instance `print`) opens the documentation for that method - use `q` to exit from this

`from x import y` is how we get external modules/features for use in the scripts

`argv` is a feature of `sys` module that allows us to accept multiple arguments when running Python scripts, ex:
`python ex22.py thing1 thing2 thing3`  where inside script ex22.py the arguments will be assigned to variables as:
`script, var1, var2, var3 = argv` and `script` is the name of the script, ex22.py here, and is a gimme which comes with `argv`
number of arguments and variables must match

`open()` method creates a file stream object which must be assigned to a variable, and which comes with several methods like `read` such as `txt = open(filename)` then later `print txt.read()` - close the file stream with `close()`

These are also filestream commands, and I copied/pasted them directly from the book:
`close()` -- Closes the file. Like File->Save.. in your editor.
`read()` -- Reads the contents of the file. You can assign the result to a variable.
`readline()` -- Reads just one line of a text file.
`truncate()` -- Empties the file. Watch out if you care about the file.
`write('stuff')` -- Writes "stuff" to the file.
`seek()` -- Move virtual cursor to some point in the file.

pass the 'w' as a parameter to the `open()` method of filestream to open the file in "write" mode or 'r' for "read" mode or 'a' for "append" mode - default is 'r' "read" mode

`os.path`
`exists`
another import to use: `from os.path import exists` which tests whether a file exists or not, ex: `ans = exists(filename)` and will return Boolean type

`echo`
`cat`
new Python commands to use at the terminal promopt (not the shell prompt): `echo` and `cat` where `echo` takes a string argument and outputs the text - either straight back to the terminal like a parrot, or piped to a file as `echo "this string" > test.txt` and `cat` takes a file name and outputs the content

`man` provides the documentation to a Python command, ex: `man echo` will open the pydoc for the `echo` command

`len()` returns the length of a string passed to it, ex: `len('answer')` will return 6

`def` used to define a function, ex: `def this_function():` defines the function called "this_function"

the line which starts `def` must end with a colon `:`

function names (like variable names) are not camelCased but snake_case

`*args` is an argument container similar to `argv` but for use in functions, ex: `def some_fun(*args):` but are unpacked as `arg1, arg2 = args` NOT `arg1, arg2 = *args`

many different ways to call a function (Exercise 19)

`return` passes something back to the calling script/method/function - anything that can be assigned with `=` can be passed back woth `return`
