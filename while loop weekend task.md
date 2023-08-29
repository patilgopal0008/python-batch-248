1)To the Power of _____
Create a function that takes a base number and an exponent number and returns the calculation.

Examples
calculate_exponent(5, 5) ➞ 3125

calculate_exponent(10, 10) ➞ 10000000000

calculate_exponent(3, 3) ➞ 27


```python
base,exp = int(input('enter a value: ')),int(input('enter exponent value: '))
result = base
i = 1
while i<exp:
    result*= base
    exp-=1
    i+=1
print(result)
    
```

    enter a value: 3
    enter exponent value: 2
    9
    

2)Find the Largest Number in a List
Create a function that takes a list of numbers. Return the largest number in the list.

Examples
findLargestNum([4, 5, 1, 3]) ➞ 5

findLargestNum([300, 200, 600, 150]) ➞ 600

findLargestNum([1000, 1001, 857, 1]) ➞ 1001


```python
numbers = [12, 45, 6, 78, 23, 56]
a = numbers[0] #let num[0] be the largest
i = 1 
while i < len(numbers):
    if numbers[i] > a:
        a = numbers[i]
    i += 1
print("The largest number is:", a)

```

    The largest number is: 78
    

3)Find the Smallest Number in a List
Create a function that takes a list of numbers and returns the smallest number in the list.

Examples
find_smallest_num([34, 15, 88, 2]) ➞ 2

find_smallest_num([34, -345, -1, 100]) ➞ -345

find_smallest_num([-76, 1.345, 1, 0]) ➞ -76

find_smallest_num([0.4356, 0.8795, 0.5435, -0.9999]) ➞ -0.9999

find_smallest_num([7, 7, 7]) ➞ 7


```python
numbers = [12, 45, 6, 78, 23, 56]
a = numbers[0] #let be the smallest
i = 1
while i < len(numbers):
    if numbers[i] < a:
        a = numbers[i]
    i += 1
print("The smallest number is:", a)

```

    The smallest number is: 6
    

4)Difference of Max and Min Numbers in List
Create a function that takes a list and returns the difference between the biggest and smallest numbers.
Examples
difference_max_min([10, 4, 1, 4, -10, -50, 32, 21]) ➞ 82
Smallest number is -50, biggest is 32.

difference_max_min([44, 32, 86, 19]) ➞ 67
 Smallest number is 19, biggest is 86.


```python
numbers = [12, 45, 6, 78, 23, 56]
a = numbers[0] #let be largest
b = numbers[0] #be amallest
i = 1
while i < len(numbers):
    if numbers[i] > a:
        a = numbers[i]
    elif numbers[i] < b:
        b = numbers[i]
    i += 1
j = a-b
print(j)
```

    72
    

5)Get the Sum of All List Elements
Create a function that takes a list and returns the sum of all numbers in the list.

Examples
get_sum_of_elements([2, 7, 4]) ➞ 13

get_sum_of_elements([45, 3, 0]) ➞ 48

get_sum_of_elements([-2, 84, 23]) ➞ 105


```python
x = [12, 45, 6, 78, 23, 56]
i = 0
sum = 0
while i<len(x):
    sum+=x[i]
    i+=1
print(sum)
```

    220
    

6)Convert Number to String of Dashes
Create a function that takes a number (from 1 - 60) and returns a corresponding string of hyphens.

Examples
num_to_dashes(1) ➞ "-"

num_to_dashes(5) ➞ "-----"

num_to_dashes(3) ➞ "---"


```python
x = int(input('enter a value: '))
if x < 1 or x > 60:
    print('x is not in range' )
result = ''
i = 0
while i<x:
    result+='-'
    i+=1
print(result)
    
    

```

    enter a value: 5
    -----
    

7)Edaaaaabit
Write a function that takes an integer and returns a string with the given number of "a"s in Edabit.

Examples
how_many_times(5) ➞ "Edaaaaabit"

how_many_times(0) ➞ "Edbit"

