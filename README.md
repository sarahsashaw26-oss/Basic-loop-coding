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
