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

## 4. extracting a host name from the given data using find and string slicing

data = "from asymptote@ak.ti.12 sat jan 2005"

atpos = data.find("@")   // 14

spacepos = data.find(" ",atpos)     // 23 

host = data[atpos+1 : spacepos]

print(host)

## 5. Python built in support for TCP ports/sockets, HTTP request in python  

import socket

mysocket = socket.socket(socket.AF_INET,socket.SOCK_STREAM)

mysocket.connect(("data.py4e.org",80))

cmd = "GET http://data.py4e.org/romeo.txt HTTP/1.0\n\n".encode()

mysocket.send(cmd)

while true : 

     data = mysocket.recv(512)
     if(len(data) <1 ) : 
          break
     print(data.decode())


mysocket.close()

