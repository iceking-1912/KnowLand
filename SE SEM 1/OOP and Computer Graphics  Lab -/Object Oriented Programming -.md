---
tags:
  - COMP_PROGRAM
YTLINKS: https://youtu.be/wN0x9eZLix4?si=dmTLtk3slsFhPA_F
Year: "2024"
Curriculum: "[[SE-Computer-Engg-2019-Patt.pdf]]"
Semester: "[[SE SEM 1]]"
Course: Computer
Lab: "[[OOP and Computer Graphics  Lab -]]"
lang: cpp
Major: "[[Object Oriented Programming -]]"
---
# Computer Science [[SE SEM 1]] : Object-Oriented Programming in C++  Syllabus - Detailed Topics

## **Unit I: Fundamentals of Object-Oriented Programming (6 Hours)**

- **Introduction to Programming Paradigms:**
    - Procedural Programming (Structured Programming)
    - Modular Programming
    - Generic Programming
    - Object-Oriented Programming (OOP)
- **Limitations of Procedural Programming:**
    - Data and logic tightly coupled
    - Difficulty in managing complexity
    - Limited code reusability
- **Need for Object-Oriented Programming:**
    - Improved modularity and maintainability
    - Code reusability through inheritance and polymorphism
    - Data encapsulation for better data security
- **OOP Paradigms:**
    - Objects: Real-world entities with data (attributes) and behavior (methods)
    - Classes: Blueprints for creating objects
    - Inheritance: Deriving new classes from existing ones (reuse)
    - Polymorphism: "One interface, multiple implementations" (flexible behavior)
- **Fundamentals of OOP in C++:**
    - Namespaces: Logical organization of code
    - Data Members: Variables within a class
    - Methods: Functions defined within a class
    - Messages: Communication between objects
    - Data Encapsulation: Data protection through access specifiers (private, public)
    - Data Abstraction: Hiding implementation details and exposing essential functionalities
    - Information Hiding: Protecting internal data from direct manipulation
- **Benefits of OOP:**
    - Improved code organization and maintainability
    - Reusability of components through inheritance
    - Easier development of complex systems
    - Better modeling of real-world entities
- **C++ as an Object-Oriented Programming Language:**
    - Supports key OOP concepts like classes, inheritance, and polymorphism

**Exemplar/Case Studies:**

- Story of C++ invention by Bjarne Stroustrup: Understanding the motivations behind OOP development.
- Mapping of Course Outcomes for Unit I (CO1): Link learning objectives to specific concepts covered.

## **Unit II: Inheritance and Pointers (6 Hours)**

- **Inheritance:**
    - Base Class and Derived Class: Parent-child relationship
    - Protected Members: Accessible within the class and derived classes
    - Relationship between Base and Derived Classes: Inheritance hierarchy
    - Constructors and Destructors in Derived Classes: Overriding behavior
    - Overriding Member Functions: Redefining inherited functionality
    - Class Hierarchies: Complex inheritance structures
    - Public and Private Inheritance: Access specifiers in inheritance
    - Types of Inheritance: Single, Multilevel, Hierarchical, Multiple (with potential ambiguity)
    - Ambiguity in Multiple Inheritance: Diamond problem and solutions (virtual base classes)
    - Abstract Class: Defining a base class with incomplete functionality
    - Friend Class: Granting special access to another class's private members
    - Nested Class: Classes defined within another class for better organization
- **Pointers:**
    - Declaring and Initializing Pointers: Memory address storage
    - Indirection Operators: Accessing data through pointers
    - Memory Management: `new` and `delete` keywords for dynamic allocation and deallocation
    - Pointers to Objects: Pointing to object instances
    - `this` Pointer: Referring to the current object within a method
    - Pointers vs. Arrays: Similarities and differences in accessing elements
    - Arrays Using Pointers: Array traversal and manipulation using pointers
    - Arrays of Pointers: Holding addresses of multiple arrays
    - Function Pointers: Pointing to functions for flexible function calls
    - Pointers to Pointers: Multi-level indirection
    - Pointers to Derived Classes: Inheritance with pointers
    - Passing Pointers to Functions: Mechanisms for argument passing
    - Returning Pointers from Functions: Returning memory addresses
    - Null Pointer: Handling invalid pointer values
    - Void Pointer: Generic pointer type for various data types

**Exemplar/Case Studies:**

- Know about Firefox and Thunderbird as popular softwares developed using C++: Real-world applications of OOP concepts.
- Mapping of Course Outcomes for Unit II (CO2, CO3, CO4): Link learning objectives to specific topics covered.

## **[[Unit III Polymorphism]] (6 Hours)**

- **Polymorphism:**
    - Introduction: Ability of objects to respond differently to the same message
    - Early Binding (Static Binding): Compile-time determination of method calls
    - Late Binding (Dynamic Binding): Runtime determination of method calls using virtual functions
- **Types of Polymorphism:**
    - Operator Overloading: Redefining operator behavior for custom classes
        - Concept of Overloading: Defining multiple functionalities for the same operator
        - Overloading Unary and Binary Operators: Examples of custom operator behavior (e.g., overloading `+` for vector addition)
    - Data Conversion: Type casting (implicit and explicit) for data type conversions
        - Pitfalls of Operator Overloading and Conversion: Potential for errors and unexpected behavior
        - Keywords `explicit` and `mutable`: Controlling type conversions and modifying const objects
