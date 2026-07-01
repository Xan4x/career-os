# Remote Access Platform Evolution

> Évolution progressive de la plateforme Remote Access de la Commission européenne afin de répondre aux nouveaux enjeux de capacité, de sécurité, de conformité et d'exploitation.

---

# Résumé

Entre 2016 et 2021, la plateforme Remote Access a connu plusieurs évolutions majeures motivées par l'augmentation continue des besoins métiers, les exigences de sécurité et l'évolution des infrastructures.

Initialement basée sur des appliances physiques, la plateforme a progressivement évolué vers une architecture virtualisée, hautement disponible et largement automatisée.

Cette évolution a été accélérée par plusieurs événements majeurs, notamment les attentats de Bruxelles, la crise sanitaire liée au COVID-19 et la multiplication des vulnérabilités critiques affectant les solutions VPN.

Au cours de cette initiative, j'ai progressivement évolué d'un rôle d'ingénieur réseau vers celui de référente technique du service Remote Access, puis d'IT Solutions Architect.

---

# Contexte

La plateforme Remote Access permettait aux collaborateurs de la Commission européenne, aux agences européennes ainsi qu'aux prestataires externes d'accéder de manière sécurisée aux ressources internes.

Elle devait répondre à plusieurs contraintes :

- haute disponibilité ;
- montée en charge importante ;
- exploitation 24/7 ;
- exigences fortes de sécurité ;
- conformité ;
- maîtrise des coûts ;
- limitation des interruptions de service.

Au fil des années, plusieurs événements sont venus accélérer son évolution :

- augmentation progressive du nombre d'utilisateurs ;
- attentats de Bruxelles (2016) ;
- préparation confidentielle du télétravail avant le COVID-19 (2020) ;
- explosion du nombre de connexions lors du confinement ;
- multiplication des CVE affectant les appliances VPN.

---

# Environnement

## Type

On-Premises

Infrastructure virtualisée VMware.

Plateforme critique utilisée quotidiennement par plusieurs dizaines de milliers d'utilisateurs, avec une capacité redimensionnée pendant la période COVID pour supporter jusqu'à environ 40 000 utilisateurs simultanés.

Données d'échelle issues de la présentation interne :

- population Remote Access d'environ 40 000 utilisateurs ;
- 40 000 licences VPN et environ 300 accès RDP ;
- infrastructure répartie sur deux sites ;
- première année COVID : par site, 1 appliance physique, 3 VM pour les accès Private, 2 VM Corporate avec authentification SAML et 13 VM Corporate avec authentification par certificat ;
- infrastructure stabilisée : 26 VM Ivanti, 12 profils / environnements distincts et 8 VM StrongSwan.

---

# Évolution de la plateforme

## Phase 1 — Infrastructure historique

La plateforme reposait initialement sur des appliances physiques.

Les différents profils utilisateurs étaient principalement regroupés sur les mêmes équipements, à l'exception des profils les plus sensibles disposant déjà d'une infrastructure dédiée.

---

## Phase 2 — Virtualisation

Afin d'améliorer la scalabilité et la rapidité de déploiement, la plateforme a progressivement été virtualisée.

Cette évolution a nécessité un important travail de conception autour :

- du dimensionnement des machines virtuelles ;
- de la capacité maximale par appliance ;
- du nombre d'instances nécessaires ;
- de l'architecture Load Balancing ;
- des profils utilisateurs.

Les recommandations constructeur ont servi de point de départ avant d'être adaptées grâce aux retours d'expérience en production.

---

## Phase 3 — COVID

La crise sanitaire a profondément modifié les besoins de la plateforme.

Un projet préparatoire a été lancé de manière confidentielle quelques jours avant le confinement afin d'anticiper l'augmentation massive du télétravail.

La plateforme a été redimensionnée afin de supporter jusqu'à environ 40 000 utilisateurs simultanés.

Cette montée en charge s'est appuyée sur :

- la mise en place de Load Balancers F5 ;
- la création d'appliances virtuelles sur VMware ;
- l'utilisation de licences ICE / In Case of Emergency ;
- la séparation des populations Private, Corporate SAML et Corporate certificate ;
- un suivi quotidien de la capacité, des licences, des vCPU, du transport VPN, du CPU Ready et des drops réseau.

---

## Phase 4 — Industrialisation

L'augmentation du nombre de machines virtuelles et la multiplication des environnements ont rapidement rendu l'administration manuelle impossible.

Une chaîne de provisioning a progressivement été mise en place afin d'automatiser :

- le déploiement ;
- la configuration ;
- l'enregistrement dans les différents services ;
- les mises à jour ;
- le monitoring.

Cette automatisation s'appuyait notamment sur une CMDB, Python, Bash et Ansible.

---

## Phase 5 — Security Hardening

La multiplication des vulnérabilités critiques publiées sur les solutions VPN a conduit à renforcer significativement la sécurité de la plateforme.

Plusieurs mécanismes ont été mis en place afin d'améliorer :

- la conformité ;
- les contrôles d'intégrité ;
- la segmentation des environnements ;
- la rapidité de reconstruction des appliances compromises.

