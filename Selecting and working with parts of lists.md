### Slicing a list
To make a slice of a list, you must specify an index for the first and last elements that we want. Like when working with `range()`, Python also stops one element before the index that you specify. *For example*, if I had a list of 5 players and gave the index `print(players[0:3])`, it would only list off elements 0, 1, and 2.

```Python
players = ["charles", "martina", "michael", "florence", "eli"]
print(players[0:3])

Output:
['charles', 'martina', 'michael']
```

When indexing, you can generate any subset that we desire so if we only want the second, third and fourth then we can make:
```Python
print(players[1:4])

Output:
['martina', 'michael', 'florence']
```

If there is no first index in a slice, Python will automatically start from the beginning of a list. This works the opposite way around also (omitting an end index).
```Python
print(players[:4])
print(players[2:])

Output:
['charles', 'martina', 'michael', 'florence']
['michael', 'florence', 'eli']
```

### Copying a lists contents
By omitting the first and second index when slicing a list, it tells Python to make a slice that begins with the first item and ends with the last item of a list, effectively copying it.

This slice can be set to another variable to create a copy of the list:
```Python
#list_copying

my_foods = ['Pizza','Fish&Chips','Red Velvet']
friend_foods = my_foods[:]

print(my_foods)
print(friend_foods)

Output:
['Pizza', 'Fish&Chips', 'Red Velvet']
['Pizza', 'Fish&Chips', 'Red Velvet']
```

Although the copy of the is based off the first one, the copy is totally independent from the first as its created a whole new list. This can be proven when adding different items to each list:
```Python 
my_foods = ['Pizza','Fish&Chips','Red Velvet']
friend_foods = my_foods[:]

print(my_foods)
print(friend_foods)

#proving that they are actually two separate lists we can add items, independent of the first

my_foods.append('Chocolate')
friend_foods.append('Ice Cream')
print(my_foods)
print(friend_foods)

Output:
['Pizza', 'Fish&Chips', 'Red Velvet']
['Pizza', 'Fish&Chips', 'Red Velvet']
['Pizza', 'Fish&Chips', 'Red Velvet', 'Chocolate']
['Pizza', 'Fish&Chips', 'Red Velvet', 'Ice Cream']
```

In Python we simply cannot set our `friend_foods` variable to be equal to `my_foods` as this does not make a copy but simply means that each name will point to the same list. If 1 item is added to each list, it will update both but *this is technically the same list*, so both supposedly separate items are added to the same list.
```Python
#the wrong way of copying a list

my_foods = ['Pizza','Fish&Chips','Red Velvet']
friend_foods = my_foods

print(my_foods)
print(friend_foods)

my_foods.append('Chocolate')
friend_foods.append('Ice Cream')
print(my_foods)
print(friend_foods)

Output:
['Pizza', 'Fish&Chips', 'Red Velvet', 'Chocolate', 'Ice Cream']
['Pizza', 'Fish&Chips', 'Red Velvet', 'Chocolate', 'Ice Cream']
```
