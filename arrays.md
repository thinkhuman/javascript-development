# Arrays and Common Array Methods

An array is a _data structure_ (really just a special variable) used to store multiple values (of any type). It looks like this:

```
var things = [ "Dog", "Cat", "Salamander", 42, {"Joe", "Ralph"}, 945.55, true ];
```

In JavaScript, an array is an _object_. Arrays in JavaScript are ordered, meaning the positions of values in an array value do not change (unless you change them).


## Common Array Methods

###concat()

Join two arrays.

```
var room1 = ["Bob", "Joanne"];
var room2 = ["Ralph", "Mary", "Linus"];
var newRoom = room1.concat(room2);

Bob, Joanne, Ralph, Mary, Linus
```

### find()

Get the value of the first element in an array that meets a test.

```
var ages = [3, 10, 14, 18, 20];
function getFirstAdult(age){
    return age >= 18;
}

ages.find(getFirstAdult);

18
```

### forEach()

Call a provided function once for each element in an array, in order.

```
var ages = [3, 10, 14, 18, 20];
ages.forEach(function(age){
    console.log(age)
    });
```
ES6 adds a `for...of` iterator, like this:

```
for (val of ages) {
    console.log(val);
}
```


### indexOf()

Return the index position of a specific value.

```
var ages = [3, 10, 14, 18, 20];
age = ages.indexOf("14");
console.log(a); // displays '2'
```


### join()
Join the elements of an array into a string.

```
var room2 = ["Ralph", "Mary", "Linus", "Eileen"];
var team = room2.join();
console.log(team);
"Ralph, Mary, Linus, Eileen"
```

### length()
Return the length of an array.

```
var ages = [3, 10, 14, 18, 20];
console.log(ages.length);
4
```

### map()
Apply a defined function to each element in an array, and return a new array with the results.

```
var ages = [3, 10, 14, 18, 20];
x = ages.map(Math.sqrt);
console.log(x);
[1.73, 3.16, 3.74, 4.24, 4.27] // Rounded for example
```

### pop()
Remove and return the last element of an array. To remove the _first_ item, use `shift()`.

```
var ages = [3, 10, 14, 18, 20];
ages.pop();
20
```

### push()
Add new items to the end of an array and return the new array. To add items to the _beginning_ of an array, use `unshift()`.

```
var ages = [3, 10, 14, 18, 20];
ages.push(55);
[3, 10, 14, 18, 20, 55];
```

### reduce()
Reduce values in an array to a single value.

```
var ages = [3, 10, 14, 18, 20];
function getSum(total, num) {
    return total + num;
}
ages.reduce(getSum);
```

### reverse()
Reverse the order of elements in an array.

```
var ages = [3, 10, 14, 18, 20];
ages.reverse();
[20,18,14,10,3]
```

### shift()
Remove and return the first element in an array. To remove the _last_ element of an array, use `pop()`.

```
var ages = [3, 10, 14, 18, 20];
ages.shift();
3
```

### sort()
Sort array elements in ascending (default) or descending order.

```
var ages = [20, 10, 14, 5, 2];
ages.sort();
[2,5,10,14,20]
```
To sort in descending order, pass in a function:

```
var ages = [20, 10, 14, 5, 2];
ages.sort(function(a, b){
    return a-b;
    });
```

### splice()
Remove elements from (and return) or add elements to an array.

```
// Add items
var ages = [20, 10, 14, 5, 2];
ages.splice(2, 0, 142); //position, # of items to remove, value to insert
[20, 10, 142, 14, 5, 2]

// Remove items
var ages = [20, 10, 14, 5, 2];
ages.splice(2,1) //position, # of items to remove
[14]
```

### toString()
Convert an entire array to a string.

```
var ages = [20, 10, 14, 5, 2];
ages.toString();
"20,10,14,5,2"
```

### unshift()
Add new elements to beginning of an array and returns new array length.

```
var ages = [20, 10, 14, 5, 2];
ages.unShift(99,33,22);
8
console.log(ages);
[99, 33, 22, 20, 10, 14, 5, 2]
```



