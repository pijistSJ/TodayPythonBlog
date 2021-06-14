# Blog 2

This techincally doesn't require making a complete another blog ,
it's just a small trick type and teaches you something about bitwise operators

<br>

whenever it's said to be written a programme that filters even number or "A even number checker programmme"
we generally think of this block <br> <br>
```python
if num%2 == 0 :
    print(num)

'''
this block of code, in simple terms translates that,
if the num (number) is divisible by 2 then only print that number
'''

```
<br> <br>
but there's also one other way to do this using binary arithmatic
bitwise operators that is  <br> <br>
```python
if num & 1 == 0 :
    print(num)
```
<br> 
this block of code, in simple terms,
first, coverts num to its binary form and than does binary
AND operation of that number with 1

so how does that work

in binary number system numbers are measured in 
powers of 2 like ;

`. . .+ 2^4 + 2^3 +2^2 + 2^1 + 2^0 + 2^{-1} + 2^{-2} + 2^{-3} + . . .`

hence if number is even, when you convert it to binary
term `2^0` goes to 0 and hence any even binary number will
end in 0, also `AND` operation in binary is like nultiplication

hence any binary even number when `AND-ed ` with 1
for eample `1010 AND 0001` always results in 0
hence the block <br> <br> 
```python
if num & 1 == 0 :
    print(num)
``` 
<br> 
makes sense when used as even number filter 










