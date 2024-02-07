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

Quelqu'un qui commence à utiliser les réseaux sociaux, il est logique de chercher sur les réseaux les plus évidents : Facebook et Instagram.
En cherchant sur Facebook nous trouvons plusieurs comptes avec le nom "Louise Colet" mais nous finissons par trouver [le bon](https://www.facebook.com/profile.php?id=100091643933854).

## Flag

Nous trouvons le flag dans la section **A propos > Détails sur Louise** :

<details>
<summary>🚩</summary>

```
404CTF{4_mon_ch3r_4mi_v1ctor}
```
</details>
