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
## use function for everyone

def prime(num):
    p=0
    for i in range(2,num):
        if (num%i==0):
            p=1
            print("not prime")
            break
    if (p==0):
            print("prime")
num=int(input("enter the value:"))
prime(num)


def prime_upto_number(num):
   
    for i in range(2,num+1):
        if (num%i!=0):
          primes.append(i)
primes=[]
num=int(input("enter the value:"))
prime_upto_number(num)
print(primes)











## 3.pattern
       *
     * * * 
   * * * * *
 * * * * * * *
* * * * * * * * *
n=5
for i in range(n):
    for j in range(i,n):
        print(" ",end=" ")
    for j in range(i):
        print("*",end=" ")
    for j in range(i+1):
        print("*",end=" ")
    print()


   * * * * * * * * *
     * * * * * * *
      * * * * *
        * * *
          *
 n= 5
for i in range(n):
    for j in range(i + 1):
        print(" ", end=" ")
    for j in range(i, n):
        print("*", end=" ")
    for j in range(i, n - 1):
        print("*", end=" ")
    print()

## 4.a)print whether the character is a letter or numeric digit or a special character 







          