how_many_times(12) ➞ "Edaaaaaaaaaaaabit"


```python
x = int(input('enter a value: '))
if x < 0:
    print('enter a positive num')
result = ''
i = 0
while i<x:
    result+='a'
    i+=1
y = 'ed'+result+'bit'
print(y)
```

    enter a value: 4
    edaaaabit
    

8)Check if All Values Are True
Create a function that returns True if all parameters are truthy, and False otherwise.

Examples
all_truthy(True, True, True) ➞ True

all_truthy(True, False, True) ➞ False

all_truthy(5, 4, 3, 2, 1, 0) ➞ False


```python
a = (True,0,'hello',1)
i = 0
while i < len(a):
    if not a[i]:
        result = False
        break
    i+= 1
else:
    result = True

print(result)
    

```

    False
    

9)Buggy Code (Part 5)
Mubashir created an infinite loop! Help him by fixing the code in the code tab to pass this challenge. Look at the examples below to get an idea of what the function should do.

Examples
print_list(1) ➞ [1]

print_list(3) ➞ [1, 2, 3]

print_list(6) ➞ [1, 2, 3, 4, 5, 6]


```python
x = int(input())
y = []
i = 1
while i<=x:
        y.append(i)
        i+=1
print(y)
```

    7
    [1, 2, 3, 4, 5, 6, 7]
    

10)Return Last Item
Create a function that returns the last value of the last item in a list or string.

Examples
last_ind([0, 4, 19, 34, 50, -9, 2]) ➞ 2

last_ind("The quick brown fox jumped over the lazy dog") ➞ "g"

last_ind([]) ➞ None


```python
x = [0, 4, 19, 34, 50, -9, 2]
i = 0
while i < len(x):
          y = x[i]
          i+=1
print(y)
          
```

    2
    


```python
x = "The quick brown fox jumped over the lazy dog"
i = 0
while i < len(x):
          y = x[i]
          i+=1
print(y)
          
```

    g
    

11)Destructuring Assignment (Ignoring Values)
You can assign variables from lists like this:

first, _ , last = [1, 2, 8]

first   = lst[0]

_   = ignores second value (2)

last   = lst[-1]

print(first) ➞ outputs 1
print(last) ➞ outputs 8
Using Destructuring Assignment (check the Resources tab), your task is to unpack the list writeyourcodehere into three variables, first, a variable to ignore all middle values and last.


```python
x = [1,2,3,4,5]
first,-,seond,three,four,five = x
    while i < len(x,y):
         x[i]=y[i]
```


      Cell In[22], line 2
        first,-,seond,three,four,five = x
               ^
    SyntaxError: invalid syntax
    


12) Century Crisis
Scientists have discovered that in four decades, the world will EXPLODE! It will also take three decades to make a spaceship to travel to a new planet that can hold the entire world population.

You must calculate the number of people there will be in three decades from now.

The variable P is the world population now.
Assume that every month, someone gives birth to more people nP.
Return the number of people there will be when the spaceship is complete.
Examples
future_people(256, 2) ➞ 976

future_people(3248, 6) ➞ 5408

future_people(5240, 3) ➞ 6320


```python
p = int(input())
np = int(input())
three_decades_months=36
months_passed = 0
y = p+np
while three_decades_months<months_passed:
    p+=np
    months_passed+=1
print(y)
```

    3248
    6
    3254
    

13)Word Numbers!
Create a function that returns a number, based on the string provided. Here is a list of all digits:

String	Number  
"one"	1  
"two"	2  
"three"	3  
"four"	4  
"five"	5  
"six"	6  
"seven"	7  
"eight"	8  
"nine"	9  
"zero"	0  
Examples
word("one") ➞ 1  

word("two") ➞ 2  

word("nine") ➞ 9


```python
digits = {"one":1,"two":2,"three":3,"four":4,"five":5,"six":6,"seven":7,"eight":8,"nine":9,"zero":0}
word = input("Enter a word: ")  

number = None
for digit_word, digit_value in digits.items():
    if word == digit_word:
        number = digit_value
        break

if number is not None:
    print(number)
else:
    print("Invalid word")
```

    Enter a word: one
    1
    

