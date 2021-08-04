## Javascript Variable

* Js is dynamic type. It means type is declared at its run time.
* Variable is a container.They are use to store data
* They can hold either primitive or non-primitive value


### Variable Declaration

- Variable in javascript can be declared using keyword as mentioned below:-
   1. <b>var</b> - can be redeclared, can be reinitialized and has functional scope. Can also get hoisted. It is es5 feature.

   ```
      var a = "Prasad";
      var a = "Prasad Tandel";

      console.log(a); //output:- Prasad Tandel
   ```
   2. <b>let</b> - let cannot be redeclared but can be reinitialized. It has lexical scope and it's es6 feature. It does not get hoisted.

   ````
      var b = 12;
      b = 4;
      console.log(b); //output:- 4
   ````  
   3. const - It cannot be redeclared neither reinitialize but non-primitive value can get updated. It has lexical scope and it's es6 feature. It does not get hoisted.

   ```
      const pi = 3.14;
      console.log(pi); // 3.14
   ```


* Primitive Data Type - which cannot be changed

    * string
    * number
    * boolean
    * undefined
    * null
    * symbol(es6)

* Non-Primitive Data Type - Which can be changed

    * Object
    * Array

