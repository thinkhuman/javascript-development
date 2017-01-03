# Arrays

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

**find()**

Get the value of the first element in an array that meets a test.

```
var ages = [3, 10, 14, 18, 20];
function getFirstAdult(age){
    return age >= 18;
}

ages.find(getFirstAdult);

18
```

**forEach()**

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


**indexOf()**

Returns the index position of a specific value.

```
var ages = [3, 10, 14, 18, 20];
age = ages.indexOf("14");

console.log(a); // displays '2'
```


* join()
* length()
* map()
* pop()
* push()
* reduce()
* reverse()
* shift()
* sort()
* splice()
* toString()
* unshift()
