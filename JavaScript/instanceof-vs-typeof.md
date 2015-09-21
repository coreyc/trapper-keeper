When to use instanceof vs typeof?

typeof: operator that returns a string representation of the type of the operand; not type comparison

instanceof: operator that does a type comparison, checking whether an object has in its prototype 
chain the prototype property of a constructor

Note that instanceof works on objects in the same window. So calling instanceof on an object will
evaluate it for the window instanceof was called in.






https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/typeof
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/instanceof
