---
title: Jeff et des Maths
date: '2023-11-23'
summary: On commence l'aventure Jeff de Saint-Etienne !
---


PROBABILITES - [1. Ensembles](#Ensembles)<br>
PROBABILITES - 1. Ensembles TD corrigé<br>
PROBABILITES - 2. Dénombrements<br>
PROBABILITES - 2. Dénombrements TD corrigé<br>
PROBABILITES - 3. Probabilités 1<br>
PROBABILITES - 3. Probabilités simples - TD corrigé<br>
PROBABILITES - 4. Conditionnelles<br>
PROBABILITES - 4. Conditionnelles TD corrigé<br>
PROBABILITES - 5. Var et loi de probabilité<br>
PROBABILITES - 5. Variable aléatoire et loi de probabilité TD<br>
Lois de probabilités - 1. Hypergéométrique<br>
Lois de probabilités - 1. hypergéométrique TD<br>
Lois de probabilités - 2. Binomiale<br>
Lois de probabilités - 2. binomiale TD<br>
Lois de probabilités - 3. Poisson<br>
Lois de probabilités - 3. Poisson TD<br>
Lois de probabilités - 4. Loi normale 1<br>
Lois de probabilités - 4. Loi normale 1 TD<br>
Lois de probabilités - 5. Loi normale 2<br>
Lois de probabilités - 5. Loi normale2 TD<br>
Lois de probabilités - 6. Echantillonnage<br>
Lois de probabilités - 6. Echantillonnage TD<br>
Lois de probabilités - 7. Estimation<br>
Lois de probabilités - 7. Estimation TD<br>
Lois de probabilités - 8. Test d'adéquation du Khi2<br>
Lois de probabilités - 8. Test d'adéquation du Khi2 TD

# PROBABILITÉS #
<ol>
    <li>Ensembles</li>
    <li>Dénombrements</li>
    <li>Probabilités simples</li>
    <li>Probabilités conditionnelles</li>
    <li>Variable aléatoire et loi de probabilité</li>
    <li>Lois de probabilités
      <ol>
        <li>Loi hypergéométrique</li>
        <li>Loi binomiale</li>
        <li>Loi de Poisson</li>
        <li>Loi normale 1</li>
        <li>Loi normale 2</li>
        <li>Échantillonnage</li>
        <li>Estimation</li>
        <li>Test d'adéquation du Khi2</li>
      </ol>
    </li>
</ol>

## Ensembles ## 

On a affaire à des <span style="color:blue">**évènements aléatoires**</span> et dont il faut savoir faire quelques <span style="color:blue">**prévisions**</span>. On va analyser des cas simples avec les objets de base suivants : pièces de monnaies (pile ou face), dés (6 faces), jeux de cartes (pique, cœur, carreau, trèfle)...<br>
*Notes : Le mot hasard provient de l'arabe médieval "az-zahr" qui signifie le dé. Le mot aléa provient du latin "alea" (comme dans la fameuse expression de Jules César franchissant le Rubicon "alea jacta est") qui signifie le dé.*

<mark>**PROBABILITÉS : intuitives**</mark>

De prime abord, les probabilités peuvent apparaître <span style="color:blue">**intuitives**</span>. On va considérer une expérience aléatoire pour laquelle plusieurs <span style="color:blue">**issues**</span> sont possibles. On va se demander quelle est la probabilité de chacune des issues.

| <span style="color:blue">**Expérience**</span> | <span style="color:green">**Évènement**</span> | <span style="color:green">**Probabilité**</span> |
| :--------------- |:---------------:| -----:|
| <span style="color:blue">lancer une pièce</span> | <span style="color:green">obtenir Face</span> |  <span style="color:green">1/2</span> |

Quelle est la probabilité d'<span style="color:green">obtenir Face</span> lorsque l'on lance une pièce de monnaie ?<br>
<u>Réponse :</u> une chance sur deux (50% ou 0,5). *NB : Dans le cas où la pièce est bien équilibrée.*<br>

Qu'est-ce que cela signifie ? À quoi cela nous sert-il ?<br>
Est-ce que cela va nous aider à deviner le résultat du prochain lancer ?<br><br>
Bien sûr que non. La probabilité n'est pas là pour ça. Elle ne peut pas nous dire ce qui va se passer la prochaine fois que l'on lancera une pièce. Lorsqu'on abordera le concept de loi de probabilité, on verra à quoi servent vraiment les probabilités. Savoir que quelque chose a une chance sur deux d'arriver, ça n'est absolument pas utile si on veut essayer l'expérience <u>une fois</u>. Que ce soit une probabilité d'une chance sur deux, une chance sur trois ou neuf cent quatre-vingt-dix-neuf chances sur mille, cela n'<span style="color:red">**assurera pas**</span> du</span> <span style="color:red">**résultat futur**</span>.<br>

Continuous dans nos exemples, et demandons-nous si systématiquement les probabilités peuvent être trouvées par intuition, avec simplement un peu de bon sens.

| <span style="color:blue">**Expérience**</span> | <span style="color:green">**Évènement**</span> | <span style="color:green">**Probabilité**</span> |
| :--------------- |:---------------:| -----:|
| *Aligné à gauche*  | *centré*          |    *Aligné à droite* |
| <span style="color:blue">lancer une pièce</span> | <span style="color:green">obtenir Face</span> |  <span style="color:green">1/2</span> |
| <span style="color:blue">lancer un dé</span> | <span style="color:green">obtenir le 1</span> |  <span style="color:green">1/6</span> |
|  | <span style="color:green">c'est pair</span> |  <span style="color:green">3/6 = 1/2</span> |

Une probabilité va pouvoir se noter comme une fraction. Bien entendu, le nombre de chances que l'on a est toujours inférieur au nombre de cas possibles. Donc on peut décrire dans la plupart des cas une probabilité comme étant le nombre de cas favorables (au *numérateur*) à l'évènement qui nous intéresse, divisé par le nombre total de cas (au *dénominateur*) que l'expérience pouvait nous faire obtenir. À l'arrivée, j'ai un résultat qui, si j'effectue la division, est un nombre compris entre 0 et 1. Une probabilité est définie mathématiquement (strictement) par un résultat compris entre 0 et 1.

<mark>**PROBABILITÉS : intuitives ... ?**</mark>

| <span style="color:blue">**Expérience**</span> | <span style="color:green">**Évènement**</span> | <span style="color:green">**Probabilité**</span> |
| :--------------- |:---------------:| -----:|
| <span style="color:blue">lancer deux pièces</span> | <span style="color:green">obtenir deux Face</span> |  <span style="color:green">1/4</span> |
| <span style="color:blue">lancer deux dés</span> | <span style="color:green">on a un double</span> |  <span style="color:green">1/6</span> |
| <span style="color:blue">tirer 5 cartes d'un jeu de 32</span> | <span style="color:green">avoir un brelan</span> |  <span style="color:green">12096/201376<br> = 54/899 ≃ 0,06</span> |

<u>Expérience :</u> <span style="color:blue">lancer deux pièces</span>. <u>Événement :</u> <span style="color:green">obtenir deux Face</span>.<br>
Lorsque je lance deux pièces de monnaie, je peux me poser la question de la probabilité d'obtenir deux Face. Et là, deux raisonnements peuvent s'opposer. Si je lance deux pièces de monnaie, qu'est-ce que je peux avoir à l'arrivée en face des yeux ? [2 Pile] ou [2 Face] ou [1 Pile et 1 Face]. Donc je pourrais me dire naïvement : j'ai une chance sur trois d'obtenir deux Face, ce qui est absolument faux !<br>
Puisque chaque pièce propose un résultat, et que une pièce va atterir à gauche et l'autre à droite (par exemple - ce sont deux objets physiques différents). Et du coup, il y a quatre **évènements** qui sont **équiprobables** : obtenir [Pile-Pile] ou [Pile-Face] ou [Face-Pile] ou [Face-Face]. Chacun de ces évènements a une chance sur quatre d'advenir, et donc la probabilité d'avoir [2 Face] est 1/4.

<u>Expérience :</u> <span style="color:blue">lancer deux dés</span>. <u>Événement :</u> <span style="color:green">obtenir un double</span>.<br>
Là, il faut déjà un peu plus de réflexion pour se dire : alors, combien d'évènements sont possibles à l'arrivée lorsque je vais lancer deux dés. Si l'on reprend l'exemple des pièces de monnaie et que l'on transpose ça aux dés, je peux avoir devant les yeux :<br>
**[1-1]**, [1-2], [1-3], [1-4], [1-5], [1-6];<br>
[2-1], **[2-2]**, [2-3], [2-4], [2-5], [2-6];<br>
[3-1], [3-2], **[3-3]**, [3-4], [3-5], [3-6];<br>
[4-1], [4-2], [4-3], **[4-4]**, [4-5], [4-6];<br>
[5-1], [5-2], [5-3], [5-4], **[5-5]**, [5-6];<br>
[6-1], [6-2], [6-3], [6-4], [6-5], **[6-6]**.<br>
On a en fait six possibilités pour le 1er dé, six possibilités pour le 2ème, etc. Au total : 36 couples à l'arrivée. Parmi ces 36 couples, combien sont des doubles ? 6 chances sur 36 soit 1/6.

<u>Expérience :</u> <span style="color:blue">tirer 5 cartes d'un jeu de 32</span>. <u>Événement :</u> <span style="color:green">avoir un brelan</span>.<br>
Là, les choses sont bien plus compliquées. Avoir un brelan, ce n'est pas aussi simple qu'avoir un double en lançant deux dés. Un brelan c'est trois cartes identiques plus deux autres cartes qui ne sont pas de même valeur que les trois premières (oar contre qui peuvent être de n'importe quelle couleur)... Bref, déjà l'évènement en lui-même est relativement complexe puisqu'il faudrait savoir comptabiliser le nombre de situations qui conduisent à un brelan (*numérateur*), et puis d'un autre côté il faudrait savoir comptabiliser aussi le nombre de situations au total que l'on a en tirant 5 cartes à partir d'un jeu de 32. Pour savoir que l'on a à l'arrive 12096 chances sur 201376 (≃ 06% de chances), on s'aperçoit que notre <span style="color:red">**intuition n'est plus utilisable**</span>.<br>

