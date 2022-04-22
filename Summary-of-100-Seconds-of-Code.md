--------------------------------------------------------------------------------------------------------------------------------------------

Video - 1 : Array Map 
Explanation : 

map() creates a new array from calling a function for every array element.
map() calls a function once for each element in an array.
map() does not execute the function for empty elements.
map() does not change the original array.

const persons = 
[
  {firstname : "Malcom", lastname: "Reynolds"},
  {firstname : "Kaylee", lastname: "Frye"},
  {firstname : "Jayne", lastname: "Cobb"}
];

persons.map(getFullName);

function getFullName(item) {
  return [item.firstname,item.lastname].join(" ");
}

Output : Malcom Reynolds,Kaylee Frye,Jayne Cobb

--------------------------------------------------------------------------------------------------------------------------------------------

Video - 2 : Big-O-Notation 
Explanation : 

Big O notation is a mathematical notation that describes the limiting behavior of a function when the argument tends towards a particular value or infinity.
In other words, Big O notation describes the complexity of your code using algebraic terms.

When we calculate big O notation, we only care about the dominant terms, and we do not care about the coefficients. Thus we take the n² as our final big O. We write it as O(n²), which again is pronounced “Big O squared”.

For example, the function g(n) = n² + 3n is O(n²)

-------------------------------------------------------------------------------------------------------------------------------------------

Video - 3 : Array Reduce 
Explanation :

The reduce() method executes a reducer function for array element.
The reduce() method returns a single value: the function's accumulated result.
The reduce() method does not execute the function for empty array elements.
The reduce() method does not change the original array.

Syntax : array.reduce(function(total, currentValue, currentIndex, arr), initialValue)

const numbers = [15.5, 2.3, 1.1, 4.7];
numbers.reduce(getSum, 0);

function getSum(total, num) 
{
  return total + Math.round(num);
}

Output : 24 

-------------------------------------------------------------------------------------------------------------------------------------------

Video - 4 : Recursion
Explanation :

A function that calls itself is known as a recursive function. And, this technique is known as recursion.
The recursion continues until some condition is met to prevent it.
To prevent infinite recursion, [ if...else ] statement (or similar approach) can be used where one branch makes the recursive call, and other doesn't.

Sum of Natural Numbers using Recursion :

#include <stdio.h>
int sum(int n);

int main() 
{
    int number, result;
    printf("Enter a positive integer: ");
    scanf("%d", &number);
    result = sum(number);
    printf("sum = %d", result);
    return 0;
}

int sum(int n) 
{
    if (n != 0)
        return n + sum(n-1); 
    else
        return n;
}


-------------------------------------------------------------------------------------------------------------------------------------------

Video - 5 : Javascript Module 
Explanation : 

A module is just a file. One script is one module.Modules can load each other and use special directives export and import to interchange functionality, call functions of one module from another one:

"export" keyword labels variables and functions that should be accessible from outside the current module.
"import" allows the import of functionality from other modules.
For instance, if we have a file sayHi.js exporting a function:

sayHi.js
export function sayHi(user) 
{
  alert(`Hello, ${user}!`);
}

Then another file may import and use it:

main.js
import {sayHi} from './sayHi.js';
alert(sayHi);
sayHi('John');

the import directive loads the module by path ./sayHi.js relative to the current file, and assigns exported function sayHi to the corresponding variable.

-------------------------------------------------------------------------------------------------------------------------------------------