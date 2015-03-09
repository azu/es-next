ECMAScript 7 is the next evolution of the ECMA-262 standard, this is at a very early stage, you may want to checkout [paws-on-es6](https://github.com/hemanth/paws-on-es6) as well.

# Exponentiation Operator
> Performs exponential calculation on operands. Same algorithm as `Math.pow(x, y)`

```js

let cubed = x => x ** 3;

cubed(2) // 8;
```

# Array comprehensions
> Declarative form for creating computed arrays with a literal syntax that reads naturally.

```js

let numbers = [ 1, 4, 9 ];

[for (num of numbers) Math.sqrt(num)];
// => [ 1, 2, 3 ]

[for (x of [ 1, 2, 3]) for (y of [ 3, 2, 1 ]) x*y];
// => [ 3, 2, 1, 6, 4, 2, 9, 6, 3 ]

[for (x of [ 1, 2, 3, 4, 5, 6 ]) if (x%2 === 0) x];
// => [ 2, 4, 6 ]
```

# Generator comprehensions
> Create a generator function based on an existing iterable object.

```js
(for (i of [ 2, 4, 6 ]) i*i );
// generator function which yields 4, 16, and 36
```



# Async functions
> Deferred Functions

```js
function wait(t){
  return new Promise((r) => setTimeout(r, t));
}
 
async function asyncMania(){
  console.log("1");
  await wait(1000);
  console.log("2");
}
 
asyncMania()
.then(() => alert("3"));

// logs: 1 2 3
```

# Async generators
> Deferred generators.

```js
// provider
async function* nums() {
  yield 1;
  yield 2;
  yield 3;
}

// consumer
async function printData() {
  for(var x on nums()) {
    console.log(x);
  }
}
```

# Object Observe 
> Asynchronously observing the changes to an object.

```js

var obj = {};

Object.observe( obj,function(changes) {console.log(changes);} );

obj.name = "hemanth";

// Would log -> [ { type: 'new', object: { name: 'hemanth' }, name: 'name' } ]
```

# Object.getOwnPropertyDescriptors
> Returns a property descriptor for an own property.

```js

let life = { answer: 42 };
Object.getOwnPropertyDescriptor(life, 'answer');
//^ { configurable: true, enumerable: true, value: 42, writable: true }
```

# Array.prototype.includes
> Determines whether an array includes a certain element or not.

```js
[1, 2, 3].includes(3, 0, 7); // true
[1, 2, NaN].includes(NaN); // true
[0,+1,-1].includes(42); // false
```

# Typed Objects
> TDB

# Reflect.Realm
> TDB











