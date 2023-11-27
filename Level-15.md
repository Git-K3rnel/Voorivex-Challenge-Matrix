# Level-15

Level15-16 (https://matrix.voorivex.academy/the-cat-is-a-gliTch)

send this request :
```text
https://matrix.voorivex.academy/the-cat-is-a-gliTch/?show-me-the-codes
```
you will get a php code:
```php
<?php
if (isset($_GET['show-me-the-codes'])) {
    show_source("index.php");
    exit();
}

// require_once("walls-can-be-broken.php");
?>
```
send a request to :
```text
https://matrix.voorivex.academy/the-cat-is-a-gliTch/walls-can-be-broken.php
```
you will get an error :
```
 Notice: Undefined index: wall in /var/www/html/level-15-the-cat-is-a-gliTch/walls-can-be-broken.php on line 5
```
now send this request:
```text
https://matrix.voorivex.academy/the-cat-is-a-gliTch/walls-can-be-broken.php?wall=1
```
you will get this error:
```text
 Warning: Use of undefined constant crack - assumed 'crack' (this will throw an Error in a future version of PHP) in /var/www/html/level-15-the-cat-is-a-gliTch/morpheus-is-behind-the-wall.inc on line 4
```
now send a request to:
```text
https://matrix.voorivex.academy/the-cat-is-a-gliTch/morpheus-is-behind-the-wall.inc
```
and you will get this :
```php
<?php

$next_level = 'morPheus-vS-sMith!';
crack
?>
```
go to:
```text
https://matrix.voorivex.academy/morPheus-vS-sMith!
```
