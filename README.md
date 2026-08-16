## Il existe un projet pour CSNET Home pour utilisation sur Home Assistant 

- Je me suis appuyé sur ce projet pour créer la passerelle sur esp32 : 
https://github.com/mmornati/home-assistant-csnet-home.git  

Utilisant Jeedom sur lequel il n'y a pas de plugin, j'ai créer une passerelle avec un esp32 et qui permet d'envoyer les infos sur MQTT 

# CsnetHome-esp32
Passerelle esp32 pour se connecter sur Csnet Home et envoyer les infos sur MQTT 

## Accès à l'esp après téléchargement  
- Depuis le navigateur rentrer l'adresse: http://csnet.local ou l'IP qui est remonté depuis Logs && Console depuis la page de téléchargement

## Page Web  

Csnet
- Il faut rentrer identifiant CSNET Home → Non d'utilisateur et mot de passe  

MQTT  
- rentrer l'IP du brocker et son port s'il n'est pas celui par défaut
- Le préfix MQTT et modifiable mais pas conseiller

- Le brocker MQTT va remonter plusieurs type en topic car l'ensemble des infos étant trop importante
  
- 1er Topic : csnet/csnet/availability  remonte juste si la connexion Csnet est online ou non
- 2e Topic : csnet/csnet/state
- 3e Topic : csnet/csnet/raw/elements
- 4e Topic : csnet/csnet/raw/installationdevices

Toutes les infos sont brutes sauf celles rentrées depuis l'appli. Exemple : si un circuit de chauffage est nommé radiateur, plancher ou autre
<img width="424" height="180" alt="image" src="https://github.com/user-attachments/assets/656fcf0f-c934-4a89-a5a6-1d840dd17d42" />



