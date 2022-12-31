# Divide and Conquer: Karatsuba Multiplication

I've been diving into data structures and algorithms lately and came across a rather interesting problem/solution, one which is rather straight forward, *The Karatsuba algorithm* :

The *Karatsuba algorithm* is a fast multiplication algorithm. It was discovered by [Anatoly Karatsuba](https://en.wikipedia.org/wiki/Anatoly_Karatsuba) in 1960 and published in 1962. It reduces the multiplication of two n-digit numbers to at most  O(nlog2^3) ~ O(n^1.59) single-digit multiplications in general (and exactly n^log2^3 when n is a power of 2). It is therefore asymptotically faster than the traditional algorithm, which requires n^2 single-digit products. For example, the Karatsuba algorithm requires 310 = 59,049 single-digit multiplications to multiply two 1024-digit numbers (n = 1024 = 2^10), whereas the traditional algorithm requires (2^10)^2 = 1,048,576 (a speedup of 17.75 times).

#### Here is a python implementation of the karatsuba multiplication algorithm. It is used here to calculate the product of two 64-digit numbers
%[https://gist.github.com/LPMatrix/3b9b75b7f943ce2aabeaf7b3a62ad1e8]
