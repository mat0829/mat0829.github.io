---
layout: post
title:      "Questions That Need Answering"
date:       2018-11-15 15:09:12 -0500
permalink:  another_day_of_grinding_on
---

# Javascript Assessment Questions:
  1. What is Scope
  
   (What will each statement log to the console?)
	 <br>
	 <br>
			I believe that var will become "first value" in the outer scope, which is true, which means that in inner block it of the if true it then becomes "second value" because it's a global variable and globally scoped and both the inner and outer scope have access to the outer block's var variable and the original var variable is reassigned to "second value" in the inner scope. 
			result = (This is what happened)
			
			I believe that let will become "first value" in the outer scope, which is true, but once it goes into the true block it will not have access to the outer block's let variable. Thus, it will stay as "first value", the value from the outer scope block. 
			result = (This is what happened)
			
			I believe that const will become "first value" in the outer scope, which is true, but like let once it goes into the true block it will not have access to the outer block's const variable so it will stay as "first value" which is the value from the outer scope block. 
			result = (This is what happened)
			
			I believe that evil will become "first value" in the outer scope, which is true, and like var, which is also globally scoped, both the inner and outer scopes will have access to the outer scope's evil variable, thus evil will be reassigned to "second value" in the inner scope. 
			result = This is what happened
			
  (remove var, let, const from inside if (true). Do we get anything different?)
	   Yes because by removing the inner scope's variables both var and evil, the only two qualifying to have their values reassigned because of being globally scoped, are not reassigned ever so every variable stays as it was assigned in the outer scope. 
			
			

