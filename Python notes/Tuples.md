A *Tuple* is an *immutable* list, meaning it cannot any of the values contained within. Anything referred to as *immutable* in Python means its values cannot change so this applied to variables.

A Tuple looks almost identical to a regular list but is defined using parentheses instead of square brackets. Once a Tuple is defined, individual elements can be accessed by using each items index, the same as you would with a list.

```Python
#tuples

dimensions = (200, 50)

print(dimensions[0])
print(dimensions[1])

Output:
200
50
```

Trying to change the value of a tuple will return a `TypeError` as this is not possible.
```Python 
#trying to change a tuple value

dimensions = (200, 50)
dimensions[0] = 250
print(dimensions)

Output:
Traceback (most recent call last):
  File "[File Location]", line 7, in <module>
    dimensions[0] = 250
    ~~~~~~~~~~^^^
TypeError: 'tuple' object does not support item assignment
```

### For Loops
For loops can also be used with Tuples the same as with any other list.
```Python
#for loops

for dimension in dimensions:
	print(dimension)

Output:
200
50
```

### Overwriting a Tuple
Although the start of this page it states "A *Tuple* is an *immutable* list, meaning it cannot any of the values contained within", Tuples can be overwritten by new variables that represent a tuple. 
```Python
#overwriting a tuple

dimensions = (200, 50)
print("Original Tuple dimensions list")
for dimension in dimensions:
    print(dimension)

dimensions = (400,100)
print("\nThe new tuple dimensions list:")
for dimension in dimensions:
    print(dimension)

Output:
Original Tuple dimensions list
200
50

The new tuple dimensions list:
400
100
```

