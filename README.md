# Mini Projet Docker (students list)
<div align="center">
  <img src="screenshots/docker.png"/>
</div>

#

Ce projet a été réalisé dans le cadre de mon parcous Devops au BootCamp n°15 de **EAZYTraining** avec [Dirane Tafen](https://github.com/diranetafen/).

## Objectifs
Les objectifs de cet examen pratique sont de garantir que vous êtes capable de gérer une infrastructure **Docker**.
Vous serez donc évalué sur les points suivants.

- Améliorer un processus de déploiement d'applications existant
- Versionner la release de l' infrastructure
- Aborder les meilleures pratiques lors de la mise en œuvre de l'infrastructure **Docker**
- Infrastructure en tant que code
- Mettre en place un Registre privé
## Context

**POZOS** est une société informatique située en France et développe des logiciels pour les lycées.
Le département de l'innovation souhaite perturber l'infrastructure existante pour garantir qu'il peut être évolutif, facilement déployé avec un maximum d’automatisation.

**POZOS** souhaite que vous créiez un POC pour montrer comment **Docker** peut  aider et à quel point cette technologie est efficace.

Pour ce POC, **POZOS** vous fournira une application et souhaite que vous construisiez une infrastructure de « découplement » basée sur **Docker**.

Actuellement, l'application s'exécute sur un seul serveur sans évolutivité et sans haute disponibilité.

Lorsque **POZOS** a besoin de déployer une nouvelle version, à chaque fois, quelque chose tourne mal.

En conclusion, **POZOS** a besoin d'agilité sur sa ferme logicielle.

## Infrastructure

Pour ce POC, vous n’utiliserez qu’une seule machine sur laquelle Docker sera installé.

Le Build et le Déploiement se feront sur cette machine.

POZOS vous recommande d'utiliser le système d'exploitation **centos7.6** car c'est le plus utilisé dans l'entreprise.

## Application

L'application sur laquelle vous allez travailler s'appelle *"student_list"*, cette application est très basique et permet à POZOS d'afficher la liste des étudiants avec leur âge.
*student_list* comporte deux modules :

- Le premier module est une **API REST** (avec authentification de base requise) qui envoie la liste de souhaits de l'étudiant basée sur un fichier JSON

- Le deuxième module est une application web écrite en **HTML + PHP** qui permet à l'utilisateur final d'obtenir une liste d'étudiants.

Votre travail consiste à créer un conteneur pour chaque module et à les faire interagir les uns avec les autres.

Le code source de l'application peut être trouvé [ici](https://github.com/diranetafen/student-list.git).    

Les fichiers que vous devez fournir (dans votre livraison) sont le **Dockerfile** et un **docker-compose.yml** 

### Rôles des différents fichiers :

**student_age.json** : contient le nom des étudiants avec leur âge au format JSON
**student_age.py** : contient le code source de l'API en python  
**index.php** : la page PHP où l'utilisateur final sera connecté pour interagir avec le service afin de - lister les étudiants avec leur âge. 

Vous devez mettre à jour la ligne suivante avant d'exécuter le conteneur de site Web pour adapter api_ip_or_name et port

voici l'url : $url = 'http://<api_ip_or_name:port>/pozos/api/v1.0/get_student_ages';
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
