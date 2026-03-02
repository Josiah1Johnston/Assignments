# Functions in python
## 1
#### a
```python
CONVERSION_KPL_TO_MPG = 2.35215
CONVERSION_MPG_TO_KPL = 0.425144

while True:

    choice = input("Convert (1) kpl to mpg or (2) mpg to kpl? Enter 1 or 2: ")

    if choice != "1" and choice != "2":
        print("Invalid choice. Please enter 1 or 2.")
        continue

    values = input("Enter value(s) separated by space: ")

    numbers = values.split()

    valid = True

    for num in numbers:
        if not num.replace('.', '', 1).isdigit():
            valid = False
            break

    if not valid:
        print("Invalid input detected. Please enter numbers only.")
        continue

    print("\nConverted values:")

    for num in numbers:
        num = float(num)

        if choice == "1":
            result = num * CONVERSION_KPL_TO_MPG
            print(f"{num} kpl = {result:.2f} mpg")
        else:
            result = num * CONVERSION_MPG_TO_KPL
            print(f"{num} mpg = {result:.2f} kpl")
```
### b:
