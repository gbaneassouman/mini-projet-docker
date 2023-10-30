# Mini Projet Docker (students list)
<div align="center">
  <img src="screenshots/docker.png"/>
#
</div>
#
Ce projet a été réalisé dans le cadre de mon parcous Devops au BootCamp 15 de EAZYTraining avec [Dirane Tafen](https://github.com/diranetafen/).
Il s'agit d'une simple application web développé en PHP et une API fait avec Flask qui permet de repertorier les étudiants .
# 
Dans le cadre de ce projet dont les spécifications techniques sont à retrouver [ici](https://github.com/diranetafen/student-list.git "here"),il m'a été demandé d'aider POZOS à déployer son application

L'application à déployer comporte deux modules :

- Le premier module est une API REST (avec authentification de base requise) qui envoie la liste de souhaits de l'étudiant basée sur un fichier JSON.

- Le deuxième module est une application web écrite en HTML + PHP qui permet à l'utilisateur final d'obtenir une liste d'étudiants.

#
Les objectifs de cet examen pratique sont de garantir que vous êtes capable de gérer une infrastructure Docker.
Vous serez donc évalué sur les points suivants.



- améliorer un processus de déploiement d'applications existant
- versionner la version de votre infrastructure
- aborder les meilleures pratiques lors de la mise en œuvre de l'infrastructure Docker
- Infrastructure en tant que code
## Context

**POZOS** est une société informatique située en France et développe des logiciels pour le lycée.
Le département d'innovation souhaite perturber l'infrastructure existante pour garantir qu'il peut être évolutif, facilement déployé avec un maximum d’automatisation.

**POZOS** souhaite que vous créiez un POC pour montrer comment **Docker** peut vous aider et à quel point cette technologie est efficace.

Pour ce POC, **POZOS** vous fournira une application et souhaitera que vous construisiez une infrastructure de « découplement » basée sur **POZOS**.

Actuellement, l'application s'exécute sur un seul serveur avec n'importe quelle évolutivité et n'importe quelle haute disponibilité.

Lorsque **POZOS** a besoin de déployer une nouvelle version, à chaque fois, quelque chose tourne mal.

En conclusion, POZOS a besoin d'agilité sur sa ferme logicielle.
## Infrastructure

Pour ce POC, vous n’utiliserez qu’une seule machine sur laquelle Docker sera installé.

Le Build et le Déploiement se feront sur cette machine.

POZOS vous recommande d'utiliser le système d'exploitation centos7.6 car c'est le plus utilisé dans l'entreprise.



## Application

L'application sur laquelle vous allez travailler s'appelle *"student_list"*, cette application est très basique et permet à POZOS d'afficher la liste des étudiants avec leur âge.

*student_list* comporte deux modules :

Le premier module est une **API REST** (avec authentification de base requise) qui envoie la liste de souhaits de l'étudiant basée sur un fichier JSON

Le deuxième module est une application web écrite en **HTML + PHP** qui permet à l'utilisateur final d'obtenir une liste d'étudiants.

Votre travail consiste à créer un conteneur pour chaque module et à les faire interagir les uns avec les autres.

Le code source de l'application peut être trouvé [ici](https://github.com/diranetafen/student-list.git)

Les fichiers que vous devez fournir (dans votre livraison) sont **Dockerfile** et **docker-compose.yml** (actuellement les deux sont vides)

Il est maintenant temps de vous expliquer le rôle de chaque fichier :

docker-compose.yml : pour lancer l'application (API et web app)
Dockerfile : le fichier qui sera utilisé pour construire l'image API (des détails seront donnés)
student_age.json : contient le nom de l'étudiant avec son âge au format JSON
student_age.py : contient le code source de l'API en python
index.php : page PHP où l'utilisateur final sera connecté pour interagir avec le service afin de - lister les étudiants avec leur âge. Vous devez mettre à jour la ligne suivante avant d'exécuter le conteneur de site Web pour adapter api_ip_or_name et port


# Bésoins

My job is to :
1) Use Virtualbox as a hypervisor for the virtual machine creation
2) Use Vagrant as infrastructure provisioner to manage the VM
3) Install Docker and Docker-compose on the VM
4) Build one container for each module (Backend & Fronted)
5) Make the containers interact with each other
6) Provide a private registry to store images

## Demo

voir [ici](https://github.com/diranetafen/student-list.git "here")


## 🚀 à propos de moi

Session           : Bootcamp DevOps N°15 de EAZYTraining

Période           : Septembre - Novembre

Prénoms & Nom : Assouman GBANE

LinkedIn          : https://www.linkedin.com/in/gbane-assouman-4ab183123/
