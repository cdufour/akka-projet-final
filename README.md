# Akka Devops - Projet final - 3 jours: 18, 21 et 22 février 2022
## Présentation
L'entreprise Nuvola, start-up ambitieuse, a développé une application nommée "nuvoquizz".
Il s'agit d'une application web réalisée en nodejs et permettant au client de tester
ses connaissances sur différents domaines via un jeu de question/réponse oui/non.

- Démo de l'application.

Nuvola souhaite développer rapidement de nouvelles fonctionnalités, et, dans cette optique, elle prévoit de recruter des développeurs supplémentaires.
Cependant, ne disposant pas de locaux physiques pour accueillir les développeurs,
elle souhaite leur fournir des machines virtuelles.

Votre mission chez Nuvola: 

__Machines de dev__
Permettre de fournir rapidement une machine virtuelle à un développeur intégrant le projet.
Ces machines devront être approvisionnées chez AWS. 
Le développeur se connectera à sa machine par ssh.
L'administrateur pourra contrôler les machines dev pour un exécuter des tâches (installation, copie de fichiers, ...)
Une machine de dev devra disposer d'une copie du dépôt local de l'application

__L'application__
A terme, Nuvola souhaiterait migrer son environnement de production vers Kubernetes.
Vous aurez en charge la conteneurisation de l'application. La technologie retenue: Docker.

Souhaitant appliquer les principes du Devops, Nuvola vous charge également d'automatiser au maximum
le processus de redéploiement.
Le choix s'est porté sur Jenkins comme serveur d'automatisation.
Vous devrez construire la pipeline permettant de
  récupérer le code source
  construire une nouvelle image
  tester le lancement de l'application
  appliquer les tests unitaires fournis
  publier l'image sur un dépôt (registry) public ou privé

L'application ayant vocation à être déployée dans un cluster k8s, vous êtes également
chargé de produire les manifestes yaml permettant d'automatiser ce déploiement.


## Notes 
### Modalités de travail
Dans le cadre de ce projet, vous devez convoquer une grande partie des connaissances accumulées, des concepts et des outils abordés durant le cursus.

Vous serez répartis en 3 groupes.

- Groupe 1: 
- Groupe 2: 
- Groupe 3: 

Vous présenterez le projet l'après-midi du dernier jour.
Durée de la présentation: environ 30 min par groupe.

Vous devrez démontrer le bon fonctionnement de votre architecture et justifier vos choix techniques.
