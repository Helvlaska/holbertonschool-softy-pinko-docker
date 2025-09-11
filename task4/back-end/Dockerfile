# Basé sur la dernière version de Ubuntu
FROM ubuntu:latest

# Mise à jour APT
RUN apt-get update
RUN apt-get upgrade -y

# Installation de python3 et pip
RUN apt-get install -y python3 python3-pip

# Corrige le problème d'environnement géré
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Installation de Flask
RUN pip3 install flask

# Installation de Flask-cors
RUN pip3 install flask-cors

# Définition du répertoire de travail dans le container
WORKDIR /app

# Copier les fichiers/dossiers de l'hôte vers l'image
COPY ./api.py /app/api.py

# Expose le port utilisé par Flask
EXPOSE 5252

# Imprime "Hello, World!" dans le terminal
CMD ["python3", "api.py"]
