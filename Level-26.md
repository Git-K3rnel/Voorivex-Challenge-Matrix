# Level-26

Level26-27

Send this request:

```text
https://matrix.voorivex.academy/the-final-fight-0a9fe5e4822afb91b8683e3d332h263h/?show-me-the-codes
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

we need to provide two values which are different but has the same hash value
the best example for it could be providing a `NULL` and empty value
i mean you should send an empyt string and not sending the second paramter so it becomes NULL
now PHP calculates the MD5 of NULL and empty string that is a same value `d41d8cd98f00b204e9800998ecf8427e`

```text
https://matrix.voorivex.academy/the-final-fight-0a9fe5e4822afb91b8683e3d332h263h/?code1=
```

now you will get this :

```text
/the-final-fight-57a31594d5784b29e02960fd427f8703
```

go to:

```text
https://matrix.voorivex.academy/the-final-fight-57a31594d5784b29e02960fd427f8703
```





