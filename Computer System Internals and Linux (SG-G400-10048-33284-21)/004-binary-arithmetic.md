### Binary Arithmetic (Norman Murray)

_2020-10-06 10:00:00 - 2020-10-06 10:50:00_

To begin the lecture, students connected to a university server using the following command:

```
ssh {username}@leto.cs.salford.ac.uk
```

Only 22 of the students were able to connect due to a configuration issue with the server / network, so the lecture about binary arithmetic continued.

#### Adding 1 at a time

In decimal we are all familiar with adding up:

```
0 + 0 = 0
0 + 1 = 1
1 + 1 = 2
2 + 1 = 3
...
9 + 1 = 10
```

We are used to adding a new number (the 1 in a 10) to the left of a number when we reach a multiple of 10.

In binary we need to re-wire our brains to change when and how we add a new number to the left when we reach a multiple of 2:

```
0 + 0 = 0
0 + 1 = 1
1 + 1 = 10
01 + 1 = 11
...
110 + 1 = 111
111 + 1 = 1000
```

In binary, when we increment (increase) the number to the left by 1, all the numbers to the right of that number return to 0:

```
1011 + 1
1100
 ^ this number incremented and numbers to the right returned to 0

11100111 + 1
11101000
    ^ this number incremented and numbers to the right returned to 0
```

#### Multiplying 

In decimal, whenever we multiple by 10 we add a 0 to the end:

```
15 * 10 = 150
150 * 10 = 1500
32 * 10 = 320
320 * 10 = 3200
```

In binary, we add a 0 to the end when we multiple by 2 instead:

```
00100 * 2 = 001000
101 * 2 = 1010
1010 * 2 = 10100
10100 * 2 = 101000
```

More complex multiplication would be `19 * 6`

In decimal:

```
19 * 6 = 114
```

In binary:

```
19 is:
00010011
```

19 * 6 can be rewritten in to powers of 2 to make it simpler:

```
19 * 6
is the same as:

(19 * 2) + (19 * 4)
```

So you can work this out by:

```
Take 19:

00010011

Multiple it by 2 and store that:

00100110

Multiple that by 2 and store that as well:

01001100
```

Now we have the following numbers:

```
19 * 2 = 00100110
19 * 4 = 01001100
```

And we can add these together tog et our final answer in binary:

```
00100110
+
01001100
=
01110010

01110010 = 114 in decimal
```

#### The next tutorial

Dr Murray gave information regarding command line tools we will cover in our next lecture. These haven't been included in these lecture notes as they aren't relevant to this session.
