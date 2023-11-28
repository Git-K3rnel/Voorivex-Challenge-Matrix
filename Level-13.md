# Level-13

send this request:

```text
https://matrix.voorivex.academy/meet-tHe-0racle/?show-me-the-codes
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

send request to this path:

```text
https://matrix.voorivex.academy/meet-tHe-0racle
```

you will get lots of cookies, one of them has the path attribute like this:

```text
/Done-w1th-0racle
```

go to:

```text
https://matrix.voorivex.academy/Done-w1th-0racle
```
