# Part 1 Answers
Stone Tao, A15910056

### 1. 
At line 11, the code will log to console the number equal to `prices.length`. This is because at line 5, we declare `var i = 0` and we run a for loop that increments `i` all the way until it is no longer smaller than `prices.length`, so now `i == prices.length`. Moreover, `var` declarations are not block scoped, so `var i` lives beyond the block at lines 5-9 and is still available at line 11

### 2. 
At line 12, the code will log to console the number equal to the last value `var discountedPrice` was set to in line 6. Again, this is because `var` is not block scoped and so `var discountedPrice` lives beyond the block at lines 5-9 and is still available at line 12

### 3. 
At line 13, the code will log to console the number equal to the last value `finalPrice` was set to in line 7. This is because `var finalPrice` was declared in the earlier line 3.

### 4.
The function will return the array `[50, 100, 150]`. It is an array because at line 2 we declare `var discounted = []` and we never change this declaration, only push elements into the array at line 8. This is eventually returned at line 15. 

We have that the element pushed to `discounted` is `finalPrice = Math.round(discountedPrice * 100) / 100;` and that `var discountedPrice = prices[i] * (1 - discount);`. Substituting `discountedPrice` in we have that `finalPrice = Math.round((prices[i] * (1 - discount)) * 100) / 100;`. As we called `discountPrices([100, 200, 300],. 5)`, then `prices = [100, 200, 300]` and `discount = 0.5`. 

So at `i == 0` `finalPrice = Math.round((100 * (1 - 0.5)) * 100) / 100 = 50`

At `i == 1` `finalPrice = Math.round((200 * (1 - 0.5)) * 100) / 100 = 100`

At `i == 2` `finalPrice = Math.round((300 * (1 - 0.5)) * 100) / 100 = 150`

Thus, at the end `discounted = [50, 100, 150]` and is what is returned.

### 5. 

At line 11, node will complain about a reference error because the variable `i` is not declared in the scope. While we do `let i = 0;` in line 5, it is scoped to the block in lines 5-9.


### 6.

At line 12, node will complain about a reference error because the variable `discountedPrice` is not declared in the scope. While we do `let discountedPrice = prices[i] * (1 - discount);` in line 6, it is scoped to the block in lines 5-9.

### 7.

AT line 13, the same thing will happen as before. The code will log to console the number equal to the last value `finalPrice` was set to in line 7. This is because `let finalPrice` was declared in the earlier line 3, and is scoped to the block in lines 1-15 so `finalPrice` is defined.

### 8.

Assuming everything works (e.g. assuming we bypass the referencee errors in lines 11 and 12) the same result will happen as described in my response to question 4.

### 9.

At line 11, the same will happen as I described in my response to problem 5. Node will complain about a reference error because the variable `i` is not declared in the scope. While we do `const i = 0;` in line 5, it is scoped to the block in lines 5-9.

### 10.

At line 12, the same will happen as I described in my response to problem 6. Node will complain about a reference error because the variable `i` is not declared in the scope. While we do `const discountedPrice = prices[i] * (1 - discount);` in line 5, it is scoped to the block in lines 5-9.

### 11.

At line 13, while we declare `const finalPrice = 0;` at line 3 earlier and thus `finalPrice` is scoped to the block in lines `1-15`, there is a variable assignment error that gets thrown first at line 7 because `finalPrice` is a constant and the code tries to assign a new value to `finalPrice`. However, assuming line 7 doesn't error, then at line 13 it will just log the value of `finalPrice` which is `0` as it was assigned the constant of `0` in line 3.

### 12.

Assumng everything works in previous lines of code and the variable assignment works, then the return result is the exact same as described in problem 8 and problem 4


### 13.

A. `student.name`

B. `student['Grad Year']`

C. `student.greeting()`

D. `student['Favorite Teacher'].name`

E. `student.courseLoad[0]`

### 14.

A. Output is `'32'` because `'3'` is a string and so when we do `'3' + 2`, the `2` converts to a string and is appended like a string to form `'32'` because the `+` operator appends strings together if one of the arguments is a string.

B. Output is `1` because while `'3'` is a string, the `-` operator causes a numeric conversion of `'3'` into `3` and thus `'3' - 2` evaluates to `3-2` and outputs `1`

