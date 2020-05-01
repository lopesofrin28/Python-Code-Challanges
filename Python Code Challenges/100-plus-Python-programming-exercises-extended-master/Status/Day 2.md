# Question 4

### **Question:**

>***Write a program which accepts a sequence of comma-separated numbers from console and generate a list and a tuple which contains every number.Suppose the following input is supplied to the program:***

```
34,67,55,33,12,98
```


>***Then, the output should be:***
```
['34', '67', '55', '33', '12', '98']
('34', '67', '55', '33', '12', '98')
```

### Hints:
>***In case of input data being supplied to the question, it should be assumed to be a console input.tuple() method can convert list to tuple***

list1 = input().split(',')  # input is being taken as string and as it is string it has a built in
                          # method name split. ',' inside split function does split where it finds any ','
                          # and save the input as list in lst variable

tuple1 = tuple(list1)          # tuple method converts list to tuple

print(list1)
print(tuple1)

-----------------------

--------------------------
# Question 5

### **Question:**

>***Define a class which has at least two methods:***
>* ***getString: to get a string from console input*** 
>* ***printString: to print the string in upper case.*** 

>***Also please include simple test function to test the class methods.***

### Hints:
>***Use __init__ method to construct some parameters***

----------------------------------
class IOstring():
    def __init__(self):
        pass

    def getString(self):
        self.s = input()

    def printString(self):
        print(self.s.upper())

xx = IOstring()
xx.getString()
xx.printString()

--------------------------
# Question 6

### **Question:**

>***Write a program that calculates and prints the value according to the given formula:***

>***Q = Square root of [(2 * C * D)/H]***

>***Following are the fixed values of C and H:***

>***C is 50. H is 30.***

>***D is the variable whose values should be input to your program in a comma-separated sequence.For example
Let us assume the following comma separated input sequence is given to the program:***
```
100,150,180
```
>***The output of the program should be:***
```
18,22,24
```
--------------------------

### Hints:
>***If the output received is in decimal form, it should be rounded off to its nearest value (for example, if the output received is 26.0, it should be printed as 26).In case of input data being supplied to the question, it should be assumed to be a console input.***

from math import * # importing all math functions

C,H = 50,30

def calc(D):
    return sqrt((2*C*D)/H)

D = input().split(',')                     # splits in comma position and set up in list
D = [str(round(calc(int(i)))) for i in D]  # using comprehension method. It works in order of the previous code
print(",".join(D))

----------------------------


---------------------
# Question 7

### **Question:**

>***Write a program which takes 2 digits, X,Y as input and generates a 2-dimensional array. The element value in the i-th row and j-th column of the array should be i * j.***

>***Note: i=0,1.., X-1; j=0,1,¡­Y-1. Suppose the following inputs are given to the program: 3,5***

>***Then, the output of the program should be:***
```
[[0, 0, 0, 0, 0], [0, 1, 2, 3, 4], [0, 2, 4, 6, 8]]
```

-------------------------------

### Hints:
>***Note: In case of input data being supplied to the question, it should be assumed to be a console input in a comma-separated form.***

------------------
x,y = map(int,input().split(','))
list1 = []

for i in range(x):
    tmp = []
    for j in range(y):     
        tmp.append(i*j)
    list1.append(tmp)
    
print(list1)

---------------------------
# Question 8

### **Question:**

>***Write a program that accepts a comma separated sequence of words as input and prints the words in a comma-separated sequence after sorting them alphabetically.***

>***Suppose the following input is supplied to the program:***
```
without,hello,bag,world
```
>***Then, the output should be:***
```
bag,hello,without,world
```
n=input().split(",")
n.sort()
print(",".join(n))

----------------------
### Hints:
>***In case of input data being supplied to the question, it should be assumed to be a console input.***


-------------------------------
# Question 9

### **Question:**

>***Write a program that accepts sequence of lines as input and prints the lines after making all characters in the sentence capitalized.***

>***Suppose the following input is supplied to the program:***
```
Hello world
Practice makes perfect
```
>***Then, the output should be:***
```
HELLO WORLD
PRACTICE MAKES PERFECT
```

----------------------
### Hints:
>***In case of input data being supplied to the question, it should be assumed to be a console input.***

-------------------
list1 = []

while True:
    x = input()
    if len(x)==0:
        break;
    list1.append(x.upper())

for line in list1:
    print(line)
    
--------------------


