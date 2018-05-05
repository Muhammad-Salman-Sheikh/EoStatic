# This is a Work in Progress (WIP)

'''
	This is the erorr handling for special cases in which we want to exit via `except`
'''
def Reserror(message):
	raise ValueError(message)


'''
	The Interpreter class for our language
'''

class Interpreter :
	def __init__(self , Input):
		self.Input = Input
		self.tokens = Input.split(' ') # split the given Input into tokens 
		self.stack = 0 # stack is 0 we will increment and decrement it
	'''
		Interpreter function that does it all 
	'''
	def Interpret(self):
		'''
			For empty programs (It's a golfing language what did you expect)
		'''
		if self.Input == '':
			'''
			We all love FizzBuzz program don't we
			'''
			a = ''
			for i in range(1,100):
				if i % 3 == 0 and i % 5 == 0:
					a += 'FizzBuzz '
				elif i % 3 == 0:
					a += 'Fizz '
				elif i % 5 == 0:
					a += 'Buzz '
				else :
					a += '' + str(i) + ' '
			Reserror('\n'.join(a.split(" ")))
			
			'''
				One byters 
			'''
		elif len(self.Input) == 1 :
			'''
				Must be `;` and add one to stack
			'''
			if self.Input == ';' :
				self.stack += 1
			else : # No `;` found exception 
				Reserror('Hello, World!') # throw `Hello, World!` to user
			'''
				Otherwise ....
			'''
		else :
			self.stack = 0
			'''
					Primality test for given input
					
					- Two possibilities :
						* input is given in which case this checks for input's
						  Primality test
						
						* other wise it checks for the number entered in the 
						  interpreter (in case input is not allowed)	
			'''
			if not self.tokens[0] == ';' :
				if not input() :
					inp = int(self.Input)
					for i in range (1 , inp):
						if(inp < 2):
							Reserror('false')
						elif (inp % i == 0):
							Reserror('false')
						elif (i == inp - 1):
							Reserror('true')
				else :
					inp = int(input()) # Our input
					for i in range (1 , inp):
						if(inp < 2):
							Reserror('false')
						elif (inp % i == 0):
							Reserror('false')
						elif (i == inp - 1):
							Reserror('true')
			elif self.tokens[0] == ';' :
				self.stack += 1
				for i in range(1 , len(self.tokens)):
					pass # Implement for everything else
				
		return self.stack

try :
	print(Interpreter('23 ').Interpret())
except ValueError as err:
	print(err)