14)Count Instances of a Character in a String
Create a function that takes two strings as arguments and returns the number of times the first string (the single character) is found in the second string.

Examples
char_count("a", "edabit") ➞ 1

char_count("c", "Chamber of secrets") ➞ 1

char_count("b", "big fat bubble") ➞ 4


```python
char = input("Enter a character: ")  # Input the character
string = input("Enter a string: ")    # Input the string

count = 0
index = 0

while index < len(string):
    if string[index] == char:
        count += 1
    index += 1

print(count)

```

    Enter a character: hello
    Enter a string: h
    0
    

15)Find the Index
Create a function that takes a list and a string as arguments and returns the index of the string.

Examples
find_index(["hi", "edabit", "fgh", "abc"], "fgh") ➞ 2

find_index(["Red", "blue", "Blue", "Green"], "blue") ➞ 1

find_index(["a", "g", "y", "d"], "d") ➞ 3

find_index(["Pineapple", "Orange", "Grape", "Apple"], "Pineapple") ➞ 0


```python
x = ["hi", "edabit", "fgh", "abc"]  
y = "fgh"  

i = 0
while i < len(x):
    if x[i] == y:
        print(i)
        break
    i += 1
else:
    print("String not found in the list")
```

    2
    

16)Recreating a len() Function
Create a function which returns the length of a string, without using len().

Examples
length("Hello World") ➞ 11

length("Edabit") ➞ 6

length("wash your hands!") ➞ 16


```python
x = input("enter a string: ")
i = 0
l = 0
while i <len(x):
    i+=1
    l+=1
print(l)
    
```

    enter a string: hello
    5
    

17)Sum of Minimums
Create a function that takes a 2D list lst and returns the sum of the minimum value in each row.

Examples
sum_minimums([
  [1, 2, 3, 4, 5],
  [5, 6, 7, 8, 9],
  [20, 21, 34, 56, 100]
]) ➞ 26

minimum value of the first row is 1
 minimum value of the second row is 5
 minimum value of the third row is 20


```python
x = [
    [1,2,3],  #2d list
    [4,5,6],
    [7,8,9]
]
i = 0
j = 0 #be sum of min value
while i<len(x):
    y = min(x[i]) #y be min val
    i+=1
    j+=y
    
print(j)
```

    12
    

18)The Forbidden Letter
Given a letter and a list of words, return whether the letter does not appear in any of the words.

Examples
forbidden_letter("r", ["rock", "paper", "scissors"]) ➞ False

forbidden_letter("a", ["spoon", "fork", "knife"]) ➞ True

forbidden_letter("m", []) ➞ True


```python
letter = input("Enter a letter: ")  
words = ["rock", "paper", "scissors"]  

i = 0
while i < len(words):
    if letter in words[i]:
        print(True)
        break
    i+= 1
else:
    print(False)

```

    Enter a letter: s
    True
    

19)Factors of a Given Number
Create a function that finds each factor of a given number n. Your solution should return a list of the number(s) that meet this criteria.

Examples
find_factors(9) ➞ [1, 3, 9]
 9 has three factors 1, 3 and 9

find_factors(12) ➞ [1, 2, 3, 4, 6, 12]

find_factors(20) ➞ [1, 2, 4, 5, 10, 20]

find_factors(0) ➞ []
 0 has no factors


```python
x = int(input())
if x < 0:
    print('no factor')
else:
    y = []
    d = 1
    while d < x:
        if d%x==0:
            y.append(d)
            d+=1
print(y)
```

20)Reverse the Case
Given a string, create a function to reverse the case. All lower-cased letters should be upper-cased, and vice versa.

Examples
reverse_case("Happy Birthday") ➞ "hAPPY bIRTHDAY"

reverse_case("MANY THANKS") ➞ "many thanks"

