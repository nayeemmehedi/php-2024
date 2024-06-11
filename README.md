## String Functions

`strlen()` : Returns the length of a string.

  ```php
echo strlen("Hello, world!"); // Output: 13

```

The `.` operator is used to concatenate strings.

```php

$str1 = "Hello, ";
$str2 = "world!";
echo $str1 . $str2; // Output: Hello, world!

```

Substrings : `substr()` Returns a part of a string.

```php

echo substr("Hello, world!", 7, 5); // Output: world

```

String Position : `strpos()` Finds the position of the first occurrence of a substring.

```php
echo strpos("Hello, world!", "world"); // Output: 7
```

String Replacement

`str_replace()`: Replaces all occurrences of a search string with a replacement string.

```php
echo str_replace("world", "PHP", "Hello, world!"); // Output: Hello, PHP!
```

Case Conversion

strtoupper(): Converts a string to uppercase.
strtolower(): Converts a string to lowercase.

```php
echo strtoupper("Hello, world!"); // Output: HELLO, WORLD!
echo strtolower("Hello, World!"); // Output: hello, world!
```

Trimming

`trim()`: Removes whitespace or other characters from both ends of a string.
`ltrim()`: Removes whitespace or other characters from the beginning of a string.
`rtrim()`: Removes whitespace or other characters from the end of a string.

```php
echo trim("  Hello, world!  "); // Output: Hello, world!
echo ltrim("  Hello, world!  "); // Output: Hello, world!  
echo rtrim("  Hello, world!  "); // Output:   Hello, world!
```



