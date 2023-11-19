# Edge_impulse
## Experiment and Description
Dans le cadre de ce Projet, nous exploiterons Edge Impulse via la plateforme cloud d'Arduino en utilisant un Arduino Nano 33 BLE Sense. L'objectif sera d'implémenter un réseau neuronal artificiel simple, capable de reconnaître des mots-clés dans la parole. Pour ce faire, nous utiliserons du microphone numérique intégré au Nano 33 BLE Sense, le MP34DT05, afin d'écouter notre environnement. Et en cas de détection d'un mot-clé, la LED RVB intégrée à la carte s'allumera.
## Tools
- [ Nano BLE Sense 33](https://store.arduino.cc/products/arduino-nano-33-ble-sense)
- [micro-usb cable](https://www.google.com/search?rlz=1C5CHFA_enUS858US858&sxsrf=ALeKk01CbJTvQbYgX6arJbsjcRVmv-3-RQ:1584929968297&q=Micro+USB+cable&spell=1&sa=X&ved=2ahUKEwjl8IOexK_oAhXDqZ4KHZ0mCmcQBSgAegQIDhAn&biw=1680&bih=832)
- Arduino Cloud to train simple Artificial Neural Network.
- [arduino IDE](https://www.arduino.cc/en/software#future-version-of-the-arduino-ide)
## Install and Run
Installer sur votre ordinateur
- [Edge Impulse CLI.](https://docs.edgeimpulse.com/docs/tools/edge-impulse-cli/cli-installation) 
- [Arduino CLI.](https://arduino.github.io/arduino-cli/0.35/) .
- [Nano 33 BLE Sense board Edge Impulse firmware](arduino-nano-33-ble-sense)
### connection de la carte au compte Edge impulse
- pour connecter la carte au compte Edge impulse taper la commande:
  *     edge-impulse-daemon --clean
-   se Rassurer d'avoir un [compte Edge impulse](https://mltools.arduino.cc/login?next=%2Fstudio%2F144605) et d'avoir créer un projet au préable
## Création & conservation de données
  cette étape consiste à créer un ensemble de données représentatif des mots-clés sélectionnés que le modèle ML est censé identifier. Pendant un laps de temps de 3secondes, nous prononcons le mot-clé **rouge** ,**jaune**, et **Vert** , tout en se rapprochant du microphone intégré sur la carte. Dans notre cas nous avons enregistré 35 échantillons pour chaque mots.
  nous enregistrons également 35 autres échantillons **noise** (c'est à dire enregistré l'environnement dans un silence complet); cet exemple va aider le modèle ML à identifier quand aucun mot-clé n'est prononcé.
   ![creation des données]()

  ## Créer une impulsion
  ici l'impulsion est la façon dont le modèle ML est formé, c'est l'endroit où l'on définit les actions qui vont être effectuées sur nos données d'entrée pour les rendre mieux adaptées au ML et un bloc d'apprentissage qui définit l'algorithme pour les données. 
  ![impulsion]()
  
  ## Entraîner le modèle ML
  * une que les fonctionnalités de notre ensemble de données sont prêtes à être utilisées, on entraine maintenant notre modèle
nous pouvons observer que notre score est de 81,3% qui n'est peut être pas optimal mais suffisant pour détecter les mots clés. celà peut être du au fait que nous avons assez enregistré de données (dans notre cas 30 échantillons) ou encore du à la présence des enregistrement non représentatifs
 ![impulsion]()
## Deployement et utilisation du modèle
Le ML que nous avons formé est déjà prêt pour son utilisation avec du matériel embarqué tel que des microcontrôleurs. 
Cela lancera un processus dans lequel Edge Impulse créera une bibliothèque pour la carte Arduino contenant le modèle ML que formé.

## Modification du programme et utilisation de la LED RVB intégrée
Programme Arduino : [Allumage de la led rvb en fonction de la détection du mot clé]()
