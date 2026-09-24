# Output with `print()`

Python uses the `print()` function to display information on the screen.

```python
print("Hello, world!")
```

Output:
```bash
Hello, world!
```

## Printing Numbers

```python
print(10)
print(3.14)
```

You can also perform calculations inside `print()`:
```python
print(10+5)
```

Output:
```bash
15
```

## Printing multiple things

```python
name = "John"
age = 20

print(name, age)
```

Output:
```bash
John 20
```

# Getting input with `input()`

The `input()` function allows the user to enter information.

```python
name = input("What is your name? ")

print(name)
```

If the user enters:
```bash
sarah
```

The program displays:
```bash
sarah
```

>[!Note]
> The important idea is:
> `input()` pauses the program and waits for the user to type something.

**Example**:
```python
age = input("What is your age? ")

print(age)
```

However, there is an important detail

>[!Warning]
>Everything received from `input()` is intitialy a string

```python
print(type(age))
```

If the user enters `20`, Python still consider it:

```bash
<class 'str'>
```

# Converting user input

Suppose we want the user to enter a number and perform mathematics with it.

This won't work as expected:

```python
age = input("Enter your age: ")

print(age + 1)
```

Why? Because `age` is a string.

We can convert it to an integer using `int()`

```python
age = int(input("Enter your age: "))

print(age + 1)
```

If the user enters:
```bash
20
```

Output:
```bash
21
```

## Converting to decimal
Use `float()`:
```python
price = float(input("Enter the price: "))

print(price)
```

**Example**:
```bash
Enter the price: 12.50
```

Python stores `12.50` as a `float`

## Common conversions

| Function  | Converts to    | Example         |
| --------- | -------------- | --------------- |
| `str()`   | String         | `str(25)`       |
| `int()`   | Integer        | `int("25")`     |
| `float()` | Decimal number | `float("25.5")` |

# Variables + Input + Output

Now we can combine everything.

```python
name = input("What is your name? ")
age = int(input("What is your age? "))

print("Name:", name)
print("Age:", age)
```

Output:
```bash
What is your name? Maria
What is your age? 22
Name: Maria
Age: 22
```

# Formatting output with f-strings

A cleaner way to display information is an **f-string**

```python
name = input("What is your name? ")
age = int(input("What is your age? "))

print(f"Hello {name}!")
print(f"You are {age} years old.")
```

If the user enters `David` and `25`

```bash
Hello David!
You are 25 years old.
```

You can also perform calculations inside an f-string:

```python
age = int(input("How old are you? "))
print(f"Next year you will be {age + 1}.")
```

# Multiple inputs
python allows you to collect several pieces of information

```python
first_name = input("First name: ")
last_name = input("Last name: ")
city = input("City: ")

print(f"Name: {first_name} {last_name}")
print(f"City: {city}")
```

You can also calculate values:
```python
number1 = int(input("Enter the first number: "))
number2 = int(input("Enter the second number: "))

print(f"Sum: {number1 + number2}")
print(f"Differnce: {nubmer1 - number2}")
print(f"Product: {number1 * number2}")
```

---