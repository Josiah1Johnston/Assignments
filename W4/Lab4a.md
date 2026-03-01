# Touples Lab
 ### part 1
 #### a:

 ```python
a = input("value 1: ")
b = input("value 2: ")
c = input("value 3: ")
d = input("value 4: ")
my_tuple = (a,b,c,d,e,)
print(my_tuple)
```
#### b:
you could assign a single element in a touple by typing your element, and following it with a comma, and it usually is in parenthases, with the sole exception of it being a lone element, where it doesent need the parenthases.

```python
a = input("your numeric input: ")
my_touple = (a, 2, 4 ,8)
print(my_touple)
```
#### c:
```python
my_tuple = (1,2,3,4,3,2,1,2,3,5,4,3,2,1)

for num in set(my_tuple):
  print(num, ":", my_tuple.count(num))
```
#### d:

the code below should print the key numbers and how many of those numbers there are in both tuple 1 and tuple 2, tuple 2 should have twice the amount of the numbers in the values as tuple 1

```python
my_tuple = (1,2,3,4,3,2,1,2,3,5,4,3,2,1)

print("my tuple")

for num in set(my_tuple):
  print(num, ":", my_tuple.count(num))

my_tuple2 = my_tuple + my_tuple

print("my tuple 2")

for num in set(my_tuple2):
  print(num, ":", my_tuple2.count(num))
```
#### e:

the code:
```python
x = (1,2,3,4)
x.append(1)
x[1] = "hello"
del x[2]
```
is not legal for the tuple because append edits a list after its creation, wheras tuples cannot be changed after their creation, so it would result in an error.

### part 2
#### a
in the code
```python
(one, two, three, four) =  (1, 2, 3, 4)
```
each variable, one two three or four, is assigned an integer, 1 2 3 and 4
#### b & c
using the code, 
```
x = (1, 2, 3, 4)
a, b, *c = x
a, b, c
```
the result of
```python
a, *b, c = x
```
will be 
```python
(1,[2,3],4)
```
### part 3

memory adresses are assigned to tuples the same way they are assigned to lists, they will reuse an exsisting adress if there is one with the same value that is trying to be stored

this is what it would kind of look like for the code 
```python
my_x = [100,200,300,400]
my_y = (200,300,400,500)
```

| Index | my_x | my_y |
| ----- | ---- | ---- |
| 0     | 100  | -    |
| 1     | 200  | 200  |
| 2     | 300  | 300  |
| 3     | 400  | 400  |
| 4     | -    | 500  |

because my_y has no 100 value, and my_x has no 500 value, they would use different adresses for them, but would use the same adress for all the values they have in common

### challenges

the only hard part was doing 1c, but other than that this was good!
