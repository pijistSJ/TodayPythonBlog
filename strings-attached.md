## This is going to be a continuous blog on strings and usecases, might be practical , might not be but it's just things i found
<br>

there are many usecases and many crucial things that can be done with strings,
[here](https://docs.python.org/3/library/stdtypes.html#str) is official documentation of strings  <br>
also here i will not talk about python built-in `string module`, i will talk about str-type variable or strings in general

there are different methods you can use with string-type variables
about all those methods you can have a look at the official documentation, which has pretty good
information with example code blocks, or elsewhere on Google/Youtube .

<br>
<hr>

> *USECASE 1*
 
capitalize or lower
perticularly used when you want to match any case but you dont know user will enter in 


... pass...     fill in later



<br>
<hr>


> *USECASE 2*
>> ** 2.1  Complete division problem**

```
problem statement : create a function that takes two arguments a,b int or float and divides a by b (a/b)
but, if the number is xomplete integer then program should return int form of number , otherwise float



For example

Input : 10/2
Output : 5

Input : 100/10
Output : 10

Input : 1/2
Output : 0.5

Input : 4/5
Output : 0.8


```
this problem can be solved via several diffrenet approaches

```python

# method 1 :using math.floor
import math 

def compl_div(a,b):
    c=round(a/b,5)
    if math.floor(c) == c:
        return int(c)
    else:
        return c
        
 
 ########################
 
 
 # second method is using string operaions
 
 def cdiv_str(a,b):
 
    if ('.' in str(a) or '.' in str(b)) and a!=b:
        return a/b
 
    else:
        
        c=str(a/b)
        
        if c.split('.')[1] == '0':
            return int(a/b)
        
        else:
            return a/b
    

```
<br>

>> **2.2 floor function and round function with strings**
```python

# round function implemented using string operations

def str_round(num,places):
    num=str(num)
    
    if type(places) == int :
        
        if places == 0:
                return int(num.split('.')[0])
        
        add = num.split('.')[0]+'.'
        add += num.split('.')[1][:places]
        
        return eval(add)
    
    else:
        print('places,second argument in function, has to be an integer')



#########################


# floor function implemented using string operations

 
def str_floor(num):

    if '.' not in str(num) :
        return num
    
    num2 = str(num).split('.')[0]
    return int(num2)




#########################


# floor function implemented using string operations


def str_ceil(num):

    if '.' not in str(num) :
        return num
    
    num2 = str(num).split('.')[0]
    return int(num2)+1

```


