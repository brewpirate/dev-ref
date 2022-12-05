#  Array Functions
Functions to work with arrays 
https://www.php.net/manual/en/ref.array.php

```php
$fruits = ['apple', 'banana', 'orange'];
```

## Get array length
```php
echo count($fruits);
```

## Search array
```php
echo in_array('banana', $fruits);
```

## Add to an array

```php
$fruits[] = 'grape';
array_push($fruits, 'mango', 'raspberry');
array_unshift($fruits, 'kiwi'); // Adds to the beginning
```

## Remove from array

```php
array_pop($fruits); // Removes last
array_shift($fruits); // Removes first
```

## Remove specific element

```php
unset($fruits[2]);
```

## Split into chunks of 2

```php
$chunkedArray = array_chunk($fruits, 2);
var_dump($chunkedArray);
```

## Concatenate arrays
```php
$arr1 = [1, 2, 3];
$arr2 = [4, 5, 6];
$arr3 = array_merge($arr1, $arr2);
var_dump($arr3);

```

## Spread Operator ...

```php
$arr4 = [...$arr1, ...$arr2]; // Use Spread
var_dump($arr4);
```


```php
// Combine arrays (Keys & values)
$a = ['green', 'red', 'yellow'];
$b = ['avocado', 'apple', 'banana'];
$c = array_combine($a, $b);

// Array of keys
$keys = array_keys($c);

// Flip keys with values
$flipped = array_flip($c);
var_dump($flipped);

// 




```

## Create array of numbers with range()
```php
$numbers = range(1, 20);
```

## Map
Map through array and create a new one
```php
$newNumbers = array_map(function ($number) {
  return "Number ${number}";
}, $numbers);
```

## Filter array
```php
$lessThan10 = array_filter($numbers, fn($number) => $number < 10);
```

## Array Reduce
"carry" holds the return value of the previous iteration
```php
$sum = array_reduce($numbers, fn($carry, $number) => $carry + $number);
var_dump($sum);
```