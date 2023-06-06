# L'âme d'un poète et le coeur d'une femme 1/4
> Difficulté : Facile


## Enoncé :

*Une jeune femme s'approche de votre table : « Bonjour, j'ai cru comprendre que vous aviez fait vos preuves lors de précédentes enquêtes. J'aurais besoin de votre aide. Connaissez vous une certaine 'Louise Colet' ? J'ai appris qu'elle commencait à utiliser les réseaux sociaux. Pouvez vous m'aider à trouver plus d'informations sur elle ? »*

## Solution

Quelqu'un qui commence à utiliser les réseaux sociaux, il est logique de chercher sur les réseaux les plus évidents : Facebook et Instagram.
En cherchant sur Facebook nous trouvons plusieurs comptes avec le nom "Louise Collet" mais nous finissons par trouver [le bon](https://www.facebook.com/profile.php?id=100091643933854).

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
Mais où peut-on donc trouver des informations sur ce **projet** ? ... *bruit d'idée*
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


## Flag



<details>
<summary>🚩</summary>

```
404CTF{https://discord.gg/NeCgh9ZZqD}
```
</details>
