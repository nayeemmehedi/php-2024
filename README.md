# PHP Object-Oriented Programming (OOP) Guide

This guide provides an overview of object-oriented programming (OOP) concepts in PHP, including classes, objects, properties, methods, inheritance, interfaces, abstract classes, traits, and more.

## Table of Contents

- [Classes and Objects](#classes-and-objects)
- [Properties and Methods](#properties-and-methods)
- [Visibility](#visibility)
  - [Public](#public)
  - [Private](#private)
  - [Protected](#protected)
- [Inheritance](#inheritance)
- [Interfaces](#interfaces)
- [Abstract Classes](#abstract-classes)
- [Traits](#traits)
- [Static Methods and Properties](#static-methods-and-properties)
- [Constructor and Destructor](#constructor-and-destructor)
- [Summary](#summary)

## Classes and Objects

### Defining a Class

```php
class Person {
    // Properties
    public $name;
    public $age;

    // Constructor
    public function __construct($name, $age) {
        $this->name = $name;
        $this->age = $age;
    }

    // Method
    public function introduce() {
        return "Hello, my name is $this->name and I am $this->age years old.";
    }
}

```


### Creating an Object

```php
$person = new Person("John", 30);
echo $person->introduce(); // Output: Hello, my name is John and I am 30 years old.
```

### Properties and Methods

```php

class Car {
    public $color;
    public $model;
}

```

Methods

```php
class Car {
    public $color;
    public $model;

    public function display() {
        return "This car is a $this->color $this->model.";
    }
}

$car = new Car();
$car->color = "red";
$car->model = "Toyota";
echo $car->display(); // Output: This car is a red Toyota.


```


### Visibility:

***Public***

```php

class Person {
    public $name;

    public function sayHello() {
        return "Hello, $this->name!";
    }
}

$person = new Person();
$person->name = "Alice";
echo $person->sayHello(); // Output: Hello, Alice!


```

***Private***

```php

class Person {
    private $name;

    public function setName($name) {
        $this->name = $name;
    }

    public function getName() {
        return $this->name;
    }
}

$person = new Person();
$person->setName("Alice");
echo $person->getName(); // Output: Alice


```

***Protected***

```php

class Person {
    protected $name;

    protected function setName($name) {
        $this->name = $name;
    }
}

class Employee extends Person {
    public function assignName($name) {
        $this->setName($name);
    }

    public function getName() {
        return $this->name;
    }
}

$employee = new Employee();
$employee->assignName("Alice");
echo $employee->getName(); // Output: Alice

```

### Inheritance

```php

class Animal {
    public $name;

    public function makeSound() {
        return "$this->name makes a sound.";
    }
}

class Dog extends Animal {
    public function makeSound() {
        return "$this->name barks.";
    }
}

$dog = new Dog();
$dog->name = "Rover";
echo $dog->makeSound(); // Output: Rover barks.



```


### Interfaces

```php

interface Speakable {
    public function speak();
}

class Human implements Speakable {
    public function speak() {
        return "Hello!";
    }
}

$human = new Human();
echo $human->speak(); // Output: Hello!


```

### Abstract Classes

```php
abstract class Animal {
    abstract public function makeSound();

    public function sleep() {
        return "Sleeping...";
    }
}

class Cat extends Animal {
    public function makeSound() {
        return "Meow";
    }
}

$cat = new Cat();
echo $cat->makeSound(); // Output: Meow
echo $cat->sleep(); // Output: Sleeping...
```


### Traits


```php


trait Logger {
    public function log($message) {
        echo "Log: $message";
    }
}

class User {
    use Logger;
}

$user = new User();
$user->log("User created"); // Output: Log: User created

```

### Static Methods and Properties

```php

class MathHelper {
    public static $pi = 3.14;

    public static function square($number) {
        return $number * $number;
    }
}

echo MathHelper::$pi; // Output: 3.14
echo MathHelper::square(5); // Output: 25


```

### Constructor and Destructor

```php

class Person {
    public $name;

    public function __construct($name) {
        $this->name = $name;
    }

    public function getName() {
        return $this->name;
    }
}

$person = new Person("Alice");
echo $person->getName(); // Output: Alice


```

Destructor


```php

class Person {
    public $name;

    public function __construct($name) {
        $this->name = $name;
    }

    public function __destruct() {
        echo "Object {$this->name} is being destroyed";
    }
}

$person = new Person("Alice");
// At the end of the script, or when the object is no longer referenced, the destructor is called:
// Output: Object Alice is being destroyed


```


