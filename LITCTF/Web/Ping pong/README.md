# Ping pong

## Enoncé :

*I made this cool website where you can ping other websites!*

Le site se présente de la forme :

<p align="center">
  <img src="photo1.jpg" alt="photo1" width="600">
</p>

Nous avons à notre disposition un .zip avec les éléments du site, notamment :

```py
from flask import Flask, render_template, redirect, request
import os

app = Flask(__name__)

@app.route('/', methods = ['GET','POST'])
def index():
    output = None
    if request.method == 'POST':
        hostname = request.form['hostname']
        cmd = "ping -c 3 " + hostname
        output = os.popen(cmd).read()

    return render_template('index.html', output=output)
```

## Solution

Il n'y a pas de vérification sur notre input, qui va donc être la vulnérabilité que nous allons chercher à exploiter.\
Nous allons injecter un payload nous permettant de récupérer le contenu de flag.txt.\
Pour cela, nous devons être capables d'écrire 2 commandes distinctes dans le cmd sur la même ligne, afin de valider la première, puis exécuter notre payload.\
\
Ainsi notre payload va prendre la forme : `127.0.0.1 ; cat flag.txt`.\
De cette manière, l'instruction finale exécutée sera de la forme : `ping -c 3 127.0.0.1 ; cat flag.txt`.

## Flag

<details>
<summary>🚩</summary>

```
LITCTF{I_sh0uld_b3_m0r3_c4r3ful}
```
</details>
