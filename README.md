# Learn-Python-the-Hard-Way
My notes and maybe some exercises to follow along with the e-book "Learn Python the Hard Way" by Zed Shaw.  Added here for 100 Days of Code.

=======================

@(WWC - Learn Python the Hard Way)

###Exercise 0 - Setup
* Author does NOT recommend setting up IDLE
* Author does NOT recommend Python 3.0
* Instruction for setting up Python on Windows and Mac and Linux are extensive
* Author offers tips for finding answers to coding questions on Google
* Some tips for navigating directories from inside a terminal

###Exercise 1 - A Good First Program

file ex1.py contains:
```
print "Hello World!"
print "Hello Again"
print "I like typing this."
print "This is fun."
print 'Yay! Printing.'
print "I'd much rather you 'not'."
print 'I "said" do not touch this.'
```

run this script by typing this in the terminal:
	```python ex1.py```

This exercises focuses on showing the relationship between the text editor and the terminal - what is typed in the file and what comes out at the end.  

:# is called "octothorpe" for some reason


###Exercise 2 - Comments and Pound Characters

Comments are important to all programs for:
* purposes of documenting what we're doing in the program, as explanation and as way-points
* debugging so coder can eliminate lines to find the source of a problem

ex2.py is:

```
# A comment, this is so you can read your program later.
# Anything after the # is ignored by python.

print "I could have code like this." # and the comment after is ignored

# You can also use a comment to "disable" or comment out a piece of code:
# print "This won't run."

print "This will run."
```

In this chapter, the author recommends a debugging technique - read the code backwards.  I've done this and it's especially helpful when you've been looking at the same lines for a while and getting nothing new out of them.  Reading them backwards helps by forcing your brain to focus on little parts at a time, rather than skimming the whole.


###Exercise 3 - Numbers and Math

Math and math symbols:
```
+ plus
- minus
/ slash
* asterisk
% percent
< less-than
> greater-than
<= less-than-equal
>= greater-than-equal
```

ex3.py:
```
print "I will now count my chickens:"

print "Hens", 25 + 30 / 6
print "Roosters", 100 - 25 * 3 % 4

print "Now I will count the eggs:"

print 3 + 2 + 1 - 5 + 4 % 2 - 1 / 4 + 6

print "Is it true that 3 + 2 < 5 - 7?"

print 3 + 2 < 5 - 7

print "What is 3 + 2?", 3 + 2
print "What is 5 - 7?", 5 - 7

print "Oh, that's why it's False."

print "How about some more."

print "Is it greater?", 5 > -2
print "Is it greater or equal?", 5 >= -2
print "Is it less or equal?", 5 <= -2
```

The script does not produce fractions, despite the division above because ```int``` is the default type when doing some math without variables.  

Division in this way rounds down the result (rather than return a fraction).  

To get the math to work out correctly, it's necessary to assign the math to variables of type ```float```  

Floating types are assigned automatically when a variable is given a number with a decimal.

In this context, the ```%``` is called "modulus" and not percent - it does not calculate the percent of a number, it returns the remainder of a division operation.

Order of operations in Python is the same as in normal math.  Acronym "PEDMAS" which stands for:
1. parenthesis
2. exponents
3. multiplication
4. division
5. addition
6. subtraction


###Exercise 4 - Variables and Names

Variables as defined in Python are pretty much the same as other programming languages EXCEPT variable names in Python must start with either an underscore or a letter.  

No other punctuation is allowed.  

Numbers are okay.  

Uppercase is okay, but convention says "no".

Reminders of some debugging techniques learned so far:
* write comments above lines to describe what it's doing
* read the code backwards
* read the file out loud

My personal debugging notes:
* console log everything
* explain in great detail to someone else what the code is meant to do (rubber duck on a monitor)

ex4.py
```
cars = 100
space_in_a_car = 4.0
drivers = 30
passengers = 90
cars_not_driven = cars - drivers
cars_driven = drivers
carpool_capacity = cars_driven * space_in_a_car
average_passengers_per_car = passengers / cars_driven


print "There are", cars, "cars available."
print "There are only", drivers, "drivers available."
print "There will be", cars_not_driven, "empty cars today."
print "We can transport", carpool_capacity, "people today."
print "We have", passengers, "to carpool today."
print "We need to put about", average_passengers_per_car, "in each car."
```

FUN FACT: python will run as a calculator - type "python" into the terminal without providing the argument file name, and then just setup statements to be calculated.

`=`  versus  `==`  is what?  Single equal is an assignment, double equal is a comparison.


###Exercise 5 - More Variables and Printing

Strings.  Another type, it exists between quotation marks.

ex5.py

