# Arrow Opperator

## Double Arrow Operator
It is an assignment operator used in the creation of associative arrays.

It is placed in between the array key and its value. It assigns to the key (what is on its left enclosed quotes), the value of what is on its right side.

Syntax
```php
"key" => value
```

Example
```php
$person = array(
    "firstName" => "John",
    "lastName" => "Doe",
    "age" => 28,
    "gender" => "Male",
    "email" => "johndoe@gmail.com",
    "city" => "Germany"
);
```


## Object Operator
It is an access operator used for access/call methods and properties in a PHP object in Object-Oriented Programming (OOP).

```php
<?php
class People {

   public $name = 'John Doe';

   public function Developer() {

   }

}
$person = new People();
$person->Developer();
echo $person->name;
?>
```