## What is the difference between Array.forEach and Array.map? When will you use one over the other?

# forEach

- Applies callback function to each array element in the array and doesn't return the new array. It returns undefined.
- Since no array is returned, it cannot be chained with other methods.
- Use forEach when we do not need to use a returned array nor the value returned from the callback function.

# map

- Applies callback function to each array element and it returns the results in a new array.
- Since new array is returned, we can chain methods to it. Eg. .map can be followed by .filter
- Use map only when we require a new array to be returned and perform further operations on it

In depth article: [here](<https://codeburst.io/javascript-map-vs-foreach-f38111822c0f#:~:text=Well%2C%20the%20forEach()%20method,to%20mutate%20the%20calling%20array.&text=The%20difference%20is%20that%20map,Array%20of%20the%20same%20size.>)

## What is the difference between Sets, Maps and Objects ?

# Object:

Implemented like a dictionary, and has much of the same functionality as a hash map, however it has some characteristics that deviate from a traditional hash map implementation. First, only strings can be keys. Second, since in JavaScript’s prototype model, an object has a prototype and therefore has default keys. Third, there is no size property on objects. In objects, key-value pairs are unordered.

# Map:

Implemented as a hash map, with a few significant differences from an Object. It can support any value as a key, including numbers and even other objects. Maps are iterable, whereas Objects are not, and key-value pairs retain the order that they were inserted in during iteration whereas Objects do not retain order. Maps have a size property.

# Set:

A set is a unique list of values, i.e. no duplicates. Sets can be iterated through, but only in order of insertion.

# When to use each:

Objects are often used as a hash map due to the familiar built-in syntax for Objects in JavaScript, however Maps will give better performance when there is significant addition or deletion of key-value pairs. Since JSON can be mapped directly to a JavaScript Object, it is often convenient to work with Objects in contexts where data is being passed around as JSON.

A set can be used in place of a list if you want only unique values. Sets do not have key-value pairs, and are simply a list of elements.
