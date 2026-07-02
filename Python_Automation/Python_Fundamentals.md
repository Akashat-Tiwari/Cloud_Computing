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