---

# Mon rôle

Au cours de cette initiative, j'ai progressivement pris le rôle de référente technique de la plateforme Remote Access.

Je participais aux décisions d'architecture aux côtés de l'architecte de l'équipe et constituais le principal point d'escalade technique pour les équipes Network Security.

Mes principales responsabilités étaient :

- participation au design de la plateforme ;
- définition du dimensionnement des machines virtuelles ;
- participation aux calculs de capacité ;
- conception des profils utilisateurs ;
- participation à l'architecture Load Balancing ;
- automatisation du provisioning ;
- migration des plateformes ;
- rédaction de la documentation ;
- définition des procédures ;
- réalisation des tests ;
- support technique.

---

# Réalisations

## Architecture

Participation à la conception de la nouvelle architecture Remote Access.

Travail sur :

- le dimensionnement des appliances virtuelles ;
- le nombre d'instances ;
- la capacité maximale ;
- les profils utilisateurs ;
- la segmentation des environnements ;
- l'équilibrage de charge.
- l'évolution vers une infrastructure multi-sites composée notamment de 26 VM Ivanti, 12 profils / environnements et 8 VM StrongSwan.

---

## Automatisation

Participation au développement de la chaîne d'automatisation de la plateforme.

Développement de scripts Python et Bash permettant notamment :

- l'interfaçage avec la CMDB ;
- le provisioning automatique ;
- la génération des configurations ;
- l'automatisation des opérations d'administration ;
- le déploiement via Ansible.

L'automatisation a permis de réduire le temps de déploiement d'une nouvelle appliance d'environ deux heures à moins d'une heure selon les opérations réalisées.

---

## Provisioning

Participation à la conception d'un processus entièrement automatisé permettant :

- le déploiement des appliances ;
- leur configuration ;
- leur intégration dans l'infrastructure ;
- leur mise à jour ;
- leur supervision.

---

## Security Hardening

Participation au renforcement de la sécurité de la plateforme.

Mise en œuvre des Integrity Checks publiés par Ivanti.

Développement d'une chaîne automatisée permettant :

- l'exécution nocturne des contrôles ;
- la détection d'une compromission ;
- l'arrêt automatique de la machine virtuelle ;
- la sauvegarde du disque et de la mémoire à destination du CERT ;
- le restage automatique de la machine ;
- la validation du résultat via Selenium.

---

# Difficultés rencontrées

Les principales difficultés du projet concernaient :

- la montée en charge rapide de la plateforme ;
- la multiplication des environnements ;
- les contraintes de disponibilité ;
- les vulnérabilités critiques publiées régulièrement ;
- la nécessité d'automatiser des opérations historiquement réalisées manuellement.

---

# Résultats

Cette initiative a permis :

- d'augmenter significativement la capacité de la plateforme ;
- de soutenir une montée en charge jusqu'à environ 40 000 utilisateurs simultanés pendant la période COVID ;
- de faire évoluer la plateforme vers une infrastructure multi-sites structurée autour de 26 VM Ivanti, 12 profils / environnements et 8 VM StrongSwan ;
- d'améliorer la rapidité de déploiement des nouvelles appliances ;
- de renforcer la sécurité des infrastructures ;
- de réduire les opérations manuelles ;
- d'améliorer la conformité des plateformes ;
- d'industrialiser le provisioning et les opérations d'administration.

Au-delà des évolutions techniques, cette initiative a également permis d'identifier les limites des solutions VPN propriétaires utilisées jusqu'alors.

Les coûts de licences, les vulnérabilités critiques publiées régulièrement sur Pulse Secure / Ivanti Connect Secure ainsi que les besoins croissants en automatisation ont conduit au lancement d'une nouvelle initiative basée sur StrongSwan.

L'objectif était de remplacer progressivement la partie IPsec de la plateforme par une solution Open Source offrant une meilleure maîtrise de l'architecture, une automatisation plus poussée, une réduction des coûts et une diminution de la dépendance aux solutions propriétaires.

---

# Compétences démontrées

- Architecture d'infrastructure
- Capacity Planning
- Haute Disponibilité
- Plateformes Remote Access
- Infrastructure as Code
- Platform Engineering
- Automatisation
- DevSecOps
- Security Hardening
- Gestion de crise
- Industrialisation des infrastructures

---

# Écosystème technique

## Solutions

- Pulse Secure
- Ivanti Connect Secure
- F5 BIG-IP

## Plateformes

- VMware

## Langages & scripting

- Python
- Bash

## Automatisation

- Ansible
- Selenium

## Infrastructure

- Load Balancing
- DNS
- PKI
- CMDB
- REST API
- Netconf

## Systèmes

- Linux

---

# Domaines concernés

- Remote Access
- Infrastructure Architecture
- Network Security
- Infrastructure Automation
- DevSecOps

---

# Références

## Entreprise

NTT DATA

## Client

Commission européenne

## Période

2016 – 2021

## Documents associés

- Présentation interne retraçant l'évolution de la plateforme Remote Access.
- `artifacts/RemoteACcessHistorique.pptx`
