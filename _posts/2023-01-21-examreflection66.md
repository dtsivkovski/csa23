---
toc: true
layout: post
title: AP Practice 66Q Exam Reflection 
description: I reflect on my performance on this practice exam.
---

# Score: 59/66

## Reflection

I believe I was much stronger on conceptual questions such as those that involved more general/broader concepts or DeMorgan's law. However, I know that I definitely struggled on the ones that asked to find more specific errors within a given piece of code, as these simply took me too long and I still struggle to wrap my brain around it, especially when it involves nested loops. However, I think the mass exposure to these questions really helped me solidify my concepts and was good practice to eventually get faster at solving them and recognizing what the question is asking.

# Questions

### Q1 addOneToEverything enhanced for loop

I thought that it was the first option, where it was an enhanced for loop that also worked to contain the same values for numbers. However, none of the code segments would actually work for it because in number 1, it would not actually change the value of the element in numbers, it just changes the value of the copy assigned within the loop.

### Q2 animals array

I originally thought that the condition in the if statement should be changed to animals[i].equals(str), however that is not the case because the if statement is fine, it's the error in the for loop that would make it go beyond the length of the String array and cause an error.

### Q16 count 2D array columns

I thought that Line 5 should be changed to arr.length instead of arr[0].length, however that would not make a difference because the array is the same length each time. What did need to be changed was to fix it to be int[] row : array because otherwise it would iterate within the column which wouldn't make sense.

### Q18 Equivalent dog cat expressions

On this one, I almost got this one right but I accidentally made a mistake in the fact that I decided that a > b was the opposite of a < b instead of it being a >= b as the opposite of a < b.

### Q43 partialSum method comparing two implementations

I thought that both implementations worked as intended with the first one being faster. However, it turns out that implementation 1 doesn't actually work because it would cause an out of bounds exception (sum[j-1] in the first iteration would be sum[-1] which is not right)

### Q54 recursive String method

I thought that the recusive method was comparing strings in alphabetical ascending order in the recursion. However, it was actually comparing them in reverse alphabetical order and therefore my answer was incorrect.

### Q58 selectSort with int array parameter

I originally thought that Line 4 should be changed to if(numbers[k] > numbers[pos]), however that is not the case because changing Line 2 to int post = j makes sense because you do not want the position to be reset to the 0th index every time when you are doing this sorting method.

