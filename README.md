# pythonNotes
Python 101 notes

## Reserved words
False, class, return , is, finally, None, if, for , lambda, continue, True, def, from, while, nonlocal, and, del, global, not, with, as, elif, try , or, yield,  assert, else, import, pass, break, except, in, raise

## Program Flow
### Sequential Steps
```python
x = 2
print(x)
```
=2 
```python
x = x + 2
print(x)
```
=2 

### Conditional Steps
```python
x = 5
if x < 10;
  print('Smaller')
if x > 20;
  print('Bigger')
Print('Finis')
```
=Smaller

=Finis

### Repeated Steps (Loops)
```python
n = 5
while n > 0:
  print(n)
  n = n - 1
print('Blastoff!')
```
```python
=5
=4
=3
=2
=1
=Blastoff!
```
## Variables
### Variables
A named place in memory where a program can store data and later retrieve the data using the variable  "name"
You can change the contents of a variable in a later statement.
You must start with a letter or underscore. But underscore mainly used when communicating with python itself.
### Constants
Constants are fixed values, aka their values do not change

## Expressions
### Numeric Expressions
Python follow left to right: Parenthesis -> Power -> Multiplication/Divsion -> Addition/Subtraction 
+ Addition
- Subtraction
* Multiplication
/ Division
**  Power
% Remainder

### Type
You cannot add different types together
You can check type like this 
```python
x = 1
y = 92.3
type(x)
=<class 'int'>
type(y)
=<class 'float'>
```
When you put an integer and floating point in an expression, the integer is implicitly converted to a float.
You can control it with int() and float()
```python
x = 1
y = float(x)
print(y)
=1.0
type(y)
=<class 'float'>
```
Integer division produces a floating point result
```python
print(10/2)
=5.0
```
## User Input
Python can pause and read data from the user using the input() function
input() returns a string
```python
yourName = input('Who are you?')
print('Welcome' , yourName)
```
The , represents a space in python.

## Comments
Python ignores anything after the # sign and treat it as comments

## Conditional Execution
### Comparison Operators 
```python
<
<=
== 
>=
>
!=
```

### One-Way Decisions
```python
x = 5
print('Before 5')
if x == 5 :
  print('Is 5')
  print('Is Still 5')
  print('Third 5')
print('afterwards 5')
print('Before 6')
if x == 6 :
  print('is 6')
  print('is still 6')
  print('third 6')
print('afterward 6')
```

### Nested Decisions
```python
x = 40
if x > 1 :
  print('more than one')
  if x < 100 :
    print('less than 100')
print('All done')
```
### Two way Deicision with else
```python
x = 4
if x > 2 :
  print('Bigger')
 else :
  print('Smaller')
print "All done'
```
### Multi-way
``` print
if x < 2 :
  print('small')
elif x < 10 :
  print('Medium')
else : 
  print('LARGE')
print('All done')
```

### Try/Except
to compensate for errors
```python
astr = 'Bob'
try:
  print('Hello')
  istr = int(astr)
  print('there')
except: 
  istr = -1
print('Done', istr)
```
## Python Functions
Two kinds of functions. Built in functions and functions we define ourselves.
Function is reuseable code that takes arguments as inputs, does some computation, and returns something.
### Max/Min Function
```python
big = max('Hello world')
print(big)
=w
tiny = min('Hello world')
print(tiny)
=
```
### Parameters
A variable which we use in the function definition. It is a handle that allows the code in the function to access the arguments for a particular function invocation.
### Return Values
Often a function will take its arguments, do some computations and returns a value to be used as the value of the function in the calling expressio. The return keyword is used for this. 

## Loops & Iterations
### While Loop
```python 
n = 5
while n > 0 :
  print(n)
  n = n - 1
print('blastoff!')
print(n)
```
### Infinite Loop
```python
n = 5
while n > 0 :
  print('lather')
  print('rinse')
print('dry off!')
```

