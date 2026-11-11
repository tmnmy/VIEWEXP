# Historique des versions

## 0.29.20

- Ombre Contact sur les chevrons, le bras, le rond et toute la ligne de séparation, à la place des contours sombres ; tracés lissés.
- Petit rond plein à l’extrémité du bras pour la rotation. Le wipe est toujours orientable, y compris à la verticale ; la bascule S entre deux types de wipe est retirée.
- Comparaison des PNG statiques RGB/RGBA 8 ou 16 bits jusqu’à 16 777 216 pixels, notamment 4096 × 4096, avec un lecteur acceptant davantage de blocs de données. Les bornes de l’aperçu couleur simple restent inchangées.
- Message d’erreur de comparaison lisible, sans traces de préparation internes.
- Rafraîchissement partiel et composition des petites commandes améliorés pour réduire le travail de dessin pendant le glissement. La fluidité réelle reste à qualifier ; des saccades peuvent persister.
- Commandes D, I, F et Ajuster conservées, ainsi que zoom lié, déplacement et informations au survol.
- Sortie SDR 8 bits et canevas de comparaison réduit à 1 MP conservés ; pas de preuve d’identité par une différence noire, ni de HDR. Réserve connue sur un test de délai de l’installateur, détaillée dans les notes de release.

## 0.29.14

- Nouveau comparateur Pupitre : sélectionner deux JPEG/PNG puis Espace, y compris dans la Galerie de l’Explorateur.
- Séparation A/B manipulable directement, mode Différence avec D, inversion avec I et séparation inclinable avec S.
- Trois alignements avec Ajuster pour comparer des images de dimensions différentes ; zoom et déplacement liés.
- Informations au survol des ⓘ, indiquant la profondeur de la source. Icônes réduites et cadre rectangulaire supprimé dans cette version.
- PNG statiques RGB/RGBA 16 bits bornés pris en charge dans l’aperçu simple et la comparaison, avec conservation de la précision source avant réduction ; sortie SDR 8 bits.
- Ouverture A/B avant le calcul de Différence à la demande. Améliorations de cache de rendu du séparateur, sans garantie de fluidité complète : des saccades restent signalées.
- Limites : canevas de comparaison réduit à 1 MP, pas de HDR ni de preuve d’identité par une différence noire. Installateur Windows x64 non signé.

## 0.28.17

- Aperçus déplacés entre écrans : cadrage, zoom, fond noir et choix du moniteur cohérents ; recalcul du rendu couleur pour l’écran de destination sans fermeture de l’aperçu.
- Couleur ICC/écran différée pour les PNG statiques RGB/RGBA 8 bits éligibles, jusqu’à 8 388 608 pixels et 65 536 pixels de largeur, avec conservation de l’alpha. Première image provisoire avant conversion ; autres PNG au rendu historique.
- Récupération des captures clavier/souris après changement de bureau Windows, livrée en 0.28.15 ; reprise après verrouillage/déverrouillage confirmée.
- Validation des chemins locaux audio/vidéo/PDF renforcée en 0.28.16 ; fichiers réseau toujours hors périmètre.
- Parcours JPG/PNG, fond et zoom acceptés sur trois écrans ; reprise après redémarrage d’Explorer, loader transparent/fluide et délai JPEG acceptés.
- Réglages et démarrage avec Windows conservés. Installateur non signé ; aucune certification HDR ou colorimétrique instrumentale.

## 0.28.14

VIEWEXP 0.28.14 ajoute les aperçus ASCII art et plusieurs corrections depuis la 0.28.12.

### Aperçus ASCII art

- Lecture des fichiers NFO, ASC et DIZ en blanc sur noir.
- Caractères DOS CP437, UTF-8 et UTF-16 avec BOM ; cadres, blocs et accents préservés.
- Grille fixe sans retour automatique à la ligne et sans numérotation ajoutée au dessin.
- Fenêtre de 80 colonnes par défaut ; taille des caractères adaptée pour montrer toute la largeur des dessins plus larges.
- Défilement vertical à la molette.
- Métadonnées SAUCE retirées du dessin lorsqu’elles sont valides.
- Lecture passive, sans interprétation ANSI ni exécution de commandes.

