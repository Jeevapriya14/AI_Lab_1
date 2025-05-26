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
```
likes(john,X):-food(X).
eats(sue,X):-eats(bill,X).
eats(bill,peanuts).
food(peanuts).
food(apple).
food(chicken).
```

### Output:
![image](https://github.com/user-attachments/assets/37da47c5-58e4-42a3-b3a6-9303cb57c4d0)
### Task 2:
Consider the following facts and represent them in predicate form: <br>              
1.	Steve likes easy courses. <br> 
2.	Science courses are hard. <br> 
3. All the courses in Have fun department are easy <br> 
4. BK301 is Have fun department course.<br> 
Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”<br> 

### Program:
```
easy(X) :- fun(X).
likes(steve, X) :- easy(X).
hard(X) :- science(X).
fun(bk301).
science(physics).
science(chemistry).
```

### Output:

![image](https://github.com/user-attachments/assets/65377fcd-d967-4885-bb2c-c72c144904f8)


### Task 3:
Consider the statement <br> 
“This is a crime for an American to sell weapons to hostile nations. The Nano , enemy of America has some missiles and its missiles were sold it by Colonal West who is an American” <br> 
Convert to Clause form and prove west is criminal by using Prolog.<br> 
### Program:
```
crime(X):-american(X),
          weapon(Y),
          hostile(Z),
           sells(X,Y,Z).
sells(west,Y,nano):-missile(Y),
    owns(nano,Y).
hostile(Z):-enemy(Z,D).
weapon(Y):-missile(Y).
american(west).
enemy(nano,american).
owns(nano,m1).
missile(m1).
```

### Output:
![image](https://github.com/user-attachments/assets/8404ec0d-2904-41ad-8de7-1d6d5cfcf1df)

### Result:
Thus the prolog programs were executed successfully and the answer of query was found.
