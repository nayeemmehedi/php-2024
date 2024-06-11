# PHP Superglobals : $GLOBALS['x'] 

PHP superglobals are built-in variables that are always accessible, regardless of scope. They are used to access data coming from forms, sessions, cookies, and other sources.

## List of Superglobals

1. **$_GLOBALS**
2. **$_SERVER**
3. **$_GET**
4. **$_POST**
5. **$_FILES**
6. **$_COOKIE**
7. **$_SESSION**
8. **$_REQUEST**
9. **$_ENV**

### 1. `$_GLOBALS`

Contains references to all variables currently defined in the global scope.

```php
<?php
$x = 75;
$y = 25;

function addition() {
    $GLOBALS['z'] = $GLOBALS['x'] + $GLOBALS['y'];
}

addition();
echo $z; // Outputs: 100
?>
```
