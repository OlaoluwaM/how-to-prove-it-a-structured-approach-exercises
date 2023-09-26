# Chapter 1: Sentential Logic (Exercises)

## 1.1 Deductive Reasoning

1. Analyze the logical forms of the following statements:
   1. We’ll have either a reading assignment or homework problems, but
we won’t have both homework problems and a test.

        $$
        \begin{aligned}
          R = \text{You will have a reading assignment} \\
          H = \text{You will be given homework problems} \\
          T = \text{You will be given a test} \\\\

          \text{We know 'but' corresponds to } \land \\
           \text{Therefore, the logical form of the above statement becomes} \\\\

          (R\,\lor\,H)\,\land\,\lnot\,(H\,\land\,T) \\
        \end{aligned}
        $$

   2. You won’t go skiing, or you will and there won’t be any snow.

        $$
        \begin{aligned}
          SK = \text{You will go skiing} \\
          SN = \text{There will be snow} \\\\

          \text{Translating the above then becomes}  \\\\

          \lnot\,SK\,\lor\,(SK\,\land\,\lnot\,SN)
        \end{aligned}
        $$

   3. $\sqrt{7}\,\leq\,2$

        $$
          \begin{aligned}
            \text{The above translates, in English to, "the } \sqrt{7} \text{ is not less than or equal to 2"} \\\\

            L2 = \sqrt{7} < 2 \\
            E2 = \sqrt{7} = 2 \\\\

            \text{With the above defined, we get the following statement} \\\\

            \lnot\,(L2\,\lor\,E2)
          \end{aligned}
        $$

