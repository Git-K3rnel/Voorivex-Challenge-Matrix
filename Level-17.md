# Level-17

Level17-18 (https://matrix.voorivex.academy/the-end-of-m0rpheus)

send this request:
```
https://matrix.voorivex.academy/the-end-of-m0rpheus/?show-me-the-codes
```

you will get a php code :

```php
<?php
if (isset($_GET['show-me-the-codes'])) {
    show_source("index.php");
    exit();
}

if ($_COOKIE['code'] == 'ｦｲｸ\'ｺｿ') {
    require_once("next.php");
    die($next);
}

?>
```

do not set cookie in burp or browser storage, do it in console:

```javascript
document.cookie = 'code=ｦｲｸ\'ｺｿ'
```

refresh the page you will get this :

```text
/dangEr-level-100
```

go to:

```text
https://matrix.voorivex.academy/dangEr-level-100
```
