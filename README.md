# Basic-loop-coding
# range(stop) — 0 to stop-1
for i in range(5):
    print(i)          # 0 1 2 3 4

# range(start, stop)
for i in range(2, 6):
    print(i)          # 2 3 4 5

# range(start, stop, step)
for i in range(10, 0, -2):
    print(i)          # 10 8 6 4 2

    # List
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)

# String (iterate characters)
for ch in "Python":
    print(ch)

# Tuple
for x in (10, 20, 30):
    print(x)

# Dictionary
person = {"name": "Alice", "age": 30, "city": "Paris"}

for key in person:                     # keys by default
    print(key)

for value in person.values():          # values
    print(value)

for key, value in person.items():      # key-value pairs
    print(key, "=", value)

# enumerate: get index + value
colors = ["red", "green", "blue"]
for index, color in enumerate(colors):
    print(index, color)

# Start index at 1
for i, color in enumerate(colors, start=1):
    print(i, color)

# zip: iterate two (or more) sequences in parallel
names = ["Alice", "Bob", "Carol"]
scores = [85, 92, 78]
for name, score in zip(names, scores):
    print(f"{name}: {score}")

    # Basic while
count = 0
while count < 5:
    print(count)
    count += 1

# while with user-like condition
total = 0
n = 10
while n > 0:
    total += n
    n -= 1
print("Sum:", total)     # 55

# while True (infinite loop, exits with break)
secret = "python"
while True:
    guess = input("Guess the word: ")
    if guess == secret:
        print("Correct!")
        break

        # break — exit the loop early
for i in range(10):
    if i == 5:
        break
    print(i)             # 0 1 2 3 4

# continue — skip to next iteration
for i in range(5):
    if i % 2 == 0:
        continue
    print(i)             # 1 3

# for/else — else runs if loop finished WITHOUT break
for n in [2, 4, 6, 8]:
    if n % 2 != 0:
        print("Found odd:", n)
        break
else:
    print("All numbers are even")   # this runs

    # Multiplication table
for i in range(1, 4):
    for j in range(1, 4):
        print(f"{i}*{j}={i*j}", end="  ")
    print()   # newline after each row

1*1=1  1*2=2  1*3=3
2*1=2  2*2=4  2*3=6
3*1=3  3*2=6  3*3=9
# Sum / product
numbers = [1, 2, 3, 4, 5]
total = 0
for n in numbers:
    total += n
print("Sum:", total)          # 15

# Find max
maximum = numbers[0]
for n in numbers:
    if n > maximum:
        maximum = n
print("Max:", maximum)        # 5

# Count matches
words = ["apple", "banana", "apple", "cherry"]
count = 0
for w in words:
    if w == "apple":
        count += 1
print("Apples:", count)       # 2

# Build a new list
squares = []
for x in range(1, 6):
    squares.append(x * x)
print(squares)                # [1, 4, 9, 16, 25]

# List comprehension
squares = [x * x for x in range(1, 6)]        # [1, 4, 9, 16, 25]

# With a condition
evens = [x for x in range(10) if x % 2 == 0]  # [0, 2, 4, 6, 8]

# Dict comprehension
lengths = {w: len(w) for w in ["hi", "hello", "hey"]}
# {'hi': 2, 'hello': 5, 'hey': 3}

# Set comprehension
unique = {x % 3 for x in range(10)}           # {0, 1, 2}

for x in reversed([1, 2, 3]):
    print(x)          # 3 2 1

for name in sorted(["Charlie", "Alice", "Bob"]):
    print(name)       # Alice Bob Charlie

    # DON'T do this (skips elements)
nums = [1, 2, 3, 4]
for n in nums:
    if n % 2 == 0:
        nums.remove(n)    # unreliable!

# DO this instead — iterate over a copy, or build a new list
nums = [1, 2, 3, 4]
nums = [n for n in nums if n % 2 != 0]   # [1, 3]
