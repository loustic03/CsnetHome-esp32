### Passerelle pour connecter une PAC HITACHI depuis Csnet Home

## Il existe un projet pour CSNET Home pour utilisation sur Home Assistant   

https://github.com/mmornati/home-assistant-csnet-home.git  

- Je me suis appuyé sur ce projet pour créer la passerelle sur esp32 
  
Utilisant Jeedom sur lequel il n'y a pas de plugin, j'ai créer une passerelle avec un esp32 et qui permet d'envoyer les infos de ma PAC sur MQTT mais ne permet pas de la piloter

# CsnetHome-esp32 (ne fonctionne que pour les PAC utilisant Csnet Home)
Passerelle esp32 pour se connecter sur Csnet Home et renvoyer les infos sur MQTT   

## Comment installer le code sur l'ESP32   
- Lancer l'installateur depuis ce lien: https://loustic03.github.io/CsnetHome-esp32/
  
  <img width="672" height="281" alt="image" src="https://github.com/user-attachments/assets/304f43d2-4db9-48ac-a17b-2fa33899f392" />

  ensuite connecter l'ESP32 en USB et cliquer sur Installer le Firmware, sélectionner le port indiquer et cliquer sur connexion
  pour certain ESP32 il faut appuyer sur le bouton Boot de l'ESP 


## Accès à l'esp après téléchargement  
- Depuis le navigateur rentrer l'adresse: http://csnet.local ou l'IP qui est remonté depuis Logs & Console depuis la page de téléchargement

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

## Projet qui peut-être fait avec un JC3248W535 C : 

<img width="249" height="177" alt="image" src="https://github.com/user-attachments/assets/d8e6dec9-0104-4956-9475-12d717bfe590" />  

<img width="205" height="136" alt="image" src="https://github.com/user-attachments/assets/b4024355-6510-4093-881f-0bf70588f13f" />





