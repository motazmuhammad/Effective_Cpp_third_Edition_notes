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
  
  
#### Chapter I
  Item 1: View C++ as a federation of languages.
