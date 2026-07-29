
## 1) Créer la config logrotate pour le projet

sudo touch /etc/logrotate.d/ia_project
sudo nano /etc/logrotate.d/ia_project

https://drive.google.com/file/d/1BaqPC_OcSvh327UprbqYoNS7ug0e2fP1/view?usp=drive_link

### Contenu
 
"/home/vagrant/IA_Project/test_setup/logs/*.log {
    daily
    rotate 7
    compress
    missingok
    notifempty
    copytruncate
}"

### Description 

daily : rotation quotidienne
rotate 7 : garde 7 anciennes versions
compress : compresse les anciens logs (.gz)
missingok : ne plante pas si le fichier n'existe pas
notifempty : ne fait pas de rotation si le fichier est vide
copytruncate : copie puis vide le fichier original sans interrompre un process qui écrirait dedans (important pour des logs actifs)

2) Test

sudo logrotate -f /etc/logrotate.d/ia_project
ls -la ~/IA_Project/test_setup/logs/

https://drive.google.com/file/d/1GL2v2Fcq9lYJokzaxV0EMNoqy-h5_Xc5/view?usp=drive_link

https://drive.google.com/file/d/1YxqUvCRT52PBgI9_FDFT1eIMr4RhPNf6/view?usp=drive_link



