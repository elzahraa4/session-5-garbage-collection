**1-Write a Python program to calculate the length of a string using 2 ways


```python
str = "ddfgt"
counter=0
for i in str:
    counter+=1
print(counter)
```

    5
    


```python
i =0
str = "ddfgt"
while i < 5:
    i += 1
print(i)
```

    5
    

way 1 using len() function


```python
x = "Ahmed"
```


```python
len(x)
```




    5



Way 2 using for loop and in operator


```python
y = '''
ab
c 
'''
L = 0
for i in y:
    L += 1
print(L)
```

    7
    

Example 2


```python
n = 'hello world !'
```


```python
Len = 0
for i in n:
    Len += 1
print(Len)
```

    13
    

way 3 using while loop & slicing


```python
def findLen(str):
    counter = 0
    while str[counter:]:
        counter += 1
    return counter
 
str = "geeks"
print(findLen(str))
```

    5
    

Example 2


```python
def Len(name):
    Lnum = 0
    while name[Lnum:]:
        Lnum +=1
    return Lnum

name = input("plz enter yr son name: ")
print(Len(name))
```

Way 4 uing str methods: Join and count


```python
def findLen(str):
    if not str:
        return 0
    else:
        some_random_str = 'py'
        return ((some_random_str).join(str)).count(some_random_str) + 1
str = "nora"
print(findLen(str))
```


```python
def countLen(str):
    if not str:
        return 0
    else:
        nullStr = ""
        return ((nullStr).join(str)).count(nullStr)-1
str = input("plz: ")
print(countLen(str))
```

Way 5 using reduce method 


```python
import functools
 
def findLen(string):
    return functools.reduce(lambda x,y: x+1, string, 0)
 
 
# Driver Code
string = 'geeks'
print(findLen(string))
```

Way 6 using sum function and list comprehension function


```python
def countLen(string):
    return  sum(1 for i in string);
string = "fullll"
print(countLen(string))
```

**2-Write a Python program to get a string made of the first 2 and last 2 characters of a given string. If the string length is less than 2, return the empty string instead ("##Sample String : 'w3resource'
Expected Result : 'w3ce'
##Sample String : 'w3'
Expected Result : 'w3w3'
##Sample String : ' w'
Expected Result : Empty String)


```python
while True:
    str = input(": ")
    if len(str)  >= 2:
        print(str[0:2]+str[-2: ])
    else:
        print("empty string")
```


```python
userstr = input("plz enter yr word: ")
#for check
print(userstr)
# convert stringg to list
userstr = list(userstr)
#for check
print(userstr)
# for check length of string
if len(userstr) > 2:
    print("".join(userstr[0]+userstr[1]+userstr[-2]+userstr[-1]))
elif len(userstr) == 2:
    print("".join(userstr * 2))
else:
    print("empty string") 
```

**3-Write a Python program to add 'ing' at the end of a given string (length should be at least 3). If the given string already ends with 'ing', add 'ly' instead. If the string length of the given string is less than 3, leave it unchanged. (Sample String : 'abc'
Expected Result : 'abcing')


```python
s = (input(": "))
if len(s) >= 3:
    if s[-3: ] == ("ing"):
       print(s[0: -3] + "ly")
    else:
        s = s + "ing"
        print(s)
else:
    print(s)
```

    : hjuing
    hjuly
    

**4-Write a Python function that takes a list of words and return the longest word and the length of the longest one
(Longest word: Exercises
Length of the longest word: 9)


```python
def returnnames():                    # Function creation
    names = []                        # create empty list
    for i in range (5):               # for loop to receive list items as input raw data
        name = input(": ")            # receive input items
        names.append(name)            # append input items to list
    return names                      # return list

nameList = returnnames()              # store list in var
print(nameList)                       # check var

maxname = ""                          # default maxname
maxLen = 0                            # default maxlen
for i in nameList:                    # for loop to check length of each item in list
    if len(i) > maxLen:               # compare item length with default value "zero"
        maxLen = len(i)               # define maxlen in list
        maxname = i                   # define maxname
print("maxname is: " + maxname, "\nmaxLen is: "+ str(maxLen))
```

    : zxdfgrhj
    : sdwef
    : wefef
    : efefwde
    : dd
    ['zxdfgrhj', 'sdwef', 'wefef', 'efefwde', 'dd']
    maxname is: zxdfgrhj 
    maxLen is: 8
    

**5-Write a Python program to change a given string to a newly string where the first and last chars have been exchanged using 2 ways (Sample String:abca  Expected Result:ebce)


```python
string = "dfrghd"
print(string[-1:]+ string[1:5] + string[0:1])


```

    dfrghd
    


