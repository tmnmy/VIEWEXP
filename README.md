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

Pour ouvrir un comparateur vide, faites un clic droit sur l’icône VIEWEXP près de l’horloge, dans la barre des tâches. Choisissez **Comparer des images…** ou **Comparer des textes…**, puis déposez vos fichiers dans la fenêtre. Le comparateur de textes accepte également le texte collé.

## Formats pris en charge

| Famille | Extensions reconnues dans VIEWEXP 0.34.7 |
| --- | --- |
| Images courantes et photo | .jpg, .jpeg, .jpe, .jfif, .png, .gif, .webp, .bmp, .dib, .ico, .tif, .tiff, .avif, .heic, .heif, .jxl |
| Cinéma, HDR et création | .exr, .dpx, .cin, .hdr, .rgbe, .pfm, .psd, .psb, .dds |
| Autres formats d’image | .wdp, .hdp, .jxr, .jp2, .j2k, .jpf, .jpx, .tga, .targa, .icb, .vda, .vst, .qoi, .pbm, .pgm, .ppm, .pnm, .pam, .pcx, .sgi, .rgb, .rgba, .bw, .ras, .sun, .fits, .fit, .fts, .jng |
| Vidéo | .mp4, .m4v, .mov, .mkv, .webm, .avi, .wmv, .asf, .mpg, .mpeg, .m2v, .mts, .m2ts, .ts, .vob, .ogv, .flv, .mxf, .3gp, .3g2 |
| Audio | .wav, .mp3, .flac, .ogg, .oga, .opus, .m4a, .aac, .wma, .aif, .aiff, .aifc, .ape, .wv, .amr, .au |
| Modèles 3D | .obj, .stl, .gltf, .glb, .fbx, .blend |
| Documents PDF | .pdf |
| Texte, documentation et sous-titres | .txt, .text, .md, .markdown, .rst, .log, .csv, .tsv, .srt, .vtt, .tex, .adoc |
| Scripts et développement | .py, .pyi, .pyw, .ps1, .psm1, .psd1, .bat, .cmd, .sh, .bash, .zsh, .js, .mjs, .cjs, .ts, .jsx, .tsx, .c, .cpp, .cc, .cxx, .h, .hpp, .cs, .rs, .go, .java, .php, .rb, .lua, .sql, .ahk, .r, .swift, .kt, .kts |
| Web, données et configuration | .json, .jsonl, .yaml, .yml, .toml, .ini, .cfg, .conf, .xml, .html, .htm, .css, .scss, .vue, .svelte, .diff, .patch, .properties, .reg, .lock |
| Dessins ASCII et ANSI | .nfo, .asc, .diz, .ans |

VIEWEXP reconnaît aussi certains fichiers par leur nom : `.env` et ses variantes `.env.*`, `.gitignore`, `.gitattributes`, `.editorconfig`, `.npmrc`, `.prettierrc`, `Dockerfile`, `Makefile`, `LICENSE` et `README`. Pour un fichier `.ts`, le contenu permet de distinguer le code TypeScript d’une vidéo MPEG-TS.

## Limites de l’aperçu et de la comparaison

La lecture vidéo dépend du codec utilisé dans le fichier. Les formats vérifiés comprennent le H.264 en MP4, le ProRes et le DNxHR en MOV, ainsi que le VP9 en WebM. L’aperçu vidéo est limité à 1 920 × 1 080 pixels et 30 images/s. Les PSD et PSB affichent le composite disponible. L’aperçu 3D montre les maillages statiques avec des couleurs simples.

Le comparateur de textes accepte les extensions de texte, de code et de configuration ci-dessus, ainsi que les dessins NFO, ASC et DIZ, jusqu’à 8 Mio et 250 000 lignes par fichier. Il lit l’UTF-8, l’UTF-16 avec BOM, le Windows-1252 et le CP437 pour les dessins ASCII. Si vous sélectionnez deux fichiers ANS, VIEWEXP compare les dessins en couleurs côte à côte.

Le comparateur d’images accepte les JPEG compatibles et les PNG statiques RVB ou RVBA à 8 ou 16 bits. Il calcule la différence sur un canevas commun d’environ un mégapixel au maximum, avec une sortie SDR 8 bits. Deux images peuvent donc donner une différence noire même si leurs fichiers d’origine diffèrent. Le bouton **Informations** sous chaque vignette permet de consulter et de copier les métadonnées EXIF, IPTC et XMP disponibles.

## Installation

Lancez l’installateur sur Windows x64. Il télécharge [FFmpeg](https://github.com/BtbN/FFmpeg-Builds/releases/tag/autobuild-2026-09-30-13-08) lors de la première installation, qui nécessite donc une connexion Internet. L’installateur est non signé. Les mises à jour conservent vos réglages.

Les aperçus fonctionnent avec les fichiers disponibles sur le disque. Pour les fichiers BLEND, installez Blender 4.2 ou plus récent dans `Program Files/Blender Foundation`.

VIEWEXP utilise notamment [ImageMagick](https://imagemagick.org/), [FFmpeg](https://ffmpeg.org/), [ufbx](https://github.com/ufbx/ufbx), LittleCMS et [Scintilla](https://www.scintilla.org/). Leurs licences accompagnent l’installation.
