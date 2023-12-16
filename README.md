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






def is_prime(num):
    """Check if a number is prime."""
    if num < 2:
        return False
    for i in range(2,num):
        if num % i == 0:
            return False
    return True

def generate_primes(n):
    """Generate the first n prime numbers."""
    primes = []
    current_num = 2  # Start with the first prime number
    while len(primes) < n:
        if is_prime(current_num):
            primes.append(current_num)
        current_num += 1
    return primes


num_primes = int(input("Enter the number of prime numbers to generate: "))


result = generate_primes(num_primes)
print(f"The first {num_primes} prime numbers are: {result}")


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

char = input("Enter a character: ")

# Check if the character is a letter
if 'a' <= char <= 'z' or 'A' <= char <= 'Z':
    print(f"{char} is a letter.")
# Check if the character is a numeric digit
elif '0' <= char <= '9':
    print(f"{char} is a numeric digit.")
# If it's not a letter or numeric digit, consider it a special character
else:
    print(f"{char} is a special character.")


    
## b) if the character is a letter,print whether the letter is uppercase or lowercase
char = input("Enter a character: ")

# Check if the character is a letter
if 'a' <= char <= 'z' or 'A' <= char <= 'Z':
    print(f"{char} is a letter.")



## c)if character is numeric digit ,print its name in text(eg if input is 9, output is NINE.

# Accept a character from the user
char = input("Enter a character: ")

# Check if the character is a numeric digit
if '0' <= char <= '9':
    # Dictionary mapping numeric digits to their names
    digit_names = {'0': 'ZERO', '1': 'ONE', '2': 'TWO', '3': 'THREE', '4': 'FOUR', '5': 'FIVE', '6': 'SIX', '7': 'SEVEN', '8': 'EIGHT', '9': 'NINE'}

    # Print the name of the numeric digit
    print(f"{char} is {digit_names[char]}.")
else:
    print(f"{char} is not a numeric digit.")

## 5.operation on a string 

## a) find the frequency of a character on a string 
    
# Accept a string from the user
input_string = input("Enter a string: ")

# Accept a character whose frequency needs to be checked
char_to_find = input("Enter the character to find its frequency: ")

# Initialize a counter variable
char_frequency = 0

# Iterate through the string
for char in input_string:
    # Check if the current character matches the one we're looking for
    if char == char_to_find:
        char_frequency += 1

# Print the result
print(f"The frequency of '{char_to_find}' in the string is: {char_frequency}")

## b)replace the character by another character in a string

# Accept a string from the user
input_string = input("Enter a string: ")

# Accept the character to be replaced
char_to_replace = input("Enter the character to be replaced: ")

# Accept the character to replace with
replacement_char = input("Enter the character to replace with: ")

# Initialize an empty string to store the result
result_string = ""

# Iterate through the input string
for char in input_string:
    # Check if the current character is the one to be replaced
    if char == char_to_replace:
        # If yes, append the replacement character to the result string
        result_string += replacement_char
    else:
        # If no, simply append the current character to the result string
        result_string += char

# Print the resulting string
print(f"The modified string is: {result_string}")


or  

a=input("enter the string")
b=input("you want replace")
c=input("char on replace ")
result=""
for char in a:
    if char==b:
        result+=c
        
    else:
        result+=char
print(f"The modified string is: {result}")



## c)remove the first occurence of the string
n=input("enter the string:")
a=input("enter the char you want to remove:")
result=" "
for i in range(len(n)):
    if n[i]==a:
       d=n[0:i]
       e=n[i+1:]
       result=d+e
       break
if result=="":
    print(a,"it is a empty string")
else:
    print("removing the first occurence of ",a, "in string",result)


## d) remove all occurence of a character from a string

n=input("enter the string:")
a=input("enter the char you want to remove:")

while(a in n):
    len(n)
    for i in range(len(n)):
      if n[i]==a:
        d=n[0:i]
        e=n[i+1:]
        n=d+e
        break
   
print(n)

## 6. WAP to swap the first n character of two strings
def swap_first_n_chars(str1, str2, n):
    if n > min(len(str1), len(str2)):
        print("Error: n is greater than the length of one or both strings.")
        return
    
    # Swap first n characters
    swapped_str1 = str2[:n] + str1[n:]
    swapped_str2 = str1[:n] + str2[n:]
    
    return swapped_str1, swapped_str2

# Example usage
string1 = "hello"
string2 = "world"
n = 2

result1, result2 = swap_first_n_chars(string1, string2, n)

print(f"After swapping first {n} characters:")
print("String 1:", result1)
print("String 2:", result2)

## 7. Write a function that accepts two strings and returns the indices of all the occurrences of the second string in the first string as a list. If the second string is not present in the first string then it should return -1
def find_occurrences(main_str, sub_str):
    occurrences = []
    main_len, sub_len = len(main_str), len(sub_str)

    if sub_len > main_len:
        return -1  # Second string cannot be present in the first string if it's longer

    for i in range(main_len - sub_len + 1):
        if main_str[i:i + sub_len] == sub_str:
            occurrences.append(i)

    if not occurrences:
        return -1  # Return -1 if the second string is not found
    else:
        return occurrences

# Example usage
string1 = "abababab"
string2 = "aba"

result = find_occurrences(string1, string2)

if result == -1:
    print(f"'{string2}' not found in '{string1}'")
else:
    print(f"Indices of occurrences of '{string2}' in '{string1}': {result}")

    
## 8.WAP to create a list of the cubes of only the even integers appearing in the input list (may
have elements of other types also) using the following:
a. 'for' loop
b. list comprehension

a)

