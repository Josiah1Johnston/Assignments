# this is for lab 2c

1, variable memory usage:

```python
# im using time to clearly see the change in number, idk i thought it was a good idea
import time
var_1 = 10
print(hex(id(var_1)))
time.sleep(1)
var_1 = 100
print(hex(id(var_1)))
```

I got 

0x7ffa0c49a598

and

0x7ffa0c49b0d8

There are two different adresses because python just moves the variable "var_1" to a different object instead of replacig the number.

```python
import time
var_1 = 10
print(hex(id(var_1)))
time.sleep(1)
var_1 = 100
print(hex(id(var_1)))
time.sleep(1)
var_2 = 100
print(hex(id(var_2)))
```

python reused the exsisting memory block for 100 for variable 2 because it was assigned to 100 along with variable 1



2, memory map:

i used the following code

```python
str1 = "Hello"
str2 = "World"
print(hex(id(str1[0])))
print(hex(id(str1[1])))
print(hex(id(str1[2])))
print(hex(id(str1[3])))
print(hex(id(str1[4])))
print(hex(id(str2[0])))
print(hex(id(str2[1])))
print(hex(id(str2[2])))
print(hex(id(str2[3])))
print(hex(id(str2[4])))
```

i got:

0x7ffa0c4aa448 h

0x7ffa0c4aa9b8 e

0x7ffa0c4aab08 l

0x7ffa0c4aab08 l

0x7ffa0c4aab98 o

0x7ffa0c4aa718 w

0x7ffa0c4aab98 o

0x7ffa0c4aac28 r

0x7ffa0c4aab08 l

0x7ffa0c4aa988 d

3, problem solving

dogcat

the dog chases the cat

dogdogdogdog
