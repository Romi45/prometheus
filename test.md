# Questions extraites des tests

## Test C/TP1 gr3_2025

### Question 1
On utilise un système multiporteuses avec : 3 sous-porteuses orthogonales rapprochées au maximum, une QPSK dans chacune, et un temps symbole de 10 ms.

**Que vaut le débit binaire (en b/s) ?**

**Quels éléments faut-il utiliser dans chaque branche du récepteur pour réaliser LE MEILLEUR récepteur analogique possible ?**
- un mixeur qui multiplie par l'exponentielle complexe de fréquence -fi
- un filtre passe-bas qui coupe à 100 Hz
- un filtre passe-bas qui coupe à 200 Hz
- un filtre passe-bande centré sur fi
- un circuit intégrateur sur le temps symbole

---

### Question 2
On dispose d'une bande de 1,5 MHz.
On utilise un temps symbole de 0,1 ms.

Combien peut-on, au maximum, utiliser de sous-porteuses dans cette bande, si on utilise pour cela des sous-porteuses orthogonales sur le temps symbole ?

**Comment s'appelle la caractéristique de notre transmission que l'on optimise alors ? (réponse en minuscule)**

---

### Question 3
Les sinusoïdes représentées ci-dessous sont-elles orthogonales, sur l'intervalle de temps considéré [0, 1 ms] ?

