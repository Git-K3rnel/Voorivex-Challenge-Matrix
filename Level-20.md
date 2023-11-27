# Level-20

Level20-21 (https://matrix.voorivex.academy/dang3r-finishEd-all-cleared)

send this request:

```text
https://matrix.voorivex.academy/dang3r-finishEd-all-cleared/?show-me-the-codes
```

you will get a php code:

```php
<?php
if (isset($_GET['show-me-the-codes'])) {
    show_source("index.php");
    exit();
}

if ($_GET["code"] == file_get_contents("secret-m")) {
    require_once("next.php");
    die($next);
}

?>
```

get the content of the `secret-m` file which is :

```text
MatrixHasYou...☺..........
```

i wrote a python script to send whatever format the previous string has as a parameter in
new request :

```python
import requests

url = 'https://matrix.voorivex.academy/dang3r-finishEd-all-cleared/secret-m'
res = requests.get(url)
result = res.text
print(result)
url2 = f'https://matrix.voorivex.academy/dang3r-finishEd-all-cleared/?code={result}'
res2 = requests.get(url2)
print(res2.text)
```

and i got this:

```text
/agent-fight-nuM-onE
```

now go to:

```text
https://matrix.voorivex.academy/agent-fight-nuM-onE
```
