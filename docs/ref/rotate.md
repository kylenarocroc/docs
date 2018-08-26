# `rotate`



_Shift the items of a list to the left or right_

Syntax: `x rotate y`, `rotate[x;y]` 

Where 

-   `x` is an integer atom
-   `y` is a list

returns `y` rotated by `x` items.
Rotation is to the ‘left’ for positive `x`, to the ‘right’ for negative `x`.

```q
q)2 rotate 2 3 5 7 11    / rotate a list
5 7 11 2 3
q)-2 rotate 2 3 5 7 11
7 11 2 3 5
q)t:([]a:1 2 3;b:"xyz")
q)1 rotate t             / rotate a table
a b
---
2 y
3 z
1 x
q)0 1 -1 rotate' 3 4#til 12
0  1 2 3
5  6 7 4
11 8 9 10
```

`rotate` is a uniform function. 

<i class="far fa-hand-point-right"></i> [`reverse`](reverse.md)