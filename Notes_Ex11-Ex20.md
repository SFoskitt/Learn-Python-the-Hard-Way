# Learn-Python-the-Hard-Way
My notes and maybe some exercises to follow along with the e-book "Learn Python the Hard Way" by Zed Shaw.  Added here for 100 Days of Code.

=======================

@(WWC - Learn Python the Hard Way)

###Exercise 11 - Asking Questions

Our first exposure to `raw_input()`

ex11.py
```
print "How old are you?",
age = raw_input()
print "How tall are you?",
height = raw_input()
print "How much do you weigh?",
weight = raw_input()

print "So, you're %r old, %r tall and %r heavy." % (
    age, height, weight)
```

The comma at the end of each `print` line prevents Python from adding a `\n` character at the end of each (these then act as prompts for the `raw_input()`)

Wrap `raw_input()` inside `int()` to force the responses to be coerced to type `int`, ex: `x = int(raw_input())`


###Exercise 12 - Prompting People

ex12.py
```
age = raw_input("How old are you? ")
height = raw_input("How tall are you? ")
weight = raw_input("How much do you weigh? ")

print "So, you're %r old, %r tall and %r heavy." % (
    age, height, weight)
```

Prompts for the `raw_input()` can be included inside the method call, ex: `x = raw_input('How you doing? ')` instead of prefacing with a `print` line

`pydoc` is a way to get documentation on Python standard library methods, ex: `$ pydoc raw_input` - this does not work for terminal methods like `echo` and `cat`


###Exercise 13 - Parameters, Unpacking, Variables

ex13.py
```
from sys import argv

script, first, second, third = argv

print "The script is called:", script
print "Your first variable is:", first
print "Your second variable is:", second
print "Your third variable is:", third
```

`import` adds features to the script from outside modules - in the above example, the module is `sys` and imports `argv` which allows us to take arguments from the terminal when starting a Python script, ex: `python ex13.py snacks naps`

the name of the script is __*ALWAYS*__ the first argument packed into `argv` and must always be unpacked in the script


###Exercise 14 - Prompting and Passing

ex14.py
```
from sys import argv

script, user_name = argv
prompt = '> '

print "Hi %s, I'm the %s script." % (user_name, script)
print "I'd like to ask you a few questions."
print "Do you like me %s?" % user_name
likes = raw_input(prompt)

print "Where do you live %s?" % user_name
lives = raw_input(prompt)

print "What kind of computer do you have?"
computer = raw_input(prompt)

print """
Alright, so you said %r about liking me.
You live in %r.  Not sure where that is.
And you have a %r computer.  Nice.
""" % (likes, lives, computer)
```

Setting a variable name as `prompt` helps make this code more DRY

The use of double-quotes three times marks out a block of string text, rather than enter four lines of text in quotes


###Exercise 15 - Reading Files

ex15.py
```
from sys import argv

script, filename = argv

txt = open(filename)

print "Here's your file %r:" % filename
print txt.read()

print "Type the filename again:"
file_again = raw_input("> ")

txt_again = open(file_again)

print txt_again.read()
```

`open(filename)` opens a file as a file object which comes with additional commands are available once a file is opened


