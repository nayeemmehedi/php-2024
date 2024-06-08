## PHP Basic Syntax:

- **Opening and Closing Tags:** PHP code is enclosed within `<?php` and `?>` tags.
  ```php
  <?php
  // PHP code goes here
  ?>

- **Statements and Comments:** PHP statements end with a semicolon (;). Comments can be single-line (//) or multi-line (/* */).

 ```php
// Single-line comment
/*
  Multi-line
  comment
*/
$variable = 10; // PHP statement
```

- **Echo and Print:** Outputting content to the browser is often done with `echo or print`.
```php
echo "Hello, world!";
print "Welcome to PHP!";
```

## Variables in PHP:

- Variable Naming: Variable names start with the dollar sign ($) followed by the name.
```php
$name = "John";
```

- Variable Types: PHP variables are loosely typed, meaning you don't need to declare a variable's data type explicitly.

```php
$count = 5;         // Integer
$price = 10.99;     // Float
$name = "John";     // String
$is_active = true;  // Boolean
```
- Variable Scope: PHP variables can have local or global scope. Local variables are defined within functions, while global variables are defined outside functions and are accessible throughout the script.
```php

 $global_variable = "I am global";

function exampleFunction() {
    $local_variable = "I am local";
    echo $local_variable;   // Output: I am local
    echo $global_variable;  // Output: I am global
}
```




