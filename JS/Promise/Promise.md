# Promise

-    A Promise is a proxy for a value not necessarily known when the promise is created. It allows you to associate handlers with an asynchronous action's eventual success value or failure reason. This lets asynchronous methods return values like synchronous methods: instead of immediately returning the final value, the asynchronous method returns a promise to supply the value at some point in the future.

- A Promise is in one of these states:

    1. pending: initial state, neither fulfilled nor rejected.
    1. fulfilled: meaning that the operation was completed successfully.
    1. rejected: meaning that the operation failed.

`Promise demo`
    ![image](../../image/promises.png)



### Promise in Layman terms

Think of it as a conversation between two people:

> Alex: Hey Mr. Promise! Can you run to the store down the street and get me itemA for this dish we are cooking tonight?

> Mr. Promise: Sure thing!

> Alex: While you are doing that, I will prepare itemB(asynchronous operation). But make sure you let me know whether you could find itemA (promise return value).

> Mr. Promise: What if you are not at home when I am back?

> Alex: In that case, send me a text message saying you are back and have the item for me (success callback). If you don’t find it, call me immediately (failure callback).

> Mr. Promise: Sounds good! See you in a bit.

So simply speaking, promiseobject is data returned by asynchronous function. It can be a resolveif the function returned successfully or a rejectif function returned an error.

### Consuming promise


```js

    run.then(function(data){
        console.log(data)
        //this executes after promise is resolved 
        //we write logic here after promise is completed
    }).catch(function(err){
        console.log(err)
        // this executes after promise is rejected
        // we write logic what to do after rejection
    })
```

` then -> is called when promise is fullfilled or resolved , catch -> is called when promise is reject`


### Creating Promise

```js

// Promise(function(){

// })


// var promise = new Promise(function(){

// })

//creating promise

//no need of specific name resolve, reject type any but first parameter is fullfiled and another one is unfullfiled

var promise = new Promise(function(resolve, reject){
    //her you have to write api call or db call for now to mimic we have used setTimeout web api
    setTimeout(function(){
        resolve(20);
    }, 2000);
});
//Promise taking a function which is receiving two parameters

//consuming promise

promise.then(function(data){
    console.log("data", data);
}).catch(function(error){
    console.log("error", error);
})

//op 
// data 20



// Promise defination wrapped in function

function execute(){
    var promise = new Promise(function(resolve, reject){
        setTimeout(function(){
            resolve(20)
        }, 2000);
    })

    return promise;
}

execute().then(function(data){
    console.log('data', data);
}).catch(function(error){
    console.log('error', error);
})
```

`In promise you can use as many as then you can`

- In the bellow example the output of first then which we return will be the input for second then

- If you are consuming promise and passing multiple then so it is called 'Promise chaining or thenable'. 

```js

function execute(){
    var promise = new Promise(function(resolve, reject){
        setTimeout(() => {
            resolve(20);
        }, 3000)
    });

    return promise;
}

var run = execute();

run.then(function (data) {
    console.log("data1", data)
    return data + 2;
}).then(function(data){
    console.log("data2", data)
}).catch(function(err){
    console.log(err);
})

//Output
/*
    data1 => 20
    data2 => 22
*/
```

- To break then in between

```js

function execute(){
    var promise = new Promise(function(resolve, reject){
        setTimeout(() => {
            resolve(20);
        }, 3000)
    });

    return promise;
}

var run = execute();

run.then(function (data) {
    console.log("data1", data)
    return data + 2;
}).then(function(data){
    console.log("data2", data)
}).then(function(data){
    throw 'error' // this will break the code in between
    console.log("data2", data)
}).then(function(data){
    console.log("data2", data)
}).catch(function(err){
    console.log(err);
})

//Output
/*
    data1 => 20
    data2 => 22
*/
```