### Breaking out of Loop
```python
while True:
  line = input('> ')
  if line === 'done' :
    break
  print(line)
print('done!')
```
### Finishing an iteration with continue
```python
while True:
  line = input('> ')
  if line[0] === '#' :
    continue
  if line === 'done' :
    break
  print(line)
print('done!')
```
### Definite Loops
Looping of a finite set of things
```python
for i in [5, 4, 3, 2, 1] :
  print(i)
print('done')
```
definite loop with strings
```python
friends = ['joseph', 'jane', 'jessica']
for friend in friends :
  print('Happy New Year: ', friend)
print('done')
```
### Looping through a Set
```python
for thing in [5, 4, 3, 2, 1] :
  print(thing)
print('done')
```
### Finding the largest value
We make a variable that contains the current largest vvalue. If the number we are looking at is larger, it is the new largest value.
```python
largest_so_far = -1
print('Before', largest_so_far)
for the_num in (9, 41, 12, 3, 74, 15] :
  if the_num > largest_so_far :
    largest_so_far = the_num
  print(largest_so_far, the_num)
print('After', largest_so_far)
```
### Counting in a loop
To Count how many times we execute a loop, we introduce a counter variable that starts at 0 and we add one t oit each time through the loop.
```python
zork = 0
print ('Before', zork)
for i in [5, 4, 3, 2, 1] :
zork = zork + 1
  print(zork, i)
print('done', zork)
```
### Summing in a Loop
To add up a value we encounter in a loop, we introduce a sum variable that starts at 0 and we add the value to the sum each time through the loop
```python
zork = 0
print ('Before', zork)
for i in [5, 4, 3, 2, 1] :
zork = zork + i
  print(zork, i)
print('done', zork)
```
### Finding the Average in a Loop
An average combines the counting and sum patterns and divides when the loop is done.
```python
count = 0
sum = 0
print('Before', count, sum)
for value in [9, 41, 12, 3, 74, 15] :
  count = count + 1
  sum = sum + value
  print(count, sum, value)
print('After', count, sum, sum / count)
```
### Filtering in a Loop
We use an if statement in the loop to catch / filter the values we are looking for
```python
print('Before')
for value in [9, 41, 12, 3, 74, 15] :
  if value > 20:
    print('Large number', value)
  print('After')
```
### Search using a Boolean variable
If we just want to search and know if a value was found, we use a variable that starts at False and is set to True as soon as we find what we are looking for.
```python
found = False
print('Before', found)
for value in [9, 41, 12, 3, 74, 15] :
  if value == 3 :
  found = True
    print(found, value)
  print('After', found)
```
### Find the smallest value
```python
smallest_so_far = 78
print('Before', smallest_so_far)
for the_num in (9, 41, 12, 3, 74, 15] :
  if the_num < smallest_so_far :
    smallest_so_far = the_num
  print(smallest_so_far, the_num)
print('After', smallest_so_far)
```
The first time we loop through smallest is None, so we take the first value to be the smallest.(9)
```python
smallest_so_far = None
print('Before')
for value in (9, 41, 12, 3, 74, 15] :
  if smallest is None :
    smallest = value
  elif value < smallest :
    print(smallest, value)
print('After')
```
## Strings
### String Data Type
A string is a sequence of characters
A string literal uses quotes like 'hi or "hi"
For strings + means concatenate
We can convert numbers in a string into a number using int()
### Single characters in strings
We can get any single character in a string using an index specified in square brackets.
```python
fruit = 'banana'
letter = fruit[0]
print(letter)
=b
```
### Check string length
```python
fruit = 'banana'
print(len(letter))
=6
```
### Looping through Strings
While Loop
```python
fruit = 'banana'
index = 0
while index < len(fruit) :
  letter = fruit[index]
  print(index,letter)
  index = index + 1
```
For Loop
```python
fruit = 'banana'
for letter in fruit:
  print(letter)
```
### Looping and Counting
Simple loop that loops through each letter in a string and counts the number of times the loop encounters the 'a' character.
```python
word = 'banana'
count = 0
for letter in word:
  if letter == 'a' :
    count = count + 1
print(count)
```

