# Blog-1 

I found this problem in online book of Christian Hill
[here](https://scipython.com/book2/chapter-2-the-core-python-language-i/questions/using-a-list-to-represent-a-polynomial/)

go through the problem and understand what is has to say, also Christian Hill is one of god authors in ``computational physics`` field

if incase link has some problem, here i rewrite the problem as it is given in the book
'''
Using a list to represent a polynomial
Question Q2.4.2
A list could be used as a simple representation of a polynomial, P(x), with the items as the coefficients of the successive powers of x, and their indexes as the powers themselves. Thus, the polynomial P(x)=4+5x+2x3 would be represented by the list [4, 5, 0, 2]. Why does the following attempt to differentiate a polynomial fail to produce the correct answer?
'''
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
