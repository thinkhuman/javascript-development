# Inheritance

Python, Java, etc. use *classical* (class-based) inheritance: you create a class (the "prototype"), then create and use _instances_ of the class. The class is a house blueprint, the instances are the actual houses built from the blueprint.

However, JavaScript uses *prototypal* inheritance: create a prototype function (a constructor), then create and use objects based on the prototype. The prototype is a house, the objects are other houses built based on the prototype. JavaScript has two basic flavors of this: prototypal and "pseudo-classical" inheritance.

**Pseudo-classical (constructor pattern)**: Make a function w/properties & methods, which looks much like a class. Then:

`var myobj = new myConstructorFunction();` creates an object that inherits from `myConstructorFunction`.

**Prototypal pattern**: 

`var myobj = Object.create(myConstructorFunction);` 

So, just use the special syntax `var newobject = Object.create(parentObject)`. That sets up the prototype chain.


## More Reading:

[Creating objects](http://www.htmlgoodies.com/beyond/javascript/object.create-the-new-way-to-create-objects-in-javascript.html)
