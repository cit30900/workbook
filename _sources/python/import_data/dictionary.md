# Import CSV Files to Dictionaries

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

(python:data:import_csv_dictionary)=
## Import a CSV as a Dictionary

If your CSV file contains a row of headings that label the data in each column of the CSV, you can import that entire structure to Python so that each value is labeled with its row heading.

This will generate a Python **dictionary** object for each row in the CSV file. The dictionary will contain **key:value pairs**, where the *key* is the row heading and the *value* is the content of that column in the current row of the CSV file.

Use the following code to import a CSV file to a Python list:

```
from csv import DictReader

filename = 'myfile.csv'
with open(filename, 'r') as f:
    # Create a DictReader object that will read the contents of the CSV file as dictionaries
    dict_reader = DictReader(f)
    # Create an iterable element that will hold the contents of the CSV file as a list
    # This will result in a LIST OF DICTIONARIES
    list_of_dict = list(dict_reader)
    # Loop through the list and view the contents of the file
    for d in list_of_dict:
        # 'k' refers to the 'key' and 'v' refers to the 'value'
        # Note that you retrieve the key:value pairs through the dictionary's `.items()` method
        for k, v in d.items():
            print(f'{k}: {v}')
```

Each **key-value pair** of *each* row will be printed to the screen.

**However**, you cannot access the values in the list outside of your `with` statement. You should assign the value of the DictReader to a Python list.

```
from csv import DictReader

filename = 'myfile.csv'
nameslist = []

with open(filename, 'r') as f:
    # Create a DictReader object that will read the contents of the CSV file as dictionaries
    dict_reader = DictReader(f)
    # Create an iterable element that will hold the contents of the CSV file as a list
    # This will result in a LIST OF DICTIONARIES
    list_of_dict = list(dict_reader)
    # Loop through the list and view the contents of the file
    for d in list_of_dict:
        namelist.append(d)
```
The above code creates a list called `nameslist` that holds a dictionary that represents each row of the CSV file.

Let's assume this is the content of your CSV file:
```
firstname, lastname
Fred, Rogers
Shirley, Bassey
```
By following the instructions above, you will receive a Python list of this shape:
```
# nameslist will contain the following:
[{'firstname': 'fred', 'lastname': 'rogers'}, {'firstname': 'shirley', 'lastname': 'bassey'}]
```

Each row of the CSV is its own dictionary, and all of the dictionaries are nested in a single list.

(python:data:import_csv_dictionary_access)=
## Accessing Values in a List of Dictionaries

Given the example above, you can access the data stored in each dictionary by looping through the list and then using the *square bracket notation* of a dictionary.

```
for name in nameslist:
    print(f"{name['firstname']} {name['lastname']}")
```

The code above will print the following to the screen:

```
Fred Rogers
Shirley Bassey
```