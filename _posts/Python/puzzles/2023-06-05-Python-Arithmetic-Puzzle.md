---
title:  "Python Arithmetic Puzzle"
date:   2023-06-05 18:52:00 +0545
categories: [Python]
tags: [Arithmetic Puzzles, Coding challenge]
---

## Operator Challenge:

```python
x = 8 - 2 * 3 + 1
y = (8 - 2) * 3 + 1
z = 8 - (2 * 3 + 1)
print(x, y, z)
```

## Division Challenge:

```python
x = 15 / 4
y = 15 // 4
z = 15 % 4

print(x, y, z)
```


## Mixed Operations:

```python
x = 3 + 2 * 4 - 1 / 2
y = (3 + 2) * (4 - 1) / 2

print(x, y)
```

## Solutions:

### Operator Challenge

```python 
x = 8 - 2 * 3 + 1   # x = 8 - 6 + 1 = 3
y = (8 - 2) * 3 + 1   # y = 6 * 3 + 1 = 19
z = 8 - (2 * 3 + 1)   # z = 8 - (6 + 1) = 8 - 7 = 1

print(x, y, z)   # Output: 3 19 1
```

### Division Challenge
```python
x = 15 / 4   # x = 3.75
y = 15 // 4   # y = 3
z = 15 % 4   # z = 3 (remainder of 15 divided by 4)

print(x, y, z)   # Output: 3.75 3 3
```

### Mixed Operations
```python
x = 3 + 2 * 4 - 1 / 2   # x = 3 + 8 - 0.5 = 10.5
y = (3 + 2) * (4 - 1) / 2   # y = 5 * 3 / 2 = 7.5

print(x, y)   # Output: 10.5 7.5
```