2. Analyze the logical forms of the following statements:

    1. Either John and Bill are both telling the truth, or neither of them is.

        $$
        \begin{aligned}
          J = \text{John is telling the truth} \\
          B  = \text{Bill is telling the truth} \\\\

          \text{Therefore, the above statement can be translated to} \\\\

          (J\,\land\,B)\,\lor\,\lnot\,(J\,\land\,B)
        \end{aligned}
        $$

    2. I’ll have either fish or chicken, but I won’t have both fish and mashed potatoes.

        $$
        \begin{aligned}
          F = \text{I'll have fish} \\
          C  = \text{I'll have chicken} \\
          MP = \text{I'll have mashed potatoes} \\\\

          \text{Therefore, the above statement can be translated to} \\\\

          (F\,\lor\,C)\,\land\,\lnot\,(F\,\land\,MP)
        \end{aligned}
        $$

    3. 3 is a common divisor of 6, 9, and 15.

        $$
        \begin{aligned}
          S = \text{3 is a common divisor of 6} \\
          N = \text{3 is a common divisor of 9} \\
          FF  = \text{3 is a common divisor of 15} \\\\

          \text{Therefore, the above statement can be translated to} \\\\

          S\,\land\,N\,\land\,FF
        \end{aligned}
        $$

3. Analyze the logical forms of the following statements:

    1. Alice and Bob are not both in the room.

        $$
        \begin{aligned}
          A = \text{Alice is in the room} \\
          B = \text{Bob is in the room} \\\\

          \text{The statement implies that either one of them is in the room, but never both.} \\
          \text{However, it is also possible for neither of them to be in the room as well} \\
          \text{Therefore, the above statement can be translated to the following} \\\\

          \lnot\,(A\,\land\,B) \\\\

          \text{Alternatively, we could say}\\\\

          NA = \text{Alice is not in the room} \\
          NB = \text{Bob is not in the room} \\\\

          \text{Thus} \\\\

          NA\,\lor\,NB
        \end{aligned}
        $$

    2. Alice and Bob are both not in the room.

        $$
        \begin{aligned}
          \text{The above statement, can be rewritten (for clarity) as "Neither Alice nor Bob is in the room"} \\\\

          A = \text{Alice is in the room} \\
          B = \text{Bob is in the room} \\\\

          \text{Therefore, the above statement can be translated to} \\\\

          \lnot\,A\,\land\,\lnot\,B

          \text{The above expression can be restated using DeMorgan's Law} \\\\

          \lnot\,(A\,\lor\,B)
        \end{aligned}
        $$

    3. Either Alice or Bob is not in the room.

        $$
        \begin{aligned}
          A = \text{Alice is in the room} \\
          B = \text{Bob is in the room} \\\\

          \text{Therefore, the above statement can be translated to} \\\\

          \lnot\,A\,\lor\,\lnot\,B \\\\

          \text{The above expression can be restated using DeMorgan's Law} \\\\

          \lnot\,(A\,\land\,B)
        \end{aligned}
        $$

    4. Neither Alice nor Bob is in the room.

        $$
        \begin{aligned}
          A = \text{Alice is in the room} \\
          B = \text{Bob is in the room} \\\\

          \text{Therefore, the above statement can be translated to} \\\\

          \lnot\,A\,\land\,\lnot\,B \\\\

          \text{The above expression can be simplified using DeMorgan's Law} \\\\

          \lnot\,(A\,\lor\,B)
        \end{aligned}
        $$

4. Analyze the logical forms of the following statements
   1. Either both Ralph and Ed are tall, or both of them are handsome

        $$
        \begin{aligned}
          RT = \text{Ralph is tall} \\
          ET = \text{Ed is tall} \\
          RH = \text{Ralph is handsome} \\
          EH = \text{Ed is handsome} \\\\

          \text{Therefore, the above statement can be translated to} \\\\

          (RT\,\land\,ET)\,\lor\,(RH\,\land\,EH)
        \end{aligned}
        $$

   2. Both Ralph and Ed are either tall or handsome.

        $$
        \begin{aligned}
          RT = \text{Ralph is tall} \\
          ET = \text{Ed is tall} \\
          RH = \text{Ralph is handsome} \\
          EH = \text{Ed is handsome} \\\\

          \text{Therefore, the above statement can be translated to} \\\\

          (RT\,\lor\,RH)\,\land\,(EH\,\lor\,ET)
        \end{aligned}
        $$

   3. Both Ralph and Ed are neither tall nor handsome.

        $$
        \begin{aligned}
          RT = \text{Ralph is tall} \\
          ET = \text{Ed is tall} \\
          RH = \text{Ralph is handsome} \\
          EH = \text{Ed is handsome} \\\\

          \text{Therefore, the above statement can be translated to} \\\\

          (\lnot\,RT\,\lor\,\lnot\,RH)\,\land\,(\lnot\,EH\,\lor\,\lnot\,ET) \\\\

          \text{The above expression can be restated using DeMorgan's Law} \\\\

          \lnot\,(RT\,\lor\,RH)\,\land\,\lnot\,(EH\,\lor\,ET)
        \end{aligned}
        $$

   4. Neither Ralph nor Ed is both tall and handsome.

        $$
        \begin{aligned}
          RT = \text{Ralph is tall} \\
          ET = \text{Ed is tall} \\
          RH = \text{Ralph is handsome} \\
          EH = \text{Ed is handsome} \\\\

          \text{Therefore, the above statement can be translated to} \\\\

          \lnot\,(RT\,\land\,RH)\,\land\,\lnot\,(ET\,\land\,EH)
        \end{aligned}
        $$

5. Which of the following expressions are well-formed formulas?

    1. $¬(¬P ∨ ¬¬R)$ - This is well-formed, can be rewritten as $P ∨ ¬R$
    2. $¬(P, Q, ∧ R)$ - This is not well-formed as it contains a comma which is not a part of the lexicon of the logical symbols
    3. $P ∧ ¬ P$ - This is well formed
    4. $(P ∧ Q)(P ∨ R)$- This is not well-formed as there is nothing connecting $(P ∧ Q)$ and $(P ∨ R)$

6. Let $P$ stand for the statement “I will buy the pants” and $S$ for the statement “I will buy the shirt.” What English sentences are represented by the following formulas?

    $$
    \begin{aligned}
      P = \text{I will buy the pants} \\
      S = \text{I will buy the shirt} \\\
    \end{aligned}
    $$

    1. $¬(P ∧ ¬S)$: Can be rewritten as $¬P ∨ S$. Translates to "Either I will not buy the pants or I will buy the shirt"
    2. $¬P ∧ ¬S$: Translates to "I will neither buy the pants nor the shirt"
    3. $¬P ∨ ¬S$: Translates to "I will either not buy the pants or I will not buy the shirt"

7. Let $S$ stand for the statement “Steve is happy” and $G$ for “George is happy.” What English sentences are represented by the following formulas?

    $$
    \begin{aligned}
      S = \text{Steve is happy} \\
      G = \text{George is happy} \\\
    \end{aligned}
    $$

    1. $(S ∨ G) ∧ (¬S ∨ ¬G)$: Translates to "Either Steve or George is happy, but not both"
    2. $[S ∨ (G ∧ ¬S)] ∨ ¬G$: Translates to "Either Steve is happy, or George is happy and Steve isn't, or George isn't happy"
    3. $S ∨ [G ∧ (¬S ∨ ¬G)]$: Translates to "Either Steve is happy, or George is happy and at least one of them is unhappy"

8. Let $T$ stand for the statement “Taxes will go up” and $D$ for “The deficit will go up.” What English sentences are represented by the following formulas?

    $$
    \begin{aligned}
      T = \text{Taxes will go up} \\
      D = \text{The deficit will go up} \\\
    \end{aligned}
    $$

    1. $T ∨ D$: Translates to "Either taxes will go up or the deficit will go up"
    2. $¬(T ∧ D) ∧ ¬(¬T ∧ ¬D)$: Can be rewritten as $(¬T ∨ ¬D) ∧ (T ∨ D)$. Translates to "Either Taxes go up, or deficit go up, but not both"
    3. $(T ∧ ¬D) ∨ (D ∧ ¬T)$: Translates to "Either Taxes go up, or deficit go up, but not both"

9. Identify the premises and conclusions of the following deductive arguments and analyze their logical forms. Do you think the reasoning is valid? (Although you will have only your intuition to guide you in answering this last question, in the next section we will develop some techniques for determining the validity of arguments.)

    A premise is a statement that is assumed to be true and from which a conclusion can be drawn

    1. Jane and Pete won’t both win the math prize. Pete will win either the math prize or the chemistry prize. Jane will win the math prize. Therefore, Pete will win the chemistry prize

        ```text
        Premises
          - Jane and Pete won’t both win the math prize
          - Pete will win either the math prize or the chemistry prize
          - Jane will win the math prize

        Conclusion
          - Pete will win the chemistry prize

        Logical Form
        ~~~text
        
        ~~~
        ```
