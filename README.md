# VIEWEXP

VIEWEXP affiche vos images et lit vos vidéos au survol dans Windows. Maintenez votre raccourci, passez la souris sur un fichier et relâchez pour fermer l’aperçu.

L’application fonctionne dans l’Explorateur, sur le Bureau et dans les fenêtres Ouvrir et Enregistrer.

**[Télécharger VIEWEXP 0.10.1 — Windows x64](https://github.com/tmnmy/VIEWEXP/releases/download/v0.10.1/VIEWEXP-0.10.1-Installer.exe)** · [Notes de la préversion et SHA-256](https://github.com/tmnmy/VIEWEXP/releases/tag/v0.10.1)

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

Téléchargez l’installateur depuis la section [Releases](https://github.com/tmnmy/VIEWEXP/releases/tag/v0.10.1), puis lancez-le. Il contient VIEWEXP et ImageMagick ; **une connexion Internet est nécessaire à la première installation** pour télécharger FFmpeg directement depuis [son fournisseur BtbN](https://github.com/BtbN/FFmpeg-Builds/releases/tag/autobuild-2026-09-30-13-08). L’archive et chaque binaire sont vérifiés par SHA-256. Vous n’avez pas à installer FFmpeg séparément.

L’installateur fait environ 35 Mo ; le téléchargement FFmpeg représente environ 77 Mo. Une mise à jour réutilise FFmpeg sans réseau si tous ses fichiers sont conformes. En cas d’échec du téléchargement, l’installation existante est conservée.

Cette version est une **préversion** : le téléchargement initial de FFmpeg n’a pas encore été validé de bout en bout depuis l’installateur. L’installation, la lecture vidéo et la désinstallation ont été testées avec l’archive officielle vérifiée.

VIEWEXP fonctionne sous Windows 10 22H2 et Windows 11, en 64 bits.

## Limites actuelles

- L’aperçu vidéo est limité à 1080p et 30 images/s maximum, sans son.
- Pour les fichiers multipages ou multicouches, seule la première page, la première image ou le composite disponible est affiché.
- L’aperçu HDR n’offre pas de garantie de fidélité pour l’étalonnage.
- Les fichiers doivent être locaux. Téléchargez les fichiers cloud avant de les prévisualiser.
- L’installateur n’est pas signé.

## Code et licences

Le code source de VIEWEXP reste privé. Ce dépôt contient la documentation et les signalements de problèmes. Le code source de l’application n’y est pas publié.

L’application utilise [ImageMagick](https://imagemagick.org/) et [FFmpeg](https://ffmpeg.org/). Les licences, attributions et références de sources sont incluses dans l’installation. FFmpeg et ses DLL sont téléchargés directement chez leur fournisseur et restent remplaçables dans le dossier installé.
