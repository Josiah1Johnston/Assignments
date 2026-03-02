#Lab 4b, dictonaries in python
## 1
### a:
```python
my_dict = {"name": "josiah", "age": "16", "city": "san diego", "color": "red", "grade": "11", "job: "none", "car": "none", "food": "pizza", "college": "yes", "height": "6ft"}
```
### b:
```python
my_user_dict = {}

while True:
    username = input("whats your name? ")
    age = input("whats your age? ")

    my_user_dict["name"] = username
    my_user_dict["age"] = age

    print(my_user_dict)

    choice = input("Do you want to continue (y/n)? ").strip().upper()

    if choice == "n":
        print("Bye")
        break
    elif choice == "y":
        continue
    else:
        print("Error in input")
        break
```
### c & d:
```python
tuple = [('Name', 'Sarah Connor'),
 ('Date of birth', '1 Jan 1980'),
 ('Address', '1000 Black Mountain Drive', 92126),
 ('Name', 'Jim Hawkins')]

my_dict = {}
i = 0
while i < len(tuple):

    pair = tuple[i]

    if len(pair) != 2:
        print("wrond key - value pair found:", pair)
        print("A pair must contain 2 elements.")

        key = input("Enter a correct key: ")
        value = input("Enter a correct value: ")

        my_dict[key] = value

    else:
        key = pair[0]
        value = pair[1]

        if key in my_dict:
            print("Duplicate key found:", key)
            new_key = input("enter new key: ")
            my_dict[new_key] = value
        else:
            my_dict[key] = value

    i += 1

print("\nFinal dictionary:")
print(my_dict)
```
#### e:
```python
text = """The tiger (Panthera tigris) is a large cat and a member of the genus Panthera native to Asia. It has a powerful, muscular body with a large head and paws, a long tail and orange fur with black, mostly vertical stripes. It is traditionally classified into nine recent subspecies, though some recognise only two subspecies, mainland Asian tigers and the island tigers of the Sunda Islands."""

words = text.split()

word_count = {}

for word in words:
    if word in word_count:
        word_count[word] += 1
    else:
        word_count[word] = 1

print(word_count)
```

## 2, troubleshooting

#### a & b:
copy troubleshoot
```python
d_orig = {123: "Coconut"}
d_copy = d_orig.copy()

# you need .copy() to make an actual copy of something, setting it as different, wheras if you just do d_orig = d_copy it sets them as equal to one another

d_copy[123] = "apple"
print(d_orig) 
print(d_copy)
```
#### c:
```python
my_dict = {}
my_key = [1, 2, 3,]
my_dict[my_key] = "hello"
#this causes the error because it is a list, something that can be changed, an muteable, aka it cannot be hashed because the storage lovation can change, so it will cause an error
```
## challenges

i feel like for almost everything on this assignment i had to learn something new that wasnt in the required stuff to complete this assighnment.
