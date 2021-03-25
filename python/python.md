<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://www.python.org/">
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Python-logo-notext.svg/768px-Python-logo-notext.svg.png" alt="Logo" width="150">
  </a>

  <h3 align="center">Python cheatsheet</h3>

  <p align="center">
  Based on <a href="https://www.pythoncheatsheet.org/#Using-for-Loops-with-Lists">pythoncheatsheet.org</a>, visit for full experience.
    <br />
    <br />
    <a href="https://github.com/johnunar/cheatsheets/issues">Report Bug</a>
    ·
    <a href="https://github.com/johnunar/cheatsheets/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
## Table of Contents
* [Useful helpers](#useful-helpers)
* [Basics](#basics)
    * [Lists](#lists)
    * [Tuples](#tuples)
* [Roadmap](#roadmap)
* [Contact](#contact)

<!-- motivation -->
## Motivation
Fire up your python console and do this first. 
```python
import this
```
<!-- Useful helpers -->
## Useful Helpers
There are some packages that will make your life easier. If you are using PyCharm, you can use my [watchers.xml](https://github.com/johnunar/cheatsheets/blob/master/python/watchers.xml) file
to automatically import File Watchers that improve your code on each save.
### [Pylint](https://www.pylint.org/)
Pylint is a tool that checks for errors in Python code, 
tries to enforce a coding standard and looks for code smells. 
It can also look for certain type errors, it can recommend suggestions about how particular blocks can be
refactored and can offer you details about the code's complexity.
### [Black](https://pypi.org/project/black/)
Black makes code review faster by producing the smallest diffs possible.
Blackened code looks the same regardless of the project you’re reading.
Formatting becomes transparent after a while and you can focus on the content instead.
### [iSort](https://pypi.org/project/isort/)
isort is a Python utility / library to sort imports alphabetically, and automatically separated
into sections and by type. It provides a command line utility,
Python library and plugins for various editors to quickly sort all your imports.
It requires Python 3.6+ to run but supports formatting Python 2 code too.

<!-- Basics -->
## Basics

### Math operators
**Highest** to **lowest** precedence
<table>
<thead><tr>
<th>Operator</th>
<th>Operation</th>
<th>Example</th>
</tr>
</thead>
<tbody>
<tr>
<td>**</td>
<td>Exponent</td>
<td><code>2 ** 3 = 8</code></td>
</tr>
<tr>
<td>%</td>
<td>Modulus/Remainder</td>
<td><code>22 % 8 = 6</code></td>
</tr>
<tr>
<td>//</td>
<td>Integer division</td>
<td><code>22 // 8 = 2</code></td>
</tr>
<tr>
<td>/</td>
<td>Division</td>
<td><code>22 / 8 = 2.75</code></td>
</tr>
<tr>
<td>*</td>
<td>Multiplication</td>
<td><code>3 * 3 = 9</code></td>
</tr>
<tr>
<td>-</td>
<td>Subtraction</td>
<td><code>5 - 2 = 3</code></td>
</tr>
<tr>
<td>+</td>
<td>Addition</td>
<td><code>2 + 2 = 4</code></td>
</tr>
</tbody>
</table>

### Data types
<table>
<thead><tr>
<th>Data Type</th>
<th>Examples</th>
</tr>
</thead>
<tbody>
<tr>
<td>Integers</td>
<td><code>-2, -1, 0, 1, 2, 3, 4, 5</code></td>
</tr>
<tr>
<td>Floating-point numbers</td>
<td><code>-1.25, -1.0, --0.5, 0.0, 0.5, 1.0, 1.25</code></td>
</tr>
<tr>
<td>Strings</td>
<td><code>'a', 'aa', 'aaa', 'Hello!', '11 cats'</code></td>
</tr>
</tbody>
</table>

### Strings

#### String Concatenation:
```python
>>> 'Alice' 'Bob'
'AliceBob'
```
**Note**: Avoid + operator for string concatenation. Prefer string formatting.

#### String Replication:
```python
>>> 'Alice' * 5
'AliceAliceAliceAliceAlice'
```

### Variables
You can name a variable anything as long as it obeys the following rules:

1. It can be only one word.
2. It can use only letters, numbers, and the underscore (_) character.
3. It can’t begin with a number.
4. Variable name starting with an underscore (_) are considered as "unuseful`.

#### The print() Function
```python
>>> print('Hello world!')
Hello world!
>>> a = 1
>>> print('Hello world!', a)
Hello world! 1
```

#### The input() Function
```python
>>> print('What is your name?')   # ask for their name
>>> myName = input()
>>> print('It is good to meet you, {}'.format(myName))
What is your name?
Al
It is good to meet you, Al
```

#### The len() Function
Evaluates to the integer value of the number of characters in a string:
```python
>>> len('hello')
5
```
**Note**: test of emptiness of strings, lists, dictionary, etc, should not use len, but prefer direct boolean evaluation.

```python
>>> a = [1, 2, 3]
>>> if a:
>>>     print("the list is not empty!")
```

<!-- LISTS -->
## Lists
**Note**: Try them on strings! Seems familiar?

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']

>>> spam
['cat', 'bat', 'rat', 'elephant']
```

### Negative Indexes
```python
>>> 'The {} is afraid of the {}.'.format(spam[-1], spam[-3])
'The elephant is afraid of the bat.'
```

### Sublists Slicing
```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']
>>> spam[0:4]
['cat', 'bat', 'rat', 'elephant']
```

```python
>>> spam[1:3]
['bat', 'rat']
```

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']
>>> spam[:2]
['cat', 'bat']
```

```python
>>> spam[1:]
['bat', 'rat', 'elephant']
```

### Changing Values
```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']
>>> spam[1] = 'aardvark'

>>> spam
['cat', 'aardvark', 'rat', 'elephant']

>>> spam[2] = spam[1]

>>> spam
['cat', 'aardvark', 'aardvark', 'elephant']

>>> spam[-1] = 12345

>>> spam
['cat', 'aardvark', 'aardvark', 12345]
```

### List Concatenation and Replication
```python
>>> [1, 2, 3] + ['A', 'B', 'C']
[1, 2, 3, 'A', 'B', 'C']

>>> ['X', 'Y', 'Z'] * 3
['X', 'Y', 'Z', 'X', 'Y', 'Z', 'X', 'Y', 'Z']

>>> spam = [1, 2, 3]

>>> spam = spam + ['A', 'B', 'C']

>>> spam
[1, 2, 3, 'A', 'B', 'C']
```

### Remove Values
```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']
>>> del spam[2]
>>> spam
['cat', 'bat', 'elephant']
```

### For Loops
```python
>>> supplies = ['pens', 'staplers', 'flame-throwers', 'binders']
>>> for i, supply in enumerate(supplies):
>>>     print('Index {} in supplies is: {}'.format(str(i), supply))
Index 0 in supplies is: pens
Index 1 in supplies is: staplers
Index 2 in supplies is: flame-throwers
Index 3 in supplies is: binders
```

### The in and not in Operators
```python
>>> 'howdy' in ['hello', 'hi', 'howdy', 'heyas']
True

>>> spam = ['hello', 'hi', 'howdy', 'heyas']
>>> 'cat' in spam
False

>>> 'howdy' not in spam
False

>>> 'cat' not in spam
True
```

### Multiple assignment
```python
>>> cat = ['fat', 'orange', 'loud']

>>> size, color, disposition = cat
```

```python
>>> a, b = 'Alice', 'Bob'
>>> a, b = b, a
>>> print(a)
'Bob'
```

### Tuples
```python
>>> eggs = ('hello', 42, 0.5)
>>> eggs[0]
'hello'
```

```python
>>> eggs[1:3]
(42, 0.5)
```

Tuples and strings are **immutable**, Lists are **not**.

<!-- ROADMAP -->
## Roadmap
* Add more code snippets
* Add more tools
* Make a separate file for each of the cheatsheets
* Generate a more human-friendly cheatsheet (.pdf most likely)

<!-- CONTACT -->
## Contact

Jan Unar
* [unar.dev](https://unar.dev/)
* [@JohnnyUnar](https://twitter.com/JohnnyUnar)
* [johnunar@gmail.com](mailto:johnunar@gmail.com)

Project Link: [https://github.com/johnunar/cheatsheets](https://github.com/johnunar/cheatsheets)