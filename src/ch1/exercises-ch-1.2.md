# Chapter 1.2: Truth Tables (Exercises)

1. Make truth tables for the following formulas:
   1. $\lnot{P}\lor{Q}$

        | P | Q | ¬P | ¬P ∨ Q |
        |---|---|----|--------|
        | T | T |  F |   T    |
        | T | F |  F |   F    |
        | F | T |  T |   T    |
        | F | F |  T |   T    |

   2. $(S\lor{G})\land{(¬S\lor{¬G})}$

        | S | G | S ∨ G | ¬S | ¬G | (S ∨ G) ∧ (¬S ∨ ¬G) |
        |---|---|-------|----|----|----------------------|
        | T | T |   T   |  F |  F |         F            |
        | T | F |   T   |  F |  T |         T            |
        | F | T |   T   |  T |  F |         T            |
        | F | F |   F   |  T |  T |         F            |

2. Make truth tables for the following formulas
   1. $\lnot{[P\land{(Q\lor{\lnot{P}})}]}$ is equivalent to $\lnot{(P\land{Q})}$

        | P   | Q   | ¬[P ∧ (Q ∨ ¬P)] |
        |-----|-----|-----------------|
        |  T  |  T  |        F        |
        |  T  |  F  |        T        |
        |  F  |  T  |        T        |
        |  F  |  F  |        T        |

        | P   | Q   | ¬(P ∧ Q) |
        |-----|-----|----------|
        |  T  |  T  |    F     |
        |  T  |  F  |    T     |
        |  F  |  T  |    T     |
        |  F  |  F  |    T     |

        | P   | Q   | ¬[P ∧ (Q ∨ ¬P)] | ¬(P ∧ Q) |
        |-----|-----|-----------------|----------|
        |  T  |  T  |        F        |    F     |
        |  T  |  F  |        T        |    T     |
        |  F  |  T  |        T        |    T     |
        |  F  |  F  |        T        |    T     |

   2. $(P\lor{Q})\land{(\lnot{P}\lor{R})}$

        | P   | Q   | R   | (P ∨ Q) | (¬P) | (¬P ∨ R) | (P ∨ Q) ∧ (¬P ∨ R)  |
        |-----|-----|-----|---------|------|----------|---------------------|
        |  T  |  T  |  T  |    T    |  F   |    T     |         T           |
        |  T  |  T  |  F  |    T    |  F   |    F     |         F           |
        |  T  |  F  |  T  |    T    |  F   |    T     |         T           |
        |  T  |  F  |  F  |    T    |  F   |    F     |         F           |
        |  F  |  T  |  T  |    T    |  T   |    T     |         T           |
        |  F  |  T  |  F  |    T    |  T   |    T     |         T           |
        |  F  |  F  |  T  |    F    |  T   |    T     |         F           |
        |  F  |  F  |  F  |    F    |  T   |    F     |         F           |

3. In this exercise we will use the symbol + to mean exclusive or. In other words, P + Q means “P or Q, but not both.”

    1. $P + Q$

        | P   | Q   | P XOR Q |
        |-----|-----|---------|
        |  T  |  T  |    F    |
        |  T  |  F  |    T    |
        |  F  |  T  |    T    |
        |  F  |  F  |    F    |

    2. Find a formula using only the connectives ∧, ∨, and ¬ that is equivalent to P + Q. Justify your answer with a truth table

        | P   | Q   | P XOR Q | (P ∨ Q) ∧ ¬(P ∧ Q) |
        |-----|-----|---------|---------------------|
        |  T  |  T  |    F    |         F           |
        |  T  |  F  |    T    |         T           |
        |  F  |  T  |    T    |         T           |
        |  F  |  F  |    F    |         F           |

        $$
        \begin{aligned}
          P + Q = \text{P XOR Q} \\
          \text{This is equivalent to} \\\\
          (P\,\lor\,Q)\,\land\,\lnot\,(P\,\land\,Q)
        \end{aligned}
        $$

4. Find a formula using only the connectives ∧ and ¬ that is equivalent to P ∨ Q. Justify your answer with a truth table.

     | P   | Q   | P OR Q | ¬(¬P ∧ ¬Q) |
     |-----|-----|--------|------------|
     |  T  |  T  |   T    |     T      |
     |  T  |  F  |   T    |     T      |
     |  F  |  T  |   T    |     T      |
     |  F  |  F  |   F    |     F      |

5. Some mathematicians use the symbol ↓ to mean nor. In other words, P ↓ Q means "neither P nor Q."

     1. Make a truth table for P ↓ Q.

          | P   | Q   | ¬P ∧ ¬Q (Neither P nor Q) |
          |-----|-----|---------------------------|
          |  T  |  T  |            F              |
          |  T  |  F  |            F              |
          |  F  |  T  |            F              |
          |  F  |  F  |            T              |

     2. Find a formula using only the connectives ∧, ∨, and ¬ that is equivalent to P ↓ Q
        1. $(\lnot{P}\land{\lnot{Q}})$
        2. $\lnot{(P\lor{Q})}$.

     3. Find formulas using only the connective ↓ that are equivalent to ¬P, P ∨ Q, and P ∧ Q.

          $$
          \begin{aligned}
               \lnot{P} = (P\downarrow{P}) \\
               P\lor{Q} = (P\downarrow{Q})\downarrow{(P\downarrow{Q})} \\
               P\land{Q} = (P\downarrow{P})\downarrow{(Q\downarrow{Q})}
          \end{aligned}
          $$

