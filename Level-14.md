# Level-14

Level14-15 (https://matrix.voorivex.academy/Done-w1th-0racle)

send this request:

```text
https://matrix.voorivex.academy/Done-w1th-0racle/?show-me-the-codes
```

you will get a php code:

```php
<?php
if (isset($_GET['show-me-the-codes'])) {
    show_source("index.php");
    exit();
}
require_once("cookie.php");
?>
```

send a request to this path and use the same cookie you found in level13:

```text
curl -H "Cookie: oracle=07409c1ca296c6df5396f6044d5ab132" https://matrix.voorivex.academy/Done-w1th-0racle/

/the-cat-is-a-gliTch
```

go to:

```text
https://matrix.voorivex.academy/the-cat-is-a-gliTch
```
