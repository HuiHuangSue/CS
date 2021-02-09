https://www.learnpython.org/
https://docs.python.org/3/tutorial/appetite.html


### python 2 vs 3
- print in 2 not a function, so print "a"; in 3 print is a function and must be invoked with print()
- range in 2 acts like xrange, which returns iterator instead of a new list. 

### standard
- indentation -- tabs or 4 spaces
- dynamically typed - dont have to declare type befpre using it
- define string with ' or ". " can include apostrophes ', \, unicode chars, carriage return. 

---------------------------------------------------
### Basic grammar
#### variables & types
```
"I said " + ("Hey " * 2) + "Hey!"
'I said Hey Hey Hey!'

True + False
1

type("a") 
isinstance(2.0, float)
print("Float: %f" % myfloat)
print("String: %s" % mystring)
print("Integer: %d" % myint)
```
#### Lists
```
myList=[1,2,3]
strlist = ["my". "name"]
mylist.append(4)
print(mylist[0])
```

#### Basic Operators
```
even_numbers = [2,4,6,8]
odd_numbers = [1,3,5,7]
all_numbers = odd_numbers + even_numbers // preserves order
print(all_numbers)
print([1,2,3] * 3) 
len(list1)
```

#### String Formatting
```
print("%s is %d years old" % ("Sue", 21))
mylist = [1,2,3]
print("A list: %s" % mylist)
%s - String (or any object with a string representation, like numbers)
%d - Integers
%f - Floating point numbers
%.<number of digits>f - Floating point numbers with a fixed amount of digits to the right of the dot.
%x/%X - Integers in hex representation (lowercase/uppercase)

data = ("John", "Doe", 53.44)
format_string = "Hello %s %s. Your current balance is $%s."
print(format_string % data)
```

#### Basic String Operations
```
astring = "Hello world!"
print(astring.count("l")) string.upper(), astring.lower(), stringstartswith("He"), endswith("fdgf"), stringsplit(" ") --> list of Hello World 2 words
print(astring.index("o") + len(astring))
print(astring[3:7]) --> index 3 -- 6 --> lo w (-3 means "3rd character from the end")
print(astring[3:7]) & print(astring[3:7:1]) same
print(astring[3:7:2])
print("The characters with odd index are '%s'" %s[1::2]) #(0-based indexing)
print("The last five characters are '%s'" % s[-5:]) # 5th-from-last to end
print(astring[::-1]) // reverse
```

#### Boolean
```
if "John" in ["John", "Bob"] and Non-empty-Object or 2 < 3
    print "a"
elif list1 is list2
    print "no way as is matches instances"
else
    print "last"
```

#### Loops
```
for x in (range(5)) --> [0, 1, 2, 3, 4]
>>> print(range(3,6)) --> [3, 4, 5]
>>> print (range(3,8,2)) --> [3, 5, 7]
```
##### while else; break skips else but continue continues.
```
while(count<5):
    print(count)
    count +=1
else:
    print("count value reached %d" %(count))

# Prints out 1,2,3,4
for i in range(1, 10):
    if(i%5==0):
        break
    print(i)
else:
    print("this is not printed because for loop is terminated because of break but not due to fail in condition")
```
#### Functions
```
def my_function_with_args(username, greeting):
    print("Hello, %s, From My Function!, I wish you %s"%(username, greeting))

def sum_two_numbers(a, b):
    return a + b
```

#### Classes & Objects
```
class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")

myobjectx = MyClass()
myobjecty = MyClass()

myobjecty.variable = "yackity"

# Then print out both values
print(myobjectx.variable)
print(myobjecty.variable)
blah
yackity



class Vehicle:
    name = ""
    kind = "car"
    color = ""
    value = 100.00
    def description(self):
        desc_str = "%s is a %s %s worth $%.2f." % (self.name, self.color, self.kind, self.value)
        return desc_str

# your code goes here
car1 = Vehicle()
car1.name = "Fer"
car1.color = "red"
car1.kind = "convertible"
car1.value = 60000.00

car2 = Vehicle()
car2.name = "Jump"
car2.color = "blue"
car2.kind = "van"
car2.value = 10000.00

# test code
print(car1.description())
print(car2.description())
Fer is a red convertible worth $60000.00.
Jump is a blue van worth $10000.00.
```

#### Dictionaries
```
for name, number in phonebook.items():
    print("Phone number of %s is %d" % (name, number))
del phonebook["John"] or phonebook.pop("John")
```

#### Numpy Arrays
```
height = [1.87,  1.87, 1.82, 1.91, 1.90, 1.85]
weight = [81.65, 97.52, 95.25, 92.98, 86.18, 88.45]

# Import the numpy package as np
import numpy as np

np_height = np.array(height)
np_weight = np.array(weight)

bmi = np_weight / np_height ** 2
bmi[bmi > 23]
```

#### List
```
sentence = "the quick brown fox jumps over the lazy dog"
words = sentence.split()
word_lengths = [len(word) for word in words if word != "the"]
```
#### Multiple function arguments
```
def foo(first, second, third, *therest):
    print("First: %s" % first)
    print("Second: %s" % second)
    print("Third: %s" % third)
    print("And all the rest... %s" % list(therest))
    
def bar(first, second, third, **options):
    if options.get("action") == "sum":
        print("The sum is: %d" %(first + second + third))

    if options.get("number") == "first":
        return first

result = bar(1, 2, 3, action = "sum", number = "first")
print("Result: %d" %(result))
```
#### Regular expression 
https://docs.python.org/3/library/re.html#regular-expression-syntax%22RE%20syntax

#### Set
```
a = set(["Jake", "John", "Eric"])
b = set(["John", "Jill"])

a.intersection(b) ==> reveerse order both set(['John'])
a.union(b)
a.symmetric_difference(b) //reverse order both set(['Jill', 'Jake', 'Eric']);  only on one set
a.difference(b) // only in one and not the other VS b.difference(a)
set(['Jake', 'Eric'])
set(['Jill'])
```

#### Partial
```
from functools import partial
def func(u,v,w,x):
    return u*4 + v*3 + w*2 + x

p = partial(func,5,6,7)
print(p(8))
```

```
# Python 3

my_strings = ['a', 'b', 'c', 'd', 'e']
my_numbers = [1,2,3,4,5]

results = list(map(lambda x, y: (x, y), my_strings, my_numbers))

print(results)
[('a', 1), ('b', 2), ('c', 3), ('d', 4), ('e', 5)]
---------------------------------------
dromes = ("demigod", "rewire", "madam", "freer", "anutforajaroftuna", "kiosk")

palindromes = list(filter(lambda word: word == word[::-1], dromes))

print(palindromes)
-------------------------------------------------------
# Python 3
from functools import reduce

numbers = [3, 4, 6, 9, 34, 12]

def custom_sum(first, second):
    return first + second

result = reduce(custom_sum, numbers)  --> 68
result = reduce(custom_sum, numbers, 10) // initially use 10 as first argument to custom_sum. ---> 78
print(result)
```
------------------------------------------------
#### Ways to take control of same line/next line/next page:
```
carriage return \r
printf("stackoverflow\rnine")
ninekoverflow

linefeed `\n` 
printf("stackoverflow\nnine")
stackoverflow
nine

formfeed \f
printf("stackoverflow\fnine")
stackoverflow
             nine
```
