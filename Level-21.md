# Level-21

Level21-22 (https://matrix.voorivex.academy/agent-fight-nuM-onE/)

send this request:

```text
https://matrix.voorivex.academy/agent-fight-nuM-onE/?show-me-the-codes
```

you will get a php code:

```php
<?php
if (isset($_GET['show-me-the-codes'])) {
    show_source("index.php");
    exit();
}

if ($_GET["code"] >= 10000 && $_GET["code"] <= 99999) {
    if (md5($_GET["code"] . "Matrix") == "389f3ebb14f4d3f20ad4c56a13393379") {
        require_once("next.php");
        die($next);
    }
}

?>
```

this code needs us to find a number between 10000 and 99999 then concat it with the word `Matrix`
to get the desired hash, i wrote a python script to do it:

```python
import hashlib

myhash = '389f3ebb14f4d3f20ad4c56a13393379'

for i in range(10000,99999):
    string = str(i) + 'Matrix'
    ca_hash = hashlib.md5(string.encode()).hexdigest()
    if ca_hash == myhash:
        print(i)
```
and i found this number :

```text
77700
```
then send this request:

```text
curl https://matrix.voorivex.academy/agent-fight-nuM-onE/?code=77700

/agent-s-fight-nuMber-tWo
```

now go to:

```text
https://matrix.voorivex.academy/agent-s-fight-nuMber-tWo
```
