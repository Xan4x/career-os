# Decisions

Ce document explique les choix de conception de Career OS.

Il permet de comprendre pourquoi certaines décisions ont été prises et d'éviter de remettre en question régulièrement l'architecture du projet.

La conversation initiale: https://chatgpt.com/share/6a43d8e4-1944-83ed-bf26-2b8620c0db85

---

# La base de connaissances est la source de vérité

## Décision

La base de connaissances est la seule source de vérité.

## Pourquoi ?

Les CV, profils LinkedIn ou lettres de motivation sont des documents temporaires.

Ils évoluent selon le poste recherché.

La base de connaissances, elle, représente l'ensemble de mon parcours professionnel.

Tous les livrables sont générés à partir de cette base.

---

# Toute la base est écrite en français

## Décision

L'ensemble du dépôt est maintenu en français.

## Pourquoi ?

Le français est ma langue de travail pour documenter mes projets, mes idées et mes expériences.

Il est plus simple de réfléchir, compléter et maintenir une base de connaissances dans sa langue maternelle.

Les livrables sont ensuite générés en anglais si nécessaire.

---

# Les projets sont plus importants que les postes

## Décision

Career OS est organisé autour des projets.

## Pourquoi ?

Un intitulé de poste décrit rarement le travail réellement effectué.

Les projets permettent de documenter :

- le contexte ;
- les responsabilités ;
- les choix techniques ;
- les réalisations ;
- les compétences démontrées.

Les postes servent principalement à donner un contexte chronologique.

---

# Les compétences sont déduites

## Décision

Les compétences ne sont jamais maintenues manuellement.

## Pourquoi ?

Une compétence doit toujours être justifiée par une expérience réelle.

Career OS déduit les compétences à partir des projets documentés.

Cela évite les listes de compétences artificielles.

---

# La base de connaissances est exhaustive

## Décision

Career OS conserve l'ensemble de mon parcours.

## Pourquoi ?

Une technologie ou une expérience ancienne peut redevenir pertinente plusieurs années plus tard.

La base de connaissances ne cherche pas à être concise.

Elle cherche à être complète.

Les livrables sélectionnent ensuite uniquement les informations pertinentes.

---

# Les technologies démontrent des concepts

## Décision

Une technologie n'est pas seulement un produit.

## Pourquoi ?

Avec l'expérience, la valeur ne réside plus uniquement dans la maîtrise d'un produit, mais dans la compréhension des concepts qu'il représente.

Par exemple :

- Blue Coat → architectures Proxy / Reverse Proxy
- Cisco ASA → sécurité réseau, segmentation, VPN
- NGINX → reverse proxy, load balancing
- Check Point → architecture de firewalling

Lors de la génération d'un livrable, l'assistant peut choisir de mettre en avant :

- une technologie ;
- une compétence ;
- une connaissance d'architecture.

Le choix dépend du poste visé.

---

# Les fichiers Markdown sont toujours renvoyés en entier

## Décision

Toute proposition de modification d'un fichier est renvoyée dans son intégralité.

## Pourquoi ?

Le dépôt est maintenu avec Git.

Le fichier complet est plus simple à relire, copier et versionner qu'une succession de fragments.

Les différences sont déjà gérées par Git.

---

# Career OS doit rester simple

## Décision

Chaque évolution doit simplifier la maintenance de ma carrière.

## Pourquoi ?

Career OS n'a pas pour objectif de devenir un framework.

Son objectif est de me faire gagner du temps.

Si une nouvelle idée complexifie le projet sans améliorer concrètement les futurs livrables, elle ne doit pas être retenue.

---

# Les domaines d'expertise sont une synthèse

## Décision

Career OS distingue les projets des domaines d'expertise.

## Pourquoi ?

Les projets décrivent ce qui a été réalisé.

Les domaines décrivent ce que ces projets démontrent.

Ils permettent de capitaliser sur l'ensemble des expériences acquises, même lorsque plusieurs projets ou technologies abordent les mêmes concepts.

Ils facilitent également la génération de CV ciblés en reliant les besoins d'une offre d'emploi à des domaines d'expertise plutôt qu'à une simple liste de technologies.

Les domaines sont une synthèse des projets.

Ils ne remplacent jamais les projets.

---

# Les expériences sont contextualisées

## Décision

Career OS distingue plusieurs niveaux de contexte :

- l'employeur ;
- le client ;
- le projet ;
- le domaine d'expertise.

## Pourquoi ?

Une carrière ne se résume pas à une succession de postes.

Dans un contexte de consulting, plusieurs projets peuvent être réalisés pour un même client, lui-même au sein d'un même employeur.

Séparer ces niveaux permet de raconter fidèlement l'évolution professionnelle sans dupliquer les informations.

Cette organisation facilite également la génération de CV adaptés à différents contextes tout en conservant une base de connaissances cohérente.

---

## Règle

Un fichier est considéré comme "V1 validé" lorsqu'il décrit fidèlement les faits connus au moment de sa rédaction.

À partir de ce moment :

- il est commité ;
- il devient la référence ;
- il n'est modifié qu'en cas de nouvelle information ou de correction factuelle.

Career OS est un projet vivant.

Il privilégie des améliorations progressives plutôt qu'une recherche permanente de perfection.

---

# Principe directeur

Maintenir ma carrière une seule fois.

Générer tout le reste.
