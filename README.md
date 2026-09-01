# PA1 | ECE2112 | EXPERIMENT 1 | DIONALDO, PVA
---

### **Introduction to Python Programming**
#### Submitted by Pierre Van Aken A. Dionaldo | 2ECE-A | 09.01.2026

This repository showcases the objective and detailed discussion of the experiment from the Programming Assignment 1 last August 25, 2026 where the class discussed Module 1 - **Base Computing with Python**


---
### **Objectives**
---
At the end of this experiment, the students are expected to:

1. use basic Python functions, operators, and string operations;
2. manipulate strings using indexing, slicing, and built-in string methods;
3. apply sequence unpacking to manipulate the elements of a list; and
4. construct simple Python functions that return a specified result.

At the end of this experiment, the students are expected to:

1. use basic Python functions, operators, and string operations;
2. manipulate strings using indexing, slicing, and built-in string methods;
3. apply sequence unpacking to manipulate the elements of a list; and
4. construct simple Python functions that return a specified result.

---
### **Programming Problems**
---
#### **A. Word Rotation Problem**
Create a function named rotate_word() that accepts a non-empty string. Move the first character
of the string to the end while keeping all remaining characters in their original order. Preserve the
capitalization of every character
<br>

**Function format**: rotate_word (text)


**CODE:**
```python
print ("Word Rotation Problem")
def rotate_word (text):
    s = text[1:len(text):1] + text [0]
    print (s)

rotate_word ("python")
rotate_word ("logic")
rotate_word ("Code")
rotate_word ("A")
```

**OUTPUT:**
```python
Word Rotation Problem

rotate_word("python")  # --> "ythonp"
rotate_word("logic")   # --> "ogicl"
rotate_word("Code")    # --> "odeC"
rotate_word("A")       # --> "A"
```


The following functions and methods in this code are:
- `print ("Word Rotation Problem \n")`: This indicates the headline for programmers to distinguish the program easily
   > "\n" specifically refers to an escaped new line

- `def rotate_word (text)`: defining the function rotate_word to the value "text" 
- `s`: variable used for the function
- `s = text [1:len(text):1] + text [0]`: a string method to slice a given string into parts
  > text [index of first element: number of characters: increment]
  > - index of first element: the index where slicing begins
  > - number of characters: the index where slicing stops
  > - increment: the number of index where it moves between elements
- `len(text)`: — a string method used to count the total number of characters
- `text [index]`: — a string method used to get the value of a specific index
- `print(s)`: prints the value of variable s, where it is defined as the function of **rotate_word (text)**

##### USER INPUT EXAMPLE
```python
- print ("Word Rotation Problem (User Input)\n")

text = str(input("Enter a Word:")) 
rotate_word (text)
```

**OUTPUT:**
```python
Word Rotation Problem (User Input)

Enter a Word: Pierre
ierreP
```

This function is also similar to the first part of the problem, as this is just a user input version of the program.

Here are the functions and methods used:
- `print ("Word Rotation Problem (User Input)\n")`: This indicates the headline for programmers to distinguish the program easily
- `text = str(input("Enter a Word:"))`: syntax for user input value
  > str is used  because it represents and manipulates textual datas

- `rotate_word(text)`: the used function for this problem
---

#### B. Username Builder Problem

Create a function named make_username() that accepts two strings: first name and last name. The
function must:

1. convert all letters to lowercase;
2. remove all spaces from the first name;
3. remove all spaces from the last name; and
4. join the processed first and last names using one period (.).

**Function format**: make_username (first_name, last_name)

**CODE:**
```python
print ("Username Builder Problem\n")

def make_username (first_name, last_name):
    first_n = first_name.lower().replace(" ","")
    last_n = last_name.lower().replace(" ","")
    return first_n + "." + last_n

print(make_username ("Ada", "Lovelace"))
print(make_username ("Alan", "Turing"))
print(make_username ("Ana Maria", "De Leon"))
```

