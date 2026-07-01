# AWS Bastion Platform

> **Projet interne : PAAAS (Platform Authentication As A Service)**

Conception d'une plateforme de bastion Open Source destinée à sécuriser les accès administrateurs aux environnements AWS de la Commission européenne.

---

# Résumé

Dans le cadre de l'arrivée des premiers environnements AWS à la Commission européenne, une nouvelle plateforme de bastion a été conçue afin de sécuriser les accès SSH des administrateurs.

L'objectif était de supprimer progressivement les accès SSH directs, tout en permettant leur contrôle, leur traçabilité et leur audit.

Cette plateforme repose sur Warpgate, une solution Open Source sélectionnée après une étude comparative du marché, et s'appuie sur une chaîne complète d'automatisation, de validation et de déploiement continu.

J'ai occupé le rôle d'architecte principal du projet, en collaboration avec le Lead Architect, le Product Owner et le référent Compliance.

---

# Contexte

L'ouverture d'environnements AWS pour les équipes clientes nécessitait une nouvelle approche des accès administrateurs.

Les accès SSH directs ne répondaient plus aux exigences de sécurité, de conformité et de traçabilité attendues.

La Commission européenne souhaitait mettre en place une plateforme :

- Open Source ;
- sans coût de licence ;
- simple à exploiter ;
- intégrable à l'écosystème existant ;
- répondant aux exigences de sécurité et de conformité.

---

# Objectifs

- Sécuriser les accès SSH administrateurs.
- Réduire les accès directs aux machines.
- Centraliser les accès.
- Permettre l'audit des connexions.
- Intégrer la plateforme dans les processus CI/CD.
- Automatiser les déploiements.
- Fournir une première plateforme exploitable (MVP).

---

# Choix de la solution

Une étude comparative de plusieurs solutions du marché avait été réalisée avant mon arrivée sur le projet.

Teleport a été écarté principalement en raison de son modèle de licence.

Boundary a été écarté en raison de sa complexité au regard des besoins de la Commission européenne.

À mon arrivée sur le projet, j'ai challengé la matrice **MoSCoW** existante avec le produit Warpgate et complété l'évaluation afin de vérifier son adéquation avec les exigences du projet.

Cette matrice, documentée dans `artifacts/docs.zip` (`docs/moscow.md`), couvre 259 exigences réparties notamment entre exigences **Must Have**, **Should Have** et **Could Have**.

La partie Compliance de la matrice a été définie par l'équipe Compliance.

La partie Core Features a été définie au travers d'échanges avec le Lead Architect et le Product Owner afin de traduire les besoins fonctionnels du MVP en critères d'évaluation concrets.

Les principaux critères retenus étaient :

- Open Source ;
- gratuit ;
- clientless ;
- simplicité d'exploitation ;
- couverture fonctionnelle des besoins.

Cette analyse a confirmé Warpgate comme la solution la plus adaptée pour la réalisation du MVP.

L'analyse MoSCoW a permis de structurer la décision en distinguant :

- les exigences indispensables pour livrer un MVP exploitable ;
- les fonctionnalités importantes mais non bloquantes ;
- les éléments pouvant être reportés après la première livraison ;
- les fonctionnalités non nécessaires au périmètre initial.

Elle a également servi de support de discussion avec le Lead Architect, le Product Owner et le référent Compliance afin d'aligner les attentes fonctionnelles, les exigences Compliance, les contraintes de sécurité et la simplicité d'exploitation.

Cette approche a permis de justifier le choix de Warpgate sur des critères concrets plutôt que sur une préférence technologique.

La matrice couvrait notamment :

- les exigences de bastion SSH ;
- les clients compatibles ;
- l'authentification locale et MFA ;
- le RBAC ;
- l'audit des accès ;
- l'export des logs ;
- la gestion des secrets ;
- les contraintes de backup, continuité et restauration ;
- les exigences de déploiement, d'exploitation et de monitoring ;
- les contraintes de licence, de support, de maturité produit et d'Open Source.

---

# Architecture

La plateforme repose notamment sur :

- AWS
- Warpgate
- HashiCorp Vault
- GitLab
- GitLab CI/CD
- Ansible
- Node-RED
- Hurl
- Prometheus
- Go

---

# Mon rôle

En tant qu'architecte principal de la plateforme, mes responsabilités comprenaient notamment :

- conception de l'architecture de la plateforme ;
- challenge de la matrice MoSCoW avec le produit Warpgate ;
- complétion de l'évaluation produit pour vérifier l'adéquation de Warpgate avec les exigences Compliance et les Core Features ;
- définition de l'architecture technique ;
- conception de la chaîne CI/CD ;
- définition de la stratégie de validation et de tests ;
- accompagnement des équipes de développement et d'exploitation ;
- rédaction de la documentation technique.

