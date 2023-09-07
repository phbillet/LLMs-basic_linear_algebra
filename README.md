# LLMs & Linear algebra

## Introduction
Are LLMs effective in solving a simple linear algebra system?

The following problems will be used to assess LLMs:
* **Problem 0**

   I bought 3 kilograms of carrots, I paid 12 euros.  
   What is the price of a kilogram of carrots?
   
   This problem has **a single solution**.

* **Problem 1**

   I bought 3 kilograms of carrots and 6 kilograms of bananas, I paid 12 euros.  
   I bought 9 kilograms of carrots and 4 kilograms of bananas, I paid 24 euros.  
   What is the price of a kilogram of carrots and the price of a kilogram of bananas?
   
   This problem has **a single solution**.

* **Problem 2**

   I bought 3 kilograms of carrots and 6 kilograms of bananas, I paid 12 euros.  
   I bought 9 kilograms of carrots and 18 kilograms of bananas, I paid 36 euros.  
   What is the price of a kilogram of carrots and the price of a kilogram of bananas?  
   
   This problem has **an infinity of solutions**.
   
* **Problem 3**

   I bought 3 kilograms of carrots and 6 kilograms of bananas, I paid 12 euros.  
   I bought 9 kilograms of carrots and 18 kilograms of bananas, I paid 32 euros.  
   What is the price of a kilogram of carrots and the price of a kilogram of bananas?  
   
   This problem has **no solution**.
    
For this experiment, the following LLMs will be used:
* [Bard](https://bard.google.com/)
* [GPT 3.5](https://app.getmerlin.in/) - using Merlin


The following prompting techniques will be used:
* [Zero-Shot prompting](https://www.promptingguide.ai/techniques/zeroshot) with verification of the solution
* [Chain-of-Thought prompting](https://www.promptingguide.ai/techniques/cot) with verification of the solution
* [Tree of Thoughts prompting](https://www.promptingguide.ai/techniques/tot) with verification of the solution
* [Cramer's rule](https://en.wikipedia.org/wiki/Cramer%27s_rule) with verification of the solution (only for problem 1 and problem 2)

The following points will be assessed:
- mathematization of the problem 
- problem solving
- ability to apply a given method - Cramer's rule
- ability to check results.

## Problem 0

Click on the link to view the results associated with [problem 0](problem_0.md).

## Problem 1

Click on the link to view the results associated with [problem 1](problem_1.md).

## Problem 2

Click on the link to view the results associated with [problem 2](problem_2.md).

## Problem 2

Click on the link to view the results associated with [problem 3](problem_3.md).

## Conclusion

The tests carried out here are fairly superficial, but we were able to observe that :
- the 2 LLMs considered easily transformed the text of the problem into an equation
- Bard had difficulty performing simple arithmetic operations, GPT 3.5 clearly has an advantage in this area (although it sometimes makes mistakes too)
- Bard's weakness in arithmetic is very detrimental to good solving and even more so to verification.  

GPT 3.5 is not necessarily better than Bard in linear algebra (both LLMs offer good solution methods), but Bard's arithmetic errors are clearly a big disadvantage.
