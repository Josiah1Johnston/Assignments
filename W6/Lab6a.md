# Lab 6, text parsing
## 1
```python
print("if there is an error please install matplotlib")

#imports used
import string
from collections import Counter
import matplotlib.pyplot as graph

#the input text
text=input("word and cout the charecters of your text:")

char_count=len(text)

words=text.split()

word_count=len(words)

print("Number of words:", word_count)
print("Number of characters:", char_count)

#counts the words
word_freq=Counter(words)

#this whole part is the creation of the graph
graph.bar(word_freq.keys(), word_freq.values())
graph.xticks(rotation=45)
graph.title("Word Frequency Histogram")
graph.xlabel("Words")
graph.ylabel("Frequency")
graph.tight_layout()
graph.show()
```
## 2 
```python
print("if there is an error please install matplotlib")

import string
from collections import Counter
import matplotlib.pyplot as graph


text=input("word and cout the charecters of your text:")

char_count=len(text)

words=text.split()

word_count=len(words)

print("Number of words:", word_count)
print("Number of characters:", char_count)

#dictonary part

word_freq={}

#this is the dictonary storing sequence instead of "counter" in part 1
for word in words:
    if word in word_freq:
        word_freq[word] += 1
    else:
        word_freq[word] = 1

#the same graphing setup
graph.bar(word_freq.keys(), word_freq.values())
graph.xticks(rotation=45)
graph.title("Word Frequency Histogram")
graph.xlabel("Words")
graph.ylabel("Frequency")
graph.tight_layout()
graph.show()
```
## 3 & 4
```python
# part 3

#imports
import re
text=input("emails and phone numbers:")

# re patterns, im not sure exactly why but these are the patterns for phone numbers and emails
email_pattern = r'[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]+'
phone_pattern = r'\b\d{3}[-.]?\d{3}[-.]?\d{4}\b'

# re.findall takes all matches and creates a list
emails = re.findall(email_pattern, text)
phones = re.findall(phone_pattern, text)

print("Emails found:", emails)
print("Phone numbers found:", phones)

# part 4

#creating a empty list
usernames=[]

#this splits the emails at the @ symbol and takes the first half, then edits the usernames list
for email in emails:
  username=email.split("@")[0]
  usernames.append(username)

print("usernames:", usernames)

new_emails = []

#this adds the new adress to the email, "@hotmail.com"
for user in usernames:
    new_emails.append(user + "@hotmail.com")

print("New emails:", new_emails)
```
