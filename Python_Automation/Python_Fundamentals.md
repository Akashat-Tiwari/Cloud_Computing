# Basics Of Python : 

* Operator Precedence : parenthesis > power(**) > mul and devision > addition and sub > left to right

* type(variable) is an inbuilt function used to know the datatype of a variable

* integer division in python3 always produces a float point number

* the input() function returns a string 

* for thing in Data :  

      statement


  ex : for i in [5,4,3,2,1]

             print(i)

* is and is not : 
   in case of comparision with None(nothing) we often use is or is not instead of == 
   

ex :  if i is None : 
            

      print("empty")

* string slicing :
    
     str[a:b] -> a is included while b is excluded

     str[:b] -> from 0 to b-1 

     str[a:] -> from a to end of string 
  
     str[:] -> whole string

* string replacement :

    str = "banana"
    str2 = str.replace("na","XX")
    print(str2) -> baxxxx

* str.split() : returns a list containing elements of string but separated by spaces

    ex : list1 = str.split()

    ex : list2 = str.split(";") : split the words/elements by semicolon ie ;

* lists are like pringles : systematic chips while dictionaries are lays packet : scattered (not organised) chips

* dictonaries are maps/hashmaps (in java) ie having (key : value) pairs

* applications of dictonaries are : histogram ie counting the frequencies

* x = counts[key] : its an traceback if the key is not in dict to avoid this we use get() method of dict  

* x = counts.get(key,0) : where x takes value if the key exists in counts(dict) else x takes the default value ie 0

* if key exists then add incr frequency by 1 and if not exits then set frequency to 1

* ***  both simultaneously by using get() : counts[key] = counts.get(key,0) + 1

## in built functions : 

* sorted(string_name) : will return the passed string in alphabetically sorted order

* generator expression :

* s = "Hello@#123!!"

* result = "".join(ch for ch in s if ch.isalnum()) : Keeps only letters and numbers.

* result = "".join(ch for ch in s if ch.isdigit()) : Keep only digits.

* result = "".join(ch for ch in s if not ch.isspace()) : removes spaces

* "".join(["a","b","c"]) : join the characters to form a string but joining without something in between due to "".

* s.upper(), s.lower(),s.swapcase(), s.capatalize() : common functions

* General slicing syntax: string[start : stop : step]

*indices :
           
            A   B   C   D   E
            0   1   2   3   4

           Negative indices

            A   B   C   D   E
           -5  -4  -3  -2  -1

* reversing a string : using slicing

*   s = "hello" =>  rev = s[::-1]