```python
string = input("")
print(string[-1:]+ string[1:-1] + string[0:1])


```

    dfergtfyhrujbvnhftyduiskuy
    yfergtfyhrujbvnhftyduiskud
    


```python
string = "sdfegrt"
print("a"+ string[1:5] + "a")
```


```python
string = input("")
print("a" + string[1:-1] + "a")


```

    dfergtfyhrujbvnhftyduiskuy
    afergtfyhrujbvnhftyduiskua
    

**6-Write a Python program to remove characters that have odd index values in a given string (Sample String:abca Expected Result:ac)


```python
string = "asdfgthyjuk"        
for i in string:                 # for loop to check char index in string
    if string.index(i)%2 == 0:   # check if char index is even 
        print(i, end= " ")       # use end arguement to separate between char with " "
    else:
       continue                  # if char index is odd, ignore it
```

    a d g h j k 


```python
string = "asdfgthyjuk"         
print(string[::2])               # print char, then jump 2
```

    adghjk
    

**7-Write a Python program to count the occurrences of each word in a given sentence (Sample String:amr and ahmed are frindes but amr is the tallest Expected Result:2)


```python
sen = "q w e e e e w s q q q w s d e f r w w q q"  # create string
wor = sen.split()                                  # split strin to list of items to count their counts later
print(wor)                                         # check list
s = set(sen)                                       # cast list to set to define items without repeating but all still exist
print(s)                                           # check set
s.discard(" ")                                     # discard spaces
for i in s:                                        # for loop to check items in set
    print(i, " : ", wor.count(i))                  # print items -from set s-  and their counts -from list wor-
```

    ['q', 'w', 'e', 'e', 'e', 'e', 'w', 's', 'q', 'q', 'q', 'w', 's', 'd', 'e', 'f', 'r', 'w', 'w', 'q', 'q']
    {'f', 'q', 'w', 'r', 'd', 'e', 's', ' '}
    f  :  1
    q  :  6
    w  :  5
    r  :  1
    d  :  1
    e  :  5
    s  :  2
    

**8-Write a Python script that takes input from the user and displays that input back in upper and lower cases


```python
string = input("plz plaplaplaa: ")
print(string.upper())
print(string.lower())
```

**9-Write a Python function to reverse a string if its length is a multiple of 4


```python
def reverse_Str():
    string = input(" : ")
    if len(string) % 4 == 0:
        print(string[::-1])
    else:
        return
reverse_Str()
```

     : fght
    thgf
    

**10- Write a Python program to remove a newline in Python


```python
s = "ghtvy;uouh\nnhhjklll\nguii;i;"

print(s[0: 10] + s[11: 19] + s[20::] )
```

    ghtvy;uouh
    nhhjklll
    guii;i;
    ghtvy;uouhnhhjklllguii;i;
    


```python
s = "ghtvy;uouh\nnhhjklll\nguii;i;"
for i in s:
    if i != "\n":
        print(i, end= " ")
    else:
        continue
    
```

    g h t v y ; u o u h n h h j k l l l g u i i ; i ; 

**11-Write a Python program to check whether a string starts with specified characters


```python
string = "ghytr"
print(string.startswith("g"))
```

    True
    


```python
string = "ghytr"
print(string[0] == "h")
```


```python
char = "g"
string = input(": ")
if string[0] == char:
    print("ok")
else:
    print("ooops")
```

    : fhrtyd
    ooops
    


```python
char = "g"
string = input(": ")
print(string[0] == char)
```

    : fgtr
    False
    

**12- Write a Python program to add prefix text to all of the lines in a string


```python
# hafez
#for printing prefix
s = "car cat cow"
animals = s.split()
for i in animals:
   print("the ", i)  

# for adding prefix
for i in range(len(animals)):
    animals[i] = "The " + animals[i]   
print(animals)

# for adding to each line__________>> split with comma
string = "base line, newer one"
newstring = string.split(",")
for i in range(len(newstring)):
    newstring[i] = "this is " + newstring[i]
print(newstring)
```

    the  car
    the  cat
    the  cow
    ['The car', 'The cat', 'The cow']
    ['this is base line', 'this is  newer one']
    


```python
s = "ghytr\nvgbftr\nghty\nmbhjuy"
s = "AA" + s[0: 6] +"AA" + s[6: 13] + "AA" + s[13:18] + "AA" + s[18:: ]
print(s)
```


