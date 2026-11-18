# VIEWEXP

Dans l’Explorateur Windows, sélectionnez un fichier et appuyez sur **Espace** pour en voir le contenu. Appuyez de nouveau sur Espace ou sur Échap pour fermer l’aperçu. Pour jeter un œil sans changer de sélection, maintenez votre raccourci et survolez un fichier. L’aperçu se ferme quand vous relâchez la touche.

[Télécharger VIEWEXP 0.34.7 pour Windows x64](https://github.com/tmnmy/VIEWEXP/releases/download/v0.34.7/VIEWEXP-0.34.7-Installer.exe) · [Notes de version et empreinte SHA-256](https://github.com/tmnmy/VIEWEXP/releases/tag/v0.34.7)

## Parcourir ses fichiers

VIEWEXP lit les images, les GIF animés, les vidéos et le son. Il affiche aussi les PDF, le texte, le code et les modèles 3D. Les dessins ASCII gardent leurs colonnes et les fichiers ANSI (.ANS) leurs couleurs.

Dans un aperçu ouvert avec Espace, les flèches gauche et droite permettent de parcourir les images du dossier. Utilisez la molette pour zoomer et **B** pour afficher un fond noir. Sur une image JPEG ou PNG, une vidéo ou un fichier audio, **I** affiche les informations du fichier.

## Comparer deux fichiers

Sélectionnez deux fichiers dans l’Explorateur, puis appuyez sur **Espace**.

- **Deux images JPEG ou PNG.** La touche **D** passe de la vue côte à côte au wipe, puis à la différence. En mode wipe, faites glisser les chevrons pour déplacer la séparation ou le petit rond pour l’incliner. **I** échange les deux images.
- **Deux textes.** Les différences apparaissent ligne par ligne, espaces compris. Vous pouvez chercher un mot dans les deux textes, modifier chaque volet et enregistrer les fichiers séparément.

Vous pouvez aussi ouvrir un comparateur vide depuis l’icône près de l’horloge, puis y déposer vos fichiers. Le comparateur de textes accepte également le texte collé.

## Formats et limites

| Usage | Ce que VIEWEXP prend en charge |
| --- | --- |
| Aperçu d’image | JPEG, PNG, WebP, TIFF, PSD/PSB, EXR et DPX, entre autres. Pour un PSD, l’aperçu affiche le composite disponible. |
| Vidéo et audio | MP4 H.264, MOV ProRes ou DNxHR, WebM VP9, ainsi que WAV, MP3 et FLAC. L’aperçu vidéo est limité à 1 920 × 1 080 pixels et 30 images/s. |
| Comparaison de textes | Jusqu’à 8 Mio et 250 000 lignes par fichier. L’éditeur lit l’UTF-8, l’UTF-16 avec marque d’ordre des octets (BOM), le Windows-1252 et le CP437 pour les dessins ASCII. |
| Objets 3D | OBJ, STL, GLB, glTF, FBX et BLEND. L’aperçu montre les maillages statiques avec des couleurs simples. |

Le comparateur d’images accepte les JPEG compatibles et les PNG statiques RVB ou RVBA à 8 ou 16 bits. Il calcule la différence sur un canevas commun d’environ un mégapixel au maximum, avec une sortie SDR 8 bits. Deux images peuvent donc donner une différence noire même si leurs fichiers d’origine diffèrent. Le bouton **Informations** sous chaque vignette permet de consulter et de copier les métadonnées EXIF, IPTC et XMP disponibles.

## Installation

Lancez l’installateur sur Windows x64. Il télécharge [FFmpeg](https://github.com/BtbN/FFmpeg-Builds/releases/tag/autobuild-2026-09-30-13-08) lors de la première installation, qui nécessite donc une connexion Internet. L’installateur est non signé. Les mises à jour conservent vos réglages.

Les aperçus fonctionnent avec les fichiers disponibles sur le disque. Pour les fichiers BLEND, installez Blender 4.2 ou plus récent dans `Program Files/Blender Foundation`.

VIEWEXP utilise notamment [ImageMagick](https://imagemagick.org/), [FFmpeg](https://ffmpeg.org/), [ufbx](https://github.com/ufbx/ufbx), LittleCMS et [Scintilla](https://www.scintilla.org/). Leurs licences accompagnent l’installation.
