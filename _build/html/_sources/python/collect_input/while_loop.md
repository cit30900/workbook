# Collect User Input Using a While Loop
When collecting user input at the command line, you frequently want to validate that the user has provided expected input before moving on. If the input is not expected, you can ask the user to try again.

One method for doing this is to use a `while` loop. When doing so, you must give the `while` loop some condition to evaluate. Here is some pseudocode that may help:

```
condition = False

while condition == False:
    collect input
    evaluate the input
        if input is expected, set condition to True
        if input is not expected, the loop will restart
```

This process is illustrated in the following activity diagram. 
* *[Download the activity diagram as a PDF](doc/user-input-loop.pdf)*

```{image} img/user-input-loop.png
:alt: Activity diagram of the user input loop
:align: center
:width: 400px
```