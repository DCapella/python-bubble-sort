# Python Bubble Sort

#### [HackerRank](www.hackerrank.com)

> Task:
> Given an array, a, of size n distinct elements,
> sort the array in ascending order using the Bubble Sort algorithm above.
> Once sorted, print the following 3 lines:
> Array is sorted in numSwaps swaps. 
> where numSwaps is the number of swaps that took place.
> First Element: firstElement 
> where firstElement is the first element in the sorted array.
> Last Element: lastElement 
> where lastElement is the last element in the sorted array.

## Pre-Work

* Let's get an example set up.

**index, array/list, and length of array/list (3)**

i: 0, 1, 2

y: 3, 2, 1

n = len(y)

**Swap w/numbers as index**

if 0 > 1:
  swap(0, 1)
  count += 1
  
if 1 > 2:
  swap(1, 2)
  count += 1
  
**Stop there because index of 2 will be last number which means (n-1)**

**Since that will only do one number we will need to do that (n-1) times because we don't need to swap the last number,
it should be sorted by then.**

## Code

* Declare necessary variables

```python
def bubble_swap(a):
  count = 0
  threshold = len(a) - 1
```

* Set up the two loops both at (n-1) coincidentally

```python
...
for _ in range(threshold):
  for i in range(threshold):
```

* Check, swap, count

```python
...
if a[i] > a[i + 1]:
  a[i], a[i + 1] = a[i + 1], a[i]
  count += 1
```

* Printing or displaying

```python
print(f'Array is sorted in {count} swaps.')
print(f'First Element: {a[0]}')
print(f'Last Element: {a[-1]}')
```

* Finished!

## Solution Code

```python
#!/bin/python3

import sys

n = int(input().strip())
a = list(map(int, input().strip().split(' ')))
# Write Your Code Here

def bubble_sort(a):
  """
  Displays how many swaps it takes; in addition, the first and
  last element for reference.

  Parameters
  ----------
  a : list
    List of numbers, n is not needed.

  Returns
  -------
  _ : None
    It displays the content so it does not return anything.
  """
  count = 0
  threshold = len(a) - 1

  for _ in range(threshold):
    for i in range(threshold):
      if a[i] > a[i + 1]:
        a[i], a[i + 1] = a[i + 1], a[i]
        count += 1

  print(f'Array is sorted in {count} swaps.')
  print(f'First Element: {a[0]}')
  print(f'Last Element: {a[-1]}')

bubble_sort(a)
```

## Conclusion

This was a very fun problem to go through. Exciting stuff.
