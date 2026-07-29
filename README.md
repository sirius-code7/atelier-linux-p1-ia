# Atelier Linux — Projet IA (Module p1ia)

## Contexte

Ce dépôt retrace la réalisation complète de l'Atelier Linux : préparer un environnement
Linux prêt pour un projet d'IA : organisation des données, gestion des utilisateurs et
des permissions, installation des outils, récupération d'un dataset, automatisation via
un script bash, et sauvegarde du projet.

**Auteur :** papa

**Machine utilisée :** Debian |debian/bookworm64| (Vagrant, ligne de commande)

## Structure du dépôt

IA_Project/
├── datasets/ # Données brutes et nettoyées (dataset iris.csv inclus)
├── config/ # Fichiers de configuration du projet
├── logs/ # Journaux applicatifs (rotation gérée via logrotate)
├── scripts/ # Scripts Python et bash (setup_project.sh, print-pause.py)
├── models/ # Informations sur le modèle IA
├── api/ # Dossier réservé au développement API
├── backup/ # Archives de sauvegarde du projet
├── documentation/ # Documents administratifs / réservé équipe
├── shared/ # Dossier partagé entre utilisateurs
└── docs/ # Documentation détaillée de chaque étape (voir ci-dessous)

## Suivi du travail — étape par étape

Chaque partie de l'atelier a été documentée et commitée séparément afin de garder un
historique clair et vérifiable :

| Partie | Description | Documentation |
|---|---|---|
| 1 | Organisation du projet (arborescence) | historique des commits |
| 2 | Manipulation des fichiers (cat, grep, tar...) | [docs/partie2_manipulation_fichiers.md](docs/partie_2_manipulation_fichiers.md) |
| 3 | Utilisateurs, groupes et permissions | [docs/partie3_utilisateurs_permissions.md](docs/partie3_utilisateurs_permissions.md) |
| 4 | Installation des logiciels + dataset iris.csv | [docs/partie4_installation_logiciels.md](docs/partie4_installation_logiciels.md) |
| 5 | Gestion des processus (PID, CPU, kill, bg/fg) | [docs/partie5_gestion_processus.md](docs/partie5_gestion_processus.md) |
| 6 | Script bash `setup_project.sh` | [docs/partie6_bash_scripting.md](docs/partie6_bash_scripting.md) |
| 7 | Bonus — rotation des logs (logrotate) | [docs/partie7_bonus_logrotate.md](docs/partie7_bonus_logrotate.md) |

## Document de synthèse final

Le document complet expliquant les principales commandes Linux utilisées et leur rôle
dans la préparation d'un environnement de développement IA est disponible ici :
[documentation/synthese_finale.md](documentation/synthese_finale.md)

## Livrables

1. Arborescence complète du projet ✅
2. Utilisateurs et groupes configurés avec permissions appropriées ✅
3. Logiciels installés et vérifiés ✅
4. Dataset téléchargé (iris.csv) ✅
5. Archive de sauvegarde du projet (`backup/`) ✅
6. Script `setup_project.sh` fonctionnel et commenté ✅
7. Document de synthèse des commandes Linux ✅
