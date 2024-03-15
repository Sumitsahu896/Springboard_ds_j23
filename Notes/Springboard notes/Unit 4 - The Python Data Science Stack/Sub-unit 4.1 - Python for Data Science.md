# March 14th 2024

# TODO

- Python for data science complete.

# Data types for Data Science

## Introduction datacamp

Things which we will learn:

- Lists
- Tuples
- Strings
- Dictionary
- Int
- Float
- Booleans
- Sets
- Advanced Datatypes:
    - Default dict
    - Named Tuple
    - Data classes

### Lists

- Creating a list
- list.extend()
    - Add elements to the list
- list.position(’Name of the element’)
    - Tells the position of the element
- list.pop(position)
    - Remove that element from the list
- sorted() function
    - For numbers, list lowest to highest
    - For alphabet, from A to Z
    - Returns a new list

### Tuple

![[Pasted image 20240315180330.png]]
- Usually created by zipping them together:
    - top_pairs = list(zip(us_cookies, in_cookies))

##### Unpacking Tuple
- Unpacking tuples is a very expressive way for working with data
```
us_num_1, in_num_1 = top_pairs[0]
print(us_num_1)
```
- Another way is to use in loop.
##### Enumerating positions
- Enumeration is used to return the position and the data:
```
for idx, item in enumerate(top_pairs):
	us_cookie, in_cookie = item
	...
```
##### Ways to make a tuple
![[Pasted image 20240315183711.png]]

### Strings
![[Pasted image 20240315184507.png]]
![[Pasted image 20240315184622.png]]
