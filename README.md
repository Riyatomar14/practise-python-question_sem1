## 1.find the root of quadratic equation

print("general equation ax^2+bx+c:")
def roots(a,b,c):
    
    #find discriminant
    d=(b**2-(4*a*c))
    if (d>=0):
        #find roots
        sol1=(-b+(d**0.5)/(2*a))
        sol2=(-b-(d**0.5)/(2*a))
        return sol1,sol2
    else:
        #real part+imaginary part
        realpart=(-b/(2*a))
        imaginarypart=((d**0.5)/(2*a))
        sol1=complex(realpart,imaginarypart)
        sol2=complex(realpart,-imaginarypart)
        return sol1,sol2
        
a=float(input("enter the value of a:"))
b=float(input("enter the value of b:"))
c=float(input("enter the value of c:"))
A=roots(a,b,c)
print("roots",A)

## 2.a)check if n is prime
##  b)generate allprime numbers till n
## c) generate first n prime numbers

