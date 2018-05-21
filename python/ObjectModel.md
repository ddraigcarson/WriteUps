# Object model

The Python interpreter invokes special methods to perform basic object operations, these special methods are called dunder methods because they start and end with two underscores '\_\_init\_\_()'

The special method names allow your objects to implement, support, and interact with basic language constructs such as:

- Iteration
- Collections
- Attribute access
- Operator overloading
- Function and method invocation
- Object creation and destruction
- String representation and formatting
- Managed contexts (i.e., with blocks)

For example, by implementing the len and getitem method our object can now behave as a sequence so we can do:

- obj[0]
- obj[1:3]
- obj[1:]
- obj[1::3] # from the first item skip 3 items at a time
- sorting

Although they are powerful and give cool benefits, they are not meant to be called by the programmer, only by the interpreter (init being the exception)

__add__ and __mul__ allow us to use the + and * operator

###### If given a choice between implementing str or repr, choose repr as python will call that if a str method is missing
