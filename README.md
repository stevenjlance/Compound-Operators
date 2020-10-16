CONDITIONAL STATEMENTS 2.0
=============================
Today we are going to increase the complexity of our conditional statements. In the last class, we examined a basic conditional statement whereby if a boolean expression was a true then the `if` portion of the code was executed and if the boolean expression was false then the `else` portion of the code was executed.
```javascript
var school = "DPCHS";
if(school == "DPCHS"){
  console.log("You go to Charter High School!");
} else {
  console.log("You do not go to DPCHS");
}
```

ELSE-IF STATEMENTS
------------------
Let's say we want to ask a user how much money they wished to spend on dinner. If the person has more than $40, we would reccomend one restaurant. If they had between $20 and $39, then we would reccomend a second type of cheeper restaurant. If they have less than $20 then we would reccomend a third type of restaurant.

This situation is very hard to do with a simple `if` statement, but is actually quite easy through the incorporation of an `else if` block in our code.
```javascript
var money = 38;
if(money >= 40){
  // This will only print if they have forty dollars or more.
  console.log("You should go to a fancy restaurant!");
} else if(money >= 20) {
  //This will print if they have less than $40 (the first condition is false), but they have more than $20 (the condition for else if is true).
  console.log("You should go to a moderate priced restaurant");
} else {
  // This will only print if all statements evaluate to false.
  console.log("Maybe stick to McDonalds tonight");
}
```

COMPOUND OPERATORS
------------------
In our last lesson, we talked about comparrison operators (>, <, ==, etc.). Boolean expressions can also include **Logical Operators** `&&`, `||`, `!=` (AND, OR, NOT). Both sides of the logical operator are reduced to a single Boolean value. An exaplanation of each can be seen below.

Logical Operator | Symbol| Description |
------------ | ------------- | ------------- 
AND | `&&` | Evaluates to **`true`** when **BOTH** expressions are `true`
OR | `||`| Evaluates to **`true`** when **at least ONE** expression is `true`
NOT | `!`| Takes a single `true`/`false` value and inverts (reverses) it (e.g. `true` becomes `false`).  

For example, if we wanted to test if a number was larger that 20 **AND** smaller than 40, then we could say:
```javascript
var num = 32
if(num > 20 && num < 40){
  console.log("Your number is between 20 and 40");
} else{
  console.log("Your number is NOT between 20 and 40");
}
```
In the above example `num > 20` evaluates to `true` and `num < 40` also evaluates to `true`. Since they both are `true`, then the entire statement evaluates to `true`. If only one of these were true, then the entire statement would be `false`.

Let's do a similar example that wants to check if someone is a student (younger than 18) **OR** a senior citizen (older than 65). We could do a similar logic with an OR statement as we only need one age statement to evaulate to `true` for the entire expression to be `true`.
```javascript
var age = 12
if(age <= 18 && age >= 65){
  console.log("You get a discount!");
} else{
  console.log("No discount for you!");
}
```


TODAY'S TASKS
--------------
All starter code can be found on the `script.js` file.
1. The line of code below will prompt the user to enter their age. If the user is 17 or older, tell them that they can see an R rated movie. If they are 13 or older,tell them that they can see a PG-13 movie. If they are 7 or older, tell them they can see a PG rated movie. Otherwise, tell them that they are too young.
2. Uncomment the var grade line of code in `script.js`. The prompt asks the user to enter a quiz score. Write an if/else-if/else statement that determines their grade. The breakdown is 90 - 100 is an A, 80 - 89 is a B, 70 - 79 is a C, and 69 and lower is a F.
3. Uncomment the line of code that will ask the user to enter a number. Check if the user's guess is equal to the secretNumber. Return a message based on 3 possible cases: (1) They were right, (2) Their guess was higher than the number, and (3) Their guess was lower than the number.
4. Uncomment the line of code. This is an example of a compound operator. Write your own AND (&&) statement and your own OR (||) statement using the example as a model.
5. **Weekend Checker**: Uncomment the prompt below that asks the user what day of the week it is. If the day is Saturday or Sunday, return the message "It's the weekend!" otherwise return a message of "Not the weekend yet :(". 
**BONUS**: This is case sensative. Use `day.toLowerCase()` to convert the response to lowercase before running the if statement (and modify if statement to be lowercase)
6. **Are you a teenager?**: Uncomment the prompt that asks the user their age. If the user is between the ages of 13 and 19, return a message that they are a teenager. Otherwise return a message telling them they are not a teenager.