La largeur et le maintien du dessin entier ont été confirmés par l’utilisateur sur la 0.28.14.

### Fiabilité

La dernière demande d’aperçu est conservée lorsque le décodeur est occupé, au lieu d’être perdue lorsque la file est pleine. Les contrôles d’annulation et de résultats périmés sont préservés.

### Installation et limites

Windows 11 x64. Réglages et démarrage automatique conservés lors de la mise à jour. Installateur non signé. Un runtime FFmpeg conforme est réutilisé ; sinon, il est téléchargé depuis son fournisseur.

Les limites existantes du README restent applicables. La forme des glyphes Unicode hors DOS dépend des polices Windows disponibles. Les fichiers exceptionnellement larges peuvent dépasser les capacités du plus petit caractère natif ; les limites et troncatures sont signalées.

Vérifications : 498 tests standards initiaux, puis contrôles ciblés après revue. Le correctif final de largeur passe 20 tests bibliothèque et 21 tests d’intégration. Les rasters natifs ont été inspectés.

Télécharger `VIEWEXP-0.28.14-Installer.exe`. L’empreinte SHA-256 figure dans `SHA256SUMS.txt`.

## 0.28.12

VIEWEXP 0.28.12 regroupe les améliorations d’aperçu et les corrections depuis la 0.26.1.

### Aperçus image et vidéo

- Taille mémorisée séparément pour les images et les vidéos, conservée après redémarrage.
- F rétablit la taille automatique adaptée à l’écran et efface la taille mémorisée du type concerné.
- Déplacement de la fenêtre par clic droit maintenu.
- Fond noir plein écran avec B, choix mémorisé.
- En mode raccourci + survol, B répond dans le contexte source et conserve la fermeture au déplacement de la souris ou au relâchement du raccourci.
- Navigation entre images : image et fond conservés jusqu’à l’affichage du fichier suivant.
- Petit indicateur de chargement transparent près de la souris, avec rotation affinée.

### Rendu et fiabilité

- Première image JPEG suivie du raffinement de la couleur ICC/écran pour les fichiers éligibles.
- Lecture du fichier exact pour les noms contenant des caractères spéciaux, notamment %d.
- Récupération prudente des nouveaux temporaires de décodage après interruption.
- Gestion améliorée des notifications secteur/batterie, des budgets de téléchargement et des dialogues d’erreur.

### Installation et vérification

Windows 11 x64. Réglages et démarrage automatique conservés lors de la mise à jour. Installateur non signé. FFmpeg est téléchargé depuis son fournisseur si aucun runtime conforme n’est déjà installé.

475 tests standards réussis, plus les contrôles natifs ciblés du fond noir image/couleur/vidéo et de la fermeture au déplacement. La confirmation visuelle utilisateur du dernier correctif de survol et du loader reste distincte des résultats automatisés. La qualification matérielle multi-écrans/DPI et les limites couleur/HDR décrites dans le README restent applicables.

Télécharger `VIEWEXP-0.28.12-Installer.exe`. Son empreinte SHA-256 est fournie dans `SHA256SUMS.txt`.

## 0.26.1

Cette version rassemble les améliorations ajoutées depuis la 0.17.2.