On ne peut pas se fier à son bon sens si on veut faire des calculs de probabilités dans des situations à peu près quelconques. Et franchement et honnêtement, tirer 5 cartes d'un jeu de 32 ça n'est pas une situation très compliquée. Pourtant même avec un jeu aussi simple que ça, on s'aperçoit que non il va nous falloir des bases, il va nous falloir des outils de calcul, il va falloir se demander si il peut exister plusieurs formules qui conduiront à plusieurs résultats différents selon les cas de figure envisagés... Bref, il va falloir qu'on <span style="color:blue">**s'organise**</span>.<br>

Alors, devant la multitude de possibilités (par exemple dans un jeu de cartes, on peut avoir des valets des dames des rois des dix des neufs des huits, mais aussi des piques des trèfles des cœurs des carreaux etc.), avec des objets qui possèdent plusieurs caractéristiques différentes, il faut savoir faire une <span style="color:blue">**classification**</span> de ces objets. Si on veut calculer des probabilités sur des évènements donnés, il faut être capable de <span style="color:blue">**dénombrer**</span> des situations qui nous intéressent parmi tout un ensemble de situations possibles. Donc il faut les compter, ces situations. Et pour les compter il faut savoir bien les classifier, c'est-à-dire les ranger dans des <span style="color:blue">**ensembles**</span> et des sous-ensembles.<br>

