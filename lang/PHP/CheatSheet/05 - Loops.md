# Loops & Iteration 

## For Loop
Syntax
```php
  for (initialize; condition; increment) {
  // code to be executed
  }
```

Example
```php 
for ($x = 0; $x <= 10; $x++) {
	echo "Number: $x <br>";
}
```

## While Loop 
Syntax
```php
while (condition) {
	// code to be executed
}
```

Example
```php
$x = 1;

while ($x <= 5) {
  echo "Number: $x <br>";
  $x++;
}
```


## Do While Loop
Syntax
```php
do {
	// code to be executed
} while (condition);

do...while loop will always execute the block of code once, even if the condition is false.
```

Example
```php
do {
	echo "Number: $x <br>";
	$x++;
} while ($x <= 5);
```

## Foreach Loop
Syntax
```php
foreach ($array as $value) {
	// code to be executed
}
```

Example
```php
$posts = ['Post One', 'Post Two', 'Post Three'];

foreach ($posts as $index => $post) {
  echo "${index} - ${post} <br>";
}

// Use the keys within the loop for an associative array

$person = [
  'first_name' => 'Brad',
  'last_name' => 'Traversy',
  'email' => 'brad@gmail.com',
];

// Get Keys
foreach ($person as $key => $val) {
  echo "${key} - ${val} <br>";
}
```

### Loop through an array
```php 
$numbers = [1, 2, 3, 4, 5];

foreach ($numbers as $x) {
  echo "Number: $x <br>";
} 
```
 
### Use the indexes within the loop
 ```php
$posts = ['Post One', 'Post Two', 'Post Three'];

foreach ($posts as $index => $post) {
	echo "${index} - ${post} <br>";
}
```

### Use the keys within the loop for an associative array
```php
$person = [
	'first_name' => 'Brad',
	'last_name' => 'Traversy',
	'email' => 'brad@gmail.com',
];

// Get Keys
foreach ($person as $key => $val) {
	echo "${key} - ${val} <br>";
}
```
