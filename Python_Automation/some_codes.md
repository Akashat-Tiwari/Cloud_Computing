## 1. Counting Word Frequency using a DICTOIANARY, also determining the biggest count and biggest word

fname = input("Enter the valid file name (file must be present in the same folder as of the corresponding code : ")

fhandle = open(fname)

counts = dict()


for line in fhandle : 
   
   line = line.rstrip()
   
   words= line.split()
  
   for word in words :
    
      counts[word] = counts.get(word,0) + 1 


print(counts,"\n")

print(counts.items(),"\n")


bigcount = float("-inf")

bigword = None


for word,count in counts.items() :
  
   if count > bigcount :
   
      bigcount = count
      bigword = word


print(bigword,bigcount)



## 2. Sorting lists of tuples from a dict

d = {'a' : 10 , 'b' : 1 , "c" : 22}

t= sorted(d.items())   // sorting on the basis of keys only

>>> t = [('a':10),('b' : 1 ),("c" : 22)]

for (k,v) in t :
   
    print(k,v)    



## 3. the top 10 most common words in a file


fname = input("enter the file name :")

fhandle = open(fname)


counts = dict()

for line in fhandle : 
   
        words = line.split()
        for word in words : 
               counts[word]  = counts.get(words,0) + 1 

lst = list()         

for (k,v) in counts.items() :
  
        lst.append((v,k))


sorted_lst = sorted(lst)

reverse_sorted_lst = sorted_lst[::-1]

top_ten = reverse_sorted_lst[:10]


for (v,k) in top_ten : 
     
       print(k,v)


 * instead we use lembda expressions:

           counts = {}
           sorted([(v,k) for k,v in counts.items()])
