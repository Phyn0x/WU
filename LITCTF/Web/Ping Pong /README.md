# Ping pong

## Enoncé :

*I made this cool website where you can ping other websites!*\

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

Il n'y a pas de vérification sur notre input, qui va donc être la vulnérabilité que nous allons chercher à exploiter.

## Flag

<details>
<summary>🚩</summary>

```
LITCTF{oOps_sh0uld_h4v3_us3d_str1ct_c0mp4r1sons}
```
</details>
