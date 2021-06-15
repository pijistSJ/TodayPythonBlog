# Blog 3

`print()` function in python 3 is amazing function , [here](https://docs.python.org/3/library/functions.html#print) is official documentation of that

very basic thing you can do with it is printing `strings,variables,list,tuples,dictionaries,sets,numbers etc.`
for example

```python


L=[1,2,3,4]
t=(1,2,3,4)
d={1:'a' , 2:'b' , 3:'c' , 4:'d'}
s={4,5,6}
var= 'x y z'


print('hello world')
# output: hello world
print(var)
# output: x y z
print(L)
# output: [1, 2, 3, 4]
print(t)
# output: (1, 2, 3, 4)
print(d)
# output: {1: 'a', 2: 'b', 3: 'c', 4: 'd'}
print(s)
# output: {4, 5, 6}
print(1,2,3)
# output: 1 2 3

```

these are very basic example of using print statements

then more arguments of print statements are `sep=''` and `end=''`

```python

''' here is how sep and end works '''

for i in range(10):
    print(i,end='')
  
#output : 0123456789

''' end is the separation between two
    consecutive prints or two rounds of print '''

for i in range(10):
    print(i,end='\n')
  
#output :
0
1
2
3
4
5
6
7
8
9


''' also similarly sep can be used like '''

for i in range(4):
    for j in 'abc':
        print(i,j,sep=' ')
        
        
#output :
0 a
0 b
0 c
1 a
1 b
1 c
2 a
2 b
2 c
3 a
3 b
3 c

```

these are more known and in-general use cases but print function also has a unique ability 
that is to converts list,set,tuple or dictionary items to independent entites and then printing then 

for example if i have a tuple `t=(1,2,3,4)` and i want to print
something like 1+2+3+4

a very naive approach of mine would be usine loops
```python
op=''  # string to store output

t=(1,2,3,4)

for i,j in enumerate(t):
    if i != (len(t)-1) :
        op += str(j)+'+'  # if index is not the last then add the number and the + sign  
    else:
        op += str(j)   #otherwise add only number to string
        
print(op)

# output : 1+2+3+4
```
## Note:
in above code if you dont know about `enumerate()` function , you can look upto it about on google or
[official documentation](https://docs.python.org/3/library/functions.html#enumerate) also I have a separate blog
on that too


the above given way using loops is although very naive way, 
there is also one another method that is `''.join()` method
here is [official documentation ref](https://docs.python.org/3/library/stdtypes.html?highlight=join#str.join) for `''.join()` method,
it is a string method and not an independent function

how that works is it joins any iterable(lists,sets,tuples,dicts) with given argument in  `''`
```python

t=(1,2,3,4)

'''
However , to use .join(), iterable should have string elements so 
you have two methods to covert it from int to str type

1. List comprehensions  and
2. map() functions

'''


####### USING LIST COMPREHESIONS #######

t= [str(x) for x in t]
print( ''.join(t) )

# output : 1+2+3+4



####### USING MAP() #######

t=(1,2,3,4)
t=map(lambda x :str(x), t)
print('+'.join(list(t)))

# output : 1+2+3+4
        

```

Also there is one last (and suitable to title ) method , using print

```pytohn
'''
in any function say add()
*L , where L stands for list , works as each element in independent way,
so to print `1+2+3+4` using print statements only

we can use sep
'''
t=(1,2,3,4)

print(*t,sep='+')

# output : 1+2+3+4

'''
also in this method you dont need type conversions, 
although it must have been done internally by the function

and in addition if you want to print some pattern like `1,2,3,4.`

it can be also done using code below
'''


t=(1,2,3,4)

print(*t,sep=',',end='.')

# output : 1,2,3,4.

```


<br> <br>

also after all this you have a new way of printing all list,set,tuple elements in newline each without using loops

```python
Li = list(range(10))

print(*Li,sep='\n')

'''
output : 
0
1
2
3
4
5
6
7
8
9
'''
```

