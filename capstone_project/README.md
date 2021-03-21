# Data Preparation
Data is present in a single file with problem statemnt beginning as '#' and then the solution in python. We need to separate these two as input and output and then tokenize both of them respectively.
  - When a line starts as a '#' consider that as input
  - All other lines to be considered as code.
  - replace '\n' as and ' ' as for easy tokenization of pyhton code and store as output.

Split and Store the data in a csv format for easy read.
define the python code tokenizer.
We need to split the code wherever we find the following: split_points = ['<space>', ':', '<new_line>', '(', ')', '[', ']', '>', '<', '=', "'", '"', '.', '%', ',', '+', '-', '*', '\t', '{', '}', '/']

# Python code embedding
Data after splitting on above points each can be conidered as a delimeter and used for embedding training while training the model.

# Evaluation Metrics
Bleu score has been used for evaulation

# 25 Examples
### problem statement:
## write a python function to count how many times the predicate is true
### truth:
```
def quantify(iterable, pred=bool):
    return sum(map(pred, iterable))
```
### prediction:
```
def quantify(iterable, pred=bool):
    return sum(map(pred, iterable))
```
### problem statement:
## write a function to return the angualr veolcity based on augualr distance travelled in radian unit and time taken
### truth:
```
def cal_angular_velocity(angular_dist:float,time:float)->float:
    return angular_dist/time
```
### prediction:
```
def cal_angular_velocity(angular_dist:float,time:float)->float:
    return angular_dist/time
```
### problem statement:
## write a function to calculate the total capacitance of capacitors in parallel in a given list
### truth:
```
def cal_total_cap_in_parallel(cap_list:list)->float:
    return sum(cap_list)
```
### prediction:
```
def cal_total_cap_in_parallel(cap_list:list)->float:
    return sum(cap_list)
```
### problem statement:
## write a functin that returns the lcm of two input numbers
### truth:
```
def lcm(a, b):
    if a>b:
        min_ = a
    else:
        min_ = b
    while true:
        if min_%a==0 and min_%b==0:
            break
        min_+=1
    return min_
```
### prediction:
```
def lcm(a,b):
    lcm.multiple=lcm(a*b)
    if(a>b):
          greater = x
    else:
        greater = y
    while(true):
        if(((greater % x == 0) and (greater % y == 0))):
            lcm.append(greater)
               break
        if(greater + 1):
               lcm(greater += 1)
      return lcm
```
### problem statement:
## write a function to calculate the gravitational force between two objects of mass m1 and m2 and distance of r between them
### truth:
```
def cal_gforce(mass1:float,mass2:float, distance:float)->float:
    g = 6.674*(10)**(-11)
    return (g*mass1*mass2)/(distance**2)
```
### prediction:
```
def cal_gforce(mass1:float,mass2:float, distance:float)->float:
    g = 6.674*(10)**(-11)
    return (g*mass1*mass2)/(distance**2)
```
### problem statement:
## write a python program to convert kilometers to miles
### truth:
```
kilometers = 10.0
conv_fac = 0.621371
miles = kilometers * conv_fac
print('%0.2f kilometers is equal to %0.2f miles' %(kilometers,miles))
```
### prediction:
```
kilometers = float(input('enter temperature in kilometers: '))
conv_fac = 0.621371
miles = kilometers * conv_fac
print('%0.2f kilometers is equal to %0.2f %(kilometers,miles))
```
### problem statement:
## write a function to return the surface area of a sphere
### truth:
```
def cal_area_sphere(radius):
    pi = 3.14
    return 4*pi*(radius**2)
```
### prediction:
```
def cal_area_sphere(radius):
    pi = 3.14
    return 4*pi*(radius**2)
```
### problem statement:
## python code to get kth column of matrix
### truth:
```
def kth_column(test_list=[[4, 5, 6], [8, 1, 10], [7, 12, 5]],k=2):
    print('the original list is : ' + str(test_list))
    k =k
    res = list(zip(*test_list)[k])
    print('the kth column of matrix is : ' + str(res))
```
### prediction:
```
def kth_column(test_list=[[4, 5, 6], [8, 1, 10], [7, 12, 5]]]
    k=test_list[0]
      k =k[k]
    while len(test_list) test_list):
          r = k[k]
            result = list(filter(lambda x: x[k], test_list))
              print('the kth column of matrix is matrix : ' + str(res))
```
### problem statement:
## write a function to return the total surface area of a cuboid of length l , bredth b and height h
### truth:
```
def cal_surface_area_cuboid(l,b,h):
    return 2*(l*b+b*h+h*l)
```
### prediction:
```
def cal_surface_area_cuboid(l,b,h):
    return 2*(l*b+h*h+h*l)
```
### problem statement:
## write a python program to multiply two list with list comprehensive
### truth:
```
l1=[1,2,3]
l2=[4,5,6]
print([x*y for x in l1 for y in l2])
```
### prediction:
```
l1 = [1,2,3]
l2 = [4,5,6]
print([5,8,7,3,2])
```
### problem statement:
##   write a python program to iterate an dict and concatenate
### truth:
```
d=dict(p='san', q='foundry')
print('{p}{q}'.format(**d))
```
### prediction:
```
d=dict(p='san', q='foundry')
print('{p}{p}{q}'.format(*****2}))
```
### problem statement:
## write a program to display date and time
### truth:
```
import datetime
now = datetime.datetime.now()
time= now.strftime('%y-%m-%d %h:%m:%s')
print(f'current date and time : {time}')
```
### prediction:
```
import datetime
print(datetime.now())
```
### problem statement:
## write a python program for creating the thread
### truth:
```
import threading
from threading import thread
import time
def print_time( threadname, delay):
    count = 0
    while count < 5:
        time.sleep(delay)
        count += 1
        print('%s: %s' % ( threadname, time.ctime(time.time()) ))
```
### prediction:
```
import time
def print_loop_with_delay(sec):
    for i in range(0, 10):
        time.sleep(sec)
        print(i)
```
### problem statement:
## write a function to return the area of a circle of raidus r
### truth:
```
def cal_area_circle(r):
    pi = 3.14
    return pi*r**2
```
### prediction:
```
def cal_area_circle(r):
    pi = 3.14
    return pi*r**2
```
### problem statement:
## write a function to return the total surface area of a cube of side a
### truth:
```
def cal_surface_area_cube(a):
    return 6*(a**2)
```
### prediction:
```
def cal_surface_area_cube(a):
    return 6*(a**2)
```
### problem statement:
## write a program to print all the even numbers in a range
### truth:
```
r1, r2 = 1, 28
for _ in range(r1, r2+1):
  if _%2 == 0:
    print(_)
```
### prediction:
```r1, r2 = 1, 28
for _ in range(r1, r2+1):
  if _%2 == 0:
    print(_)
```
### problem statement:
## python program to implement gnome sort
### truth:
```
def gnomesort(arr, n):
    index = 0
    while index < n:
        if index == 0:
            index = index + 1
        if arr[index] >= arr[index - 1]:
            index = index + 1
        else:
            arr[index], arr[index - 1] = arr[index - 1], arr[index]
            index = index - 1
    return arr
arr = [34, 2, 10, -9]
n = len(arr)
arr = gnomesort(arr, n)
print('sorted seqquence after applying gnome sort :')
for i in arr:
    print(i)
```
### prediction:
```
def gnomesort(arr, n):
    index = 0
    while index < n:
        if index == 0:
            index = index + 1
        if arr[index] >= arr[index - 1]:
            index = index + 1
        else:
            arr[index], arr[index - 1] = arr[index - 1]
                  index = index - 1
    return arr
arr = [34, 2, 10, -9]
n = len(arr)
arr = gnomesort(arr, n)
print('sorted seqquence after applying gnome sort :')
for i in arr:
    print(i)
```
### problem statement:
## write a program to extract and print digits of a number in reverse order . the number is input from user .
### truth:
```
num = int(input('enter a number with multiple digit: '))
n=0
while num>0:
    a = num%10
    num = num - a
    num = num/10
    print(int(a),end='')
    n = n + 1
```
### prediction:
```
n=int(input('enter number: '))
rev=0
while(n>0):
    dig=n%10
    rev=rev*10+dig
    n=n//10
print('reverse of the number:',rev)
```
### problem statement:
## write a function to calculate the pressure p of ideal gas based on ideal gas equation - volume v , and temperatue t are given
### truth:
```
def find_pressure_of_ideal_gas(volume:float, temp:float,n:float)->float:
    r = 8.3145 ## gas constant r
    return (n*r*temp)/volume
```
### prediction:
```
def find_pressure_of_ideal_gas(volume:float, temp:float,n:float)->float:
    r = 8.3145 ## gas constant r
    return (n*r*temp)/volume
```
### problem statement:
## write a python function that finds square roots of a given number , if the square root is an integer , else returns the message error - the square root is not an integer " "
### truth:
```
def find_integer_square_roots(num):
    found = false
    for k in range(1, (num//2)+1):
        if ((k**2)==num):
            found = true
            break
    if not found:
        return 'error - the square root is not an integer'
    return -k, k
```
### prediction:
```
def find_integer_square_roots(num):
    found = false
    for k in range(1, (num//2)+1):
        if (k**2)==num):
             found = true
            break
    if not found:
        return 'error - the square root is not an integer'
    return -k, k
```
### problem statement:
##   write a python program to do lstrip on string
### truth:
```print('xyyzxxyxyy'.lstrip('xyy'))
```
### prediction:
```print('xyyzxxyxyy'.lstrip('xyy'))
```
### problem statement:
## write a python program to break when the num is perfectly divisible
### truth:
```
i = 1
while true:
    if i%3 == 0:
        break
    print(i)
 
    i+= 1
```
### prediction:
```
i = 1
while true:
    if i%3 == 0:
        break
     else:
    print(i)
```                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          
### problem statement:
## write a function that takes number of disks in tower of hanaoi problem and returns the minimum number of steps required
### truth:
```
def hanoi(x):
    if x == 1:
        return 1
    else:
        return 2*hanoi(x-1) + 1
```
### prediction:
```
def hanoi(x):
    if x == 1:
        return 1
    else:
        return 2*hanoi(x-1) + 1
```
### problem statement:
## write a python program to explain enclosing and global scope
### truth:
```
x = 'global'
def f():
    x = 'enclosing'
    def g():
        print(x)
    g()
    return x
obj1 = f()
print('explain global scope:',obj1)
```
### prediction:
```
a = 'hello world!'
b = a + b
print('a is b, a = a good a + b)
```
