# L'inondation
> Difficulté : Introduction


## Enoncé :

*Vous prenez une collation accolé au bar du Procope, et remarquez au bout d'une dizaine de minutes un post-it, sur lequel votre nom est écrit, et en dessous une inscription : « Salut, le nouveau, viens à ma rencontre, porte de derrière ».
Curieux, vous sortez du café par cette porte et tombez nez à nez avec un jeune homme.

« Bonjour, pouquoi ce post-it ?

— Salut ! Excellente question. Dernièrement, un évènement étrange a bouleversé ma ville : elle a été prise d'une épidémie de gens se transformant en rhinocéros. Alors que ce n'était jusqu'hier qu'une dizaine de gens qui étaient touchés, j'ai vu ce matin un troupeau de ce qui semblait être plusieurs centaines de rhinocéros passer sous ma fenêtre. J'ai aussitôt saisi mon appareil photo et photographié régulièrement le troupeau pour avoir une estimation du nombre de rhinocéros, mais il y en a bien trop pour compter tout ça à moi seul ou même à deux.

— Certes, et où voulez-vous donc en venir ?

— Voyez-vous, j'ai entendu parler de vos talent dans les nouvelles technologies par le biais d'un ami qui fréquente ce café. J'imagine qu'un ordinateur saura compter bien plus vite que nous deux, ça vous dirait de m'aider ? D'ailleurs, on ne s'est toujours pas présentés. Moi, c'est Béranger. »


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
