# List Comprehensions
*Comprehensions* are a Python mechanism that allow you to quickly loop through and modify or create subsets of lists.

(python:data:list_comprehension)=
## Create a New List with a Comprehension

Let's duplicate a list into a new list with a comprehension *(this is a silly example, but gets us started)*.
```
# Create a copy of a list
numbers = [1,2,3,4,5,6,7,8,9,10]

new_numbers = [num for num in numbers]
```
The value of `new_numbers` will now be `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]`.

The code `num for num in numbers` translates to "Add each 'num' in the 'numbers' array to the `new_numbers` list.

(python:data:list_comprehension_mod)=
## Create a New, Modified List with a Comprehension
In the code above, `num` represents a single element of the `numbers` list. We can modify the value of `num` before adding it to the `new_numbers` list.

```
# Add 1 to each element of a list and put the new values in a new list
numbers = [1,2,3,4,5,6,7,8,9,10]

new_numbers = [num+1 for num in numbers]
```
The value of `new_numbers` will now be `[2, 3, 4, 5, 6, 7, 8, 9, 10, 11]`.

Because we are working with integers, we can do any mathematical equation here. For example, let's cube all of the numbers (raise them to the power of 3).

```
# Cube each element of a list and put the new values in a new list
numbers = [1,2,3,4,5,6,7,8,9,10]

new_numbers = [num**3** for num in numbers]
```

The value of `new_numbers` will now be `[1, 8, 27, 64, 216, 343, 512, 729, 1000]`.

(python:data:list_comprehension_subset)=
## Create a Subset of a List with a Comprehension

You can add conditional logic to a comprehension to filter specific values into a new list.

```
# Filter the numbers list for even numbers
numbers = [1,2,3,4,5,6,7,8,9,10]

# Use the modulus operator (%) to check for a remainder
# If the remainder of the division `num/2` is 0, it's an even number
new_numbers = [num for num in numbers if num % 2 == 0]
```
The value of `new_numbers` will now be `[2, 4, 6, 8, 10]`.

This works for strings too. Assume I want to find values in a list that match a certain pattern.

```
# Filter a list of strings to find words that contain 'e'
fruits = ['Apple', 'Banana', 'Cherry', 'Date', 'Eggplant', 'Fig']

e_fruits = []

e_fruits = [f for f in fruits if 'e' in f]

```
The value of `e_fruits` will now be `['Apple', 'Cherry', 'Date']`.

```{tip}
Why isn't 'Eggplant' included in the filtered list?
```