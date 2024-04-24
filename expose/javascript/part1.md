#Part 1

**1. What is printed by line 9? If the code returns an error, explain why.**
> values added: 20

**2. What is printed by line 13? If the code returns an error, explain why.**
> final result: 20

**3. What is printed by line 9? If the code returns an error, explain why.**
> values added: 20

**4. What is printed by line 13? If the code returns an error, explain why.**
> The code returns an error because this line attempts to print "final result: " then the variable `result`, but `result` was declared with the `let` declaration inside the `if(add){}` code block. Thus, the scope of `result` is only within that code block because of how `let` variables work and using it outside of it like in line 13 returns an error.

**5. What is printed by line 9? If the code returns an error, explain why.**
> The code returns an error because line 7 is attempting to change the value of variable `result`, but `result` was declared with the `const` declaration on line 5: `const result = 0;`. `const` variables cannot be changed, thus the code returns an error.

**6. What is printed by line 13? If the code returns an error, explain why.**
> The code returns an error because this line attempts to print "final result: " then the varaible `result`, but `result` was declared with the `const` declaration inside the `if(add){}` code block. Thus, the scope of `result` is only within that code block because of how `const` variables work and using it outside of it like in line 13 returns an error.
