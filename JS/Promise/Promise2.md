### Running promise one after another

```js
var promFunc = function(){
    return new Promise(function (resolve, reject) {
        setTimeout(() => {
            resolve({})
        }, 2000)
    })
}


var task2 = function(){
    return new Promise(function (resolve, reject) {
        setTimeout(() => {
            reject({})
        }, 3000);
    })
}

promFunc().then(function (data) {
    console.log("resolve",data);
    return task2();
}).then(function(data){
    console.log("data2", data)
}).catch(function(err){
    console.log(err)
})

//Output
/*
    resolve {}
    {}
*/
```


### Avoiding Promise Hell


```js

var withDrawMoney = function (data) {
    return new Promise(function (resolve, reject) {
        setTimeout(() => {
            resolve(data);
        }, 2000)
    });
}

var buyRice = function (data) {
    return new Promise(function (resolve, reject) {
        setTimeout(() => {
            resolve({
                money: data,
                rice: "rice",
            });
        }, 1000)
    });
}

var cookRice = function (data) {
    return new Promise(function (resolve, reject) {
        setTimeout(() => {
            resolve({
                rice: data
            });
        }, 4000)
    });
}


// withDrawMoney(100).then(function (data) {
//     console.log("money", data);
//     buyRice(data).then(function (val) {
//         console.log("Bought rice", val)
//         cookRice(val.rice).then(function (val) {
//             console.log("rice cooked", val)
//         }).catch(function (error) {
//             console.log("valerr", error)
//         })
//     }).catch(function (error) {
//         console.log("valerr", error)
//     })
// }).catch(function (err) {
//     console.log("error", err)
// })


// To avoid the above code we use promise chain or thenable, to also avoid multiple catch

withDrawMoney(100).then(function (data) {
        console.log("money", data);
        return buyRice(data)
    }).then(function (params) {
        console.log("Bought rice", params)
        return cookRice(params.rice)
    }).then(function (vals) {
        console.log("rice cooked", vals)
    })
    .catch(function (error) {
        console.log("valerr", error)
    })

//Output

/*
money 100
Bought rice { money: 100, rice: 'rice' }
rice cooked { rice: 'rice' }
*/
```