C. Output is `3` because `null` undergoes numeric conversion and becomes `0` and `3+0` evaluates to `3`

D. Output is `'3null'` because `'3'` is one of arguments to the `+` operator and so `null` undergoes string conversion into `'null'` and adding the strings together outputs `'3null'`

E. Output is `4` since `true` undergoes numeric conversion into `1` and `true + 3` evaluates to `1 + 3` and outputs `4`

F. Output is `0` since `false` and `null` undergo numeric conversion into `0` both. So `false + null` evaluates to `0 + 0` and outputs `0`

G. Output is `'3undefined'` since `undefined` undergos string converion into `'undefined'` and so `'3' + undefined` outputs `3undefined`

H. Output is `NaN` since the `-` operator expects numerical operands and converts `'3'` and `undefined` to numbers, namely `3` and `NaN`. However, any operation involving a `NaN` results in `NaN` so `'3' - undefined` evaluates to `NaN`

### 15.

A. Output is `true` since the string `'2'` converts to the number `2` due to comparing different types and `2 > 1` is true.

B. Output is `false` since we are comparing 2 strings, `'2'` and `'12'` and the first character of the first string is greater than the first character of the 2nd string, thus `'2' < '12'` outputs false.

C. Output is `true` since the string `'2'` converts to the number `2` due to comparing different types and `2 == 2` is true.

D. Output is `false` since we perform a strict equality and `2` is of type `number` wheras `'2'` is of a different type `string` so `2 === '2'` outputs false.

E. Output is `false` since the boolean `true` converts to the number `1` due to comparing different types and `1 == 2` is false.

F. Output is `true` since the value `Boolean(2)` evaluates to `true` as `Boolean` returns `false` for values `0, null, undefined, NaN, ""` and `true` for all else, and `true === true` is true.

### 16.

The `==` operator performs a regular equality check wheras `===` performs a strict equality check. The difference is that in strict equality, it checks the equality without type conversion that `==` does. So `===` always returns false if we compare values of different types when it might otherwise return `true` when using `==`.


### 17.

`'How are you?'` gets printed since line 4 is run. This is because first, the `2 == true` check evaluates to `false` because it uses regular equality check and thus `true` converts to the number `1` and `2 == 1` is false. Since line 1 check is `false`, then the code moves to line 3 where the code checks for the truthiness of `2`, which evalutes to `true` because `Boolean` returns `false` only for values `0, null, undefined, NaN, ""` and `2` is not one of them and is considered to be `true` and so we enter the branch at line 3 and run the console.log command at line 4.

### 19.

By calling `modifyArray([1,2,3], doSomething)` we have that the `array` is `[1,2,3]` and `callback` is `doSomething` in the lines 1-9.

For each element in the array at index `i` from `i = 0` to `i = array.length - 1`, we iterate once and call 

```
newArr.push(callback(array[i], function(x) {
  return x*2;
}));
```

As `callback` is `doSomething`, we are passing in the ith element in the array as well as the function that returns twice the value of the input.

As `doSomething` simply uses the given function and passes it the first parameter + 2, the above block of code is equivalent to

```
newArr.push((array[i] + 2) * 2);
```


Thus, at `i == 0` of the loop,  `array[i]` is `1` then we push `(1 + 2) * 2 == 6` to `newArr`

Thus, at `i == 1` of the loop,  `array[i]` is `2` then we push `(2 + 2) * 2 == 8` to `newArr`

Thus, at `i == 2` of the loop,  `array[i]` is `3` then we push `(3 + 2) * 2 == 10` to `newArr`

Thus by line 8, `newArr` is equal to `[6, 8, 10]` and `[6, 8, 10]` is returned.

### 21.

First, line 8 calls `printNums`. Then line 2 logs `1` to the console. Then at line 3 a timeout of 1000ms is placed to then call a function that logs `2`.
Then line 3 puts a timeout of 0ms to then call a function that logs `3`. Then line 4 logs `4`. 

However, timeout functions are throttled to a minimum of once every 4ms, so the console.logs in line 2 and 5 execute first. Then the earlier timeout executes logging `3`. Then the slowest one at 1000ms logs the final number `2` at approximately 1000ms after the initial function call. Thus, the output is

```
1
4
3
2
```


