================================================================================
                              T.I.C.K
                   Target Input Compatible Kickoff
================================================================================

T.I.C.K est un outil simple pour créer des raccourcis de vos jeux Windows
(lancés via Bottles) avec support Steam Input. Profitez de vos manettes et
de Steam Deck pour tous vos jeux !


================================================================================
FONCTIONNALITÉS
================================================================================

✓ Détection automatique des jeux dans vos Bottles
✓ Création de raccourcis .desktop pour le menu applications
✓ Ajout à Steam avec Steam Input activé (configuration manette)
✓ Téléchargement automatique des artworks (bannières, logos)
✓ Extraction des icônes depuis les fichiers .exe
✓ Synchronisation automatique Steam/fichiers
✓ Bouton "Régénérer" pour réparer les problèmes
✓ Interface graphique simple et intuitive


================================================================================
POURQUOI T.I.C.K ?
================================================================================

Vous utilisez Bottles pour lancer vos jeux Windows sur Linux, mais vous
voulez profiter de Steam Input pour configurer vos manettes ? T.I.C.K crée
des raccourcis qui passent par Steam, vous donnant accès à toutes les
fonctionnalités de Steam (Input, Overlay, Big Picture, Steam Deck).

Votre jeu apparaît dans Steam comme un jeu natif, avec sa bannière, son
logo, et tout le support manette de Steam !


================================================================================
PRÉREQUIS
================================================================================

- Linux (Ubuntu, Fedora, Arch, etc.)
- Python 3.10 ou supérieur
- PySide6 (Qt pour Python)
- Bottles installé et configuré
- bottles-cli accessible dans le PATH
- Steam (optionnel, pour l'ajout à Steam)

Outils optionnels (pour extraction d'icônes) :
- icoutils (wrestool, icotool)
- ImageMagick (convert)


================================================================================
INSTALLATION
================================================================================

1. Clonez le repository :
   git clone https://github.com/Andalrick/T.I.C.K.git
   cd T.I.C.K

2. Installez les dépendances Python :
   pip install --break-system-packages PySide6
   pip install --break-system-packages vdf

3. (Optionnel) Installez les outils d'extraction d'icônes :
   
   Ubuntu/Debian :
   sudo apt install icoutils imagemagick
   
   Fedora :
   sudo dnf install icoutils ImageMagick
   
   Arch :
   sudo pacman -S icoutils imagemagick

4. Lancez T.I.C.K :
   python3 tick-dev-enhanced.py


================================================================================
UTILISATION
================================================================================

CRÉER UN RACCOURCI
------------------

1. Onglet "Nouveau jeu"
2. Sélectionnez votre lanceur Bottles
3. Tapez le nom du jeu (recherche automatique)
4. Sélectionnez l'exécutable .exe
5. (Optionnel) Cochez "Ajouter à Steam"
6. Cliquez sur "Créer le raccourci"

Voilà ! Votre jeu est prêt à être lancé.


GÉRER VOS RACCOURCIS
---------------------

1. Onglet "Raccourcis créés"
2. Liste de tous vos jeux avec leur statut
3. Colonnes :
   - Steam : Cochez pour ajouter/retirer de Steam
   - .desktop : Cochez pour créer/supprimer le raccourci menu

Boutons disponibles :
- [Actualiser] : Rafraîchit la liste
- [Régénérer] : Répare tous les fichiers d'un jeu
- [Supprimer] : Supprime complètement le raccourci


ARTWORKS STEAM (OPTIONNEL)
---------------------------

Pour télécharger automatiquement les bannières et logos :

1. Créez un compte sur https://www.steamgriddb.com
2. Allez dans Preferences → API
3. Générez une clé API (gratuit, 100 requêtes/jour)
4. T.I.C.K vous demandera la clé au premier téléchargement
5. La clé est sauvegardée pour les prochaines fois


================================================================================
STRUCTURE DES FICHIERS
================================================================================

T.I.C.K crée plusieurs fichiers pour chaque jeu :

Scripts de lancement :
  ~/.local/bin/tick-shortcuts/nom-du-jeu-tick-YYYYMMDD.sh

Fichiers .desktop :
  ~/.local/share/applications/tick-nom-du-jeu.desktop

Icônes extraites :
  ~/.local/share/tick/icons/

Base de données :
  ~/.local/share/tick/games.db

Configuration :
  ~/.config/tick/config.json


================================================================================
PROBLÈMES COURANTS
================================================================================

"Mon jeu n'apparaît pas dans Steam"
------------------------------------
→ Fermez Steam COMPLÈTEMENT (via le menu)
→ Relancez Steam
→ Le jeu devrait apparaître dans votre bibliothèque


"Les artworks ne s'affichent pas"
----------------------------------
→ Sélectionnez le jeu dans l'onglet "Raccourcis créés"
→ Cliquez sur [Régénérer]
→ Redémarrez Steam


"Le .desktop ne se crée pas"
-----------------------------
→ Vérifiez que le dossier existe : ~/.local/share/applications
→ Essayez [Régénérer] dans T.I.C.K


"bottles-cli introuvable"
--------------------------
→ Vérifiez que Bottles est installé
→ Testez dans un terminal : bottles-cli --version
→ Si Flatpak : le PATH peut ne pas être configuré


"Tout est cassé !"
------------------
→ Sélectionnez le jeu
→ Cliquez sur [Régénérer]
→ Ça devrait réparer automatiquement
→ Si ça persiste, supprimez et recréez le raccourci


================================================================================
STEAM INPUT
================================================================================

Une fois votre jeu ajouté à Steam :

1. Lancez Steam en mode Big Picture
2. Allez dans les paramètres du jeu
3. Onglet "Manette"
4. Configurez votre layout manette
5. Profitez du support manette complet !

Steam Input fonctionne avec :
- Manettes Xbox, PlayStation, Switch
- Steam Controller
- Steam Deck
- N'importe quelle manette supportée par Steam


================================================================================
CONTRIBUTION
================================================================================

T.I.C.K est open source ! Les contributions sont les bienvenues.

Bugs et suggestions :
→ GitHub Issues : https://github.com/Andalrick/T.I.C.K/issues

Code :
→ Fork, branch, PR !

Restez courtois et constructif. Nous sommes tous là pour améliorer
l'expérience gaming sur Linux !


================================================================================
LICENCE
================================================================================

[À préciser - MIT / GPL-3.0 / Apache-2.0]


================================================================================
REMERCIEMENTS
================================================================================

- L'équipe Bottles pour leur excellent gestionnaire de préfixes Windows
- Valve pour Steam et Steam Input
- SteamGridDB pour la base de données d'artworks
- La communauté Linux Gaming


================================================================================
CONTACT
================================================================================

GitHub : https://github.com/Andalrick/T.I.C.K
Issues : https://github.com/Andalrick/T.I.C.K/issues


================================================================================

Bon jeu ! 🎮

================================================================================
