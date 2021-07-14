# Errors
Error objects are thrown when runtime errors occur. The Error object can also be used as a base object for user-defined exceptions. See below for standard built-in error types.
Runtime errors result in new Error objects being created and thrown.

![errdfgdfors](https://pbs.twimg.com/profile_images/1119245036091256832/rv1l6uqy_400x400.png)



# Error types
Besides the generic Error constructor, there are other core error constructors in JavaScript. For client-side exceptions, see Exception handling statements.

**1-EvalError**      
Creates an instance representing an error that occurs regarding the global function eval().       
**2-RangeError**       
Creates an instance representing an error that occurs when a numeric variable or parameter is outside of its valid range.      
**3- ReferenceError**      
Creates an instance representing an error that occurs when de-referencing an invalid reference.             
**4- SyntaxError**        
Creates an instance representing a syntax error.        
**5- TypeError**           
Creates an instance representing an error that occurs when a variable or parameter is not of a valid type.           
**6- URIError**            
Creates an instance representing an error that occurs when encodeURI() or decodeURI() are passed invalid parameters.                 
**7- AggregateError**                    
Creates an instance representing several errors wrapped in a single error when multiple errors need to be reported by an operation, for example by Promise.any().            
**8- InternalError**                          
Creates an instance representing an error that occurs when an internal error in the JavaScript engine is thrown. E.g. "too much recursion".                   
# Code Debugging

![depugging](https://files.realpython.com/media/Python-Debugging-With-Pdb_Watermarked.a50a90b655cf.jpg)

Programming code might contain syntax errors, or logical errors.

Many of these errors are difficult to diagnose.

Often, when programming code contains errors, nothing will happen. There are no error messages, and you will get no indications where to search for errors.

Searching for (and fixing) errors in programming code is called code debugging.

# JavaScript Debuggers
Debugging is not easy. But fortunately, all modern browsers have a built-in JavaScript debugger.

Built-in debuggers can be turned on and off, forcing errors to be reported to the user.

With a debugger, you can also set breakpoints (places where code execution can be stopped), and examine variables while the code is executing.

Normally, otherwise follow the steps at the bottom of this page, you activate debugging in your browser with the F12 key, and select "Console" in the debugger menu.
