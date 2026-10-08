# Python Fundamentals

  * print() - provides a copy of items in ().
  * type() - built-in function that returns the type of value that is the argument.
            x = Rod
            print(tyoe(x))

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	
# int - A whole number with no decimal or fractional value. Unbounded, or has no max value. 


# float - (floating point) number with a decimal. 

# help() - will provide help on provided 

### Numerical or Mathematical Operations With Ints and Floats ------------------------------------------------------------------------------------------------------------

    "| Operation |               Result              |\n",
    "| --------- | ----------------------------------|\n",
    "| x + y     | Sum of x and y                    |\n",
    "| x - y     | difference of X and Y             |\n",
    "| x * y     | Product of X and Y                |\n",
    "| x / y     | Quotient of x and Y               |\n",
    "| x // y    | Floored (integer) Quotient of X and Y   |\n",
    "| x % y     | Modulus: The remainder of x / y   |\n",
    "| x ** y    | x raised to the y power           |\n",
    "| -x        | x negated                         |\n",
    "| +x        | x unchanged                       |\n",
    "| abs(x)    | Absolute Value(or magnitude of x) |\n"
    
### Mathematical Operators --------------------------------------------------------------------------------------------------------------------------------------------------------

    "print(a + b)    # addition\n",
    "print(a - b)    # subtraction\n",
    "print(a * b)    # multiplication\n",
    "print(a / b)    # division\n",
    "print(4 / 2)    # division always results in a float\n",
    "print(a // b)   # integer division\n",
    "print(a % b)    # modulo division\n",
    "print(a ** b)   # exponentation"
    
### Boolean -----------------------------------------------------------------------------------------------------------------------------------------------------------------

# bool - data type can hold only the values 0 or 1. True = 1, False = 0. Anything other than 0.

### String & Literal String -------------------------------------------------------------------------------------------------------------------------------------------------------
str - string, sequence of characters (upper and lowercase alphabetical characters, numers, or special) surrounded by quotation marks. ("G3T$")
	* may also be refered to as a string literal. A literal is a basic value.
	* Immutable, cannot be changed once created. Sequence of zero or more characters.
# len - can be used to determine the number of characters the string contains.

# strings denoted in three ways: single quote, double quote, triple quotes
print('This string is formed by single quotes.')
print("This string is formed by double quotes, which is neat don't you think?")
print('''He shouted, "This string is formed by triple quotes, ma'am!"''')

# triple quote strings can extend to multiple lines
# these are sometimes used to make multi-line comments
print('''one
two
three
four''')

'''
This
is
a
multi-line
comment
'''

### Various Excape Character Meanings ----------------------------------------------------------------------------------------------------------------------------------------------

| Sequence | Character/Meaning |
| ------- | ---------------- |
| \        | Line Continuation |
| \\       | Backslash         |
| \'       | single Quote      |
| \"       | Double Quote      |
| \a       | ASCII Bell(BEL)   |
| \b       | Backspace         |
| \f       | Form Feed         |
| \n       | Line feed         |
| \r       | Carriage Return   |
| \t       | Horizontal Tab    |
| \v       | Vertical Tab      |
| \ooo     | ASCII Character (octal value ooo)|
| \xhhh    | ASCII Character (hex value hhh) |
| \uxxxx   | Unicode Character with 16-bit hex value xxxx |
| \Uxxxxxxxx| Unicode Character with 32-bit hex value xxxxxxxx | 

### Examples -----------------------------------------------------------------------------------------------------------------------------------------------------------------

# more on strings - escape character (backslash)
print('This string is formed by single quotes, but includes a contraction, wouldn\'t you agree?')
print('This string includes a new line.\nThis sentence is on the next line!')
print('Part 1\n\tSection A\n\t\ti. bullet 1\n\t\tii. bullet 2')
print('Happy Face Emoji:', '\u263A' ) # 16-bits
print('Pensive Face Emoji:', '\U0001F614' ) # 32-bits


### List -----------------------------------------------------------------------------------------------------------------------------------------------------------------

list([]) - ordered collection of 0 or more elements. 

### Tuple -----------------------------------------------------------------------------------------------------------------------------------------------------------------

tuple() - similar to lists as they can hold multiple items of varying data types separated by commas, they are immutable.
!!! Must add comma after item or Python will interpret as mathematical operator

### NoneType -----------------------------------------------------------------------------------------------------------------------------------------------------------------

print(type(None)) - none means nothing and will evaluate to false in a conditional statement. Often used to check the result of some action or to ensure a variable has value and is not nothing.

### Python Keywords -----------------------------------------------------------------------------------------------------------------------------------------------------------

Pyhton Keywords - reserved words. These words cannot be used as names of variables or functions.
help('keywords') - will generate table of keywords NOT to use.


