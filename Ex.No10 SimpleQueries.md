# Ex.No: 10  Logic Programming –  Simple queries from facts and rules
### DATE: 6/9/2025                                                                        
### REGISTER NUMBER : 212222040093
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

likes(jhon,X):-food(X).
food(apple).
food(chicken).
eats(sue,X):-eats(bill,X).
eats(bill,peanuts).


### Output:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b1db467f-6281-4462-8e2b-0fda06a8de6f" />


### Task 2:
Consider the following facts and represent them in predicate form: <br>              
1.	Steve likes easy courses. <br> 
2.	Science courses are hard. <br> 
3. All the courses in Have fun department are easy <br> 
4. BK301 is Have fun department course.<br> 
Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”<br> 

### Program:

likes(steve,X):-easycourse(X).
hard(science).
easycourse(X):-dept(basketweaving,X).
dept(basketweaving,bk301).


### Output:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/375edf99-5cf3-42a5-a70c-5b9ef1e29cc6" />


### Task 3:
Consider the statement <br> 
“This is a crime for an American to sell weapons to hostile nations. The Nano , enemy of America has some missiles and its missiles were sold it by Colonal West who is an American” <br> 
Convert to Clause form and prove west is criminal by using Prolog.<br> 
### Program:

crime(X):-american(X),weapon(Y),hostile(X,Z),sells(X,Y,Z).
sells(west,Y,nano):-owns(nano,Y),missile(Y).
weapon(Y):-missile(Y).
hostile(B,A):-enemy(A,B).
enemy(nano,west).
owns(nano,m1).
missile(m1).
american(west).


### Output:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/029e9859-3639-41f2-806c-b8e56f8fe4af" />


### Result:
Thus the prolog programs were executed successfully and the answer of query was found.