```python
s = "ghytr\nvgbftr\nghty\nmbhjuy"
for i in s:
    if i == "\n":
        i += "AA"
    print(i)

```

    g
    h
    y
    t
    r
    
    AA
    v
    g
    b
    f
    t
    r
    
    AA
    g
    h
    t
    y
    
    AA
    m
    b
    h
    j
    u
    y
    

**13-Write a Python program to print the following numbers up to 2 decimal places


```python
i = 1025.236
i = round(i, 2)
print(i)
```

    1025.24
    

**14-Write a Python program to print the following numbers up to 2 decimal places with a sign


```python
i = 1025.235
i = (round(i, 2))
if i > 0:
    print("+", i)
else:
    print("-", i)
```

    + 1025.23
    

**15-Write a Python program to display a number with a comma separator


```python
i = 99999999999999
print("{:,}".format(i))
```

    99,999,999,999,999
    


```python
#Hafez
n = 1234
n = str(n)
new_s = ""
for i in n:
    new_s = new_s +  i + " ,"
new_s = new_s[ :-1] # without last comma
print(new_s)
```

    1 ,2 ,3 ,4 
    

**16-Write a Python program to reverse a string using 2 ways


```python
def reverse_Str():
    string = input(" : ")
    print(string[::-1])
    
reverse_Str()
```

     : Ahmed
    demhA
    


```python
#Hafez
name = "Ahmed"
result = ''
for i in range(len(name)):
    result = result + name[len(name) -1 - i]
result   
```




    'demhA'



 **17-Write a Python program to count repeated characters in a string (hint:use dictionary)


```python
s = 'Python Programming'   # insert string
d = {}                     # create new, empty dict
for i in s:                # for loop on char in string
    if i in d.keys():      # check if char within dict keys to add it to eys
        d[i] += 1          # add 1 to value of this key if it already existed before ------>> value = 2
    else:                  
        d[i]=1             # if char not exist, make value = 1

print(d)               # print dict
```

    {'P': 2, 'y': 1, 't': 1, 'h': 1, 'o': 2, 'n': 2, ' ': 1, 'r': 2, 'g': 2, 'a': 1, 'm': 2, 'i': 1}
    


```python
#hafez
s = "ahmedessamm7mdaliosama"
chars = []
for i in s:
    chars.append(i)
chars = set(chars)
chars
#loop on set to count i
for i in chars:
        print(i, ":", s.count(i) )

```

    o : 1
    l : 1
    h : 1
    a : 5
    7 : 1
    i : 1
    s : 3
    e : 2
    m : 5
    d : 2
    


```python
#ramy:if string input
#hafez: as if all program work as a function
s = input("plz: ")
def countchars(s):
    chars = []
    for i in s:
        chars.append(i)
    chars = set(chars)
    chars
    #loop on set to count i
    for i in chars:
            print(i, ":", s.count(i) )
countchars(s)
```

    plz: fghtyrhfkdeirutnfjfndhfeferlt4tggffdfdsqwwqw
    w : 3
    4 : 1
    r : 3
    f : 9
    j : 1
    n : 2
    q : 2
    k : 1
    g : 3
    l : 1
    i : 1
    u : 1
    s : 1
    h : 3
    y : 1
    t : 4
    e : 3
    d : 4
    


```python
#hafez: as if all program work as a function

def countchars(s):
    chars = []
    for i in s:
        chars.append(i)
    chars = set(chars)
    chars
    #loop on set to count i
    for i in chars:
            print(i, ":", s.count(i) )
countchars(input())
```

    fdgrtgdggeteewwwwww
    w : 6
    r : 1
    f : 1
    g : 4
    e : 3
    t : 2
    d : 2
    

**18-Write a Python program to find the first non-repeating character in a given string


```python
sen = "q w e e e e w s q q q w s d e f r w w q q"  # create string
wor = sen.split()                                  # split string to list of items to count their counts later
print(wor)                                         # check list
s = set(sen)                                       # cast list to set to define items without repeating but all still exist
print(s)                                           # check set
s.discard(" ")                                     # discard spaces
for i in s:                                        # for loop to check items in set
    if wor.count(i) == 1:
        print(i, " : ", wor.count(i))                  # print items -from set s-  and their counts -from list wor-
        break
    
```

    ['q', 'w', 'e', 'e', 'e', 'e', 'w', 's', 'q', 'q', 'q', 'w', 's', 'd', 'e', 'f', 'r', 'w', 'w', 'q', 'q']
    {'r', 'w', 's', 'e', 'd', 'f', ' ', 'q'}
    r  :  1
    


