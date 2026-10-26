# Historique des versions

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
