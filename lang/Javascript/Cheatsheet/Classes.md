# Class

## Pre ES6
```javascript
function Animals(name, specie) {
    this.name = name;
    this.specie = specie;
}

Animals.prototype.sing = function () {
    return `${this.name} can sing`;
}

Animals.prototype.dance = function () {
    return `${this.name} can dance`;
}


```

### Subclassing

```js
sadasdasd
```


## ES6 Class
```javascript

class Animals {
    constructor(name, specie) {
        this.name = name;
        this.specie = specie;
    }
    sing() {
        return `${this.name} can sing`;
    }
    dance() {
        return `${this.name} can dance`;
    }
}
let bingo = new Animals("Bingo", "Hairy");
console.log(bingo);

```

### Subclassing
```javascript
class Cats extends Animals {
    constructor(name, age, whiskerColor) {
        super(name, age);
        this.whiskerColor = whiskerColor;
    }
    whiskers() {
        return `I have ${this.whiskerColor} whiskers`;
    }
}
let clara = new Cats("Clara", 33, "indigo");

```


### Links
- [Object Oriented Programming in JavaScript – Explained with Examples](https://www.freecodecamp.org/news/how-javascript-implements-oop/)
- [The Hard Parts of Object Oriented JavaScript](https://frontendmasters.com/courses/object-oriented-js/)
- [Object-oriented JavaScript for beginners](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Classes_in_JavaScript)
- [Introduction to Object Oriented Programming in JavaScript](https://www.geeksforgeeks.org/introduction-object-oriented-programming-javascript/)