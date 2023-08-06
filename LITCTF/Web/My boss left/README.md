# My boss left

## Enoncé :

*My boss left... Guess I can be a bit more loose on checking people.*
*http://litctf.org:31784/*

## Solution

En suivant ce site, nous trouvons une page de login.\
Mais nous avons à notre disposition un .zip, dans lequel nous trouvons les éléments du site, notamment **login.php** :\

```php
<?php
// Check if the request is a POST request
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    // Read and decode the JSON data from the request body
    $json_data = file_get_contents('php://input');
    $login_data = json_decode($json_data, true);

    // Replace these values with your actual login credentials
    $valid_password = 'dGhpcyBpcyBzb21lIGdpYmJlcmlzaCB0ZXh0IHBhc3N3b3Jk';

    // Validate the login information
    if ($login_data['password'] == $valid_password) {
        // Login successful
        echo json_encode(['status' => 'success', 'message' => 'LITCTF{redacted}']);
    } else {
        // Login failed
        echo json_encode(['status' => 'error', 'message' => 'Invalid username or password']);
    }
}
?>
```

Nous lisons clairement qu'il y a un "mot de passe valide" qui devrait nous permettre de nous authentifier, sans précision sur le nom d'utilisateur.\
C'est ce que nous faisons, et trouvons le flag.


## Flag

<details>
<summary>🚩</summary>

```
LITCTF{oOps_sh0uld_h4v3_us3d_str1ct_c0mp4r1sons}
```
</details>