reverse_case("sPoNtAnEoUs") ➞ "SpOnTaNeOuS"


```python
x = input("enter a string ")
i = 0
while i<len(x):
    y=x.swapcase()
    i+=1
print(y)
```

    enter a string hELLO
    Hello
    

21)Hashes and Pluses
Create a function that returns the number of hashes and pluses in a string.

Examples
hash_plus_count("###+") ➞ [3, 1]

hash_plus_count("##+++#") ➞ [3, 3]

hash_plus_count("#+++#+#++#") ➞ [4, 6]

hash_plus_count("") ➞ [0, 0]


```python
x = input('enter a string: ')
a = 0 #(#)count
b = 0 # + count
i = 0
while i<len(x):
    if x[i]=='#':
        a+=1
    elif x[i]=='+':
        b+=1
    i+=1
y = [a,b]
print(y)    
```

    enter a string: #++
    [1, 2]
    

22)Even and Odd Strings
Given a one word lowercase string txt, return another string such that even-indexed and odd-indexed characters are grouped and groups are space-separated.

Examples
even_odd_string("mubashir") ➞ "mbsi uahr"  
 Letters at even indexes = "mbsi"  
 Letters at odd indexes = "uahr"  
 Join both strings with a space  

even_odd_string("edabit") ➞ "eai dbt"  

even_odd_string("airforce") ➞ "aroc ifre"  


```python
x = input('enter a string: ')
y = "" #even char
z = "" #odd char
i = 0
while i < len(x):
    if i%2==0:
        y+=x[i]
    else:
        z+=x[i]
    i+=1
a = y+z
print(a)
    
```

    enter a string: heterigenous
    htrgnueeieos
    

23)Sum of the Odd Numbers
Create a function which returns the total of all odd numbers up to and including n. n will be given as an odd number.

Examples  
add_odd_to_n(5) ➞ 9  
  1 + 3 + 5 = 9  

add_odd_to_n(13) ➞ 49  

add_odd_to_n(47) ➞ 576  


```python
n = int(input("Enter an odd number: "))  
total = 0
num = 1

while num <= n:
    total += num
    num += 2  

print(total)
    
```

    Enter an odd number: 5
    9
    

24)Summing the Squares
Create a function that takes a number n and returns the sum of all square numbers up to and including n.

squares_sum(3) ➞ 14
# 1² + 2² + 3² =
# 1 + 4 + 9 =
# 14
Examples
squares_sum(3) ➞ 14

squares_sum(12) ➞ 650

squares_sum(13) ➞ 819


```python
n = int(input('enter a number: '))
total = 0
number = 1
while number <= n:
    total += number*number
    number+=1
print(total)
```

    enter a number: 13
    819
    

25)Negate the List of Numbers
Given a list of numbers, negate all elements contained within.

Negating a positive value -+n will return -n, because all +'s are removed.
Negating a negative value --n will return n, because the first - turns the second minus into a +.
Examples
negate([1, 2, 3, 4]) ➞ [-1, -2, -3, -4]

negate([-1, 2, -3, 4]) ➞ [1, -2, 3, -4]

negate([]) ➞ []


```python
numbers = [1, 2, 3, 4]  

index = 0
while index < len(numbers):
    numbers[index] = -numbers[index]
    index += 1

print(numbers)
```

    [-1, -2, -3, -4]
    

26)Additive Inverse
A number added with its additive inverse equals zero. Create a function that returns a list of additive inverses.

Examples
additive_inverse([5, -7, 8, 3]) ➞ [-5, 7, -8, -3]

additive_inverse([1, 1, 1, 1, 1]) ➞ [-1, -1, -1, -1, -1]

additive_inverse([-5, -25, 35]) ➞ [5, 25, -35]


```python
nums = [5, -7, 8, 3]  

inverses = []
index = 0

while index < len(nums):
    inverses.append(-nums[index])
    index += 1

print(inverses)
```

    [-5, 7, -8, -3]
    

