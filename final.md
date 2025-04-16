# Question 1

On fait une transmission multiporteuses et on choisit les paramètres suivants :
- un temps utile \( T_u = 1 \) ms
- des sous-porteuses de fréquences \( f_1 = -4.5 \) kHz, \( f_2 = -1.5 \) kHz, \( f_3 = 0 \) kHz, \( f_4 = 1.5 \) kHz, \( f_5 = 4.5 \) kHz

Dites si les affirmations suivantes sont vraies ou fausses :

- Sur le temps utile, les fréquences sont toutes orthogonales deux à deux : **FAUX**
- on peut, à la réception, utiliser pour chaque sous-canal un mixer et un filtre passe-bas de fréquence de coupure 4 kHz : **FAUX**
- on peut, à la réception, utiliser pour chaque sous-canal un mixer et un filtre passe-bas de fréquence de coupure 1 kHz : **VRAI**

# Question 2

Compléter le schéma ci-dessous, permettant de mettre en place un récepteur OFDM (dont tirant parti de l'orthogonalité) analogique jusqu'au bloc de demapping, avec \( T_u = T_s \) (pas de temps de garde).

![Schéma](https://via.placeholder.com/800x400)

# Question 3

Un récepteur multifréquences tirant parti de l'orthogonalité, mais qui calcule les produits scalaires sous forme analogique n'est pas réalisable à grande échelle. Pourquoi ?

- a. Il prend trop de place ⊙
- b. Il oblige à laisser une bande de garde entre sous-canaux
- c. Il est trop cher ⊙
- d. Il ne permet pas d'atteindre un grand débit

**Réponses correctes :**
- Il est trop cher
- Il prend trop de place

# Question 4

Un récepteur numérique à FFT réalise des produits scalaires entre le signal reçu, appelé \( y[k] \) (ou \( x[k] \) si le canal est parfait), et les fonctions de la base des exponentielles complexes. Vrai ou Faux ?

- a. Peut-être
- b. VRAI ⊙
- c. FAUX

**Réponse correcte :**
VRAI

# Question 5

On relève le spectre reçu après transmission sur un canal multichemins et retour en bande de base :

![Graph](https://via.placeholder.com/600x400)

Au vu de ce relèvé, vous direz que la bande de cohérence est plutôt de l'ordre...

- a. de 20 kHz
- b. de 100 kHz
- c. on ne peut pas répondre avec ce seul relèvé
- d. de 4 kHz ⊙

**Réponse correcte :**
de 4 kHz

# Question 6

On modélise un canal multichemins en utilisant, pour les différents chemins, des gains complexes. Pourquoi ?

- a. Parce que c'est ce que fait Matlab
- b. C'est un facteur de normalisation, pour tenir compte du délai de la première copie reçue (qu'on suppose reçue à \( t = 0 \))
- c. Parce que c'est toujours comme ça en régime harmonique (permet de ne pas avoir de cosinus)
- d. Parce que ce serait trop simple avec des signaux réels
- e. Parce qu'on utilise un modèle en bande de base, incluant, en plus du canal, les étapes de transposition côté émetteur et récepteur. Pour une sinusoïde à fréquence porteuse, le délai crée un déphasage, qui se retrouve, une fois faite la transposition en bande de base, dans la phase du signal \( y(t) \) [ui même déjà complexe] ⊙

**Réponse correcte :**
Parce qu'on utilise un modèle en bande de base, incluant, en plus du canal, les étapes de transposition côté émetteur et récepteur. Pour une sinusoïde à fréquence porteuse, le délai crée un déphasage, qui se retrouve, une fois faite la transposition en bande de base, dans la phase du signal \( y(t) \) [ui même déjà complexe]

# Question 7

Suite à une transmission, on enregistre le spectre reçu autour en bande de base à deux instants différents.

![Graph](https://via.placeholder.com/600x400)

Le fait que le spectre ait changé est en évidence :

- a. le fait que les coefficients du canal sont complexes
- b. l'espacement entre les canaux
- c. le canal a introduit un retard sur les sous-canaux
- d. l'effet Doppler ⊙
- e. le fait que les temps de cohérence sont pas infinis

**Réponse correcte :**
l'effet Doppler


# Question 14

Soit un émetteur OFDM.
Le temps symbole vaut 1 ms; le nombre de sous-porteuses utilisées vaut 100; la taille de l'IFFT vaut 128, et le préfixe cyclique compte 5 échantillons.

Quelle est la bande occupée ? Réponse en kHz (arrondir au kHz le plus proche)

**Réponse :** 105

**Réponse correcte :** 104,9

# Question 15

Soit un canal dont l'étalement maximum est de 300 ns. On dispose de 10 MHz de bande.

Quelle valeur vous paraît être la plus pertinente pour le temps utile \( T_u \) ?
- 30 µs ⊙

Avec cette valeur, combien de sous-canaux actifs (N) recommandez-vous pour occuper la totalité de la bande ? (vous pouvez négliger la durée du préfixe cyclique)
- 300 ⊙

Quelle valeur d'IFFT vous paraît pertinente ?
- 512 ⊙

Quelle sera la fréquence d'échantillonnage (fe) en sortie de l'émetteur ? (en MHz, 3 chiffres après la virgule si nécessaire)
- 17,067 ⊙

# Question 9

Soit un système OFDM avec \( T_e = 100 \) ns (temps d'échantillonnage à la sortie de l'émetteur OFDM).
Soit un canal avec trois chemins principaux dont les délais d'arrivée réels (par rapport à l'instant d'émission) sont de 0, 363 ns et 447 ns, respectivement.
Sous Simulink, on utilise un bloc "SISO Fading Channel" pour simuler ce canal; on rappelle qu'il s'agit d'un modèle à temps discret. On met dans le paramètre "Discrete path delays" du bloc le vecteur suivant : [0 X Y].

Quel nombre mettre dans Y ? (en ns)
- 4 ⊙

Simulink utilise un filtre numérique pour simuler ce canal. Si l'on note \( h \) sa réponse impulsionnelle, quelle est la taille (nombre d'échantillons) de \( h \) ?
On n'attend pas ici le nombre d'échantillons non nuls, mais la taille du vecteur \( h \) (qui est différent du vecteur "Discrete path delays").
Autrement dit, si \( h = [h_0 h_1 \ldots h_{n-1}] \) où \( h_{n-1} \) est non nul (les précédents peuvent être nuls)
alors \( n \) est la taille attendue.
- 5 ⊙

# Question 10

En OFDM, l'égalisation consiste à diviser le signal bande de base reçu \( y[k] \), par la réponse impulsionnelle du canal estimée \( h[k] \).

- a. Vrai
- b. Faux ⊙

**Réponse correcte :**
Faux

# Question 11

Après égalisation, on obtient la constellation suivante :

![Constellation](https://via.placeholder.com/600x400)

Que peut-on dire de cette constellation ?

- a. Le point à droite sur l'axe des réels sera éliminé avant demapping ⊙
- b. L'égalisation fonctionne mal
- c. L'égalisation fonctionne plutôt bien ⊙
- d. Le point à droite sur l'axe des réels a été mal égalisé
- e. Le point à droite sur l'axe des réels est un pilote ⊙

# Question 12

Soit un canal dont l'étalement est de 400 ns maximum. Au niveau de l'émetteur, le temps d'échantillonnage est fixé et vaut 22,5 ns. Le préfixe cyclique...

- a. doit avoir une taille d'au moins 19 échantillons (h[0] à h[18])
- b. sera éliminé dès réception du signal bande de base y[k] ⊙
- c. est ajouté dans le domaine fréquentiel, au début du vecteur X
- d. doit avoir une taille d'au moins 18 échantillons (h[0] à h[17]) ⊙
- e. servira à absorber l'ISI ⊙
- f. est ajouté dans le domaine temporel, au début du vecteur x ⊙

**Réponses correctes :**
- est ajouté dans le domaine temporel, au début du vecteur x
- doit avoir une taille d'au moins 19 échantillons (h[0] à h[18])
- servira à absorber l'ISI
- sera éliminé dès réception du signal bande de base y[k]

# Question 13

Soit un système OFDM dont le temps symbole OFDM vaut 10 µs.
La taille de l'IFFT est 64, et le nombre de sous-porteuses actives (transportant des bits ou utilisées comme pilotes) est 50. Le préfixe cyclique vaut 8.

Quelle est la fréquence d'échantillonnage de x[k] ? Réponse en MHz.
- 7,2 ⊙

Jusqu'à quel étalement maximum du canal \( \Delta \tau_{max} \) ce système pourra-t-il fonctionner ? Réponse en ns.
- 1111 ⊙


## Question 17

En OFDM, on utilise les paramètres suivants :

- **N** = 72  
- **N_IFFT** = 128  
- **v** = 12 (nombre d'échantillons du préfixe cyclique)  

On insère périodiquement un symbole d'entraînement tel que celui décrit par *Schmidl and Cox* dans des trames contenant 10 symboles OFDM (dont 1 d'entraînement).

À la réception, le calcul de la métrique permet d'obtenir périodiquement des plateaux.  
**Quelle est cette période, en nombre d'échantillons ?**  
*(On parle bien de la période d'apparition du motif "plateau", et pas du tout de la longueur du plateau !)*

**Réponse** : 1400

---

## Question 18

La métrique de **Minn** présente, elle, un **maximum**.  
Si on a ce maximum en un index temporel donné, cela signifie...

**Choix :**

a. que le prochain échantillon est celui de la seconde moitié du symbole d'entraînement  
b. que le prochain échantillon est celui du préfixe cyclique du symbole d'entraînement  
c. que les **N_IFFT** derniers échantillons arrivés sont ceux du symbole d'entraînement (ceux qui viennent après le préfixe cyclique)  
d. que le prochain échantillon est celui du préfixe cyclique du symbole qui suit le symbole d'entraînement  

**Réponses correctes** :  
- que les **N_IFFT** derniers échantillons arrivés sont ceux du symbole d'entraînement (ceux qui viennent après le préfixe cyclique)  
- que le prochain échantillon est celui du préfixe cyclique du symbole qui suit le symbole d'entraînement

---

## Question 19

Si le récepteur OFDM présente un **offset fréquentiel** par rapport à l'émetteur, alors la corrélation calculée par la métrique de *Schmidl and Cox*...

**Choix :**

a. est toujours une somme de termes présentant tous le même déphasage  
b. doit être modifiée d'une façon que nous n'avons pas encore étudiée  
c. continue à fonctionner de la même façon (à présenter un plateau au niveau du symbole d'entraînement)  

**Réponse correcte** :  
- continue à fonctionner de la même façon (à présenter un plateau au niveau du symbole d'entraînement)

---

## Question 20

On considère une transmission à **868 MHz**.

- Côté émetteur, la précision de l'oscillateur est de **1 ppm**.  
  **Quel est l'écart maximal par rapport à 868 MHz ?** (réponse en Hz) : **868**

- Côté récepteur, elle est de **10 ppm**.  
  **Quel est l'écart maximal entre les deux oscillateurs ?** (réponse en Hz) : **9548**

---

## Question 21

**Compléter la partie synchronisation du récepteur**, telle que vue en TP.

---

## Question 16

À l'entrée du schéma ci-dessous, on trouve les échantillons de la trame OFDM.  
Relier chaque lettre à la métrique calculée :

- **Point D** : détection du maximum de la métrique de Minn *(retard d’un échantillon)*  
- **Point C** : métrique de Minn (**M1**)  
- **Point B** : métrique **Rf**  
- **Point A** : métrique **Mf**

**Réponse correcte** :

- Point D : détection du maximum de la métrique de Minn *(retard d’un échantillon)*  
- Point C : métrique de Minn (**M1**)  
- Point B : métrique **Rf**  
- Point A : métrique **Mf**
