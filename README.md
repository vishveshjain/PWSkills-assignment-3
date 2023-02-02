# PWSkills-assignment-3
PWSkills assignment 3 of Data Science Masters all answers
---
Q1. Explain with an example each when to use a for loop and a while loop?<br/>
Ans: For loops are used when you have a known number of iterations or when you want to iterate through a sequence (list, tuple, string, etc.) to perform an action for each item in the sequence.

Example:
<pre>
<code>
# print the numbers 0 to 9
for i in range(10):
    print(i)
</code>
</pre>
While loops are used when you want to keep executing a block of code as long as a certain condition is met.

Example:
<pre>
<code>
# print the numbers 0 to 9
i = 0
while i < 10:
    print(i)
    i += 1
</code>
</pre>
It is important to keep in mind that while loops can lead to infinite loops if the termination condition is never met, so it's crucial to make sure that the condition eventually becomes false.

Q2. Write a python program to print the sum and product of the first 10 natural numbers using for
and while loop?<br/>
Ans: Here's an example using a for loop to print the sum and product of the first 10 natural numbers:
<pre>
<code>
sum = 0
product = 1

for i in range(1, 11):
    sum += i
    product *= i

print("The sum of the first 10 natural numbers is:", sum)
print("The product of the first 10 natural numbers is:", product)
</code>
</pre>
And here's an example using a while loop:
<pre>
<code>
sum = 0
product = 1
i = 1

while i <= 10:
    sum += i
    product *= i
    i += 1

print("The sum of the first 10 natural numbers is:", sum)
print("The product of the first 10 natural numbers is:", product)
</code>
</pre>


Q3. Create a python program to compute the electricity bill for a household.
The per-unit charges in rupees are as follows: For the first 100 units, the user will be charged Rs. 4.5 per
unit, for the next 100 units, the user will be charged Rs. 6 per unit, and for the next 100 units, the user will
be charged Rs. 10 per unit, After 300 units and above the user will be charged Rs. 20 per unit.
You are required to take the units of electricity consumed in a month from the user as input.
Your program must pass this test case: when the unit of electricity consumed by the user in a month is
310, the total electricity bill should be 2250.<br/>
Ans:
<pre>
<code>
units = int(input("Enter the units of electricity consumed: "))

if units <= 100:
    bill = units * 4.5
elif units <= 200:
    bill = 100 * 4.5 + (units - 100) * 6
elif units <= 300:
    bill = 100 * 4.5 + 100 * 6 + (units - 200) * 10
else:
    bill = 100 * 4.5 + 100 * 6 + 100 * 10 + (units - 300) * 20

print("The total electricity bill is: Rs.", bill)
</code>
</pre>
Q4. Create a list of numbers from 1 to 100. Use for loop and while loop to calculate the cube of each
number and if the cube of that number is divisible by 4 or 5 then append that number in a list and print
that list.<br/>
Ans: Here is a program that uses a for loop to create a list of numbers from 1 to 100, and then calculates the cube of each number and appends the numbers that are divisible by 4 or 5 to a new list:
<pre>
<code>
numbers = []
cube_divisible = []

for i in range(1, 101):
    numbers.append(i)
    cube = i ** 3
    if cube % 4 == 0 or cube % 5 == 0:
        cube_divisible.append(cube)

print("The list of cubes that are divisible by 4 or 5:", cube_divisible)
</code>
</pre>
And here is the same program using a while loop:
<pre>
<code>
numbers = []
cube_divisible = []
i = 1

while i <= 100:
    numbers.append(i)
    cube = i ** 3
    if cube % 4 == 0 or cube % 5 == 0:
        cube_divisible.append(cube)
    i += 1

print("The list of cubes that are divisible by 4 or 5:", cube_divisible)
</code>
</pre>
Both programs will produce the same output, which is the list of cubes of the numbers from 1 to 100 that are divisible by 4 or 5.

Q5. Write a program to filter count vowels in the below-given string.
string = "I want to become a data scientist" <br/>
Ans:
<pre>
<code>
string = "I want to become a data scientist"
vowels = "aeiouAEIOU"
count = 0

for char in string:
    if char in vowels:
        count += 1

print("The number of vowels in the string is:", count)
</code>
</pre>