**Ensembles >>> Dénombrements >>> Probabilités**

1) Rappel sur les <span style="color:blue">**ensembles**</span> afin que l'on acquiert une certaine <u>logique de pensée</u> et également une certaine <u>notation</u>, un <u>langage</u> associé à ça, qui nous permettent d'être sûrs de ce que l'on dit et de faire une "économie" de place et de volume dans ce qu'on va écrire et dans ce que l'on va dire. Le langage des ensembles est très pratique pour ça.<br>
2) Une fois que l'on maîtrisera ce langage, on ira voir du côté des <span style="color:blue">**dénombrements**</span> : comment est-ce que l'on peut comptabiliser des situations.<br>
3) Une fois que l'on sera à peu près faire tout ça, on pourra commencer à calculer des <span style="color:blue">**probabilités**</span> d'évènements.

Cela peut parâitre assez furstrant, mais l'exemple du brelan dans notre jeu de cartes est suffisament significatif pour nous faire dire : il faut avoir des bases et prendre des précautions. L'objectif de cette vidéo, c'est de parler des **rappels sur les ensembles**. Déjà d'avoir le bon langage, la bonne formulation pour tout ce qui va pouvoir nous intéresser.<br>


<mark>**PROBABILITÉS**</mark>
1. **Dénombrements**<br>
    1.1. **Rappels sur les ensembles**<br>
    