**OUPUT:**
```python
Username Builder Problem

make_username("Ada", "Lovelace")        # --> "ada.lovelace"
make_username("Alan", "Turing")         # --> "alan.turing"
make_username("Ana Maria", "De Leon")   # --> "anamaria.deleon
```

The following functions and methods in this code are:
- `print ("Username Builder Problem\n")`: This indicates the headline for programmers to distinguish the program easily
  > "\n" specifically refers to an escaped new line

- `def make_username (first_name, last_name)`: defining the function make_username to the value "first_name" and "last_name"
- `first_n`: variable used for first_name
- `first_name.lower().replace(" ","")`: function for converting the FIRST name to lowercase and removing all spaces
  > lower () is used to convert all text to lowercase
  > replace () is used to change certain characters to new characters
- `last_n`: variable used for last_name
- `last_name.lower().replace(" ","")`: function for converting the LAST name to lowercase and removing all spaces
  > lower () is used to convert all text to lowercase
  > replace () is used to change certain characters to new characters
- `return first_n + "." + last_n`: the return value of the function **make_username**
  
- `print (make_username("Ada", "Lovelace")`: prints the output of the function **make_username**


##### USER INPUT EXAMPLE
```python
print ("Username Builder Problem (User Input)\n")

first_name = str(input("Enter First Name: "))
last_name = str (input("Enter Last Name: "))
print (make_username (first_name, last_name))
```

**OUTPUT:**
```python
Username Builder Problem (User Input)

Enter First Name:  Pierre Van Aken
Enter Last Name:  Dionaldo
pierrevanaken.dionaldo
```

The following functions and methods in this code are:
- `print ("Username Builder Problem (User Input\n")`: This indicates the headline for programmers to distinguish the program easily
- `first_name = str(input("Enter First Name: "))`: syntax for user input value of the first name
  > str is used because it represents and manipulates textual data
- `last_name = str(input("Enter Last Name: "))`: syntax for user input value of the last name
  > str is used because it represents and manipulates textual data

- `print (make_username (first_name, last_name))`: prints the output of the function **make_username**
---

#### C. Bookend Swap Problem

Create a function named swap_bookends() that accepts a list containing at least two elements. Unpack the list into three variables:

- first – the first element;
- middle – a list containing everything between the first and last elements; and 
- last – the last element.
  
Using these variables, return a new list in which the first and last elements have exchanged positions. The elements in middle must remain in their original order. Do not modify the input list.

**Function format**: swap_bookends (items)

**CODE:**
```python
print ("Bookend Swap Problem\n")

def swap_bookends (items):
    first, *middle, last = items
    return [last] + middle + [first]

print (swap_bookends([1,2,3,4,5,6]))
print (swap_bookends(["red", "green", "blue"]))
print (swap_bookends ([8,3]))
```

**OUTPUT:**
```python
Bookend Swap Problem

[6, 2, 3, 4, 5, 1]
['blue', 'green', 'red']
[3, 8]
```

The following functions and methods in this code are:
- `print ("Bookend Swap Problem\n")`: This indicates the headline for programmers to distinguish the program easily
> "\n" specifically refers to an escaped new line

- `def swap_bookends (items)`: defining the function swap_bookends to the value of "items"
- `Items`: value used for the function swap_bookends (can be in string or integer format)
- `first, *middle, last = items`: extended sequence in the form of unpacking
  > Sequence unpacking in Python allows you to assign values from a sequence (like a list or tuple) to multiple variables in a single statement. This is particularly useful when dealing with functions that return multiple values. (Sadrach, 2020)
  > - first — gets index zero (0)
  > - middle — combines all intermediate values
  > - last — gets the last index (-1)
- `return [last] + middle + [first]`: returns the value of items in an exchanged position

- `print (swap_bookends([items]))`: prints the output of the defined function
- ---
### **END OF NOTEBOOK**