### Slicing Strings
```python
s = 'Monty Python'
print(s[0:4])
=Mont
print(s[6:7])
=P
print(s[6:20])
=Python
print(s[:2])
=Mo
print(s[8:])
=thon
print(s[:])
=Monty Python
```
### String Concatenation
```python
a = 'Hello'
b = a + "There'
print(b)
=HelloThere
```
### Using in as a logical Operator
The in keyword can also be used to check to see if one string is "in" another string
```python
fruit = 'banana'
'n' in fruit
=True
'm' in fruit
=False
'nan' in fruit
=True
```

### String Library
Pythong has a number of string functions which are in the string library
These functions are already built into every string
We do not modify the original string, instead we return a new string that has been altered
```python
greet = 'Hello Bob'
zap = greet.lower()
print(zap)
=hello bob
```
### Searching a String
```python
fruit = 'banana'
pos = fruit.find('na')
print(pos)
=2
```
### Make everything Upper case
```python
greet = 'Hello Bob'
nn = greet.upper()
print(nn)
=HELLO BOB
```
### Search and Replace
```python
greet = 'Hello Bob'
nstr = greet.replace('Bob', 'Jane')
print(nstr)
=Hello Jane
```
### Stripping Whitespace
```python
greet = '   Hello Bob  '
greet.lstrip()
='Hello Bob  '
greet.rstrip()
='.   Hello Bob'
greet.strip()
='Hello Bob'
```
### Parsing and Extracting
From justin@gmail.com Tue July 14 8:04:30:30 2020
```python
data = 'From justin@gmail.com Tue July 14 8:04:30:30 2020'
atpos = data.find('@')
print(atpos)
=11
sppos = data.find(' ',atpos)
print(sppos)
=21
host = data[atpos+1 : sspos]
print(host)
gmail.com
```
## Files
### Opening a File
Before we can read the contents of a file we tell python which file and what we are doing with the file.
open() function 
handle = open(filename,mode)
returns a handle use to manipulate the file
filename is a string
mode is optional and should be 'r' if we are planning to read the file and 'w' if we are going to write to the file
```python
fhand = open('mbox.txt')
print(fhand)
<_io.TextIOWrapper name='mbox.txt' mode='r' encoding='UTF=8'>
```
### Newline Character
\n 
```python
stuff = 'Hello\nWorld!'
print(stuff)
=Hello
=World!
```
### File Handle as a Sequence(READ ALL LINES)
```python
xfile = open('mbox.txt')
for cheese in xfile:
  print(cheese)
```
### Counting Lines in a File
Open a file read-only
Use a for loop to read each line
Count the lines and print out the number of lines
```python
fhand = open('mbox.txt')
count = 0
for line in fhand:
  count = count + 1
print('Line Count:', count)
```
```python
python open.py
=Line Count: 132045
```
### Reading the WHOLE File
Read the whole file into a single string
```python
fhand = open('mbox.txt')
inp = fhand.read()
print(len(inp))
=94626
print(inp[:20])
From justin.kim@gma
```
### Searching through a File
```python
fhand = open('mbox.txt')
for line in fhand: 
  if line.startswith('From:') :
    print(line)
```
### Skipping with continue ( Searching through File Fixed)
```python
fhand = open('mbox.txt')
for line in fhand: 
  line = line.rstrip()
  if not line.startswith('From:') :
    continue
  print(line)
```
### Using in to select lines
We can look for a string anywhere in a line as our selection criteria

```python
fhand = open('mbox.txt')
for line in fhand: 
  line = line.rstrip()
  if not '@uct.ac.za' in line:
    continue
  print(line)
```
### Prompt for File Name
```python
fname = input('Enter file name: ')
fhand = open(fname)
count = 0
for line in fhand:
  if line.startswith('Subject:') :
    count = count + 1
print("there were", count, "subject lines in", fname)
```
### Dealing with Bad File Names
```python
fname = input('Enter file name: ')
try:
  fhand = open(fname)
except:
  print('file cannot be opened:', fname)
  quit()
count = 0
for line in fhand:
  if line.startswith('Subject:') :
    count = count + 1
print("there were", count, "subject lines in", fname)
```

























