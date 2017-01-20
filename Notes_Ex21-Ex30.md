
# Learn-Python-the-Hard-Way
My notes and maybe some exercises to follow along with the e-book "Learn Python the Hard Way" by Zed Shaw.  Added here for 100 Days of Code.

=======================

@(WWC - Learn Python the Hard Way)

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