27)Add a Consecutive List of Numbers
Write a function that takes the last number of a consecutive list of numbers and returns the total of all numbers up to and including it.

Examples
add_up_to(3) ➞ 6
# 1 + 2 + 3 = 6

add_up_to(10) ➞ 55
# 1 + 2 + 3 + ... + 10 = 55

add_up_to(7) ➞ 28
# 1 + 2 + 3 + ... + 7 = 28


```python
x = int(input('enter a num: '))
total = 0
num = 1
while num <=x:
    total+=num
num+=1
print(total)
```

    enter a num: 3
    

28)Give Me the Even Numbers
Create a function that takes two parameters (start, stop), and returns the sum of all even numbers in the range.

Examples
sum_even_nums_in_range(10, 20) ➞ 90
# 10, 12, 14, 16, 18, 20

sum_even_nums_in_range(51, 150) ➞ 5050

sum_even_nums_in_range(63, 97) ➞ 1360


```python
s,e = int(input('starting: ')),int(input('ending: '))
total = 0
i = s
while i<=e:
    i%2==0
    total+=i
    i+=1
print(total)
    
```

    starting: 1
    ending: 9
    45
    

29)Is the String a Palindrome?
A palindrome is a word that is identical forward and backwards.

mom
racecar
kayak
Given a word, create a function that checks whether it is a palindrome.

Examples
is_palindrome("mom") ➞ True

is_palindrome("scary") ➞ False

is_palindrome("reviver") ➞ True

is_palindrome("stressed") ➞ False


```python
word = input("Enter a word: ")
word = word.lower()  
is_palindrome = True
left = 0
right = len(word) - 1

while left < right:
    if word[left] != word[right]:
        is_palindrome = False
        break
    left += 1
    right -= 1

if is_palindrome:
    print("It's a palindrome!")
else:
    print("It's not a palindrome.")

```

    Enter a word: mom
    It's a palindrome!
    

30)List of Consecutive Numbers
Implement a function that returns a list containing all the consecutive numbers in ascendant order from the given value low up to the given value high (bounds included).

Examples
get_sequence(1, 5) ➞ [1, 2, 3, 4, 5]

get_sequence(98, 100) ➞ [98, 99, 100]

get_sequence(1000, 1000) ➞ [1000]


```python
s,e = int(input('starting num: ')),int(input('end num: '))
lst =[]
i = s
while i<=e:
    lst.append(i)
    i+=1
print(lst)
```

    starting num: 1
    end num: 9
    [1, 2, 3, 4, 5, 6, 7, 8, 9]
    

31)Find the Index (Part 1)
Create a function that finds the index of a given item.

Examples
search([1, 5, 3], 5) ➞ 1

search([9, 8, 3], 3) ➞ 2

search([1, 2, 3], 4) ➞ -1


```python
lst = [1, 5, 3]
item = 5
found_index = -1
index = 0

while index < len(lst):
    if lst[index] == item:
        found_index = index
        break
    index += 1

print(found_index)
```

    1
    

32)Count the Capital Letters
Given a string of letters, how many capital letters are there?

Examples
capital_letters("fvLzpxmgXSDrobbgMVrc") ➞ 6

capital_letters("JMZWCneOTFLWYwBWxyFw") ➞ 14

capital_letters("mqeytbbjwqemcdrdsyvq") ➞ 0


```python
s = "fvLzpxmgXSDrobbgMVrc"
count = 0
index = 0

while index < len(s):
    if s[index].isupper():
        count += 1
    index += 1

print(count)
```

    6
    

33)N Tables + 1
Create a function that takes a number num and returns the first 10 multiples of num with 1 added to it, separated by commas.

Examples
n_tables_plus_one(7) ➞ "8,15,22,29,36,43,50,57,64,71"

n_tables_plus_one(1) ➞ "2,3,4,5,6,7,8,9,10,11"

n_tables_plus_one(3) ➞ "4,7,10,13,16,19,22,25,28,31"


