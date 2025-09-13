# Ex.No: 10  Logic Programming –  Simple queries from facts and rules
### DATE: 13/09/2025                                                                           
### REGISTER NUMBER : 212223060031
### AIM: 
To write a prolog program to find the answer of query. 
###  Algorithm:
 Step 1: Start the program <br> 
 Step 2: Convert the sentence into First order Logic  <br> 
 Step 3:  Convert the sentence into Horn clause form  <br> 
 Step 4: Add rules and predicates in a program   <br> 
 Step 5:  Pass the query to program. <br> 
 Step 6: Prolog interpreter shows the output and return answer. <br> 
 Step 8:  Stop the program.
### Program:
### Task 1:
Construct the FOL representation for the following sentences <br> 
1.	John likes all kinds of food.  <br> 
2.	Apples are food.  <br> 
3.	Chicken is a food.  <br> 
4.	Sue eats everything Bill eats. <br> 
5.	 Bill eats peanuts  <br> 
   Convert into clause form and Prove that John like Apple by using Prolog. <br> 
### Program:
```
likes(steve,X):- easycourse(X).

hard(science).
easycourse(X):-dept(basketweaving,X).
dept(basketweaving,bk301).
```


### Output:
<img width="966" height="151" alt="image" src="https://github.com/user-attachments/assets/29d91afd-9389-4846-9e60-c578829aede0" />


### Task 2:
Consider the following facts and represent them in predicate form: <br>              
1.	Steve likes easy courses. <br> 
2.	Science courses are hard. <br> 
3. All the courses in Have fun department are easy <br> 
4. BK301 is Have fun department course.<br> 
Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”<br> 

### Program:
```
likes(john, X) :- food(X).                % John likes all food

food(apple).
food(chicken).

% Rules
eats(sue, X) :- eats(bill, X).            % Sue eats everything Bill eats
eats(bill, peanut).


```


### Output:
<img width="482" height="225" alt="image" src="https://github.com/user-attachments/assets/696b872e-fbe0-4902-bced-21cfdf4337ac" />



### Task 3:
Consider the statement <br> 
“This is a crime for an American to sell weapons to hostile nations. The Nano , enemy of America has some missiles and its missiles were sold it by Colonal West who is an American” <br> 
Convert to Clause form and prove west is criminal by using Prolog.<br> 
### Program:
```
% General rule: Crime if an American sells weapons to hostile nations
criminal(X) :-
    american(X),
    weapon(Y),
    hostile(Z),
    sells(X, Y, Z).

% Facts
american(west).
missile(m1).
owns(nono, m1).
hostile(nono).
sells(west, m1, nono).

% Rule: missiles are weapons
weapon(X) :- missile(X).
```


### Output:
<img width="463" height="150" alt="image" src="https://github.com/user-attachments/assets/7c434299-99c8-4c27-8bd1-e9121bf10c5d" />



### Result:
Thus the prolog programs were executed successfully and the answer of query was found.