Les décisions d'architecture étaient préparées avec le Lead Architect puis discutées et validées conjointement avec le Product Owner et le référent Compliance.

---

# Réalisations

## Architecture

Conception d'une plateforme de bastion permettant de contrôler les accès administrateurs aux environnements AWS.

---

## Analyse fonctionnelle MoSCoW et Compliance

Challenge de la matrice MoSCoW avec le produit Warpgate et complétion de l'évaluation produit sur 259 exigences.

L'objectif était de vérifier que la solution pouvait couvrir le périmètre attendu du MVP sans introduire une complexité excessive.

La matrice combinait :

- les exigences Compliance définies par l'équipe Compliance ;
- les Core Features définies avec le Lead Architect et le Product Owner ;
- l'évaluation de Warpgate face aux besoins du MVP ;
- l'identification des limites acceptées, des écarts et des sujets délégués aux services de support.

Cette analyse a notamment permis :

- de comparer les besoins réels du projet avec les fonctionnalités disponibles ;
- de challenger les exigences avec les capacités réelles de Warpgate ;
- de compléter l'évaluation produit pour identifier ce qui était couvert, partiellement couvert, non couvert ou délégué ;
- d'identifier les exigences indispensables pour sécuriser les accès SSH administrateurs ;
- de distinguer les fonctionnalités nécessaires au MVP de celles pouvant être reportées ;
- de fournir un support clair pour la validation avec le Lead Architect, le Product Owner et le référent Compliance ;
- de documenter les écarts entre exigences Compliance, fonctionnalités produit et responsabilités déléguées ;
- de confirmer que Warpgate répondait au meilleur compromis entre sécurité, simplicité, Open Source et absence de coût de licence.

La matrice a également permis d'identifier clairement les limites acceptées pour le MVP, par exemple les fonctionnalités non incluses au périmètre initial ou déléguées à des services de support.

---

## CI/CD

Conception et mise en œuvre d'une chaîne CI/CD permettant notamment :

- linting ;
- génération de la documentation ;
- build ;
- déploiement automatisé ;
- création des plateformes de test ;
- tests fonctionnels ;
- validation de l'environnement d'acceptation.

---

## Automatisation

Automatisation complète du déploiement de la plateforme à l'aide d'Ansible.

Automatisation des traitements techniques via Node-RED.

Gestion des secrets avec HashiCorp Vault.

---

## Observabilité

Développement d'un exporter Prometheus en Go afin d'exposer des métriques spécifiques à la plateforme, non disponibles nativement dans Warpgate.

---

## Validation

Mise en place de tests automatisés permettant de valider le bon fonctionnement de la plateforme tout au long de la chaîne CI/CD.

Les validations couvraient notamment :

- le déploiement ;
- les tests fonctionnels ;
- la validation dans l'environnement d'acceptation.

---

# Résultats

Cette initiative a permis de livrer une première plateforme de bastion répondant aux besoins des administrateurs système.

Cette plateforme permet notamment :

- de limiter les accès SSH directs ;
- de centraliser les accès administrateurs ;
- d'améliorer la traçabilité des connexions ;
- de faciliter les audits ;
- de disposer d'une plateforme entièrement automatisée et industrialisée.

---

# Compétences démontrées

- Solution Architecture
- Cloud Architecture
- Bastion Architecture
- AWS
- Infrastructure Automation
- CI/CD
- DevSecOps
- Compliance by Design
- Security by Design
- GitLab CI/CD
- HashiCorp Vault
- Ansible
- Node-RED
- Go
- Prometheus
- Hurl

---

# Technologies

## Cloud

- AWS

## Solutions

- Warpgate

## Infrastructure

- HashiCorp Vault

## Automatisation

- GitLab CI/CD
- Ansible
- Node-RED
- Hurl

## Développement

- Go

## Observabilité

- Prometheus

---

# Références

## Entreprise

NTT DATA

## Client

Commission européenne

## Période

2024 - En cours

## Documents associés

- `artifacts/docs.zip`
- `artifacts/docs.zip/docs/moscow.md`
- `artifacts/docs.zip/docs/PAAAS_Project_Overview.md`
- `artifacts/docs.zip/docs/PAAAS_CICD.md`
- `artifacts/docs.zip/docs/PAAAS_access_design.md`
- `artifacts/docs.zip/docs/PAAAS_LMA_design.md`
