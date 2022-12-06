
## Maps
Like an object, keys don't update.

```js
const fruit = new Map();

fruit.set(1, 'Banana');
fruit.set(1, 'Apple');

fruit.get(2)

fruit.delete(2);

 fruit.set(4, {
    type: 'Orange',
    color: 'orange',
    flavor: 'orangey'
});



```

## Sets
```js
const fruit = new Set();

fruit.add('Banana');
fruit.add('Apple');

```
Like an array but cannot have duplicvate records