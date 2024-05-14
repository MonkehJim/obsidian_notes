- For loops are used for looping through entire sets of data in lists. Some of the first examples of loops use a list called `magicians`
```Python
magicians = ['Harry','Luke','George']
for magician in magicians:
	print(f"That was a good trick {magician.title()}")
print("That was a great show everyone!")

"""That was a good trick Harry
That was a good trick Luke
That was a good trick George
That was a great show everyone!"""
```

- From what I initially thought, Python does not know how to differentiate between singular `magician` and plural `magicians`. The way the for loop works is that a temporary variable is created that exists only for the for loop. The value of this variable is then set to the first item of the list it is referencing, so the first item in `magicians`.
- Python will carry out the loop for that first element then repeat for the next element in a list. It does this until it reaches the end of the list.

### Using range() function
'Pythons `range()` function makes it easy to generate a series of numbers. For example, you can use the `range()` function to print a series of numbers like so:'
```Python
for value in range(1,5):
	print(value)

1
2
3
4
```

- Note that it prints numbers from 1 to 4 and NOT to 5. Programming languages often do this when counting numbers. Python interprets this as 'start at number 1 and finish printing numbers at 5'. This means it totally stops when it reaches 5 and doesn't print it.

To print numbers 1 to 5, we actually need to use a `range(1,6)`:
```Python
for value in range(1,6):
	print(value)

1
2
3
4
5
```

The previous two examples used a range that was given *two arguments* (i.e. A start and an end value like start at 1, end at 5). 

You can give `range()` one argument and it will give a sequence of numbers starting at 0:
```Python
for value in range(6):
	print(value)

0
1
2
3
4
5
```

`range()` can also tell Python to skip numbers in a given range. If given a third *argument*, Python will use this as a step size when generating the range. This will add that value onto the original starting value in the range.

### Lists of numbers

For example, to get every even number between 2 and 20 in a list format, we can do:
```Python 
even_num = list(range(2,21,2))
print(even_num)

[2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
```

- The reason that the range starts at 2 and not 1 is because if we added 2 to that starting value, we would get every odd number between 1 and 21
- Although 21 is an odd number, it must go up to this number in order to include 20 in the range

Alternatively, here is odd numbers between 1 and 21:
```Python
odd_num = list(range(1,22,2))
print(odd_num)

[1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21]
```

You can make practically any set of numbers with the `range()` function. In this case, we can make a blank list and have a `for loop` append values into the list then print it at the end. This takes each value in `range(1,11)`, multiplies by ^3 then adds it to the empty list.
```Python
cube_num = []
for value in range(1,11)
	cube = value ** 3
	cube_num.append(cube)
print(cube_num)

[1, 8, 27, 64, 125, 216, 343, 512, 729, 1000]
```

The approach above does work, but it can be simplified to carry out the same function. The point of showing the above example is that the code needs to be understandable first before it can be made *more efficient* (less lines of code). Now getting the square numbers between 1 and 10 will look like this:
```Python
square_num = []
for value in range(1,11)
	square_num.append(value**2)
print(square_num)

[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```
