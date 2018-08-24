#Apache logfile
import collections

logfile = open("yourlogfile.log", "r")

clean_log=[]

for line in logfile:
    try:
        # copy the URLS to an empty list.
        # We get the part between GET and HTTP
        clean_log.append(line[line.index("GET")+4:line.index("HTTP")])
    except:
        pass

counter = collections.Counter(clean_log)

# get the Top 50 most popular URLs
for count in counter.most_common(50):
    print(str(count[1]) + "	" + str(count[0]))

logfile.close()

# use FTP in Python
from ftplib import FTP

ftp = FTP('ftp.cwi.nl')   # connect to host, default port

ftp.login()               # user anonymous, passwd anonymous@

ftp.retrlines('LIST')     # list directory contents 

#Dictionaries
# key/value pairs declaration
 dict = {
 ‘key1′:’value1′,
 ‘key2′:’value2′,
 ‘key3′:’value3′
 }

#Get all keys
 dict.keys()

#Get all values
 dict.values()

#Modifying
 dict['key2'] = ‘value8′

#Accessing
 print dict['key1']

# prints ‘value2′
 print dict['key2']

# empty declaration + assignment of key-value pair
 emptyDict = {}
 emptyDict['key4']=’value4′

# looping through dictionaries (keys and values)
 for key in dict:
 print dict[key]

# sorting keys and accessing their value in order
 keys = dict.keys()
 keys.sort()
 for key in keys:
 print dict[key]

# looping their values directory (not in order)
 for value in dict.values():
 print value

# getting both the keys and values at once
 for key,value in dict.items():
 print “%s=%s” % (key,value)

# deleting an entry
 del dict['key2']

# delete all entries in a dictionary
 dict.clear()

# size of the dictionary
 len(dict)
