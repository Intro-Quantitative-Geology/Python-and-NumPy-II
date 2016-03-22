# Introduction to Python and NumPy, part II

## Sources
This tutorial is based on a combination of [a MATLAB tutorial from Prof. Todd Ehlers (Uni Tübingen)](http://www.geo.uni-tuebingen.de/arbeitsgruppen/mineralogie-geodynamik/geologie-geodynamik/ibm-documentation/matlab-tutorial.html) and the [Software Carpentry group's](http://software-carpentry.org/) lessons on [Programming with Python](http://swcarpentry.github.io/python-novice-inflammation/).

## Getting started
1. Since [Anaconda may be installing in the background](Anaconda.md), you should open a second Terminal window by clicking on the Dash Home icon at the top left corner of the screen, typing `terminal` into the search box, and clicking on the Terminal icon. Alternatively, you can right click on the existing Terminal icon and select **New Terminal**.
2. I assume you have also already [downloaded and extracted the lesson data](Data.md), so you can navigate to the `Data` directory to start this lesson.

    ```bash
    $ cd ~/Desktop/Lab-2/Data
    ```
**Reminder**: the `$` symbol above represents the command prompt in the Terminal window.
3. Open a new IPython window.

    ```bash
    ipython
    ```

Now we are ready to start.

## `for` loops
Loops allow parts of code to be repeated over some number of times.

1. Let's consider an example. Suppose we want to take a word and print out each letter of the word separately. We could do the following:

    ```python
    >>> word = 'rock'
    >>> print(word[0])
    r
    >>> print(word[1])
    o
    >>> print(word[2])
    c
    >>> print(word[3])
    k
    ```
But this is a bad idea. Why? Well there are two reasons. First, it does not scale nicely for long strings, and will take forever to type in. Second, it won't work if the word is not 4 characters long.

    ```python
    >>> word = 'ore'
    >>> print(word[0])
    o
    >>> print(word[1])
    r
    >>> print(word[2])
    e
    >>> print(word[3])
    ---------------------------------------------------------------------------
    IndexError                                Traceback (most recent call last)
    <ipython-input-14-e3303df6f566> in <module>()
    ----> 1 print(word[3])

    IndexError: string index out of range
    ```

2. We could do a much better job by using a `for` loop.

    ```python
    >>> word = 'rock'
    >>> for char in word:
    ...    print(char)
    ...
    r
    o
    c
    k
    ```
Note here that the `...` is displayed in the IPython window when entering code in a loop and you do not need to type in the `...`. Not only is this shorter, but it is also more flexible. Try out a different word such as `granite`. Still works, right?
3. `for` loops in Python have the general form below.

    ```python
    for variable in collection:
        do things with variable
    ```
The `variable` can be any name you like, and the statement of the `for` loop must end with a `:`. The code that should be executed as part of the loop must be indented beneath the `for` loop, and the typical indentation is 4 spaces. There is not additional special word needed to end the loop, just change the indentation back to normal.
4. Let's consider another example.

    ```python
    >>> length = 0
    >>> for letter in 'earthquake':
    ...    length = length + 1
    ...
    >>> print('There are', length, 'letters')
    There are 10 letters
    ```
Can you follow what happens in this loop?
5. Note that the variable used in the loop, `letter` in the case above is just a normal variable and still exists after the loop has completed with the final value given to letter.

    ```python
    >>> letter = 'x'
    >>> for letter in 'fault':
    ...     print(letter)
    ...
    f
    a
    u
    l
    t
    >>> print('After the loop, letter is', letter)
    ```
6. A loop can be used to iterate over any list of values in Python. So far we have considered only character strings, but we could also write a loop that performs a calculation a specified number of times.

    ```python
    >>> for number in range(5):
    ...     print(number)
    ...
    0
    1
    2
    3
    4
    ```
What happens here? Well, in this case, we use a special function called `range()` to give us a list of 5 numbers `[0, 1, 2, 3, 4]` and then print each number in the list to the screen. When given a integer (whole number) as an argument, `range()` will produce a list of numbers with a length equal to the specified number. The list starts at zero and ends with number-1. You can learn a bit more about range by typing

    ```python
    >>> help(range)
    ```
7. **Something involving array index values???**

## Conditional statements
5. Making choices
	1. Conditional statements - can change behaviour based on certain conditions `num = 37` `if num > 100:` `    print('greater')` `else:` `    print('not greater')` `print('done')` Note again that code within the given condition is indented and the statement ends with a `:` On line 2 the code check the value of `num` and proceeds differently based on the comparison that is made; Figure of this statement
	2. `if`, `else` is common, but `else` is not required `num = 53` `print('before conditional...')` `if num > 100:` `    print('53 is greater than 100')` `print('...after conditional')`
	3. Can also have multiple conditions using `elif`, which is short for `else if`: `num = -3`  `if num > 0:` `    print(num, "is positive")` `elif num == 0:` `    print(num, "is zero")` `else:` `    print(num, "is negative")` Note the usage of the `==` to compare whether a value is equal to another, rather than assigning a value.
	4. Challenge question 5.1
	4. We can also use `and` or `or` to meet multiple conditions: `if (1 > 0) and (-1 > 0):` `    print('both parts are true')` `else:` `    print('one part is not true')` versus `if (1 < 0) or (-1 < 0):` `    print('at least one test is true')`
	5. Checking out the inflammation data
		1. Checking for suspicious maxima: `if data.max(axis=0)[0] == 0 and data.max(axis=0)[20] == 20:` `    print('Suspicious looking maxima!')`
		2. Checking for healthy individuals: `elif data.min(axis=0).sum() == 0:` `    print('Minima add up to zero!')`
		3. Make note if the data look OK. `else:` `    print('Seems OK!')`
		4. Challenge question 5.2

## Other ways to read files (*Optional*)

## Github basics
