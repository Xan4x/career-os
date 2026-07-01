# CV

Ce dossier contient les sources LaTeX du CV généré depuis Career OS.

Un CV est un livrable.
Il n'est jamais la source de vérité.

---

# Structure

```text
deliverables/
└── cv/
    ├── cv.tex
    ├── Makefile
    ├── README.md
    ├── sections/
    │   ├── summary.tex
    │   ├── experience.tex
    │   ├── projects.tex
    │   ├── skills.tex
    │   ├── languages.tex
    │   ├── education.tex
    │   └── certifications.tex
    └── theme/
        ├── colors.tex
        ├── fonts.tex
        └── layout.tex
```

---

# Rôle des fichiers

## `cv.tex`

Point d'entrée du CV.

Il assemble :

- les réglages de thème ;
- l'en-tête ;
- les sections du CV.

Il ne doit pas contenir toute la logique de mise en page ni tout le contenu.

## `sections/`

Contient les blocs visibles du CV.

Chaque fichier correspond à une section :

- `summary.tex` : résumé professionnel ;
- `skills.tex` : expertises principales ;
- `experience.tex` : parcours professionnel ;
- `projects.tex` : projets sélectionnés ;
- `languages.tex` : langues ;
- `education.tex` : placeholder non inclus tant que Career OS ne contient pas de données formation ;
- `certifications.tex` : placeholder non inclus tant que Career OS ne contient pas de données certification.

## `theme/`

Contient la présentation :

- `colors.tex` : couleurs ;
- `fonts.tex` : polices ;
- `layout.tex` : marges, sections, commandes réutilisables.

## `Makefile`

Permet de générer le PDF avec :

```bash
make
```

---

# Source de vérité

Le contenu de carrière doit être maintenu dans :

- `person/`
- `companies/`
- `customers/`
- `projects/`
- `domains/`

Le CV sélectionne et reformule ces informations en anglais professionnel.

Si une information de carrière est fausse ou incomplète :

1. corriger d'abord Career OS ;
2. vérifier si un domaine doit aussi être mis à jour ;
3. régénérer ensuite le CV.

Ne pas corriger uniquement les fichiers LaTeX.

---

# Modifier le CV

## Modifier les faits

Ne pas modifier directement `sections/` si le fait n'existe pas dans Career OS.

Exemples :

- nouvelle responsabilité ;
- nouveau projet ;
- nouvelle technologie ;
- nouvelle période ;
- impact plus précis.

Action correcte :

1. modifier la base Career OS ;
2. adapter le CV depuis cette base.

## Modifier la présentation

Modifier `theme/`.

Exemples :

- marges ;
- couleurs ;
- taille des titres ;
- espacement ;
- commandes LaTeX réutilisables.

## Modifier la sélection du contenu

Modifier `sections/`.

Exemples :

- CV plus court ;
- CV ciblé pour une offre ;
- ordre des projets ;
- formulation plus orientée impact.

Toujours rester aligné avec Career OS.

---

# Générer le PDF

Depuis `deliverables/cv/` :

```bash
make
```

Sortie attendue :

```text
cv.pdf
```

---

# Erreur `pdflatex`

Erreur :

```text
make: pdflatex: No such file or directory
```

Cause :

`pdflatex` n'est pas installé.

Solution :

installer une distribution LaTeX, par exemple :

- TeX Live sur Linux ;
- MiKTeX sur Windows ;
- MacTeX sur macOS.

Sur Ubuntu/Debian, paquet typique :

```bash
sudo apt install texlive-latex-base texlive-latex-recommended texlive-fonts-recommended
```

Après installation :

```bash
cd deliverables/cv
make
```
