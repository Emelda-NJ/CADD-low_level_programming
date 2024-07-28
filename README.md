# CADD-low_level_programming
# R-Scripts

R is mostly used to perform statistical computing i.e. performing statistical tests on data to develop statistical models. 
R is an object-oriented language, which means every operation in R is performed around objects. 
These objects can be anything that can be stored in a variable, like one-dimensional data structures, two-dimensional data structures, user-defined functions, etc.
R is relatively easy to learn considering it is a low-level language. This is another reason why it requires longer codes. 
However, when pitted against other low-level languages like C, R is relatively one step higher.

# Basics of R Programming Language
# Objects and Environment
Being an object-based language, in R anything that can be saved in a variable is known as an object. In turn, all the operations in R are performed on or around these objects. 
The class of the object determines the associated functions that can be used to manipulate these objects. The data type or the data structure of the object determines the class of the object.
All these objects are shown in the Environment window. This makes managing objects extremely easy as the user can see the objects that are currently occupying the space in RAM. 
The user can export, and import objects using a .RData file and can even delete objects that are unnecessary to make the coding process more efficient.

Function	                                     and                                 Formula

Finding all the names of objects in the environment	         🡪                   >> ls()

Saving all the objects that are there in the environment	  🡪       >> save.image(“MyBackup.RData”)

Saving one object from the environment	                  🡪       >> save(Cities, file=”cityobj.RData”)

Removing an object	                                    🡪                       >> rm(Cities)

Removing all the object from the environment	          🡪                     >> rm(list=ls())

Loading a RData file	                               🡪                    >> load(“MyBackup.RData”)

# Console
It is considered the brain of the R programming language and the IDE used for running R- R Studio.  
In the console, you can write the code, execute it and simultaneously see the output. Any code written in the console, however, cannot be saved in the form of a script. 
Also, codes that have been already executed in the console cannot be edited. Interestingly, any code that is written in the code window is executed in the console only.

# Script
Codes written in the code window can be saved as a .R file. This file is commonly known as an R script. These scripts are helpful in sharing and re-using the codes.

# Operators
These are symbols that allow us to perform certain operations.

Type	                            and                              Operators

Assignment Operators	           🡪                                   =
                                                                    ->
                                                                    <-
                                                                    
Arithmetic Operators	         🡪                               / (division)
                                                            * (multiplication)
                                                              + (addition)
                                                            – (substraction)
                                                          %% (modulus) Remainder
                                                        %/% (Integer Division) Quotient
                                                                ^ (Power)
                                                                
Relational Operators	      🡪                                  > (Greater than)
                                                                < (Less than)
                                                          <= (Greater than equal to)
                                                            >= (Less than equal to)
                                                            == (Equal to Equal to)
                                                            
Logical Operators	         🡪                                       & (AND)
                                                                  | (OR)

# Syntax Rules
Case Sensitivity:
Any object name (including any name of the library, function, etc) should be written in the exact same case as required.
Example: print()This function name is in the lower case and; View() function requires the first letter to be in the upper case.
If we create objects with the same name but in different cases then those objects are considered separate i.e. city and City will be considered as two different objects.

The use of comments:
We use the # symbol to create a comment

Naming Rules:
When creating objects in R, one must make sure that the name of the object doesn’t start from a number, 
doesn’t have any symbol (. and _ are acceptable symbols generally used in the object name to denote space) and 
doesn’t coincide with another pre-existing function or object.

# Data Types and Type Casting
- Data type related to Numbers

numeric - for any numerical value eg: 1, 1.5, 20, pi.
The most commonly used and found data type in R includes-     short numbers with decimal;
                                                              long numbers with decimals;
                                                              short numbers without decimal;
                                                              long numbers without decimals.
  
integer - for integer numbers (e.g., 2L, the L indicates to R that it’s an integer) eg: 2L, 500L, -17L.
It is found in special cases during the importing of certain files or when a certain package’s function output is pre-coded to have this as the output’s data type.
Only small numbers without decimal can have an integer as the data type.
Definition of a small number is a value between -21474763648 to 21474763647.

