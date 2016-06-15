# Lec 2.5, slide 4
``` python
x = 3
x = x * x    # square value of x
print(x)
y = float(raw_input('Enter a number: '))
print(y * y)
```
# Lec 2.6, slide 2
``` python
x = int(raw_input('Enter an integer: '))
if x % 2 == 0:
    print('')
    print('Even')
else:
    print('')
    print('Odd')
print('Done with conditional')
```

# Lec 2.6, slide 4
``` python
x = 6

if x % 2 == 0:
    if x % 3 == 0:
        print('Divisible by 2 and 3')
    else:
        print('Divisible by 2 and not by 3')
elif x % 3 == 0:
    print('Divisible by 3 and not by 2')
else:
    print('Not divisible by 2 or 3');
```
# Lec 3.1, slide 2
``` python
# repetitive addition
x = 3
ans = 0
itersLeft = x
while (itersLeft != 0):
    ans = ans + x
    itersLeft = itersLeft - 1
print(str(x) + '*' + str(x) + ' = ' + str(ans))
```
# lecture 3.2, slide 4
``` python
# Find the cube root of a perfect cube
x = int(raw_input('Enter an integer: '))
ans = 0
while ans ** 3 < x:
    ans = ans + 1
if ans ** 3 != x:
    print(str(x) + ' is not a perfect cube')
else:
    print('Cube root of ' + str(x) + ' is ' + str(ans))
```
# lecture 3.2, slide 6
``` python
# Find the cube root of a perfect cube
x = int(raw_input('Enter an integer: '))
ans = 0
while ans ** 3 < abs(x):
    ans = ans + 1
if ans ** 3 != ans(x):
    print(str(x) + ' is not a perfect cube')
else:
    if x < 0:
        ans = -ans
    print('Cube root of ' + str(x) + ' is' + str(ans))
```
