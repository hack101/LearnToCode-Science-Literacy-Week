# Science Literacy Week: Learn To Code With HackMcGill

###### Note:
This tutorial is designed to presented in person and give you a flavour for programming in under an hour, so there are a couple things missing... If you're reading this at home then you have the luxury of more involved tutorials and interactive! See the resources listed at the bottom.

###### Note:
We'll be using this online programming evironment [https://repl.it/languages/python3](https://repl.it/languages/python3)

## Why learn coding?
 > "IDC Canada estimates there are 54,000 unfilled information technology jobs in Canada"

Source: [CBC](http://www.cbc.ca/news/business/54-000-canadian-it-jobs-unfilled-idc-estimates-1.3230733)

> "223,000 unfilled coding jobs in the US. [...] And the gap is growing."

Source: [Quartz](http://qz.com/778380/the-future-is-software-engineers-who-cant-code/)

> "It's super fun and you get to make cool stuff!"

Source: Amiel

## What is coding?
Coding (or programming) is writing a series of instructions that a computer can execute.
These series of instructions are called a program.

Computers are actually very dumb. They can only do a few basic things.
- They have memory.
    - They can read things in their memory
    - They can write (update, or add to) their memory
- They can do basic logical operations
    - `+`, `-`, `*`, `/`, `if ... then do ...`,
- They have input and output (keyboards and screens, for example)

The power of computers comes from the fact that, while they are very dumb, they don't make mistakes and they're __very__ fast.

Right now, a machine that can do the operations listed above doesn't seem too useful.
In writing a program, we are compounding these operations in order to make something useful. 
Big programs (like a video game, or Facebook) will have millions and millions of lines of code, but it all comes down to those operations above!

There are multiple _Coding Languages_, each coding language is a middleman for you
and your computer. You write something a little closer to spoken language and it
will be translated in a series of machine instructions which look like the operations
I described above.

In this tutorial we will be learning Python 3, but all the concepts we learn will
generalize to other langauges. Here are some lanaguages you may have heard of
and what they're used for:

| Language  | Uses 
|-----------|------
|Python     | Web development, scientific computing 
|Java       | Enterprise (a lot of big companies use Java), Android apps 
|C++        | Game developement
|JavaScript | Web development

And many more!

## Your First Program
As a matter of tradition, the first program someone usually learns (either if it's your first time programming, or you're an experienced programmer learning a new coding langauge) is the ["Hello, world!" program](https://en.wikipedia.org/wiki/%22Hello,_World!%22_program#History)

This program prints "Hello, world!" to the screen!

In Python, when we want to print something to the screen, we use the print function.
In our python editor, we can write the following, then hit "Run". Of course, you
don't have to say "Hello, world!", you can have your computer say whatever you want!!

```python
print("Hello, world!")
```

## Variables

Remember I said computers can remember things? As a programmer, it's your job to tell
the computer what to remember. When you're writing up an assignment, 
you would make and save a document, but in the context of a program, we'll use _variables_.

Let's say you're writing a letter. You open up Word, write the letter, and save it
with a good name so you can find it later. The content of the letter is the
information you wanted to save, and the name of the file is the label for this information.

Variables are the same thing. They have two parts: the information (or data) and a 
label.

Let's see a couple examples.

```python
x = 5
```

I've just _declared a variable_. I've said, from now on in my program, `x` is just a 
label for 5. Let's see another example

```python
hello = "Hello, world!"

print(hello)
```

What do you think this does? Remember, `hello` is just a label for `"Hello, world!"`.
When we tell the computer `print(hello)`, we're telling it: go to the label `hello`,
find the information that label refers to and print that informat.

Your labels can be anything with letters, numbers or underscores (as long as it
doesn't start with a number)

```python
x = 5
hello = "Hello, world!"
my_variable_y = 2.5
z_is_bigger_than_1000 = 100000
```

Generally, we like to have short and simple variable names.

### Data Types

Notice anything different about `x`, `hello`, and `y` in the above example?
They're different __types__! What does that mean? Well `x` is an integer, 
`hello` is a bunch of letters and characters, and `y` is a number with a decimal point.

Each variable has a type. In some languages, we have to tell the computer what type
a variable is going to be, but Python can figure it on its own. 

Whole numbers are called integers "ints".
Numbers with decimal points are called "floats" (floating point number) 
(or sometimes "doubles" for double precision floating point number)
The bunches of characters and letters are called "strings" (strings of characters).
Some languages make a disctintion between individual characters "chars" and strings,
Python does not. 

The more complicated your programs become, types will become more and more important!
For now, just keep in mind that not all variables are the same. 

There's one basic type that we haven't seen yet and that's a _boolean_.
A boolean is a special type that can only have two values. `True` or `False`.

```python
my_boolean = True
```

We'll see how we use booleans soon.

### Reassignment

When you saved that letter, it doesn't have to stay the same forever! You can always
open it up, edit and, and save it again. The same is true with variables!

What do you think the following does?
```python
hello = "Hello, world!"
hello = "Goodbye, world!"

print(hello)
```

At first, `hello` holds the information "Hello, world!", but on the second line that
information is replaced with "Goodbye, world!". By the time we get to the print 
statement, `hello` holds "Goodbye, world!" so that is what's printed. 

In Python we can even change the type of a variable (though some langauges
don't allow this and it's generally a bad idea).

```python
x = 5
x = "x is a string now. don't do this"
```

---

## Operations on variables

So we've covered the memory part! When we say `x = 5`, we're telling the computer to
remeber a value and when we say `print(hello)`, we're telling to computer to access
the value it remembered.

Next, I said computers can do basic operations. Let's say we want to do some addition.

```python
x = 5 + 5
```

The computer will do the operation on the right, and then the result will be stored 
in the variable on the left! *Assignment is always right to left*

Let's look at another example
```python
x = 5
y = 10
z = x + y
```
What do you think `z` is? 

```python
x = 5
y = x + 5
z = y + x + 5
``` 
What about now?

In the first example, `z` is 15, and in the second example `z` is 20. If this 
isn't what you got, try reading the code line by line and at each step keep track of
what value every variable has.

Not let's look at a couple more complicated examples

```python
x = 5
y = x * 5
x = y
```
What's `x`?

```python
x = 5
x = x - 1
```
How about now? (Remember, assignment goes from right to left!!!)

In the first example, `x` is 25. Let's follow it line by line.

1. `x` stores the value 5.
2. We access the value of `x`, see 5, multiply that by 5 and then store the value in `y`, `y` is now 25 and `x` is still 5.
3. We access the value of `y` (25), and *reassign* `x` to that value. `x` is 25!

In the second example, `x` has the value 4. The important thing to remember here is
that assignment goes from right to left. **Assignment goes from right to left!**
Every assignment has two steps: Evaluate the right side, store that in the left side.
So, let's walk through this one

1. `x` stores the value 5
2. We access the value of `x`, see 5. We subtract 1 from this value, get 4. We assign the left to this new value. Now x has value `4`!

This operation of subtracting or adding one is so common there are shorter versions of it.

The following are entirely equivalent. 
```python
x = x - 1
x -= 1
```

```python
x = x + 5
x += 5
```

Some langauges let you do `x++` or `x--` to add or subtract 1 respectively, but 
python doesn't allow this.


So far I've only shown operations on integers, but what about other variable types?

```python
x = 2.5 * 2
hello = "Hello, " + "world!"
false = not True
```

Basic arithmetic works as you would expect on floats.
`+` can be used to join strings. `hello` has the value "Hello, world!"
For booleans, the `not` inverts the value, so `not True` is false and
`not False` is true.

Note that types are important here!! You can add strings with strings, ints with ints and floats, but you can't add an int to a string (that doesn't make sense!).

This program will fail!!
```python
x = 5
hello = "Hello, world!"

print(hello + x)
```
This is the first program we've encountered that won't run. When a program either doesn't run, or does run but does the wrong thing, it is said to "have a bug".

We can change the type of a variable, however, using special functions. For example, if we wanted to print "Hello, world!5" in the above example, we could use the `str` (short for string function) on `x` to *cast* it into (i.e. turn it into) a string and then add the two.

```python
x = 5
hello = "Hello, world!"

print(hello + str(x))
```

### Comments

Now we've covered memory and arithmetic! All that's left is logic and input output.
Before we move on, one more useful thing to know is comments.

Sometimes, when we write code, we want to leave comments about the code to either
our future selves reading it again later, or to anyone else who might read our 
code. Always write a couple comments in your code!!!!!

In Python, comments start with a hashtag. The computer will ignore 
everything from the hashtag to the end of the line.
```python
x = 5
# this is a comment, the computer will ignore this line
y = 5 # this is also a comment
```

### Exercise

OK, now we know how to make a computer follow some simple instructions, write
a useful program!

We'll do a tip calculator. The goal is, given the bill amount, add tax and tip then print the new amount.

Try creating three variables. Call them what you like, but I'll call mine
`bill`, `tax`, and `tip`. Assign these three variables to the appropriate amount 
then print the final total! 



```python
bill = 28.50
tax = bill * 0.13  # sales tax is 13%
tip = bill * 0.18  # I was happy, so 18% tip

# now calculate the new total.
total = bill + tax + tip

print(total)
```

---

## Input/Ouput

Called I/O for short. We've already seen some of this, the `print` function is 
output!

In order to get input, we will have someone type at our computers. In python, we
can use the `input` function. it works like so:

```python
name = input("Enter your name: ")
print("Hello " + name)
```

The input function will print `Enter your name: ` then wait for the user to type
something. The name variable is then assigned to whatever the user types.
(We say "Input _returns_ whatever the user typed".)

Try the above code snippet out!

Just a little digression: I/O doesn't have to be the screen and keyboard. Maybe you
want to write a program which takes in a text document, and replaces all instances of
"Bill" with "William". 
In this case the input and outputs are both files! This is all possible with 
Python but we won't cover it today.

---

## Control flow and loops

Looks like I've almost covered everything on that list of what a computer can do! 
All I'm missing is `if ... then ...`

This is called control flow, and refers to a bunch of programming contrsucts that
allow us to control the flow of our program.

### if then else
If-else statements allow us to specify to a computer different sets of instructions
(often called code blocks) for a computer to execute depending on the outcome of a
condition. 

If statements have the following structure

```
if <condition>:
    <code to execute if the condition is true>
else:
    <code to execute if the condition isn't true>
```

It's best explained by an example:

```python
if True:
    # all the instructions in this code block will be executed
    hello = "Hello, world!"
    x = 5
    print("This line of code will be executed!!")
else:
    hello = "Goodbye, world!"
    x = 10
    print("This line won't be :(")
```

Note how the lines of code after the `if` and `else` are indented. 
In python the indentation is important. The indentation groups code together.
This is saying: if the condition is true then group all the indented code below it. 
This group of code is called a code block

The else statement is always optional. The condition is a boolean,
but we can do comparisons!

Let's look at some more interesting examples.

```python
x = 5

# here our condition is that x is equal to 5.
# note that we're using two '=' signs to compare numbers!! 
# (one equals sign is reserved for assignment)
if x == 5:
    print("x is five!")
```
Note no else statement here, it's optional! That just means that if `x` isn't 5, do nothing!

A couple more examples

```python
x = 10

if x > 9:
    print("x is less than 9")
else:
    print("x is greater than or equal to 9")
```

This prints `x is greater than or equal to 9`.


```python
hello = "Hello"

if hello == "Goodbye":
    print("Goodbye, world!")
elif hello == "Hello":
    print("Hello, world!")
else:
    print("????")
```

This prints `Hello`. Note the `elif`, this is short for "else if" and allows you to
handle multiple conditions.

Some other ways of comparing

| Condition | Meaning
|-----------|--------
`x > y`     | `x` is greater than `y`
`x < y`     | ... less than
`x == y`    | ... is equal to
`x != y`    | ... is not equal
`x >= y`    | ... greater than or equal to
`x <= y`    | ... less than or equal to

You can join the above with `and` and `or`
```python
print(5 < 10 and 2 > 3)  # prints False
print(5 < 10 or 2 > 3)  # prints True
```

### Looping

There are two types of loops in Python, `for` and `while`. We'll focus on the while loop. It has the following structure:
```
while <condition>
    <execute this code block>
```

Just like an if statement, it checks a condition. If the condition is true it
will execute the code block indented beneath it. The difference between a while loop and an if is that an if only executes that block once.
Every time a while loop finishes it checks the condition again. If the condition is still true, it starts over!

Let's look at an example 
```python
counter = 0
while counter < 5:
    print("again!")
    counter = counter + 1

print("done")
```
What do you think this code will do?



As the variable name suggests, this program counts to 5.
Let's run through what happens:

1. `counter` gets the value 0
2. `counter` is 0, which is less than 5, so we enter the code block
3. We print "again!"
4. `counter` is incremented by 1. Its new value is 1.
5. We've reached the end of the while loop! Now we go back and check the condition again.
6. `counter` is 1 and is less than 5, so we enter the code block again!
7.  ...

We repeat this process until eventually `counter` is 4
8. `counter` is 4, which is less than 5, so we enter the loop
9. print "again"
10. `counter` is incremented by 1, now `counter` is 5.
11. We've reached the end of the loop! We go back and check the condition once more. This time the condition is not true! So we exit the loop and start executing the code below
12. print "done"

If we run this code, we get the output
```
again!
again!
again!
again!
again!
done
```

### for loops
`for` loops are another way to iterate with a little bit of a different syntax. We won't talk about them here, but here's an example of how you would write the above program with a for loop for those interested.

```python
for count in range(5):
    print("again!")

print("done")
```

This says "Declare a variable `count`, and for each iteration of the loop change its value to range from 0 to 5 (not including 5 itself)"

----
## Final exercise

For our final exercise, we're going to make a guessing game. The game will ask the user to think of a number between 1 and 100, and then try to guess the number.

First, let's be friendly and get the user's name. 
Then, we'll tell them to guess a number.

```python
name = input("Hi! What's your name? :")
print("Hi " + name + ". Guess a number between 1 and 100")
```

Now, how should we go about guessing? The same way we would in the real world!

We first ask: "Is it 1?", then "Is it two?" then ...
Since we don't want to write that all out, let's used a loop!

We'll use a variable `guess` to store our current guess and a variable
`correct` to store if we've guessed correctly yet or not.

`correct` starts out as false, because we can't have guessed correctly if we haven't guessed anything yet!

Our logic will be: while our current guess isn't correct, guess the next number.

```
guess = 1
correct = False

while not correct:
    guess = guess + 1
```

But wait, we need to ask the user if we got it right!

```
name = input("Hi! What's your name? :")
print("Hi " + name + ". Guess a number between 1 and 100")
guess = 1
correct = False

while not correct:
    answer = input("Is your guess " + str(guess) + "? ")
    if answer == "yes":
        print("Yay!")
        correct = True
    guess = guess + 1
    
print("Thanks for playing!")
```

When we get it right, `correct` becomes `True` then `not correct` becomes false and we'll exit the loop.

Great, we did it! But it's really slow... What if the user guesses 100? It'll take a while for us to get it right.

Let's think of a way to do it differently. If we are looking for a name in a phone book, would we open it to the first page and read every name until we find the one we want? Of course not! We'd flip to the middle and then check if we're before or after the name, then flip left or right and repeat!

In computer science, this is called a *binary search*, and it will let us find the guessed number much faster!

Like we would do with the phone book, we will start in the middle but guessing 50.
If we're too low, we'll guess 75, if we're too high we'll guess 25 and so on...

If we just guess every number, in the worst case it'll take us 100 tries! (if the user picked 100) But with the binary search method, where we start with 50, it'll take us at most 7 tries. Much better!!

You can try and implement this more efficient solution yourself!
I've included a completed example below, for you to read through, but I won't give it a full explanation (we're probably out of time by now).

Just a quick note, here we have used two different *algorithms* to guess the number. One algorithm was just two guess every number and the other was to use a binary search. While coding is all about what we've been doing today, computer science is all about finding effecient algorithms! A lot of the time that means just thinking about what would be faster without writing any actual code (like we've done here).

There is a difference between programming/coding and computer science!

For your reference:

| Class  | Topic 
|--------|-------
| COMP 202 | Mostly programming, a *tiny* bit of computer science
| COMP 250 | Half and half
| COMP 251 | All computer science, no coding at all!

----
## Resources

### Tutorials
* [CodeCademy](https://www.codecademy.com/lrn/python): Great for a first time programmer! Covers all the concepts in this tutorial and everything this tutorial left out with plenty of practice excercies. 
* [LearnPython](http://www.learnpython.org/): A little less explanation than CodeCademy. If this tutorial seemed slow to you then this is the place to go!

Both the above have links to resources for other languages as well! If you enjoyed this tutorial, I highly suggest you check out one of the tutorials above! There are a couple important things I left out since I didn't have time. 

### Other
* [Excercies](http://www.cplusplus.com/forum/articles/12974/): This is a blog post from a C++ community about excercies to get practice coding, once you're comfortable with all the material we touched on today. Even though it was written for C++, they're great excercies for all languages.
* [HackMcGill](https://www.facebook.com/groups/hackmcgill/): A computer science community at McGill, we host events and tutorials. This is a great place to go if you're looking to learn more about the computer science community or get involved.
* [Hack101](https://github.com/hack101): Once you are comfortable with programming, and want to put your skills to use, we have two tutorial series here! One on web programming (in Python) and one on Android programming (Java). Stay tuned in the HackMcGill group in case we hold these tutorials again.
* Me: If you don't want to post in the HackMcGill group, feel free to ask me any questions! You can find me on facebook (Amiel Kollek) or shoot me an email at [amiel.kollek@mail.mcgill.ca](mailto:amiel.kollek@mail.mcgill.ca). I'm always happy to suggest resources or answer questions about programming.


# Thanks for coming!

---
# Binary search for guessing game

```python
# a function we use to get the ceiling of a number
# the ceiling of a number just means rounding up!
#    ceil(2.0) == 2
#    ceil(1.6) == 2
#    ceil(3.2) == 4
from math import ceil

name = input("Hi! What's your name? :")
print("Hi " + name + ". Guess a number between 1 and 100")
guess = 50  # start at 50!!
attempt = 1
correct = False

while not correct:
    attempt += 1
    answer = input("Is this guess lower, higher or right? " + str(guess) + " ")
    if answer == "right":
        # same as before when we got it right!
        print("Yay!")
        correct = True
    elif answer == "lower":
        # two *'s means exponent. 2**3 == 8
        guess -= ceil(100 / 2 ** attempt) 
    elif answer == "higher":
        guess += ceil(100 / 2 ** attempt)
    else:
        print("please type 'lower', 'higher', or 'right'")
        # since we're redoing this try, decrement try
        attempt -= 1

print("Thanks for playing!")
```



