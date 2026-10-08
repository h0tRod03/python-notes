### Loops ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

While Loops -----------------------------------------------------------------------------------------------------------------------------------------------------------

* The while statement causes Python to loop through a suite of statements if the test expression evaluates to True.

* The while statement uses the same evaluations for True and False as the if statement. 

* Likewise, the same indenttation rules are used for a while as the if statement.

* Each time through the loop, if the condition is the while is True, then the body of the while loop is executed.

* While loops often require the ise of a counter variable.
	* When this is the case, remember to incrememnt the counter variable to prevent an infinite loop!
	 
	 
					# Declaring a counter
					counter = 1

					# While the counter is less than or equal to 5 print counter
					while counter <= 5:
					    print(f'Loop iteration: {counter}')
					    counter += 1  #update the counter to prevent infinite loop
					    
					   
					  --->	Loop iteration: 1
						Loop iteration: 2
						Loop iteration: 3
						Loop iteration: 4
						Loop iteration: 5	
					    

* While loops REQUIRE a True condition in order to execute the instructions inside
* When executing a while True loop, you must include a break in the loop somewhere to prevent an infinite loop from happening.

### Break ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------



* Any looping construct can have its control flow changed through a break statement within it.

* When a break is executed, control of the program jumps to the first statement beyond or outside the loop.

* A break is often used when searching through a collection for thr occurrence of a particular item.

					uiList = []
					
					while True:
						ui = input('Enter some characters or simply enter to stop: ')
						if not ui:
							break
						uiList.append(ui)
						
					print(uiList)
					
continue Statement ------------------------------------------------------------------------------------------------------------------------------------------

					# the continue statement will immediately end the current iteration of the loop 
					# and go to the next iteration (if the loop condition is still True)

					# use a while loop to append only single digit odd numbers to a list

					oddList = []
					num = 0

					while num < 10:
					    num += 1
					    if num % 2 == 0:
						continue
					    oddList.append(num)

					print(oddList)	         ---> [1, 3, 5, 7, 9]		 		
					
For Loops -------------------------------------------------------------------------------------------------------------------------------------


* The for loop in Python is used to iterate over the items of any sequence, such as a str, list, tuple, or iterable object.
* The generic syntax of a for loop is: for target in sequence: suite
* Each item in the sequence is evaluated once and assigns the item to target and then the suite is executed.
* The loop terminates after processing the last item in the sequence.

* Any time you need to do something with each or every item in a list or str or any other iterable item, think for loop.

		for every_item in iterable_item
		
Using Range and Length Functions Together -----------------------------------------------------------------------------------------------------------------------------------------

Isolating and Identifying Index Positions

range(len()) 

Using the `range()` and `len()` functions together is helpful when needing to iterate over a collection of items while also identifying which index position each item is in.


Enumerate Function -------------------------------------------------------------------------------------------------------------------------------------------------------------

enumerate() accepts up to two arguments and is a fucntion that retunrs an enumerate object that assigns numbers to each item found in an iterable object.

This built-in function is another way of accomplishing what the range(len()) function can also do.

enumerate() can be given a start int; by default when no int is supplied the function begins numbering items at 0.


Syntax:
enumerate(iterable, start=0)


The `enumerate()` function is like the `range()` function that creats a range object that by itself is not abundantly helpful. However, combining it with a `list()` conversion function or using it inside a `for` loop leverages the usefulness of this built-in function.



reverse items in a list:


							def reverseit(): # define function
							    result = []  # empty list to store results
							    while True:  # stores user input
								rit = input()
								
								if rit == '': # prevents infinite loop through conditional 
								    break
								result.append(rit[::-1]) # reverses items in list. (list).change(user input)[::-1])
							    return result 


edit individual items in a list:


							def leetString(s):
							    result = ""
							    for i in range(len(s)):
								if i % 2 == 0:
					    result += s[i].upper()
								else:
								    result += s[i].lower()
								    
							    return result



print evens and odds separately:


							def evensandodds(first, last):
							   even = []
							   for num in range(first, last +1):
							       if num % 2 == 0:
								   print(num)
								   
							   for num in range (first, last +1):
							       if num % 2 != 0:
								   print(num)
       



return list in equal parts:

							def disect(lst):
							    middle = len(lst) // 2
							    first = lst[:middle]
							    last = lst[middle:]
							    return (first, last)
							    
							    
							    


round #s:


							def round_to_position(lst):       # Defines a function called round_to_position; lst is the list we give it
							    new1 = []                     # Creates an empty list where we will store the rounded numbers

							    for i in range(len(lst)):     # Loops through each position (index) in the list: 0, 1, 2, 3, ...
								new1.append(round(lst[i], i))  # Rounds the number at position i and adds it to new1

							    return new1                   # Gives back the completed list


