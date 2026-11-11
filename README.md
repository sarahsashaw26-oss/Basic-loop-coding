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
