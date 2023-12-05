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

4. Find a formula using only the connectives ∧ and ¬ that is equivalent
to P ∨ Q. Justify your answer with a truth table.

     | P   | Q   | P OR Q | ¬(¬P ∧ ¬Q) |
     |-----|-----|--------|------------|
     |  T  |  T  |   T    |     T      |
     |  T  |  F  |   T    |     T      |
     |  F  |  T  |   T    |     T      |
     |  F  |  F  |   F    |     F      |

5. Some mathematicians use the symbol ↓ to mean nor. In other words,
P ↓ Q means “neither P nor Q.”
