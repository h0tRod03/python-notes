### Function Definitions --------------------------------------------------------------------------------------------------------------------------------------------------------------

Creating Functions

		#def _____(a,b) - used to define a new function. Function must be defined before called. We create functions to group code that we are going to call multiple times - 			(i.e, write the code once, run it multiple times)
		
		
				def multiply(a,b): #the parameters for this function are a and b
				    print(a*b)     #this is the function of the body
				    
				def noParams():
				    print('this function has no parameters')
				    
				  
Calling Functions

		#A function call calls the function that is defined which will execute what's in the function. When called, the arguments are the data passed into the method's 			parameters. 
		
				multiply(2,3)       # call the function with arguments; they must match up with the parameters
				noParams()          # call a function that does not take any arguments
				
		#Neither multiply nor noParams have a return statement so they implicitly return None
		
				multRet = multiply(2,3)
				noParamsRet = noParams()
				print(multRet)
				print(noParamsRet)
				
				
Returning Data ----------------------------------------------------------------------------------------------------------------------------------------------------------------------


		#Functions often return values via the return statement.
		#Its common to save returned values for later use BUT if not needed, the function call is equivalent to the returned value when used by the calling code.
		
		
		#return Statement
		
		#user defined function with a return statement - base^exponent (2 to the power of 10)
		
		def power(base, exp):
		    return base ** exp
		    
		funcReturn = power(2,10)
		print(funcReturn)        ---> 1024
		
		
Print vs. Return --------------------------------------------------------------------------------------------------------------------------------------------------------------------

		#print() function provides a copy of the function's result
		#return() will provide a value that can be assigned to a variable and used
		
		
				def meantToReturn(x)
				    return x*2
				    
				def meantToPrint(x)
				    print(x*2)
				    
				print(f'The return value is: {meantToReturn(10)}')
				print(f'The return value is: {meantToPrint(10)}')
				
pass Statement -----------------------------------------------------------------------------------------------------------------------------------------------------------------------

				
				# pass statement - legal code that does nothing
				# generally provided after a function definition that does not yet have a function body

				def myFunction():       # legal function definition
				    pass                # legal function body

				myFunction()            # function call
				
				
Name Scopes -----------------------------------------------------------------------------------------------------------------------------------------------



		#functions proivde a nested namespace (sometimes called a scope), which localizes the names they use, such that names inside the function won't clash with those 		outside (in a module or other function). 
		
		
		The FOUR Python Scopes:
		
		1. local - names created inside a function
		2. enclosed - names created in a function that encloses (contains) another function. 
		3. global - names created inside a script outside of all functions.
		4. built-in - names that Python reserves for its own internal workings. 	
		
		
		----------------------------------------------------------------------------------------------------------------------------------------------------------------------
		|* Python examines scopes 'inside-out'.
		|
		|* Python looks at the most restrictive scope first and works its way outward to increasingly larger scopes.
		|
		|* Pythonistas express this concept as the LEGB rule.
		|
		|* Python looks first in local scope, followed by enclosed, followed by global, followed by builtin (LEGB).
		|
   		|* Each function contains its own scope; if a Python program has six functions that program contains six local scopes. The scope is activated when the function is 			|	called and disappears when the function terminates.
		| 			|		                                                                                                                                                                                                                                                               		|* A function cannot change the value of data bound to a name outside its scope                                                                                      |
		|                                                                                                                                                                    |
		|* If a Python function uses the name defined in global (or any enclosing) scope, Python creates a new name known only in the local scope and binds data to it.      |
		|                                                                                                                                                                    |
		---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-
		
		
		
		#Example of Local Scope
		
		def func():
			within_function = 'This is locally defined'
			print(within_function)
			
		func()
		
		
		#Example of Enclosed Scope
		#Creating a function and defining num
		
		def func_1():
			num = 20
			#Creating a function and printing num and num2 
			def func_2():
				print(num)
				print(num2)
			   func_2()
			num2 = 50
			func_1()
		
		* The name num2 is defined (known) in the global scope. Functions may access names outside their scope provided the scope is an outer scope (E, G, or B scopes)	
		
		
		#Global Scope
		#Declaring a global variable
		global_var = 'I am global'
		
		#Creating a function and changing global_var
		def func_1():
			global_var = 'New global'
			print(global_var)
			
		#Creating a function and prifpnting global_var
		def func_2():
			print(global_var)
			
		func_1()
		func_2()
		


		
### Building Custom Functions ---------------------------------------------------------------------------------------------------------------------------------------------------

			def multiply():        #Function is hardcoded to only multiply 2 & 4	
				return 2 * 4 	
		
			def multiply(num1, num2):
				return num1 * num2
				
			def username(first, last):
				return f"{last} . {first}"
				
				
				
				
				
				
				zero question format
				 
				def zero_pad_number(number, length):
   					 return f"{number:0{length}}"
				
				
		
		
		
		
		
		
		
		
		
		
		
		
