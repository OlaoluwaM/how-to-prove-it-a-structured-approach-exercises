# Exercises

1. Question 1
   1. Factor $215 − 1 = 32,767$ into a product of two smaller positive integers.

      $$
      \begin{aligned}
        n = 15 \\
        2^n - 1 = 2^15 - 1 = 32,767 \\
        15 = 5 * 3 \\\\

        a = 5, \space b = 3 \\\\

        x = 2^b - 1 = \\\\
        y = 1 + 2^b + 2^b + ... + 2^{(a - 1)b} \\\\

        x = 2^3 - 1 = 7\newline
        y = 1 + 2^{3} + 2^{6} + 2^{9} + 2^{12} = 4681 \\\\

        {\boldsymbol{xy = 7 * 4681 = {\bold 32,767}}}
      \end{aligned}
      $$

   2. Find an integer $x$ such that $1 < x < (2^32,767) − 1$ and $2^32,767 − 1$ is divisible by $x$.

      $$
      \begin{aligned}
        2^32767 - 1 = ... \\
        n = 32,767 \\\\

        a = 4681, \space b = 7 \\\\

        x = 2^b - 1 \\
        {\boldsymbol{x = 2^7 - 1 = 128}}
      \end{aligned}
      $$

2. Make some conjectures about the values of $n$ for which $3n − 1$ is prime or the values of $n$ for which $3n − 2n$ is prime

    | **n** | **is n Prime** | **3^n -1** | **is 3^n -1 prime** |
    |-------|----------------|------------|---------------------|
    | 2     | yes            | 8          | no                  |
    | 3     | yes            | 26         | no                  |
    | 4     | no             | 80         | no                  |
    | 5     | yes            | 242        | no                  |
    | 6     | no             | 728        | no                  |
    | 7     | yes            | 2186       | no                  |
    | 8     | no             | 6560       | no                  |
    | 9     | no             | 19682      | no                  |
    | 10    | no             | 59048      | no                  |

    **Conjecture 1:** Suppose $n$ is an integer greater than $1$ and $n$ is prime. Then $3^n - 1$ is not prime

    **Conjecture 2:** Suppose $n$ is an integer greater than $1$ and $n$ is not prime. Then $3^n - 1$ is not prime

3. The proof of **Theorem 3** gives a method for finding a prime number different from any in a given list of prime numbers.
   1. Use this method to find a prime different from 2, 3, 5, and 7.

      $$
      \begin{align*}
        primes = 2,3,5,7 \\
        P = 2*3*5*7 + 1 = 211 \\
        {\boldsymbol{P = 211}}
      \end{align*}
      $$

   2. Use this method to find a prime different from 2, 5, and 11.

      $$
      \begin{aligned}
        primes = 2,5,11 \\
        P = 2*5*11 + 1 = 111 \\
        {\boldsymbol{P = 111}}
      \end{aligned}
      $$

4. Find five consecutive integers that are not prime

    $[5042,5043,5044,5045,5046]$

    ```haskell
    factorial :: Integer -> Integer
    factorial 0 = 1
    factorial 1 = 1
    factorial 2 = 2
    factorial n = n * (factorial $ n - 1)

    isPrime :: Integer -> Bool
    isPrime k = length [ x | x <- [2..k], k `mod` x == 0] == 1

    main :: IO ()
    main = do
      let x = (factorial $ 6 + 1) + 2
      let xs = take 5 $ enumFrom x
      print $ isPrime <$> xs
      print xs
    ```

5. Use the table in Figure 1.1 and the discussion on p.5 to find two more
perfect numbers.

    It is proven that, if $2^n - 1$ is prime, then $2^{n - 1}(2^n - 1)$ is perfect. Thus, to find other perfect numbers, we must find values for $n$ such that $2^n - 1$ is prime

    $$
    \begin{aligned}
      n = 5 \\
      2^5 - 1 = 31 \\
      2^{4}(31) = \boldsymbol{496} \\\\

      n = 7 \\
      2^7 - 1 = 127 \\
      2^{6}{127} = \boldsymbol{8128}
    \end{aligned}
    $$

6. The sequence $3, 5, 7$ is a list of three prime numbers such that each pair of adjacent numbers in the list differ by two. Are there any more such “triplet primes”?

    No because, as noted in the text, the occurrence of primes thins out as we look at larger numbers. Meaning, as we look at larger numbers, the gap between any two primes begins to widen. Hence, there is only one of such sequence of prime numbers

    Evidence of this can be found using the proof for theorem 4. This sequence is possible only when we set $n$ to $0$. When $n$ is set to anything greater, the gap between primes starts to widen as well

7. A pair of distinct positive integers (m, n) is called amicable if the sum of all positive integers smaller than n that divide n is m, and the sum of all positive integers smaller than m that divide m is n. Show that $(220, 284)$ is amicable.

    ```haskell
    areAmicable :: (Integer, Integer) -> Bool
    areAmicable (m, n) = isNAmicable && isMAmicable
     where
      isNAmicable = calc n == m
      isMAmicable = calc m == n

    calc :: Integer -> Integer
    calc v = sum $ [x | x <- [1..(v - 1)], (mod v) x == 0]

    main :: IO ()
    main = do
      print $ areAmicable (220, 284) -- True
    ```
