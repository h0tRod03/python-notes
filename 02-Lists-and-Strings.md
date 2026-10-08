### Indexing Through Iterable Items ---------------------------------------------------------------------------------------------------------------------------------------------------


	# Indexing allows us to access individual items in an ordered collection (string, list, tuple)
	# Python uses 0-based indexing: the first time is index 0, the second item is index 1, ...
	# Python also allows negative indexing: the last item is index -1, the second to last time is index -2, ...

		#          01234
	     	aString = 'hello'
		print(aString[0]) ---> h
		print(aString[4]) ---> o
		print(aString[-5])---> h
		print(aString[-1])---> o
		
What about a list in a list or a list with multiple strs?

		word_lst = ['cyber','is','so','much','fun']
		# print the letter "s" in the word "so"
		print(word_lst[2][0])
		
		
### Modifying, and methods of Lists and Tuples ----------------------------------------------------------------------------------------------------------------------------------------

Modify a list:

		# Mutability
		# list is an ordered sequence that is mutable

		a = [1,2,3,4,5]
		print(a)                             ---> [1,2,3,4,5]

		# modify a list with item assignment
		a[0] = 9
		print(a)                             ---> [9,2,3,4,5]
		
		
                                                  *********You cannot modify a string or tuple with item assignment*********

### List Methods -------------------------------------------------------------------------------------------------------------------------------------------------------------------

#append(item) - adds new element to the end of the list, increasing length by one
#count(item) - return total number of time item is found inside the list
#extend(iterable) - adds each listed in the iterable to the end of the list. 

		# Using extend(iterable)
		numbers = [1, 2, 3]
		numbers.extend([4, 5, 6,])
		print(numbers)             ---> [1, 2, 3, 4, 5, 6]
		
#insert(index, item) - adds specified item at sepecified index position. I,e. insert(1,4) puts the number 1 in the 4th spot.
#pop(index) - deletes the element at the specified index or the end if no index is provided.
#remove(value) - deletes the first instance of the specified value.


.append Method

		#append Method - add an item to the end of the list
		aList = [1,2,3,4]
		print(aList)
		aList.append(5)
		print(aList)      ---> [1, 2, 3, 4, 5]
		
.extend Method

		#extend Method - add one list onto the end of another list
		aList = [1, 2, 3, 4]
		bList = [5, 6, 7, 8]
		aList.extend(bList)
		print(aList)         ---> [1, 2, 3, 4, 5, 6, 7, 8]
		
.insert Method

		#insert Method - insert value into a list at the index position
		lst - [1, 2, 3]
		lst.insert(0, 'zero')
		print(lst)            ---> ['zero', 1, 2, 3]
		
.remove Method		
		
		#remove Method - removes and returns item at index provided as argument
		aList = [1, 2, 2, 3]
		aList.remove(2)
		print(aList)         ---> [1, 2, 3]	
		
del keyword

		#del is a keyword to delete items from the list
		lst = [1, 2, 3]
		del lst[0]
		print(lst)      ---> [2, 3]
		
.pop Method
		
		#pop() Method - removes and returns item at index provided as argument (default is last item)
		aList = [1, 2, 3, 4]
		a = aList.pop(0)
		print(a)             --->  1
		print(aList)         ---> [2, 3, 4]
		b = aList.pop() ---- (Since nothing was indexed, it will default to last item in list)
		print(b)             --->  4
		print(aList)         ---> [2, 3]
		
.count Method

		#count() Method - returns the number of occurences of the argument in the list
		aList = [1, 4, 4, 3]
		print(aList.count(1)) ---> 1
		print(aList.count(4)) ---> 2
		print(aList.count(5)) ---> 0
		
		
### Tuple Methods -------------------------------------------------------------------------------------------------------------------------------------------------------------------
		

# Tuples are NOT mutable ans cannot be changed using methods.
	*count(item) - returns the total number of times the item is found inside the tuple
	*index(item) - returns the index position of the item
	
