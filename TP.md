# Jour 1
## Configuration du Raspberry
Sur Raspberry Pi Imager, nous installons le système d'exploitation.  
<img width="806" height="599" alt="image" src="https://github.com/user-attachments/assets/7fe95c10-51f8-4d01-b6e3-0003fdcfe863" />  
<img width="799" height="597" alt="image" src="https://github.com/user-attachments/assets/d7f5e60e-a29c-42ae-8e9e-8ebacd34ac85" />  
<img width="756" height="581" alt="image" src="https://github.com/user-attachments/assets/8cba55f4-70c2-4357-bef8-e7113ba0ba41" />  
<img width="616" height="356" alt="image" src="https://github.com/user-attachments/assets/c9c0e0fc-91b6-4dcb-ab06-3fb0a50925fa" />  
<img width="656" height="483" alt="image" src="https://github.com/user-attachments/assets/e296064f-96e0-43d9-a7f2-3764ab272e3d" />  

La carte est insérée et le Pi est alimenté on termine donc l'installation sur http://homeassistant.local:8123  
Créer l'utilisateur :  
<img width="393" height="403" alt="image" src="https://github.com/user-attachments/assets/7ffe6d2a-7f68-4e53-a778-d1074a97cb79" />  
  
Tout autoriser :  
<img width="368" height="407" alt="image" src="https://github.com/user-attachments/assets/1bdd9335-6e74-450a-85bd-e3aa9bebddf0" />  
  
Voici le premier rendu du home assistant :  
<img width="780" height="291" alt="image" src="https://github.com/user-attachments/assets/f7e04ec8-c68b-4de3-b9bd-8975c2210542" />  

Pour connecter les objets intelligent, nous configurons le protocole Zigbee grâce à la documentation suivante : https://www.domo-blog.fr/installer-mqtt-zigbee2mqtt-home-assistant-en-mode-supervision-guide-domotique-all-inclusive/  
Aller dans paramètre puis dans Appareils et services :  
<img width="744" height="408" alt="image" src="https://github.com/user-attachments/assets/421dc4ae-d839-4a80-ac47-b1e38d489053" />  
  
Il n'y a pas de modules complémentaires donc aller dans la boutique :  
<img width="656" height="395" alt="image" src="https://github.com/user-attachments/assets/87867000-386c-4fb2-8407-b9e10c070d92" />  
  
Rechercher et installer Zigbee2MQTT :  
<img width="782" height="371" alt="image" src="https://github.com/user-attachments/assets/5d7f6879-d721-4403-9b09-f13efdf030e0" />  

  
Rechercher le port :  
<img width="366" height="285" alt="image" src="https://github.com/user-attachments/assets/dcac1a92-fc5b-478c-bee2-0153498cf143" />  
  
Inscrire son nom de la manière suivante :  
<img width="619" height="364" alt="image" src="https://github.com/user-attachments/assets/8a01b49a-6c57-4329-9e55-3680c81fcedb" />  

  
Ajouter Mosquitto Broker :  
<img width="593" height="338" alt="image" src="https://github.com/user-attachments/assets/a05f9999-6508-4f04-a500-09725295271c" />  
  
Ajouter l'utilisateur :  
<img width="394" height="403" alt="image" src="https://github.com/user-attachments/assets/029cd6de-1a39-4dd0-9503-d26143e975d7" />  
  
<img width="304" height="336" alt="image" src="https://github.com/user-attachments/assets/26298d23-b357-49b4-b614-d53d55eeeccc" />  
  
  
Sur Zigbee2MQTT, activer l'appeirage pour connecter les différents outils :  
<img width="321" height="415" alt="image" src="https://github.com/user-attachments/assets/554ecf7d-27ac-4649-94c5-73ed83d66542" />  
  
Voilà :  
<img width="740" height="255" alt="image" src="https://github.com/user-attachments/assets/b8d493b0-843f-480c-b8aa-15e4ae1e5696" />  
  
  
# Jour 2
Après multiples complications, nous nous reconnectons sur Home Assistant en filaire via http://10.60.0.3:8123 :  
<img width="1820" height="839" alt="image" src="https://github.com/user-attachments/assets/d082d23b-89ce-4997-9605-16c949ca742d" />  

Ensuite on s'occupe de l'installation de HACS.  
On va dans Paramètres -> Modules complementaires -> Boutique des modules complementaires puis on installe le module Terminal & SSH  
Il ne s'agit pas de ce module. Erreur de notre part.  
<img width="1452" height="543" alt="image" src="https://github.com/user-attachments/assets/be0a9f93-ae95-4f98-9375-49d6d3a6ff43" />  

Mais si vous ne trouvez rien d'autre que lui aller sur le profil de l'utilisateur, descendre et activer le mode avancé.  
<img width="1527" height="385" alt="image" src="https://github.com/user-attachments/assets/2928caab-2b72-40fd-9ed1-ea909e4fe80a" />  
  
Puis recommancer la recherche et installer CE terminal & SSH :  
<img width="1428" height="546" alt="image" src="https://github.com/user-attachments/assets/a54ba49b-1525-46d4-8ed2-b0ce8cb8597f" />  
  
