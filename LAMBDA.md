Lambda Function:

A lambda function is a small anonymous function.

A lambda function can take any number of arguments, but can only have one expression.

Syntax:

lambda arguments : expression

The expression is executed and the result is returned.


```python
# Add 10 to argument a, and return the result:

x = lambda a : a + 10
print(x(5))
```

    15
    

Lambda functions can take any number of arguments:


```python
# Example
x = lambda a, b : a * b
print(x(5, 6))
```

    30
    


```python
# Example
# Summarize argument a, b, and c and return the result:

x = lambda a, b, c : a + b + c
print(x(5, 6, 2))
```

    13
    

Higher Order Functions:

->
A function is called Higher Order Function if it contains other functions as a parameter or returns a function as an output 

i.e, the functions that operate with another function are known as Higher order Functions.

Map, Filter, Reduce

Map():

* The map() function executes a specified function for each item in an iterable.
* The item is sent to the function as a parameter.

Syntax:

map(function, iterables)

* function = The function to execute for each item

* iterable = A sequence, collection or an iterator object. You can send as many iterables as you like, just make sure the      function has one parameter for each iterable.




```python
# Example
# Make new fruits by sending two iterable objects into the function:

def myfunc(a, b):
  return a + b

x = map(myfunc, ('apple', 'banana', 'cherry'), ('orange', 'lemon', 'pineapple'))

print(list(x))

```

    ['appleorange', 'bananalemon', 'cherrypineapple']
    

Filter():

* The filter() function returns an iterator where the items are filtered through a function to test if the item is accepted or not.

Syntax

filter(function, iterable)

* function = A Function to be run for each item in the iterable
* iterable = The iterable to be filtered


```python
## filter:
list(filter(lambda x: True if x%2==0 else False,[1,2,3,4,5]))
```




    [2, 4]




```python
list(filter(lambda x:True if x in "aeiouAEIOU" else False,"string"))
```




    ['i']




```python
list(filter(lambda x:True if x.isalnum() else False,'Abc$#123'))
```




    ['A', 'b', 'c', '1', '2', '3']




```python
list(filter(lambda x:True if x.isalnum() is False else False,'Abc$#123'))
```




    ['$', '#']



Reduce():
   
   The reduce(fun,seq) function is used to apply a particular function passed in its argument to all of the list elements mentioned in the sequence passed along.This function is defined in “functools” module.
   
   Working :  

* At first step, first two elements of sequence are picked and the result is obtained.

* Next step is to apply the same function to the previously attained result and the number just succeeding the second element and the result is again stored.

* This process continues till no more elements are left in the container.

* The final returned result is returned and printed on console.


![OIP%20%282%29.jpg](attachment:OIP%20%282%29.jpg)


```python

```
