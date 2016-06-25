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
# Only works for positive integers
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
# lecture 3.3, slide 3
``` python
# Find the cube root of a perfect cube
x = int(raw_input('Enter an integer: '))
for ans in range(0, abs(x) + 1):
    if ans ** 3 == abs(x):
        break
    if ans ** 3 != abs(x):
        print(str(x) + ' is not a perfect cube')
    else:
        if x < 0:
            ans = -ans
        print('Cube root of ' + str(x) + ' is ' + str(ans))
```
# lecture 3.4, slide 3
``` python
# Given a decimal number, we can convert it into binary form.
num = 302

if num < 0:
    isNeg = True
    num = abs(num)
else:
    isNeg = False
result = ''
if num == 0:
    result = '0'
while num > 0:
    result = str(num % 2) + result   # next bit
    num = num / 2       # shift left
if isNeg:
    result = '-' + result      # do a conversion back
```
# lecture 3.4, slide 4
``` python
x = float(raw_input('Enter a decimal number between 0 and 1: '))

p = 0
while((2 ** p) * x) % 1 != 0:
  print('Remainder = ' + str((2 ** p) * x - int((2 ** p) * x)))
  p += 1
num = int(x * (2 ** p))

result = ''
if num == 0:
  result = '0'
while num > 0:
  result = str(num % 2) + result
  num = num / 2

for i in range(p - len(result)):
  result = '0' + result

result = result[0:-p] + '.' + result[-p:]
print('The binary representation of the decimal ' + str(x) + ' is ' + str(result))
```
# lecture 3.5, slide 2
``` python
x = 25
epsilon = 0.01
step = epsilon ** 2
numGuesses = 0
ans = 0.0
while (abs(ans**2 - x)) >= epsilon and ans <= x:
  ans += step
  numGuesses += 1
print('numGuessses = ' + str(numGuesses))
if abs(ans**2 - x) >= epsilon:
  print('Failed on square root of ' + str(x))
else:
  print(str(ans) + ' is close to the square root of ' + str(x))
```
