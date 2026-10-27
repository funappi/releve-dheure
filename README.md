# Relevé d'heures

Un outil autonome et minimaliste pour noter ses horaires de travail, calculer ses heures et estimer sa rémunération en net et en brut, directement dans le navigateur.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Dépendances](https://img.shields.io/badge/dépendances-0-brightgreen?style=flat-square)
![Licence](https://img.shields.io/badge/licence-PolyForm%20Noncommercial-orange?style=flat-square)

---

## Présentation

L'application fonctionne comme un bloc-notes. Tu saisis tes horaires ligne par ligne, et le relevé du mois se calcule tout seul : durée de chaque journée, sous-total par semaine, total du mois et rémunération estimée.

- **Zero setup** : aucun serveur, aucun outil de build. Un seul fichier `.html` suffit.
- **Local-first** : tes horaires, tes taux et tes réglages sont enregistrés dans le `localStorage` de ton navigateur. Rien n'est envoyé ailleurs.
- **Adaptatif** : utilisable sur ordinateur comme sur téléphone. Le thème est clair, sombre ou automatique (il suit le réglage de ton appareil), et se change d'un clic dans la page.

---

## Fonctionnalités

### Relevé

- **Un relevé par mois**, avec des flèches pour passer d'un mois à l'autre et un retour au mois en cours.
- **Saisie libre** : plusieurs formats acceptés, par exemple `lundi 19 9h30-12h10 13h30-16h10`.
- **Plages multiples et passage de minuit** : plusieurs créneaux par jour, et `22h-2h` compte bien 4 h.
- **Dates** : un numéro de jour (`19`) ou jour/mois (`19/10`) suffit. Les jours sans numéro suivent l'ordre de la semaine. Une alerte signale un jour qui ne correspond pas à la date, ou une date qui n'existe pas dans le mois.
- **Semaines du lundi au dimanche**, avec un sous-total pour chacune.
- **Contrôle de cohérence** : une alerte apparaît si le total noté en fin de ligne (ex. `5h20`) diffère du total calculé.
- **Net et brut liés** : tu saisis l'un des deux taux, l'autre se calcule grâce à un ratio réglable (78 % par défaut).
- **Détail des montants** : net et brut par jour, total du mois, heures décimales, heures supplémentaires et pauses retirées.
- **Export** : copie d'un récapitulatif en texte, ou copie en tableau à coller directement dans Excel ou Google Sheets.

### Paramètres

Tout ce qui suit se règle dans l'onglet **Paramètres**.

- **Affichage** : chaque élément de la page peut être masqué (introduction, aide de saisie, navigation par mois, montants, heures décimales, lignes ignorées, boutons de copie).
- **Calcul automatique** : immédiat, 2 s (par défaut), 5 s, 10 s, ou seulement sur le bouton Calculer.
- **Net et brut** : ratio net/brut modifiable selon ton statut.
- **Heures supplémentaires** : seuil hebdomadaire (35 h par défaut), +25 % jusqu'à 43 h, puis +50 % au-delà. Tous ces chiffres sont modifiables.
- **Majorations**
  - **Dimanche** : +50 % par défaut, avec la date ou le nom du jour sur la ligne.
  - **Heures de nuit** : +25 % par défaut, appliqué aux seules minutes comprises dans la plage de nuit.
- **Horaires de nuit** : plage de nuit par défaut de 21h à 6h, modifiable.
- **Pause non payée** : retrait de 30 min par défaut, pour les journées d'au moins 6 h. Option pour ne pas retirer la pause quand la journée a déjà plusieurs plages.
- **Arrondi** : pas de 5, 10, 15 ou 30 min, arrondi au plus proche, vers le bas ou vers le haut.
- **Données** : rétablir les réglages par défaut, ou effacer tous les relevés.

---

## Utilisation

1. Ouvre `Index.html` dans un navigateur moderne.
2. Saisis tes horaires dans la zone de gauche.
3. Le calcul se lance selon le délai choisi dans Paramètres (2 s par défaut). Tu peux aussi cliquer sur **Calculer** ou appuyer sur `Ctrl + Entrée` (`Cmd + Entrée` sur macOS).
4. Renseigne ton taux horaire, net ou brut, pour obtenir l'estimation.
5. Ajuste les majorations, la pause et l'arrondi dans **Paramètres** selon ton contrat.

### Exemples de syntaxe acceptée

```text
mercredi 14  14h30-18h30
lundi 19     9h30-12h10 13h30-16h10  5h20
mardi 20     00h-2h30
dim 18       13h15-18h15 5h
```

---

## Licence

Ce projet est distribué sous la licence [PolyForm Noncommercial 1.0.0](LICENSE) : utilisation, modification et partage libres pour tout **usage non commercial**.

**Usage commercial : contacte-moi pour une licence séparée** — [Funappi](https://github.com/funappi).
