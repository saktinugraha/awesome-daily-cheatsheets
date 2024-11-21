# Global Objects > Object
[MDN Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)

## Global Object: Properties

| Property             | Description                                                                                                              |
|----------------------|--------------------------------------------------------------------------------------------------------------------------|
| `Object.length`      | Indicates how many arguments a function expects (excluding the rest parameter). Has a value of `1`.                     |
| `Object.prototype`   | Represents the Object prototype object and allows adding new properties and methods to all objects of type `Object`.     |

## Methods of the Object Constructor

| Method                                     | Description                                                                                      |
|-------------------------------------------|--------------------------------------------------------------------------------------------------|
| `Object.assign(target, ...sources)`       | Copies values of all enumerable own properties from one or more source objects to a target object. Returns the target object. |
| `Object.create(proto)`                    | Creates a new object with the specified prototype object and properties.                        |
| `Object.defineProperty(obj, prop, descriptor)` | Adds a named property described by a descriptor to an object.                              |
| `Object.defineProperties(obj, props)`     | Adds named properties described by descriptors to an object.                                    |
| `Object.entries(obj)`                     | Returns an array of `[key, value]` pairs of a given object's own enumerable string properties.   |
| `Object.freeze(obj)`                      | Freezes an object to prevent modification or deletion of its properties.                        |
| `Object.getOwnPropertyDescriptor(obj, prop)` | Returns a property descriptor for a named property on an object.                            |
| `Object.getOwnPropertyDescriptors(obj)`   | Returns all property descriptors for an object.                                                 |
| `Object.getOwnPropertyNames(obj)`         | Returns an array of all enumerable and non-enumerable property names.                           |
| `Object.getOwnPropertySymbols(obj)`       | Returns an array of all symbol properties directly on an object.                                |
| `Object.getPrototypeOf(obj)`              | Returns the prototype of a specified object.                                                    |
| `Object.is(value1, value2)`               | Compares if two values are the same, equating all `NaN` values.                                 |
| `Object.isExtensible(obj)`                | Checks if an object can be extended.                                                            |
| `Object.isFrozen(obj)`                    | Checks if an object is frozen.                                                                  |
| `Object.isSealed(obj)`                    | Checks if an object is sealed.                                                                  |
| `Object.keys(obj)`                        | Returns an array of enumerable string property names.                                           |
| `Object.preventExtensions(obj)`           | Prevents any extensions to an object.                                                           |
| `Object.seal(obj)`                        | Prevents deletion of properties from an object.                                                 |
| `Object.setPrototypeOf(obj, prototype)`   | Sets the prototype of an object.                                                                |
| `Object.values(obj)`                      | Returns an array of values of enumerable string properties.                                      |

## Object Instances and Object Prototype Object
(*`Object.prototype.property`* or *`Object.prototype.method`*)

### Properties

| Name              | Description                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------|
| `obj.constructor` | Specifies the function that creates an object's prototype.                                  |
| `obj.__proto__`   | Points to the object which was used as a prototype when the object was instantiated.         |

### Methods

| Name                              | Description                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------|
| `obj.hasOwnProperty(prop)`        | Returns a boolean indicating whether an object contains the specified property as a direct property of that object (not inherited). |
| `prototypeObj.isPrototypeOf(object)` | Returns a boolean indicating whether the object this method is called upon is in the prototype chain of the specified object. |
| `obj.propertyIsEnumerable(prop)`  | Returns a boolean indicating if the internal ECMAScript `[[Enumerable]]` attribute is set.     |
| `obj.toLocaleString()`            | Calls `toString()`.                                                                            |
| `obj.toString()`                  | Returns a string representation of the object.                                                 |
| `object.valueOf()`                | Returns the primitive value of the specified object.                                           |

# Global Objects > Array
[MDN Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

## Global Object: Properties

| Property         | Description                                                                                   |
|------------------|-----------------------------------------------------------------------------------------------|
| `Array.length`   | Reflects the number of elements in an array.                                                  |
| `Array.prototype`| Represents the prototype of the Array constructor.                                            |

## Global Object: Methods

| Method                                      | Description                                                                                      |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|
| `Array.from(arrayLike[, mapFn[, thisArg]])`| Creates a new array from an array-like or iterable object.                                       |
| `Array.isArray(obj)`                       | Checks if a variable is an array.                                                               |
| `Array.of(...elements)`                    | Creates a new array instance with the specified elements.                                        |

## Instance Properties

| Property      | Description                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------|
| `arr.length`  | Reflects the number of elements in an array.                                                  |

## Instance: Mutator Methods

| Method                              | Description                                                                                       |
|------------------------------------|---------------------------------------------------------------------------------------------------|
| `arr.copyWithin(target, start, end)`| Copies elements within the array.                                                                |
| `arr.fill(value, start, end)`       | Fills elements with a static value.                                                              |
| `arr.pop()`                         | Removes and returns the last element.                                                            |
| `arr.flat()`                        | Flattens nested arrays into a single array.                                                      |
| `arr.push(...elements)`             | Adds elements to the end of the array.                                                           |
| `arr.reverse()`                     | Reverses the array in place.                                                                     |
| `arr.shift()`                       | Removes and returns the first element.                                                           |
| `arr.sort()`                        | Sorts the array in place.                                                                        |
| `arr.splice(start, deleteCount, ...items)` | Adds or removes elements.                                                                      |
| `arr.unshift(...elements)`          | Adds elements to the beginning of the array.                                                     |

## Instance: Accessor Methods

| Method                              | Description                                                                                       |
|------------------------------------|---------------------------------------------------------------------------------------------------|
| `arr.at(index)`                     | Returns the element at the specified index.                                                      |
| `arr.concat(...values)`             | Combines arrays and/or values.                                                                   |
| `arr.includes(searchElement, fromIndex)` | Checks if the array contains a value.                                                        |
| `arr.indexOf(searchElement[, fromIndex])` | Finds the index of a value or returns `-1`.                                                  |
| `arr.join(separator)`               | Joins array elements into a string.                                                             |
| `arr.lastIndexOf(searchElement, fromIndex)` | Finds the last index of a value or returns `-1`.                                             |
| `arr.slice(begin, end)`             | Extracts a section into a new array.                                                            |
| `arr.toString()`                    | Converts the array to a string.                                                                 |
| `arr.toLocaleString(locales, options)` | Converts the array to a localized string.                                                    |

## Instance: Iteration Methods

| Method                              | Description                                                                                       |
|------------------------------------|---------------------------------------------------------------------------------------------------|
| `arr.entries()`                     | Returns an iterator with key/value pairs.                                                        |
| `arr.every(callback[, thisArg])`    | Tests if all elements pass a test.                                                               |
| `arr.filter(callback[, thisArg])`   | Creates a new array with elements that pass a test.                                              |
| `arr.find(callback[, thisArg])`     | Finds the first element that satisfies the test.                                                 |
| `arr.findIndex(callback[, thisArg])`| Finds the index of the first element that satisfies the test.                                     |
| `arr.forEach(callback[, thisArg])`  | Executes a callback for each element.                                                            |
| `arr.keys()`                        | Returns an iterator with array keys.                                                             |
| `arr.map(callback[, thisArg])`      | Creates a new array with the results of a callback.                                              |
| `arr.reduce(callback[, initialValue])` | Reduces array values to a single value.                                                       |
| `arr.reduceRight(callback[, initialValue])` | Reduces array values from right to left.                                                     |
| `arr.some(callback[, thisArg])`     | Tests if at least one element passes a test.                                                     |
| `arr.values()`                      | Returns an iterator with array values.                                                          |