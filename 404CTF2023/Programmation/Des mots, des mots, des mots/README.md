# Des mots, des mots, des mots
> Difficulté : Difficile


## Enoncé :

*Prenant du bon temps à votre table en lisant un livre, vous buvez une gorgée de café. En baissant votre tasse, vous remarquez à travers la fenêtre une petite silhouette, elle semble chercher quelque chose ou quelqu'un.*

*Cette intrigante situation vous pousse à aller à sa rencontre. La silhouette est en réalité une jeune fille rousse. Vos regards se croisent, elle a l'air perdue. Vous la rejoignez, et lui demandez :*

*« Bonjour, puis-je t'aider ?*
*— Oui. Je cherche à traduire un texte selon des règles étranges mot à mot. Il s'agit d'un livre nommé Les Misérables. Peux-tu m'aider ? Au fait, moi c'est Cosette !*
*— Je vois, aucun problème. Je peux justement te faire un script qui va transformer chaque mot de ton texte. Quelles sont ces règles ?*
*— Je vais tout t'expliquer, allons nous installer à l'intérieur.»*

*Elle vous suit à votre table et vous vous mettez au travail.*


## Solution

En utilisant la commande `nc challenges.404ctf.fr 31420` nous constatons que nous avons besoin de créer un algorithme qui compte le nombre de rhinocéros et renvoie ce nombre.

Ci-joint le code commenté corresponsdant à la résolution de ce challenge :

```py
from pwn import *

conn = remote('challenges.404ctf.fr',31420)
for i in range(100) :                         #Après test, nous avons vu qu'il y avait 100 itérations de l'algo à faire.
    temp = conn.recvuntil(b">")               #Nous recevons jusqu'à ce caractère, qui correspond à la demande d'input.
    print(temp.decode())
    nb = temp.decode().count("~c`°^)")        #Compte des rhinocéros
    print(nb)
    conn.sendline(str(nb).encode())           #Envoi du nombre
    ans = conn.recvline().decode()
    print(ans)
result = conn.recvall()                       #Après avoir répondu correctement à toutes les itérations, nous recevons le flag.
print(result.decode())
```

## Flag

<details>
<summary>🚩</summary>

```
404CTF{4h,_l3s_P0uvo1rs_d3_l'iNforM4tiqu3!}
```
</details>




