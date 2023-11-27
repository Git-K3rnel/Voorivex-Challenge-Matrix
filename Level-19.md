# Level-19

Level19-20 (https://matrix.voorivex.academy/m0re-dangeR-needed/)

send this request:

```text
https://matrix.voorivex.academy/m0re-dangeR-needed/?show-me-the-codes
```

you will get this php code:

```php
<?php
if (isset($_GET['show-me-the-codes'])) {
    show_source("index.php");
    exit();
}

if (hash('SHA256', $_GET["code"]) == "92615529c262cc0d45e57aa13a4a067b11cd2e8fdc015346cd24a6d69e6d4831") {
    require_once("next.php");
    die($next);
}

?>
```

just bruteforce the hash online or with john, you will get this password:

```text
P@ssw0rd@123
```

then send this request:
```text
curl https://matrix.voorivex.academy/m0re-dangeR-needed/?code=P@ssw0rd@123
/dang3r-finishEd-all-cleared
```

go to:

```text
https://matrix.voorivex.academy/dang3r-finishEd-all-cleared
```