complex
These are the real + imaginary numbers for example = 5+6i.
They are very rarely used in day to day operations.

- Data type related to characters (text)

character: It is used to store any alphabets or alphanumeric or symbol - for text values, denoted by using quotes (“”) around value eg: “anytext”, “5”, “TRUE”.

factor: This data type is unique to R. Here the values can look like a character to the user, however, internally the values are stored in the form of levels which are represented in the form of numbers.
        Factors are the data objects which are used to categorize the data and store it as levels.
        They are useful for storing categorical data. They can store both strings and integers.
        They are useful to categorize unique values in columns like “TRUE” or “FALSE”, or “MALE” or “FEMALE”, etc.. They are useful in data analysis for statistical modeling.
        To create a factor in R you need to use the function called factor(). The argument to this factor() is the vector. 

- Data related to Boolean

logical - eg: TRUE, FALSE, T, F
This is the data type that is used to represent the Boolean i.e. TRUE ad FALSE.
All the relational and logical operators provide us with a Boolean output.

- Date and Time
Date and Time generally are not a naturally occurring data types in many languages such as R and Python.
These are derived data types i.e. we have to manually convert the object into this data type.

Date
This is the data type for denoting dates in R.
POSIXct (Portable OS Interface Exchange).
POSIX is the data type in which dates are stored in all the OS; and ct is the conversion of POSIX to R.

To find the different data types in R we have a function known as a class()

For changing the data types, a process also known as type casting requires functions such as as.character(), as.factor(), as.numeric() etc.
However, before changing the data types one must be aware of the hierarchy of typecasting where the highest data type is character and lowest is logical.
A higher data type cannot be converted to a lower data type apart from a few specific exceptions.

# Data Structures
Data Structure is the mechanism for saving multiple elements in an object in an efficient manner. They can be differentiated on the basis of their homogeneity and dimensions. 

In R the most common data structures are-

vector: 1 Dimensional Homogeneous Data Structure
        A vector is an ordered collection of basic data types of a given length. The only key thing here is all the elements of a vector must be of the identical data type.
        Vectors are one-dimensional data structures.
        
matrix: 2 Dimensional Homogenous Data Structure.
        A matrix is a rectangular arrangement of numbers in rows and columns.
        To create a matrix in R you need to use the function called matrix. The arguments to this matrix() are the set of elements in the vector.
        You have to pass how many numbers of rows and how many numbers of columns you want to have in your matrix.

data.frame/data.table: 2 Dimensional Heterogeneous Data Structure used to store the tabular data.
                        To create a data frame we use the data.frame() function.
                        These are lists of vectors of equal lengths.
                        A data-frame must have column names and every row should have a unique name.
                        Each column must have the identical number of items.
                        Each item in a single column must be of the same data type.
                        Different columns may have different data types.
                        
list: A mechanism to contain other objects inside of it, A list can be a list of vectors, list of matrices, a list of characters and a list of functions and so on
      A list is a generic object consisting of an ordered collection of objects.
      These are also one-dimensional data structures.
      
Arrays: homogeneous data structures.
        R data objects which store the data in more than two dimensions.
        Arrays are n-dimensional data structures. For example, if we create an array of dimensions (2, 3, 3) then it creates 3 rectangular matrices each with 2 rows and 3 columns.
        To create an array in R you need to use the function called array().
        The arguments to this array() are the set of elements in vectors and you have to pass a vector containing the dimensions of the array.

# Packages/Libraries
In R the packages can be divided into two parts – system and user where system packages are those that are provided by the R by default 
whereas user libraries are the third party libraries that the user downloads from CRAN

 	                                                                      Functions
                                                                        
To find all the libraries available in the CRAN repository	  🡪    available.packages()

To find all the installed packages	                       🡪       installed.packages()

To load a library	                               🡪           install.package(“library name”)

To load a library	                        🡪                        library(libraryname)

# Shortcuts
One can find all the shortcuts available in R and R studio by using the shortcut – Alt + Shift + K

Control +Enter 🡪 Execute the code

Control + Shift + N 🡪 Creating new R Script

Control + S 🡪 Saving the R Script

Control + L 🡪 Clears the console