- **Function Overloading:** Multiple functions with the same name but different parameter lists
- **Run-Time Polymorphism:** Using virtual functions for dynamic method calls
    - Pointers to Base Class: Enabling polymorphism through base class pointers
    - Virtual Function and its Significance: Ensuring correct method calls in inheritance hierarchies
    - Pure Virtual Function and Virtual Table: Defining abstract classes and enabling polymorphism for derived classes
    - Virtual Destructor: Proper memory management in inheritance scenarios

**Exemplar/Case Studies:**

- Study about use of C++ SDKs wrappers for Java and .Net: How polymorphism simplifies interactions between different programming languages.
- Explore virtual function usage in game development: Polymorphism enables creating objects with various behaviors (e.g., different types of enemies with unique attack methods).
- Mapping of Course Outcomes for Unit III (CO2, CO3, CO4): Link learning objectives to specific polymorphism concepts covered.

## **[[Unit IV Files and Streams]] (6 Hours)**

- **Data Hierarchy:** Understanding different data organization levels (bits, bytes, records, files)
- **Streams and Files:** Introduction to data flow mechanisms for file operations
- **Stream Classes:** C++ classes for handling input/output (e.g., `ifstream`, `ofstream`)
- **Stream Errors:** Detecting and handling errors during file operations
- **Disk File I/O with Streams:** Reading from and writing to files using streams
- **File Pointers and Error Handling:** Managing file position and potential errors
- **File I/O with Member Functions:** Stream class member functions for file operations
- **Overloading the Extraction and Insertion Operators:** Customizing data input/output using operators (e.g., `>>` for reading, `<<` for writing)
- **Memory as a Stream Object:** Treating memory buffers as streams for data manipulation
- **Command-Line Arguments:** Accessing arguments passed to the program during execution
- **Printer Output:** Sending output to a printer device

**Exemplar/Case Studies:**

- Study features used for Microsoft Office, Internet Explorer and Visual Studio that are written in Visual C++: Exploring how file I/O is used in real-world applications.
- Investigate text editors or file management tools: Analyze how these programs utilize streams and file operations.
- Mapping of Course Outcomes for Unit IV (CO2, CO3, CO4): Link learning objectives to specific file I/O concepts covered.

## **[[Unit V Exception Handling & Templates]] (6 Hours)**

- **Exception Handling:**
    - Fundamentals: Mechanism for managing errors during program execution
    - Other Error Handling Techniques: Comparison with traditional error handling approaches
    - Simple Exception Handling: Examples of catching common exceptions (e.g., division by zero)
    - Multiple Catching: Handling different types of exceptions in separate blocks
    - Re-throwing an Exception: Propagating exceptions to higher levels in the program
    - Exception Specifications: Specifying types of exceptions a function might throw
    - User-Defined Exceptions: Creating custom exception classes
    - Processing Unexpected Exceptions: Handling unforeseen exceptions gracefully
    - Constructor, Destructor, and Exception Handling: Considerations for exception safety in object construction and destruction
- **Templates:**
    - The Power of Templates: Generic programming for code reusability
    - Function Template: Defining functions with generic types
    - Overloading Function Templates: Multiple versions of a function template with different parameter types
    - Class Template: Creating generic classes that work with various data types
    - Class Template and Nontype Parameters: Templates with parameters beyond data types
    - Template and Friends: Granting access to private members within a template
    - Generic Functions: Functions that operate on different data types based on template arguments
    - The `typename` and `export` Keywords: Specifying template parameter types and controlling visibility

**Exemplar/Case Studies:**

- Study about use of exception handling in Symbian Operating System (discontinued mobile operating system) that was developed using C++: Exploring exception handling in a real-world system.
- Analyze exception handling mechanisms in popular libraries or frameworks written in C++: Understanding practical applications of exception handling.
- Mapping of Course Outcomes for Unit V (CO2, CO3, CO4): Link learning objectives to specific exception handling and template concepts covered.

## **[[Unit VI Standard Template Library (STL)]]  (6 Hours)

- **Introduction to STL:** Powerful collection of container classes and algorithms in C++
- **STL Components:** Key elements of the STL, including containers and algorithms
- **Containers:**
    - Sequence Containers: Ordered collections like vectors and lists
    - Associative Containers: Unordered collections with key-value pairs (e.g., maps, sets)
    - Container Adapters: Wrappers for existing containers providing additional functionalities
- **Application of Container Classes:** Examples of using specific containers like vectors for dynamic arrays and maps for efficient key-value lookups
- **Algorithms:**
    - Basic Searching and Sorting Algorithms: Built-in algorithms for searching (linear search) and sorting (e.g., insertion sort, merge sort)
    - Min-Max Algorithm: Finding minimum and maximum elements within a container
    - Set Operations: Algorithms for manipulating sets (e.g., union, intersection)
    - Heap Sort: Efficient sorting algorithm using heap data structures
- **Iterators:**
    - Input, Output, Forward, Bidirectional, and Random Access Iterators: Different types of iterators for traversing containers with varying access capabilities
- **Object Oriented Programming – a Road Map to Future:** Discussing the broader impact of OOP on software development

**Exemplar/Case Studies:**

- Study MySQL open source C++ code available at GitHub: Analyze real-world usage of STL in a database management system.
- Explore algorithms used in game development: Investigate how STL algorithms are applied for tasks like pathfinding or character AI.
- Mapping of Course Outcomes for Unit VI (CO2, CO3, CO4): Link learning objectives to specific STL concepts covered.