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
