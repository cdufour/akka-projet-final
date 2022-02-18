# Akka Devops - Projet final - 3 jours: 18, 21 et 22 février 2022
## Présentation
L'entreprise Nuvola, start-up ambitieuse, est en train de développer une application nommée *nuvolapp* 
Il s'agit d'une application web réalisée en nodejs/mongodb. 
Cette application devra offrir au client la possibilité d'enregistrer ses dépenses. 

- [Démo de l'application](http://ec2-3-71-40-139.eu-central-1.compute.amazonaws.com:4000)

Nuvola souhaite développer rapidement de nouvelles fonctionnalités, et, dans cette optique, elle prévoit de recruter des développeurs supplémentaires. 
Cependant, ne disposant pas de locaux physiques pour accueillir les développeurs, 
elle souhaite leur fournir des machines virtuelles déjà pré-configurées.

## Votre mission chez Nuvola comporte deux tâches principales:

### Approvisionnement et configuraiton d'une machine de dev
Permettre de fournir rapidement une machine virtuelle à un développeur intégrant le projet.  
Cette machine devra être approvisionnée chez AWS.  
Le développeur pourra se connecter à sa machine par ssh grâce à une clé rsa privée que vous pourrez lui transmettre.  
L'administrateur pourra contrôler les machines de dev afin d'exécuter des tâches (installation, copie de fichiers, création de compte utilisateur, etc.)   
La machine devra disposer d'un compte utilisateur nommé selon le prénom de l'utilisateur, bas de casse, sans accent. Exemple: Jean-Rachid => *jean-rachid*.  
Le hostname de la machine devra être nommée *nuvola*.  
Ainsi, si Jean-Rachid se connecte à sa VM, son bash devra lui apparaître comme suit:  
*jean-rachid@nuvola:$*  

La machine devra disposer d'un groupe *developers* 
L'utilisateur devra appartenir au groupe *developers* ainsi qu'au groupe *docker* 
Une machine de dev devra disposer de: 
- copie du dépôt local de l'application nuvolapp (placée dans le home directory de l'utilisateur). L'utilisateur pourra "pousser" des _commits_ sur le dépôt.
- nodejs
- npm
- docker
- images docker suivantes: node:14-alpine, mongo:4.4

### Conteneurisation et déploiement de l'application en continue
A terme, Nuvola souhaiterait migrer son environnement de production vers Kubernetes. 
Vous aurez en charge la conteneurisation (Docker) de l'application. 

Souhaitant appliquer les principes du Devops, Nuvola vous charge également d'automatiser au maximum
le processus de (re)déploiement. 
Le choix s'est porté sur Jenkins comme serveur d'automatisation. 
Vous devrez construire la pipeline permettant de: 
- récupérer le code source
- construire une nouvelle image
- tester le lancement de l'application
- appliquer les tests unitaires (en option, si fournis)
- publier l'image sur un dépôt (registry) public ou privé

Toutes les 3 heures (choisir une fréquence moindre durant la phase de test) la pipeline devra se redéclencher afin de rebuilder l'application en cas de changement sur le dépôt.  

L'application ayant vocation à être déployée dans un cluster k8s, vous êtes également chargé de produire les manifestes yaml permettant d'automatiser ce déploiement.


## Notes

### Livrables attendus
- Script ou playbook de lancement d'une instance ec2
- Playbook de configuration d'une machine de dev
- Dockerfile de l'application nuvolapp
- Lien vers votre repository d'image docker (par exemple, vers le docker hub)
- Jenkinsfile de la pipeline d'intégration continue
- Manifestes kubernetes de déploiement de l'application

### Technogies à employer
AWS, Docker, Jenkins, Kubernetes, Ansible

### Modalités de travail
Dans le cadre de ce projet, vous devez convoquer une grande partie des connaissances accumulées, des concepts et des outils abordés durant le cursus.

Vous serez répartis en 3 groupes.

- Groupe 1: Amine, Franck, Mouaad
- Groupe 2: Jérôme, Aboubakr, Charly
- Groupe 3: Bruno, Maxime, François

Vous présenterez le projet l'après-midi du dernier jour.
Durée de la présentation: environ 30 min par groupe.

Vous devrez démontrer le bon fonctionnement de votre architecture et justifier vos choix techniques.
