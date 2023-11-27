# Level-22

Level22-23 (https://matrix.voorivex.academy/agent-s-fight-nuMber-tWo)

send this request:
```text
https://matrix.voorivex.academy/agent-s-fight-nuMber-tWo/?show-me-the-codes
```

you will get a php code:

```php
<?php
if (isset($_GET['show-me-the-codes'])) {
    show_source("index.php");
    exit();
}

if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    
    // Get the raw POST data
    $json_data = file_get_contents('php://input');
    
    // Decode the JSON data into a PHP array
    $data = json_decode($json_data, true);
    
    if ($data === NULL) {
        // Handle JSON decoding error
        echo json_encode(['error' => 'Invalid JSON']);
        exit();
    }

    if (array_key_exists('code', $data)) {
        if(strcmp($data['code'], NULL) === 0){
            require_once("next.php");
            die($next);
        }
    }
}

?>
```

the code needs a post request with json data with a key called `code` and no value
send this request:

```text
curl -X POST -d '{"code":""}' https://matrix.voorivex.academy/agent-s-fight-nuMber-tWo/

/let-us-go-to-save-him!
```

now go to :

```text
https://matrix.voorivex.academy/let-us-go-to-save-him!
```
