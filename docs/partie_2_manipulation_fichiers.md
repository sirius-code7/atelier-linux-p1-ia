# Partie 2 : Manipulation des fichiers

## 1) Afficher le contenu de readme.txt

Commande : cat datasets/brut/readme.txt

https://drive.google.com/file/d/1dhuuPE3wv1PmheDvc_5DNavExJQ2ACGZ/view?usp=drive_link

## 2) Afficher les 5 premières lignes de train.csv

Commande : head -n 5 datasets/brut/train.csv

https://drive.google.com/file/d/1GGdc0Di0pUDU-dRpnY0aI64ew3VqXrUQ/view?usp=drive_link

## 3) Afficher les 3 dernières lignes de application.log

Commande : tail -n 3 logs/application.log

https://drive.google.com/file/d/1tke8uagQHpwPC-_hxjYrTLix6slvTeli/view?usp=drive_link

## 4) Compter le nombre de lignes de clients.csv

Commande : wc -l datasets/brut/clients.csv

https://drive.google.com/file/d/1ss7c_qYBRi5FYGY3jQxYtybJCfwHdIzx/view?usp=drive_link

## 5) Rechercher les lignes contenant WARNING

Commande : grep "WARNING" logs/application.log

https://drive.google.com/file/d/1-MHKWrJciYah2CgmglAzVfuFEy1dKmIH/view?usp=drive_link

## 6) Rechercher le mot INFO dans les journaux

Commande : grep "INFO" logs/*.log

https://drive.google.com/file/d/1B956by2xxkPISR_ch2X3e_g7jHXFGBj5/view?usp=drive_link

## 7) Copier train.csv dans datasets/clean

Commande : mkdir -p datasets/clean
cp datasets/brut/train.csv datasets/clean/

https://drive.google.com/file/d/10JKj2g1yPJRps34dFlxzDg2G2-yoaV_k/view?usp=drive_link

## 8) Renommer model_info.txt en modele.txt

Commande : mv models/model_info.txt models/modele.txt

https://drive.google.com/file/d/13fDR4meDxVYudmKWoi6Mpvb4G0vzoQdM/view?usp=drive_link


## 9) Supprimer test.csv

Commande : rm datasets/brut/test.csv

https://drive.google.com/file/d/15U3bRA7n5ePgcr_amcVe--S8VvwQmp19/view?usp=drive_link

## 10) Rechercher les fichiers csv

Commandes : find . -name "*.csv"

https://drive.google.com/file/d/1wHVQiOPKycORhqXALZuLyU5VoORbpUVl/view?usp=drive_link

## 11) Tous les fichiers .log

Commandes : find . -name "*.log"

https://drive.google.com/file/d/1rxqI5e5giC2GtYvBN_D7VjL37apdyuJQ/view?usp=drive_link

## 12) Fichiers triés par taille

Commandes : find . -type f -exec ls -la {} \; | sort -k5 -n

## 13) Concaténer application.log et training.log dans un nouveau fichier

Commandes : cat logs/application.log logs/training.log > logs/all_logs.log


## 14) Extraire les lignes contenant "Loss" dans loss.log

Commandes : grep "Loss" logs/training.log > logs/loss.log

## 15) Compter le nombre de fichiers du projet

Commandes: find . -type f | wc -l

## 16) Créer projet_IA.tar.gz dans backup

Commandes: mkdir -p backup
cd ..
tar -czvf IA_Project/backup/projet_IA.tar.gz IA_Project
cd IA_Project

https://drive.google.com/file/d/1y6Np4K330_fG8fLBWLqyf3JLY6OeHdrh/view?usp=drive_link

## 17) Restaurer la sauvegarde ailleurs, en dehors du projet

Commandes: mkdir -p ~/restore_test
tar -xzvf backup/projet_IA.tar.gz -C ~/restore_test
ls ~/restore_test

https://drive.google.com/file/d/18smDuazSHZ-H5fARo_-DwAMDi89qoui4/view?usp=drive_link


## END
