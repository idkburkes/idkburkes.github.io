# Reading Notes 3 #

The reading assignments for class 3 covered file reading & writing operations as well as exception handling.

## Read & Write Files in Python ##

This article defined files as simply being an arrangement of bytes as a way to store data. Different types of files have different formats and character encodings depending on the type of data that you are storing. Some of the important functions for manipulating files in python include

- open()
- close()
- read()
- readlines()

You may input different parameters into the open function defending on the type of file object you would like to open. The 3 types of file objects in Python are

- Text Files
- Buffered Binary Files
- Raw Binary Files

I also learned about the __file__ attribute, which is another special dunder attribute that is helpful for handling files. __file__ will return the path relative to where the initial Python script was called. This is a very important thing to pay attention to because file paths might be different if the module is imported or if a function is being called from a test file.

 
## Exceptions in Python ## 

I read about exception handling in python. It is pretty similar to exception handling in other programming languages that I have used such as Java or JavaScript. Here are some of the most useful blocks used in exception handling that I found

try: 
      The try block is where you'll be putting your code that has a possibility of raising an exception

except:
      The except block will execute when any exception is raised

except SpecificException
       If you name a specific exception after except then this block of code will only be executed when the specific exception is raised

except AnothherException as e
       This except block is similar to the previous block but it also gives you an error object that can help you in handling the exception

finally:
      The finally block is executed no matter what. If no exception is raised it will be executed last, but it will also be executed after an except block if an exception is raised.

else:
       The else block will only be executed last if no exception is raised