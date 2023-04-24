# Python-Program-to-check-Abundant-Number

Check Whether or Not the Number is an Abundant Number in Python
Given an integer input as the number, the objective is to check whether or the given integer number is an Abundant Number or not. Therefore, we’ll write a program to Check Whether or Not the Number is an Abundant Number in Python Language.

Example
Input : 21
Output : It's not an Abundant Number. 
abundant or not in python
Check Whether or Not the Number is an Abundant Number in Python Language
Given an integer input the objective is to check whether or not the given integer is an Abundant Number. To do so we’ll use loop to find the factors of the number except the number itself and sum them all up. We’ll check Whether the number is lower or greater than the sum. For a Number to be classified as Abundant, the sum of it’s factors must be greater than the number itself. Here are the method’s we’ll be using to Check Whether or Not the Number is an Abundant Number in Python Language,

Method 1: Using Range until Number
Method 2: Using Range until Sqrt( Number )
We’ll discuss the above mentioned methods in detail in the upcoming sections. Do check out the blue box given below for better understanding of the above mentioned questions.

Abundant Number
A Number that is smaller than the sum of all it's factors except the number itself is known as an Abundant number.
Let's try and understand the concept better using an example

Example
Input : Number = 12
Output : Yes, It's an Abundant Number
Explanation : The Factors for the number 12 are, 1, 2, 3, 4 and 6. We don't want to include the number itself.
Now the sum of the factors except the number itself is :
1 + 2 + 3 + 4 + 6 = 16
as the number 16>12 , the number itself.
It's an abundant number.
We'll discuss on how to check for it in the upcoming sections.

Method 1: Using Range until Number
Python Code
Run
n = 12

sum=1 # 1 can divide any number 

for i in range(2,n):
  if(n%i==0):    #if number is divisible by i add the number 
   sum=sum+i

if(sum>n):
  print(n,'is Abundant Number')

else:
  print(n,'is not Abundant Number')
Output
12 is Abundant Number
Method 2: Using Range until Sqrt( Number )
Python Code
Run
import math
n = 12
sum=1 # 1 can divide any number 
i=2

while(i<=math.sqrt(n)): 
  if(n%i==0): 
#if number is divisible by i add the number 
    if(n//i==i): 
# if quotient is equal to divisor add only one of them 
      sum=sum+i 
    else: 
        sum=sum + i + n/i 
        i=i+1 
    if(sum>n):
        print(n,"is Abundant Number")
    else:
        print(n,"is not Abundant Number")
Output
12 is Abundant Number
