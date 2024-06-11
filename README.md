## Types of Arrays
   
***PHP supports `three` main types of arrays:***
1. Indexed Arrays : $fruits = ["Apple", "Banana", "Cherry"];
2. Associative Arrays : $ages = ["Alice" => 25, "Bob" => 30, "Charlie" => 35];
3. Multidimensional Arrays : $contacts = [
    ["name" => "Alice", "email" => "alice@example.com"],
    ["name" => "Bob", "email" => "bob@example.com"]

];

```php

// Indexed array
echo $fruits[1]; // Outputs: Banana

// Associative array
echo $ages["Alice"]; // Outputs: 25

// Multidimensional array
echo $contacts[0]["name"]; // Outputs: Alice



```

4. Modifying Arrays :

a. Adding Elements :

```php

$fruits[] = "Date"; // Adds "Date" to the end of the array

$ages["David"] = 40; // Adds a new key-value pair to the associative array

```

b. Modifying Elements :

```php
$fruits[1] = "Blueberry"; // Changes "Banana" to "Blueberry"

$ages["Alice"] = 26; // Updates Alice's age to 26

```

c. Removing Elements : 

```php

unset($fruits[2]); // Removes "Cherry" from the array

unset($ages["Bob"]); // Removes Bob's entry from the associative array


```

5. Common Array Functions


```php

$numbers = [1, 2, 3, 4, 5];

// Count elements in an array
echo count($numbers); // Outputs: 5

// Merge two or more arrays
$moreFruits = ["Elderberry", "Fig"];
$allFruits = array_merge($fruits, $moreFruits);

// Check if a key exists in an array
if (array_key_exists("Alice", $ages)) {
    echo "Alice is in the array";
}

// Check if a value exists in an array
if (in_array("Banana", $fruits)) {
    echo "Banana is in the array";
}

// Get all keys or values from an array
$keys = array_keys($ages);
$values = array_values($ages);



```

6. Sorting Arrays

```php

$numbers = [3, 1, 4, 1, 5, 9];

// Sort an array in ascending order
sort($numbers);

// Sort an array in descending order
rsort($numbers);

// Sort an associative array by values
asort($ages);

// Sort an associative array by keys
ksort($ages);


```

7. Iterating Over Arrays

 ```php

   foreach ($fruits as $fruit) {
    echo $fruit . " ";
}
// Outputs: Apple Banana Blueberry Date

foreach ($ages as $name => $age) {
    echo "$name is $age years old. ";
}
// Outputs: Alice is 26 years old. Charlie is 35 years old. David is 40 years old.



```


8. Multidimensional Arrays

```php

foreach ($contacts as $contact) {
    echo "Name: " . $contact["name"] . ", Email: " . $contact["email"] . "\n";
}
// Outputs:
// Name: Alice, Email: alice@example.com
// Name: Bob, Email: bob@example.com



```

9. Array Destructuring

```php

$person = ["Alice", 25, "alice@example.com"];
[$name, $age, $email] = $person;

echo $name; // Outputs: Alice
echo $age; // Outputs: 25
echo $email; // Outputs: alice@example.com


```