```python
num = int(input("Enter a number: "))
result = []
multiple = 1

while len(result) < 10:
    result.append(str(num * multiple + 1))
    multiple += 1

result_str = ",".join(result)
print(result_str)
```

    Enter a number: 7
    8,15,22,29,36,43,50,57,64,71
    

34)Reverse Coding Challenge #3
This is a reverse coding challenge. Normally you're given explicit directions with how to create a function. Here, you must generate your own function to satisfy the relationship between the inputs and outputs.

Your task is to create a function that, when fed the inputs below, produces the sample outputs shown.

Examples
[5, 7, 8, 2, 1], 2 ➞ [1, 1, 0, 0, 1]

[9, 8, 16, 47], 4 ➞ [1, 0, 0, 3]

[17, 11, 99, 55, 23, 1], 5 ➞ [2, 1, 4, 0, 3, 1]

[6, 1], 7 ➞ [6, 1]

[3, 2, 9], 3 ➞ [0, 2, 0]

[48, 22, 0, 19, 33, 100], 10 ➞ [8, 2, 0, 9, 3, 0]


```python

```

    [2, 3, 4, 1, 0]
    

35)Burglary Series (11): Say What
The insurance guy calls again. Apparently, they were informed by your spouse that some items were not stolen at all and you failed to mention this detail to them. This is a fraud attempt! You freeze and mumble something unintelligible. Find out what you said.

Given a dictionary, return a string that concatenates all the values and adds the 2nd key at the end. Make sure you keep an empty space between them but not at the beginning or end of the string. Look at the examples for a clearer picture.

Examples
{ 1: "Mommy", 2: "please", 3: "help" } ➞ "Mommy please help please"

{ 1: "Me", 2: "innocent", 3: "is" } ➞ "Me innocent is innocent"

{ 1: "Must", 2: "lawyer", 3: "call" } ➞ "Must lawyer call lawyer"


```python
data = {1: "Mommy", 2: "please", 3: "help"}
keys = list(data.keys())

index = 0
result = ""

while index < len(keys):
    result += data[keys[index]] + " "
    index += 1

result += data[keys[1]]

print(result)
```

    Mommy please help please
    

36)Word Endings
Create a function that adds a string ending to each member in a list.

Examples
add_ending(["clever", "meek", "hurried", "nice"], "ly")
➞ ["cleverly", "meekly", "hurriedly", "nicely"]

add_ending(["new", "pander", "scoop"], "er")
➞ ["newer", "panderer", "scooper"]

add_ending(["bend", "sharpen", "mean"], "ing")
➞ ["bending", "sharpening", "meaning"]


```python
words = ["clever", "meek", "hurried", "nice"]
ending = "ly"

index = 0

while index < len(words):
    words[index] += ending
    index += 1

print(words)
```

    ['cleverly', 'meekly', 'hurriedly', 'nicely']
    

37)Sum of Cubes
Create a function that takes a list of numbers and returns the sum of its cubes.

Examples
sum_of_cubes([1, 5, 9]) ➞ 855
# Since 1^3 + 5^3 + 9^3 = 1 + 125 + 729 = 855

sum_of_cubes([3, 4, 5]) ➞ 216

sum_of_cubes([2]) ➞ 8

sum_of_cubes([]) ➞ 0


```python
x = [1,5,9]
i =0
total = 0
while i<len(x):
    total+=x[i]*x[i]*x[i]
    i+=1
print(total)
    
```

    855
    

38)Minimum Removals to Make Sum Even
Create a function that returns the minimum number of elements removed to make the sum of all elements in a list even.

Examples
minimum_removals([1, 2, 3, 4, 5]) ➞ 1

minimum_removals([5, 7, 9, 11]) ➞ 0

minimum_removals([5, 7, 9, 12]) ➞ 1


```python
nums = [1, 2, 3, 4, 5]
total_sum = sum(nums) #using sum fun
r = 0
index = 0

while total_sum % 2 != 0:
    total_sum -= nums[index]
    r += 1
    index += 1

print(removals)

```

    1
    

