#When to use instanceof vs typeof?

typeof: operator that returns a string representation of the type of the operand; not type comparison

instanceof: operator that does a type comparison, checking whether an object has in its prototype 
chain the prototype property of a constructor

Note that instanceof works on objects in the same window. So calling instanceof on an object will
evaluate it for the window instanceof was called in.

It has been recommended to use 'instanceof' for custom types (assuming constructor exists) and complex native types (i.e.-Array, RegExp) and typeof for simple native types.

There are some quirks, however. For example, because a string can be both a literal and an object depending on how it's constructed, the below code is useful to check against both.
```javascript
function isString(str) {
    return typeof(str) === 'string' || str instanceof String;
}
```
Another tricky example is below:
```javascript
typeof null // object
```

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/typeof
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/instanceof
http://stackoverflow.com/a/6625960
