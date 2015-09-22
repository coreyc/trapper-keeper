#Quickly get the values from a set of object's keys using functional programming

The following takes an object and for each key, returns the value. Object.keys() returns an array
of the object's keys, in numeric order.

The functional style of solving this problem is more expressive and readable than using a for loop,
and is, thus, a nice tool to have in your toolbelt.
```javascript
var inputObject = { 0: 'a', 1: 'b', 2: 'c' };
var values = [];
Object.keys(inputObject).forEach(function(key) {
  values.push(inputObject[key]);
  return values;
});
console.log(values);
```

Note that forEach() (an Array method) and Object.keys() (an Object method, obviously) are not 
supported by IE8 and below.

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/keys