```python
sen = "q w  e e e e  w s q q  q w s d e f r w w q q"  # create string
wor = sen.split()                                  # split string to list of items to count their counts later
print(wor)                                         # check list
for i in sen:                                        # for loop to check items in set
    if wor.count(i) == 1:
        print(i, " : ", wor.count(i))                  # print items -from set s-  and their counts -from list wor-
        break
    
```

    ['q', 'w', 'e', 'e', 'e', 'e', 'w', 's', 'q', 'q', 'q', 'w', 's', 'd', 'e', 'f', 'r', 'w', 'w', 'q', 'q']
    d  :  1
    


```python
#hafez

```

**19-Write a Python program to remove spaces from a given string


```python
s = "lk iju jki"
s = s[0:2] + s[3:6] + s[-3: ]
s
```

    l
    k
    i
    j
    u
    j
    k
    i
    


```python
#hafez
name = "Ahmed Hafez"
name = name.replace(" ", "")
print(name)
```

    AhmedHafez
    


```python
s = input(": ")
new_s = ""
for i in s:
    if i != " ":
        new_s = new_s + i
    else:
        continue
print(new_s)
```

    : asdfgr bvgfhty nfhgueieo fghtto
    asdfgrbvgfhtynfhgueieofghtto
    

**20-Write a Python program to count the number of non-empty substrings of a given string


