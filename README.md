# VIEWEXP

VIEWEXP affiche vos images et lit vos vidéos au survol dans Windows. Maintenez votre raccourci, passez la souris sur un fichier et relâchez pour fermer l’aperçu.

L’application fonctionne dans l’Explorateur, sur le Bureau et dans les fenêtres Ouvrir et Enregistrer.

La première version publique est en préparation. Aucun installateur n’est encore disponible dans ce dépôt.

## Affichage et commandes

Choisissez un aperçu en plein écran ou près du pointeur, sur fond transparent. Les petites images restent à 100 % ; les grandes sont ajustées à l’écran sans déformation. Les vidéos démarrent automatiquement, sans son, et tournent en boucle.

Le raccourci se configure par appui sur une touche ou une combinaison. Les options, la pause et le démarrage avec Windows sont accessibles depuis l’icône près de l’horloge.

| Action | Résultat |
|---|---|
| Maintenir le raccourci et survoler un fichier | Ouvrir l’aperçu |
| Relâcher le raccourci | Fermer l’aperçu |
| Bouger de plus de 10 pixels avant le zoom | Fermer l’aperçu |
| Tourner la molette | Activer le zoom |
| Après le zoom, maintenir le clic gauche ou le bouton central et glisser | Se déplacer dans la vue |
| Appuyer sur Échap ou faire un clic droit | Fermer l’aperçu |

## Formats

Pour les images : JPEG, PNG, WebP, EXR, DPX, PSD/PSB, TIFF, AVIF, JPEG XL, JPEG 2000, BMP, GIF, ICO, TGA, HDR et d’autres formats.

Les vidéos vérifiées comprennent les MP4 H.264, MKV, MOV ProRes/DNxHR et WebM VP9.

## Installation

L’installateur sera proposé dans la section [Releases](https://github.com/tmnmy/VIEWEXP/releases). Il contiendra l’application et ses décodeurs. Vous n’aurez pas besoin d’installer FFmpeg séparément.

VIEWEXP fonctionne sous Windows 10 et 11, en 64 bits.

## Limites actuelles

- L’aperçu vidéo est limité à 1080p et 30 images/s maximum, sans son.
- Pour les fichiers multipages ou multicouches, seule la première page, la première image ou le composite disponible est affiché.
- L’aperçu HDR n’offre pas de garantie de fidélité pour l’étalonnage.
- Les fichiers doivent être locaux. Téléchargez les fichiers cloud avant de les prévisualiser.
- L’installateur n’est pas signé.

## Code et licences

Le code source de VIEWEXP reste privé. Ce dépôt contient la documentation et les signalements de problèmes, puis accueillera les téléchargements.

L’application utilise notamment ImageMagick et FFmpeg. Leurs licences, attributions et informations sur les sources accompagneront la distribution.
