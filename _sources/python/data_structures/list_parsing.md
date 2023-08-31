# Parsing Python Lists

There are several ways to retrieve specific elements of a Python list.

(python:data:list_index)=
## Obtain List Element by Index
Python lists are indexed by number, starting from 0. To obtain a specific list element, you can select the index with square brackets.

```
cars = ['Ford', 'Toyota', 'GM', 'Volvo', 'Chevrolet', 'Porsche']

# Get the first element of the list
print(cars[0])
```
The previous code will print `Ford` to the screen.

```
cars = ['Ford', 'Toyota', 'GM', 'Volvo', 'Chevrolet', 'Porsche']

# Get the third element (index 2) of the list
print(cars[2])
```
The previous code will print `GM` to the screen.

You can also easily get the last element of the list by reading it backwards
```
cars = ['Ford', 'Toyota', 'GM', 'Volvo', 'Chevrolet', 'Porsche']

# Get the last element of the list
print(cars[-1])
```
The previous code will print `Porsche` to the screen.

(python:data:list_slice)=
## Obtain List Element by Slice
You can obtain specific subsets of a list by **slicing** the list according to its indices.

```
cars = ['Ford', 'Toyota', 'GM', 'Volvo', 'Chevrolet', 'Porsche']

# Get the first two elements of the list
print(cars[0:2])
```
The previous code will print `['Ford', 'Toyota']` to the screen.

The slice syntax is **inclusive of the first index** and **EXclusive of the second**. 

The slice `[0:3]` will retrieve elements with the index of 0, 1, and 2, but **not** the element with index of 3.

You can slice a list from any index to any other index.

```
cars = ['Ford', 'Toyota', 'GM', 'Volvo', 'Chevrolet', 'Porsche']

# Get the first two elements of the list
print(cars[3:5])
```
The previous code will print `['Volvo', 'Chevrolet']` to the screen (indices 3 and 4, but **not** index 5).