39)Generate a Countdown of Numbers in a List
Create a function that takes a number as an argument and returns a list of numbers counting down from this number to zero.

Examples
countdown(5) ➞ [5, 4, 3, 2, 1, 0]

countdown(1) ➞ [1, 0]

countdown(0) ➞ [0]


```python
num = int(input("Enter a number: "))
countdown_list = []

while num >= 0:
    countdown_list.append(num)
    num -= 1

print(countdown_list)
```

    Enter a number: 9
    [9, 8, 7, 6, 5, 4, 3, 2, 1, 0]
    

40)Who's in First Place?
Create a function that takes a string road and returns the car that's in first place. The road will be made of "=", and cars will be represented by letters in the alphabet.

Examples
first_place("====b===O===e===U=A==") ➞ "A"

first_place("e==B=Fe") ➞ "e"

first_place("proeNeoOJGnfl") ➞ "l"


```python
road = "====b===O===e===U=A=="
index = 0
first_car = None

while index < len(road):
    if road[-index].isalpha():
        first_car = road[-index]
        break
    index += 1

print(first_car)
```

    A
    

41)Sum of Resistance in Series Circuits
When resistors are connected together in series, the same current passes through each resistor in the chain and the total resistance, RT, of the circuit must be equal to the sum of all the individual resistors added together. That is:

RT = R1 + R2 + R3 ...
Create a function that takes an array of values resistance that are connected in series, and calculates the total resistance of the circuit in ohms. The ohm is the standard unit of electrical resistance in the International System of Units ( SI ).

Examples
series_resistance([1, 5, 6, 3]) ➞ "15 ohms"

series_resistance([16, 3.5, 6]) ➞ "25.5 ohms"

series_resistance([0.5, 0.5]) ➞ "1.0 ohm"


```python
resistance = [1, 5, 6, 3]
total_resistance = 0
index = 0

while index < len(resistance):
    total_resistance += resistance[index]
    index += 1
print(f"{total_resistance}ohms")
```

    15ohms
    

42)Instant JAZZ
Create a function which concatenates the number 7 to the end of every chord in a list. Ignore all chords which already end with 7.

Examples
jazzify(["G", "F", "C"]) ➞ ["G7", "F7", "C7"]

jazzify(["Dm", "G", "E", "A"]) ➞ ["Dm7", "G7", "E7", "A7"]

jazzify(["F7", "E7", "A7", "Ab7", "Gm7", "C7"]) ➞ ["F7", "E7", "A7", "Ab7", "Gm7", "C7"]

jazzify([]) ➞ []


```python
words = ["G", "F", "C"]
ending = "7"

index = 0

while index < len(words):
    words[index] += ending
    index += 1

print(words)
```

    ['G7', 'F7', 'C7']
    

43)Convert a Number to Base-2
Create a function that returns a base-2 (binary) representation of a base-10 (decimal) string number. To convert is simple: ((2) means base-2 and (10) means base-10) 010101001(2) = 1 + 8 + 32 + 128.

Going from right to left, the value of the most right bit is 1, now from that every bit to the left will be x2 the value, value of an 8 bit binary numbers are (256, 128, 64, 32, 16, 8, 4, 2, 1).

Examples
binary(1) ➞ "1"
# 1*1 = 1

binary(5) ➞ "101"
# 1*1 + 1*4 = 5

binary(10) ➞ "1010"
# 1*2 + 1*8 = 10


```python
decimal_num = int(input("Enter a decimal number: "))
binary_str = ""

if decimal_num == 0:
    binary_str = "0"
else:
    while decimal_num > 0:
        remainder = decimal_num % 2
        binary_str = str(remainder) + binary_str
        decimal_num //= 2

print(binary_str)
```

    Enter a decimal number: 1
    1
    

44)How Many Vowels?
Create a function that takes a string and returns the number (count) of vowels contained within it.

Examples
count_vowels("Celebration") ➞ 5

count_vowels("Palm") ➞ 1

