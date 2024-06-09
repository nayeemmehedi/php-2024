NULL in PHP
NULL is a special constant in PHP that represents a variable with no value. A variable is considered to be NULL if it has been assigned the constant NULL, it has not been set to any value yet, or it has been unset using the unset() function.
```php
$var = NULL;
echo $var; // Output: (nothing)

$var;
var_dump($var); // Output: NULL

$var = 'Hello';
unset($var);
var_dump($var); // Output: NULL
```

Checking for NULL
To check if a variable is NULL, you can use the is_null() function or the identity operator (===):

```php
$var = NULL;

if (is_null($var)) {
    echo 'Variable is NULL';
}

if ($var === NULL) {
    echo 'Variable is NULL';
}
```

undefined in PHP
PHP does not have an equivalent to JavaScript's undefined. However, in PHP, if you try to use a variable that has not been set, you will get a notice that the variable is undefined. You can use the isset() function to check if a variable has been set and is not NULL.


Checking if a variable is set:

```php

if (isset($undefinedVar)) {
    echo 'Variable is set';
} else {
    echo 'Variable is not set';
}

$var = NULL;
if (isset($var)) {
    echo 'Variable is set';
} else {
    echo 'Variable is not set';
}
```

var_dump is  type and value

```php

$a = 123;
var_dump($a);

output:
int(123)

```

