# Module 4 Graded Assessment

### 1. Fill in the blank to complete the “first_character” function. This function should return the first character of any string passed in.  Complete the string operation needed in this function so that input like "Hello, World" will produce the output "H".

```
def first_character(string):
    # Complete the return statement using a string operation.
    return string[0] 


print(first_character("Hello, World")) # Should print H
print(first_character("Python is awesome")) # Should print P
print(first_character("Keep going")) # Should print K
```

### 2.Complete the for loop and string method needed in this function so that a function call like "alpha_length("This has 1 number in it")" will return the output "17". This function should:

### 1. accept a string through the parameters of the function;

### 2. iterate over the characters in the string;

### 3. determine if each character is a letter (counting only alphabetic characters; numbers, punctuation, and spaces should be ignored);

### 4. increment the counter;

### 5. return the count of letters in the string.

```
def alpha_length(string):
    character = ""
    count_alpha = 0
    # Complete the for loop sequence to iterate over "string".
    for char in string: 
        # Complete the if-statement using a string method. 
        if char.isalpha():
            count_alpha += 1  
    return count_alpha
 
print(alpha_length("This has 1 number in it")) # Should print 17
print(alpha_length("Thisisallletters")) # Should print 16
print(alpha_length("This one has punctuation!")) # Should print 21
```

### 3. Consider the following scenario about using Python lists: 

### A professor gave his two assistants, Aniyah and Imani, the task of keeping an attendance list of students in the order they arrived in the classroom. Aniyah was the first one to note which students arrived, and then Imani took over. After class, they each entered their lists into the computer and emailed them to the professor. The professor wants to combine the two lists into one and sort it in alphabetical order. 

### Complete the code by combining the two lists into one and then sorting the new list. This function should:

### 1. accept two lists through the function’s parameters;,

### 2. combine the two lists;

### 3. sort the combined list in alphabetical order;

### 4. return the new list. 

```
def alphabetize_lists(list1, list2):
    new_list = [] # Initialize a new list.
    new_list.extend(list1) # Combine the lists.
    new_list.extend(list2)
    new_list.sort() # Sort the combined lists.
    return new_list # Assign the sorted combined list to the "new_list".

Aniyahs_list = ["Jacomo", "Emma", "Uli", "Nia", "Imani"]
Imanis_list = ["Loik", "Gabriel", "Ahmed", "Soraya"]

print(alphabetize_lists(Aniyahs_list, Imanis_list))
# Should print: ['Ahmed', 'Emma', 'Gabriel', 'Imani', 'Jacomo', 'Loik', 'Nia', 'Soraya', 'Uli']

```
### 4. Fill in the blank to complete the “squares” function. This function should use a list comprehension to create a list of squared numbers (using either the expression n*n or n**2). The function receives two variables and should return the list of squares that occur between the “start” and “end” variables inclusively (meaning the range should include both the “start” and “end” values). Complete the list comprehension in this function so that input like “squares(2, 3)” will produce the output “[4, 9]”.

```
def squares(start, end):
    return [  n*n for n in range(start,end+1) ] # Create the required list comprehension.


print(squares(2, 3)) # Should print [4, 9]
print(squares(1, 5)) # Should print [1, 4, 9, 16, 25]
print(squares(0, 10)) # Should print [0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

### 5. Fill in the blanks to complete the “car_listing” function. This function accepts a “car_prices” dictionary. It should iterate through the keys (car models) and values (car prices) in that dictionary. For each item pair, the function should format a string so that a dictionary entry like ““Kia Soul“:19000” will print "A Kia Soul costs 19000 dollars". Each new string should appear on its own line.

```
def car_listing(car_prices):
  result = ""
  for car, cost in car_prices.items():
    result += "{} costs {} dollars".format(car, cost) + "\n"
  return result

print(car_listing({"Kia Soul":19000, "Lamborghini Diablo":55000, "Ford Fiesta":13000, "Toyota Prius":24000}))
```

### 6. Consider the following scenario about using Python dictionaries: 

### Tessa and Rick are hosting a party. Together, they sent out invitations, and collected the responses in a dictionary, with names of their friends and the number of guests each friend will be bringing. 

###  Complete the function so that the “check_guests” function retrieves the number of guests (value)  the specified friend “guest” (key) is bringing. This function should:

### 1. accept a dictionary “guest_list” and a key “guest” variable passed through the function parameters;

### 2. print the values associated with the key variable.

```
def check_guests(guest_list, guest):
    if guest in guest_list:
        return guest_list[guest] # Return the value for the given key
    else:
        return "Guest not found" # If guest is not found in the dictionary, return this message

guest_list = { "Adam":3, "Camila":3, "David":5, "Jamal":3, "Charley":2, "Titus":1, "Raj":6, "Noemi":1, "Sakira":3, "Chidi":5}

print(check_guests(guest_list, "Adam")) # Should print 3
print(check_guests(guest_list, "Sakira")) # Should print 3
print(check_guests(guest_list, "Charley")) # Should print 2
print(check_guests(guest_list, "Nia")) # Should print "Guest not found"

```

### 7. Use a dictionary to count the frequency of numbers in the given “text” string. Only numbers should be counted. Do not count blank spaces, letters, or punctuation. Complete the function so that input like "1001000111101" will return a dictionary that holds the count of each number that occurs in the string  {'1': 7, '0': 6}. This function should: 

### 1. accept a string “text” variable through the function’s parameters;

### 2. initialize an new dictionary;

### 3. iterate over each text character to check if the character is a number’

### 4. count the frequency of numbers in the input string, ignoring all other characters;

### 5. populate the new dictionary with the numbers as keys, ensuring each key is unique, and assign the value for each key with the count of that number;

### 6. return the new dictionary.
```
def count_numbers(text):
  # Initialize a new dictionary.
  result = {} 
  # Complete the for loop to iterate through each "text" character.
  for letter in text:
    # Complete the if-statement using a string method to check if the
    # character is a number.
    if letter.isnumeric():
      # Complete the if-statement using a logical operator to check if 
      # the number is not already in the dictionary.
      if letter in result:
        # Use a dictionary operation to increment the number count value 
        # for the existing key.
        result[letter] += 1
      else:
        # Use a dictionary operation to add the number as a key
        # and set the initial count value to one.
        result[letter] = 1
  return result

print(count_numbers("1001000111101"))
# Should be {'1': 7, '0': 6}

print(count_numbers("Math is fun! 2+2=4"))
# Should be {'2': 2, '4': 1}

print(count_numbers("This is a sentence."))
# Should be {}

print(count_numbers("55 North Center Drive"))
# Should be {'5': 2}

```

### 8. What do the following commands return when car_make = "Lamborghini"?

```
print(car_make[3:-5])
print(car_make[-4:])
print(car_make[:7])
```

    
    bor, hini, Lamborg

### 9. What does the list "colors" contain after these commands are executed?

```
colors = ["red", "white", "blue"]
colors.insert(2, "yellow")
```

    ['red', 'white', 'yellow', 'blue']

### 10. What do the following commands return?

```
host_addresses = {"router": "192.168.1.1", "localhost": "127.0.0.1", "google": "8.8.8.8"}
host_addresses.keys()
```

    ['router', 'localhost', 'google']