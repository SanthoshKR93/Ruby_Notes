# Ruby

## Basic Concepts

Ruby is a dynamic, object-oriented, general-purpose programming language.
Its popularity is increased by the framework built in Ruby called as Ruby on Rails.
In Ruby even a number is an object.

### Input & Output

#### puts

prints the value assigned to it and provides a new line after the value is printed.

```
puts "hello world!!"
```

#### print

prints the value assigned to it but does not provide a new line at the end. 

```
print "hello world!!"
```

#### gets

gets method gets the input from the user including the new line at the end.
Inorder to get the input only without the new line, we use 'gets.chomp'
```
x = gets                # storing the user input into a variable.
puts x
# gets the new line at the end.

y = gets.chomp
puts y
# will not get the new line.
```
<b>NOTE:</b><br>
The gets method gets the user input as a string so inorder to use integer of float values, we have to explicitly convert the string to integer or float.

```
x = gets
puts x.to_i      # converts the user input to integer.
```

### Comments

- single line comment is given by using '#'

```
# this is a comment
```
- Multiline comments are given using =begin and =end

```
=begin
this 
is 
a 
multiline
comment
=end
```
### Variables

Variables store data and data can be assigned to a variable.

```
x = value
```
#### Constants

Variables starting with a capital letter are called constants.Its value cannot be changed once assigned.

```
MyValue = 3.14
```
### Datatypes

All variables in Ruby can have any datatype.Ruby automatically determines the datatype of a variable by checking the values assigned to the variable.

```
x = 42                          # integer
x = 42.0                        # float
x = "42"                        # string
```

<b>Note</b><br>
A variable value can be attached to a string by using '#' and curly braces around the variable name.
It can also contain operations.

```
val = 10
puts "he scored #{val} marks in English exam."
puts "he scored #{val+1} marks in English exam."
```

#### Datatype Conversion

Methods available in Ruby for this are

- to_i      # convert to integer
- to_s      # convert to string
- to_f      # convert to float

```

```

### Operations

- Addition
- Subtraction
- Multiplication
- Division
- Modulus
- Exponent

#### Short Hand Assignment

```
x+=y
x-=y
x*=y
x/=y
x%=y
x**=y
```

#### Parallel Assignment

Assigning variable values in parallel

```
x,y,z = 1,2,3
```

Swapping values

```
x,y = y,x                      # swaps x and y values.
```

### String Operations

Strings are values enclosed in single or double quotes.
Single Quotes - to escape a character, \ is used.

```
x = 'I\'m a computer programmer.'
```
Double Quotes - we can use '\n' new line in strings enclosed in double quotes.

```
x = "he is a boy. \n He is 2 years old."
```

#### String Interpolation

It means running an operation inside a string.

```
maths = 70
science = 78
x = "he scored #{maths+science} marks."
```

#### Concatenation

Adding strings to form a bigger string.

```
x = "hello"
y = "world!!"
puts x+y
# helloworld!!
```
#### Repeating a String

multiplying an integer value 'n' with a string to repeat the string n times.

```
x = "hello"
puts x*2    
# hellohello
```


## Control Structures


### Booleans

Two values:
- True
- False

There are other boolean values possible in Ruby.

- Truthy - For True and also all other values given as boolean.
<b>eg:</b>

```
"hello" - Truthy
8 - Truthy
```

- Falsey - For False and nil.

### Comparison Operators

- Equality check ==
- not equal !=
- greater >
- lesser <
- greater or equal >=
- lesser or equal <=
- eql? method for both value and type equality check.

### if statement

if evaluates a condition and if the condition is True, it evaluates the statements in the if block.
The if block is terminated using 'end' statement.

```
if condition
statements
end
```

#### else statement

else statement is evaluated when the if condition turns out to be False.

```
if condition
statements
else
statements
end
```

#### elsif statement

elsif statement is 'else if' in other languages. Its block is executed when the if conditions turns out to be false.

```
if condition
statements
elsif condition
statements
else
statements
end

```

#### unless statement

unless statement is the opposite of if statement. That is, the condition for the unless statement must be false inorder to execute the statements in the unless block.

```
unless condition #here the condition must be false inorder to execute statement1,if true,then executes the else block.
statement1
else
statement2
end
```

### Logical Operators

- (&&)  # and -  both true then true both false then false else false in all conditions.
- (||)  # or - both true then true both false then false either of them true then true.
- (!)   # not - if true then false and if false then true.

### case statements

It uses a case expression and when statements for evaluating cases.

```
days = 12
case days
when 12
 puts "12 days"
when 10
 puts "10 days"
else
 puts "invalid days"
end 
```

### Ranges

Range represents a sequence. 
There are two range operators in Ruby 

- (..)           # upper and lower limit included.
- (...)          # Lower limit not included.

```
a = (1..7).to_a
puts a
# [1,2,3,4,5,6,7]
```

<b>NOTE</b><br>
- 'to_a' method is used to explicitly convert a range into an array. 
- Range can be used in case statements together with 'when'  

### Loops

#### while

while loop executes as long as the condition specified in the while statement remains true.
Because of that the while statements must consist of a break condition so that at some point the execution of the while loop is terminated.
```
while condition
statements
 if condition
  break
 end
end
```

#### until

until statement is the opposite of while statement. That is the loop body executes if the condition is false and terminates when the condition turns out to be true.

```
until condition
statements
 if condition
  statements
 end
end
```

#### for

The for loop iterates over a range of values and executes the statement that much time the loop executes.

```
for i in (1..10)
 puts i
end
```
<b>break</b><br>
break statement exits the loop and terminates further execution of the loop.

```
for i in 1..5
 break if i>3
 puts i
end
```

<b>next</b><br>
next statement skips the cuttent iteration and moves on to the next without exiting the loop.

```
for i in 1..10
 next if i%2 == 0
 puts i
end
```

<b>redo</b><br>
This statement results in repeated execution of the current loop iteration.

<b>retry</b><br>
This statement causes the whole loop to start again from the beginning.

#### loop do

it works like a normal loop which executes according to the conditions given in its code block.If the execution is not made to stop by breaking, the loop will run for ever.

```
val = 1
loop do
 val = val+1
 puts val
 break if val>5
end
```

## Collections

### Arrays


