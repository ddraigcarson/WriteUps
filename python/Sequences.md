# Sequences

Python has these built in sequences that are implemented in C:

##### Container sequences - 
list, tuples and collections.deque
They hold references and can hold objects of different types

##### Flat sequences
str, bytes, bytearray, memoryview and array.array 
They hold only one type and physically store the value in their memory space thus they are more compact but are limited to storing primitive types like char, bytes and numbers

Another way to group them could be 

##### Mutable
list, bytearray, array.array, collections.deque, memoryview

##### Immutable
tuple, str and bytes

### List comprehensions or Listcomps
A listcomp can be used to create a list, same way as a for loop but it is often quicker and more readable to use the list comp
```python
symbols = '$¢£¥€¤'
codes = [ord(symbol) for symbol in symbols]
```
In Python 3 they have their own scope but in 2.X variables declared inside would leak into the outer scope. They will also not mask the scope of surrounding scopes e.g. 

```python
>>> x = 'ABC'
>>> dummy = [ord(x) for x in x]
>>> x  1
'ABC'
>>> dummy  2
[65, 66, 67]
>>>
```