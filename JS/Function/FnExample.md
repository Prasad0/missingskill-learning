## Function Example

```js

//IIFE 

;(function(p1){
    console.log("Value", p1)
})(10);

//output -> Value 10

/*
    - In IIFE the function is immediately invoke once it have been called
    - In the above example we have passed the parameter 10 which will be passed in above function p1
*/



var input2 = function(){
    console.log("Input 2 is called");
}

;(function(callback){
    (typeof callback === "function") && callback();
})(input2);

// In the above function we are passing input2 as a parameter and IIFE is receiving input2 as a parameter so we are getting output as "Input 2 is called"

// But if we call input2() in another line still input2 will get executed  so avoid this we can pass the function inline only as shown below

;(function(cb){
    (typeof cb === "function") && cb();
})(function(){
    console.log("Input 2 is called")
})

```



```js

//Function as an expression

var invoke = function(){
    const value = 20;

    return value;
}

const result = invoke();
console.log(result);

/*
    Output => 
*/
```