count_vowels("Prediction") ➞ 4


```python
s = "Celebration"
vowels = "aeiouAEIOU"  # List of vowels
count = 0
index = 0

while index < len(s):
    if s[index] in vowels:
        count += 1
    index += 1

print(count)
```

    5
    

45)Find the Odd Integer
Create a function that takes a list and finds the integer which appears an odd number of times.

Examples
find_odd([1, 1, 2, -2, 5, 2, 4, 4, -1, -2, 5]) ➞ -1

find_odd([20, 1, 1, 2, 2, 3, 3, 5, 5, 4, 20, 4, 5]) ➞ 5

find_odd([10]) ➞ 10


```python


```

46)Hamming Distance
Hamming distance is the number of characters that differ between two strings.

To illustrate:

String1: "abcbba"
String2: "abcbda"

Hamming Distance: 1 - "b" vs. "d" is the only difference.
Create a function that computes the hamming distance between two strings.

Examples
hamming_distance("abcde", "bcdef") ➞ 5

hamming_distance("abcde", "abcde") ➞ 0

hamming_distance("strong", "strung") ➞ 1


```python
str1,str2 = input(),input()
distance = 0
while str1 and str2:
    if str1[0] != str2[0]:
        distance += 1
        str1 = str1[1:]
        str2 = str2[1:]
print(distance)

```

    abcde
    bcdef
    5
    

47)Filter out Strings from an Array
Create a function that takes a list of non-negative integers and strings and return a new list without the strings.

Examples
filter_list([1, 2, "a", "b"]) ➞ [1, 2]

filter_list([1, "a", "b", 0, 15]) ➞ [1, 0, 15]

filter_list([1, 2, "aasf", "1", "123", 123]) ➞ [1, 2, 123]


```python
x = [1, 2, "a", "b"]
i = 0
while i<len(x):
    if type(x[i]) == str:
        x.pop(i)
    else:
        i += 1
print(x)
    
```

    [1, 2]
    

48)Filter Strings from Array
Create a function that takes a list of strings and integers, and filters out the list so that it returns a list of integers only.

Examples
filter_list([1, 2, 3, "a", "b", 4]) ➞ [1, 2, 3, 4]

filter_list(["A", 0, "Edabit", 1729, "Python", "1729"]) ➞ [0, 1729]

filter_list(["Nothing", "here"]) ➞ []


```python
x =["A", 0, "Edabit", 1729, "Python", "1729"]
i = 0
while i<len(x):
    if type(x[i]) == str:
        x.pop(i)
    else:
        i += 1
print(x)
    
```

    [0, 1729]
    

49)Add the Index
Given a list of numbers, create a function which returns the list but with each element's index in the list added to itself. This means you add 0 to the number at index 0, add 1 to the number at index 1, etc...

Examples
add_indexes([0, 0, 0, 0, 0]) ➞ [0, 1, 2, 3, 4]

add_indexes([1, 2, 3, 4, 5]) ➞ [1, 3, 5, 7, 9]

add_indexes([5, 4, 3, 2, 1]) ➞ [5, 5, 5, 5, 5]


```python
x = [1,2,3,4,5]
i = 0
while i<len(x):
    x[i]+=i
    i+=1
print(x)
```

    [1, 3, 5, 7, 9]
    

50)Triangular Number Sequence
This Triangular Number Sequence is generated from a pattern of dots that form a triangle. The first 5 numbers of the sequence, or dots, are:

1, 3, 6, 10, 15
This means that the first triangle has just one dot, the second one has three dots, the third one has 6 dots and so on.

Write a function that returns the number of dots when given its corresponding triangle number of the sequence.
Examples
triangle(1) ➞ 1

triangle(6) ➞ 21

triangle(215) ➞ 23220


```python
n = int(input("Enter a triangle number: "))  

dots = 0
counter = 1

while counter <= n:
    dots += counter
    counter += 1

print(dots)
```

    Enter a triangle number: 6
    21
    


```python

```


```python

```


```python

```
