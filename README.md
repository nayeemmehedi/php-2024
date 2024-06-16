### basic

```php

$ages = ["Alice" => 25, "Bob" => 30, "Charlie" => 35];

$json = json_encode($ages);

echo $json;

ans : {"Alice":25,"Bob":30,"Charlie":35}

```

## middium

```php
<?php

$people = [
    ["name" => "Alice", "age" => 25],
    ["name" => "Bob", "age" => 30],
    ["name" => "Charlie", "age" => 35]
];

$json = json_encode($people);

echo $json;

?>
ans: [{"name":"Alice","age":25},{"name":"Bob","age":30},{"name":"Charlie","age":35}]

```
## advance

```php
<?php

$ages = ["Alice" => 25, "Bob" => 30, "Charlie" => 35];

$json = json_encode($ages);

if (json_last_error() === JSON_ERROR_NONE) {
    echo $json;
} else {
    echo "JSON encode error: " . json_last_error_msg();
}

?>

```
