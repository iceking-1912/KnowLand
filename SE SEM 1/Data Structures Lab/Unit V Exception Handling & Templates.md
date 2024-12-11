## **Unit V: Exception Handling & Templates (6 Hours)**
1. **Introduction to Exception Handling (1 hour)**

- Understanding the concept of exceptions
- Different types of exceptions in C++
- try, catch, throw, and exception specifications
- Using exception handling to handle errors gracefully
- Custom exceptions

2. **Exception Propagation & Chaining (1 hour)**

- Exception propagation: When an exception is not handled by the current function, it 
gets propagated up the call stack until it is either handled or terminates the program
- Exception chaining: When a new exception is created within a catch block and 
re-thrown, it can contain a reference to the original exception that caused it, 
providing additional context about the error

3. **Rethrowing Exceptions (0.5 hour)**

- Rethrowing exceptions: Throwing an exception again after handling it in a function. 
This is useful when a function cannot handle the exception but wants to pass it on to 
another function that can handle it.

4. **Exception Specifications & noexcept (0.5 hour)**

- Exception specifications: A way to inform the compiler about the exceptions that a 
function may throw
- noexcept keyword: A way to specify that a function does not throw any exception

5. **try-blocks with Multiple Catch Clauses (1 hour)**

- Using multiple catch clauses in a try-block to handle different types of exceptions
- The order of the catch clauses matters: more specific catch clauses should come first

6. **Resource Acquisition Is Initialization (RAII) & Smart Pointers (1.5 hour)**

- RAII principle: Resource acquisition and release are done in the constructor and 
destructor respectively
- Smart pointers: Classes that automatically manage memory for dynamically allocated 
objects, ensuring resources are freed when they're no longer needed
	+ unique_ptr: A smart pointer that owns an object and ensures it is deleted when the 
unique_ptr goes out of scope
	+ shared_ptr: A smart pointer that allows multiple owners to share ownership of an ob
object and manages its lifespan accordingly
	+ weak_ptr: A smart pointer that provides a non-owning reference to an object managed 
by a shared_ptr

7. **Exception Safe Destructors (0.5 hour)**

- Ensuring destructors are exception-safe so they can be called even if an exception is 
thrown within the constructor of the object being destroyed




>>> Fundamentals: Mechanism for managing errors during program execution
...     - Other Error Handling Techniques: Comparison with traditional error handling approac
... hes
...     - Simple Exception Handling: Examples of catching common exceptions (e.g., division b
... y zero)
...     - Multiple Catching: Handling different types of exceptions in separate blocks
...     - Re-throwing an Exception: Propagating exceptions to higher levels in the program
...     - Exception Specifications: Specifying types of exceptions a function might throw
...     - User-Defined Exceptions: Creating custom exception classes
...     - Processing Unexpected Exceptions: Handling unforeseen exceptions gracefully
...     - Constructor, Destructor, and Exception Handling: Considerations for exception safet
... y in object construction and destruction
1. **Fundamentals: Mechanism for managing errors during program execution**
   - Error handling is crucial to ensure that a program can recover from unexpected 
situations during its runtime.

2. **Other Error Handling Techniques:**
   - Compare traditional error-handling approaches like `errno` in C or the GOTO 
statement with exception handling for better flexibility and code readability.

3. **Simple Exception Handling:**
   - Demonstrate examples of catching common exceptions (e.g., division by zero).

4. **Multiple Catching:**
   - Show how to handle different types of exceptions in separate blocks.

5. **Re-throwing an Exception:**
   - Discuss the process of propagating exceptions to higher levels in the program.

6. **Exception Specifications:**
   - Explain the concept of specifying the types of exceptions a function might throw, 
helping callers prepare for potential errors.

7. **User-Defined Exceptions:**
   - Teach learners how to create custom exception classes tailored to their specific 
needs.

8. **Processing Unexpected Exceptions:**
   - Demonstrate techniques for handling unforeseen exceptions gracefully, such as 
logging the error and providing a user-friendly message.

9. **Constructor, Destructor, and Exception Handling:**
   - Highlight considerations for exception safety in object construction and 
destruction, including resource acquisition and resource release patterns.




>>> **Templates:**
...     - The Power of Templates: Generic programming for code reusability
...     - Function Template: Defining functions with generic types
...     - Overloading Function Templates: Multiple versions of a function template with diffe
... rent parameter types
...     - Class Template: Creating generic classes that work with various data types
...     - Class Template and Nontype Parameters: Templates with parameters beyond data types
...     - Template and Friends: Granting access to private members within a template
...     - Generic Functions: Functions that operate on different data types based on template
...  arguments
...     - The `typename` and `export` Keywords: Specifying template parameter types and contr
... olling visibility
... 
1. **The Power of Templates:**
   - Explain the value of templates in promoting code reusability through generic 
