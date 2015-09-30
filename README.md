# prop-type

Small wrapper to wrap your custom type check so that you can use `myCustomType.isRequired` in a similar fasion to React's built-in types.

### Install

    npm install prop-type

### Usage:
     
     var type = propType(function isFoo(props, name){  
         if(props[name] !== "foo")
             return new TypeError("not a foo");
     });

     // optional by default:
     assert.ok( ! type(null) );

     // required like so:
     assert.ok( type.isRequired(null) );
