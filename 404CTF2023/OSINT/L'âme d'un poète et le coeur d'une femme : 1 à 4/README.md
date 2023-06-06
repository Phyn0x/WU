# L'âme d'un poète et le coeur d'une femme 1/4
> Difficulté : Facile


## Enoncé :

*Une jeune femme s'approche de votre table : « Bonjour, j'ai cru comprendre que vous aviez fait vos preuves lors de précédentes enquêtes. J'aurais besoin de votre aide. Connaissez vous une certaine 'Louise Colet' ? J'ai appris qu'elle commencait à utiliser les réseaux sociaux. Pouvez vous m'aider à trouver plus d'informations sur elle ? »*

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
  
# L'âme d'un poète et le coeur d'une femme 2/4
> Difficulté : Facile


## Enoncé :

*« Vous avez réussi à trouver toutes ces informations ? Félicitations ! Mais avez vous entendu parler de l'évènement organisé par Mme Colet ? »*

## Solution

Nous avons trouvé le premier flag sur Facebook, et en fouillant nous ne trouvons pas davantage d'informations. Allons voir sur instagram.
Nous cherchons Louise Colet et trouvons [ce compte](https://www.instagram.com/colet_louise/).

## Flag

Le seul post existant nous donne l'information recherchée, que nous mettons au format du flag :

<details>
<summary>🚩</summary>

```
404CTF{25_mai_colet_louise}
```
</details>

# L'âme d'un poète et le coeur d'une femme 3/4
> Difficulté : Facile


## Enoncé :

*« C'est exactement ça ! 'Le salon littéraire de Louise Colet'. Pensez vous pouvoir me trouver une invitation ? »*

## Solution

Nous cherchons donc une invitation, soit un lien discord (l'évènement se déroulant sur discord).
Cepedant, en cherchant les réseaux classiques nous ne trouverons rien.
Mais où peut-on donc trouver des informations sur ce **projet** ? ... *\*bruit d'idée\**<br>
Qui dit projet dirait GitHub ? C'est bien [là](https://github.com/LouiseRevoil/Salon-litteraire-de-Louise-Colet) que nous trouvons ce que nous cherchons.

## Flag

Nous trouvons l'invitation tout en bas du README.md :

<details>
<summary>🚩</summary>

```
404CTF{https://discord.gg/NeCgh9ZZqD}
```
</details>

# L'âme d'un poète et le coeur d'une femme 4/4
> Difficulté : Moyenne


## Enoncé :

*« Je vous remercie pour l'invitation ! Avez-vous pu vous en procurer une ? J'ai entendu dire que Mme Colet tenait ce salon pour permettre à des personnes talentueuse de se rencontrer. Je suis sûre qu'elle sera ravie de faire votre connaissance, vos talents ne sont plus à démontrer. Peut-être qu'en répondant à ses questions, vous pourrez obtenir un cadeau de sa part ? »*

## Solution

Nous avons utilisé le flag précédenant pour [rejoindre le serveur discord](https://discord.gg/NeCgh9ZZqD) de Louise Colet et arrivons maintenant sur la dernière étape de la série de challenge.
Cette étape se constitue de plusieurs petites étapes.
Nous écrivons `le_petit_salon` pour aller à la première étape.
* le-petit-salon :<br>
    *Bonjour , savez vous en quelle année un promeneur inoccupé qui, sortant du jardin des Tuileries, se serait dirigé sous les arcades de la rue de Rivoli, aurait pu apercevoir sous la porte cochère d'un des plus beaux hôtels du quartier, un grand vieillard à la chevelure et à la moustache blanches ?*<br>
    En cherchant dans google *La porte cochère...->...moustache blanche* nous trouvons assez facilement l'année : <details><summary>🚩</summary>```1835```</details>
* le-boudoire :<br>
    Complétez la suite du poème :<br>
    *Laisse à l'homme la gloire,*<br>
    *Les triomphes, le bruit,*<br>
    En cherchant ces vers en ligne, nous trouvons [ce site](https://www.persee.fr/doc/grif_0770-6081_1975_num_7_1_1458) qui nous donne la suite du poème : <details><summary>🚩</summary>```Pour nous, aimer et croire Au bonheur nous conduit.```</details>
     
* le-fumoir :<br>
    *Où et quand ai-je rendu visite à Mon ami Victor Hugo pour la première fois ?*<br>
    En cherchant, nous trouvons [ce site](https://gallica.bnf.fr/ark:/12148/bpt6k8572147/f7.item) où on trouve les extraits d'un livre parlant de Hugo et Colet.
    Nous y trouvons ce que nous cherchons : <details><summary>🚩</summary>```Guernesey_1857```</details>

## Flag

Notre réussite à toutes ces étapes nous donne le flag final dans le salon `la-bibliothèque`.


<details>
<summary>🚩</summary>

```
404CTF{j3_su1s_ravie_d_av0ir_fait_v0tre_connaiss4nce} 
```
</details>
