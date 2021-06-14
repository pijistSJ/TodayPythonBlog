# Blog-1 

I found this problem in online book of Christian Hill
[here](https://scipython.com/book2/chapter-2-the-core-python-language-i/questions/using-a-list-to-represent-a-polynomial/)

go through the problem and understand what is has to say, also Christian Hill is one of god authors in ``computational physics`` field

if incase link has some problem, here i rewrite the problem as it is given in the book

```python

'''
Using a list to represent a polynomial
Question Q2.4.2
A list could be used as a simple representation of a polynomial, P(x),
with the items as the coefficients of the successive powers of x,
and their indexes as the powers themselves.

Thus, the polynomial P(x)=4+5x+2x3 would be represented by the list [4, 5, 0, 2].
Why does the following attempt to differentiate a polynomial fail to produce the correct answer?

'''

######################################

P = [4, 5, 0, 2]
dPdx = []
for i, c in enumerate(P[1:]):
    dPdx.append(i*c)
dPdx
[0, 0, 4]            # wrong!

######################################

'''
How can this code be fixed?
'''


```

<br> <br> 
~~~
My version/modification to this problem is 
~~~

<br> <br> 
```
Write a program/function that returns a string that is
output of differentiation of input string

Input string has to be polynomial only in X
AND 
increasing form of power only


For example

Input : "5+4x+3x**2+2x**3"

Output : "4+6x+6x**2"


Also if polynomial have some step missing for example 
Input is   5x³ + 4x + 2
Then also input string has to be 
2+4x+0x**2+5x**3 


"WARNING"  ::  Do not use any library, only do it with
               help of lists strings dictionaries and pure logic
               
NOTE :: Program , when returning, should not return x**1 in string,
        only coefficient with x should be returned,
        
        for example;
        
        2+3x**1+4x**2+5X**3   # WRONG
        2+3x+4x**2+5X**3   # RIGHT


SIMILAR PROBLEM / SUB PROBLEM STATEMENT :: similarly create function/program for integration

```
