Recursion

 I learned a handful of things after reading the three articles on recursion, python modules, and test driven development. Recursion is the concept of a function being called inside of itself. This is useful for solving many different problems where we can come to a solution by breaking up the problem in smaller subproblems. There must be a base case in recursive functions or we are at risk of having a StackOverflow exception in our program. Since memory is allocated on the stack for each recursive call, in my experience I have found it might be a good idea to use an iterative approach over recursion when it is likely that our program will perform very deep recursive calls before any memory deallocation occurs.  

Python Modules

   I also got a more thorough understanding of python modules, a concept we have covered in our lectures already. The Python interpreter is responsible for defining several global variables before Python code is executed. One of these global variables is the __name__ variables, which defines the behavior of our module based on how it is run. If a Python module is run directly as a script then the __name__ variables will be set to '__main__'. Alternatively, if the module is imported and used in another module, then the __name__ variable will be the same as the file name without the .py extension.

Test Driven Development

   The final article covered some concepts about Test Driven Development. We learned about naming conventions for test files, as well as test methods. It is important to be very explicit about the purpose of a test method so that there is absolutely no obscurity regarding what functionality the specific method is testing. I thought the Arrange, Act, and Assert convention was an interesting way to remember how to write great Python tests.