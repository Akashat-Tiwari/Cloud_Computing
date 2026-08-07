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

## 5. Python built in support for TCP ports/sockets, HTTP request in python \

Start
  │
  ▼
Create socket
  │
  ▼
Connect to data.py4e.org
  │
  ▼
Send GET request
  │
  ▼
Receive 512 bytes
  │
  ▼
More data?
 ├── Yes → Print it → Receive next 512 bytes
 └── No → Close socket

import socket

mysocket = socket.socket(socket.AF_INET,socket.SOCK_STREAM)  // IPV4 and TCP/IP

mysocket.connect(("data.py4e.org",80))

cmd = "GET http://data.py4e.org/romeo.txt HTTP/1.0\n\n".encode()      //  converting string to bytes for socket as it can only communicate in bytes

mysocket.send(cmd)                 // send request in bytes

while true : 

     data = mysocket.recv(512)        // receive data in bytes
     if(len(data) <1 ) : 
          break
     print(data.decode())          // bytes to readable strings


mysocket.close()

## 6. parsing through XML :

import xml.etree.ElementTree as ET 

data = '''

    <stuff>
        <users>
           <user x= "2">
              <id>001</id>
              <name>chuck</name>   
           <user>
           <user x= "7">
              <id>009</id>
              <name>braint</name>   
           <user>
        </users>/
    </stuff>

stuff = ET.fromstring(data)

lst = stuff.findall('users/user')

print('user count :',len(lst))

for item in lst:

        print('name',item.find('name').text)
        print('Id',item.find('id').text)
        print('Attribute',item.get("x))


## 7. parsing through JSON

import json

data = '''{
         
    "name" : "akashat",
    "phone" : {"type" : "intl","number" : "+1 4869454005"},
    "email" : {"hide" : "yes"}

}'''

info = json.loads(data)



print("name : ", info["name"])

print("email : " , info["email"]["hide"])

print("phone number: " ,info["phone"]["number"])

print("phone type: " ,info["phone"]["type"])

## 8.  parsing through JSON , via list 

     import json

     data = '''[
         
            {
       "id" : "01",
       "name" : "akashat",
       "x" : "2"
    },
    {
        "id" : "02",
        "name" : "tiwari",
        "x" : "4"
    }

     ]'''

    info = json.loads(data)

    for item in info:  
    print("name : ", item["name"])
    print("id : ", item["id"])
    print("x: ", item["x"])
