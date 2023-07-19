[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=30&duration=3000&pause=600&width=435&lines=Installation+Docker-Compose)](https://git.io/typing-svg)

# Debian & Ubuntu

1 - Mise à jour de l'index des paquets apt :

```bash
$ sudo apt update
```

2 - Utilisez curl pour télécharger le repo de Docker Compose dans le répertoire /usr/local/bin/docker-compose :

```bash
$ sudo curl -L "https://github.com/docker/compose/releases/download/v2.20.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
Pour modifier la version à installer modifier "v2.20.0" par le numéro de version que vous avez choisi.