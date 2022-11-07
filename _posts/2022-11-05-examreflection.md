---
toc: true
layout: post
title: AP MC Reflection
description: AP CSA Tri 1 Practice MC Reflection
image: https://sjhexpress.com/wp-content/uploads/2021/04/collegeboard-900x430.png
---

# Finals Week Submission

## Links to Units 1-5 Lessons
| Week | Lesson | Lesson | Lesson |
| ----- | ----- | ----- | ----- |
| Week 1 | [Unit 1 - Primitives](https://dtsivkovski.github.io/csa23/week8/primitives) | [Unit 2 - Objects](https://dtsivkovski.github.io/csa23/week8/oop) | |
| Week 2 | [Unit 3 - Booleans / Ifs](https://dtsivkovski.github.io/csa23/week9/booleans-ifs) | [Unit 4 - Iteration](https://dtsivkovski.github.io/csa23/week9/iteration) | [Unit 5 - Classes](https://dtsivkovski.github.io/csa23/week9/classes) |

## Final Exam Reflection
- I got 30/40. I think I could definitely do better than that, however I think that part of it was me trying to stay on pace with the AP exam timing, and I did not want to spend too long on concepts that I was unsure about. Additionally, there were a few problems that really tricked me, such as the one that returned the recursive function twice instead of just once. Overall, I think that though this is a decent score, I could definitely do more practice. I'll pay more careful attention to certain parts of the problem that I may have usually glanced over. I will plan to study these concepts further, such as arraylists and loops (as they are the most time-intensive questions), and will hopefully do better on the next one as a result.

### Question 4
![image](https://user-images.githubusercontent.com/89223402/200199321-294cff92-a476-444d-a13e-5bb30a7df3d7.png)
The correct answer that I should have picked was C, as the multiplication or division part is in integer type, which will round down to 2, even if it would have been 2.33333 if it had not been an integer.

### Question 14
![image](https://user-images.githubusercontent.com/89223402/200199411-f28a3b6a-f008-4722-b6df-d6e044fdbd11.png)
I did not realize that when iterating through an arraylist using the enhanced for loop, that it already gets each vehicle and you do not need to use the get() function.

### Question 15
![image](https://user-images.githubusercontent.com/89223402/200199464-1edb5341-35c9-4a96-9b14-d2008d40edfd.png)
I chose I and II only, even though it was only I. It cannot be the second option because when it tries to check if data[k] > data[k + 1], it gets an out of bounds exception as data[k+1] on the last iteration is out of bounds.

### Question 19
![image](https://user-images.githubusercontent.com/89223402/200199622-7ad1ed0a-8d0f-4c84-9526-53326af70caa.png)
The opposite of !(a != b) is only (a != b). Therefore, it would be applicable to use an OR operator with this opposite value here.

### Question 25
![image](https://user-images.githubusercontent.com/89223402/200199634-d6f763f7-4236-4643-9d14-0e16c7d96aa0.png)
Out of these interfaces, I believed that III would also work as I thought that knowing both surface area and volume can be used in a formula to identify if the boxes could fit within each other. However, I neglected the fact that the 'smaller' box could just be really long and not fit in the larger box.

### Question 30
![image](https://user-images.githubusercontent.com/89223402/200199691-59935a1b-3960-4269-9798-cacdf218d7c3.png)
This returns only ``` ilercom ``` and not ``` ilercomp ```, as the final index of the second part is to up to howFar, which would only be ``` com ```.

### Question 31
![image](https://user-images.githubusercontent.com/89223402/200200146-ff6560d4-38cc-4783-b9ee-276821cafb5b.png)
In this case, I believed that the same array would be printed because I thought that passing it into the function does not actually change its values. However, it seems like passing it into the function still does change the values of it and thus would give the result.

### Question 33
![image](https://user-images.githubusercontent.com/89223402/200200269-f3ccd27a-956e-4215-af7d-ac2c2256f03a.png)
On this one, I believed that incrementing the sum would eventually close the loop. However, because of the OR gate, it would continue on infinitely because k never increments and it would satisfy the while loop condition.

### Question 34
![image](https://user-images.githubusercontent.com/89223402/200200387-53f285a8-dbfa-49f9-8a71-b6ca5185a148.png)
Only II works in this one, as in choice III, x and y are private variables and thus cannot be accessed and modified in that way by the missing code.

### Question 39
![image](https://user-images.githubusercontent.com/89223402/200200420-5d10fdc2-f688-4276-8151-8db4fa98009d.png)
I did not notice that it was ```return recur(recur(n/3));``` and not ```return recur(n/3);```. As a result, it would actually go from 27 to 9 to 18 to 6 to 12 to 4 to 8 to 16.
