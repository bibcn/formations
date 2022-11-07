---
title: Arduino
tags: arduino, formation


slideOptions:
  #theme: white	
  transition: 'fade'
  progress: true
  hideAddressBar: true
  spotlight:
    enabled: false
  slideNumber: 'c/t'
  touch: true
  viewDistance: 3
  display: 'block'
  autoPlay: true

---

<style>
    .reveal {
        font-size: 22px;
    }
    .alert-warning {
        color: #ffffff;
        background-color: #000000;
        border-color: #faebcc;
}
    .alert-info {
        background-color: black;
        opacity : 50%;
    }
    .reveal blockquote {
        margin: var(--r-block-margin) 0px; margin-top: 200px;
        font-style: normal;
    }
</style>

<!-- .slide: data-background="https://i.imgur.com/ju5xPsO.jpg" data-background-color="#191919" -->

<div style="text-align: left">

# Conquérir le monde avec Arduino





#### Bibliothèque des sciences du Campus MIL

</br>
</br>
</br>
</br>
Lien direct vers la présentation : hackmd.io/@creanum/arduino

</br>
</br>
</br>
</br>

###### CC-BY 4.0 



    
![Logo des bibliothèques](https://i.imgur.com/e4SQ78e.png =200x)

</div>

---

<div style="text-align: left">

## Plan 

<!-- .slide: data-background="https://i.imgur.com/iF1db2L.jpg" data-background-color="#191919" -->


<span>1. Présentation Arduino<!-- .element: class="fragment" data-fragment-index="1" --></span>
<span>2. Découverte du logiciel<!-- .element: class="fragment" data-fragment-index="2" --></span>
<span>3. Les circuits<!-- .element: class="fragment" data-fragment-index="3" --></span>
<span>4. Exercice<!-- .element: class="fragment" data-fragment-index="4" --></span>

</div>
    
Note:
Avez-vous de expérience avec Arduino?
Avez-vous de l'expérience en code?


---

<div style="text-align: left">



<!-- .slide: data-background="https://i.imgur.com/GY0n8is.jpg" data-background-color="#191919" -->
    
## 1 - C'est quoi un Arduino?

- Marque déposée!
- Carte électronique matériellement libre
- Logiciel (Arduino IDE)
- Communauté de pratique




> Une carte Arduino est un cerveau qui permet de rendre intelligent 
    des systèmes électroniques et d'animer des dispositifs mécaniques. [Source](https://www.positron-libre.com/electronique/arduino/arduino.php)


</div>


---

### Le coeur de la carte : le microcontrôleur*

![image du microcontrôleur](https://i.imgur.com/pOqcCxJ.png =400x)
**ATmega328**


*plus petit en vrai

---

<img align="right" height="350" style="float: right" src="https://i.imgur.com/lkeGZy8.jpg">


<div style="text-align: left">
    
### Ça fait quoi?

* ### Mesure et détection
    Capteur de gaz, présence, distance
    
* ### Contrôle
    Drone, robot
    
* ### Automatisation
    Arrosage de plante, alarme

</div>

---

![Dessin explicatif sur l'entrée, le traitement et la sortie avec un Arduino](https://i.imgur.com/ytlr7Gi.png)

Capteurs / Microcontrôleur / Actionneurs

---

### Exemple de schéma

![Un exemple d'un branchement d'un Arduino, d'une DEL et d'une photorésistance](https://i.imgur.com/qPEsZvz.png)

[Anatomie d'un microcontrôleur Arduino
](https://creanum.notion.site/Arduino-Anatomie-515db21609d74d29ac1509c20d4e5751)

---

### Et le Raspberry Pi?

![Un exemple d'un branchement d'un Arduino, d'une DEL et d'une photorésistance](https://i.imgur.com/oZBlsC5.jpg)
###### [Source](https://www.raspberrypi.org/)

---

### Arduino VS Raspberry Pi

| Arduino Uno                         | Raspberry Pi                      |
| ------------------------------- | --------------------------------- |
| Équipé d'un **microcontrôleur** | Équipé d'un **microprocesseur**   |
| Pas d'OS                        | Linux (Raspberry Pi OS)           |
| Matériel libre                  | Propriétaire (matériel), OS libre |
| Pas de sortie vidéo/audio*      | Deux HDMI 4K et sortie son        |
| Pas de Wifi/Bluetooth*          | Équipé du Wifi/Bluetooth          |


*sauf si équipé d'une carte d'interface (*Shield*)

---

<img align="right" height="300" style="float: right" src="https://i.imgur.com/h0rj8nD.jpg">

</br>
</br>
</br>

<div style="text-align: left">

### Alternatives à Arduino Uno

Arduino Nano 
NodeMCU (ESP8266)
ESP32
Microbit
...

</div>

---

![](https://i.imgur.com/x48xpqR.jpg)
##### Photo : NASA

:::warning
**ESP8266 : 78 fois plus puissant que l'ordinateur de bord du module d'alunissage du programme Apollo.**
##### [Source](https://labs.sogeti.com/homage-hardware-engineers/)
:::

---

<!-- .slide: data-background="https://i.imgur.com/3fnVOs2.jpg" data-background-color="#191919" -->

### Notre projet
Faire réagir une lumière DEL en fonction de la luminosité de la pièce.

---

## 2 - Arduino IDE

1. Connecter le microcontrôleur
2. Lancer Arduino IDE

:::warning
Télécharger [Arduino IDE](https://www.arduino.cc/en/software) et le [pilote CH340](http://www.wch-ic.com/downloads/CH341SER_ZIP.html) (selon votre OS)
:::


---

### Sélectionner le bon port

![Capture d'écran de l'interface d'Arduino IDE. Sélectionner Select Brand > COM x (x est le numéro du port USB)](https://i.imgur.com/KuCl0wn.png =500x)

---

### Sélectionner le bon modèle

![Capture d'écran de l'interface d'Arduino IDE. Sélectionner Boards Arduino Uno et Port COM x](https://i.imgur.com/FeqpOXG.png =600x)

---

### Ouvrir un exemple

**File > Examples > 01.Basics > Blink**


```arduino [1-12|2-4|7-12]
// configuration initiale
void setup() {
  pinMode(13, OUTPUT); // Initialise la pin digital numéro 13 en Output
}

// Instructions exécutées en boucle
void loop() {
  digitalWrite(13, HIGH);  // Allume la DEL (HIGH est la valeur du voltage)
  delay(1000);             // Attendre une seconde
  digitalWrite(13, LOW);   // Éteindre la DEL en mettant la valeur du voltage LOW
  delay(1000);             // Attendre une seconde
}
```

Référence du langage : https://www.arduino.cc/reference/fr/

Note:
Language inspiré du C++

---


<svg width="120pt" height="120pt" version="1.1" viewBox="0 0 1200 1200" xmlns="http://www.w3.org/2000/svg">
 <g fill="#45dee0">
  <path d="m600 174c-235.2 0-426 190.8-426 426s190.8 426 426 426 426-190.8 426-426-190.8-426-426-426zm0 780c-195.6 0-354-158.4-354-354s158.4-354 354-354 354 158.4 354 354-158.4 354-354 354z"/>
  <path d="m754.8 454.8-223.2 223.2-86.398-86.398c-14.398-14.398-37.199-14.398-50.398 0-14.398 14.398-14.398 37.199 0 50.398l111.6 111.6c7.1992 7.1992 16.801 10.801 25.199 10.801 8.3984 0 18-3.6016 25.199-10.801l248.4-248.4c14.398-14.398 14.398-37.199 0-50.398-14.398-14.398-36-14.398-50.398 0z"/>
 </g>
</svg>

Vérifier le code

<svg width="100pt" height="100pt" version="1.1" viewBox="0 0 1200 1200" xmlns="http://www.w3.org/2000/svg">
 <path d="m599.52 1109.1c280.99 0 509.59-228.61 509.59-509.59s-228.61-509.59-509.59-509.59-509.59 228.6-509.59 509.59c0 280.99 228.6 509.59 509.59 509.59zm0-953.2c244.61 0 443.6 199.01 443.6 443.6s-199 443.6-443.6 443.6-443.6-199-443.6-443.6c0-244.59 199-443.6 443.6-443.6zm-247.46 506.91h334.88s-81.18 81.191-131.46 131.45c-21.469 21.48-21.469 56.301 0 77.781 3.543 3.543 7.125 7.1172 10.668 10.656 21.469 21.48 56.289 21.48 77.77 0 65.812-65.805 196.42-196.42 241.96-241.96 10.316-10.305 16.113-24.297 16.113-38.879v-4.707c0-14.574-5.7969-28.562-16.113-38.879-45.535-45.535-176.14-176.15-241.96-241.96-21.48-21.48-56.305-21.48-77.77 0-3.543 3.5312-7.125 7.1289-10.668 10.656-21.469 21.48-21.469 56.293 0 77.77 50.285 50.273 131.46 131.46 131.46 131.46h-334.88c-30.379 0-54.992 24.625-54.992 54.992v16.617c0 30.379 24.613 54.992 54.992 54.992z" fill="#45dee0" fill-rule="evenodd"/>
</svg> 

Vérifier et téléverser le code

:::warning
:warning: **Problème?**
Changer le port ou la prise USB.
:::



Note: 
    ![image représentant les messages lors de l'exécution du code et son transfert](https://i.imgur.com/XdqlI03.png)


---

### Variable

```arduino [1-14|1|5|10|12|1-14]
int maLumiere = 13;       // J'ai donné un nom au numéro 13

// configuration initiale
void setup() {
  pinMode(maLumiere, OUTPUT); // Initialise la pin digital numéro 13 en Output
}

// Instructions exécutées en boucle
void loop() {
  digitalWrite(maLumiere, HIGH);  // Allume la DEL (HIGH est la valeur du voltage)
  delay(1000);                       // Attendre une seconde
  digitalWrite(maLumiere, LOW);   // Éteindre la DEL en mettant la valeur du voltage LOW
  delay(1000);                       // Attendre une seconde
}
```

---

## 3 - Premier circuit
#### Faire allumer une DEL

- DEL de la couleur de votre choix
- Une résistance de 200 Ω
- Platine d'essai (*Breadboard*)
- Câbles dupont

![Schéma du premier circuit avec un Arduino et une lumière DEL](https://i.imgur.com/XL3VzUd.png =700x)

---

![](https://i.imgur.com/tebhaDE.png =300x)

---

### Deuxième circuit
#### Photorésistance

- Photorésistance
- Résistance 10k Ω

![Schéma du deuxième circuit avec un Arduino, une lumière DEL et une photorésistance](https://i.imgur.com/qPEsZvz.png)

---


```arduino [1|1-2|1-3|7|7-8|7-9|14|15-16]
int maLumiere = 7; // J'ai donné un nom à la pin 7
int photoresistance = A1; // ma photorésistance est branchée dans A1
int valeur = 0; // initialise la variable valeur à 0

// configuration initiale
void setup() {
  Serial.begin(9600); // ouvre le port série
  pinMode(maLumiere, OUTPUT); // Initialise la pin digital numéro 7 en Output
  pinMode(photoresistance, INPUT); // initialise la lecture de la pin A1
}

// Instructions exécutées en boucle
void loop() {
  valeur = analogRead(photoresistance); // lecture de ma valeur et stockage dans la variable valeur. 
  Serial.println("La valeur est de "); // s'affiche dans le moniteur
  Serial.println(valeur);  // ma valeur
  delay(250); // délai de 1/4 de seconde

  digitalWrite(maLumiere, HIGH);  // Allume la DEL (HIGH est la valeur du voltage)
  delay(1000);                       // Attendre une seconde
  digitalWrite(maLumiere, LOW);   // Éteindre la DEL en mettant la valeur du voltage LOW
  delay(1000);                       // Attendre une seconde
}
```

---

### Valeur normale
![](https://i.imgur.com/eD94UNA.png =800x)


### Valeur en cachant la photorésistance 
![](https://i.imgur.com/NcGTAgs.png =800x)

---

### Créer une condition 

```arduino [1-99|19|19-21|22-24|1-99]
int maLumiere = 7; // J'ai donné un nom à la pin 7
int photoresistance = A1; // ma photorésistance est branchée dans A1
int valeur = 0; // initialise la variable valeur à 0

// configuration initiale
void setup() {
  Serial.begin(9600); // ouvre le port série
  pinMode(maLumiere, OUTPUT); // Initialise la pin digital numéro 7 en Output
  pinMode(photoresistance, INPUT); // initialise la lecture de la pin A1
}

// Instructions exécutées en boucle
void loop() {
  valeur = analogRead(photoresistance); // lecture de ma valeur et stockage dans la variable valeur. 
  Serial.println("La valeur est de "); // s'affiche dans le moniteur
  Serial.println(valeur);  // ma valeur
  delay(250); // délai de 1/4 de seconde

  if (valeur<500) { 
    digitalWrite(maLumiere, HIGH); // Allume la DEL (HIGH est la valeur du voltage)
  }
  else {
    digitalWrite(maLumiere, LOW); // Éteint la DEL
  }

}
```

---

![](https://i.imgur.com/segVjXx.jpg =300x)

---


### Code final (sans les commentaires) 

```arduino
int maLumiere = 7; 
int photoresistance = A1; 
int valeur = 0; 

void setup() {
  Serial.begin(9600); 
  pinMode(maLumiere, OUTPUT); 
  pinMode(photoresistance, INPUT); 
}

void loop() {
  valeur = analogRead(photoresistance); 
  Serial.println("La valeur est de "); 
  Serial.println(valeur);  
  delay(250); 

  if (valeur<500) { 
    digitalWrite(maLumiere, HIGH); 
  }
  else {
    digitalWrite(maLumiere, LOW);
  }

}
```

---

## 4 - Exercice

- Inclure une deuxième DEL
- Faire une condition : 
si valeur <500 = allume DEL 1
Sinon, allume DEL 2

---

[CREANUM.NOTION.SITE](https://CREANUM.NOTION.SITE)
Documentations et projets



<img align="left" height="500" style="float: left" src="https://i.imgur.com/FJdfWT1.png">



<br/>
<br/>
<br/>

    
#### Prochaine formation en création numérique
* Impression 3D
* Découpe numérique
* Montage vidéo
* Baladodiffusion
* ...

[S'inscrire!](https://bib.umontreal.ca/formations/calendrier?cid=7690&t=g&cal=7690&d=0000-00-00&ct=34766&inc=0)

<br/>
<br/>
<br/>

Questions? Commentaires?
creanum@bib.umontreal.ca

---

<img align="right" height="70" style="float: right" src="https://media.giphy.com/media/CT5Ye7uVJLFtu/giphy.gif">

**Formulaire de rétroaction anonyme**
Temps de remplissage ≈ 1 minute
<iframe width="640px" height="480px" src="https://forms.office.com/r/JMT79tpiAW?embed=true" frameborder="0" marginwidth="0" marginheight="0" style="border: none; max-width:100%; max-height:100vh"> </iframe>

