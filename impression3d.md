---
title: Atelier impression 3D
tags: impression 3d, CreaNum
description:
---

## Atelier impression 3D

slide: hackmd.io/@creanum/impression3d

<br>
<br>
<br>

<img src="https://i.imgur.com/vjaedfV.png" alt="drawing" width="200"/>

---

<br>
<br>
<br>
<br>

###### Sauf indications contraires, les contenus de cette présentation créée par les bibliothèques UdeM sont sous licence CC-BY. 
<br>
<br>

###### Équipe CreaNum - Les bibliothèques de l'Université de Montréal

<br>

<img src="https://i.imgur.com/vjaedfV.png" alt="drawing" width="200"/>

---

# Impression 3D
Passer d'un modèle numérique à un modèle réel
![https://3d.si.edu/object/3d/statuette-mountain-lion-or-panther-man-god-key-marco-cat:9868cadc-d331-4b13-9864-a1740df6e47f](https://i.imgur.com/j6pmP6G.png =200x300) > ![](https://i.imgur.com/Y8FZeZ8.jpg =210x300)

---

## Les différents procédés : fabrication soustractive vs fabrication additive

---

### Fabrication soustractive

<div style="text-align: left"> 
Toutes opérations qui permettent de transformer un bloc de matériau solide par retrait progressif de matière : usinage avec machine CNC, découpe laser, etc. 

</div>
<img src="https://upload.wikimedia.org/wikipedia/commons/8/8f/Vikingshiprelief.jpg" alt="carving" width="400"/>
<div style="text-align: center">  
© Woodcarvings by W.F. Judt
</div>

---

### Fabrication additive
Fabrication de pièces par ajout de matière en couches successives

<div style="text-align: left">  
- FDM (Fused Deposition Modeling ou modelage par dépôt de matière en fusion)  
</div>

<img src="https://i.imgur.com/Q0VN7nt.jpg" alt="drawing" width="400"/>
    
[Source](https://www.kimya.fr/en/how-does-an-fdm-3d-printer-work/)

---

<div style="text-align: left">      
- SLA (Stéréolithographie Apparatus) photopolymérisation sur de la résine sensible à l'UV, couche par couche. 
</div>

<img src="https://i.imgur.com/H6pl1ju.jpg" alt="drawing" width="400"/>

---

{%youtube LCXjaTNx_vg %}

---

# À quoi cela peut servir ?

---

## Spatiale, aéronautique et automobile


<img src="https://i.imgur.com/mP9EmwF.jpg" alt="drawing" width="400"/>

https://www.youtube.com/watch?v=kz165f1g8-E

---

## Santé, médecine

{%youtube 3N684MaB0b8 %}

---

## Médecine régénérative (bio-impression)

<img src="https://i.imgur.com/24vRQxx.jpg" width ="600">

Voir par exemple https://www.youtube.com/watch?v=64-ujrKUxLc&t


---

## Aliments

![sugarlab3d.com](https://i.imgur.com/1SxgBgC.jpg)
https://www.youtube.com/watch?v=v5IL31B3-yg

---

## Haute couture

<img src="https://danitpeleg.com/wp-content/uploads/2017/06/download.gif" alt="3-d-ress" height="500"/>
    
[Source](https://danitpeleg.com/)


---



## Architecture 

![https://www.designingbuildings.co.uk/wiki/3D_printing_in_construction](https://i.imgur.com/Pi8bV7K.jpg)

---

## Recherche

![](https://i.imgur.com/06CahcP.png =500x500)

[Source](https://nouvelles.umontreal.ca/article/2022/04/19/audrey-laventure-la-chercheuse-qui-imprime-en-3d-des-materiaux-multifonctionnels/)

---

- Objets personnalisés 
- Pièces pour réparation
- [...](https://www.pocket-lint.com/gadgets/news/131685-best-3d-prints-the-crazy-and-coolest-things-people-have-printed)

---

## Matériaux

---

### PLA (Acide polylactique)

À base d'amidon de maïs

Facile d'utilisation, bon marché, respectueux de l'environnement

Température de fusion : 180°C-230°C
Température du lit : 50°C-70°C

---

### ABS (Acrylonitrile butadiène styrène)

À base de combustibles fossiles

Durable et robuste mais dégage de fortes émanations => pas utilisé aux bibliothèques

Température de fusion : 210°C-250°C
Température du lit : 90°C-100°C

---

### PVA (Alcool polyvinylique)

<img src="https://www.simplify3d.com/wp-content/uploads/2019/04/3d-printed-pva-filament-1024x774-1024x774.jpg" alt="pva" width="800"/>


---

# Par où commencer?

---

## 1 - Le modèle

- Modélisation ([Blender](https://www.blender.org/), [Tinkercad](https://www.tinkercad.com/), [OpenSCAD](https://openscad.org/))
- Depuis Internet (par exemple : [Thingiverse](https://www.thingiverse.com/))


---

### Le fichier STL 

STL provient de **St**éréo**l**ithographie 
Aussi nommé Standard Tesselation Language ou Standard Triangle Language

Tesselation = daller une surface avec des formes géométriques

Décrit la géométrie du modèle par sa surface externe avec des petits triangles. Les coordonnées des sommets de chaque triangle sont stockés dans le fichier.



---

## 2 - Découper le modèle

- Logiciel de découpe (Slicer)
    - Hauteur de la couche
    - Remplissage (motif et densité)
    - Support
    - Vérification

---


Exemples de support

![](https://i.imgur.com/8Xi2T8c.png)

---

<img src="https://i.imgur.com/zesj0ww.jpg" alt="drawing" width="1000"/>



---

Le slicer convertit le fichier STL en GCODE => le fichier .gcode est généré automatiquement par le logiciel

le gcode contient une série d'instructions pour l'imprimante




---

![](https://i.imgur.com/MrYeNWq.png)

[Première impression avec la Prusa](https://www.notion.so/creanum/Premi-re-impression-avec-la-Prusa-3d61002c9950411e98f8e97d1c626ac6)

---

![](https://i.imgur.com/dll65Ab.png)

[Première impression avec l'Ultimaker](https://www.notion.so/creanum/Premi-re-impression-avec-l-Ultimaker-03e3807d0757488296d6bce88824f03b)

--- 
## 3 - Impression

1. Préparer l'imprimante
2. Changer le filament
3. Lancer l'impression
4. Surveiller les premières couches

---

Merci!

---

[Wiki CréaNum](https://creanum.notion.site/)