```python
def count_substrings(s):
    l =len(s)
    return int(l*(l + 1)/ 2)
s1 = input(": ")
print("number of substrings is : ", count_substrings(s1))
```

    : sdfrgh gjtyeikdf r djfegir[vd  dfor34r
    number of substrings is :  741
    


```python
#hafez
ahm = a, h, m, ah, am, hm, ahm, amh, hma, ham, mah,mha
```

**21-write a Python program to swap first and last element of any list.


```python
#hafez
l = [1, 2, 3, 4, 5]
x = l[0]
l[0] = l[-1]
l[-1] = x
l
```




    [5, 2, 3, 4, 1]




```python
#me
l = [1, 2, 3, 4]
y =l.pop(0)
l.insert(-1, y)
x = l.pop(-1)
l.insert(0, x)
l
```




    [4, 2, 3, 1]




```python
# hafez___>> insert ele as input
l =[]
for i in range(5):
    l.append(input())
y =l.pop(0)
l.insert(-1, y)
x = l.pop(-1)
l.insert(0, x)
l    
```

    sd
    ed
    wd
    wd
    qe
    




    ['qe', 'ed', 'wd', 'wd', 'sd']



**22-Given a list in Python and provided the positions of the elements, write a program to swap the two elements in the list. (Input : List = [23, 65, 19, 90], pos1 = 1, pos2 = 3
Output : [19, 65, 23, 90])


```python
#me
l = [1, 2, 3, 4, 5, 6, 7]
x = l[0: 2]
l[0:2] = l[-2: ]
l[-2: ] = x
l
```




    [6, 7, 3, 4, 5, 1, 2]




```python
#me
l = [1, 2, 3, 4, 5, 6, 7, 8, 9]
# pos1 = 3 ----->> 4
# pos2 = 6 ----->> 7
x = l[3]
l[3] = l[6]
l[6] = x
l
```




    [1, 2, 3, 7, 5, 6, 4, 8, 9]




```python
#hafez
l = [1, 2, 3, 4, 5, 6, 7, 8, 9]
pos1 = l.index(4) 
pos2 = l.index(7)
x = l[pos1]
l[pos1] = l[pos2]
l[pos2] = x
l
```




    [1, 2, 3, 7, 5, 6, 4, 8, 9]



**23- search for the all ways to know the length of the list


```python
#same problem 1
```

**24-write a Python code to find the Maximum number of list of numbers.


```python
l = [1, 2, 3, 4, 5, 6, 7, 8, 9]
max(l)

```




    9



**25-write a Python code to find the Minimum number of list of numbers.


```python
l = [1, 2, 3, 4, 5, 6, 7, 8, 9]
min(l)
```




    1



**26-search for if an elem is existing in list


```python
l = [1, 2, 3, 4, 5, 6, 7, 8, 9]
print(i == 10)
    
```

    False
    

**27- clear python list using different ways


```python
l = [1, 2, 3, 4, 5, 6, 7, 8, 9]
l.pop(0)
l

```




    [2, 3, 4, 5, 6, 7, 8, 9]




```python
l = [1, 2, 3, 4, 5, 6, 7, 8, 9]
l.clear()
l
```




    []



**28-remove duplicated elements from a list


```python
l =[1, 2, 3, 3, 4, 2, 5, 6]
s = set(l)
for i in s:
    if l.count(i) >1:
        l.remove(i)
print(l)
```

    [1, 3, 4, 2, 5, 6]
    


```python
#hafez
l =[1, 2, 3, 3, 4, 2, 5, 6]
l = set(l)
l = list(l)
l

```




    [1, 2, 3, 4, 5, 6]




```python
# Ramy
l =[1, 2, 3, 3, 4, 2, 5, 6]
l = list(set(l))
l
```




    [1, 2, 3, 4, 5, 6]



**29-Given list values and keys list, convert these values to key value pairs in form of list of dictionaries. (Input : test_list = [“Gfg”, 3, “is”, 8], key_list = [“name”, “id”]
Output : [{‘name’: ‘Gfg’, ‘id’: 3}, {‘name’: ‘is’, ‘id’: 8}])


```python
l = ["A", 3, "b", 90, "c", 23]
char = []
num = []

for i in l:
   if type(i) == str:
        char.append(i) 
        
        
for i in l:
     if type(i) == int:
        num.append(i)
d = dict()

for i in range(len(char)):
    d[char[i]] = num[i]
d
```




    {'A': 3, 'b': 90, 'c': 23}



**30-write a python program to count unique values inside a list using different ways


```python
# hafez
l = [1, 2, 2, 3, 5, 8, 4]
counter =0
for i in l:
    if l.count(i) == 1:
        counter += 1
        print(i)
counter # check number of unique values

```

    1
    3
    5
    8
    4
    




    5




```python
# Menna
l = [1, 2, 2, 3, 5, 8, 4]
new_l = []
for i in l:
    if i in new_l:
        new_l.remove(i) #hafez
        continue
    else:
        new_l.append(i)
print(new_l)
len(new_l)

```

    [1, 3, 5, 8, 4]
    




    5



**31-write a python program Extract all elements with Frequency greater than K (Input : test_list = [4, 6, 4, 3, 3, 4, 3, 4, 3, 8], K = 3 
Output : [4, 3] )


```python
#HAFEZ
l = [1, 2, 2, 2, 2, 3, 3, 3, 4, 4, 5, 5 ,5 , 6, 6] #create list with unique and frequent values
k = 3                                              # frequent number

ele = set()                                        # create empty set named ele
for i in l:                                        # loop on l
    if l.count(i) > k:                             # if count of each i greater than k, add i to the set "ele"
        ele.add(i)
        
        
print(ele)                                        # check elements in set

```

    {2}
    

**32-write a python program to find the Strongest Neighbour (Input: 1 2 2 3 4 5
Output: 2 2 3 4 5)


```python
l = [ 1, 2, 2, 3, 2, 4, 5]           # create list with random arranged numbers

for i in range(len(l)):              # loop on each i in l according to its length
    for j in range(i+1, len(l)):     # loop on each i after 1st i "j" in l according to its length
        if l[j] >= l[i]:             # if there is any element greater than i in l after 1st one 
            print(l[j], end = " ")   # print it and take space after
            break                    # exit after print and loop on next element i
                
```

    2 2 3 4 4 5 

**33-write a Python Program to print all Possible Combinations from the three Digits (Input: [1, 2, 3]
Output:
1 2 3 ##
1 3 2 ##
2 1 3 ##
2 3 1 ##
3 1 2 ##
3 2 1)


```python
#Rana
def all(l):
    for i in range(len(l)):
        for j in range(len(l)):
            for k in range(len(l)):
                if (i != j and j != k and i !=k):
                    print(f"{l[i]} {l[j]} {l[k]} ##", end =" ")
print(all([1, 2, 3]))        
```

    1 2 3 ## 1 3 2 ## 2 1 3 ## 2 3 1 ## 3 1 2 ## 3 2 1 ## None
    


```python
#hafez
import itertools
print(list(itertools.permutations([1, 2, 3, 4])))
```

    [(1, 2, 3, 4), (1, 2, 4, 3), (1, 3, 2, 4), (1, 3, 4, 2), (1, 4, 2, 3), (1, 4, 3, 2), (2, 1, 3, 4), (2, 1, 4, 3), (2, 3, 1, 4), (2, 3, 4, 1), (2, 4, 1, 3), (2, 4, 3, 1), (3, 1, 2, 4), (3, 1, 4, 2), (3, 2, 1, 4), (3, 2, 4, 1), (3, 4, 1, 2), (3, 4, 2, 1), (4, 1, 2, 3), (4, 1, 3, 2), (4, 2, 1, 3), (4, 2, 3, 1), (4, 3, 1, 2), (4, 3, 2, 1)]
    

**34-write a Python program to find all the Combinations in the list with the given condition (Input: test_list = [1,2,3] 
Output: 
 [1], [1, 2], [1, 2, 3], [1, 3]
 [2], [2, 3], [3])


```python
s = "123"
combinations = [int(s[i : j]) for i in range(len(s)) 
             for j in range(i +1, len(s) +1)]
print(combinations)
```

    [1, 12, 123, 2, 23, 3]
    

**35-write a Python program to get all unique combinations of two Lists (List_1 = ["a","b"]
List_2 = [1,2]
Unique_combination = [[('a',1),('b',2)],[('a',2),('b',1)]] )


```python
l = [1, 2]
l2 =['a', 'b']
for i in range(len(l)):
    for j in l2:
        print(l[i], j)
```

    1 a
    1 b
    2 a
    2 b
    

**36-Remove all the occurrences of an element from a list in Python (Input : 1 1 2 3 4 5 1 2 1 

**Output : 2 3 4 5 2)


```python
l = [1, 1, 2, 3, 4, 5, 1, 2, 1]
element = 1
c = l.count(element)
for i in range(c):
    l.remove(element)
print(l)    
```

    [2, 3, 4, 5, 2]
    


```python
l = [1, 1, 2, 3, 4, 5, 1, 2, 1]
for i in l:
    if l.count(i) > 1:
        l.remove(i)
print(l)
```

    [3, 4, 5, 2, 1]
    

**37-write a python program to Replace index elements with elements in Other List (The original list 1 is : [‘Gfg’, ‘is’, ‘best’] The original list 2 is : [0, 1, 2, 1, 0, 0, 0, 2, 1, 1, 2, 0] The lists after index elements replacements is : [‘Gfg’, ‘is’, ‘best’, ‘is’, ‘Gfg’, ‘Gfg’, ‘Gfg’, ‘best’, ‘is’, ‘is’, ‘best’, ‘Gfg’])


```python
l1 = ['gfg', 'is', 'best']
l2 = [0, 1, 2, 1, 0, 0, 0, 2, 1, 1, 2, 0]  

for i in range(len(l2)):
    if l2[i] == 0:
        l2[i] = l1[0]
    elif l2[i] == 1:
        l2[i] = l1[1]
    elif l2[i] == 2:
        l2[i] = l1[2]

print(l2)

```

    ['gfg', 'is', 'best', 'is', 'gfg', 'gfg', 'gfg', 'best', 'is', 'is', 'best', 'gfg']
    

**38- write python program to Retain records with N occurrences of K(Input : test_list = [(4, 5, 5, 4), (5, 4, 3)], K = 5, N = 2 
Output : [(4, 5, 5, 4)]
Input : test_list = [(4, 5, 5, 4), (5, 4, 3)], K = 5, N = 3 
Output : [] )


```python
l = [(4, 5, 5, 4), (5, 4, 3)]
k = 5
n = 2
for i in l:
    if i.count(k) == n:
        print(i)
```

    (4, 5, 5, 4)
    

**39-write a Python Program to Sort the list according to the column using lambda
array = [[1, 3, 3], [2, 1, 2], [3, 2, 1]]
Output :
Sorted array specific to column 0, [[1, 3, 3], [2, 1, 2], [3, 2, 1]]
Sorted array specific to column 1, [[2, 1, 2], [3, 2, 1], [1, 3, 3]]
Sorted array specific to column 2, [[3, 2, 1], [2, 1, 2], [1, 3, 3]]


```python
lst = [('candy','30','100'), ('apple','10','200'), ('baby','20','300')]
lst.sort(key=lambda x:x[1])
print(lst)
```

    [('apple', '10', '200'), ('baby', '20', '300'), ('candy', '30', '100')]
    


```python
**40- write a program to Sort Python Dictionaries by Key or Value
Input:
{'ravi': 10, 'rajnish': 9, 'sanjeev': 15, 'yash': 2, 'suraj': 32}

Output: 
{'rajnish': 9, 'ravi': 10, 'sanjeev': 15, 'suraj': 32, 'yash': 2}
```


```python
f = {'dad' : 39, 'mom' : 33, 'yahya' : 7, 'fafy' : 10}

f_keys = list(f.keys())
print(f_keys)

f_keys.sort()
print(f_keys)

new_f = dict()

for i in f_keys:
    new_f[i] = f[i]

print(new_f)
```

    ['dad', 'mom', 'yahya', 'fafy']
    ['dad', 'fafy', 'mom', 'yahya']
    {'dad': 39, 'fafy': 10, 'mom': 33, 'yahya': 7}
    


```python
f = {'dad' : 39, 'mom' : 33, 'yahya' : 7, 'fafy' : 10}

f_sorted = sorted(f.items(), key=lambda x:x[1])
print(f_sorted)
```

    [('yahya', 7), ('fafy', 10), ('mom', 33), ('dad', 39)]
    


```python
#hafez
f = {'dad' : 39, 'mom' : 33, 'yahya' : 7, 'fafy' : 10}
f_sorted = dict(sorted(f.items(), key=lambda  item: item[1]))
print(f_sorted)
```

    {'yahya': 7, 'fafy': 10, 'mom': 33, 'dad': 39}
    

**41-write python program to Remove keys with Values Greater than K ( Including mixed values )
nput : test_dict = {‘Gfg’ : 3, ‘is’ : 7, ‘best’ : 10, ‘for’ : 6, ‘geeks’ : ‘CS’},
K = 7 
Output : {‘Gfg’ : 3, ‘for’ : 6, ‘geeks’ : ‘CS’}


```python
#hafez
f = {'dad' : 39, 'mom' : 33, 'yahya' : 7, 'fafy' : 10}

keys = []

for i in f:
    if f[i] > 30:
        keys.append(i)
        
for i in keys:
    f.pop(i)
f
```




    {'yahya': 7, 'fafy': 10}



**42-Write a Python program to concatenate the following dictionaries to create a new one

Sample Dictionary :
dic1={1:10, 2:20}
dic2={3:30, 4:40}
dic3={5:50,6:60}
Expected Result : {1: 10, 2: 20, 3: 30, 4: 40, 5: 50, 6: 60}


```python
#hafez
f = {'dad' : 39, 'mom' : 33, 'yahya' : 7, 'fafy' : 10}
f_root = {'grand pa': 66, 'grand ma': 65}

f_tree = dict()

for i in f:
    f_tree[i] = f[i]

for i in f_root:
    f_tree[i] = f_root[i]

f_tree
```




    {'dad': 39, 'mom': 33, 'yahya': 7, 'fafy': 10, 'grand pa': 66, 'grand ma': 65}



**43-Write a Python program to iterate over dictionaries using for loops


```python
f = {'dad' : 39, 'mom' : 33, 'yahya' : 7, 'fafy' : 10}
for i in f:
    print(i, f[i])
```

    dad 39
    mom 33
    yahya 7
    fafy 10
    

**44- Write a Python script to merge two Python dictionaries


```python
f = {'dad' : 39, 'mom' : 33, 'yahya' : 7, 'fafy' : 10}
f_root = {'grand pa': 66, 'grand ma': 65}

f_tree = dict()

for i in f:
    f_tree[i] = f[i]

for i in f_root:
    f_tree[i] = f_root[i]

f_tree
```




    {'dad': 39, 'mom': 33, 'yahya': 7, 'fafy': 10, 'grand pa': 66, 'grand ma': 65}



**45-Write a Python program to get the maximum and minimum values of a dictionary values


```python
f = {'dad' : 39, 'mom' : 33, 'yahya' : 7, 'fafy' : 10}
v = list(f.values())
max(v)
```




    39




```python
f = {'dad' : 39, 'mom' : 33, 'yahya' : 7, 'fafy' : 10}
v = list(f.values())
min(v)
```




    7



**46- Write a Python program to drop empty items from a given dictionary.
Original Dictionary:
{'c1': 'Red', 'c2': 'Green', 'c3': None}
New Dictionary after dropping empty items:
{'c1': 'Red', 'c2': 'Green'}


```python
f = {'dad' : 39, 'mom' : None, 'yahya' : 7, 'fafy' : 10}

keys = []

for i in f:
    if f[i] == None:
        keys.append(i)
        
for i in keys:
    f.pop(i)
f
```




    {'dad': 39, 'yahya': 7, 'fafy': 10}



**47-Write a Python program to create a tuple of numbers and print one item


```python
t = (1, 2, 3)
print(t[1])
```

    2
    

**48-Write a Python program to unpack a tuple into several variables


```python
t = (1, 2, 3)
a =t[0]
b= t[1]
c = t[2]
print(a, b, c)
```

    1 2 3
    

**49-Write a Python program to add an item to a tuple


```python
t = (1, 2, 3)
new_t =list(t)
new_t.append(4)
new_t
new_tuple = tuple(new_t)
new_tuple
```




    (1, 2, 3, 4)



**50-Write a Python program to convert a tuple to a string


```python
t = ("a", "b", "c")
a =t[0]
b= t[1]
c = t[2]
s = a+b+c
s
```




    'abc'




```python
def convertTuple(tup):
        
    str = ''                     # initialize an empty string
    for item in tup:
        str = str + item
    return str
 
 
# Driver code
tuple = ('g', 'e', 'e', 'k', 's')
str = convertTuple(tuple)
print(str)
```

    geeks
    

**51-Write a Python program to convert a list to a tuple


```python
from functools import reduce
 
s = "hello"
print(*s, )





```

    h e l l o
    

**52-Write a Python program to reverse a tuple


```python
t = (1, 2, 3, 4, 5)
new_t = t[::-1]
new_t
```




    (5, 4, 3, 2, 1)



**53-Write a Python program to replace the last value of tuples in a list.
Sample list: [(10, 20, 40), (40, 50, 60), (70, 80, 90)]
Expected Output: [(10, 20, 100), (40, 50, 100), (70, 80, 100)]


```python
l = [(10, 20, 40), (40, 50, 60), (70, 80, 90)]
print([t[:-1] + (100,) for t in l])
```

    [(10, 20, 100), (40, 50, 100), (70, 80, 100)]
    


```python
l = [(10, 20, 40), (40, 50, 60), (70, 80, 90)]
for t in l:
    print(t[:-1] + (100,))
```

    (10, 20, 100)
    (40, 50, 100)
    (70, 80, 100)
    

**54-Write a Python program to convert a given string list to a tuple
Original string: python 3.0
<class 'str'>
Convert the said string to a tuple:
('p', 'y', 't', 'h', 'o', 'n', '3', '.', '0')


```python
sample_list = ['Compile', 'With', 'Favtutor']

#unpack list items and form tuple
tuple1 = (*sample_list,)

print(tuple1)
print(type(tuple1))
```

    ('Compile', 'With', 'Favtutor')
    <class 'tuple'>
    

**55-Write a Python program to calculate the average value of the numbers in a given tuple of tuples


```python
def average_tuple(nums):
    result = [sum(x) / len(x) for x in zip(*nums)]
    return result

nums = ((10, 10, 10, 12), (30, 45, 56, 45), (81, 80, 39, 32), (1, 2, 3, 4))

print("\nAverage value of the numbers of the said tuple of tuples:\n",average_tuple(nums))


```

    
    Average value of the numbers of the said tuple of tuples:
     [30.5, 34.25, 27.0, 23.25]
    

**56-Write a Python program to add member(s) to a set.


```python
s = {1, 2, 3}
s.add(4)
s
```




    {1, 2, 3, 4}



**57-Write a Python program to remove an item from a set if it is present in the set.


```python
s = {1, 2, 3}
s.discard(1)
s
```




    {2, 3}



**58-Write a Python program to create an intersection,union,difference and symmetric difference of sets


```python
s = {1, 2, 3, 5}
s2 = {2, 4, 3, 7}
s.intersection(s2)
```




    {2, 3}




```python
s = {1, 2, 3, 5}
s2 = {2, 4, 3, 7}
s.difference(s2)
```




    {1, 5}




```python
s = {1, 2, 3, 5}
s2 = {2, 4, 3, 7}
s.union(s2)
```




    {1, 2, 3, 4, 5, 7}




```python
s = {1, 2, 3, 5}
s2 = {2, 4, 3, 7}
s.symmetric_difference(s2)
```




    {1, 4, 5, 7}



**59-Write a Python program to find the maximum and minimum values in a set


```python
s = {1, 2, 4}
l = list(s)
print(min(l))
print(max(l))
```

    1
    4
    

**60- Write a Python program that finds all pairs of elements in a list whose sum is equal to a given value.


```python
from collections import Counter
 
def findPairs(lst, K):
    s = []
    count = Counter(lst)
 
    for x in lst:
        y = K - x
        if (x != y and count[y]) or (x == y and count[y] > 1):
            s.append((x, y))
            count.subtract((x, y))
             
    return s
     
    
lst = [1, 5, 3, 7, 9]
K = 12
print(findPairs(lst, K))
```

    [(5, 7), (3, 9)]
    


```python
from itertools import combinations
 
def findPairs(l, K):  
    s = []
    for i in combinations(l, 2):
        if i[0] + i[1] == K:
            s.append((i[0], i[1]))
         
    return s
     

l = [1, 5, 3, 7, 9]
K = 12
print(findPairs(l, K))
```

    [(5, 7), (3, 9)]
    


```python
def find_pairs(l, K):
    s = []
    for i in range(len(l)):
        for j in range(i + 1, len(l)):
            if l[i] + l[j] == K:
                s.append((l[i], l[j]))
    return s
l = [1, 5, 3, 7, 9]
K = 12
print(find_pairs(l, K))
```

    [(5, 7), (3, 9)]
    
