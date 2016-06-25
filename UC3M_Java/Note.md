# LeapYear
``` Java
if(year % 4 != 0)
  return false;
else if(year % 100 != 0)
  return true;
else if(year % 400 != 0)
  return false;
else
  return true;
```
is equivalent to: 

``` Java
if(year % 4 != 0)
  return false;
else if(year % 4 == 0 && year % 100 != 0)
  return true;
else if(year % 4 == 0 && year % 400 != 0)
  return false;
else
  return true;
```
and in turn is equivalent to:

``` java
if(year % 4 != 0)
  return false;
else if(year % 4 == 0 && year % 100 != 0)
  return true;
else if(year % 4 != 0 || year % 400 == 0)
  return true;
else 
  return false;
```

``` java
return((year % 4 == 0 && year % 100 != 0) || year % 400 == 0);
```