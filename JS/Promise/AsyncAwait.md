### How async await code is written


```js
var task1 = function(){
    return new Promise(function(resolve, reject){
        setTimeout(()=>{
            resolve('Promise is resolve')
        }, 2000)
    })
}

var task2 = function(){
    return new Promise(function(resolve, reject){
        setTimeout(()=>{
            resolve('Promise is resolve')
        }, 3000)
    })
}


var task3 = function(vals){
    return new Promise(function(resolve, reject){
        setTimeout(()=>{
            resolve('Promise is resolve')
        }, 6000)
    })
}


;(async function(){
    const result = await task1();
    const result2 = await task2(result);
    const result3 = await task3(result2);

    console.log(result3)
})();
```


`Error handling in async`

```js
var task1 = function(){
    return new Promise(function(resolve, reject){
        setTimeout(()=>{
            resolve('Promise is resolve')
        }, 2000)
    })
}

var task2 = function(){
    return new Promise(function(resolve, reject){
        setTimeout(()=>{
            resolve('Promise is resolve')
        }, 3000)
    })
}


var task3 = function(vals){
    return new Promise(function(resolve, reject){
        setTimeout(()=>{
            resolve('Promise is resolve')
        }, 6000)
    })
}


;(async function(){
    try{
        const result = await task1();
        const result2 = await task2(result);
        const result3 = await task3(result2);
        console.log(result3)
    } catch(e){
        console.log('error from task', e);
    }
})();
```