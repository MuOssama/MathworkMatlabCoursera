# **MathworkMatlabCoursera**
## Mathworks Matlab Coursera course solution
## **Content**
>1- Operators\
>2- Matrices operators\
>3- Functions\
>4- inputs and outputs\
>5- Plotting\

## **Syntax**
### 1 operators
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
### Logical operators
logic operators\
& and\
| or\
~ not
### relational operators
< > == <= >=
### 2 Matrices operators
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

#### indexing
>T=ones(3,3) %building a 3x3 matrix all its elements are ones\
>T(n,m) is to get the element at row n and column m\
>T(1,1) is to get the element at row one and column one
#### slicing and ranging
consider this T matrix\
T = 1 1 1\
    2 2 2\
    3 3 3
    
>T(a:b,x:y)

this will get slice of the T matrix from rows a to b and columns from x and y\
let a =1, b=2, x=1, and y=2

>T(1:2,1:2)

T =\
1 1\
2 2\
this is a sub matrix that slice the first 2 rows and the first t columns of matrix T

### 3 Functions
#### syntax
function [] = func_name(param1, param2, , )

end
for example:
function [add, sub] = operations(op1, op2)
add = op1+op2
sub = op1-op2
>operations(6,5)

>output=[11,1]

thats bec. it returns 11 which is add and 1 which is sub

NOTE: you can use many functions in one file.m
but only the first one will be accessed outside
this is useful when a complex function, so rather
than writing all thing in one function, multliple 
function could be written then one main function 
calls them, i.e one main function calls subfunctions

NOTE return statement finishes the function 
### 4 inputs and outputs
you can take inputs from user with input()
>x = input('enter a number)

you can output with fprintf() like in c programming
>fprintf('the value you entered %d', x)

remember %d is to output an integer
remember... \
%d integer \
%u unsigned integer \
%f float \
%c char \
%s string
#### nargin and nargout
built-in functions\
nargin returns the number of inputs\
nargout returns the number of outputs
#### local global persistent variables
local variables: variables that alive in a scope and get deleted after the function excutes\
global variables: variables that alive in the whole programm and could be called anywhere\
persistent variables: local variables in the functions but never get deleted, it can be usefel in cases\
such; you want to keep track a variable like how many time the function get called\
persistent variables like static local variables in c programming language
>function out=func(in)\
>persistent times_called\
>if isempty(times_called)\
count = 0; % Initialize count to 0 if it's empty\
>else\
>times_called=times_called+1\
>end\
>end
### 5 Plotting
to plot functions\
**for more visual deiatls**
NOTE: you can show the matlab live code at : [Matlab Live Code](https://github.com/MuOssama/MathworkMatlabCoursera/blob/main/plottingLiveCode.mlx)\
NOTE: you can show pdf for matlab live code at: [pdf for the code](https://github.com/MuOssama/MathworkMatlabCoursera/blob/main/plottingLiveCode.pdf])
#### figure()
to make a new figure to plot 
to select existing figure for plotting or editing
#### plot(x1,y1,options)
x1 is the horzental vector
y1 is the vertical options
options could be 'color' like\
'b' blue\
'r' red\
'k' black\
#### plot(x1,y1,options,x2,y2,options)
for multiple plotting on the same figure

#### hold on
to plot mutiple function also\
>plot(x1,y1) %plotting first function\
>hold on\
>plot(x2,y2) %plotting another functions on the same figure

you can use plot as alternative:
>plot(x1,y1,x2,y2)

NOTE: to turn off hold on state
>hold off

#### styling the graph
##### grid() %to show grids on the figure
##### title() %to add title to the figure
##### legand() %to show what color related to which graph
##### xlabel() %to give x axis title
##### ylabel() %to give y axis title

#### close()
for closing a figure
#### closeall()
for closing all figures

### 6 Loops
#### for loops
for loop syntax:\
for var = range\
end
> sum=0
>for i=1:1:10\
>sum=sum+i\
>end\
>sum=55

you can also use for loop to iterate a list like in python prog lang
>m = randi(2,2)\
>for item = m\
>fprintf('%d\n',item)\
>end

this will print all the matrix element

#### while loops


