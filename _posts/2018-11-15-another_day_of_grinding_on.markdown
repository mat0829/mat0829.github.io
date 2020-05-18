---
layout: post
title:      "Questions That Need Answering"
date:       2018-11-15 15:09:12 -0500
permalink:  another_day_of_grinding_on
---

# Javascript Assessment Questions:
  ## 1. What is Scope
  
   (What will each statement log to the console?)
<br>
<br>
			I believe that var will become "first value" in the outer scope, which is true, which means that in inner block it of the if true it then becomes "second value" because it's a global variable and globally scoped and both the inner and outer scope have access to the outer block's var variable and the original var variable is reassigned to "second value" in the inner scope. 
			result = (This is what happened)
<br>
<br>
			I believe that let will become "first value" in the outer scope, which is true, but once it goes into the true block it will not have access to the outer block's let variable. Thus, it will stay as "first value", the value from the outer scope block. 
	 <br>
			result = (This is what happened)
<br>
<br>
			I believe that const will become "first value" in the outer scope, which is true, but like let once it goes into the true block it will not have access to the outer block's const variable so it will stay as "first value" which is the value from the outer scope block. 
	 <br>
			result = (This is what happened)
<br>
<br>
			I believe that evil will become "first value" in the outer scope, which is true, and like var, which is also globally scoped, both the inner and outer scopes will have access to the outer scope's evil variable, thus evil will be reassigned to "second value" in the inner scope.
	 <br>
			result = This is what happened
<br>
<br>
  (remove var, let, const from inside if (true). Do we get anything different?)
<br>
<br>
	   Yes because by removing the inner scope's variables both var and evil, the only two qualifying to have their values reassigned because of being globally scoped, are not reassigned ever so every variable stays as it was assigned in the outer scope. 
<br>
<br>
## 2. Take a look at the following functions:

  (What would sayName log?)
<br>
<br>
			I think that theName will be undefined because of the fact that var theName is globally scoped so it gets declared like the function with hoisting during the compilation phase but only get assigned to undefined.
			<br>
		  result = This is what happened.
<br>
<br>
  (What would speakName log?)
<br>
<br>
    I think that the function speakName will throw an error because of the fact that let theName is not globally scoped so it goes not get hoisted during the compilation phase and declared so it can't access the variable because it doesn't get assigned until the execution phase of the Javascript engine. 
		<br>
		result = It gave an ReferenceError
<br>
<br>
  (What would yellName log?)
<br>
<br>
   I think that the function will work as desired because of functions being hoisted in the Javascript Engine during the compilation phase and the function yellName having access to both it's own scope and variables and the inner function theName's scope and variables.
	 <br>
	 result = It worked! :)
<br>
<br>
## 3. What will the following three lines log?
<br>
<br>
  (game.details.characterName()?)
<br>
<br>
  I think that it will return the name "Yoshi" because it is "this" in the current execution context when the function is being run as it went first to game, then details, where the character "Yoshi" is the character string. 
	<br>
	result = I was right. 
<br>
<br>
  (game.details.characterName.bind(game)?)
<br>
<br>
  I think that it will return the name "Mario" because first it goes to game, then details, but this time it goes to the function characterName() which then binds this to game, which makes the current character string "Mario". 
	<br>
	result = I go a weird result of "Function: bound characterName". I think because it bound game which is an object. 
<br>
<br>
  (const characterName = game.details.characterName; 
	characterName()?)
<br>
<br>
  I think that it will be Daisy because it reassigning characterName to what it was originally in the traditional call of the function characterName() where this.character is "Daisy". 
	<br>
	result = This is what happened.

