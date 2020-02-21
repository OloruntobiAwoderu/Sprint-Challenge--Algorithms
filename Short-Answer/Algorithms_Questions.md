# Analysis of Algorithms

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```python
a)  a = 0  # -o(1)
    while (a < n * n * n): # 0(n* 3)
      a = a + n * n # o(1)
```


```
b)  sum = 0   o(1)
    for i in range(n): 0(n)
      j = 1     o(1)
      while j < n: 0(n)
        j *= 2 o(1)
        sum += 1 o(1)
```

```
c)  def bunnyEars(bunnies):
      if bunnies == 0: 
        return 0

      return 2 + bunnyEars(bunnies-1)
```

## Exercise II

Suppose that you have an n-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor f or higher, and doesn't get broken if dropped off a floor less than floor f. Devise a strategy to determine the value of f such that the number of dropped + broken eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode AND give the runtime complexity of your solution.


 n - story buildings
 f - floor number (breakpoint ) if < f, egg doesn't break, if > f, egg breaks
 so the best way, i would go about this is to use a binary search method
 since n is the number of floors, i would divide n // 2 and thn throw an egg from the floor, if the egg breaks,
 I'll divide the same number by 2, else if it doesnt break I'll increment the number by 1, and compare the numbers
