# Historique des versions

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