La toute première chose que l'on voit, dès l'école primaire, c'est ce qu'on appelle un <span style="color:blue">**diagramme de Venn**</span>. Un ensemble est considéré comme un **sac** dans lequel on peut mettre des **objets**, que l'on va appeler des **éléments**. Exemple : ensemble des évènement a,b,c,d,e,f. Les éléments ne sont pas dans un ordre particulier. Tout ce qui est intéressant dans un ensemble, c'est de savoir <u>ce qu'il y a à l'intérieur</u>. L'ensemble lui-même on lui donnera un nom, et on le désignera systématiquement par un lettre majuscule. Si possible, on désignera par des minuscules les éléments qui sont à l'intérieur (attention : ces éléments peuvent être des arbres ou des chiffres, on a pas forcément affaire à des lettres de l'alphabet).<br>

Si on veut éviter de dessiner l'ensemble, on pourra le citer entre accolades.<br>
Exemple avec les **éléments** a,b,c,d,e,f de l'<span style="color:blue">**ensemble**</span> A (penser à un ensemble comme à un "sac").<br>
$$A = \{a;b;c;d;e;f\}$$

Équivaut à :<br>
$$A = \{d;e;f;a;b;c\}$$

Il s'agit du même ensemble. L'ordre n'a pas d'importance.

Notion d'<span style="color:blue">**élément**</span>.<br>
On utilisera le symbole $\in$ "***appartient à***" ou "***est élément de***".<br>
$b \in A$<br>
$h \not\in A$<br>

Notion de <span style="color:blue">**sous-ensemble**</span> d'un ensemble (ou de **partie**).<br>
Il s'agit d'un ensemble qui se trouve à l'intérieur d'un autre ensemble. Il s'agit d'un sac dans un autre sac.<br>
$\{a;b;c\} \subset A$<br>

Je peux citer maintenant un ensemble B, dont les éléments sont des ensembles.<br>
$B = \{\{a;b\};\{a;c\};\{b;d;f\}\}$<br>
$\{a;b\} \in B$<br>
$\{a;b;c\} \not\in B$<br>
$a \not\in B$<br>


```python
import cv2

video = cv2.VideoCapture("PROBABILITES - 1. Ensembles.mp4")

nr_frames = video.get(cv2.CAP_PROP_FRAME_COUNT)
fps = video.get(cv2.CAP_PROP_FPS)

timestamp = input('Enter timestamp in hh:mm:ss format')
#timestamp = '00:47:03'

timestamp_list = timestamp.split(':')
hours, minutes, seconds = timestamp_list
timestamp_list_floats = [float(i) for i in timestamp_list]
hh, mm, ss = timestamp_list_floats

frame_nr = hh * 3600 * fps + mm * 60 * fps + ss * fps

video.set(1, frame_nr)
success, frame = video.read()
cv2.imwrite(f'Frame at {hours}_{minutes}_{seconds}.jpg', frame)

from PIL import Image
from IPython.display import display


img = Image.open(f'Frame at {hours}_{minutes}_{seconds}.jpg')
display(img)
```

    Enter timestamp in hh:mm:ss format00:15:37



    
![png](./PROBABILITES%20%28Jeff%20des%20Maths%29_3_1.png)
    



```python

```
