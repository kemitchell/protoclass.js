protoclass is a thin class library that helps create, and extend prototypes.

## Example


```javascript

var protoclass = require("protoclass");


function Animal(name) {
  this.name = name;
}

protoclass(Animal);

function Cat(name) {
  Cat.superclass.apply(this, arguments);
}

Animal.extend(Cat, {
  meow: function() {
    console.log(this.name + ": meow");
  }
});


console.log(Class.prototype.constructor == Class); // true
console.log(Class.superclass == Animal); // true
consoele.log(Class.name); // Cat
```

## API

### fn protoclass([superclass,] subclass[, mixins])

### fn.superclass

### fn.__super__

super prototype

### fn.extend(subclass[, mixins])

### fn.mixin(mixins)

copies the the mixins over to the prototype