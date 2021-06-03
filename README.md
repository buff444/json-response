# json-response
Simple class with properly formatted json response with HTTP status

## Installation
composer require person55/json-response

### Usage
```php
<?php
require_once __DIR__ ."/vendor/autoload.php";

use Person55\ResponseClass\JsonResponse;

$student = array(
    'name' => 'John Doe',
    'course' => 'Software Engineering',
    'level' => '200',
    'collections' => ['books' => 'Intro to UML', 'music' => 'rap']

);
new JsonResponse('ok','', $student);


```


### Param 1 (Required)
1. success or ok - 200 http status
2. unauthorized - 401 http status
3. exception - 500 http status (internal server error)

### Param 2 (Optional)
string - the return message, use empty quote if not available

### Param 3 (Optional)
rray - Array of Data