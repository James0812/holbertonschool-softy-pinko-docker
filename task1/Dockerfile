FROM ubuntu:latest

RUN apt-get update
RUN apt-get upgrade -y

# Installer Python3 et pip3
RUN apt-get install -y python3 python3-pip

# Contourner le problème "externally managed" sur Ubuntu récent
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Installer Flask via pip3
RUN pip3 install flask

# Définir le dossier de travail
WORKDIR /app

# Copier api.py dans le container
COPY ./api.py /app/api.py

# Lancer le serveur Flask au démarrage
CMD ["python3", "api.py"]
