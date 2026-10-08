### File Overview ---------------------------------------------------------------------------------

* To handle files in Python, you need to know:

open() - Opens a file so Python can work with it.
		file = open("example.txt", "r")

read() - Gets the contents of a file.
		file = open("example.txt", "r")
		contents = file.read()
		print(contents)

write() - Puts information into a file. Will overwrite whatever is currently inside.
		file = open("example.txt", "w")
		file.write("Hello world!")
		file.close()
append() - if you want to add another line,:

		file = open("example.txt", "a")
		file.write("Another line!")
		file.close()

close() - Closes the file when you're finished with it.

		file.close()
		
		
Specify -----------------------------------------------------------------------------------------

File name as string or path expression. The name/path may be absolute or relative.

- Remember, for Windows OS, the \\ is the path separator versus the / which is the path separator for Linux/Mac.

File Modes ---------------------------------------------------------------------------------------

Mode options allow for the ability to read or write to a file.

|Keyword | Description |
| :----- | :-----------|
| r | reads from file, this is used by default | 
| w | writes to a file, will overwrite if file exists |
| a | appends to a file, will not overwrite |
| x | creates a file if it does not exist |
| b | allows for reading or writing to binary |
| t | text mde, can read or write |
| w+ or r+ | file must eist, can read and write |



Reading Files ------------------------------------------------------------------------------------

# open file in read mode, and store it in a variable
file_obj = open("info.txt", "r")

# reading from a file
file_content = file_obj.read()
print(file_content)

# close the file
file_obj.close()


Output: 
Line1 Hello
Line2 World
Line3 Another
Line4 Final


-----------------------------------------------------------------------------------------------

* readline() - reads one line of the text file at a time.

			# open file in read mode, and store it in a variable
			file_obj = open("info.txt", "r")

			# reading from a file
			file_content = file_obj.readline()
			print(file_content)

			# close the file
			file_obj.close()

Output: Line1 Hello

-----------------------------------------------------------------------------------------------


with - automatically closes file. "use this thing temporarily and close it when i am done"

			with open("example.txt", "r") as file:
			    text = file.read()
			    print(text)
			    
as - gives name to file that is often easier to reference than a full file name

			with open("example.txt", "r") as file

------------------------------------------------------------------------------------------------			    
readlines() - returns the whole text file in the form of a list.

			# Opening info.txt and reading the lines
			with open("info.txt") as file_obj:
			   file_content = file_obj.readlines()
			   print(file_content)
			   
			   
	Output: ['Line1 Hello\n', 'Line2 World\n', 'Line3 Another\n', 'Line4 Final']
----------------------------------------------------------------------------------------------

# How to use readlines() without returning newline character:

# Opening info.txt and reading the lines without the new line character
with open("info.txt") as file_obj:

   file_content = file_obj.read()
   file_lines = file_content.splitlines()
   print(file_lines)
   # The splitlines() method splits a string into a list. The splitting is done at line breaks.
   
	Output: ['Line1 Hello', 'Line2 World', 'Line3 Another', 'Line4 Final']
	
---------------------------------------------------------------------------------------------	
# How to obtain words from a file. In order to do this, use the _io.TextIOWrapper method of read() to return a string. From there, we use string.split() with a space as an argument to return a list of words.


			# Opening info.txt and create a list of words
			with open("info.txt") as file_obj:
			   file_content = file_obj.read()
			   words = file_content.split(" ")
			   print(words)

			with open("info.txt") as file_obj:
			   file_content = file_obj.read().replace('\n', ' ')
			   words = file_content.split(" ")
			   print(words)
			   
	Output: ['Line1', 'Hello\nLine2', 'World\nLine3', 'Another\nLine4', 'Final']
		['Line1', 'Hello', 'Line2', 'World', 'Line3', 'Another', 'Line4', 'Final']
	
------------------------------------------------------------------------------------------------

file objects are iterable:

# we can also iterate through a file object to get one line on each iteration

			with open('info.txt', 'r') as fp:
			    for line in fp:
				print(line.strip('\n'))
				
	Output: Line1 Hello
		Line2 World
		Line3 Another
		Line4 Final
		
-----------------------------------------------------------------------------------------------
write() - writes a single string to a file.
writelines() writes list of strings to a file, does not add new lines.
-----------------------------------------------------------------------------------------------
'w' mode when opening file
	
	# write() - method for writing a string to a file; file must have been opened in a mode supporting write

# 'w' mode will create the file if it does not exist; if it exists it will truncate the file
data = [("California", 39937489, "Sacramento"),
       ("Texas", 29472295, "Austin"),
       ("Florida", 21992985, "Tallahassee")]

with open("info.txt", "w") as data_obj:
       for state, population, capital in data:
           data_obj.write(f'{state}, {population}, {capital}\n')
------------------------------------------------------------------------------------------------
'a' mode when opening file

# 'a' mode will create the file if it does not exist; if it exists it will append to the end of the file

			with open('info.txt', 'a') as fp:
			    fp.write('Here is another line\n')

			with open('info.txt', 'r') as fp:
			    print(fp.read())         
           
------------------------------------------------------------------------------------------------           