programming.

2. **Function Template:**
   - Demonstrate how to define functions with generic types.

3. **Overloading Function Templates:**
   - Show multiple versions of a function template with different parameter types.

4. **Class Template:**
   - Teach learners how to create generic classes that work with various data types.

5. **Class Template and Nontype Parameters:**
   - Discuss templates with parameters beyond data types.

6. **Template and Friends:**
   - Explain the process of granting access to private members within a template.

7. **Generic Functions:**
   - Demonstrate functions that operate on different data types based on template 
arguments.

8. **The `typename` and `export` Keywords:**
   - Teach learners about specifying template parameter types and controlling 
visibility.




>>> - **Exception Handling:**
1. Define what exceptions are in the context of C++ 
programming.
Exceptions are a way to handle and manage errors or 
unusual conditions that may occur during program 
execution in C++. They provide a means for the program 
to signal an error, allowing the error to be handled in 
a centralized and consistent manner without interrupting 
the normal flow of the program.

2. List different types of exceptions in C++.
- Standard exceptions: These are built-in exceptions 
defined in the C++ standard library. Examples include 
`std::exception`, `std::runtime_error`, and 
`std::logic_error`.
- User-defined exceptions: Custom exceptions that can be 
created to handle specific error conditions in a 
program. These are typically derived from the 
`std::exception` class.
- System-defined exceptions: Exceptions defined by 
system libraries, such as those related to file I/O or 
network communication errors.

3. Describe the main components of exception handling in 
C++.
- try: A block of code where the program's normal 
execution flow is temporarily suspended, and the code 
within the block is monitored for exceptions.
- throw: A keyword used to raise an exception when an 
error or unusual condition occurs. It can be used inside 
a function to indicate that an error has occurred and 
should be handled by a suitable catch clause.
- catch: A block of code that handles exceptions thrown 
within the corresponding try block. Each catch clause 
specifies a specific type of exception it can handle.

4. Explain what exception propagation is, and how it 
works.
Exception propagation occurs when an exception is not 
handled by the current function, it gets passed up the 
call stack to the calling function until it is either 
handled or terminates the program. Each function that 
calls another function should be prepared to handle 
exceptions thrown by the called functions or propagate 
them further up the call stack.

5. Describe what exception chaining is and explain its 
purpose.
Exception chaining is the process of creating a new 
exception within a catch block and re-throwing it with 
additional context about the original error. This allows 
the upper layers of the program to handle the overall 
error without having to dig deep into the underlying 
details. It provides a clear chain of events leading up 
to the exception, making it easier to debug and 
understand the root cause of the problem.

6. Explain what rethrowing exceptions is and when it 
might be useful.
Rethrowing exceptions refers to the process of catching 
an exception within a function and then throwing it 
again so that it can be handled by another function 
further up the call stack. Rethrowing an exception is 
useful when the current function cannot handle the error 
but wants to pass it on to a higher-level function that 
can handle it more appropriately.

7. Describe what exception specifications are and how 
they work.
Exception specifications are declarations made in the 
function definition that inform the compiler about the 
exceptions a function may throw. This helps the compiler 
check for consistency in the code and avoid potential 
runtime errors due to unhandled exceptions. The 
`noexcept` keyword can be used to specify that a 
function does not throw any exception, which can improve 
performance by allowing the compiler to optimize the 
function's code.

8. Explain what Resource Acquisition Is Initialization 
(RAII) is and how it relates to exception handling.
Resource Acquisition Is Initialization (RAII) is a programming principle that ensures that resources acquired by an 
object are automatically released when the object goes out of scope or is destroyed. 
This helps manage resources such as memory, files, and network connections efficiently and avoids resource leaks when 
exceptions occur. Smart pointers like `unique_ptr`, `shared_ptr`, and `weak_ptr` 
implement RAII to manage dynamically allocated objects effectively.

9. Describe the difference between unique_ptr, shared_ptr, and weak_ptr.
- unique_ptr: A smart pointer that owns an object and ensures it is deleted when the 
unique_ptr goes out of scope. It allows only one owner at a time.
- shared_ptr: A smart pointer that allows multiple owners to share ownership of an 
object and manages its lifespan accordingly. It keeps track of the number of owners and 
deletes the object when the last owner goes out of scope.
- weak_ptr: A smart pointer that provides a non-owning reference to an object managed 
by a shared_ptr. It can be used when the weak_ptr doesn't need to manage the lifetime 
of the object but still needs a reference to it for other purposes.