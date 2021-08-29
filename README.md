# My Home Assistant config 

![Project Maintenance][maintenance-shield]
[![License][license-shield]](LICENSE.md)

[![Github workwlow][workflow-shield]][workflow]
[![GitHub Activity][commits-shield]][commits]
[![GitHub Last Commit][last-commit-shield]][commits]

[![Discord francophone][discord-shield-fr]][discord-fr]
[![Forum francophone][forum-shield-fr]][forum-fr]
[![Awesome francophone][awesome-shield]][awesome-fr]


[![Official Discord][discord-shield]][discord]
[![Official community Forum][forum-shield]][forum]

Welcome to my Home Assistant configuration!
Bienvenue chez ma configuration Home Assistant !

You will find English README content [here](#for-english-speaking-users).

Vous trouverez le contenu en français du README [ici](#pour-les-francophones).

## Pour les francophones

Ne soyez pas effrayés par la structure non standard de cette configuration pour Home-Assistant.
J'ai été inspiré par [la structure propsée par Franck Nijhof](https://github.com/frenck/home-assistant-config).

Cette approche est très modulaire et très différente dans sa strucutre des autres configurations que vous trouverez sur Internet.

L'idée c'est que chaque fichier dans ce dépôt ne fait qu'une seule chose !
Vous pouvez ainsi chercher le fichier qui correspond à un composant,
cliquez et vous trouverez rapidement l'information.
Le fichier `configuration.yaml` n'est utilisé que pour amorcer le système
et contient des paramètres minimaux, mais vitaux.

Si vous êtes à l'aise en anglais, je conseille le visionnage [de la video de Franck](https://www.youtube.com/watch?v=lndeybw21PY)
expliquant pourquoi il a fait ces choix.

J'ai essayé d'ajouter des commentaires et des liens vers la documentation pour chaque fichier YAML quand cela à une valeur ajoutée.

Attention: ma décision d'avoir une documentation bilingue en ajoutant le français a été faite dans un second temps.
Donc la partie francophone n'est pas encore complète.

Si vous avez des questions ou voulez discuter de ma configuration,
vous pouvez me retrouver sur [le réseau HACF (forum, Discord, organisation GitHub, etc...)
où on y parle français](https://hacf.fr) ou sur [le réseau Home Assistant officiel](https://www.home-assistant.io/).

### Appareils utilisés

- Un Microseveur HP Gen8 pour héberger un Machine Virtuelle HassOS
- Les objets Xiaomi:
  - Robot aspirateur Roborock cleaner
  - Pleins de capteurs et interrupteurs
- Zwaves:
  - Prises avec contrôle de la consomation
  - Détecteurs incendies
- RFXCOM pour accéder à des capteurs Oregon
- Ampoules Philips Hue et appareils Zigbee compatibles
- Quelques objets DIY à base d'esp32 en utilisant [ESPHome](https://esphome.io)
- Telegram pour les notifications
- Google home et Chromecast
- Renault Zoé ma voiture électrique
- Linky
- Serveur Plex qui tourne sur mon NAS
- Conbee 2 pour controler mes appareils Zigbee (Xiaomi, Hue and OSRAM)
- UPC Back-UPS pour protéger des coupures électriques mon Microserveur, mon
  switch et mon NAS.
- Un Sonoff POW R2 gérer la pompe de filtration de ma piscine
- Un NAS Synology
- Une imprimante Brother
- Une Livebox pour ma connexion ADSL.
- Les téléphones de la maisons (iOS et Android)

### Automations

Vous trouverez dans mes scripts et automations les fonctionalités suivantes:

- Un backup régulier de ma configuration Home-Assistant.
- Surveiller la disponibilité des appareils critiques de ma maison.
- Surveiller la qualité de ma connexion Internet.
- Piloter le robot Aspirteur à partir de Google Home.
- Les routines quotidiennes pour nettoyer avec le robot aspirateur.
- Gestion d'un alarme (besoin de retravailler cette partie).
- Vérification et notification si des lumières devraient être éteintes
- Envoie une notification en cas d'alerte météo ou de pluie attendue
- Envoie un notification si j'ai oublié de brancher ma voiture électrique
- Piloter le calendrier de la pompte de filtration de la piscine.
- Et pleins d'autre choses...

### les _Custom components_ utilisés

Les custom components qui m'aident:

- [HACS](https://github.com/custom-components/hacs)&#42; pour gérer la mise à jour
  des composants utilisés.
- [variable](https://github.com/Wibias/hass-variables)&#42; merci à
  **rogro82** pour la création et **Wibias** pour la maintenance.
- [Pool Pump Manager](https://github.com/oncleben31/ha-pool_pump)&#42; pour piloter la pompe de filtration de ma piscine. Merci à moi même ;-) et à **exxamalte** pour l'inspiration de son module [pool-pump](https://github.com/exxamalte/home-assistant-customisations/tree/master/pool-pump)
- [Orange Livebox Router](https://github.com/Cyr-ius/hass-livebox-component)&#42; pour récupérer des information de ma livebox. Merci à **Cyr-ius**
- [Blitzortung.org lightning detector](https://github.com/mrk-its/homeassistant-blitzortung)&#42; pour détecter les orages près de chez moi. Merci à **mrk-its**.

(&#42;): intégrations gérées avec HACS

### Integrations configurées via l'IHM dans HA

Les integrations suivantes ne sont pas configurées dans les fichiers YAML.
Vous ne les verrez donc pas dans ce dépôt:

- [Application mobile](https://www.home-assistant.io/integrations/mobile_app/) pour intégrer les informations des smartphones de la famille.
- Blitzortung (cf. liste des customs components).
- [Brother](https://www.home-assistant.io/integrations/brother/) pour avoir
  l'état de mon imprimante.
- CO2 Signal
- [deCONZ](https://www.home-assistant.io/integrations/deconz/) pour piloter mes
  appareils Zigbee.
- [ESPHome](https://www.home-assistant.io/components/esphome/) pour intégrer des
  ESP ou SONOFF.
- [IFTTT](https://www.home-assistant.io/components/ifttt/) utilisé pour piloter
  le robot aspirateur par la voix.
- [Google Cast](https://www.home-assistant.io/components/cast/) utilisé pour
  envoyer des message TTS sur ma Google Home
- [Météo-France](https://www.home-assistant.io/integrations/meteo_france/) pour
  avoir la météo, les alertes météo et la prévision de pluie dans l'heure.
- [Network UPS Tool (NUT)](https://www.home-assistant.io/integrations/nut) pour
  surveiller mon UPC Back-UPS. Pour les NAS synology il y a une astuce sur le site de [Cachem.fr](https://www.cachem.fr/ups-domoticz-synology/)
- Livebox (cf. liste des customs components).
- [Plex](https://www.home-assistant.io/integrations/plex/) pour connceter mon
  serveur Plex
- [Renault](https://www.home-assistant.io/integrations/renault/) pour remonter les information de ma Zoe. Big up a @epenet qui a investi beaucoup d'energie (avec un peu de mon aide) pour rendre cette integration officielle et aboutie.
- [RFXTRX](https://www.home-assistant.io/integrations/rfxtrx/) pour gérer mes appareils radios.
- [SpeedTest](https://www.home-assistant.io/integrations/speedtestdotnet/) pour surveiller ma connexion ADSL.
- [Synology](https://www.home-assistant.io/integrations/synology_dsm/) pour surveiller mon NAS.
- [Waze](https://www.home-assistant.io/integrations/waze_travel_time/) pour surveiller la durée des trajets quotidiens de la famille.

### Addons utilisés

- [InfluxDB](https://github.com/hassio-addons/addon-influxdb)
- [SSH & Web Terminal](https://github.com/hassio-addons/addon-ssh)
- [Unifi Controller](https://github.com/hassio-addons/addon-unifi): attention
  celui là consomme beaucoup de mémoire et peu être la cause racine de problème
  sur un Rasberry Pi 3.
- [deCONZ](https://github.com/home-assistant/hassio-addons/tree/master/deconz)
- [MariaDB](https://github.com/home-assistant/addons/tree/master/mariadb) pour héberger ma base de donnée Home Assistant.

### One more thing

J'ai ajouté d'autres information spécifiques dans le [wiki](https://github.com/oncleben31/home-assistant-config/wiki).
N'oubliez pas de le visiter. Attention pas encore traduit.

### Me contacter

Si vous voulez discuter de ma configuration, vous pouvez le faire à travers les outils suivant:

- GitHub par l'intermédiare [des issues][issues] ou [des discussions][discussions].
- Sur [le forum officiel anglophone][forum] ou sur [celui de la communauté HACF en français][forum-fr].
- Sur le [Discord de la communauté HACF][discord-fr].

## For English speaking users

Don't be scared by the non standard structure of the Home Assistant configuration folder.
I'm inspired by [the strucutre propsed by Franck Nijhof](https://github.com/frenck/home-assistant-config).

This system is very modular and very differently structured compared to other,configurations you'll find online.

Basically, each file in the repository does 1 (one, uno, eins) thing only!
Search file with the name of the component, click through it, you'll get it pretty fast.
The `configuration.yaml` is only used to bootstrap the system
and contains some minimal, but vital, settings.

You can watch [a video by Franck](https://www.youtube.com/watch?v=lndeybw21PY)
explaining why is doing that way.

I try to add comments and link with external documentations for each YAML file when needed.

If you have questions or want to discuss about my configuration,
you can reach me on [the HACF network (forum, Discord, GitHub organization, etc...)
where we speak French](https://hacf.fr) or on [the official Home Assistant network](https://www.home-assistant.io/).

### Devices used

- A Microserver HP Gen8 to host a HassOS Virtual Machine
- Xiaomi devices:
  - Vacuum Roborock cleaner
  - Lot of sensors and switchs
- Zwaves:
  - Switchs with energy monitoring
  - Fire detectors
- RFXCOM to access Oregon sensors
- Philips Hue bulbs and compatible Zigbee devices
- DIY with esp32 using [ESPHome](https://esphome.io)
- Telegram
- Google home and Chromecast
- Renault Zoé my electric car
- Linky electrcity monitoring system
- Plex server running on my NAS
- Conbee 2 for managing Zigbee devices (Xiaomi, Hue and OSRAM)
- UPC Back-UPS to protect against power failure my Microserver, my switch and
  my NAS.
- Sonoff POW R2 for managing the swiming pool pump (in progress)
- NAS Synology
- ADSL box from Orange.
- Family phones (iOS and Android)

### Automations

You can find in my automations and scripts the following features:

- Regular Home Assistant backup
- Monitoring of the availibility of the crtical systems of the house.
- Monitoring the quality of the internet connexion.
- Control thru Google Assistant of the Vacuum.
- Daily routines for cleaning the house with the Vacuum.
- Alarm management (need rework).
- Check and notification if lights could be switch off.
- Send notification in case of weather alert or rain expected.
- Send notification if I forget to plug the electrical car.
- Manage the pool pump schedule.
- And many other things...

### Custom components used

To help me I used the following custom components:

- [HACS](https://github.com/custom-components/hacs)&#42; to follow updates of custom
  components and cards.
- [variable](https://github.com/Wibias/hass-variables)&#42; integration thanks to
  **rogro82** for creating it and **Wibias** for maintenance.
- [Pool Pump Manager](https://github.com/oncleben31/ha-pool_pump)&#42; to manage the swiming pool pump thanks to me ;-) and **exxamalte** for inspiring me with his [pool-pump](https://github.com/exxamalte/home-assistant-customisations/tree/master/pool-pump) module.
- [Orange Livebox Router](https://github.com/Cyr-ius/hass-livebox-component)&#42; to monitor my ADSL box. Thanks to **Cyr-ius**
- [Blitzortung.org lightning detector](https://github.com/mrk-its/homeassistant-blitzortung)&#42; For lightning detection. Thanks to **mrk-its**.

(&#42;): integrations update managed with HACS

### Integrations configured thru HA GUI

The following integrations are not configured in YAML files. So you won't see it
in this repository:


- [Mobile App](https://www.home-assistant.io/integrations/mobile_app/) to integrate familly smartphones data.
- Blitzortung (cf. customs components list).
- [Brother](https://www.home-assistant.io/integrations/brother/) to have a status
  of my new printer.
- CO2 Signal
- [deCONZ](https://www.home-assistant.io/integrations/deconz/) pour control my Zigbee devices.
- [ESPHome](https://www.home-assistant.io/components/esphome/) devices
  integration in HA.
- [IFTTT](https://www.home-assistant.io/components/ifttt/) used for piloting the
  vacuum robot from the Google Home.
- [Google Cast](https://www.home-assistant.io/components/cast/) used for some
  TTS messages in the house.
- [Météo-France](https://www.home-assistant.io/integrations/meteo_france/) to
  have weather alerts and rain forecast within the hour.
- [Network UPS Tool (NUT)](https://www.home-assistant.io/integrations/nut) to
  monitor my UPC Back-UPS.
- Livebox (cf. custom components list).
- [Plex](https://www.home-assistant.io/integrations/plex/) to connect my Plex
  server.
- [Renault](https://www.home-assistant.io/integrations/renault/) to integrate my Zoe data. Kudos to @epenet who has invest a lot of energy with a little support from me to have this official integration.
- [RFXTRX](https://www.home-assistant.io/integrations/rfxtrx/) to control my radio devices.
- [SpeedTest](https://www.home-assistant.io/integrations/speedtestdotnet/) to monitor my ISP connexion.
- [Synology](https://www.home-assistant.io/integrations/synology_dsm/) to monitor my NAS.
- [Waze](https://www.home-assistant.io/integrations/waze_travel_time/) to monitor the duration of our commutes.


### Addons used

- [InfluxDB](https://github.com/hassio-addons/addon-influxdb)
- [SSH & Web Terminal](https://github.com/hassio-addons/addon-ssh)
- [Unifi Controller](https://github.com/hassio-addons/addon-unifi): warning this
  one use a lot of memory and can be the root cause of issues on Raspberry Pi 3.
- [deCONZ](https://github.com/home-assistant/hassio-addons/tree/master/deconz)
- [MariaDB](https://github.com/home-assistant/addons/tree/master/mariadb) to host Home Assisant database.

### One more thing

I have and will add specific explanations in the [wiki](https://github.com/oncleben31/home-assistant-config/wiki).
So don't forget to visit it.

### Contact me

If you want to discuss with me about my configuration, you can do it through the following tools:

- GitHub with [the issues][issues] or [the discussions][discussions].
- On [the official forum in English][forum] or on [the HACF community one in French][forum-fr].
- On the [HACF community Discord in French][discord-fr].


[commits-shield]: https://img.shields.io/github/commit-activity/y/oncleben31/home-assistant-config
[commits]: https://github.com/oncleben31/home-assistant-config/commits/master
[discord-shield]: https://img.shields.io/discord/330944238910963714?label=Official%20HA%20Discord&logo=discord
[discord]: https://discord.gg/c5DvZ4e
[discord-shield-fr]: https://img.shields.io/discord/706096417000652840?label=Discord%20francophone%20HACF&logo=discord
[discord-fr]: https://discord.com/invite/PaZFEjX
[discussions]: https://github.com/oncleben31/home-assistant-config/discussions
[forum-shield]: https://img.shields.io/discourse/topics?label=Official%20HA%20forums&logo=discourse&server=https%3A%2F%2Fcommunity.home-assistant.io%2F
[forum]: https://community.home-assistant.io/
[forum-shield-fr]: https://img.shields.io/discourse/topics?label=Forum%20francophone%20HACF&logo=discourse&server=https%3A%2F%2Fforum.hacf.fr%2F
[forum-fr]: https://forum.hacf.fr/
[issues]: https://github.com/oncleben31/home-assistant-config/issues
[last-commit-shield]: https://img.shields.io/github/last-commit/oncleben31/home-assistant-config.svg
[license-shield]: https://img.shields.io/github/license/oncleben31/home-assistant-config.svg
[maintenance-shield]: https://img.shields.io/maintenance/yes/2021.svg
[workflow-shield]: https://github.com/oncleben31/home-assistant-config/workflows/Home%20Assistant%20configuration/badge.svg
[workflow]: https://github.com/oncleben31/home-assistant-config/actions
[awesome-shield]: https://awesome.re/badge.svg
[awesome-fr]: https://github.com/hacf-fr/awesome-francophone-home-assistant