- Les images ouvertes avec Espace, ou après un cran de molette en mode survol, se redimensionnent en tirant un coin avec le clic gauche. Les proportions et le cadrage sont conservés. Le correctif du clic de la 0.26.1 a été confirmé à l’usage.
- Les grandes photos JPEG peuvent apparaître rapidement sous forme d’aperçu, puis gagner en netteté. Le passage à l’image affinée conserve le cadrage et les protections contre une ancienne image.
- Le budget de mémoire graphique propose un réglage automatique.
- Les PDF disposent d’une fenêtre redimensionnable, du plein écran, du déplacement par le cadre, d’un bouton Imprimer et d’une barre de défilement pour les documents de plusieurs pages. La molette fonctionne aussi lorsque le pointeur reste sur le fichier source pendant le survol.
- Avec Espace, les flèches gauche et droite ouvrent le fichier précédent ou suivant. Par défaut, les images restent entre images et les PDF entre PDF ; une préférence permet de parcourir tous les formats.
- Audio et vidéo : barre de lecture adaptée à l’aperçu, lecture/pause, progression cliquable, timecode et bouton son mémorisé. L’aperçu 3D indique le nombre de triangles.
- Plusieurs corrections portent sur les options, les ressources des PDF et la stabilité Windows.

Les petites images restent à 100 % à l’ouverture. Le zoom et le redimensionnement volontaire permettent ensuite de les agrandir. En survol, relâcher le raccourci ferme toujours l’aperçu ; avec Espace, il reste ouvert jusqu’à Espace ou Échap.

Qualification de ce paquet : 327 tests standards et contrôles natifs ciblés réussis ; coins confirmés par l’utilisateur. Le rendu couleur ICC/écran avancé reste en préparation et n’est pas activé. Pas de garantie d’étalonnage HDR.

Windows x64. Installateur d’environ 38 Mo, non signé. Réglages et démarrage Windows conservés lors d’une mise à jour. FFmpeg est téléchargé chez son fournisseur lors d’une première installation si aucun runtime conforme n’est déjà présent. Code source privé.

## 0.17.2

- Aperçus Espace centrés sur le moniteur de la fenêtre source, indépendamment du pointeur.
- Fond transparent et limite 1 200 × 800 conservés dans le mode correspondant, avec contenu centré.
- Petites images à 100 %, grandes images ajustées et placement au survol préservés.

## 0.17.1

- Audio et réouverture du même fichier corrigés en mode Espace.
- Capture d’Échap et annulation des demandes de chargement coordonnées.
- Distinction TypeScript et vidéos MPEG-TS pour les fichiers .ts.
- Options adaptées aux petites zones de travail avec défilement et focus clavier visible.
- Budget glTF vérifié avant allocation, numéros de lignes et synchronisation GDI corrigés.
- Moins d’allocations dans la préparation des textes, avec mesures CPU avant/après.
- Paquets construits dans un dossier neuf, contenu autorisé exact, manifeste complet et intégrité des décodeurs contrôlée.

## 0.17.0

- Aperçu du fichier sélectionné avec Espace ; Espace à nouveau ou Échap ferme.
- Vue conservée après relâchement et mouvement de souris, avec les interactions existantes.
- Protection des champs de saisie, des combinaisons de touches et de la répétition automatique.
- Annulation des chargements en cours et vérification de la sélection avant affichage.
- Mode survol et commandes des médias conservés.

## 0.16.1

- Clic gauche après un cran de molette : même rotation autour du modèle que le bouton central, avec les axes inversés déjà retenus.
- Remplace le déplacement dans le cadre de la 0.16.0 conformément au geste demandé.
- Zoom, fermeture au relâchement du raccourci et commandes des autres médias conservés.

## 0.16.0

- Après un cran de molette, clic gauche maintenu pour déplacer le modèle 3D dans le cadre sans fermer l’aperçu.
- Rotation au bouton central et zoom à la molette conservés ; cadrage réinitialisé pour chaque nouvel objet.
- Fermeture au relâchement du raccourci conservée.

## 0.15.0

- Son des vidéos activé par défaut, sans changement du volume système.
- Audio et image déplacés ensemble à la molette et arrêtés à la fermeture de l’aperçu.
- Cadencement vidéo sur l’horloge de la sortie audio, préparation silencieuse et protection contre les résultats périmés.
- Vidéos sans piste audio conservées ; libellés et diagnostic mis à jour.
- BLEND, orbite inversée, réglages et correctifs d’installation précédents conservés.

