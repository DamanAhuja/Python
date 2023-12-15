# Practical 1
''' bash
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
'''
