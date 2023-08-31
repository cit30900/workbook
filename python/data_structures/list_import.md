# Import CSV Files to Lists

The simplest way to import a CSV file to a Python list is to use the `csv` module.

```{important}
Ensure you activate your virtual environment with the following command:

`workon cit30900env`
```

(python:data:install_csv)=
## Install the `csv` Module
Use the following command **in your active virtual environment** to install the `csv` module:

```
pip install csv
```

(python:data:import_csv_list)=
## Import a CSV to a Python List

Use the following code to import a CSV file to a Python list:

```
import csv

filename = 'myfile.csv'
with open(filename, 'r') as f:
    # Create an iterable element that will hold the contents of the CSV file
    reader = csv.reader(f)
    # Loop through reader and view the contents of the file
    for row in reader:
        print(row)
```
Each row of the CSV file will be printed to the screen.

**However**, you cannot use the `reader` as a variable in your program. You should assign the value of the reader to a Python list.

```
import csv

filename = 'myfile.csv'
mylist = []
with open(filename, 'r') as f:
    # Create an iterable element that will hold the contents of the CSV file
    reader = csv.reader(f)
    # Convert the reader to a list
    mylist = list(reader)
```

This will create a "list of lists" where each row in the CSV file is a list, and each list is an element of a "parent" list.

Let's assume this is the content of your CSV file:
```
A, B
C, D
```
By following the instructions above, you will receive a Python list of this shape:
```
[['A', 'B'], ['C', 'D']]
```

Each row of the CSV is its own list, and all of the lists are nested in a single list. Unfortunately, this is the case even when your CSV contains a single row of data.

Here is a CSV file with a single row of data
```
W, X, Y, Z
```

When imported and converted to a list, Python will report the value as:
```
[['W', 'X', 'Y', 'Z']]
```

A CSV with one row of data should be imported into a **1-dimensional** list in Python. However, your list is nested in a parent list, giving you a **2-dimensional** list.

(python:data:import_csv_list_1dimension)=
## Import a CSV to a 1-Dimensional List
If you need to import your CSV into a 1-dimensional list, do the following:

1. Declare an empty list
2. Import the CSV to a `reader` object
3. Loop through the `reader` and **`extend`** the list variable with each value in the reader

```
import csv

filename = 'myfile.csv'
mylist = []
with open(filename, 'r') as f:
    # Create an iterable element that will hold the contents of the CSV file
    reader = csv.reader(f)
    # Loop through the reader and extend the list with values
    for row in reader:
        mylist.extend(row)
```

Using this technique will convert a CSV with a single row into a 1-dimensional list in Python.

CSV file contents:
```
G, H, I, J, K
```

Will become:
```
['G', 'H', 'I', 'J', 'K']
```