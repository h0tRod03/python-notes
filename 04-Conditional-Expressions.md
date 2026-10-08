### Relation vs. Logical vs. Membership Operators

		* Relational, logical, and membership operators yield results of either True/ Flase
		* True - any non-zero
		* Flase - 0, empty: disctionaries, tuples, or lists
		
		
***Relational & Comparison Operators***
										
										
 | Operator | Meaning |
| :------- | :------ |
| <        | Strictly Less than |
| <=       | Less than or Equal |
| >        | Strictly Greater Than |
| >=       | Greater than or Equal |
| ==       | Equal                 |
| !=       | Not Equal             | 
| is       | Object identity       |
| is not   | Negated Object identity |
| in       | Collection Membership |
| not in   | Negated Collection Membership |


#bool
print(type(True))
print(type(False))

#relational / comparison operators -------------------------------------------------------------------------------------------------------------------------------------------------

a = 4
a = 3
print(a == b)   # equality ---> False
print(a < b)    # less than ---> False
print(a > b)    # greater than ---> True
print(a != b)   # not equal ---> True
print(a <= b)   # less than or equal --->  False
print(a >= b)   # greater than or equal ---> True


# collection membership  --------------------------------------------------------------------------------------------------------------------------------------------------------------
print('e' in 'hello') ---> True
print('f' in 'hello') ---> False
print(1 in [1, 2, 3, 4]) ---> True
print(5 in [1, 2, 3, 4]) ---> False

print('e' not in 'hello') ---> False
print('f' not in 'hello') ---> True
print(1 not in [1, 2, 3, 4]) ---> False
print(5 not in [1, 2, 3, 4]) ---> True


# object id match ----------------------------------------------------------------------------------------------------------------------------------------------------------------
a = 4
b = 3
print(id(a)) ---> 9789056
print(id(b)) ---> 9789024

print(a is a) True
print(a is b) False

print(a is not a) False
print(a is not b) True

c = 4
print(id(a)) 9789056
print(id(c)) 9789024

print(a is c) False

print(a is not c) True

# Logical Operators ----------------------------------------------------------------------------------------------------------------------------------------------------------------

| Operator | Unary or Binary | The Result is True When... |
| :------- | :-------------- | :--------------------------|
| not      | unary           | Operand is False           |
| and      | binary          | Both Operands Must be True |
| or       | binary          | Only one Operand needs to be True |

and Truth Table

| X  AND | Y    | Evaluates To:  |
| :----- | :--- | :------------- |
| True   | True | True           |
| True   | False| False          |
| False  | True | False          |
| False  | False| False          | 


# and logical operator
print(True and True) ---> True
print(True and False) ---> Flase
print(False and True) ---> Flase
print(False and False) ---> False

timeInRank = True
enoughPromotionPoints = False

elligibleForPromotion  = timeInRank and enoughPromotionPoints

print(f'SGT Smith elligble for promotion: {elligibleForPromotion}') ---> SGT Smith elligble for promotion: False


or Truth Table

| X  OR  | Y    | Evaluates To:  |
| :----- | :--- | :------------- |
| True   | True | True           |
| True   | False| True           |
| False  | True | True           |
| False  | False| False          |






| X  OR  | Y    | Evaluates To:  |
| :----- | :--- | :------------- |
| True   | True | True           |
| True   | False| True           |
| False  | True | True           |
| False  | False| False          |

# or logical operator
print(True or True) ---> True
print(True or False) ---> True
print(False or True) ---> True
print(False or False) ---> False

ballThrownToFirstBeforeRunner = True
runnerTaggedByBallBeforeFirst = False

runnerIsOut = ballThrownToFirstBeforeRunner or runnerTaggedByBallBeforeFirst

print(f'The batter is out: {runnerIsOut}') ---> The batter is out: True




not Truth Table 

| X | NOT X Evaluates To: |
|---|---------------------|
| True | False |
| False | True |




