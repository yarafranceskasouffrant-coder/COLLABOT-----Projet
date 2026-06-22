# COLLABOT-----Projet
# CollabBot — Collaboration homme-robot en cellule de production

## Membres du groupe (Groupe 5)
| Nom | Rôle |
| :--- | :--- |
| Etienne Maxi Christopher | Chef de projet & Intégration de la scène CoppeliaSim |
| Souffrant Yara Franceska | Responsable Documentation : Création et rédaction du fichier README.md |
| Christopher O. Raisin | Amélioration apporter au projet |
| Paul Laëka Nafawi | Recherche sur le cobot type Franka FR3 |
| Joseph Estha-Lenie S. | Conclusion |

## Description du projet
CollabBot simule une cellule industrielle automatisée et sécurisée où un cobot collabore activement avec un opérateur humain virtuel. Le robot exécute une tâche répétitive de prise et dépose de pièces en boucle sur une table de travail partagée. Grâce à l'intégration de capteurs de proximité dynamiques, la distance entre l'humain et le cobot est surveillée en temps réel conformément à la norme ISO 10218. Le système adapte la vitesse du robot (ralentissement progressif puis arrêt complet) selon la zone franchie, avant de reprendre sa tâche automatiquement une fois la sécurité rétablie.

## Lien GitHub / Scène CoppeliaSim
* **Dépôt GitHub Public :** [URL_DE_VOTRE_DEPOT_ICI](https://github.com/) *(À remplacer par votre lien)*
* **Fichier de la scène :** `scene_collabbot.ttt` *(Disponible à la racine du dépôt)*

## Capture / Vidéo de la simulation
![Statut de la simulation](https://via.placeholder.com/800x450.png?text=Insérer+ici+une+capture+d+écran+ou+un+GIF+de+CoppeliaSim) 
*(Rplacez ce lien par le chemin de votre capture d'écran ou de votre GIF une fois importé dans GitHub, ex: `images/simulation.gif`)*

## Composants / Modèles 3D utilisés
Le projet utilise les composants clés suivants au sein de CoppeliaSim :

| Composant / Modèle | Qté | Rôle |
| :--- | :--- | :--- |
| **Cobot Franka FR3** | 1 | Robot collaboratif principal (7 axes configurés avec Dummy IK cibles) |
| **Modèle humain articulé** | 1 | Opérateur virtuel simulant des mouvements sur un chemin (`Path`) |
| **Proximity Sensor** | 3 | Capteurs sphériques configurant les 3 zones de sécurité (Loin / Proche / Critique) |
| **Table de travail 3D** | 1 | Espace et plan de collaboration partagé entre l'opérateur et le cobot |
| **Pièces d'assemblage** | 5+ | Objets manipulés séquentiellement par l'effecteur (pince) du cobot |
| **Script Python/Lua de sécurité** | 1 | Logique principale de contrôle d'impédance et de gestion des événements |
| **UI Overlay (Interface)** | 1 | Affichage 2D du statut en temps réel : `NORMAL` (Vert), `ALERTE` (Orange), `ARRÊT` (Rouge) |
