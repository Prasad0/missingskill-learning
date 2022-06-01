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


# Example to solve

- Write a function which takes function as parameter

```js
    function f2(){
        console.log("Hello");
    }

    function getFun(demo){
    if(typeof demo === 'function'){
        demo();
    }
    }

    getFun(f2);
```

- Write a function which takes function as parameter and function should be an inline function.

```js
    function getFun(demo){
    if(typeof demo === 'function'){
        demo();
    }
    }

    getFun(function (){
        console.log("Hello");
    });
```


-  Write a function which returns another function

```js
    function getFun(){
        let demo = function(){
            console.log("hello")
        }

        return demo
    }

    var f1 = getFun();
    (typeof f1 === 'function') && f1()
 
```

- Write a function which returns another function and inner function takes one parameter, 
print the parameter when inner function is called.

```js

    function mainFn(){
        let inner = function(main){
            console.log("inner", main)
        }
        return inner;
    }

    let val = mainFn();

    val("function")
```
- write a function which execute itself the moment it declared. should be called only once

```js
    ;(function(){
        console.log("It a iife function")
    })();
```


- Write a function which takes function as parameter, return the same function as a output

```js
    var f1 = function(cb){
        return cb
    }

    var fn = function(){
        console.log("Called");
    }


    var result = f1(fn);
    result();
```

- Write a function which take 2 function as a parameter and call both the function

```js
    var f1 = function(cb1, cb2){
        (typeof cb1 === 'function') && cb1();
        (typeof cb2 === 'function') && cb2();
    }

    var fn1 = function(){
        console.log('fn1 is called');
    }

    var fn2 = function(){
        console.log('fn2 is called');
    }

    f1(fn1, fn2);
```