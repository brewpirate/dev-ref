# Arrays
 If you need to store multiple values, you can use arrays. Arrays hold "elements"

## Simple array of numbers
```php
$numbers = [1, 2, 3, 4, 5];
```

## Simple array of strings
```php
$colors = ['red', 'blue', 'green'];
```

## Using the array function to create an array of numbers
```php
$numbers = [1, 2, 3, 4, 5];
```

## Outputting values from an array
```php
echo $numbers[0];
echo $numbers[3] + $numbers[4];
```

#  Associative Arrays
 Associative arrays allow us to use named keys to identify values.
 ```php
$colors = [
  1 => 'red',
  2 => 'green',
  3 => 'blue',
];

echo $colors[1];

// Strings as keys
$hex = [
  'red' => '#f00',
  'green' => '#0f0',
  'blue' => '#00f',
];

echo $hex['red'];
var_dump($hex);
```

# Multi-dimensional arrays
Multi-dimansional arrays are often used to store data in a table format.

```php
// Single person
$person1 = [
  'first_name' => 'Brad',
  'last_name' => 'Traversy',
  'email' => 'brad@gmail.com',
];

// Array of people
$people = [
  $person1, //   [...$person1]
  [
    'first_name' => 'John',
    'last_name' => 'Doe',
    'email' => 'john@gmail.com',
  ],
  [
    'first_name' => 'Jane',
    'last_name' => 'Doe',
    'email' => 'jane@gmail.com',
  ],
];

var_dump($people);

```

## Accessing values in a multi-dimensional array

```php
echo $people[0]['first_name'];
echo $people[2]['email'];
```

## Encode to JSON

```php
json_encode($people)
var_dump(json_encode($people)); 
```

## Decode from JSON

```php
$jsonobj = '{"first_name":"Brad","last_name": "Traversy","email":"brad@gmail.com"}';
var_dump(json_decode($jsonobj));
```