## Préparer : le fichier de doc

Commandes : touch docs/partie3_utilisateurs_permissions.md

## Bloc 1 : Créer les 5 utilisateurs

sudo useradd -m alice
sudo useradd -m bob
sudo useradd -m charles
sudo useradd -m diane
sudo useradd -m eva

note: -m crée automatiquement le répertoire personnel (/home/alice, etc.).

https://drive.google.com/file/d/1sKK9NArMVCp0FKUxTEXHGEScyRfHtryH/view?usp=drive_link

### Créer un mot de passe pour chacun :

sudo passwd alice
sudo passwd bob
sudo passwd charles
sudo passwd diane
sudo passwd eva

https://drive.google.com/file/d/1hu2XNVkpzruDjIG3IDfGJlfSJwO74-uy/view?usp=drive_link

### Vérifier que le répertoire personnel a bien été créé :

ls -la /home

https://drive.google.com/file/d/1rSjd7rL-N1mQcqZo8h45XVFzbumptt_P/view?usp=drive_link

### Afficher l'UID et les groupes de chacun :

id alice
id bob
id charles
id diane
id eva

https://drive.google.com/file/d/1heTQ7CCJwZwPlr2tEBWY1671-VCuff9C/view?usp=drive_link

## Bloc 2 : Créer les groupes

sudo groupadd data
sudo groupadd models
sudo groupadd api
sudo groupadd mlops
sudo groupadd interns

https://drive.google.com/file/d/1qEXj1QYEpS_5upsDzHGCwCauiFjXHNlG/view?usp=drive_link

## Bloc 3 : Ajouter les utilisateurs dans leurs groupes

(fonction → groupe logique) :

sudo usermod -aG data alice        # Data Scientist
sudo usermod -aG data,models bob   # Data Engineer
sudo usermod -aG api charles       # Développeur API
sudo usermod -aG mlops diane       # MLOps Engineer
sudo usermod -aG interns eva       # Stagiaire

https://drive.google.com/file/d/155cDDZpeIz44ZSQmtTWgsBr2of4zuWcn/view?usp=drive_link

note: -aG = ajoute (append) aux groupes secondaires sans écraser les groupes existants.

## Bloc 4 : Créer les sous-dossiers à la racine du projet

cd ~/IA_Project
mkdir -p api backup documentation shared

https://drive.google.com/file/d/1j1SCS8PlOcgLz3v27-k3zLKp8nhAkuGf/view?usp=drive_link

## Bloc 5 : Attribution des propriétaires (chown)

sudo chown alice datasets
sudo chown alice models
sudo chown charles api
sudo chown diane logs
sudo chown diane backup
sudo chown bob documentation
sudo chown root shared

https://drive.google.com/file/d/1p_daM1krXJPwjbObhZ0246x6PKq7y9M9/view?usp=drive_link

## Bloc 6 : Attribution des groupes (chgrp)

sudo chgrp data datasets
sudo chgrp data models
sudo chgrp api api
sudo chgrp mlops logs
sudo chgrp mlops backup
sudo chgrp data documentation
sudo chgrp data shared

https://drive.google.com/file/d/1jd9voHSj0aqdEM_FLVuqtlchKgKta8Xn/view?usp=drive_link

## Bloc 7 : Permissions exactes (chmod)

note: correspondances rwx → chiffre : rwx=7, r-x=5, r--=4, ---=0.

Dossier	Propriétaire	Groupe	Autres	Octal
datasets	rwx	rwx	---	770
models		rwx	r-x	---	750
api		rwx	rwx	---	770
logs		rwx	r--	---	740
backup		rwx	---	---	700
docu		rwx	r--	r--	744
shared		rwx	rwx	r-x	775

Commandes: 

sudo chmod 770 datasets
sudo chmod 750 models
sudo chmod 770 api
sudo chmod 740 logs
sudo chmod 700 backup
sudo chmod 744 documentation
sudo chmod 775 shared

https://drive.google.com/file/d/1HwPnXqenePbrHI2fhkz0Qow-2EHS2O8D/view?usp=drive_link









