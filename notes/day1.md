Section 1 => The engine of the JS does the registration for the variables first before starting to run the code. This process is called hoisting. The var/let/function are hoisted in different ways: var is hoisted and can be assigned a value before declaration, and let is hoisted but in the TDZ, so we cannot access it before declaration. 
Function declaration is hoisted, and you can call it before function declaration normally, but function expression/arrow depends on the variables assigned to them, like var/let, so with var it is hoisting, but the value is still undefined for the variable when you try to call it before the declaration, so it gives you a type error, while with let you cannot call it before declaration also because the let is in the TDZ and not initialized, so it gives you a reference error.

    
Section 2 => I predict that the call of the function (a) is then inside function (a), which calls function (b), so it will be looking for 
the value of the variable inside function (b) then (a) then in the global scope.
Q6: This block of code will run 3 times; the output will be (0,1,2), and the settimeout() is a function. It is async code, so it will be run after the for loop.


Section 3 => | Reference error | var name = ahmed; console.log(x); | variable not defined 
             -------------------------------------------------------------------------------
             | Reference error | console.log(name); let name = ahmed; | need to read let/const variable before the line that declares it runs 
             -------------------------------------------------------------------------------
             | Type error | name(); var name = function(){}; | calling a var variable that holds an undefined value
             -----------------------------------------------------------------------------------

Section 4 =>  I learned today about shadowing, which is when we have two variables with the same name in different scopes, so they are different variables, and also about scope chain 

