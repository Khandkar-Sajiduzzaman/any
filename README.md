#Task 1
Write a function called even_checker that takes a number as an argument and prints whether the number is even or odd inside the function.

[ ]
  1
  2
  3
  4
  5
  6
def even_checker(n):
    if n%2==0:
       print("Even!!!")
    else:
       print("Odd!!!")
even_checker(int(input()))
4
Even!!!
Task 2
Write a python function that takes the limit as an argument of the Fibonacci series and prints till that limit.

[ ]
  1
  2
  3
  4
  5
  6
  7
  8
  9
def fibonacci(n):
   fibo1=0
   fibo2=1
   while fibo1<=n:
        print(fibo1, end=" ")
        num=fibo1+fibo2
        fibo1=fibo2
        fibo2=num
fibonacci(int(input("Enter the number: ")))
Enter the number: 10
0 1 1 2 3 5 8 
Task 3
Write a function called foo_moo that takes a number as an argument and returns the following statements according to the below mentioned conditions. Then, finally prints the statement in the function call.
def foo_moo(n):
    if n%2==0 and n%3==0:
        return "FooMoo"
    elif n%2==0:
        return "Foo"
    elif n%3==0:
        return "Moo"
    else:
        return "Boo"
print(foo_moo(int(input())))

Task 4
Write a python function that takes a string as an argument. Your task is to calculate the number of uppercase letters and lowercase letters and print them in the function.
def func(n):
    upper=0
    lower=0
    for i in n:
        if 64<ord(i)<91:
            upper+=1
        elif 96<ord(i)<123:
            lower+=1
    print(f"No. of Uppper Character: {upper}")
    print(f"No. of Lowercase Character:{lower}")
func()

Task 5
Write a function called calculate_tax that takes 3 arguments: your age, salary, and current job designation. Your first task is to take these arguments as user input and pass these values to the function. Your second task is to implement the function and calculate the tax as the following conditions:

age=int(input("Enter your age: "))
salary=float(input("Enter your salary: "))
designation=input("Your designation: ")
def calculate_tax(age, salary, designation):

    if age<18 or salary<10000 or designation.lower()=="president":
        return 0
    elif 10000<salary<20000:
        return salary*0.05
    else:
        return salary*0.1
print(calculate_tax(age, salary, designation))

Task 6
Write a function which will take 1 argument, number of days. Your first task is to take the number of days as user input and pass the value to the function. Your second task is to implement the function and calculate the total number of years, number of months, and the remaining number of days as output. No need to return any value, print inside the function. Note: Assume, each year to be 365 days and month to be 30 days.

days=int(input("Enter the days: "))
def yamete_kudasai(days):
    x=days//365
    days=days%365
    y=days// 30
    z=days % 30
    print(f"{x} years, {y} month and {z} days")
yamete_kudasai(days)

Task 7
Write a function called show_palindrome that takes a number as an argument and then returns a palindrome string. Finally, prints the returned value in the function call.

def show_palindrome(n):
    s=""
    for i in range(1,n+1):
        s+=str(i)+" "
    for i in range(n-1,0,-1) :
        s+=str(i)+" "
    return s
user=int(input("Enter the digit: "))
print(show_palindrome(user))
 
Task 8
Write a function called show_palindromic_triangle that takes a number as an argument and prints a Palindromic Triangle in the function.

user=int(input("Enter input: "))
def show_palindromic_triangle(n):
    for i in range(1, n+1):
        v =" "*(n-i)
        x = v+show_palindrome(i)
        print(x)
show_palindromic_triangle(user)

 
Task 9
Write a function called area_circumference_generator that takes a radius of a circle as a function parameter and calculates its circumference and area. Then returns these two results as a tuple and prints the results using tuple unpacking in the function call according to the given format.

import math
def area_circumference_generator(x):
    cir=2*math.pi*x
    area=math.pi*(x**2)
    return (area,cir)
results=area_circumference_generator(float(input("Enter the radius: ")))
x,y=results
print(results)
print(f"Area of the circle is {x} and circumference is {y}")

Task 10
Write a function called make_square that takes a tuple in the parameter as a range of numbers (starting point and ending point (included)). The function should return a dictionary with the numbers as keys and its squares as values.

def make_square(x):
    a,b=x
    y={}
    for i in range(a,b+1):
        y[i]=(i**2)
    return y
print(make_square((1,6)))


Task 11
Write a function called rem_duplicate that takes a tuple in the parameter and return a tuple removing all the duplicate values. Then print the returned tuple in the function call.

[Cannot use remove() or removed() for this task]
Hints: Unlike lists, tuples are immutable, so the tuple taken as an argument cannot be modified. But the list can be modified and lastly for returning the result use type conversion. You need to use membership operators (in, not in) for preventing adding any duplicates values.

def rem_duplicate(num):
    lst=list(num)
    lst2=[]
    for i in lst:
        if i not in lst2:
            lst2.append(i)
    return tuple(lst2)
print(rem_duplicate((1,1,1,2,3,4,5,6,6,6,6,4,0,0,0)))


Task 12
Write a python function that takes a list as an argument. Your task is to create a new list where each element can be present at max 2 times. Inside the function, print the number of elements removed from the given list. Finally, return the new list and print the result.

def func(lst):
    rem=0
    lst1=[]
    for i in lst:
        if lst1.count(i)>1:
            rem+=1
        else:
            lst1.append(i)
    print(f"Removed:{rem}")
    return lst1
print(func())


def func(lst):
    rem=0
    lst1=[]
    for i in lst:
        if i not in lst1:
            lst1.append(i)
        else:
            if lst1.count(i)<2:
                lst1.append(i)
            else:
                rem+=1
    print(f"Removed {rem}")
    return lst1
