# Relevé d'heures

Un outil autonome et minimaliste pour calculer rapidement ses heures de travail et estimer sa rémunération en net et en brut, directement dans le navigateur.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Zero Dependencies](https://img.shields.io/badge/dépendances-0-brightgreen?style=flat-square)
![Licence](https://img.shields.io/badge/licence-MIT-blue?style=flat-square)

---

## Présentation

L'application fonctionne comme un bloc-notes : tu saisis tes horaires ligne par ligne, et le tableau de bord calcule en direct la durée de chaque journée, le total général, ainsi que la rémunération équivalente.

- **Zero setup** : aucun serveur, aucun runtime, aucun outil de build requis. Un simple fichier `.html` suffit.
- **Local-first** : tes horaires et tes taux sont enregistrés dans le `localStorage` de ton navigateur ; aucune donnée n'est envoyée vers l'extérieur.
- **Responsive & ergonomique** : interface adaptative optimisée pour ordinateur et mobile, supportant nativement les modes clair et sombre via `prefers-color-scheme`.

---

## Fonctionnalités

- **Saisie libre et fluide** : analyse syntaxique par regex acceptant des formats variés (ex. `lundi 19 9h30-12h10 13h30-16h10`).
- **Plages multiples & passage de minuit** : prise en charge de plusieurs créneaux par jour et des horaires de nuit (`22h-2h` = 4 h).
- **Contrôle de cohérence** : alerte visuelle si un total estimé saisi en fin de ligne (ex. `5h20`) diffère du total calculé.
- **Conversion net / brut automatique** : saisie bidirectionnelle basée sur un ratio paramétrable (cotisations estimées à 22 % pour un statut non cadre).
- **Affichage polyvalent** : totaux formatés en heures/minutes (`h`), heures décimales, net estimé et brut estimé.
- **Export rapide** : bouton pour copier un récapitulatif textuel propre dans le presse-papiers.

---

## Utilisation

1. Ouvre le fichier `Relevé_d_heures.html` dans n'importe quel navigateur moderne.
2. Saisis tes horaires dans la zone de gauche.
3. Le calcul se déclenche automatiquement 10 secondes après la dernière frappe, immédiatement via le bouton **Calculer**, ou avec le raccourci `Ctrl + Entrée` (`Cmd + Entrée` sur macOS).
4. Renseigne ton taux horaire (en net ou en brut) pour obtenir l'estimation financière.

### Exemples de syntaxe acceptée

```text
mercredi 14  14h30-18h30
lundi 19     9h30-12h10 13h30-16h10  5h20
mardi 20     00h-2h30
dim 18       13h15-18h15 5h