def cubes_of_even_numbers_for_loop(input_list):
    result = []
    for element in input_list:
        if type(element) == int and element % 2 == 0:
            result.append(element**3)
    return result

# Example Usage:
input_list = [1, 2, 3, 4, 5, 'a', 6, 7, 8, 'b', 9, 10]
result_for_loop = cubes_of_even_numbers_for_loop(input_list)
print(result_for_loop)

          
b)

def cubes_of_even_numbers_list_comprehension(input_list):
    result = [x**3 for x in input_list if type(x) == int and x % 2 == 0]
    return result

# Example Usage:
input_list = [1, 2, 3, 4, 5, 'a', 6, 7, 8, 'b', 9, 10]
result_list_comprehension = cubes_of_even_numbers_list_comprehension(input_list)
print(result_list_comprehension)


## 9. WAP to read a file and
a. Print the total number of characters, words and lines in the file.
b. Calculate the frequency of each character in the file. Use a variable of dictionary
type to maintain the count.
c. Print the words in reverse order.
d. Copy even lines of the file to a file named ‘File1’ and odd lines to another file
named ‘File2.


def count_chars_words_lines(filename):
    total_chars = 0
    total_words = 0
    total_lines = 0
    char_frequency = {}
    reverse_words = []
    
    with open(filename, 'r') as file:
        for line_number, line in enumerate(file, start=1):
            total_lines += 1
            total_chars += len(line)
            
            words = line.split()
            total_words += len(words)
            
            for char in line:
                if char.isalpha():  # Consider only alphabetic characters
                    char_frequency[char] = char_frequency.get(char, 0) + 1
            
            reverse_words.extend(reversed(words))
            
            # Copy lines to 'File1' and 'File2'
            if line_number % 2 == 0:
                with open('File1', 'a') as file1:
                    file1.write(line)
            else:
                with open('File2', 'a') as file2:
                    file2.write(line)

    # Print results
    print(f"Total characters: {total_chars}")
    print(f"Total words: {total_words}")
    print(f"Total lines: {total_lines}")
    
    print("\nCharacter frequency:")
    for char, count in char_frequency.items():
        print(f"{char}: {count}")
    
    print("\nWords in reverse order:")
    print(" ".join(reverse_words))

# Example usage:
filename = 'your_file.txt'  # Replace with the actual file name
count_chars_words_lines(filename)

## 10.10. WAP to define a class Point with coordinates x and y as attributes. Create relevant methods and print the objects. Also define a method distance to calculate the distance between any two point objects.


class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def print_coordinates(self):
        print(f"Point coordinates: ({self.x}, {self.y})")

    def distance(self, other_point):
        # Calculate distance without using inbuilt functions
        dx = self.x - other_point.x
        dy = self.y - other_point.y
        distance_squared = dx ** 2 + dy ** 2
        distance = distance_squared ** 0.5
        return distance

# Example Usage:
point1 = Point(1, 2)
point2 = Point(4, 6)

# Print coordinates of the points
point1.print_coordinates()
point2.print_coordinates()

# Calculate and print the distance between two points
distance_between_points = point1.distance(point2)
print(f"Distance between points: {distance_between_points}")


## 11. Write a function that prints a dictionary where the keys are numbers between 1 and 5 and the values are cubes of the keys.

def create_cubes_dictionary():
    cubes_dict = {}
    for i in range(1, 6):
        cubes_dict[i] = i * i * i
    return cubes_dict

# Example Usage:
result_dict = create_cubes_dictionary()
print(result_dict)

## 12.Consider a tuple t1=(1, 2, 5, 7, 9, 2, 4, 6, 8, 10). WAP to perform following operations:
a) Print half the values of the tuple in one line and the other half in the next line.
b) Print another tuple whose values are even numbers in the given tuple.
c) Concatenate a tuple t2=(11,13,15) with t1.
d) Return maximum and minimum value from this tuple


def tuple_operations(t1):
    # a) Print half the values of the tuple in one line and the other half in the next line.
    half_length = len(t1) // 2
    print("Half of the values of the tuple in one line:", t1[:half_length])
    print("Other half of the values in the next line:", t1[half_length:])

    # b) Print another tuple whose values are even numbers in the given tuple.
    even_numbers_tuple = tuple(x for x in t1 if x % 2 == 0)
    print("Tuple with even numbers:", even_numbers_tuple)

    # c) Concatenate a tuple t2=(11, 13, 15) with t1.
    t2 = (11, 13, 15)
    concatenated_tuple = t1 + t2
    print("Concatenated tuple:", concatenated_tuple)

    # d) Return maximum and minimum value from this tuple.

# Calculate maximum and minimum without using built-in functions
    max_value = t1[0]
    min_value = t1[0]

    for element in t1:
        if element > max_value:
            max_value = element
        if element < min_value:
            min_value = element

# Print maximum and minimum values
    print("Maximum value:", max_value)
    print("Minimum value:", min_value)

t1=(11,13,15)
# Perform operations and print results
result = tuple_operations(t1)
print("\nMaximum and Minimum values from the tuple:", result)


## 13.WAP to accept a name from a user. Raise and handle appropriate exception(s) if the text entered by the user contains digits and/or special characters.


def validate_name(name):
    for char in name:
        if not char.isalpha() and char != ' ':
            raise ValueError("Invalid name! Name should contain only letters and spaces.")

try:
    # Accept a name from the user
    user_input = input("Enter your name: ")
    
    # Validate the name
    validate_name(user_input)
    
    # If the name is valid, print a success message
    print("Name entered:", user_input)

except ValueError as e:
    # Handle the exception and print the error message
    print("Error:", e)




