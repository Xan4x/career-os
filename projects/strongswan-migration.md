# StrongSwan Migration (Pulse Away)

> Conception et déploiement d'une nouvelle plateforme VPN Open Source basée sur StrongSwan afin de remplacer progressivement la partie IPsec des solutions Pulse Secure / Ivanti Connect Secure.

---

# Résumé

Le projet **Pulse Away**, lancé en 2021, a pour objectif de remplacer progressivement la partie IPsec de la plateforme Remote Access historique par une solution Open Source basée sur StrongSwan.

Cette initiative répond à plusieurs enjeux stratégiques : réduction des coûts de licences, diminution de la dépendance aux solutions propriétaires, amélioration de la sécurité face aux vulnérabilités récurrentes et industrialisation de la plateforme.

Après une première phase consacrée à la migration des utilisateurs Corporate, j'ai pris en charge l'architecture et la migration des populations Administrateurs ainsi que plusieurs chantiers structurants autour de l'automatisation et de la modernisation de la plateforme.

---

# Contexte

La plateforme Remote Access historique reposait principalement sur Pulse Secure / Ivanti Connect Secure.

Malgré les nombreuses améliorations apportées lors du projet **Remote Access Platform Evolution**, plusieurs limites subsistaient :

- coûts importants des licences ;
- dépendance à une solution propriétaire ;
- vulnérabilités critiques (CVE) publiées régulièrement ;
- besoin d'améliorer l'automatisation ;
- volonté de standardiser la plateforme.

La Commission européenne a donc décidé de développer une nouvelle plateforme VPN IPsec basée sur StrongSwan.

---

# Objectifs

- Remplacer progressivement la partie IPsec de Pulse Secure.
- Réduire les coûts de licences.
- S'appuyer sur une solution Open Source.
- Améliorer la sécurité de la plateforme.
- Standardiser les déploiements.
- Industrialiser l'automatisation.
- Moderniser les outils d'exploitation.

---

# Architecture

La nouvelle plateforme repose notamment sur :

- StrongSwan (IPsec)
- Linux
- F5 Load Balancer
- PKI interne de la Commission européenne
- NetBox (Source of Truth, IPAM, Inventory)
- AWX
- GitLab
- GitLab CI/CD

Cette architecture introduit une nouvelle chaîne d'automatisation et de déploiement plus moderne que celle utilisée sur la plateforme historique.

---

# Mon rôle

À partir de 2022/2023, j'ai pris en charge plusieurs chantiers majeurs autour de cette nouvelle plateforme.

Mes responsabilités comprenaient notamment :

- conception de l'architecture des populations Administrateurs ;
- migration des populations Administrateurs ;
- migration de la CMDB vers NetBox ;
- intégration de NetBox comme nouvelle source de vérité ;
- intégration de l'automatisation avec AWX ;
- migration des dépôts Git locaux vers GitLab ;
- mise en place des premiers pipelines GitLab CI/CD ;
- rédaction de la documentation technique ;
- accompagnement des équipes Network Security.

Ces responsabilités ont marqué ma transition progressive vers un rôle d'IT Solutions Architect, officialisé début 2024.

---

# Réalisations

## Architecture

Participation à la conception de la nouvelle plateforme VPN basée sur StrongSwan.

Définition des architectures destinées aux populations Administrateurs.

---

## Automatisation

Modernisation de la chaîne d'automatisation de la plateforme.

Principales évolutions :

- migration de la CMDB historique vers NetBox comme Source of Truth, IPAM et Inventory ;
- intégration d'AWX pour le provisioning, la configuration, les mises à jour et les tests des plateformes ;
- migration des dépôts Git onprem vers GitLab ;
- mise en place des premiers pipelines GitLab CI/CD (linting dans un premier temps) ;

---

## Validation de conformité

Développement de tests de conformité permettant de vérifier automatiquement la plateforme après un déploiement ou un changement.

Ces contrôles vérifiaient notamment :

- la bonne application de la configuration ;
- le chargement correct des certificats ;
- la présence des éléments attendus ;
- la conformité avec les standards définis.

Cette approche permettait de détecter rapidement les erreurs de configuration avant leur mise en production.

---

# Résultats

Cette initiative a permis :

- de lancer la transition vers une plateforme VPN Open Source ;
- de moderniser les outils d'exploitation ;
- de standardiser les déploiements ;
- d'améliorer l'automatisation ;
- de préparer l'industrialisation des futurs déploiements ;
- d'accompagner la migration progressive des différentes populations d'utilisateurs.

---

# Compétences démontrées

- Architecture VPN
- VPN IPsec
- Open Source
- Linux
- PKI
- Infrastructure Automation
- AWX
- GitLab
- GitLab CI/CD
- NetBox
- Tests de conformité
- Standardisation
- Migration de plateforme

---

# Technologies

## Solutions

- StrongSwan

## Infrastructure

- Linux
- PKI
- NetBox

## Automatisation

- AWX
- GitLab
- GitLab CI/CD
- Bash

## Clients

- Windows
- Linux
- macOS

## Clients VPN

- Linux (client StrongSwan natif)
- Windows (client IPsec natif)
- macOS (client IPsec natif)

---

# Références

## Entreprise

NTT DATA

## Client

Commission européenne

## Période

2021 - En cours