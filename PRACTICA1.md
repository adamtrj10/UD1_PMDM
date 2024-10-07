# PRÀCTICA 1 : APP COMPTADOR

## 1. Anàlisi de l'estructura del projecte:

### 1.1 ESTRUCTURA GENERAL
- El projecte està estructurat en Empty View Activity (Gradle). 
- La seua estructura es la següent: \
![Alt text](https://i.postimg.cc/52V6mQN0/Captura-de-pantalla-2024-10-07-093621.png "img")
- Les carpetes i fitxers a destacar son: **codi font de l'aplicació:** *kotlin+java* ; **scripts de gradle:** *formats en Kotlin DSL* ; **els descriptors de l'app:** *androidmanifest.xml (defineix aspectes com el nom de l'aplicació i el paquet, la icona, i els seus diferents components)* ; **res:** 
*son els recursos (imatges/dissenys/etc).*

### 1.2 ESTRUCTURA D'ACTIVITY (*MainActivity*)
**Activitats: Representen les diferents pantalles de l'aplicació i recullen la interacció amb l'usuari**
- Estructurat de la següent manera: 
1. *MainActivity.kt* : realitza les tasques principals de l'aplicació.
2. *activity_main.XML* : interfície gràfica que amb la que interactua l'usuari. (textview, botons(btOpen,btAdd)...)
   
- Si volguerem afegir una nova activitat, seria suficient crear el fitxer de layout i el fitxer Kotlin amb la classe? \
La resposta es que no, ja que també tindriem que crear un fitxer XML (interfície gràfica) i afegir-ho a *androidManifest.XML*

## 2. Anàlisi del cicle de vida i el problema de la pèrdua d'estat
- **ANÀLISI DEL CICLE DE VIDA:**
  Pel que fa a l'activitat principal, ens trobem el cicle de vida **onCreate()**, on s'activa en la creació de l'activitat. Ací es realitza la initzaliciació bàsica (inici de components/enllaçar vistes/vincular dades).
- **IMPLEMENTACIÓ DE DIVEROS MÉTODES:** \
  ![Alt text](https://i.ibb.co/LkgDDHZ/Captura-de-pantalla-2024-10-07-105254.png "img")

## 3. Solució a la pèrdua d'estat
**Per què ix error quan fem debug?**
*Log.D* requereix de 2 arguments: El **primer**, com a *"tag"*, i el **segon**, com a *"missatge"*. \
Per tal de solucionar-ho, afegir el primer argument que falta, i ho aplicarem a tots el métodes: \
![Alt text](https://i.ibb.co/9YGvhTQ/Captura-de-pantalla-2024-10-07-110640.png "img")


## 4. Ampliant la funcionalitat amb decrements i resets

## 5. Aplicant el View Binding