```
my_name = 'Zed A. Shaw'
my_age = 35 # not a lie
my_height = 74 # inches
my_weight = 180 # lbs
my_eyes = 'Blue'
my_teeth = 'White'
my_hair = 'Brown'

print "Let's talk about %s." % my_name
print "He's %d inches tall." % my_height
print "He's %d pounds heavy." % my_weight
print "Actually that's not too heavy."
print "He's got %s eyes and %s hair." % (my_eyes, my_hair)
print "His teeth are usually %s depending on the coffee." % my_teeth

print "If I add %d, %d, and %d I get %d." % (
my_age, my_height, my_weight, my_age + my_height + my_weight)
```

`%s`  and  `%r`  and  `%d`  are formatters - these stand in strings as placeholders for variables, listed at the end of the string.  The variables listed at the end of the string will replace each formatter in the order they are listed.

Floating point numbers can be rounded with the built-in function `round()`


###Exercise 6 - Strings and Text

Strings are usually for display, always wrapped in single quotes or double quotes.

ex6.py
```
x = "There are %d types of people." % 10
binary = "binary"
do_not = "don't"
y = "Those who know %s and those who %s." % (binary, do_not)

print x
print y

print "I said: %r." % x
print "I also said: '%s'." % y

hilarious = False
joke_evaluation = "Isn't that joke so funny?! %r"

print joke_evaluation % hilarious

w = "This is the left side of..."
e = "a string with a right side."

print w + e
```

String concatenation with `+`

String formatter `%r` is for "raw" and for debugging (displays raw data of the variable) - the other formatters `%s` and `%d` are for displaying to users.


###Exercise 7 - More Printing

ex7.py
```
print "Mary had a little lamb."
print "Its fleece was white as %s." % 'snow'
print "And everywhere that Mary went."
print "." * 10  # what'd that do?

end1 = "C"
end2 = "h"
end3 = "e"
end4 = "e"
end5 = "s"
end6 = "e"
end7 = "B"
end8 = "u"
end9 = "r"
end10 = "g"
end11 = "e"
end12 = "r"

# watch that comma at the end.  try removing it to see what happens
print end1 + end2 + end3 + end4 + end5 + end6,
print end7 + end8 + end9 + end10 + end11 + end12
```

Python style is 80 characters per line.

Print the character and `* 10` repeats the character that many time - this saves a `for/loop`


###Exercise 8 - Printing, Printing

ex8.py
```
formatter = "%r %r %r %r"

print formatter % (1, 2, 3, 4)
print formatter % ("one", "two", "three", "four")
print formatter % (True, False, False, True)
print formatter % (formatter, formatter, formatter, formatter)
print formatter % (
    "I had this thing.",
    "That you could type up right.",
    "But it didn't sing.",
    "So I said goodnight."
)
```

Demonstrates the ways to combine strings with formatters.  Note the use of the `formatter` variable used two ways.  Output looks like this:

```
1 2 3 4
'one' 'two' 'three' 'four'
True False False True
'%r %r %r %r' '%r %r %r %r' '%r %r %r %r' '%r %r %r %r'
'I had this thing.' 'That you could type up right.' "But it didn't sing." 'So I said goodnight.'
```

`%r` may return (when string) the string in either single quote or double quote depending which is more efficient at the time.  <--- this really sounds dubious, but it's almost a direct quote.


###Exercise 9 - Printing, Printing, Printing

ex9.py
```
# Here's some new strange stuff, remember type it exactly.

days = "Mon Tue Wed Thu Fri Sat Sun"
months = "Jan\nFeb\nMar\nApr\nMay\nJun\nJul\nAug"

print "Here are the days: ", days
print "Here are the months: ", months

print """
There's something going on here.
With the three double-quotes.
We'll be able to type as much as we like.
Even 4 lines if we want, or 5, or 6.
"""
```

This introduces the new line character `\n`

This introduces the triple quote use for blocks of text (string).

New line character does not work well with the `%r` formatter, which prints things in "raw" format, so the output is just "\n" rather than a new line.



###Exercise 10 - What Was That?

The backwards slash, back slash, `\` is called an escape character and is used in various "escape sequences" to indicate to Python "the next character has special meaning"

Example of the need for this is to escape the single or double quote inside a string, as "it's" or 'Hello, "friend" of mine' - these should be written "it\'s" and 'Hello, \"friend\" of mine' 

Example from the book:
```
"I am 6'2\" tall."  # escape double-quote inside string
'I am 6\'2" tall.'  # escape single-quote inside string
```

ex10.py
```
tabby_cat = "\tI'm tabbed in."
persian_cat = "I'm split\non a line."
backslash_cat = "I'm \\ a \\ cat."

fat_cat = """
I'll do a list:
\t* Cat food
\t* Fishies
\t* Catnip\n\t* Grass
"""