![Graphique des sinusoïdes](https://via.placeholder.com/600x400)

- a. OUI
- b. on ne peut pas répondre au vu de cette image
- c. NON

## Test C/TP5 gr3_2025

### Question 1
Soit un système OFDM à 4 porteuses utiles dans une transmission.

**Accolade** : Tableau de bord - Mode const. - Aide à... - Aide à l'application...

**grande nombre porteuses** : nombre de porteuses utilisées : un entier

**Démodulation Diagramme**

![Diagramme](https://via.placeholder.com/600x400)

**Reponse**

- le bruit est un problème : **OUI**
- on n'a pas utilisé un profil de fréquence suffisamment : **NON**
- la valeur de l'ICI) est : 0,2 **non**

---

### Question 2
En OFDM, on utilise les paramètres suivants :
- N = 36
- N_FFT = 64
- N_CP = 16

**On veut pénaliser un symbole d'information pour que celui-ci soit par schéma et ICI dans les trames contiennent les symboles OFDM**

A la transmission, on ajoute un intervalle de garde. Cet intervalle de garde est-il toujours utile ? **NON**

**La réponse correcte est : **NON**

---

### Question 3
En OFDM, y a-t-il un avantage à utiliser un temps de symbole et ICI pour chaque symbole d'information ?

- a. oui car cela permet de réduire l'effet de l'écho
- b. et les modulations à éviter les interférences provoquées par les éléments voisins sur la fréquence porteuse
- c. et l'interpolation, et est compensé par l'intervalle symbole choisi par avance
- d. à la transmission, et est compensé par l'intervalle symbole choisi par avance

**La réponse correcte est : **c**

---

### Question 4
Ces effets sur la transmission OFDM avec les paramètres suivants :
- N_FFT = 256
- N_CP = 64
- N = 128

**Quelle est la bande occupée, en MHz ?** 20 MHz

**Quelle est la valeur ICI, en MHz ?** 16/27

**Quel est l'intervalle de garde, en MHz ?** 200 ns

**Quelle est la valeur de la composante continue, en MHz ?** 200 ns

**Quelle est la valeur de la composante continue, en MHz ?** 200 ns

---

### Question 5
En 802.11a et 802.11n, on a les paramètres suivants :
- N_FFT = 64
- N_CP = 16
- N = 48

**Quelle est la valeur de l'ICI, en MHz ?** 1/12.8

**Quelle est la valeur de l'intervalle de garde, en MHz ?** 1/12.8

**Quelle est la valeur de la composante continue, en MHz ?** 1/12.8

**Quelle est la valeur de la composante continue, en MHz ?** 1/12.8

## Test C/TP2 gr3_2025

### Question 1
Le signal OFDM ci-dessous a été obtenu en prenant un temps de garde correctement choisi en fonction des caractéristiques du canal.

![Graphique](https://via.placeholder.com/600x400)

**Quelle est la durée nécessaire pour que les temps d'arrivée soient tous inférieurs, arrondis au plus proche, et réponse en ms ?**

**Réponse : **10**

---

### Question 2
On génère un signal OFDM en utilisant une FFT, les paramètres choisis sont les suivants :
- N = 1024
- N_FFT = 128
- N_CP = 32

**Donnez la valeur d'un symbole utile, en MHz :**

**Réponse : **12**

---

### Question 3
On souhaite transmettre OFDM et on choisit les paramètres suivants :
- N = 1024
- N_FFT = 128
- N_CP = 32

**La bande doit-elle être plus grande que la bande utile ?**

**Réponse : **OUI**

---

### Question 4
On souhaite transmettre OFDM et on choisit les paramètres suivants :
- N = 1024
- N_FFT = 128
- N_CP = 32

**Quelle est la durée du temps de garde, présent à chaque début de temps symbole OFDM (réponse en ms) ?**

**Réponse : **0.1**

---

### Question 5
Sur un canal avec les caractéristiques d'un système OFDM, dans un canal tel que ΔTmax = 500 ns, la bande absolue vaut 12 MHz.

**Quel est le MEILLEUR choix de paramètres selon vous ?**

- a. Tu = 50 μs, N = 115, N_FFT = 256
- b. Tu = 200 ns, N = 2, N_FFT = 16
- c. Tu = 1 μs, N = 115, N_FFT = 12
- d. Tu = 50 μs, N = 115, N_FFT = 128

**La réponse correcte est : **Tu = 50 μs, N = 115, N_FFT = 256**

---

### Question 6
Apparence de notions en reprenant des idées vagues, du type à l'aide :

**Le canal a un temps de cohérence de 10 ms maximum.**

- le récepteur se déplace donc le canal varie
- le récepteur se déplace donc le canal est statique en fréquence
- la réponse impulsionnelle décrivible du canal a des coefficients aléatoires
- chaque chemin principal donne lieu à des réflexions, diffractions locales

**La réponse correcte est : **le récepteur se déplace donc le canal varie**

---

### Question 7
OFDM permet l'obtention de hauts débits en transmission radio.

**Quel est le paramètre qui permet de faire en sorte de l'on compare aux modulations monoporteuses par exemple ?**

- a. il y a des nombresuses superpositions : permettre le débit total est la somme des débits dans chaque sous-porteuse, il augmente, le débit utile
- b. on peut grâce à cela les contributions sont dispersibles
- c. c'est l'utilisation des sous-porteuses qui sont la largeur de bande allouée

**La réponse correcte est : **c**

---

### Question 8
En pratique, quels sont les principaux avantages de l'OFDM par rapport aux autres modulations ?

- a. pas de filtre
- b. VRAI
- c. FAUX

**La réponse correcte est : **VRAI**

---

### Question 9
On veut faire transmettre OFDM avec les paramètres suivants :
- temps utile du temps symbole : Tu = 0.5 μs
- N_FFT = 128
- N = 120

**Quel est la bande occupée ?** Réponse en MHz : **200**

**Quel est la fréquence d'échantillonnage ?** Réponse en MHz : **256**

**Quel est l'intervalle entre deux porteuses ?** Réponse en MHz : **2**

---

### Question 10
Soit un canal avec deux chemins principaux dont les délais d'arrivée sont de 0 et 2.33 ms, respectivement.

Soit L = 320ns, temps d'un échantillonnage à moins critical.

**Quel est le temps de garde nécessaire pour éviter les ISI (Inter Symbol Interference) pour réduire les composantes lentes cela est dans le paramètre ?** Choix :

- a. 0 ns
- b. 200 ns
- c. 400 ns
- d. 1000 ns

**Quel sera l'indice du dernier coefficient non nul de h ?** (Attention la première index est 0) : **1**