.count Method

		tup = (9,8,7,9,8,7)
		tup.count(9)
		nine_count = tup.count(9)
		print(nine_count)        ---> 2
		
.index Method

		tup = (1, 2, 3)
		tup.index(2)       #Note: The returned index number can be saved as variable if needed
		where_is_2 = tup.index(2)
		print(where_is_2)        ---> 1
		

Make changes to a tuple
#Scenario: Joe Smith is being reassigned to Ft. Gordon and his record needs to be updated.

		soldier_123 = ('Joe', 'Smith', '17A', 'Ft. Meade')
		soldier_123 = list(soldier_123) #converting to a list IOT access mutable properties
		soldier_123[-1] = 'Ft. Gordon'
		soldier_123 = tuple(soldier_123) # converting back to tuple IOT lockdown/ deny mutability
		print(soldier_123)
		
		
### List Methods  -----------------------------------------------------------------------------------------------------------------------------------------------------		
		
		
	#Strings in python are an immutable sequence of 0+ characters. 
	#Raw strings - putting a r or R infront of the string to treat the characters exactly as typed.

		"hello\nworld" would normally print as hello
		                                       world
		 r\"hello\nworld" would print as hellonworld		                                       		

#String Casing methods

	#upper() - returns copy of string with all cased characters converted to uppercase
	#lower() - returns copy with all cased characters converted to lowercase
	#casefold() - similar to lower(), will also convert unicode characters to lowercase. (will target alphanumeric characters of other spoken languages)
	#title() - returns copy of str with the first letter of each word being capatalized as seen in a title
	#capitalize - returns copy of str with the first letter capitalized
		
		string = "python is fun"                                                        
		print("String is now upper:", string.upper()) 
		print("String is now lower", string.lower())
		print("String is now casefold:", string.casefold())
		print("String is now title:", string.title())  
		print("String is now capitalized:", string.capitalize())
		
#Finding Substrings -----------------------------------------------------------------------------------------------------------------------------------------------------	
		
	count(s) - returns number of times value is found within string
	index(s) - returns the index position of the first instance of value. Will raise ValueError if value is not found in string.
	find(s) - similar to index, but will return -1 when the sub-string is not found
		
