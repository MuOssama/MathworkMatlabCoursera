# **MathworkMatlabCoursera**
## Mathworks Matlab Coursera course solution
**Syntax**
### Arithmatic operators
#### - + / * %
like any prrogramming language
>output = x + y   
>output = x - y

and so on...
NOTE: if you want to use reminder dont use % like in C/C++/python 
you have to use mod func
bec % in matlab is used for comments
>output = mod(10,3)

>output = 1 

### Matrices operators
#### Building matrix
>ones(rows,columns) %making matrix having all ones

>zeros(rows,column) %making matrix having all zeros
#### Addition and substractions
the matrix must have the same dimentions
>x=[1 2 3]; % x is 1 rows 3 coulmns

>y=[4 5 6]; % y is 1 rows 3 coulmns

>output = x+y

>output = [ 5 7 9]

you can use size() func to know the size of the array
>size(x)

>x =  1 3

#### multiplication
in matlab wde have ton types of multiplictions
x*y and x.*y
the x*y is the ordanary multiplication
>output = x*y

>dimention error as x is 1x3 and y 1x3 >>> it must be mx3 and 3xn and the size of the output will be mxn

you can transpoze the y matrix to be 3x1 by using y'
>output = x*y'

>output = [32] the answer is matrix of 1x1 as we expected

the x.*y is used to multiply every element to the corresponding  element in the other
so the two element must be the same dimentions
>output = x.*y

>output =  [4 10 18]

this bec [1x4 2x5 3x6]
NOTE the . can be used for power "^" or for division "/"
>output = x./y

>output = [0.25 0.4 0.5]

ie output is [1/4 2/5 3/6]
### Functions
#### syntax
function [] = func_name(param1, param2, , )

end
for example:
function [add, sub] = operations(op1, op2)
add = op1+op2
sub = op1-op2
end
>operations(6,5)
>output=[11,1]

thats bec. it returns 11 which is add and 1 which is sub

