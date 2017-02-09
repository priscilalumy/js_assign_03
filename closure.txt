Closure

A closure is a function inside another function that can access the variables and parameters from the parent function, even if it is already closed.

This is an example of this definition:  

function sumOne () {
    let sum = 0;
    return function (counter) {
        return sum += counter;   
    }
}

let num = sumOne()
console.log(num(5));
//5
console.log(num(10));
//15

Explanation:

The variable num will return the value of a function.

This function sumOne will run only once. It will set the variable sum to 0 (zero) and return the value of an inner function.

That inner function will add a value to the parameter counter.

When the variable num is called and runs the function, the variable sum will keep the value after the function is closed. So when the variable num is called and runs the function again, that specific instance of counter parameter will be used to run the function.




References:
Eloquent Javascript
http://eloquentjavascript.net/03_functions.html
MDN – Mozilla Developer Network
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures
W3schools
http://www.w3schools.com/js/js_function_closures.asp
Javascript. Is Sexy
http://javascriptissexy.com/understand-javascript-closures-with-ease/
