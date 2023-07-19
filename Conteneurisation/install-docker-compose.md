[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=30&duration=3000&pause=600&width=435&lines=Installation+Docker-Compose)]
# Debian & Ubuntu

1 - Mise à jour de l'index des paquets apt :

```bash
sudo apt update
```


2 - Utilisez curl pour télécharger le repo de Docker Compose dans le répertoire /usr/local/bin/docker-compose :

```bash
sudo curl -L "https://github.com/docker/compose/releases/download/v2.20.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
Pour modifier la version à installer modifier "v2.20.0" par le numéro de version que vous avez choisi.


3 - Donner la permission et rendre le fichier téléchargé exécutable :

```bash
sudo chmod +x /usr/local/bin/docker-compose
```


4 - Vérifier la version de docker-compose pour s'assurer que l'installation a réussi :

```bash
docker-compose --version
```
Output :
```bash
Docker Compose version v2.0.1
```
