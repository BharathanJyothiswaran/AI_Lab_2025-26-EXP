# Ex.No: 10  Logic Programming –  Simple queries from facts and rules
### DATE:                                                                            
### REGISTER NUMBER : 
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

likes(john,X):-food(X).

eats(sue,X):-eats(bill,X).

eats(bill,peanuts).

food(apple).

food(peanuts).

food(chicken).


### Output:

<img width="503" height="266" alt="image" src="https://github.com/user-attachments/assets/b33be5c6-96df-4d20-9fa6-8e6262fa8e18" />


### Task 2:
Consider the following facts and represent them in predicate form: <br>              
1.	Steve likes easy courses. <br> 
2.	Science courses are hard. <br> 
3. All the courses in Have fun department are easy <br> 
4. BK301 is Have fun department course.<br> 
Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”<br> 

### Program:

likes(steve, X) :- easy(X).

hard(X) :- science_course(X).

easy(X) :- have_fun_department_course(X).

have_fun_department_course(bk301).


### Output:

<img width="555" height="186" alt="image" src="https://github.com/user-attachments/assets/a9ad3700-5220-480a-ae45-347475a4888c" />


### Task 3:
Consider the statement <br> 
“This is a crime for an American to sell weapons to hostile nations. The Nano , enemy of America has some missiles and its missiles were sold it by Colonal West who is an American” <br> 
Convert to Clause form and prove west is criminal by using Prolog.<br> 
### Program:

criminal(X):-

american(X),

weapon(Y),

hostile(Z),

sells(X,Y,Z).

weapon(Y):-

missile(Y).

hostile(Z):-

enemy(Z,X).

sells(west,Y,nano):-

missile(Y),

owns(nano,Y).

missile(m).

owns(nano,m).

enemy(nano,america).

american(west).


### Output:

<img width="598" height="251" alt="image" src="https://github.com/user-attachments/assets/0c3f44a8-4e1a-466d-a949-a7f1212368fe" />


### Result:
Thus the prolog programs were executed successfully and the answer of query was found.
