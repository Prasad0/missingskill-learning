### This

* In JavaScript, this keyword refers to the object where it is called.

1. this Inside Global Scope

When this is used alone, this refers to the global object (window object in browsers). For example,

```js
    let a = this;
    console.log(a);  // Window {}

    this.name = 'Sarah';
    console.log(window.name); // Sarah
```
* Here, this.name is the same as window.name.

2. This inside Function

* When this is used in a function, this refers to the global object (window object in browsers). For example,

```Js
function greet() {

    // this inside function
    // this refers to the global object
    console.log(this);
}

greet(); // Window {}
```
3. This inside Constructor Function

* In JavaScript, constructor functions are used to create objects. When a function is used as a constructor function, this refers to the object inside which it is used. For example,

```Js
function Person() {

    this.name = 'Jack';
    console.log(this);

}

let person1 = new Person();
console.log(person1.name);

//Output

/**
 * Person {name: "Jack"}
    Jack
*/
```


https://www.programiz.com/javascript/this

