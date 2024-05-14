### Useful functions
There are a few functions that are helpful when working with lists of numbers. For example, you can easily find the minimum, maximum and sum of a list using `min()`,`max()`and `sum()`.
```Python
digits = list(range(11)) #Generates a list of numbers from 0-10, sequentially
print(min(digits))
print(max(digits))
print(sum(digits))

Output:
0
10
55

```

### List *comprehensions*
List comprehensions allow you to generate lists of numbers in less lines of code compared to previous methods seen in [[For loops & range()#Lists of numbers]].

This new *comprehension* combined the functionality of a for loop with the creation of new elements to generate something like this:
```Python
squares = [value**2 for value in range(1,11)]
print(squares)

Output:
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

In the example above, a list name is chosen (a particularly descriptive or useful name depending on what the function inside actually does). Inside the square brackets defines the expression that the new values should follow, so `value**2` will raise each number to the second power and `for value in range(1,11)` will repeat this expression for every number between 1 and 10.



