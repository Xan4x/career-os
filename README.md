# Career OS

> Écrire ma carrière une seule fois. Générer tout le reste.

## Pourquoi ce projet ?

Je ne veux plus réécrire mon CV tous les quelques années.

À la place, je maintiens une base de connaissances décrivant ma carrière.

Cette base permet de générer automatiquement :

- un CV ;
- un profil LinkedIn ;
- des lettres de motivation ;
- une préparation aux entretiens ;
- d'autres documents professionnels.

Le dépôt est la source de vérité.

Les documents générés ne sont que des livrables.

---

## Objectifs

Career OS doit me permettre de :

- maintenir facilement ma carrière ;
- retrouver rapidement un projet ou une technologie ;
- générer un CV adapté à une offre d'emploi ;
- générer un profil LinkedIn à jour ;
- préparer un entretien ;
- adapter mes candidatures aux offres d'emploi ;
- éviter de repartir de zéro.

---

## Principes

- La base de connaissances est la seule source de vérité.
- Toute la base est écrite en français.
- Les livrables professionnels sont générés en anglais (sauf demande contraire).
- Les projets sont plus importants que les postes.
- Les compétences sont déduites des projets.
- Le dépôt doit toujours me faire gagner du temps.
- Toujours fournir le fichier markdown complet lorsque l'on propose une update dans le repo.

---

## Structure

```text
career-os/
│
├── README.md
├── STYLE_GUIDE.md
│
├── ai/
│   └── AI_INSTRUCTIONS.md
│
├── meta/
│   ├── CHANGELOG.md
│   ├── DECISIONS.md
│   ├── ROADMAP.md
│   └── VERSION.md
│
├── person/
├── companies/
├── projects/
├── domains/
│   ├── README.md
│   └── ...
│
├── notes/
├── archive/
└── outputs/
```

### Organisation des connaissances

Career OS organise les informations selon plusieurs niveaux.

| Dossier | Rôle |
|---------|------|
| **person** | Informations personnelles stables (profil, formation, certifications, centres d'intérêt...). |
| **companies** | Contexte professionnel et évolution au sein des entreprises. |
| **projects** | Les projets réalisés, leurs objectifs, leurs architectures, leurs réalisations et les technologies utilisées. |
| **domains** | Les domaines d'expertise déduits des projets. Ils regroupent les concepts, connaissances d'architecture et compétences acquises tout au long de la carrière. |
| **notes** | Idées, souvenirs ou éléments à documenter ultérieurement. |
| **outputs** | Les documents générés (CV, LinkedIn, lettres de motivation...). Ils ne sont jamais la source de vérité. |
| **archive** | Anciens documents conservés à titre historique (anciens CV, exports LinkedIn, etc.). |

---

## Fonctionnement

Lorsque je me souviens d'une nouvelle information :

1. je mets à jour la base de connaissances ;
2. je valide le changement dans Git ;
3. je régénère les documents uniquement lorsque j'en ai besoin.

Je ne maintiens jamais directement un CV ou un profil LinkedIn.

Je maintiens uniquement la base de connaissances.

---

## Vision

Career OS est un projet personnel destiné à m'accompagner tout au long de ma carrière.

Son objectif est de maintenir une base de connaissances fiable et à jour afin de pouvoir générer rapidement des livrables professionnels de qualité.

Grâce à cette base de connaissances, je dois pouvoir :

- générer un CV moderne et pertinent en quelques minutes ;
- maintenir facilement mon profil LinkedIn ;
- adapter mon CV à une offre d'emploi ;
- préparer un entretien technique ;
- produire d'autres documents professionnels sans repartir de zéro.

Le temps investi dans la maintenance de Career OS doit me faire gagner du temps à chaque future candidature.