6. Some mathematicians write P | Q to mean "P and Q are not both true." (This  connective is called *nand*, and is used in the study of circuits in computer science.)

   1. Make a truth table for P | Q.

     | P   | Q   | ¬(P ∧ Q) (P and Q are not both true) |
     |-----|-----|--------------------------------------|
     |  T  |  T  |                   F                  |
     |  T  |  F  |                   T                  |
     |  F  |  T  |                   T                  |
     |  F  |  F  |                   T                  |

   2. Find a formula using only the connectives ∧, ∨, and ¬ that is equivalent to P | Q

      1. $\lnot{(P\land{Q})}$
      2. $\lnot{P}\lor{\lnot{Q}}$

   3. Find formulas using only the connective | that are equivalent to ¬P, P ∨ Q, and P ∧ Q.

      1. $\lnot{P} = P\,|\,P$
      2. $P\lor{Q} = (P\,|\,P)\,|\,(Q\,|\,Q)$
      3. $P\land{Q} = (P\,|\,Q)\,|\,(P\,|\,Q)$

7. Use truth tables to determine whether or not the arguments in exercise 9 of Section 1.1 are valid.
   1. Jane and Pete won’t both win the math prize. Pete will win either the math prize or the chemistry prize. Jane will win the math prize. Therefore, Pete will win the chemistry prize

        ```text
          Premises
            - Jane and Pete won’t both win the math prize
            - Pete will win either the math prize or the chemistry prize
            - Jane will win the math prize

          Conclusion
            - Pete will win the chemistry prize

          Logical Form
            P = Pete will win the Math prize
            J = Jane will win the Math prize
            C = Pete will win the Chemistry prize

            not (J and P)
            P or C
            J
            Therefore, C
        ```

        The argument is valid

        | P | J | C | ¬(P ∧ J) | P ∨ C | J | Conclusion: C |
        |---|---|---|----------|-------|---|---------------|
        | T | T | T | F        | T     | T | T             |
        | T | T | F | F        | T     | T | F             |
        | T | F | T | T        | T     | F | T             |
        | T | F | F | T        | T     | F | F             |
        | F | T | T | T        | T     | T | T             |
        | F | T | F | T        | F     | T | F             |
        | F | F | T | T        | T     | F | T             |
        | F | F | F | T        | F     | F | F             |

   2. The main course will be either beef or fish. The vegetable will be either peas or corn. We will not have both fish as a main course and corn as a vegetable. Therefore, we will not have both beef as a main course and peas as a vegetable.

        ```text
          Premises
            - The main course will be either beef or fish
            - The vegetable will be either peas or corn
            - We will not have both fish as a main course and corn as a vegetable

          Conclusion
            - We will not have both beef as a main course and peas as a vegetable

          Logical Form
            B = The main course will be beef
            F = The main course will be fish
            P = The vegetable will be peas
            C = The vegetable will be corn

            B or F
            P or C
            not (F and C)
            Therefore, not (B and P)
        ```

        The argument is invalid

        | B | F | P | C | B ∨ F | P ∨ C | ¬(F ∧ C) | Conclusion: ¬(B ∧ P) |
        |---|---|---|---|-------|-------|----------|----------------------|
        | T | T | T | T | T     | T     | F        | F                    |
        | T | T | T | F | T     | T     | T        | F                    |
        | T | T | F | T | T     | F     | F        | T                    |
        | T | T | F | F | T     | F     | T        | T                    |
        | T | F | T | T | T     | T     | T        | F                    |
        | T | F | T | F | T     | T     | T        | F                    |
        | T | F | F | T | T     | F     | T        | T                    |
        | T | F | F | F | T     | F     | T        | T                    |
        | F | T | T | T | T     | T     | F        | F                    |
        | F | T | T | F | T     | T     | T        | F                    |
        | F | T | F | T | T     | F     | F        | T                    |
        | F | T | F | F | T     | F     | T        | T                    |
        | F | F | T | T | F     | T     | T        | F                    |
        | F | F | T | F | F     | T     | T        | F                    |
        | F | F | F | T | F     | F     | T        | T                    |
        | F | F | F | F | F     | F     | T        | T                    |

   3. Either John or Bill is telling the truth. Either Sam or Bill is lying. Therefore, either John is telling the truth or Sam is lying.

        ```text
          Premises
            - Either John or Bill is telling the truth
            - Either Sam or Bill is lying

          Conclusion
            - Either John is telling the truth or Sam is lying

          Logical Form
            J = John is telling the truth
            B = Bill is telling the truth
            S = Sam is telling the truth

          J or B
          not S or not B
          Therefore, J or not S
        ```

        The argument is valid
