# VIEWEXP

VIEWEXP affiche vos fichiers au survol dans Windows. Maintenez votre raccourci, passez la souris sur un fichier et relâchez pour fermer l’aperçu.

L’application fonctionne dans l’Explorateur, sur le Bureau et dans les fenêtres communes Ouvrir et Enregistrer.

**[Télécharger VIEWEXP 0.30.10 — Windows x64](https://github.com/tmnmy/VIEWEXP/releases/download/v0.30.10/VIEWEXP-0.30.10-Installer.exe)** · [Notes et SHA-256](https://github.com/tmnmy/VIEWEXP/releases/tag/v0.30.10)

**Aperçu rapide à la barre Espace** : sélectionnez un fichier puis appuyez sur Espace. L’aperçu reste ouvert après relâchement et pendant les mouvements de souris. Espace à nouveau ou Échap ferme. Les champs de saisie conservent leur fonctionnement normal. Le mode survol reste disponible.

## Consulter ses fichiers

Choisissez un aperçu en plein écran ou près du pointeur. Les petites images restent à 100 % ; les grandes sont ajustées sans déformation. Un damier gris rend les zones transparentes visibles. Les marges extérieures restent transparentes dans le mode près du pointeur, dont le cadre initial est limité à 1 200 × 800 pixels. Les images peuvent ensuite être redimensionnées par leurs coins.

| Fichier | Aperçu et commandes |
| --- | --- |
| Images | Molette pour zoomer ; clic gauche ou central maintenu pour se déplacer. Après Espace ou un cran de molette, tirer un coin avec le clic gauche redimensionne l’aperçu. |
| Vidéos | Lecture automatique avec son et en boucle. Barre avec lecture/pause, progression et bouton son mémorisé. Molette : avancer ou reculer de cinq secondes. |
| Audio | Lecture avec son, barre de lecture, progression et son mémorisé. Molette : avancer ou reculer de cinq secondes. |
| Objets 3D | Bouton central maintenu pour tourner autour du centre de l’objet, axes horizontal et vertical inversés ; molette pour zoomer ; après un cran de molette, clic gauche maintenu pour tourner autour du modèle. Compteur de triangles affiché. |
| PDF | Page ajustée en largeur, fenêtre redimensionnable, plein écran et bouton Imprimer. Molette, clic gauche maintenu + glisser et barre latérale pour parcourir le document. Le cadre permet de déplacer la fenêtre. |
| Texte et code | Lecture seule, sans exécution. Molette ou clic gauche maintenu + glisser pour défiler. |

Avec **Espace**, les flèches **← et →** ouvrent le fichier précédent ou suivant du dossier. Par défaut, les images restent entre images et les PDF entre PDF ; ces flèches changent de fichier PDF, pas de page. Dans les options, « Tous les formats » permet de mélanger les types.

Sur les JPEG éligibles et les PNG statiques RGB/RGBA 8 ou 16 bits éligibles, un premier aperçu apparaît avant le raffinement de la couleur ICC/écran. Les JPEG éligibles peuvent aussi affiner leur netteté. Le cadrage est conservé. Lors d’un déplacement entre écrans, la couleur se recalcule pour l’écran de destination ; l’image précédente reste provisoirement visible pendant ce calcul. Le zoom et le fond noir suivent l’aperçu. Le budget de mémoire graphique est géré automatiquement.

Le timecode audio et vidéo s’affiche en bas. Relâcher le raccourci ferme toujours l’aperçu et arrête la lecture. Avant interaction, déplacer la souris de plus de 10 pixels ferme aussi la vue si « Fermer l’aperçu quand la souris bouge » est activé dans les options. Désactivez cette option pour garder la vue jusqu’au relâchement du raccourci. Échap permet de la fermer.

Le raccourci se choisit par appui sur une touche ou une combinaison. Les options, la pause et le démarrage avec Windows sont accessibles depuis l’icône près de l’horloge.

## Commandes image et vidéo

- Redimensionnez l’aperçu : la dernière taille image et la dernière taille vidéo sont mémorisées séparément, même après redémarrage.
- **F** revient à la taille automatique adaptée à l’écran et oublie la taille mémorisée du type concerné.
- **Clic droit maintenu + déplacement** déplace la fenêtre d’aperçu.
- **B** active ou retire un fond noir sur tout le moniteur de l’aperçu. Ce choix est mémorisé. En mode raccourci + survol, B conserve le comportement transitoire : relâcher le raccourci ferme l’aperçu et le fond ; déplacer la souris les ferme également si cette option est activée.

Un petit arc cyan sur fond transparent apparaît près du pointeur pendant les chargements suffisamment longs, puis disparaît. La navigation entre images avec Espace et les flèches conserve l’image précédente et le fond jusqu’à ce que la nouvelle image soit prête.

## ASCII art : NFO, ASC et DIZ

Les fichiers NFO, ASC et DIZ disposent d’un aperçu dédié en blanc sur noir. Les caractères DOS CP437, les fichiers UTF-8 et UTF-16 avec BOM, les cadres et les blocs sont pris en charge. Les espaces et les colonnes restent alignés, sans retour automatique à la ligne.

La fenêtre fait **80 colonnes de large par défaut**, avec adaptation de la taille des caractères pour afficher toute la largeur des dessins plus larges. La molette permet de défiler verticalement. Les NFO, ASC et DIZ sont affichés passivement, sans interprétation des séquences ANSI. Les fichiers TXT conservent leur présentation texte habituelle.

## Dessins ANSI : ANS

Les fichiers **ANS** disposent d’un rendu statique en couleurs : caractères CP437 ou Unicode reconnu, styles, couleurs 16/256/RGB et commandes de placement. La grille utilise 80 colonnes par défaut ou la largeur SAUCE, jusqu’à 512 colonnes. Les passages de ligne après une rangée pleine et les déplacements horizontaux traversant le bord droit conservent l’alignement du dessin.

Sélectionnez **deux ANS puis Espace** pour afficher leurs dessins complets **côte à côte**, avec nom et information de chaque fichier en en-tête. Zoom et déplacement sont liés ; **I** inverse les dessins, **D** consulte la différence visuelle optionnelle et revient aux deux volets. Les codes sources ne sont pas éditables dans cette vue.

Il s’agit d’un lecteur de dessins, pas d’un terminal : pas d’exécution de commandes, son, animation, Sixel ou polices téléchargées. Lecture limitée à 8 Mio par fichier, 2 097 152 cellules, 32 768 rangées et un budget de traitement. Une police système est utilisée ; certains formats ou effets ANSI avancés ne sont pas reproduits.

## Comparer et modifier deux textes

Sélectionnez deux fichiers texte compatibles puis appuyez sur **Espace**. La fenêtre présente deux volets Scintilla éditables, les lignes numérotées et les différences visuelles. Le verdict identiques/différents compare le texte exactement, espaces compris ; il ne certifie pas l’identité binaire des fichiers.

- Copiez, collez et modifiez le texte dans chaque volet.
- Le défilement est lié par défaut ; une commande permet de le dissocier.
- La recherche commune en bas surligne toutes les occurrences dans les deux textes en cyan pendant la frappe. **Ctrl+F** rejoint la recherche ; **Entrée/F3** passe aux occurrences suivantes. La bascule permet des recherches séparées.
- Chaque en-tête propose sa propre sauvegarde et **Enregistrer sous**. Les changements non enregistrés sont protégés à la fermeture ; annuler un dialogue garde la fenêtre ouverte.
- Les textes ordinaires reviennent visuellement à la ligne suivant la largeur. Les dessins **NFO/ASC/DIZ** gardent leurs colonnes, avec tabulations de huit colonnes et caractères adaptés au volet.

Le comparateur charge les fichiers complets dans ses bornes : 8 Mio et 250 000 lignes par fichier. UTF-8, UTF-16 avec BOM, Windows-1252 et CP437 pour les dessins sont pris en charge avec contrôle de l’encodage à la sauvegarde. Les fichiers ANS utilisent la comparaison des dessins rendus, sans édition des codes.

## Comparer deux images

Sélectionnez deux JPEG ou PNG dans l’Explorateur ou sa Galerie, puis appuyez sur **Espace**. La fenêtre Pupitre affiche les deux images dans un cadrage commun.

- Faites glisser les deux chevrons centraux pour déplacer la séparation A/B.
- **D** bascule entre A/B et Différence ; le calcul de Différence commence à la demande.
- **I** inverse les images A et B.
- Le wipe est toujours orientable : faites glisser le petit rond plein au bout du bras latéral pour tourner la séparation. La touche S ne bascule plus entre deux types de wipe.
- **Ajuster** change l’alignement entre adaptation de B à A, coins supérieurs gauches et centrage. **F** recadre les images dans la fenêtre.
- Survolez les petits **ⓘ** en bas des images pour consulter les informations du fichier et sa profondeur source.
- Molette pour zoomer, déplacement lié des images et **Échap** pour fermer.

Les commandes du wipe et toute la ligne utilisent une ombre courte pour rester visibles sur une image blanche, avec des traits lissés et un petit rond plein.

Le comparateur accepte les JPEG éligibles et les PNG statiques RGB/RGBA 8 ou 16 bits éligibles jusqu’à **16 777 216 pixels**, notamment 4096 × 4096. Les PNG comportant de nombreux blocs de données sont pris en charge dans les bornes du lecteur ; palette, gris, tRNS, APNG et HDR restent hors sous-ensemble. Le canevas commun est réduit à 1 048 576 pixels au maximum, avec sortie SDR 8 bits. Cette limite d’entrée est propre au comparateur ; l’aperçu couleur différé simple garde sa borne de 8 388 608 pixels. Une différence noire ne prouve pas l’identité des fichiers originaux. Des saccades du séparateur restent signalées et leur correction est en cours.

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

Téléchargez l’installateur depuis les [Releases](https://github.com/tmnmy/VIEWEXP/releases/tag/v0.30.10), puis lancez-le. Il contient VIEWEXP et ImageMagick. Une connexion Internet est nécessaire à la première installation pour télécharger FFmpeg directement depuis [son fournisseur BtbN](https://github.com/BtbN/FFmpeg-Builds/releases/tag/autobuild-2026-09-30-13-08). L’archive et chaque binaire sont vérifiés par SHA-256. Vous n’avez pas à installer FFmpeg séparément.

L’installateur fait environ 40 Mo ; FFmpeg représente environ 77 Mo supplémentaires. Une mise à jour réutilise les fichiers FFmpeg conformes et conserve les réglages ainsi que le choix de démarrage avec Windows. Si la préparation échoue, l’installation existante est conservée.

À partir de la 0.13.0, VIEWEXP recherche les nouvelles versions sur GitHub en arrière-plan. Une notification et le menu de l’icône signalent une version disponible. Le téléchargement de l’installateur commence à votre clic sur « Installer VIEWEXP… ». Autorisez les connexions de VIEWEXP dans votre pare-feu pour utiliser cette fonction.

La 0.13.3 a corrigé un blocage lorsque le menu de l’icône reste ouvert pendant une mise à jour. Si le remplacement échoue et que l’installation précédente est entièrement restaurée, l’installateur tente de relancer cette version. L’erreur précise reste disponible dans le journal local.

Les versions antérieures à la 0.13.0 nécessitent une première mise à jour manuelle. Le téléchargement initial de FFmpeg depuis l’installateur reste à qualifier sur une installation neuve ; les tests d’installation utilisent l’archive officielle vérifiée ou un runtime déjà conforme.

## Limites actuelles

- Un test automatique exigeant la sortie de l’installateur en trois secondes a échoué sur la 0.29.18 et reste à diagnostiquer. Ce scénario de délai n’a pas été requalifié sur la 0.30.10 ; l’installation réelle de cette version, le redémarrage et la conservation des réglages ont été vérifiés.

- Comparateur : des saccades peuvent persister pendant le glissement ou la rotation du séparateur.

- Vidéo limitée à 1080p et 30 images/s.
- 3D : maillages statiques et couleurs simples ; pas de textures ni d’animations.
- Images multipages ou multicouches : première image ou composite disponible. Les PDF disposent de leur navigation entre pages.
- Texte : aperçu des huit premiers Mio, encodages UTF-8, UTF-16 avec BOM ou Windows-1252. DOCX, XLSX, RTF et EPUB non pris en charge.
- PDF : fichier de 256 Mio et 10 000 pages maximum ; pas de demande de mot de passe.
- La couleur ICC/écran différée est activée sur les JPEG éligibles et les PNG statiques RGB/RGBA 8 ou 16 bits jusqu’à 8 388 608 pixels et 65 536 pixels de largeur. PNG palette, gris, tRNS et APNG : rendu habituel. Autres formats hors sous-ensemble : rendu habituel. Pas de certification colorimétrique instrumentale ni de garantie de fidélité HDR pour l’étalonnage.
- Fichiers locaux uniquement ; téléchargez les fichiers cloud avant de les prévisualiser.
- Installateur non signé. Qualification sous Windows 11 x64 ; parcours JPG/PNG transparent, zoom et fond noir acceptés sur trois écrans à 100 % et 150 %. Cela ne certifie pas tous les moniteurs ni tous les profils ICC.

## Code et licences

Le code source de VIEWEXP reste privé. Ce dépôt contient la documentation, les installateurs et les signalements de problèmes.

L’application utilise notamment [ImageMagick](https://imagemagick.org/), [FFmpeg](https://ffmpeg.org/) et [ufbx](https://github.com/ufbx/ufbx), LittleCMS et [Scintilla](https://www.scintilla.org/). Les licences, attributions et références de sources tierces accompagnent l’installation. FFmpeg et ses DLL sont téléchargés chez leur fournisseur et restent remplaçables dans le dossier installé.

La 0.17.1 corrige notamment l’audio avec Espace, la réouverture du même fichier et les aperçus TypeScript. Les options deviennent défilables sur les petits écrans. La préparation des aperçus texte utilise moins d’allocations.

Avec Espace, le média est centré sur l’écran de la fenêtre source, indépendamment de la souris. En mode transparent, le cadre initial centré est limité à 1 200 × 800 pixels. Les petites images restent à 100 % à l’ouverture ; zoom et redimensionnement volontaire permettent ensuite de les agrandir.

