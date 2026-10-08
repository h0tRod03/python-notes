### Slicing Iterable Objects ---------------------------------------------------------------------------------------------------------------------------------------------------------

Slicing - gives you the ability to access more than one item or character at a time.

item_to_slice_from[start:stop:step]
	* The start:stop:step numbers are integers that represent the index values for the sequence being sliced from
	* stop value is exclusive which means it slices up to be not including the provided number
	* When using a negative step, the start has to be greater than the stop
	
		lst = ['zero', 1, 'two', 3, 'four', 5]
		print(lst[0:3]) ---> ['zero', 1, 'two']
		
		
		sentence = 'This is an example sentence.' 
		print(sentence[5:18]) ---> is an example
		
		sentence = "This is an example sentence."
		print(sentence[5:]) ---> is an example sentence.
		
		
		
### Length, Range, Sum, and Rounds Functions -----------------------------------------------------------------------------------------------------------------------------------------

	Length Function
	
	len() function returns the total number of items found inside of an iterable object.
			* len(iterable_item)
	# len() - built-in function that returns the number of elements in a collection.
	
	aStr = 'hello'
	print(len(aStr)) ---> 5
	
	aList = [1, 2, 3, 4]
	print(len(aList)) ---> 4
	
	aTuple = (1, 2, 3, 4, 5, 6)
	print(len(aTuple)) ---> 6
	
	3:lst2 = [1,2,3['a', 'b', 'c'], (9,'8',7)]
	tup_len = len(lst2[-1])
	print(tup_len) ---> 3
	
	
	-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
	
	lst1 = [1,2,3,4]
	tup1 = ('hello', 'world')
	str1 = 'Pyhton was first released in 1991'
	total = len(lst1) + len(tup1) + len(str1)
	print(total) ----> 39
	
	
	
### Range Function  ----------------------------------------------------------------------------------------------------------------------------------------------------------------

	range() function requires at least one int argument and returns a sequence of integers stored inside a literal range object type. Is it important to note that the range() 		function does NOT return a list object type.
	
	
	range(start, stop, step) 
		* The start and step values are optional. They have a default value of 0 (for start) and 1 (for step).
		* Its important to note that the stop value is EXCLUSIVE.
		* The range() function is helpful when you need a sequence of numbers.
		* creating a range object using on the stop value will default to a start value of 0 and a step of 1
		
			
			# range() - built-in function that creates a range object
			# arguments are start, stop, step where only stop is mandatory; by default start is 0 and step is 1

			print(range(10))               ---> range(0, 10)
			print(type(range(10)))         ---> <class 'range'>

			print(list(range(10)))         ---> [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]			# ordered sequence from 0 to 9
			print(list(range(1,10)))       ---> [1, 2, 3, 4, 5, 6, 7, 8, 9]  			# ordered sequence from 1 to 9
			print(list(range(1,10,2)))     ---> [1, 3, 5, 7, 9] 					# ordered sequence of odd numbers from 1 to 9
			print(list(range(10,-1,-1)))   ---> [10, 9, 8, 7, 6, 5, 4, 3, 2, 1, 0]		# ordered sequence from 10 to 0
			
	
	myString = 'Hello World'
	myStringIndices = list(range(len(myString)))
	print(myStringIndices) ---> [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
	
	
	num_lst = list(range(5,101))
	print(num_lst) ---> [5, 6, 7, 8, 9, 10, 11, ....]
	
	
	even_nums = lst(range(1,101,2))
	print(even_nums) ---> [0, 2, 4, 6, 8, 10, ...]
	
	
### Sum Function  --------------------------------------------------------------------------------------------------------------------------------------------------------	
	
	sum() function requires only ONE iterable item and returns either an int or float (depending on number types used in functions)
	
	syntax:
	sum(iterable_item) 
	
	
	# sum() - built-in Function that adds up all numbers in an iterable (every item must be a number)
	aList = [1, 2, 3, 4]
	print(sum(aList)) ---> 10

	aTuple = (1.1, 2, 3.57)
	print(sum(aTuple)) ---> 6.67
		

### Round Function --------------------------------------------------------------------------------------------------------------------------------------------------------

	round() function accepts up to two arguments and returns a float that is rounded to the level of precision (or number of decimal places) specified by the second argument, 		the digits. If the level of precision is 0, the round() returns an int.

	# round() - built-in function that rounds argument to nearest integer (up or down)
	print(round(4.3)) ---> 4
	print(round(4.6)) ---> 5
	
	
	pi = 3.141592653589793238462643383279502884197

	default = round(pi)
	print(default) ---> 3

	level_one = round(pi,1)
	print(level_one) ---> 3.1

	level_four = round(pi,4)
	print(level_four) ---> 3.1416
	
