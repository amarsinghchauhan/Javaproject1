# TravisCI_Experimentation
This repository is a 4/5hours homework for testing the CI/CD software named Travis CI.
it's supposed to create a CI for a random java project.


## Documentation du Pipeline

### Objectifs

On souhaite établir un pipeline de livraison : une serie d'etape Build/Test jusqu'a demander une validation 
manuel de la part d'un utilisateur avant le deploiement sur la branche master.

![Pipeline](https://github.com/iesseddik/TravisCI_Experimentation/blob/master/pipeline.png?raw=true)


Lien du depôt de code du projet sur github : https://github.com/iesseddik/TravisCI_Experimentation (vous y êtes)

Lien d'acces a l'outil de CI/CD : https://travis-ci.org/iesseddik/TravisCI_Experimentation

### Fonctionnement de Travis

Pour regler les fonctionnalités de l'outil Travis, il existe un fichier nommé ".travis.yml" que l'on doit placer dans le depôt du code pour parser et identifier sa structure.
Ce dernier contient des instructions obligatoire à mentionner et d'autres qui sont optionnelles. Les dependances Maven sont automatiquement par defaut.

Dans notre fichier .yml on y trouve par exemple:

-language: java 
(pour indiquer le langage du code source du projet)

-sudo: false 
(pour configurer les droit utilisateur)

-install: true 
(on indique ici la valeur a true pour sauter l'etape)

script:mvn compile (ici on entre les commandes shell a éxecuter, par exemple pour la compilation).

Ainsi, a chaque pull/merge Request sur ce depôt, Travis se chargera de la bonne execution de chaque etape du pipeline decrit dans le fichier yml.

### Conclusion

Ayant depassé les 5h de travaille je n'ai pas encore pu trouver comment executer le deploiement avant de pouvoir le faire manuellement.