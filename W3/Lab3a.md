# Lab 3a
## if statements, and logic blocks

### 1, comparison operators:

```python
for i in range(32, 127):
  print("ascii value", i, "keyboard key", chr(i))
```

The question was a bit confuzing but I got it, i had to use gpt to help walk me through it though

the i is the all the numbers between the range of 32 and 127, which after looking at an ascii table are the ones that are on a keyboard, then i used print and a few different statements in it to show the different ascii numbers and their corresponding key, and chr goes hand in hand ord, ord turns the key to ascii, and chr does the other way around. so what the program gives you is a list of all ascii numbers and their corresponding keys.

### 2, logical operators:

```python
#and functions

print(20>10 and 60>100)
#that should be false
print(10>2 and 13>2)
#that should be true

#or functions

print(30>20 or 40<10)
#that should be true
print(10<2 or 1<0)
#that should be false

#not function
print(not(4>2))
#this should be true but because of not it is false
```

### 3, bitwise logical operators :

im going to explain how your example works, because i dont want to make my own example, it compares the numbers binary, so 1110 and 1011, and if there is one with a 1, the output is going to be one, sothe outcome is 1111, because afer comparing there are no points on either binary numbers where there is a 0, so it all becomes 1, in turn making the binary number 15

### 4, decision statements:

### 5, problem solving: 

#### a,

I am going to do this the only way i know how

```python
number1 = int(input("Enter the first number: "))
number2 = int(input("Enter the second number: "))
number3 = int(input("Enter the third number: "))
number4 = int(input("Enter the fourth number: "))

if(number1 > number2):
    larger_number1 = number1
    smaller_number1 = number2
else:
    larger_number1 = number2
    smaller_number1 = number1
if(number3 > number4):
    larger_number2 = number3
    smaller_number2 = number4
else:
    larger_number2 = number4
    smaller_number2 = number3
if(larger_number1 > larger_number2):
    largest_number = larger_number1
    second_largest_number = larger_number2
else:
    largest_number = larger_number2
    second_largest_number = larger_number1
if(smaller_number1 > smaller_number2):
    third_largest_number = smaller_number1
else:
    third_largest_number = smaller_number2

print("the largest number is", largest_number)
print("the second largest number is", second_largest_number)
print("the third largest number is", third_largest_number)
```

#### b,

way 1

```python
number = int(input("Enter a number: "))
if(number % 2 == 0)
  print(number, "is even")
else:
  print(number, "is odd")
```

way 2

```python
number = int(input("Enter a number: "))
if(number & 1 == 0):
   print(number, "is even")
else:
  print(number, "is odd")
```

#### c,

this calculates the score for you, you give it your score, then your total points.

```python
score = int(input("you got a: "))
total = int(input("out of: "))

percent = score/total*100
if(percent >= 90):
    print(percent, "Work of genuinely superior quality.")
elif(89 >= percent >= 80):
    print(percent, "Passing performance falls approximately in the upper distribution of passing grades.")
elif(79 >= percent >= 71):
    print(percent, "Passing performance falls approximately in the center of the distribution of all passing grades.")
elif(70 >= percent >= 65):
    print(percent, "Passing performance falls approximately in the lower distribution of passing grades.")
elif(65 >= percent):
    print(percent, "Failing performance that does not satisfy the basic requirements of the course and needs to be improved in significant ways.")
```
#### d,

i do not know how to do this

#### e,

```python
number = int(input("Enter a number: "))
if(number & 1 == 0):
   print(number, "is even")
else:
  print(number, "is odd")
```

### 6, code revision

```python
name = input("What's your name? ")
time = int(input("What time is it? "))

# if time is under 12
if (time < 1200):
    print("Hi "+name + ", good morning!")

#if time is under 6
elif (time < 1800):
    print("Hi "+name + ", good afternoon!")

#anything unused, aka after 6 oclock
else:
    print("Hi "+name + ", good evening!")

print("Good Bye")
```

### 7, output verification

it should output :

one

two

because intigers are considered equal to floats, and i fact checked it too.
