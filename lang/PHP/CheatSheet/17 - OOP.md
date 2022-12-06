# Object Oriented Programming 
From PHP5 onwards you can write PHP in either a procedural or object oriented way. OOP consists of classes that can hold "properties" and "methods". Objects can be created from classes.

```php
class User {
  // Properties are just variables that belong to a class.
  // Access Modifiers: public, private, protected
  // public - can be accessed from anywhere
  // private - can only be accessed from inside the class
  // protected - can only be accessed from inside the class and by inheriting classes
  private $name;
  public $email;
  public $password;

  // The constructor is called whenever an object is created from the class.
  // We pass in properties to the constructor from the outside.
  public function __construct($name, $email, $password) {
    // We assign the properties passed in from the outside to the properties we created inside the class.
    $this->name = $name;
    $this->email = $email;
    $this->password = $password;
  }


  function getName() {
    return $this->name;
  }

  function login() {
    return "User $this->name is logged in.";
  }

  function __destruct() {
    echo "The user name is {$this->name}.";
  }
}

// Instantiate a new user
$user1 = new User('Brad', 'brad@gmail.com', '123456');
echo $user1->getName();
echo $user1->login();

// Add a value to a property
// $user1->name = 'Brad';

var_dump($user1);
// echo $user1->name;

```

## Constructor 
The constructor is called whenever an object is created from the class.

```php
public function __construct($foo, $bar) {
	$this->foo = $foo;
	$this->bar = $bar;
}
```

## Methods
Methods are functions that belong to a class.

```php
function setName() {
  $this->name = $name;
}
```

## Destructor
Destructor is called when an object is destroyed or the end of the script.

```php
  function __destruct() {
    echo "The foo is {$this->bar}.";
  }
```
## Inheritence
Inheritence is the ability to create a new class from an existing class. It is achieved by creating a new class that extends an existing class.

```php
public function __construct($foo, $bar) {
    parent::__construct($foo, $bar);
  }
```

```php
class employee extends User {
  public function __construct($name, $email, $password, $title) {
    parent::__construct($name, $email, $password);
    $this->title = $title;
  }

  public function getTitle() {
    return $this->title;
  }
}

$employee1 = new employee('John','johndoe@gmail.com','123456','Manager');
echo $employee1->getTitle();
```


## Interface 
Interface does'n contains Constructors 
```php
interface A
{
    public function foo();
}

interface B extends A
{
    public function baz(Baz $baz);
}

// This will work
class C implements B
{
    public function foo()
    {
    }

    public function baz(Baz $baz)
    {
    }
}

// This will not work and result in a fatal error
class D implements B
{
    public function foo()
    {
    }

    public function baz(Foo $foo)
    {
    }
}
```



## Abstraction
"Base class" thats to be instinciated in Inheritence, Abstract class contains Constructors
https://www.php.net/manual/en/language.oop5.abstract.php

```php
<?php
abstract class AbstractClass
{
    // Force Extending class to define this method
    abstract protected function getValue();
    abstract protected function prefixValue($prefix);

    // Common method
    public function printOut() {
        print $this->getValue() . "\n";
    }
}

class ConcreteClass1 extends AbstractClass
{
    protected function getValue() {
        return "ConcreteClass1";
    }

    public function prefixValue($prefix) {
        return "{$prefix}ConcreteClass1";
    }
}

class ConcreteClass2 extends AbstractClass
{
    public function getValue() {
        return "ConcreteClass2";
    }

    public function prefixValue($prefix) {
        return "{$prefix}ConcreteClass2";
    }
}

$class1 = new ConcreteClass1;
$class1->printOut();
echo $class1->prefixValue('FOO_') ."\n";

$class2 = new ConcreteClass2;
$class2->printOut();
echo $class2->prefixValue('FOO_') ."\n";
?>
```

## Interface vs Abstract Class
https://codenphp.blogspot.com/search?q=abstract%20class%20vs%20interface%20


Interface support multiple inheritance | Abstract class does not support multiple inheritance
Interface does'n Contains Data Member | Abstract class contains Data Member

Interface does'n contains Constructors | Abstract class contains Constructors
An interface Contains only incomplete member (signature of member) | An abstract class Contains both incomplete (abstract) and complete member
An interface cannot have access modifiers by default everything is assumed as public | An abstract class can contain access modifiers for the subs, functions, properties

Members of interface can not be Static | Only Complete Member of abstract class can be Static



## Object Composition


## Value Objects


## Static Methods
Declaring class properties or methods as static makes them accessible without needing an instantiation of the class. These can also be accessed statically within an instantiated class object.


https://www.php.net/manual/en/language.oop5.static.php


```php
class Foo {
    public static function aStaticMethod() {
        // ...
    }
}

Foo::aStaticMethod();
$classname = 'Foo';
$classname::aStaticMethod();
```

