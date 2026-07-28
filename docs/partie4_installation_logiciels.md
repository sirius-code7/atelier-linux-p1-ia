## 1) Mettre à jour les paquets et installer les outils

sudo apt update
sudo apt install -y git curl wget htop tree python3 python3-pip unzip

git est probablement déjà installé "already the newest version".

## 2) Vérifier l'installation de chaque outil

git --version
curl --version
wget --version
htop --version
tree --version
python3 --version
python3 -m pip --version
unzip -v

https://drive.google.com/file/d/1GmMZlTX2h2MbaYqyEgm7PiY8M3vEkF2C/view?usp=drive_link

https://drive.google.com/file/d/1E5uodjxfuToU1O6eyiZE5i5QQyYGB6c0/view?usp=drive_link

## 3) Télécharger le dataset

cd ~/IA_Project
wget https://raw.githubusercontent.com/mwaskom/seaborn-data/master/iris.csv -P datasets/brut/

note: -P datasets/brut/ place directement le fichier dans le bon dossier

https://drive.google.com/file/d/1at9OFD_QoyyQkdobgdM8WW0UG9NVHvEP/view?usp=drive_link

## 4) Vérifier sa présence

ls -la datasets/brut/iris.csv

https://drive.google.com/file/d/1l88PJcENmhtlvGbHEwyPZtcSUIuNgvvv/view?usp=drive_link

## 5) Consulter son contenu

head -n 10 datasets/brut/iris.csv
wc -l datasets/brut/iris.csv

https://drive.google.com/file/d/18HBOpEq_bH7KLVq_t-caToundxsGMcQu/view?usp=drive_link


