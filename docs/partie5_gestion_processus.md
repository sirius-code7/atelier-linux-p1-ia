## 1) Créer le script print-pause.py dans scripts/

cd ~/IA_Project
nano scripts/print-pause.py

import time

for i in range(1000):
    print(i)
    time.sleep(1)

https://drive.google.com/file/d/1FKLeqZGl1TMZLjDYGCaoCaFajIw7rUx3/view?usp=drive_link

## 2) Lancer le script

En premier plan :

python3 scripts/print-pause.py

Il va afficher 0, 1, 2... toutes les secondes en boucle. Pour l'observer pendant qu'il tourne, ouvre un second terminal SSH/vagrant vers la même VM 

## 3) Observer son PID

Depuis le second terminal :

ps aux | grep print-pause

https://drive.google.com/file/d/1P76n7dGjizNCbP6uUnIM9etoaq_aOpiy/view?usp=drive_link

Note le PID affiché pour kill.

## 4) Consulter son utilisation CPU

htop

https://drive.google.com/file/d/1FCYqRPdE_J2SG4e2pKLi9QDx1DPuxlxT/view?usp=drive_link

## 5) Arrêter le processus

kill <PID>

https://drive.google.com/file/d/13dCirWo1w_vdvSraNa4ViYdJVw6ARTLM/view?usp=drive_link

## 6) Relancer en arrière-plan

cd ~/IA_Project
python3 scripts/print-pause.py &

le & à la fin lance le processus en arrière-plan et te rend la main immédiatement. Le terminal affiche un job number et un PID

https://drive.google.com/file/d/1bgOvE6R-u9WJ5r2mCj4j1W8wmpAMpRkR/view?usp=drive_link










