# Task

Define a function called `largest`{.python} that takes:

* a list as a required positional argument;
* a boolean keyword argument named `abs_value`{.python}, defaulting to `False`{.python}.

# Required behaviour

* If `abs_value`{.python} is `False`{.python}, return the largest value in the list.
* If `abs_value`{.python} is `True`{.python}, return the absolute value of the list item with largest absolute value.

You may assume that the list is not empty.

# Starter cell

```py-cell
# Write your function here

# Test on a few lists
print(largest([1, 2, -3])) # Should return 2
print(largest([1, 2, -3], False)) # Should return 2
print(largest([1, 2, -3], True)) # Should return 3, since -3 has the largest absolute value
print(largest([1, 2, -3, 4], True)) # Should return 4

```
