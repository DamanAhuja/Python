# Practical 1
``` bash
a=int(input("Enter the coefficient of x^2: "))
b=int(input("Enter the coefficient of x: "))
c=int(input("Enter the constant: "))
print("Your Equation is:")
print(a,"x^2 + ",b,"x +",c)
d=b**2-4*a*c
e=d**(1/2)
if d>=0:
    x=(-b+e)/(2*a)
    y=(-b-e)/(2*a)
    print("Roots are: ")
    print(x ,"  ",y)
else:
    print("Reals roots does not exist")
```
# Practical 2
``` bash
# Check Prime
n=int(input("Enter a number: "))
for i in range(2,n):
    if n%i==0:
        print(n," Is not Prime")
        break
else:
    print(n," Is Prime")
# Prime Numbers less than n 
print("Prime Numbers less than ",n," are:")
for k in range(2,n):
    for j in range(2,k):
        if k%j==0:
            break
    else:
        print(k)
# First n prime numbers
c=0
l=2
print("First ",n," prime numbers are: ")
while (c<n):
    for j in range (2,l):
        if l%j==0:
            break
    else:
        print(l)
        c+=1
    l+=1
```
# Practical 3
``` bash
# Taking Input
n=int(input("Layers of pyramid: "))
# Pyramid
print("Pyramid: ")
c=1
d=n-1
for i in range(n):
    print(d*" ",end='')
    print(c*"*")
    c+=2
    d-=1
# Reverse Pyramid
print("Reverse Pyramid: ")
c=2*n-1
d=0
for i in range(n):
    print(d*" ",end='')
    print(c*"*")
    d+=1
    c-=2
```
# Practical 4
``` bash
a=input("Enter a Character: ")
if a.isnumeric():
    print("Numeric")
elif a.isalpha():
    print("Alphabet")
    if a.isupper():
        print("Upper Case")
    else:
        print("Lower Case")
else:
    print("Special Character")
```
# Practical 5
``` bash
a=str(input("Enter a string: "))
# Finding Frequency
b=str(input("Enter the character to find frequency: "))
print(a.count(b))
# Replacing Character
d=input("Enter the character you want to replace: ")
e=input("Enter the new character: ")
a=a.replace(d,e)
print(a)
# Removing First Occurence of a character
g=input("Enter the character you want to remove (first occurence): ")
a=a.replace(g,"",1)
print(a)
# Removing all Occurences of a character
i=input("Enter the character you want to remove: ")
a=a.replace(i,"",)
print(a)
```
# Practical 6
``` bash
a=str(input("First string: "))
b=str(input("Second string: "))
n=int(input("Enter number of elements: "))
x=a[0:n]
a=a.replace(a[0:n],b[0:n])
b=b.replace(b[0:n],x)
print(a)
print(b)
```
# Practical 7
``` bash
a=str(input("First string: "))
b=str(input("Second string: "))
c=[]
d=0
if b in a:
    for i in a:
        if i==b:
           c.append(d)
        d+=1
    print(c)
else:
    print("-1")
```
# Practical 8
``` bash
a=[]
n=int(input("Number of elements: "))
for i in range (n):
    f=input("Enter Element: ")
    a.append(f)
b=[]
for i in a:
    if i.isnumeric():
        d=int(i)
        if d%2==0:
            b.append(d**3)
print(b)
```
# Practical 9
``` bash
f=open("C:\\Users\\daman\\Desktop\\a.txt",'r')
d=f.read()
print("Characters= ",len(d))
a=d.split(" ")
print("Words= ",len(a))
b=d.split("\n")
print("Lines= ",len(b))
dic={}
c=[]
for i in d:
    if i not in c:
        c.append(i)
for i in c:
    q=d.count(i)
    dic[i]=q
print(dic)
f.close()
g=open("C:\\Users\\daman\\Desktop\\a.txt",'r')
data=g.readlines()
for i in data:
    print(i[::-1])
f2=open("C:\\Users\\daman\\Desktop\\b.txt",'w+')
f3=open("C:\\Users\\daman\\Desktop\\c.txt",'w+')
count=0
for i in g:
    if count%2==0:
        f2.write(i)
    else:
        f3.write(i)
    count+=1
d1=f2.readlines()
for i in d1:
    print(i)
d2=f3.readlines()
for i in d2:
    print(i)
g.close()
f2.close()
f3.close()
```
# Practical 10
``` bash
import math

class Point:
    def __init__(self,x,y):
        self.x = x
        self.y = y

    def display(self):
        print(f"Point({self.x}, {self.y})")

    def distance(self, other_points):
        distance = math.sqrt((self.x-other_points.x)**2 + (self.y - other_points.y)**2)
        return distance

point1 = Point(3,4)
point2 = Point(6,8)

point1.display()
point2.display()
distance = point1.distance(point2)
print("The distance between Point({}, {}) and Point({}, {}) is: {}".format(point1.x,point1.y,point2.x,point2.y,distance))
```
# Practical 11
``` bash
def Dict():
    d={}
    d[1]=1**3
    d[2]=2**3
    d[3]=3**3
    d[4]=4**3
    d[5]=5**3
    print(d)
Dict()
```
# Practical 12
``` bash
t1=(1,2,5,7,9,2,4,6,8,10)
a=int(len(t1)/2)
for i in t1[:a]:
    print(i,end='')
print("\n")
for i in t1[a:]:
    print(i,end='')
print("\n")
t=[]
for i in t1:
    if int(i)%2==0:
        t.append(i)
print(tuple(t))
t2=(11,13,15)
t1=t1+t2
print(t1)
c=0
for i in t1:
    if int(i)>c:
        c=i
print("Max= ",c)
d=int(t1[0])
for i in t1:
    if int(i)<d:
        d=i
print("Min= ",d)
```
# Practical 13
``` bash
def handleName(name):
    try:
        if any(char.isdigit() for char in name):
            raise ValueError("Name can't contain digits")
        elif not name.isalpha():
            raise ValueError("Name con't contain spechil character")
        print("Name Entered: ",name)
    except ValueError as e:
        print("Error",e)

name = input("Enter your name: ")
handleName(name)
```
