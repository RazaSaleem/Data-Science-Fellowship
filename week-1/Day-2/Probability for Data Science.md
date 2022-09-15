# Probability for Data Science 
## Contents
1.	Probability
2.	Mutually Exclusive Events
3.	Non-Mutually Exclusive Events
4.	Dependent and Independent Events
5.	Summary for Rules and formula


## Probability
Probability defines the likelihood of occurrence of an event or chances of occurrence of an event. <br>
Probability (Event) = No of ways an event occurs/Total Outcomes <br>
e.g., Rolling a Dice
S = {1,2,3,4,5,6} <br>
Then <br>
P(1) = 1/6 = 0.1667 <br>

Tossing a coin
S = { H , T } <br>
Then <br>
P(H) = 1/2 = 0.5 <br>
<br>**Experiment:** A trial or an operation conducted to produce an outcome is called an experiment. <br>
<br>**Sample Space:** All the possible outcomes of an experiment together constitute a sample space. For example, the sample space of tossing a coin is head and tail. <br>
<br>**Favorable Outcome:** An event that produces the desired or expected result is called a favorable outcome. For example, when we roll two dice, the possible/favorable outcomes of getting the sum of numbers on the two dice as 4 are (1,3), (2,2), and (3,1). <br>
<br>**Trial:** A trial denotes doing a random experiment. <br >

## Mutually Exclusive Events
In probability theory, two events are said to be mutually exclusive if they cannot occur at the same time or simultaneously. In other words, mutually exclusive events are called disjoint events. If two events are considered disjoint events, then the probability of both events occurring at the same time will be zero. <br>
**Additive Rule (Mutually Exclusive)** <br>
e.g., Rolling a Dice <br>
P (1 or 2 or 3) = P (1) + P (2) + P (3) <br>

 *certain rules for probability are concluded.* <br>
- Addition Rule: P (A + B) = 1 
-	Subtraction Rule: P (A U B)’ = 0
-	Multiplication Rule: P (A ∩ B) = 0

**Example** <br>
What is the probability of a die showing a number 3 or number 5? <br>
Solution: Let,<br>
P(3) is the probability of getting a number 3 <br>
P(5) is the probability of getting a number 5 <br>
P(3) = 1/6 and P(5) = 1/6 <br>
So, <br>
P(3 or 5) = P(3) + P(5) <br>
P(3 or 5) = (1/6) + (1/6) = 2/6 <br>
P(3 or 5) = 1/3 <br>




## Non-Mutually Exclusive Events <br>
Non-mutually exclusive events are events that can happen at the same time. Or Two events are called not mutually exclusive if they have at least one outcome in common. If the two events A and B are not mutually exclusive events, then A ∩ B ≠ ϕ A ∩ B ≠ ϕ.  <br>

**Additive Rule (Non-Mutually Exclusive)**<br>
e.g., Taking out Card from Deck <br>
P (K) = 4/ 52   &emsp;       P(♥)  = 13 / 52    &emsp;         P (K and ♥) = 1/52 <br>
P (K or ♥) = P (K) + P (♥) -- P (K and ♥) <br>
P (K or ♥) = 4/52 + 13/52 – 1/52  = 16/52 <br>



**EXAMPLE** 
In a math class of 30 students, 17 are boys and 13 are girls. On a unit test, 4 boys and 5 girls made an A grade. If a student is chosen at random from the class, what is the probability of choosing a girl or an A student? <br>
P(girl) = 13 / 30		P(A) = 9/30 <br>

P (girl and A) = 5 / 30  <br>

P(girl or A ) = 13/30 + 9/30 – 5/30 <br>

## Dependent and Independent Events
Two events are said to be dependent if the occurrence of one event changes the probability of another event. Two events are said to be independent events if the probability of one event does not affect the probability of another event. If two events are mutually exclusive, they are not independent. Also, independent events cannot be mutually exclusive. <br>

**Multiplicative Rule**
 
### Independent Event 
e.g Tossing a coin three times <br>
S= {1, 2 , 3}  let’s assume the outcome is {H, T, H} <br>
P (H) = 1/2	 &ensp; P (T) = 1/2  &ensp;	P (H) =  1/2 <br>

e.g., Rolling a Dice P (1 and 3) <br>
P (A and B) = P (A) * P (B) <br>
P (1 and 3) = 1/6 * 1/6 = 1/36 <br>


### dependent Event 
e.g Taking a card from a deck <br>
1st experiment for K <br>
P (K) = 1/52 <br>
2nd experiment for Q <br>
P (Q) = 1/51 <br>
3rd experiment for J <br>	
P (J) = 1/50 <br>

e.g., Removing card from deck P (K and Q) <br>
P (A and B) = P (A) * P (B/A)      &emsp;      -> **Conditional Probability** <br>
P (K and Q) = P (K)  * P(Q/K) <br>
P (K and Q) =  1/52  * 1 /51 = 1/2652 <br>



## Summary for Rules and formula
### Additive Rule
P (A or B) = P (A) + P (B)   &emsp;     for Mutually Exclusive <br> 
P (A or B) = P (A) + P (B) – P (A ∩ B)   &emsp; for Non- Mutually Exclusive <br> 

### Multiplicative Rule 
P (A and B) = P (A) * P (B) &emsp; for Independent Event <br>
P (A and B) = P (A) * P (B/A) &emsp; for dependent Event also called conditional Probability <br>
