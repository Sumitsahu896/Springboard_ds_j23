
# Data types for Data Science

## Introduction datacamp

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
### Using dictionaries
![[Pasted image 20240315194027.png]]
![[Pasted image 20240315194225.png]]
##### Altering dictionaries
![[Pasted image 20240315195056.png]]
![[Pasted image 20240315195159.png]]
![[Pasted image 20240315195241.png]]
##### Pythonically using dictionaries
![[Pasted image 20240316114600.png]]
- in operator is more clearer because it returns boolean
![[Pasted image 20240316114718.png]]


##### Mixed data types in dictionaries

![[Pasted image 20240318150300.png]]
![[Pasted image 20240318150748.png]]

## Numeric Data Types
- integer
- float
- decimal
- string print 
	- ``` print(f"{0.0000001: .7f}")```
- 
##### Set
- Unique
- Unordered
- Mutable
##### Counter
![[Pasted image 20240318164707.png]]
![[Pasted image 20240318164736.png]]

##### Default dictionary
![[Pasted image 20240319113114.png]]

##### namedtuple

![[Pasted image 20240319114455.png]]
![[Pasted image 20240319114537.png]]

##### Dataclasses
![[Pasted image 20240319115530.png]]

![[Pasted image 20240319115551.png]]

![[Pasted image 20240319115620.png]]

![[Pasted image 20240319115649.png]]

![[Pasted image 20240319115719.png]]
![[Pasted image 20240319115733.png]]


# Python data science toolbox

##### User-defined functions
- str()
- Function header, function body
- ![[Pasted image 20240320182737.png]]

##### Multiple parameters and return values
- Make functions return multiple tuples.
![[Screenshot 2024-03-20 at 6.53.53 PM.png]]

##### Scope and user-defined functions
