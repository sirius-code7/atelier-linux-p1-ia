# Synthèse finale — Atelier Linux : Environnement pour un projet IA

## 1. Contexte et objectif

Cet atelier reproduit la mission d'un nouvel arrivant en entreprise chargé de préparer
un environnement Linux pour un projet d'intelligence artificielle. Il couvre les
fondamentaux d'administration système : organisation des fichiers, gestion des
utilisateurs et permissions, installation d'outils, automatisation et sauvegarde.

## 2. Vue d'ensemble de l'architecture

*(schéma de l'arborescence à insérer ici)*

## 3. Commandes clés par domaine

### 3.1 Organisation et manipulation de fichiers
| Commande | Rôle |
|---|---|
| `mkdir -p` | Crée une arborescence de dossiers en une seule commande |
| `touch` | Crée un fichier vide |
| `cat`, `head`, `tail` | Affichent tout ou partie du contenu d'un fichier |
| `grep` | Recherche un motif dans un ou plusieurs fichiers |
| `cp`, `mv`, `rm` | Copient, renomment/déplacent, suppriment des fichiers |
| `find` | Recherche des fichiers selon des critères (nom, extension...) |
| `tar` | Archive et compresse un dossier (sauvegarde) |

### 3.2 Utilisateurs et permissions
| Commande | Rôle |
|---|---|
| `useradd -m`, `passwd` | Créent un utilisateur et son mot de passe |
| `groupadd` | Crée un groupe |
| `usermod -aG` | Ajoute un utilisateur à un groupe sans écraser ses groupes existants |
| `chown`, `chgrp` | Attribuent un propriétaire / un groupe à un fichier ou dossier |
| `chmod` | Définit les droits (lecture/écriture/exécution) |
| `su - utilisateur` | Change de session pour vérifier les droits réels |

### 3.3 Installation et outils
| Commande | Rôle |
|---|---|
| `apt-get update / install` | Met à jour et installe des paquets système |
| `wget` | Télécharge un fichier depuis Internet (ici : dataset iris.csv) |

### 3.4 Processus
| Commande | Rôle |
|---|---|
| `ps`, `pgrep` | Identifient un processus et son PID |
| `htop`, `top` | Surveillent l'utilisation CPU/mémoire en temps réel |
| `kill` | Arrête un processus |
| `&`, `jobs`, `fg`, `bg` | Gèrent l'exécution en arrière-plan / premier plan |

### 3.5 Automatisation
| Commande / notion | Rôle |
|---|---|
| script bash (`setup_project.sh`) | Automatise l'ensemble des étapes de création du projet |
| `logrotate` | Automatise l'archivage et la compression des logs (bonus) |

## 4. Pourquoi c'est pertinent pour un projet IA

- Une arborescence claire évite de mélanger données brutes, code et modèles.
- Une gestion fine des permissions protège les données sensibles (`clients.csv`) et
  évite qu'un stagiaire modifie un modèle en production.
- L'automatisation (script + logrotate) garantit une mise en place reproductible et
  un environnement qui ne se dégrade pas dans le temps (logs qui grossissent, etc.).

## 5. Difficultés rencontrées et résolutions

- Erreur de syntaxe `tar --exclude` positionné après les arguments → corrigée en
  plaçant l'option avant les arguments positionnels.
- Avertissement `apt` non stable en script → remplacé par `apt-get` pour la fiabilité.

## 6. Documentation détaillée

Le détail commande par commande, avec les résultats obtenus, est disponible dans le
dossier [`docs/`](../docs) :
- [Partie 2 — Manipulation des fichiers](../docs/partie2_manipulation_fichiers.md)
- [Partie 3 — Utilisateurs et permissions](../docs/partie3_utilisateurs_permissions.md)
- [Partie 4 — Installation des logiciels](../docs/partie4_installation_logiciels.md)
- [Partie 5 — Gestion des processus](../docs/partie5_gestion_processus.md)
- [Partie 6 — Script bash setup_project.sh](../docs/partie6_bash_scripting.md)
- [Partie 7 — Bonus : logrotate](../docs/partie7_bonus_logrotate.md)
