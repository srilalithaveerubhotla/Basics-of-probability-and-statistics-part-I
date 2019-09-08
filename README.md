# Basics-of-probability-and-statistics



# Statistical thinking will one day be as necessary for efficient citizenship as the ability to read and write- H.G Wells



A Useful high level information glossary to kick start as Data scientist
As a part of my journey towards learning the subject from roots this is one of the practises that I scripted for myself on high level.

# INFORMATION GLOSSARY

Data : Any observations that are been collected

Population: the complete set of elements being studied

Sample: Subset of the population

Census: collecting data from every member of the population

Probability : is the study of random events.

Statistics : 1)  It’s a field where we try to find the unknown from the knows incase of uncertain situations
             2)  Collect analyze, summarise ,interpret and draw conclusions on data


Notes:
-------
An event that occurs for sure is called a Certain event and its probability is 1.
An event that doesn’t occur at all is called an impossible event and its probability is 0.
This means that all other possibilities of an event occurrence lie between 0 and 1.
This is depicted as follows:
0 <= P(A) <= 1

where A is an event and P(A) is the probability of the occurrence of the event.


Basic formula of probability:
----------------------------

P(A) = (No. of ways A can occur) / (Total no. of possible outcomes)

Example:

Another example is the rolling of dice. When a single die is rolled, the sample space is {1,2,3,4,5,6}.
What is the probability of rolling a 5 when a die is rolled?
No. of ways it can occur = 1
Total no. of possible outcomes = 6
So the probability of rolling a particular number when a die is rolled = 1/6.


Types of probability:
----------------------
Lets explain this topic with a example:


![example picture](C:/Users/Owner/Pictures/subjective/prob_types.png?raw=true)


Marginal Probabilities :It basically describes about single atributes 
Example from above figure
P(No) = 0.816
P(Old Age) = 0.008

Joint Probability : It Describes about the a combination of attributes

P(Yes And  Young) = 0.077

Union Probability : It Describes about the either of the attributes

P(Yes or Young) = P(Yes) +P(Young) -P(Yes And Young)
				= 0.189+0.362-0.077

Probability - Types Attention Check
-----------------------------------
 Identify the type of probability in each of the below cases:
 1. P(Old and Yes)
 2. P(Yes and Old) 
 3. P(Old)
 4. P(Yes)
 5. P(Old | Yes) 
 6. P(Yes | Old)
 7. P(Young | No)
 8. P(Middle-aged or No)
 9. P(Old or Young)  
				
1 and 2: Joint; 3 and 4: Marginal; 5, 6 and 7: Conditional; 8 and 9: Union  

Compound Probability:
---------------------
Compound probability is when the problem statement asks for the likelihood of the occurrence of more than one outcome.

Formula for compound probability
	• P(A or B) = P(A) + P(B) – P(A and B)
where A and B are any two events.
P(A or B) is the probability of the occurrence of atleast one of the events.
P(A and B) is the probability of the occurrence of both A and B at the same time.


Mutually Exclusive Events : If I have mutually exclusive events then that means  that only one of them could possibly be true.
   Example:  1)  events include ﬂipping heads or tails with a coins
	2) rolling a 1, 2, 3, 4, 5 or 6 on dice
	3)  drawing a red or black card from a deck of cards
	
Note: For a mutually exclusive event, P(A and B) = 0.

Independent Events :  Name itself explains, Outcome of one event is not dependent on the outcome of another event

Complement of an event
-----------------------
A complement of an event A can be stated as that which does NOT contain the occurrence of A.
A complement of an event is denoted as P(Ac) or P(A’).
P(Ac) = 1 – P(A)
or it can be stated, P(A)+P(Ac) = 1
For example,
if A is the event of getting a head in coin toss, Ac is not getting a head i.e., getting a tail.

Conditional probability :
------------------------
Name itself explain that a probability on a given conditions. It is exactly the probability of one event occuring with some relationship to one or many events 

EXAMPLE:
Event A -Raining Outside
Probability of Event A to happen today is 30%
Event B-You are going out
Probability of Event B to happen today is 50%


![conditional example](C:\Users\Owner\Pictures\subjective\conditional_prob.png?raw=true)

So 42% chance that its raining and going out

Points to Remember:
------------------
According to multiplicative rule of probability:

If A and B events are independent in a probability experiment then both events occur simultaneously

P(A and B)=P(A)⋅P(B)

Example: You have a converse white shoe, and a pair of  blue nike shoes. You also have four shirts: white, black, green, and pink. If you choose one pair of shoes and one shirt at random, what is the probability that you choose the nike and the black shirt?

P(nike and black)=p(nike) * p(black)
			=1/2 *1/4
			=1/8
If A and B events are Dependent in a probability experiment then also both occur simultaneously
 but other event occur by the given occurred event

P(A and B)=P(A)⋅P(B|A)P(A and B)=P(A)⋅P(B|A)
(The notation P(B|A)P(B|A) means "the probability of B, given that A has happened.")

Example:
Suppose you take out two cards from a standard pack of cards one after another, without replacing the first card. What is probability that the first card is the ace of spades, and the second card is a heart?


The two events are dependent events because the first card is not replaced.
There is only one ace of spades in a deck of 52cards. So:
P(1st card is the ace of spades)=152

If the ace of spaces is drawn first, then there are 5151 cards left in the deck, of which 1313 are hearts:
P(2nd card is a heart | 1st card is the ace of spades)=13/51

So, by the multiplication rule of probability, we have:
P(ace of spades, then a heart)=1/52⋅13/51=13/4⋅13⋅51=1/204

I would like to explain confusion matrix before we start Bayes theorem

Confusion matrix :
------------------

We all know that a Binary Value takes  either 0 or 1 
In the same way a binary classifier takes yes or no for predicting

Evaluation of performance in your given data is called test data so it consists of these binary classifier and a problem related to this is said to be a binary classification problem


![binary probabilities](C:\Users\Owner\Pictures\subjective\classifier.png?raw=true)

We typically get 4 different outcomes if a binary classifier predicts data 

• True positive (TP): correct positive prediction
• False positive (FP): incorrect positive prediction
• True negative (TN): correct negative prediction
• False negative (FN): incorrect negative prediction


![confusion matrix](C:\Users\Owner\Pictures\subjective\classifier_1.png?raw=true)

Below picture explains you in a better way

![confusion matix as table](C:\Users\Owner\Pictures\subjective\classifier_3.png?raw=true)

An example :

![example matrix](C:\Users\Owner\Pictures\subjective\confusion_matrix.png?raw=true)


Recall or Sensitiving or True positive rate:  TP / TP+FN

Specificity or True negative rate:   TN / TN+FP

Precision or positive predective values: TP / TP+FP

False Positive Rate or Accuracy:  FP / TN+FP
>>> can also be written as 1-Specificity

F1 Score is also easily extracted from outcomes  and is written as : 2 *(Precision * Recall/Precision + Recall)
























