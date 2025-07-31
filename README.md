# github_action
Terminologie Clé à Comprendre
Workflow :

Fichier YAML (.yml) qui définit le processus d'automatisation

Stocké dans .github/workflows/

Peut contenir plusieurs jobs

Job :

  Ensemble d'étapes qui s'exécutent sur le même runner
  
  Exemple : build, test, deploy
  
  S'exécutent en parallèle par défaut
  
Step :

  Tâche individuelle dans un job
  
  Peut exécuter une commande shell ou une action

Action :

  Brique réutilisable (ex: checkout, setup-java)
  
  Peut être écrite par la communauté ou vous-même

Runner :

  Machine qui exécute vos workflows
  
  Soit GitHub-hosted (ubuntu, windows, macos)
  
  Soit self-hosted (votre propre serveur)

Artifact :

  Fichiers produits par un job et conservés
  
  Exemple : fichier JAR, rapport de tests

Secret :

  Variables sensibles stockées de manière sécurisée
  
  Accessibles via ${{ secrets.NOM_SECRET }}

Étapes pour Automatiser le Déploiement
1. Configuration Initiale
Créer le dossier .github/workflows à la racine du projet

Créer un fichier YAML (ex: deployment.yml)
