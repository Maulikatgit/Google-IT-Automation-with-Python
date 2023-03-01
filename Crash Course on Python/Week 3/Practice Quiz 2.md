# Practice Quiz: For Loops

### 1. How are while loops and for loops different in Python?

    While loops iterate while a condition is true, for loops iterate through a sequence of elements.

### 2. Which option would fix this for loop to print the numbers 12, 18, 24, 30, 36? 
####  for n in range(6,18,3):
####    print(n*2)

    for n in range(6,18+1,3):
    print(n*2)

### 3. Which for loops will print all even numbers from 0 to 18? Select all that apply.

    1 >> for n in range(19):
         if n % 2 == 0:
         print(n)

    2 >> for n in range(10):
         print(n+n)

### 4. Write a script that prints the first 10 cube numbers (x**3), starting with x=1 and ending with x=10.

    for x in range(1,11):
    print(x**3)

### 5. Write a script that prints the multiples of 7 between 0 and 100. Print one multiple per line and avoid printing any numbers that aren't multiples of 7. Remember that 0 is also a multiple of 7.

    for n in range(0,101):
        if n == 0 or n % 7 == 0:
            print(n)
