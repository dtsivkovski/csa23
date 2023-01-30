---
toc: true
layout: post
title: AP Practice 52Q Exam Reflection 
description: I reflect on my performance on this practice exam.
---

# Score: 39/52

## Reflection

I am surprised by how much worse I did on this test compared to the previous 66 question one, and I believe I definitely could have done better on it. My pacing on this test was better though, and I think most of my mistakes on this test can be attributed to small mistakes or misreading a small detail.

# Questions

### Q3 2D array with multi-way selection

On this one, my mistake was that I misread how the int[][] was initialized, as I read it as having 4 rows and 3 columns as opposed to the actual 3 rows and 4 columns.

### Q5 array with A through L

This was also a small mistake, where I didn't notice that both the rows and columns started at 1 instead of 0, so my answer for the output was based on the fact that they started at zero and not at 1.

### Q6 calculate method with 2D int array parameter

I thought that the method would return the row index of an element with the largest value in the 2D array, but it was actually returning the column index instead.

### Q9 compSci substring

The value of num is actually 7 and not 3 because printing a substring of the string does not affect the length of the string after that substring is printed.

### Q10 concat 0s and 8s

I didn't realize that there was a += in `str += str + 0 + 8`, so I selected 008 instead of 0008.

### Q11 concat one two zee

For this one, I thought that printing integers automatically converts them to strings if there is a string present in the print statement, but it turns out that they get added together until a string is present, then they start to get converted to strings, so it would be 3Z instead of 12Z.

### Q12 Consider the following code segment

I didn't realize that the set method returns the value being replaced, so I thought that it would be Alex 3 times instead of Alex Bob Carl.

### Q19 for loop substring

I thought that it would return the index of the first occurence of check inside str, but it was actually the index of the last occurence of check inside str. This is due to the fact that you have num = k in the for loop, so the last occurence of check inside str would be the one that is returned.

### Q20 how many times exclamation point printed

I thought that ! would be printed only twice, but that is not the case as it would actually be printed 6 times. I thought that the operator in the statement was < instead of >, so I thought that it would only print the ! twice.

### Q24 loop on string abcdef

I didn't realize that substring(rep, rep+2) would cause an IndexOutOfBoundsException to be thrown because the substring method would be trying to access a character that is out of bounds of the string.

### Q25 manipulate method and animals List

Here, my answer would have been correct if the remove happened before size was calculated in the add statement, but it was not the case here and so it would have caused bear to be at the beginning and baboon at the end.

### Q42 Remove zeros from ArrayList by index

In this case, I forgot that using the remove method would cause the index of the elements to be shifted, throwing an ArrayIndexOutOfBoundsException at the end.

### Q45 strArrMethod - last day of the school year

I thought that the method is executed once for every loop in the nest for loops, which would be 15 times, but I forgot that the if statement would cause it to only be run the 4 times when the condition is true.