# not logical operator
print(not(True)) ---> False
print(not(False)) ---> True

minesPresent = False

safeToProceed = not(minesPresent)

print(f'The platoon may proceed through the obstacle: {safeToProceed}') ---> Thee platoon may proceed through the obstacle: True



Operator Order of Precedence

| Order | Operator | Comments |
|-------|----------|----------|
| 1     | ()       |          |
| 2     | **       |right to left |
| 3     | *,/,//,% | left to right |
| 4     | +,-      | left to right | 
| 5     |==,!=,<=,>=,<,>,is,is not, in, not in | left to right |
| 6     | not      | left to right |
| 7     | and      | left to right |
| 8     | or       | left to right | 



###Identify Pythonic Code Blocks


- Python mandates the use of indenting within a compound statement. The first line of the compound statement is referred to as the header.

- All other statements within the compound statement are referred to as the suite or body and must be indented the same number of columns to be part of the same suite.

- The suite ends with the first statement that is “indented” to the column of the header.

- One such type of compound statement is a control structure.

- Suites must be indented the same amount of white space from the starting column of the header.

- If tabs are used in the source code, a single tab is not equal to the number of spaces used in a tab.

- It is recommended that spaces be used over tabs.


### Conditionals (Branching or Selection Statements)

if: - The fundamental decision making control structure. Code inside an if suite is only executed if a given condition is True. Required to use : at the end.


number = 25

if number <= 25:
	print("number is smaller or equal to 25") ---> number is smaller or equal to 25
-----------------------------------------------------------------------------------------------	
lst = [1,2,3,4,5]

	if 5 in lst:
		print('5 is found in lst') ---> 5 is found in lst
-----------------------------------------------------------------------------------------------		
		
if 50 in lst:
	print('50 found in lst') ---> nothing will print, there is no else statement.
	
------------------------------------------------------------------------------------------------	
	

condition = True

	if condition:
		print('this line will display if the condition is True.') ---> this line will display if the condition is True.
		
	print('this line always displays') ---> this line always displays
	
-------------------------------------------------------------------------------------------------

ui = input('Enter an integer:  ')
if ui.isdigit():
	print(f'The integer you enterred is {int(ui)}')
	
-------------------------------------------------------------------------------------------------

else - useful when zero specified conditions are met.

lst = [1,2,3,4,5]

if 50 in lst:
	print('50 found in lst')
else:
	print('50 was not found')	
-------------------------------------------------------------------------------------------------	

condition = True

if condition:
	print('this line will display if the condition is True.')
else:
	print('this line will display if the condition is False.')
	
print('this line always displays.')

-------------------------------------------------------------------------------------------------

ui = input('Enter an integer:  ')
if ui.isdigit():
	print(f'The integer you entered is {int(ui)}') 
else:
	print(f'{ui} is not an integer!')
	
--------------------------------------------------------------------------------------------------

elif 

* When writing an if statement, there can be zero or more elif blocks and the else block is optional.
* the keyword elif can be used to prevent the test of multiple if statements when only one of the if statements can ever be true at a time.
* It can also sometimes prevent the need for nesting if statements inside of an else. 
* elif gives the opportunity to have multiple conditional checks. 
* When one conditional check results in True, the True part of the suite is executed and the rest of the elif statements are skipped.

--------------------------------------------------------------------------------------------------
number = 25

if number <= 25:
	print("number is smaller or equal to 25")
	
elif number == 50:
	print("number is 50")
	
elif number <= 75:
	print("number is less than or equal to 75")
	

else:
	print("number is greater than 75")
-----------------------------------------------------------------------------------------------------

# correct logic

grade = 100

if grade >= 90:
    print('You got an A')
elif grade >= 80:
    print('You got a B')
elif grade >= 70:
    print('You got a C')
elif grade >= 60:
    print('You got a D')
else:
    print('You failed.')
    
-------------------------------------------------------------------------------------------------------





