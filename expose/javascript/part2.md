#Part 2
**1. What will happen at line 12 and why? If the code causes an error, explain why.**
> Line 12 will print "3" because in the for loop on line 6, the variable `i` is declared with the `var` declaration. The for loop stops at the length of the `prices` array. Because `i` is a `var` variable, it can be used outside of the scope of the for loop. Line 19 executes `discountPrices([100,200,300],0.5);` so the `prices` array has a length of 3. The for loop stops at this length, meaning `i == 3` at the point of termination. Thus, line 12 prints "3".

**2. What will happen at line 13 and why? If the code causes an error, explain why.**
> Line 13 will print "150" because in the for loop on line 6, the variable `discountedPrice` is declared with the `var` declaration. Line 19 executes `discountPrices([100,200,300],0.5);` so at the last sequence of the for loop, `discountedPrice = 300 * (1 - 0.5);` which results in 150. Because `discountedPrice` is a `var` variable and how `var` variables an be accessed outside of its original scope, line 13 prints "150".

**3. What will happen at line 14 and why? If the code causes an error, explain why.**
> Line 14 will print "150". Using my answer from the previous question, `discountedPrice = 150` at the last sequence of the for loop. Then, during this last sequence `finalPrice = Math.round(150 * 100) / 100;` which results in 150. Also, `finalPrice` is declared using the `var` declaration, meaning it can be used outside the scope of the for loop. Thus, line 14 prints "150".

**4. What will this function return? Give a brief explanation why. If the code causes an error, explain why.**
> This function will return [50,100,150]. In the function, the for loop goes through each element in the array, `prices`. There are 3 elements in the array `[100,200,300]` and our discount is `0.5` given in line 19. In the first sequence we have: `var discountedPrice = 100 * (1 - 0.5);` which equals 50, this gets pushed onto the `discounted` array. The second sequence we have: `var discountedPrice = 200 * (1 - 0.5);` which equals 100, this gets pushed onto the `discounted` array. The third sequence we have: `var discountedPrice = 300 * (1 - 0.5);` which equals 150, this gets pushed onto the `discounted` array. Lastly, after the for loop `discounted` is returned, thus returning [50,100,150].

**5. What will happen at line 12 and why?  If the code causes an error, explain why.**
> The code returns an error because this line attempts to print `i` but `i` was declared with the `let` declaration inside the for loop. Thus, the scope of `i` is only within that for loop because of how `let` variables work and using it outside of it like in line 12 returns an error.

**6. What will happen at line 13 and why? If the code causes an error, explain why.**
> The code returns an error because this line attempts to print `discountedPrice` but `discountedPrice` was declared with the `let` declaration inside the for loop. Thus, the scope of `discountedPrice` is only within that for loop because of how `let` variables work and using it outside of it like in line 13 returns an error.

**7. What will happen at line 14 and why? If the code causes an error, explain why.**
> Line 14 will print "150". The value of "150" comes from the same reasoning of my answer in question 3. The logic follows even though `finalPrice` is a `let` variable instead of a `var` variable. This is because `finalPrice` was declared on line 4: `let finalPrice = 0;` before the for loop, so printing it on line 14 is still within the proper scope. Thus, line 14 prints "150".

**8. What will this function return? Give a brief explanation. If the code causes an error, explain why.**
> This function will return [50,100,150]. The values [50,100,150] come from the same reasoning of my answer in question 4. The logic follows even though `discounted`,`finalPrice`,`i`,`discountedPrice` were declared as `let` variables instead of `var` variables. This is because they are all declared and used within their proper scopes. Variables `discounted` and `finalPrice` although declared outside the for loop, can be used in the for loop because it is declared before it. 

**9. What will happen at line 11 and why? If the code causes an error, explain why.**
> The code will return an error because line 11 is attempting to print `i`, but `i` was declared with the `let` declaration inside the for loop. Thus, the scope of `i` is only within the for loop because of how `let` variables work and using it outside of it like in line 11 returns an error.