print tabby_cat
print persian_cat
print backslash_cat
print fat_cat
```

Escape sequences - this is a table copied directly from the book here:
https://learnpythonthehardway.org/book/ex10.html

Escape	What it does.
\\	| Backslash (\)
\'	| Single-quote (')
\"	| Double-quote (")
\a	| ASCII bell (BEL)
\b	| ASCII backspace (BS)
\f	| ASCII formfeed (FF)
\n	| ASCII linefeed (LF)
\N{name}	| Character named name in the Unicode database (Unicode only)
\r	| Carriage Return (CR)
\t	| Horizontal Tab (TAB)
\uxxxx	| Character with 16-bit hex value xxxx (u'' string only)
\Uxxxxxxxx	| Character with 32-bit hex value xxxxxxxx (u'' string only)
\v	| ASCII vertical tab (VT)
\ooo	| Character with octal value ooo
\xhh	| Character with hex value hh


Author suggests putting each of these on a flash card to help memorize, but I'm using Anki for this instead.


###Exercise 21 - Functions Can Return Something

Up to now all our functions do is output something - typically "print".  This chapter demonstrates that a called function can pass information back to the calling function (caller).

Anything that can be assigned to a variable (on the right side of a "=") can be returned from a function.  It's a nice rule of thumb.

ex21.py
```
def add(a, b):
    print "ADDING %d + %d" % (a, b)
    return a + b

def subtract(a, b):
    print "SUBTRACTING %d - %d" % (a, b)
    return a - b

def multiply(a, b):
    print "MULTIPLYING %d * %d" % (a, b)
    return a * b

def divide(a, b):
    print "DIVIDING %d / %d" % (a, b)
    return a / b


print "Let's do some math with just functions!"

age = add(30, 5)
height = subtract(78, 4)
weight = multiply(90, 2)
iq = divide(100, 2)

print "Age: %d, Height: %d, Weight: %d, IQ: %d" % (age, height, weight, iq)


# A puzzle for the extra credit, type it in anyway.
print "Here is a puzzle."

what = add(age, subtract(height, multiply(weight, divide(iq, 2))))

print "That becomes: ", what, "Can you do it by hand?"
```

Crazy nested function in there assigned to variable `what` near the end.  


###Exercise 22 - What Do You Know So Far?

This chapter is a review and recommends scouring the previous chapters for Python words and symbols to create a list of study objects for future review.


###Exercise 23 - Read Some Code

In this chapter, author makes an excellent suggestion to go to Bitbucket or Github and find someone else's Python code and read it.  IMHO the best way to learn to code better is to read other people's code.  Good, bad, or ugly there's always something to learn reading others' work.


###Exercise 24 - More Practice

The gyst of this chapter was to gain more muscle memory by typing in the exercise, which was a little long.  There is no new information to learn here except typing.


###Exercise 25 - Even More Practice

ex25.py
```
def break_words(stuff):
    """This function will break up words for us."""
    words = stuff.split(' ')
    return words

def sort_words(words):
    """Sorts the words."""
    return sorted(words)

def print_first_word(words):
    """Prints the first word after popping it off."""
    word = words.pop(0)
    print word

def print_last_word(words):
    """Prints the last word after popping it off."""
    word = words.pop(-1)
    print word

def sort_sentence(sentence):
    """Takes in a full sentence and returns the sorted words."""
    words = break_words(sentence)
    return sort_words(words)

def print_first_and_last(sentence):
    """Prints the first and last words of the sentence."""
    words = break_words(sentence)
    print_first_word(words)
    print_last_word(words)

def print_first_and_last_sorted(sentence):
    """Sorts the words then prints the first and last one."""
    words = sort_sentence(sentence)
    print_first_word(words)
    print_last_word(words)
```

Running this script as "python ex25.py" does nothing, it's not intended to output or print anything.  But do it anyway and look for an absence of errors which would (one hopes) indicate no issues with the way the script is typed into the document.

In this chapter we learn how to run the python shell by typing in "python" and provide it no file names or other arguments.

Once in the shell it's possible to import the script ex25.py by typing "import ex25" and NOTE there is no file extension ".py" on that command.

When imported correctly, the functions defined in the script are available for use in the shell by calling them by name as part of ex25 thusly  `ex25.print_first_and_last`  

The shell will hold variable names so typing `sentence = "All good things come to those who wait"` and then `words = ex25.break_words(sentence)` we then have access to these two variables later in the shell session.

When importing the script this way, it's necessary to preface each function call with `ex25.` as `ex25.sort_words` HOWEVER it's possible to import these and access them without the preface as this  `from ex25 import * ` where the asterisk is a wildcard character and everything in the script is imported into the shell.

I can imagine this is a bad idea if it's necessary to import from two or more scripts and maybe they have same/similar function definitions, then prefacing with the script name is a good idea to keep things separate.

The sample script in this chapter contains some information for the man page.  In the shell type `help(ex25)` and the documenation is provided.  The triple quote sections are "documentation comments".  Makes sense.

