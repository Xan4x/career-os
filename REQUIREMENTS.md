# Requirements

Ce fichier décrit les outils nécessaires pour utiliser Career OS sur un autre poste.

Career OS est principalement un dépôt Markdown.
La seule partie nécessitant une chaîne d'outils spécifique est la génération du CV LaTeX.

---

# Outils obligatoires

## Git

Utilisé pour cloner, versionner et synchroniser le dépôt.

Vérification :

```bash
git --version
```

## Éditeur Markdown

N'importe quel éditeur convient.

Exemples :

- VS Code ;
- Codium ;
- Vim ;
- Obsidian ;
- éditeur texte classique.

---

# Outils pour générer le CV

## Make

Utilisé pour lancer la génération du CV avec une commande simple.

Vérification :

```bash
make --version
```

## LaTeX

Le CV est généré avec `pdflatex`.

Vérification :

```bash
pdflatex --version
```

## Poppler

Optionnel mais recommandé.

Utilisé pour vérifier le contenu texte ou convertir le PDF en image lors des contrôles.

Commandes utiles :

```bash
pdftotext -v
pdftoppm -v
```

---

# Installation Debian / Ubuntu

Commande recommandée :

```bash
sudo apt update
sudo apt install git make texlive-latex-base texlive-latex-recommended texlive-fonts-recommended poppler-utils unzip
```

Paquets :

- `git` : gestion du dépôt ;
- `make` : lancement du build ;
- `texlive-latex-base` : base LaTeX ;
- `texlive-latex-recommended` : paquets LaTeX courants ;
- `texlive-fonts-recommended` : polices recommandées ;
- `poppler-utils` : `pdftotext` et `pdftoppm` ;
- `unzip` : lecture des artifacts `.zip`.

---

# Installation macOS

Installer :

- Git ;
- Make ;
- MacTeX ;
- Poppler.

Avec Homebrew :

```bash
brew install git make poppler
brew install --cask mactex
```

Après installation de MacTeX, ouvrir un nouveau terminal.

---

# Installation Windows

Installer :

- Git for Windows ;
- MiKTeX ;
- Make via MSYS2, Chocolatey ou WSL ;
- Poppler si vérification PDF nécessaire.

Option simple recommandée :

- utiliser WSL Ubuntu ;
- suivre la section Debian / Ubuntu.

---

# Cloner le projet

```bash
git clone <URL_DU_DEPOT>
cd career-os
```

Remplacer `<URL_DU_DEPOT>` par l'URL réelle du dépôt.

---

# Générer le CV

Depuis la racine du dépôt :

```bash
cd deliverables/cv
make rebuild
```

Sortie attendue :

```text
cv.pdf
```

Le PDF généré se trouve ici :

```text
deliverables/cv/cv.pdf
```

---

# Vérifier le PDF

Vérifier que le texte est lisible par un ATS :

```bash
pdftotext deliverables/cv/cv.pdf -
```

Vérifier visuellement une page :

```bash
pdftoppm -png -f 1 -l 1 -r 120 deliverables/cv/cv.pdf /tmp/cv-page
```

Le fichier généré sera :

```text
/tmp/cv-page-1.png
```

---

# Nettoyer le build du CV

Depuis `deliverables/cv` :

```bash
make clean
```

Cette commande supprime :

- le PDF généré ;
- les fichiers temporaires LaTeX.

---

# Structure importante

```text
career-os/
├── README.md
├── AI_INSTRUCTIONS.md
├── AI_HANDOVER.md
├── REQUIREMENTS.md
├── person/
├── companies/
├── customers/
├── projects/
├── domains/
├── artifacts/
├── archives/
└── deliverables/
    └── cv/
        ├── cv.tex
        ├── Makefile
        ├── sections/
        └── theme/
```

---

# Rappel important

Career OS est la source de vérité.

Le CV est un livrable généré.

Si une information de carrière doit être corrigée :

1. modifier d'abord les fichiers `person/`, `companies/`, `customers/`, `projects/` ou `domains/` ;
2. mettre à jour le CV ensuite ;
3. régénérer le PDF.