**10. What will happen at line 12 and why? If the code causes an error, explain why.**
> Line 12 prints "3" because line 17 executes: `discountPrices([100,200,300],0.5);` and the array [100,200,300] has a length of 3. Line 4 assigns `const length = prices.length;` so in this case, `const length = 3;` and line 12 is printing `length`. Thus, line 12 prints "3".

**11. What will this function return? Give a brief explanation. If the code causes an error, explain why.**
> This function will return [50,100,150]. The values [50,100,150] come from the same reasoning of my answer in question 4. The logic follows even though `discounted`,`finalPrice`,`discountedPrice` were declared as `const` variables instead of `var` variables. This is because they are all declared and used within their proper scopes. You can still push elements onto a const array like in line 8. You can redeclare `const discountedPrice` during every iteration of the for loop in line 7. Thus, this function will return [50,100,150].

**12. Given the above Object, write the notation for:**
**A. Accessing the value of the name property in the student object**
>`student.name;`
**B. Accessing the value of the Grad Year property in the student object**
>`student['Grad Year'];`
**C. Calling the function for the greeting property in the student object**
>`student.greeting();`
**D. Accessing the name property of the object in the Favorite Teacher property in student**
>`student['Favorite Teacher'].name;`
**E. Access index zero in the array of the courseLoad property of the student object**
>`student.courseLoad[0];`

**13. Arithmetic**
**A. ‘3’ + 2**
>`'32'`
**B. ‘3’ - 2**
>`1`
**C. 3 + null**
>`3`
**D. ‘3’ + null**
>`'3null'`
**E. true + 3**
>`4`
**F. false + null**
>`0`
**G. '3' + undefined**
>`'3undefined'`
**H. '3' - undefined**
>`NaN`

**14. Comparison**
**A. ‘2’ > 1**
> `true`
**B. ‘2’ < ‘12’**
>`false`
**C. 2 == ‘2’**
>`true`
**D. 2 === ‘2’**
>`false`
**E. true == 2**
>`false`
**F. true === Boolean(2)**
>`true`

**15. Explain the difference between the == and === operators.**
>The == operator does type conversion then checks for equality between the two values. On the other hand, the === operator, aka the *strict equality operator*, checks for equality without converting the types.

**16. Given the above Object, write a for...in loop that will iterate through it and print out the value of the property if the property starts with the letter r, or if the value of that property is an odd number.  (This should be in a JS file part2-question16.js)**
```
for (let property in statistics) {
    let value = statistics[property];
    if ((property.startsWith('r')) || (value % 2 != 0)) {
        console.log(statistics[property]);
    }
}
```
**17. If the function above is called with the following parameters modifyArray([1,2,3], doSomething), what will be the result? Briefly walk through how you arrived at that result. (This should be in your part2.md). Here we are passing in a function as a parameter, however we can also return a function from another function just as easily, you're encouraged to play around with callbacks as they are used heavily in frontend JS development.**
> The result is [2,4,6]. First, we have the array `newArr`. Then, we have a for loop that iterates through array `array`, which in this case is [1,2,3]. For each iteration of the loop, we execute the function `callback` on the current element in `array` and push this value onto `newArr`. In this case, our function is `doSomething`. The function `doSomething` returns the input * 2. So the for loop will do, 1 * 2 = 2, push this onto `newArr`. 2 * 2 = 4, push this onto `newArr`. 3 * 2 = 6, push this onto `newArr`. Then `modifyArray` returns `newArr`, giving us [2,4,6].

**18. The above program only prints out the time once when executed. Modify this code such that the program prints out the time every second.  (This should be a JS file - part2-question18.js)**
```
setInterval(() => {
    let d = new Date();
    let time = d.toLocaleTimeString();
    console.log(time);
  }, 1000);
```

**19. What is the output of the above code? (This should be in your part2.md)**
> 1
> 4
> 3
> 2