#Methods To Create Modified Copies of Strings

	#strip() - remove any leading and trailing whitespace from str
	#lstrip - remove white space to left
	#rstrip() - remove white space to right
		
		aStr = '    characters     '
		print(aStr)     p            --->____characters____     (#_ denotes whitespace in this example)
		print(aStr.strip())         ---> characters
		
		bStr = 'www.example.com'
		print(bStr.strip(w.com))    ---> example
		
		
		#replace(old, new) - replace all instances of first parameter with instances of second parameter.
			* optional third parameter can be used to specify the number of times replacement is to be made.
		
		aStr = '192.168.68.101'
		print(aStr.replace('.','+') ---> 192+168+68+101
		
		
#Splittling and Joining Strings Working With Lists

	.split() - returns a list of original string elements separated by index item specified (default value is whitespace)
		* it is important to note that item porvided to .split() will be removed entirely from string
		
		aStr = 'This is a sentence'
		print(aStr.split(' '))      ---> ['This', 'is', 'a', 'sentence']
		print(aStr.split())         ---> ['This', 'is', 'a', 'sentence']

		csvString = 'This,might,be,what,a,csv,file,looks,like'
		print(csvString.split(',')) ---> ['This', 'might', 'be', 'what', 'a', 'csv', 'file', 'looks', 'like']

		aMACaddress = '07:bb:21:3d:a9:29'
		print(aMACaddress.split(':')) ---> ['07', 'bb', '21', '3d', 'a9', '29']

		anIPaddress = '192.168.68.101'
		print(anIPaddress.split('.')) ---> ['192', '168', '68', '101']

		full_name = 'Joe Smith'
		fname = full_name.split()[0]
		lname = full_name.split()[1]
		print(fname)                 ---> Joe
		print(lname)		      ---> Smith
		
		
	.join Method
	
		#join() method - construct a string from a list where each list element is separated by the given string 
		
		myStr = 'line tree'  
		print(myStr)        ---> line tree
		
		myStrList = list(myStr)
		print(myStrList)    ---> ['l', 'i', 'n', 'e', ' ', 't', 'r', 'e', 'e']
		
		myStrList[0] = 'p'
		print(myStrList)    ---> ['p', 'i', 'n', 'e', ' ', 't', 'r', 'e', 'e']
		
		myStr = ''.join(myStrList)
		print(myStr)        ---> pine tree
		
		
		anIPaddress = '192.168.68.101'
		print(anIPaddress)            ---> 192.168.68.101

		anIPaddressList = anIPaddress.split('.')
		print(anIPaddressList)        ---> ['192', '168', '68', '101']
		anIPaddressList[-1] = str(int(anIPaddressList[-1])+1)
		print(anIPaddressList)        ---> ['192', '168', '68', '102']

		anIPaddressReassembled = '.'.join(anIPaddressList)
		print(anIPaddressReassembled) ---> 192.168.68.102
		
		
		
		
		
#is METHODS for Strings ---------------------------------------------------------------------------------------------------------------------------------------			
		
#Methods can be used to validate if a string contains a certain set of characters, when the method validates it will return True or Flase
	
	*isdigit() - returns True if all characters are digits
	*islower() - returns True if all characters are lowercase
	*isupper() - returns True if all characters are uppercase
	*isalnum() - returns True if all characters are alphanumeric		
		
		
#Escape Characters ---------------------------------------------------------------------------------------------------------------------------------------			
		
| sequence | Character/Meaning |
| :------- | :---------------- |
| \newline | Ignored           |
| \\       | Bckslash          |
| \'       | Single Quote      |
| \"       | Double Quote      |
| \a       | ASCII Bell(Bel)   |
| \b       | Backspace         |
| \f       | form feed         | 
| \n       | newline/Line feed |
| \r       | Carriage Return   |
| \t       | Horizontal Tab    |
| \v       | Vertical Tab      |
| \ooo     | ASCII Character(octal value ooo) |
| \xhhh    | ASCII Character (Hex Value hhh)  |
| \uxxxx   | Unicode Character with 16-bit hex alue xxxx |
| \Uxxxxxxx | Unicode Character with 32-bit hex value xxxxxxx |

	
		single_quote = "This is a \'single quote\'" # The string will escape char for a single quote
		print(single_quote) ---> This is a 'single quote'

		new_line = "This: \n will produce a newline." # The string will produce a newline at the end of it
		print(new_line) ---> This: 
 					will produce a newline.

		tab = "This is a \t tab" # The string will add a tab
		print(tab) ---> This is a 	 tab

		chess_piece = "\U0000265F" # Use unicode to create a chess piece
		print(chess_piece) ---> ♟	
				
		
			
#String Formating -----------------------------------------------------------------------------------------------------------------------------------------------------


#f-string - (formatted string literals)

		coding_language = "Pyhton"
		print(f'{coding_language} is fun') ---> Python is fun
		
		------------------------------------------------------
		
		coding_language = "Python"
		audience = "Students"
		long_string = f"{coding_language} is fun. {audience} seem to enjoy learning {coding_language}"
		print(long_string) ---> Python is fun. Students seem to enjoy learning Python

# When using f-strings, a format specifier can be appended to the field after a colon (:) and inside the curly braces {}.

| Type |  Meaning |
| :----| :-------- |
| s  | String format. This is the default type for strings and may be omitted. |
| none | The same as 's'. |
| b  | Binary Format. The Number is display as base 2. |
| c  | Character. Converts the integer to a Unicode Character. |
| d  | Decimal Integer. This converts the number to base 10.   | 
| x or X | Hex format. Display the number in base 16. The case of the hex number will match the case of the specifier. |
| f | Fixed point number. Displays the number with a decimal point. Default precision is 6. |
| % | percentage. Multiplies the number by 100 and displays in fixed ('f') fromat with a percent sign. |



			PI = 3.14159
			print(f"PI is now 2 decimal places: {PI:.2f}") ---> PI is now 2 decimal places: 3.14

			PI = 3.14159
			print(f"PI is now 4 decimal places: {PI:.4f}") ---> PI is now 4 decimal places: 3.1416

			num = .5
			print(f"num is now a percentage: {num:%}") ---> num is now a percentage: 50.000000% (default is 6 if no value is entered)

			print(f"num is now 2 decimal places: {num:.2%}") ---> num is now 2 decimal places: 50.00%


.format Method --------------------------------------------------------------------------------------------------------------------------------------------------------------------

# str.format() - uses curly braces in a template string to make where the output should be replaced. The sytax to create a literal string with fields marked with curly braces {} wgere you want the output to appear.

			
			name = 'Smilla'
			pet = 'dog'
			myString = 'I have a {} whose name is {}.'.format(pet, name)
			print(myString) ---> I have a dog whose name is Smilla.

			pi = 3.14159
			aStr = 'Pi rounded to four decimal places is {:.4f}.'.format(pi)
			print(aStr) ---> Pi rounded to four decimal places is 3.1416.

			# alternately can use f-strings
			myString = f'I have a {pet} whose name is {name}.'
			print(myString) ---> I have a dog whose name is Smilla.

			aStr = f'Pi rounded to four decimal places is {pi:.4f}.'
			print(aStr) ---> Pi rounded to four decimal places is 3.1416. 


.zfill() Method ----------------------------------------------------------------------------------------------------------------------------------------------------------------



#.zfill() - zero fill this string util it reaches x length.

			string.zfill()




























capitalize()	Converts the first character to upper case
casefold()	Converts string into lower case
center()	Returns a centered string
count()	Returns the number of times a specified value occurs in a string
encode()	Returns an encoded version of the string
endswith()	Returns true if the string ends with the specified value
expandtabs()	Sets the tab size of the string
find()	Searches the string for a specified value and returns the position of where it was found
format()	Formats specified values in a string
format_map()	Formats specified values in a string
index()	Searches the string for a specified value and returns the position of where it was found
isalnum()	Returns True if all characters in the string are alphanumeric
isalpha()	Returns True if all characters in the string are in the alphabet
isascii()	Returns True if all characters in the string are ascii characters
isdecimal()	Returns True if all characters in the string are decimals
isdigit()	Returns True if all characters in the string are digits
isidentifier()	Returns True if the string is an identifier
islower()	Returns True if all characters in the string are lower case
isnumeric()	Returns True if all characters in the string are numeric
isprintable()	Returns True if all characters in the string are printable
isspace()	Returns True if all characters in the string are whitespaces
istitle()	Returns True if the string follows the rules of a title
isupper()	Returns True if all characters in the string are upper case
join()	Joins the elements of an iterable to the end of the string
ljust()	Returns a left justified version of the string
lower()	Converts a string into lower case
lstrip()	Returns a left trim version of the string
maketrans()	Returns a translation table to be used in translations
partition()	Returns a tuple where the string is parted into three parts
replace()	Returns a string where a specified value is replaced with a specified value
rfind()	Searches the string for a specified value and returns the last position of where it was found
rindex()	Searches the string for a specified value and returns the last position of where it was found
rjust()	Returns a right justified version of the string
rpartition()	Returns a tuple where the string is parted into three parts
rsplit()	Splits the string at the specified separator, and returns a list
rstrip()	Returns a right trim version of the string
split()	Splits the string at the specified separator, and returns a list
splitlines()	Splits the string at line breaks and returns a list
startswith()	Returns true if the string starts with the specified value
strip()	Returns a trimmed version of the string
swapcase()	Swaps cases, lower case becomes upper case and vice versa
title()	Converts the first character of each word to upper case
translate()	Returns a translated string
upper()	Converts a string into upper case
zfill()	Fills the string with a specified number of 0 values at the beginning




