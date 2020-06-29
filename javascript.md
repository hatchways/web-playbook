## What is the difference between Array.forEach and Array.map? When will you use one over the other?

# forEach
- Applies callback function to each array element in the array and doesn't return the new array. It returns undefined.
- Since no array is returned, it cannot be chained with other methods. 
- Use forEach when we do not need to use a returned array nor the value returned from the callback function.

# map
- Applies callback function to each array element and it returns the results in a new array.
- Since new array is returned, we can chain methods to it. Eg. .map can be followed by .filter
- Use map only when we require a new array to be returned and perform further operations on it

In depth article: [here](https://codeburst.io/javascript-map-vs-foreach-f38111822c0f#:~:text=Well%2C%20the%20forEach()%20method,to%20mutate%20the%20calling%20array.&text=The%20difference%20is%20that%20map,Array%20of%20the%20same%20size.)

