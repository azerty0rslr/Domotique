# Domotique
Domotique : pouvoir piloter des appareils
Avantage : confort, sécurité (caméra de sécurité), économie d'énergie 
Limitation : interopérabilité, sécurité, coûts

Histoire : bâteau en domotique, computer de cuisine 

Applications de la domotique : 
- Sécurité
- Thermostat
- Appareils électroménagers intelligents (frigo connecté)
- Santé et bien-être (traqueur de sommeil, détecteur de présence)

=> Permet d'automatiser et créer des routines quotidiennes

Dans l'industrie : CBENS - intègre des modules dans l'armoire industrielle

Protocoles liés à la domotique : zigbee, bluetooth, google home, amazon alexa, RTS, LoRaWAN, wifi

**Zigbee** - protocole par onde radio, porté de 15-20m, sortie en 1998
Avantages : très peu cher, peu de problèmes de compatibilité, basse consommation des dispositifs, réseau maillé entre les dispositifs, communications sécurisées et cryptées.

Inconvénients : risques de perturbations avec le WIFI car même fréquence 

**Z-Wave** - notion de classe, sortie en 1999, très peu répendu
Avantages : meilleure portée, meilleure compatibilité
Inconvénient : n'utilise pas la même fréquence dans le monde

**Thread** - mode de communication entre les appareils, apparition en 2015, utilise un réseau maillé, autoréparation du réseau
**Matter** - language utilisé avec le thread

**Bluetooth/Bluetooth Low Energy**

Normes à respecter sur certains protocoles pour pas d'interférences

Home Assistant - plateforme pour centraliser tout les éléments domotiques (vue centralisé des appareils domotiques, tableau de bord)
Compatible windows, apple, linux, VMWare, RasperyPY, Odroid - possibilité de virtualisation et de contenerisation

Architecture logicielle : les add-ons (permet d'intégrer des thèmes, des vues différentes)
Les 3 types de composants : 
Différents types d'entités : sensor, binary sensor, light, switch, camera, cover (ouvrants)
Sur home Asssistant possibilité de gestion des accès, de backup, de création de labs


### TP
- Rasperry
- Capteur de porte
- Zygbee
Port 8143 pour la configuration