Une fois installé, le démarrer puis cliquer sur Ouvrir l’interface utilisateur web :  
<img width="1266" height="337" alt="image" src="https://github.com/user-attachments/assets/ec200fc3-cc03-4881-8d7b-6f6c31dd6a63" />  
  
Puis copier coller ```wget -O - https://get.hacs.xyz | bash -```.  
<img width="676" height="784" alt="image" src="https://github.com/user-attachments/assets/6dc36639-5f75-4546-b7e6-938125e1f57b" />  
  
Ensuite aller dans Outils de développement, faire Redémarrer puis Redémarrer Home Assistant.  
<img width="1753" height="823" alt="image" src="https://github.com/user-attachments/assets/86f93fb5-f13b-42bc-82bd-1c752972d1f3" />  
  
Aller dans Paramètres -> Appareils et services, faire Ajouter une intégration, rechercher HACS et l'ajouter.  
<img width="1507" height="836" alt="image" src="https://github.com/user-attachments/assets/a4fedac8-2c04-41c8-b1db-1fea93d3c532" />  
  
Tout cocher puis s'authentifier sur GitHub comme demandé :  
<img width="715" height="508" alt="image" src="https://github.com/user-attachments/assets/cffcc0fe-2744-4d28-9e9a-dfd5cf7caf32" />  

Autoriser HACS sur GitHub :  
<img width="630" height="695" alt="image" src="https://github.com/user-attachments/assets/b6ec3565-6766-4390-9f70-3b0498bfa284" />  
  
Et voilà de cette manière, nous avons débloqué pleins d'intégrations via HACS :  
<img width="1772" height="847" alt="image" src="https://github.com/user-attachments/assets/b8bdbcae-a89a-421b-a59d-ba94f8f1c9d4" />  

## Configuration d'une interface
Nous avons trouvé la documentation suivante https://www.hacf.fr/un-beau-dashboard-tout-simplement/#hacs-pour-aller-plus-loin pour configurer un beau dashboard, nous avons donc décidé de la suivre.  
Aller dans Paramètres -> Tableau de bord  
<img width="1508" height="902" alt="image" src="https://github.com/user-attachments/assets/039bb081-d677-40a2-83ce-f3b623c6c093" />  

Faire "Ajouter un tableau de bord"  
<img width="584" height="718" alt="image" src="https://github.com/user-attachments/assets/9b7be024-39c1-4df0-a85a-3497324620ca" />  

Et voilà, plus qu'à ajouter les différentes sections :  
<img width="1506" height="871" alt="image" src="https://github.com/user-attachments/assets/2dd87a66-ed7e-49cb-aec1-805835461175" />  

  
# Jour 3
## Météo France 
En suivant le readme de https://github.com/hacf-fr/lovelace-meteofrance-weather-card ainsi que le tuto d'installation de cartes personnalisées https://www.home-assistant.io/dashboards/cards/ nous avons installé un module météo France :  
<img width="1511" height="830" alt="image" src="https://github.com/user-attachments/assets/51983713-defd-48c8-9351-8a8cc6bb7915" />  

Cliquer sur la carte qui s'affiche et faire Télécharger :  
<img width="1486" height="805" alt="image" src="https://github.com/user-attachments/assets/b5d5b5fe-9c24-4f5c-8913-90cdd73456ed" />  
  
Aller dans Appareils et Services puis dans Hacs :  
<img width="1470" height="861" alt="image" src="https://github.com/user-attachments/assets/cb9b70f1-f7de-435c-b0f1-a55cd6246a60" />  
  
Faire le petit crayon et s'assurer que "Activer service" est bien activé :  
<img width="870" height="625" alt="image" src="https://github.com/user-attachments/assets/12c57146-9fdb-44ee-b55a-21b4427ec351" />  
  
Ensuite aller sur le tableau de bord, faire Ajouter au tableau de bord et sélectionner la carte personnalisé :  
<img width="1503" height="902" alt="image" src="https://github.com/user-attachments/assets/4d8f540b-80cf-4971-837f-f3b8fae160a6" />  
  
Et voilà :  
<img width="1478" height="873" alt="image" src="https://github.com/user-attachments/assets/50e47769-bea5-4bd0-851a-43a7ebc678da" />  
  
## Mushroom
Pour un peu plus d'esthétisme, nous avons décidé d'installer Mushroom à notre dashboard grâce à sa documentation https://github.com/piitaya/lovelace-mushroom.  
Dans HACS, taper "Mushroom" et l'installer :  
<img width="1496" height="914" alt="image" src="https://github.com/user-attachments/assets/573c4f61-e50f-4c87-a956-c3129b683b70" />  
  
On peut désormais rajouter quelques cartes un peu plus esthétiques.  
<img width="481" height="172" alt="image" src="https://github.com/user-attachments/assets/68acb103-f2ca-487e-9f35-01c3f76a1006" />  

## Liaison de deux appareils
Nous avons suivi le tutoriel suivant pour lier le bouton à la bande LED : https://rdr-it.com/domotique/home-assistant-changer-la-couleur-dampoule-avec-un-bouton-connecte/.  
  