|               |               |    Avoid     |                 |                 |
| ------------  | ------------- | ------------ | ----------------| ----------------|
| ```False```   | ```class```   | ```finally```| ```is```        |  ```return```   |
| ```None```    | ```continue```| ```for```    | ```lambda```    |  ```try```      |
| ```True```    | ```def```     | ```from```   |  ```nonlocal``` |  ```while```    |
| ```and```     | ```del```     | ```global``` |  ```not```      | ```with```      |
| ```as```      | ```elif```    | ```if```     |  ```or```       |  ```yield```    |
| ```assert```  | ```else```    | ```import``` | ```pass```      |  ```break```    |
| ```except```  | ```in```      | ```raise```  |                 |                 |

### Variables ----------------------------------------------------------------------------------------------------------------------------------------------------------------------

Python Identifier - name that is used to identify variables, functions/ methods, classes, or modules.
	* Must start with a letter of the alphabet or _
	* This can be followed by more letters, digits, or _
	* Identifier names cannot consist of any other characters
	* Variable and function names typically begin with a lowercase letter 
	* Class names typically begin with uppercase
	
snake_case - use of underscores between multi-word names (my_number)
CamelCase - capitalizing the first letter of each word with no spaces (MyNumber)

id() - function returns a unique identifier of an object thats referenced by a particular varible

### Augmented Assignment Operators with Math ---------------------------------------------------------------------------------------------------------------------------------------

Augmented assingment is when we want to perform a operation and capture the result of that operation inside our variable.


| Operation |               Result                            |
| --------- | ------------------------------------------------|
| x += y     | Sum of x and y assigned to x                   |
| x -= y     | difference of X and Y assigned to x            |
| x *= y     | Product of X and Y assigned to x               |
| x /= y     | Quotient of x and Y assigned to x              |
| x //= y    | Floored Quotient of X and Y  assigned to x     |
| x %= y     | Remainder of x / y  assigned to x              |
| x **= y        | x to the power of y assigned to x          |


 ### int Function ---------------------------------------------------------------------------------------------------------------------------------------

# type conversion - convert a value from one type to another
# int() - attempt to convert to int type
print(int(1))     # int to int [1]
print(int(True))  # bool to int [1]
print(int(3.1))   # float to int [3]
print(int('3'))   # str to  int [3]

### float Function ---------------------------------------------------------------------------------------------------------------------------------------

# float() - attempt to convert to float type
print(float(3.1))   # float to float [3.1]
print(float(1))     # int to float [1.0]
print(float(True))  # bool to float [1.0]
print(float('3.3')) # str to float [3.3]

### str Function ---------------------------------------------------------------------------------------------------------------------------------------

# str() - convert to string type
print(str('hello'))     # str to str [hello]
print(str(1))           # int to str [1]
print(str(1.1))         # float to str [1.1]
print(str(True))        # bool to str [True]
print(str([1, 2, 3]))   # list to str [1, 2, 3]
print(str((1, 2, 3)))   # tuple to str (1, 2, 3)

### list Function ---------------------------------------------------------------------------------------------------------------------------------------
(tuple is the same, just swap list with tuple. tuple() will not succeed if the value is not iterable)
# list() -  attempt to convert to list type
print(list([1, 2, 3]))  # list to list [1, 2, 3]
print(list('hello'))    # str to list ['h', 'e', 'l', 'l', 'o']
print(list((1, 2, 3)))  # tuple to list [1, 2, 3]


### bool Function ---------------------------------------------------------------------------------------------------------------------------------------

# bool() - convert to bool type
print(bool(True))       # bool to bool [True]
print(bool(1))          # int to bool [True]
print(bool(0.0))        # float to bool [False]
print(bool('hello'))    # str to bool [True]
print(bool([]))         # list to bool [False]
print(bool((1, 2, 3)))  # tuple to bool [True]


### Print and Input Functions ---------------------------------------------------------------------------------------------------------------------------------------

# more on print() function
# print() takes a variable number of arguments

# by default the comma will generate a space in the output
print('hello', 'world') 

# can change this with 'sep' keyword argument
print('hello', 'world', sep='+')

# by default print() adds a newline; can change this with the 'end' keyword argument
print('hello world', end=' ')
print('hello world')

### Prompt a User for Input ---------------------------------------------------------------------------------------------------------------------------------------

input() - collects input from users. Initiates a prompt to the user and returns a str of user entered data. It is also important to note that any input collected must be assigned to a variable if you would like to save it or manipulate it in any way.

# input() function -  used to get input from the user via the keyboard
# optional argument is the prompt: this is a message outputed to the screen

a = input('Enter something for me: ')
print(a)


# input() always returns a string

a = input('Enter an integer: 4 ')
print(a)
print(type(a))


# If we want to do math, then we must convert the user input
a = input('Enter the first integer: ')
b=  input('Enter the second integer: ')
add = int(a) + int(b)
print('The sum of the two integers is', add)
prod = int(a) * int(b)
print('The product of the two integers is', prod)
