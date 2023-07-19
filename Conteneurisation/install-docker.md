[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=30&duration=3000&pause=600&width=435&lines=Installation+Docker)]

# Debian & Ubuntu

1 - Mise à jour de l'index des paquets apt et des paquets d'installation pour permettre à apt d'utiliser un dépôt via HTTPS :

```bash
sudo apt update
sudo apt-get install ca-certificates curl gnupg
```

2 - Ajouter la clé GPG officielle de Docker :

```bash
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg
```

3 - Utilisez la commande suivante pour configurer le repository :

```bash
echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/debian \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

4 - Mise à jour de l'index des paquets apt :

```bash
sudo apt-get update
```

5 - Installer Docker Engine, containerd et Docker Compose :

```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

6 - Vérifiez que l'installation de Docker Engine est réussie en exécutant l'image hello-world :

```bash
sudo docker run hello-world
```
Cette commande télécharge une image de test et l'exécute dans un conteneur. Lorsque le conteneur s'exécute, il affiche un message de confirmation et se termine.
