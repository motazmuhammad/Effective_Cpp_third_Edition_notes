# Effective_Cpp_third_Edition_notes
This includes my notes from the book Effective C++ by Scott Meyers

#### Introduction

###### Definitions

  A *declaration* tells the compilers about the name and type of something but it omits certain details. ( it can be for an object, function, class, or template) e.g. extern int x; // object declaration.
  
  A *signature* is a function's parameters and return type.
  
  A *definition* provides compilers with the details a declaration omits.
  
  *Initialization* the process of giving an object its first value.
  
  *Default constructor* is a constructor that can be called without any arguments, such a constructor either has no parameters or has a default value for every parameter. (Note: It is a good practice to use the keyword explicit in your constructors to avoid the compiler doing undesired implicit type conversion).
  
  *Copy Constructor* is used to initialize an object with a different object of the same type.
  *The copy assignment operator* is used to copy the value from one object to another of the same type. Note the copy constructor is what defines how the object is passed by value. 
  Note: Derefercing a NULL pointer holds an undefined behaviour.
  
  *interface* in C++ interfaces are not integral part of the languages. Therefore, in this book the word interface is used to refer to a funcion or a set of function that can be called by an object. For example, public interface of a class is just the set of public functions of that class same goes for private interface or protected interface. When the word interface is used in context of templates it means the expressions that are valid for the template type parameter.
  
  
## Chapter I
  #### Item 1: View C++ as a federation of languages.
  ###### C++ is a multipardigm language
  It supports combination of procedural, object-oriented,functional, generic, and metaprogramming features.
  This view as a federation of languages instead of just one language makes it clear when the rules are to be followed and when not to be.
  ###### C++ sublanguages
  1. C
  2. Object Oriented C++
  3. Template C++
  4. The STL
  
  ###### Rules for effective C++ programming vary depending on which part of the language one uses.
  #### Item 2: Prefer consts, enums, and inlines to #defines aka prefer compiler to preprocessor
   Why? Because the symbolic name in the preprocessor will not be seen by the compiler nor the debugger. Making it more difficult to track any errors.
   Special case 1: when referring to a pointer please remember the proper use of constants
   e.g. const char* const authorName="Scott Meyers"; actually strings are usually preferred to char*.
   Special case 2: When using a const inside a class remember to make it static so that there is only one version of it during the lifetime fo the code.
   Use enums to prevent people from getting a pointer to your variable/constant
   
   Take home message:
    For simple constants, prefer const objects or enums to #define.
    For function-like macros, prefer inline functions to #defines
   
   #### Item 3: Use const whenever possible.
   
   The main four different scenarios for const
   1.  char greeting[]="hello";
    char*p= greeting not const pointer not const data;
   2. const char * p= greeting; non const pointer const data;
   3. char * const p= greeting; const pointer non const data
   4. const char* const p= greeting; const pointer const data;
   
   Use const in the return of a binary operator to prevent it from being assignable. 
   For example, const Rational operator *( const Rational &lhs, const Rational & rhs)
   
   without const at the beginnging an operation like (a*
   b)=c would be legal which is undersirable.
   
   
   
  