## 0.14.0

- Aperçu 3D interactif des fichiers BLEND via le Blender installé, avec scripts automatiques désactivés, chargement borné et cache mémoire.
- Orbite 3D : sens du glissement horizontal et vertical inversé ; bouton central et zoom à la molette conservés.
- BLEND : maillages enregistrés uniquement ; modificateurs, textures et animations non évalués. Blender non inclus dans l’installateur.
- Réglages, démarrage Windows et correctifs de mise à jour 0.13.3 conservés.

## 0.13.3

- Correction d’un blocage de l’arrêt lorsque le menu de l’icône reste ouvert pendant une mise à jour, y compris depuis les anciennes versions.
- Relance de l’ancienne application si le remplacement échoue et que sa restauration est complète et vérifiée.
- Conservation du diagnostic de l’installateur dans le journal local, même en mode silencieux ; code de sortie ajouté au message d’échec.
- Réglages et démarrage Windows conservés. Aucun changement des commandes d’aperçu.

## 0.13.2

- Damier derrière les zones transparentes des images, en plein écran et près du pointeur.
- PDF ajustés en largeur ; défilement au clic gauche maintenu et glissement pour les PDF et les textes. Taille et glissement validés par l’utilisateur en 0.13.1.
- Aperçus texte et code sans exécution, avec défilement à la molette et prise en charge d’UTF-8, UTF-16 avec BOM et Windows-1252.
- Lecture audio avec son ; molette audio/vidéo par sauts de cinq secondes et timecode en bas.
- Aperçus OBJ, STL, GLB, glTF et FBX : rotation au bouton central, zoom à la molette. Maillages statiques sans textures ni animations.
- Recherche des releases stables sur GitHub et commande d’installation depuis le menu de l’application. Aucun téléchargement d’installateur sans clic de l’utilisateur.
- 130 tests automatiques réussis, avec des tests natifs supplémentaires de transparence, de rendu, de remplacement d’image et d’installation.

Le premier téléchargement de FFmpeg depuis l’installateur et le cycle de mise à jour depuis une version publique antérieure restent à qualifier de bout en bout. L’installateur n’est pas signé.

## 0.10.1 — Préversion publique

- Installateur d’environ 35 Mo ; FFmpeg est téléchargé directement depuis son fournisseur à la première installation (environ 77 Mo).
- Vérification SHA-256 de l’archive et des neuf binaires FFmpeg avant installation.
- Réutilisation hors ligne d’un FFmpeg déjà installé si ses fichiers sont conformes.
- Installation existante conservée en cas d’échec du téléchargement.
- Travail d’installation effectué en arrière-plan pour garder la fenêtre réactive.
- 91 tests automatiques réussis, test du rendu vidéo dans les deux modes et vérification de l’installateur final en emplacement isolé.

Le téléchargement initial de FFmpeg reste à confirmer de bout en bout depuis l’installateur. La connexion native a été refusée dans l’environnement de test ; les tests d’installation utilisent l’archive officielle dont l’empreinte a été vérifiée. L’installateur n’est pas signé.

## 0.10.0 — Version locale

- Lecture vidéo automatique, sans son et en boucle, limitée à 1080p et 30 images/s maximum.
- MP4 H.264, MKV, MOV ProRes/DNxHR et WebM VP9 vérifiés.
- Même raccourci personnalisable et mêmes modes d’affichage que pour les images.
- Fermeture au relâchement du raccourci ; zoom à la molette et déplacement au clic gauche ou central.
- FFmpeg intégré à l’installateur autonome, sans installation séparée.
- Lecture et fermeture validées lors d’un essai utilisateur sur Windows.

La version locale 0.10.0 n’a pas été publiée. La distribution publique commence avec la préversion 0.10.1, dont l’installateur télécharge FFmpeg auprès du fournisseur.
