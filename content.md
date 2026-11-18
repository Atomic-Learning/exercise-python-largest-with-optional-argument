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

# Sample Solution

Click below to reveal a sample solution.

>[!HIDDEN]
> We can start by using the `max()`{.python} function to find the largest value in the list. When `abs_value`{.python} is `True`{.python}, the code compares the positive maximum with the negative of the smallest value and returns the larger of the two. When `abs_value`{.python} is `False`{.python} the if-block will not be entered and the largest value `max_value`{.python} will be returned.
>
> ```py-cell
> def largest(list_in, abs_value=False):
>     max_value = max(list_in)
>     if abs_value:
>         min_value = min(list_in)
>         return max(max_value, -min_value)
>     return max_value
> ```
>
> ## Test Calls
>
> ```py-cell
> print(largest([1, 2, -3]))
> print(largest([1, 2, -3], False))
> print(largest([1, 2, -3], True))
> print(largest([1, 2, -3, 4], True))
> ```
