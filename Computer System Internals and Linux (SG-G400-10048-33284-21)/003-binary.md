### Binary (Norman Murray)

_2020-10-01 10:00:00 - 2020-10-01 10:50:00_

Binary numbers use a "power of 2", this means that instead of counting up to ten repeatedly (like our own numbers: 8, 9, 10, 11) they count up to two repeatedly (where those "two " numbers they count through are 0 and 1)

Over the next four weeks students will study the following topics:

* This week: Binary to decimal and decimal to binary conversion
* Next week: Adding and multiplication
* The week after: Substraction and division
* The final week: Floating point numbers

Counting in Binary is simple, every time the number on the far right changes from 1 to 0, the number to it's left increases by 1:

```
0
1
10
11
100
101
110
111
```

If we expand the counting above (by adding extra 0s to the left which do nothing) it looks like this:

```
000
001
010
011
100
101
110
111
```

#### Easily converting from binary to decimal

Binary numbers are just powers 2. Decimal numbers are powers of 10 (10 is just 10^1, 100 is just 10^2, 1000 is just 10^3, so on).

Here is a simple map of powers of 2, you will notice that because it is a power of 2, you **just double it each time**:

```
2^0: 1
2^1: 2
2^2: 4
2^3: 8
2^4: 16
```

If you lay these out horizontally (in reverse order), you can easily count:

```
Count to 3:

16    8    4    2    1
0     0    0    1    1
```

To explain this above: 

* Take the number you want to reach (3) and then see the highest number in the list you can subtract from 3
* You can't subtract 16, you can't subtract 8 or 4, because these are all bigger than 3.
* You can subtract 2, so take that away from 3 and you will be left with 1. (that is why there is a 1 under the number 2, we can subtract 2 from 1).
* Then subtract the final 1 and you're left with 0 - you've reached the number you wanted.
* The numbers in the bottom row is the binary representation of the number you wanted.

If you still don't understand this, go over the example below, then re-read the above section. This is hard and needs you to re-wire your brain. Don't worry if it takes you a while to "get" it - that's normal when learning binary for the first time. Just be patient, keep reading it and give your brain time to absorb it.

```
Count to 6:

16    8    4    2    1
0     0    1    1    0

Count to 0:

16    8    4    2    1
0     0    0    0    0

Count to 19:

16    8    4    2    1
1     0    0    1    1
```

_Editor's note: At this point I would suggest picking some small, easy numbers (less than 32) and trying to count up to them in binary. Doing this yourself instead of just reading it will make it much more intuitive._

There is a resource for testing your binary knowledge which coud be useful once you get comfortable with it: [https://www.firstyearmatters.info/cgi-bin/binary.cgi](https://www.firstyearmatters.info/cgi-bin/binary.cgi)
