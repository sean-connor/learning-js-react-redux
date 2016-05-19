# Special Considerations of Javascript

## OO in Javascript
* [MDN Object-Oriented Programming in Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Introduction_to_Object-Oriented_JavaScript)

* Takeaways:
  * Namespacing
  * Classes in JS(going to change in ES6)
  * Object
  * Relationship between Object and:
    * Property
    * Method
    * Constructor
  * Inheritance
  * Encapsulation
  * Abstraction

## Scoping
  * Variable Scope (Try taking the examples below, think about what the output will be then use JSFiddle or similar to evaluate them)
    * Global Scope  
      ```javascript

      // All ES5 Syntax
      var x = 'global';
      function global() {
        alert(x);
      }
      global();
      //
      ```
    * Local Scope  
      ```javascript

      // All ES5 Syntax
      var x = 'global';

      function local1(x) {
        alert(x);
      }
      local1('local1');

      function local2() {
        var x = 'local2';
        alert(x);
      }
      local2();
      //
      ```  
    * Lack of block scope in ES5, ES6 fixes this by using 'let' instead of 'var'
      ```javascript

      // All ES5 Syntax
      var x = 'global';

      function blockscope() {
        if (true){
          var x = 'block';
        }
        alert(x);
      }

      blockscope();
      //
      ```  
    * Object Properties - "this"
      ```javascript

      // All ES5 Syntax
      var x = 'global';

      function thisScope() {
        this.x = 'this';
        alert(this.x);
      }
      thisScope();
      //
      ```  
    * Closures
      ```javascript

      // All ES5 Syntax
      var x = 'global';

      function closure = (function() {
        var x = 'closedOver';
        return function() {
          alert(x);
        }
      })();
      //The structure of function closure is called an Immediately-invoked function, covered more below. Note the return value of the IIFE is an anonymous function and that the variable x still holds onto it's scope and has access to the 'x' variable where the function was defined, this is a closure.
      closure();
      //
      ```       
    * Variable Hoisting - Javascript hoists the variable declarations to the top of their respective functions:

      ```javascript

      // All ES5 Syntax
      var x = 'global'

      var local = function(){
        console.log(x);
        var x = 'local';
        console.log(x);
      }

      //While it may seem like this would
      //console log 'global' and then 'local'
      //you find it logs 'undefined' and
      //'local', what Javascript is really
      //doing...
      var x = 'global'

      var local = function(){
        var x; //The variable declaration is hoisted, set to undefined
        console.log(x);
        x = 'local'; // The variable assignment remains
        console.log(x);
      }

      //
      ```
  * IIFEs(Immediately-invoked function expressions)
  * Function Scope
  * Binding


## Callbacks
  * Basic
  * Events
  * Promises

## The Event Loop
  * [Event Loop with Loupe](http://bit.ly/1Btu0Iy)
  * [MDN Concurrency and the Event Loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop)
