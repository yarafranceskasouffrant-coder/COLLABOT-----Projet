# COLLABOT-----Projet
# CollabBot — Collaboration homme-robot en cellule de production

## Membres du groupe (Groupe 5)
| Nom | Rôle |
| :--- | :--- |
| Etienne Maxi Christopher | Chef de projet & Intégration de la scène CoppeliaSim |
| Souffrant Yara Franceska | Responsable Documentation : Création et rédaction du fichier README.md |
| Christopher O. Raisin | Amélioration apporter au projet |
| Paul Laëka Nafawi | Présentation du Robot UR5|
| Joseph Estha-Lenie S. | Conclusion |

## Description du projet
CollabBot simule une cellule industrielle automatisée et sécurisée où un cobot collabore activement avec un opérateur humain virtuel. Le robot exécute une tâche répétitive de prise et dépose de pièces en boucle sur une table de travail partagée. Grâce à l'intégration de capteurs de proximité dynamiques, la distance entre l'humain et le cobot est surveillée en temps réel conformément à la norme ISO 10218. Le système adapte la vitesse du robot (ralentissement progressif puis arrêt complet) selon la zone franchie, avant de reprendre sa tâche automatiquement une fois la sécurité rétablie.

## Lien GitHub / Scène CoppeliaSim
* **Dépôt GitHub Public :** [https://drive.google.com/file/d/1QflpbwY330M5ULykuFFfANesKITFCWj6/view?usp=drivesdk](https://drive.google.com/file/d/1QflpbwY330M5ULykuFFfANesKITFCWj6/view?usp=drivesdk)

(https://github.dev/)

## Capture / Vidéo de la simulation
![https://drive.google.com/file/d/1ylC86AG1KDoSUMGH0h37z7rugh9xfYK3/view?usp=drivesdk](https://drive.google.com/file/d/1ylC86AG1KDoSUMGH0h37z7rugh9xfYK3/view?usp=drivesdk) 
<img width="1365" height="722" alt="collabBot-Screen" src="https://github.com/user-attachments/assets/0188ddea-a7fa-431b-9e8a-7d2e5a6ec91f" /> 



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

## Conclusion
Ce projet de certification nous a permis de concevoir, programmer et valider une cellule robotique collaborative conforme aux exigences strictes de la norme de sécurité industrielle **ISO 10218**. Grâce à l'environnement de simulation CoppeliaSim et au script Sandbox, notre groupe a réussi à orchestrer une synergie parfaite entre l'exécution d'une tâche industrielle (Pick & Place du cube) et la sécurité d'un opérateur humain. Cette expérience met en lumière les défis de la proxémique en robotique et l'importance cruciale de la programmation événementielle dans l'industrie.