print(func([1, 2, 3, 3, 3, 3, 4, 5, 8, 8]))

Task 13
Write a python function that will perform the basic calculation (addition, subtraction, multiplication and division) based on 3 arguments. They are: Operator ('+', '-', '/', '*') First Operand (any number) Second Operand (any number) Your first task is to take these arguments as user input and pass the values to the function parameters. Your second task is to write a function and perform the calculation based on the given operator. Then, finally return the result in the function call and print the result.

user1=input("Enter the operator: ")
user2=int(input("First Operand : "))
user3=int(input("Second Operand: "))
def operations(x,y,z):
    if x=="+":
        return (y+z)
    elif x=="-":
        return (y-z)
    elif x=="/":
        return (y/z)
    elif x=="*":
        return (y*z)
print(operations(user1,user2,user3))


Task 14
Write a function which will take 2 arguments. They are: Sentence Position Your first task is to take these arguments as user input and pass these values to the function parameters. Your second task is to implement the function and remove the characters at the index number which is divisible by the position (Avoid the index number 0 as it will always be divisible by the position, so no need to remove the index 0 character). Finally, add the removed characters at the end of the new string. Return the value and then finally, print the new string at the function call.

sentence=input("Enter the sentence: ")
position=int(input("Enter the position: "))
def remover(x,y):
    z=x[0]
    a=""
    for i in range(1, len(x)):
        if i%y!=0:
            z+=x[i]
        else:
            a+=x[i]
    return (z+a)
print(remover(sentence, position))


Task 15
You have been hired as an app developer for the company. The company plans to make an app for a grocery store where the user can order groceries and see the total amount to be paid in the cart section. To build this feature, you have to write a function that takes 2 arguments. They are: order_items (must be a list) location (default value should be set to "Dhanmondi") Your first task is to take a list of items from the user. Pass the list into the function parameter along with the optional location (Use default argument technique). (Also, no need to take location as input, pass this any value you want.)
Your second task is to implement the function. In the function, create a dictionary for the items shown in the table. Calculate the total price of the items passed as a list to the function. Additionally, add a delivery fee of 30 takas if the location is Dhanmondi. Otherwise, add a delivery fee of 70 takas. Finally, return the value and print it. Item Price(Tk) Rice 105 Potato 20 Chicken 250 Beef 510 Oil 85

user=int(input("Enter the number of items: "))
lst=[]
for i in range(user):
    item=input("Enter the item: ").lower()
    lst.append(item)
def cart(x, y="Dhanmondi"):
    total=30
    dic={"rice":105, "potato":20,"chicken":250, "beef" :510, "oil":85}
    for i in x:
        if i in dic.keys():
            total+=dic[i]
    if y!="Dhanmondi" :
        total+=40
    return total
print(cart(lst, "Mohakhali"))


Task 16
Write a function called splitting_money that takes an “amount” of money as an argument. Your first task is to take the “amount” of money as user input and pass the value to the function parameter. Your second task is to implement the function and calculate how that money can be split into 500, 100, 50, 20, 10, 5, 2, and 1 taka notes. Then print the returned value in the function call

user=int(input("Enter the amount: "))
def splitting_money(x):
    n500=n100=n50=n20=n10=n5=n2=n1=""
    if x//500!=0:
        n500=(f"500 Taka: {(x//500)} note(s)\n")
        x=x%500
    if x//100!=0:
        n100=(f"100 taka: {x//100} notes(s)\n")
        x=x%100
    if x//50!=0:
        n50=(f"50 taka: {x//50} notes(s)\n")
        x=x%50
    if x//20!=0:
        n20=(f"20 Taka: {x//20} notes(s)\n")
        x=x%20
    if x//10!=0:
        n10=(f"10 Taka: {x//10} notes(s)\n")
        x=x%10
    if x//5!=0:
        n5=(f"5 Taka: {x//5} notes(s)\n")
    if x//2!=0:
        n2=(f"2 Taka: {x//2} notes(s)\n")
    if x//1!=0:
        n1=(f"1 Taka: {x//1} notes(s)\n")
    return (n500+n100+n50+n20+n10+n5+n2+n1)
print(splitting_money(user))


Task 17
Write a function called remove_odd that takes a list of numbers that have both even and odd numbers mixed. Your function should remove all the odd numbers and return a compact list which only contains the even numbers. [Cannot use remove() or removed() for this task]

[ ]
  1
#Too easy
Task 18
Write a function which will take 4 arguments. They are: starting value(inclusive) ending value(exclusive) first divisor second divisor Your first task is to take these arguments as user input and pass these values to the function. Your second task is to implement the function and find all the numbers that are divisible by the first divisor or second divisor but not both from the starting value(inclusive) and ending value(exclusive). Add all the numbers that are divisible and finally return this value. Print the returned value in the function call.

start=int(input("Starting value: "))
end=int(input("Ending: "))
div1=int(input("divisior 1: "))
div2=int(input("Divisior 2: "))
def func(a,b,c,d):
    total=0
    for i in range(a,b):
        if i%c==0 and i%d==0:
            pass
        elif i%c==0 or i%d==0:
            total+=i
    return total
print(func(start, end , div1, div2))
Task 19
Write a python function which will take a string as an argument. Your first task is to take a string as user input and pass the value to the function. Your second task is to implement a function which will check whether all the alphabets from a to j (convert all the alphabets to lowercase) have appeared at least once in the given string or not. If all of these alphabets (a to j) appear at least once, then the result will be 5. If any one of the alphabets (a to j) is not in the given string, then the result will be 6. Return this result and print the statement, "PSG will win the Champions League this season" that many

user=input("Enter the string: ").lower()
def function(x):
    y="abcdefghij"
    result=5
    for i in y:
        if i in x:
            result=5
        else:
            result=6
            break

