# Edge_impulse
## Experiment and Description
Dans le cadre de ce Projet, nous exploiterons Edge Impulse via la plateforme cloud d'Arduino en utilisant un Arduino Nano 33 BLE Sense. L'objectif sera d'implémenter un réseau neuronal artificiel simple, capable de reconnaître des mots-clés dans la parole. Pour ce faire, nous utiliserons du microphone numérique intégré au Nano 33 BLE Sense, le MP34DT05, afin d'écouter notre environnement. En cas de détection d'un mot-clé, la LED RVB intégrée à la carte sera alumée.
## Tools
- [ Nano BLE Sense 33](https://store.arduino.cc/products/arduino-nano-33-ble-sense)
- [micro-usb cable](https://www.google.com/search?rlz=1C5CHFA_enUS858US858&sxsrf=ALeKk01CbJTvQbYgX6arJbsjcRVmv-3-RQ:1584929968297&q=Micro+USB+cable&spell=1&sa=X&ved=2ahUKEwjl8IOexK_oAhXDqZ4KHZ0mCmcQBSgAegQIDhAn&biw=1680&bih=832)
- Arduino Cloud to train simple Artificial Neural Network.
- [arduino IDE](https://www.arduino.cc/en/software#future-version-of-the-arduino-ide)
## Install and Run
Installer sur votre ordinateur
- [Edge Impulse CLI.](https://docs.edgeimpulse.com/docs/tools/edge-impulse-cli/cli-installation) 
- [Arduino CLI.](https://arduino.github.io/arduino-cli/0.35/) .
- [Nano 33 BLE Sense board Edge Impulse firmware]()
### connection de la carte au compte Edge impulse
- pour connecter la carte au compte Edge impulse taper la commande:
  *      -edge-impulse-daemon --clean
-   se Rassurer d'avoir un [compte Edge impulse](https://mltools.arduino.cc/login?next=%2Fstudio%2F144605) et d'avoir créer un projet au préable
## Création & conservation de données
