## Functions 

* Js function are like a block whatever we define inside remain private and no one can access it from outside
* It can be invoke multiple time and can also be reused
* In Javascript every thing is an object even the function is and object
* Javascript behave like Js Variable
* Behaviour:- 

    * act like container
    * can be hoisted
    * has local and global scope
    * Are Object
    * Can Override

```javascript
//Normal defining a function

function hello(){
    console.log("Hello");
}
hello(); 

// Hello
```


### Function can be declared in two ways

* Function declaration

    - Declaration in done by function keyword and this will get hoisted

        ```js
    
        monday();

        function monday(){
            console.log("Good morning it's monday")
        }
        ```

* Assignment function

    - function is assigned to variable and it does not get hoisted instead if it's es5 variable then it will get hoisted
    
        ```js
            const print = function(val){
            console.log("Print ->", val)
            }
            const completeTask = function(b){
                const a = "200";
                const c = a * 5;
                b(c);
            }
            completeTask(print)
        ```
### Returning  a function from inside through outside function

* If we want to pass value through function or we want to access inner function from outside we can use return keyword

```Javascript

    function helloDouble(somedata){
        console.log("Hi" + somedata);
        function inner(){
            console.log(somedata * 2)
        }
        return inner;
    }
    var value = 10;
    var result = helloDouble(value);
    console.log(result);

    /* (return inner) This is returning a function  and it is an object means it is a pass by reference means it is not returning a function it is returning reference where the function is defined*/
```

`Safty measure to be taken to check whether we are calling a function or not and also we can handle if it returns empty function`

```javascript
!!inner && (typeof inner === "function") && inner()
```

### Function passing to another function as parameter

* When we are passing function to another function as parameter we are actually passing a reference of it

```js
const print = function(val){
    console.log("Print ->", val)
}
const completeTask = function(b){
    const a = "200";
    const c = a * 5;
    b(c);
}
completeTask(print)

//Output Print -> 1000
```

`! Note :- Never pass the hard code of function inside a function like the above example do not pass print directly into completeTask function `

### Higher order function

* Any function which takes function as a parameter and/or return function is called higher order function.

```js

var sport = function(){
    var football = function(player){
        var euro = function(team){
            return team
        }
        return euro;
    }
    return football;
}

var football = sport();
var result = football("Muller");
var final = result("Germany");
console.log(final); // Germany

/* Here euro is not a higher order function because it is neither returning function nor taking function as parameter*/
```

### Pure Function

* It is a function when you pass the value it will return same value and does not change the input value
* You cannot voilate the principle of pure function by just updating, adding, modifying the paramter which is pass

```js
function add(a, b){
    return a + b;
}
var one = 30;
var two = 50;
const result = add(one ,two);
console.log(result) //80
```

### IIFE - Immediately Invoked Function Expression / Self Executing Function Expression(SEF)

* It is use to execute function immediately. 
```js

(function()
{
console.log("Hello world");
})(); // Hello world
```
`Note:- Add semicolon(;) at start of function for safe guard`

### Arrow Function

* Basic Structure 
    ```js 
    var a = () =>{console.log("hi")}
    ```
* They are always function expression or function assignment not function declaration.
* No need of parenthesis if we are passing single parameter
* You can also pass arrow function in parenthesis 