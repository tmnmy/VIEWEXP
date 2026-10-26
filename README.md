# VIEWEXP

VIEWEXP affiche vos fichiers au survol dans Windows. Maintenez votre raccourci, passez la souris sur un fichier et relâchez pour fermer l’aperçu.

L’application fonctionne dans l’Explorateur, sur le Bureau et dans les fenêtres communes Ouvrir et Enregistrer.

**[Télécharger VIEWEXP 0.17.0 — Windows x64](https://github.com/tmnmy/VIEWEXP/releases/download/v0.17.0/VIEWEXP-0.17.0-Installer.exe)** · [Notes et SHA-256](https://github.com/tmnmy/VIEWEXP/releases/tag/v0.17.0)

**Aperçu rapide à la barre Espace** : sélectionnez un fichier puis appuyez sur Espace. L’aperçu reste ouvert après relâchement et pendant les mouvements de souris. Espace à nouveau ou Échap ferme. Les champs de saisie conservent leur fonctionnement normal. Le mode survol reste disponible.

## Consulter ses fichiers

Choisissez un aperçu en plein écran ou près du pointeur. Les petites images restent à 100 % ; les grandes sont ajustées sans déformation. Un damier gris rend les zones transparentes visibles. Les marges extérieures restent transparentes dans le mode près du pointeur, limité à 1 200 × 800 pixels.

| Fichier | Aperçu et commandes |
| --- | --- |
| Images | Molette pour zoomer ; clic gauche ou central maintenu pour se déplacer dans l’image agrandie. |
| Vidéos | Lecture automatique avec son et en boucle. Molette : avancer ou reculer de cinq secondes. |
| Audio | Lecture avec son. Molette : avancer ou reculer de cinq secondes. |
| Objets 3D | Bouton central maintenu pour tourner autour du centre de l’objet, axes horizontal et vertical inversés ; molette pour zoomer ; après un cran de molette, clic gauche maintenu pour tourner autour du modèle. |
| PDF | Page ajustée en largeur. Clic gauche maintenu + glisser pour défiler ; molette pour changer de page. |
| Texte et code | Lecture seule, sans exécution. Molette ou clic gauche maintenu + glisser pour défiler. |

Le timecode audio et vidéo s’affiche en bas. Relâcher le raccourci ferme toujours l’aperçu et arrête la lecture. Avant interaction, déplacer la souris de plus de 10 pixels ferme aussi la vue. Échap ou clic droit permet de la fermer.

Le raccourci se choisit par appui sur une touche ou une combinaison. Les options, la pause et le démarrage avec Windows sont accessibles depuis l’icône près de l’horloge.

## Formats

- Images : JPEG, PNG, WebP, EXR, DPX, PSD/PSB, TIFF, AVIF, JPEG XL, JPEG 2000, BMP, GIF, ICO, TGA, HDR et d’autres raster.
- Vidéos vérifiées : MP4 H.264, MKV, MOV ProRes/DNxHR et WebM VP9.
- Audio vérifié : WAV, MP3, FLAC, M4A, AAC, WMA, Ogg, Opus et AIFF.
- 3D : OBJ, STL, GLB, glTF, FBX et BLEND.
- Documents : PDF, TXT, MD, LOG, CSV, TSV, PY, PS1, JS, TS, C/C++, CS, RS, JSON, YAML, TOML, XML, HTML, CSS et d’autres fichiers texte usuels.

Les PSD restent des aperçus d’image. Le code, le HTML et les tableaux sont affichés comme texte brut.

Les fichiers **BLEND** nécessitent Blender 4.2 ou plus récent installé dans `Program Files/Blender Foundation`. VIEWEXP utilise un processus séparé, sans interface et avec scripts automatiques désactivés. L’aperçu porte sur les maillages enregistrés : les modificateurs, animations et textures ne sont pas évalués. Le premier chargement prend plus de temps ; les réouvertures utilisent un cache mémoire borné. Blender n’est pas inclus ni téléchargé par l’installateur.

Le **son des vidéos est activé par défaut** lorsqu’une piste audio est présente. La molette avance ou recule le son et l’image ensemble ; relâcher le raccourci ferme la vue et arrête le son. VIEWEXP utilise la sortie Windows par défaut, sans changer le volume système.

## Installation et mises à jour

Téléchargez l’installateur depuis les [Releases](https://github.com/tmnmy/VIEWEXP/releases/tag/v0.17.0), puis lancez-le. Il contient VIEWEXP et ImageMagick. Une connexion Internet est nécessaire à la première installation pour télécharger FFmpeg directement depuis [son fournisseur BtbN](https://github.com/BtbN/FFmpeg-Builds/releases/tag/autobuild-2026-09-30-13-08). L’archive et chaque binaire sont vérifiés par SHA-256. Vous n’avez pas à installer FFmpeg séparément.

L’installateur fait environ 36 Mo ; FFmpeg représente environ 77 Mo supplémentaires. Une mise à jour réutilise les fichiers FFmpeg conformes et conserve les réglages ainsi que le choix de démarrage avec Windows. Si la préparation échoue, l’installation existante est conservée.

À partir de la 0.13.0, VIEWEXP recherche les nouvelles versions sur GitHub en arrière-plan. Une notification et le menu de l’icône signalent une version disponible. Le téléchargement de l’installateur commence à votre clic sur « Installer VIEWEXP… ». Autorisez les connexions de VIEWEXP dans votre pare-feu pour utiliser cette fonction.

La 0.13.3 a corrigé un blocage lorsque le menu de l’icône reste ouvert pendant une mise à jour. Si le remplacement échoue et que l’installation précédente est entièrement restaurée, l’installateur tente de relancer cette version. L’erreur précise reste disponible dans le journal local.

Les versions antérieures à la 0.13.0 nécessitent une première mise à jour manuelle. Le téléchargement initial de FFmpeg depuis l’installateur reste à qualifier sur une installation neuve ; les tests d’installation utilisent l’archive officielle vérifiée ou un runtime déjà conforme.

## Limites actuelles

- Vidéo limitée à 1080p et 30 images/s.
- 3D : maillages statiques et couleurs simples ; pas de textures ni d’animations.
- Images multipages ou multicouches : première image ou composite disponible. Les PDF disposent de leur navigation entre pages.
- Texte : aperçu des huit premiers Mio, encodages UTF-8, UTF-16 avec BOM ou Windows-1252. DOCX, XLSX, RTF et EPUB non pris en charge.
- PDF : fichier de 256 Mio et 10 000 pages maximum ; pas de demande de mot de passe.
- Pas de garantie de fidélité HDR pour l’étalonnage.
- Fichiers locaux uniquement ; téléchargez les fichiers cloud avant de les prévisualiser.
- Installateur non signé. La qualification actuelle est réalisée sous Windows 11 x64 ; la matrice multi-écrans et DPI reste à compléter.

## Code et licences

Le code source de VIEWEXP reste privé. Ce dépôt contient la documentation, les installateurs et les signalements de problèmes.

L’application utilise notamment [ImageMagick](https://imagemagick.org/), [FFmpeg](https://ffmpeg.org/) et [ufbx](https://github.com/ufbx/ufbx). Les licences, attributions et références de sources tierces accompagnent l’installation. FFmpeg et ses DLL sont téléchargés chez leur fournisseur et restent remplaçables dans le dossier installé.
