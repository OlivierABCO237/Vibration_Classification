# Vibration_Classification
Recognition of vibration of a device, with 

### Etape 1: **Récupération des données**
- Vibrations réalisées par une application sur android
- L'arduino Nano BLE sense collée sur l'arrière du téléphone, pour enregistrer les vibrations dedit téléphone
- Réalisation de plusieurs labels de données: petite vibration, repos, grande vibration, vibration cardiaques

### Etape 2: **Création de l'impulse**
- Ajout d'un bloc "Spectral analysis" dans processing bloc et d'un bloc "Anomaly detection" dans learning bloc
- Sauvegarde de l'impulse et génération des features:
  Ces données sont relatives au positionnement suivant x, y et z du capteur; et de l'acceleration suivant x, y et z du capteur
- Entrainement des données: Les résultats de l'entrainement sont assez mauvais. 33.33% de précision.
  ceci est surement du aux conditions de prise des données, et à la difference assez fine entre les types de vibrations.
  Ceci est aussi du à la quantité de données.
- Annomaly detection: Les facteurs accx RMS, accy RMS et accz RMS sont representés ici comme les annomalies 

  ### Etape 3: **Test du modele**
  - D'autres données sont prises de la meme manière pour une tester le modèle.
  - Une seule des classes est representée, et un enregistrement de 30 secondes est prise
  - Classification du label pris. 
  - comme attendu, le résultat n'est pas bon.
 
  ### Etape 4: **Implementation**
  - Une bibliothèque arduino est générée
  - après inclusion de la bibliothèque dans arduino IDE, des tests sont réalisés pour afficher sur le moniteur serie la nature de la vibration.
  - Ce code peut permettre d'entreprendre d'autres actions, si le bon type de vibration est détecté.
     Par exemple, allummer une led et dénérer un signal sonore sur un buzzer si l'appareil ne vibre pas comme il devrait,
     Allumer une led d'une autre couleur l'ors d'un fonctionnement normal
     Allumer une led avec une troisième couleur l'ors d'un fonctionnement d'un mode precis.
