# Problem 2

The problem 1 is: 
-  I bought 3 kilograms of carrots and 6 kilograms of bananas, I paid 12 euros.  
   I bought 9 kilograms of carrots and 18 kilograms of bananas, I paid 36 euros.  
   What is the price of a kilogram of carrots and the price of a kilogram of bananas?  

## Zero-Shot prompting with verification of the solution
The prompt is:
>I bought 3 kilograms of carrots and 6 kilograms of bananas, I paid 12 euros.  
 I bought 9 kilograms of carrots and 18 kilograms of bananas, I paid 36 euros.  
 What is the price of a kilogram of carrots and the price of a kilogram of bananas?  
 Verify that the solution satisfies the problem.  

### Bard
Bard returns by default 3 suggestions, let's see them:
- sugestion 1:
![alt text](pictures/pb2_0s_bard_1_1.png)
![alt text](pictures/pb2_0s_bard_1_2.png)
- sugestion 2:
![alt text](pictures/pb2_0s_bard_2_1.png)
- sugestion 3:
![alt text](pictures/pb2_0s_bard_3_1.png)
![alt text](pictures/pb2_0s_bard_3_2.png)

### GPT 3.5
GPT returns only 1 suggestion, let's see it:
![alt text](pictures/pb2_0s_GPT.png)

## Chain-of-Thought prompting with verification of the solution
The prompt is:
>I bought 3 kilograms of carrots and 6 kilograms of bananas, I paid 12 euros.  
 I bought 9 kilograms of carrots and 18 kilograms of bananas, I paid 36 euros.  
 What is the price of a kilogram of carrots and the price of a kilogram of bananas?  
 Let's think step by step.  
 Verify that the solution satisfies the problem.

### Bard
- sugestion 1:
![alt text](pictures/pb2_cot_bard_1_1.png)
- sugestion 2:
![alt text](pictures/pb2_cot_bard_2_1.png)
![alt text](pictures/pb2_cot_bard_2_2.png)
- sugestion 3:
![alt text](pictures/pb2_cot_bard_3_1.png)
![alt text](pictures/pb2_cot_bard_3_2.png)

### GPT 3.5
#### First try
![alt text](pictures/pb2_cot_GPT_1.png)
#### Second try
![alt text](pictures/pb2_cot_GPT_2.png)

## Tree of Thoughts prompting with verification of the solution
The prompt is:
>Imagine three different experts are answering this question.  
All experts will write down 1 step of their thinking,  
then share it with the group.  
Then all experts will go on to the next step, etc.  
If any expert realises they're wrong at any point then they leave.  
Verify that the solution satisfies the problem.  

>I bought 3 kilograms of carrots and 6 kilograms of bananas, I paid 12 euros.  
 I bought 9 kilograms of carrots and 18 kilograms of bananas, I paid 36 euros.  
 What is the price of a kilogram of carrots and the price of a kilogram of bananas?  


### Bard
- sugestion 1:
![alt text](pictures/pb2_tot_bard_1_1.png)
![alt text](pictures/pb2_tot_bard_1_2.png)
- sugestion 2:
![alt text](pictures/pb2_tot_bard_2_1.png)
![alt text](pictures/pb2_tot_bard_2_2.png)
- sugestion 3:
![alt text](pictures/pb2_tot_bard_3_1.png)
![alt text](pictures/pb2_tot_bard_3_2.png)

### GPT 3.5
#### First try
![alt text](pictures/pb2_tot_GPT_1.png)
#### Second try
![alt text](pictures/pb2_tot_GPT_2.png)

## Cramer's rule prompting with verification of the solution
The prompt is:
>I bought 3 kilograms of carrots and 6 kilograms of bananas, I paid 12 euros.  
I bought 9 kilograms of carrots and 18 kilograms of bananas, I paid 36 euros.  
What is the price of a kilogram of carrots and the price of a kilogram of bananas?  
Solve the problem using Cramer's rule.  
Verify that the solution satisfies the problem.  


### Bard
- sugestion 1:
![alt text](pictures/pb2_crr_bard_1_1.png)
![alt text](pictures/pb2_crr_bard_1_2.png)
- sugestion 2:
![alt text](pictures/pb2_crr_bard_2_1.png)
![alt text](pictures/pb2_crr_bard_2_2.png)
- sugestion 3:
![alt text](pictures/pb2_crr_bard_3_1.png)
![alt text](pictures/pb2_crr_bard_3_2.png)

### GPT 3.5
#### First try
![alt text](pictures/pb2_crr_GPT_1.png)
#### Second try
![alt text](pictures/pb2_crr_GPT_2.png)

## Conclusion

| Bard            | 0-shot | CoT | ToT | Cramer | 
|-----------------|--------|-----|-----|--------|  
| mathematization |  OK    | OK  | OK  | OK     |  
| problem solving |  KO    | KO  | OK  | KO     |
| result checking |  KO    | KO  | OK  | KO     |  

| GPT 3.5         | 0-shot | CoT | ToT | Cramer |  
|-----------------|--------|-----|-----|--------|  
| mathematization |  OK    | OK  | OK  | OK     |  
| problem solving |  KO    | OK  | OK  | OK     |  
| result checking |  KO    | OK  | OK  | OK     | 

**Note:**
- once again, GPT 3.5 offers better computing capacity than Bard, although a repeat request may be necessary. 
- However, Bard's suggestion 2 (using the "Tree of thoughts" technique) gives a correct answer.
- GPT 3.5 and Bard are capable of initialising the treatment of the problem using Cramer's rule. Only LLM GPT 3.5 detects the nullity of the determinant, unfortunately it tries to find an alternative solution.