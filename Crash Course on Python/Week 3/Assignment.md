# Module 3 Graded Assessment

### 1. Fill in the blanks to print the numbers from 15 to 5, counting down by fives.

    number = 15 # Initialize the variable
    while number >= 5: # Complete the while loop condition
       print(number, end=" ")
       number -= 5 # Increment the variable

### 2. Find and correct the error in the for loop below.  The loop should check each number from 1 to 5 and identify if the number is odd or even.  

    for number in range(1, 6):
    if number % 2 == 0:
        print("even")
    else:
        print("odd")


### 3. Complete the function digits(n) that returns how many digits the number has. For example: 25 has 2 digits and 144 has 3 digits. Tip: you can figure out the digits of a number by dividing it by 10 once per digit until there are no digits left.

    def digits(n):
        count = 0
        if n == 0:
        return 1
        while (n > 0):
            count += 1
            n = n // 10
        return count
        
    print(digits(25))   # Should print 2
    print(digits(144))  # Should print 3
    print(digits(1000)) # Should print 4
    print(digits(0))    # Should print 1

### 4. This function prints out a multiplication table (where each number is the result of multiplying the first number of its row by the number at the top of its column). Fill in the blanks so that calling multiplication_table(1, 3) will print out:
```
    1 2 3
    2 4 6
    3 6 9
```

    def multiplication_table(start, stop):
        for x in range(start,stop+1):
            for y in range(start,stop+1):
                print(str(x*y), end=" ")
            print()

    multiplication_table(1, 3)
    # Should print the multiplication table shown above

### 5. The counter function counts down from start to stop when start is bigger than stop, and counts up from start to stop otherwise. Fill in the blanks to make this work correctly.

    def counter(start, stop):
        x = start
        if start > stop:
            return_string = "Counting down: "
            while x >= stop:
                return_string += str(x)
                if x != stop:
                    return_string += ","
                x -= 1
        else:
            return_string = "Counting up: "
            while x <= stop:
                return_string += str(x)
                if x != stop:
                    return_string += ","
                x += 1
        return return_string

    print(counter(1, 10)) # Should be "Counting up: 1,2,3,4,5,6,7,8,9,10"
    print(counter(2, 1)) # Should be "Counting down: 2,1"
    print(counter(5, 5)) # Should be "Counting up: 5"

### 6. Fill in the blanks to complete the “odd_numbers” function. This function should return a space-separated string of all odd positive numbers, up to and including the “maximum” variable that's passed into the function. Complete the for loop so that a function call like “odd_numbers(6)” will return the numbers “1 3 5”.

   def odd_numbers(maximum):
    
    return_string = "" # Initializes variable as a string

    # Complete the for loop with a range that includes all 
    # odd numbers up to and including the "maximum" value.
    for x in range(1, maximum+1, 2): 

        # Complete the body of the loop by appending the odd number
        # followed by a space to the "return_string" variable.
        return_string += str(x) + " "
    # This .strip command will remove the final " " space 
    # at the end of the "return_string".
    return return_string.strip()


    print(odd_numbers(6))  # Should be 1 3 5
    print(odd_numbers(10)) # Should be 1 3 5 7 9
    print(odd_numbers(1))  # Should be 1
    print(odd_numbers(3))  # Should be 1 3
    print(odd_numbers(0))  # No numbers displayed



### 7. The following code is supposed to add together all numbers from x to 10.  The code is returning an incorrect answer, what is the reason for this?
```
x = 1
sum = 5
while x <= 10:
    sum += x
    x += 1
print(sum)
# Should print 55
```

    The "sum" variable is initialized with the wrong value

### 8. What is the value of x at the end of the following code?
```
for x in range(1, 10, 3):
    print(x)
```
    7

### 9. What number is printed at the end of this code?
```
num1 = 0
num2 = 0

for x in range(5):
    num1 = x
    for y in range(14):
        num2 = y + 3

print(num1 + num2)
```
    20

### 10.The following code causes an infinite loop. Can you figure out what’s missing and how to fix it?
```
def count_numbers(first, last):
  # Loop through the numbers from first to last 
  x = first
  while x <= last:
    print(x)


count_numbers(2, 6)
```

    Variable x is not incremented