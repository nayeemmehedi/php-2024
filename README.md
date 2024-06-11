1. If, Elseif, and Else
 ```php

if (condition) {
    // Code to execute if condition is true
} elseif (another_condition) {
    // Code to execute if another_condition is true
} else {
    // Code to execute if none of the above conditions are true
}

```

2. Switch

```php

   switch (expression) {
    case value1:
        // Code to execute if expression equals value1
        break;
    case value2:
        // Code to execute if expression equals value2
        break;
    default:
        // Code to execute if expression does not match any value
}

 ```

3. While

```php

while (condition) {
    // Code to execute as long as condition is true
}



```

4. For

```php

for (initialization; condition; increment) {
    // Code to execute as long as condition is true
}


 ```

5. Foreach

   The `foreach` loop is used to iterate over arrays or objects

```php

foreach ($array as $value) {
    // Code to execute for each value in the array
}

foreach ($array as $key => $value) {
    // Code to execute for each key-value pair in the array
}

```

6. Break


```php

   while (condition) {
    if (another_condition) {
        break; // Exit the loop
    }
    // Other code
}


```

7.Continue

```php

for ($i = 0; $i < 10; $i++) {
    if ($i % 2 == 0) {
        continue; // Skip the rest of the code in this iteration for even numbers
    }
    // Code to execute for odd numbers
}



```


8. Match (Introduced in PHP 8.0)

```php
 $result = match ($value) {
    1 => 'One',
    2 => 'Two',
    default => 'Other',
};

echo $result; // Outputs the corresponding value

```
9. Try, Catch, Finally

```php

try {
    // Code that may throw an exception
} catch (ExceptionType $e) {
    // Code to handle the exception
} finally {
    // Code that will always run, regardless of whether an exception was thrown
}



```
