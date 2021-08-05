### Array

* It is a special kind of object
* It store value of different type
* To access array element we make use of index

**How to declare array**
 
 ```js
 //basic syntax to declare an array

   var arr = ["eiusmod","culpa","ullamo", 20, true];
   console.log(arr);
 ```

 #### Basic things with array

 * **How to add something in array**

    ```js

        var arr = ["eiusmod","culpa","ullamo", 20, true];

        arr[7] = "nate";
        console.log(arr); //(8) ["eiusmod", "culpa", "ullamo", 20, true, empty × 2, "nate"]
    ```
 * See the length of array

    `Index of an array is calculated as last index plus one`

    ```js
    console.log(arr.length) //8
    ```

 * **Add element at last index of array**

    ```js
    var arr = ["eiusmod","culpa","ullamo", 20, true];
    arr[arr.length] = "Prasad"
    console.log(arr)
    ```
### Array methods

1. **push** 
    - It is built in method used to add item at end of array

    ```js
    var arr = ["eiusmod","culpa","ullamo", 20, true];
    arr.push(40,"City");
    console.log(arr); // ["eiusmod", "culpa", "ullamo", 20, true, 40, "City"]
    ```
1. **pop**
    - Use to remove item from end of an array

    ```js
    var arr = ["eiusmod", "culpa", "ullamo", 20, true, 40, "City"];
    arr.pop();
    console.log(arr); // ["eiusmod", "culpa", "ullamo", 20, true, 40]
    ```
1. **unshift**

    - To add item at start of an array

    ```js
    var arr = ["eiusmod", "culpa", "ullamo", 20, true, 40, "City"];
    arr.unshift("Hello");
    console.log(arr); // ["Hello","eiusmod", "culpa", "ullamo", 20, true, 40]
    ```
1. **shift**

    - To remove item from start position of an array
    ```js
        var arr = ["eiusmod", "culpa", "ullamo", 20, true, 40, "City"];
        arr.shift();
        console.log(arr); // ["eiusmod", "culpa", "ullamo", 20, true, 40]
    ```

1. **forEach**
    
    - forEach method is use to iterate through array elements

    ```js
    var arr = ["eiusmod", "culpa", "ullamo", 20, true, 40, "City"];

    //Traditional way
    var val
    for(let i=0; i<arr.length;i++){
        val += arr[i] + " ";
    }
    console.log(val) //  eiusmod culpa  ullamo  20  true  40   City 

    //Using forEach method

    var loop = function(item){
        console.log("Items =>", item);
    }

    arr.forEach(loop)

    /*
    Output :- Items => eiusmod
              Items => culpa
              Items => ullamo
              Items => 20
              Items => true
              Items => 40
              Items => City
    */
    ```
1. **map**

    - It iterate through array item and return new array
    - It is also called transforming array

    ```js

    var arr = ["eiusmod", "culpa", "ullamo", 20, true, 40, "City"];

    var newArr = arr.map(function(item){
        let value = item + "One";
        return value;
    })

    console.log(newArr) // ["eiusmodOne", "culpaOne", "ullamoOne", "20One", "trueOne", "40One", "CityOne"]
    ```
1. **filter**

    - Filter Method is use to filter out the element from array which has certain condition

    ```js

    // Filter out the array Item that contains number

    var arr = ["eiusmod", "culpa", "ullamo", 20, true, 40, "City"];

    var filt = arr.filter(function(item){
        return typeof item !== 'number'
    })

    console.log(filt)
    ```
1. **join**

    - It returns array as a string

    ```JS

    var arr = ["eiusmod", "culpa", "ullamo", 20, true, 40, "City"];

    var filt = arr.join(" ")

    console.log(filt) //eiusmod culpa ullamo 20 true 40 City

    ```

