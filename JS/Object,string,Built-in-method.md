### Object

* In Object items are stored in key value format
* Object can be created using object literal or using object keywords

```js

    const user = {
        "id" : 332,
        "name" : "Prasad",
        "city" : "Mumbai",
        "age" : 23,
        "Edu" : "MCA",
        "skills" : ["Js","linux","Bootstrap","css"]
    }

    //how to access object

    console.log(user.name) // Prasad

    // how to access object from array element

    console.log(user.skils[0]) //Js

```

**this keyword**

 - In js if method is attach to object then only this keyword will point to it's function else it will point to global

 - arrow function alway retain its parent function. So this will point to nearest parent function

```js

    const user = {
    "id" : 332,
    "name" : "Prasad",
    "city" : "Mumbai",
    "age" : 23,
    "Edu" : "MCA",
    "skills" : ["Js","linux","Bootstrap","css"],
    "getPrimitive" : function(){ //method
        return this;
    }
}

var result = user.getPrimitive();
console.log(result)

/*Output

explaination:- here method is attached to object so it will point to its nearest function

{
  id: 332,
  name: 'Prasad',
  city: 'Mumbai',
  age: 23,
  Edu: 'MCA',
  skills: [ 'Js', 'linux', 'Bootstrap', 'css' ],
  getPrimitive: [Function: getPrimitive]
}
*/
```
```js

 const user = {
    "id" : 332,
    "name" : "Prasad",
    "city" : "Mumbai",
    "age" : 23,
    "Edu" : "MCA",
    "skills" : ["Js","linux","Bootstrap","css"],
    "getPrimitive" : function(){ //method
        return function(){ //It is not attached to any method so this will point to global
          return this;
        }
    }
}

var result = user.getPrimitive();
console.log(result) // [Function (anonymous)]
```

* using arrow function

```Js
  const user = {
    "id" : 332,
    "name" : "Prasad",
    "city" : "Mumbai",
    "age" : 23,
    "Edu" : "MCA",
    "skills" : ["Js","linux","Bootstrap","css"],
    "getPrimitive" : function(){ //method
        return function(){ //It is not attached to any method so this will point to global
          return this;
        }
    },
    "getFriend" : function() {
            return () => {
              console.log("ret =>", this.id)
              return this.id;
            }
      }
  }

var result2 = user.getFriend();
console.log(result2) // 332
```


### String methods:-

1. toUpperCase() 
- Convert Sting into upper case.
    ```javascript
    var text = "Prasad";
    console.log(text.toUpperCase());// PRASAD
    ```
2. toLowerCase() 
- Convert String into lower case.
    ```javascript
    var text = "Prasad";
    console.log(text.toLowerCase()); //prasad
    ```
3. replace() 
-  It replace only the first match.
    ```javascript
    var text = "Prasad ts";
    console.log(text.replace("ts","TS")); //Prasad TS
    ```

4. trim() 
- remove whitespace from both the edges of string
    ```javascript
    console.log(text.trim("    Hi there"));
    ```

5.  split() 
- used to split a string into an array of substrings, and returns the new array.

```javascript
console.log(text.split("," ));
```
6. tostring() 

- converting number into string value.
```javascript
console.log(no.tostring(2));
```
 
 ### Built-in methods:-

 1. setTimeout() 
    
    - It has a time API in js
    - It helps in delaying code for specific period of time.
    - It takes parameter as function

    ```javascript
            const timefn = function (){
                console.log("printing after 2 sec") ;
                } 
            console.log("Running 1");
            setTimeout(timefn,32000);
            console.log("Running 2");
    ```

2. setInterval() 
    - It is like setTimeout but it runs continuously it is like timer loop.
    - setInterval keep on looking.

    ```js
        const timefn = function (){
            console.log("printing after 1 sec") ;
            } 
        setTimeout(timefn,1000);
    ``` 
3. clearInterval()

    - we need to be vary sure because setInterval leaks memory
    - it stops the Interval.
    ```javascript
   
    let counter = 0 ;
    const timer = setInterval(function(){
        console.log("printing after 5 sec");
        if (counter > 5 ){
            clearInterval (timer);
        }counter ++;
    },3000);
    console.log("Running 2");
    ```
4. parseInt() 
    - it converts into integer number.
    ```javascript
        Nums ="20.53";
        parseInt(Nums);
        console.log(int Nums);
    ``` 

### JSON

- It helps converting object into JSON and JSON into object
- Object as data used within program, JSON as data use outside of program

- they are two method
    
    1. Stringfy - Convert object in JSON String

        ```javascript
        JSON.Stringify({});
        ``` 
    1. Parse - Convert string in JSON object

        ```javascript
        JSON.parse("{}");
        ``` 

