# Reading Notes 4 #

## Classes and Objects ##
You can create an instance of a class by using the class name followed by parenthesis. You can access object variables and object functions using dot notation. 
```
my_object = AClass()   
my_object.object_variable
my_object.object_function() 
```
### init() ###
The ```__init__()``` is called every time an object is instantiated. The init function in the class of the instantiated object will refer to this function in order to determine if any values need to be assigned during instantiation.
``` 
def __init__(self, variable):
      self.variable = variable
```

## Thinking Recursively ##
This article further expands on some of the Recursion concepts that we have covered in the class. Recursive functions are used to break problems up into smaller sub-problems by having a function call itself. A base case is necessary in order to prevent the function from infinitely calling itself and causing a StackOverflow error. There were two methods explained for maintaining state throughout recursive functions, I found this part to be the most helpful part of the article.
### Maintaining State ###
- Thread the state through each recursive call so that the current state is part of the current call’s execution context
- Keep the state in global scope

### Naive Recursion is Naive ###
In many cases it can be helpful to cache values that have previously been returned from recursive calls of a function in order to avoid excessive/unnecessary allocation of memory on the stack. One way of doing this in python is to use the lru_cache decorator as shown below (I think I can implement this manually with a dictionary)
```
from functools import lru_cache

@lru_cache(maxsize=None)
def my_recursive_func(input):
  # do stuff

  # if lru_cache has already stored results of these inputs to the function then we don't execute it again
  return my_recursive_func(some_input) + my_recursive_func(other_input)
```

## Pytest Fixtures and Coverage ## 
- Fixtures - Objects that can be made available to all of our tests within the entire 'test suite'. This is useful for creatings objects that contain data we want to share across multiple tests, or involve a network of the file system.
- Code Coverage - A mesaure of how thoroughly we have tested our code. There are usually multiple 'paths' through a function, and it is better to test as many of them as possible to avoid unexpected bugs in the future.
- pytest-cov : A pytest code coverage package. It gives reports showing where our programs still lack test coverage.