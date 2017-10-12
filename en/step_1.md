There are a few ways in which what we think of as 'a number' can be stored as a variable in Python. Let's start with the most common type that you're likely to want to round: a **float**. Python floats are real numbers that include a decimal point, for example `234.8`, `60.0`, or `1.23456`.

- If you want to round a `float` to a certain number of decimal places, you can use the `round` function.

```python
>>> round(1.23456,2)
1.23
>>>
```

- In the example above, you rounded to two decimal places. If you want to change that to three decimal places, you simply alter the number after the comma in the `round` function.

```python
>>> round(1.23456,3)
1.235
>>>
```
- The same method applies to **integers** as well. Even though they're whole numbers, they can still be rounded (for example, to the nearest 10).

```python
>>> round(458,-1)
460
>>>
```

Here you've used a `-` sign to indicate that you're rounding before the decimal point (i.e. the whole number component).

- Using `-` works on floats too:

```python
>>> round(666.66,-1)
670
>>>
```

There is one other way in which you can handle a number in Python, and that's as a **string**.

- If you try to use `round` on a string, you'll receive a `TypeError`:


```python
>>> round(23.67,1)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: type str doesn't define __round__ method
>>>
```
- However, you can still achieve the same goal using the `.format` function.

```python
>>> "{0:.2f}".format(56.767856)
56.77
>>>
```
  Note that the output here is now a string, not a float.

- If you want to alter the number of decimal places, then just change the modifier.

```python
>>> "{0:.4f}".format(56.767856)
56.7679
>>>
```

This can be useful if you have a program that is processing floats and you want to retain its high level of precision, but you also want to neatly present one the values as a string output — perhaps to write it to a log file or to display it on a GUI.
