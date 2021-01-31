# Part 1 Answers
Stone Tao, A15910056

1. At line 11, the code will log to console the number equal to `prices.length`. This is because at line 5, we declare `var i = 0` and we run a for loop that increments `i` all the way until it is no longer smaller than `prices.length`, so now `i == prices.length`. Moreover, `var` declarations are not block scoped, so `var i` lives beyond the block at lines 5-9 and is still available at line 11

2. At line 12, the code will log to console the number equal to the last value `var discountedPrice` was set to in line 6. Again, this is because `var` is not block scoped and so `var discountedPrice` lives beyond the block at lines 5-9 and is still available at line 12

3. At line 13, the code will log to console the number equal to the last value `finalPrice` was set to in line 7. This is because `var finalPrice` was declaed in the earlier line 3.

4. The function will return the array `[50, 100, 150]`. It is an array because at line 2 we declare `var discounted = []` and we never change this declaration, only push elements into the array at line 8. This is eventually returned at line 15. 

We have that the element pushed to `discounted` is `finalPrice = Math.round(discountedPrice * 100) / 100;` and that `var discountedPrice = prices[i] * (1 - discount);`. Substituting `discountedPrice` in we have that `finalPrice = Math.round((prices[i] * (1 - discount)) * 100) / 100;`. As we called `discountPrices([100, 200, 300],. 5)`, then `prices = [100, 200, 300]` and `discount = 0.5`. 

So at `i == 0` `finalPrice = Math.round((100 * (1 - 0.5)) * 100) / 100 = 50`

At `i == 1` `finalPrice = Math.round((200 * (1 - 0.5)) * 100) / 100 = 100`

At `i == 2` `finalPrice = Math.round((300 * (1 - 0.5)) * 100) / 100 = 150`

Thus, at the end `discounted = [50, 100, 150]` and is what is returned.

5. 
