# pythonNotes
Python notes

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
=5
=4
=3
=2
=1
=Blastoff!

## Variables
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
### User Input
Python can pause and read data from the user using the input() function
input() returns a string
```python
yourName = input('Who are you?')
print('Welcome' , yourName)
```
The , represents a space in python.

### Comments
Python ignores anything after the # sign and treat it as comments

## Conditional Execution
### Comparison Operators 
<
<=
== 
>=
>
!=

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














