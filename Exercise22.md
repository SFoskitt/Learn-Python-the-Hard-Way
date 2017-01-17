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

`%s` `%r` `%d` are string formatters - these act like variables to stand in place of a list of replacement values at the end of a string
```
print "If I add %d, %d, and %d I get %d." % (
    my_age, my_height, my_weight, my_age + my_height + my_weight)
```
    
