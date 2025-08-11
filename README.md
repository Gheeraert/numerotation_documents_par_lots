# Script de numérotation et fusion de fichiers (Tkinter + PyPDF2)

Ce script Python permet de :
- **Numéroter automatiquement** tous les fichiers d’un dossier (préfixe `NNN_`)
- Choisir le **critère de tri** (nom ou date de modification)
- Choisir l’**ordre** (croissant ou décroissant)
- **Fusionner** les fichiers PDF numérotés en un seul fichier (optionnel)

## Fonctionnalités

1. **Sélection du dossier** :
   - Une boîte de dialogue permet de choisir le dossier à traiter.

2. **Choix des critères** :
   - Critère de tri : `Nom` ou `Date de modification`
   - Ordre : `Croissant` ou `Décroissant`
   - Option : *Fusionner les PDF en un seul fichier* (si tous les fichiers numérotés sont des PDF).

3. **Numérotation** :
   - Les fichiers sont renommés avec un préfixe `NNN_` basé sur l’ordre choisi.
   - Les fichiers déjà numérotés ne sont pas renommés.
   - La numérotation reprend après le plus grand numéro existant dans le dossier.

4. **Fusion PDF** :
   - Si l’option est cochée et que tous les fichiers sont des PDF, ils sont fusionnés en un seul PDF final.

## Installation

### Prérequis
- Python 3.7+
- Bibliothèques Python :
  ```bash
  pip install PyPDF2
  ```

## Utilisation

1. Téléchargez le script Python (`numerotation_fusion.py`).
2. Lancez-le :
   ```bash
   python numerotation_fusion.py
   ```
3. Choisissez le dossier contenant vos fichiers.
4. Sélectionnez vos options de tri et d’ordre.
5. Validez pour lancer la numérotation et (optionnel) la fusion PDF.

## Notes
- Les fichiers cachés (commençant par `.`) ne sont pas pris en compte.
- La fusion fonctionne uniquement si **tous** les fichiers numérotés sont des PDF.
- Les collisions de noms sont gérées automatiquement grâce à un renommage en deux passes.

## Licence
Ce script est fourni *tel quel*, librement modifiable et distribuable.
