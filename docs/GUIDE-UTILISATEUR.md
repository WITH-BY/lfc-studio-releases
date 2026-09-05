# Guide d'utilisation — LIGHTFORMCOLOR Studio

**Préversion `1.0.0-beta.9`.** Ce guide décrit ce que le Studio fait
aujourd'hui. Ce qui n'est pas encore qualifié est signalé comme tel, à
l'endroit où vous le rencontrerez.

Pour installer : [macOS](INSTALLATION-MACOS.md) · [Windows](INSTALLATION-WINDOWS.md).

---

## 1. Ce que fait le Studio

Le Studio prépare des images et des vidéos, les adapte au format exact de vos
écrans **LFC Tube**, puis les envoie et les programme.

Le principe : vous travaillez sur une **composition** dans le Studio, vous
associez chaque **écran de sortie** à un appareil, et le Studio se charge du
reste — redimensionnement, conversion vidéo, transfert, lecture.

Six onglets, dans la colonne de gauche :

| Onglet | À quoi il sert |
| --- | --- |
| **Accueil** | l'état du parc en un coup d'œil, allumer/éteindre, appliquer les changements en attente |
| **Contenus** | la bibliothèque : importer, composer, dupliquer, ranger |
| **Planning** | le calendrier : ce qui passe, quel jour, à quelle heure, et les plages de veille |
| **Live** | la régie événementielle — **démonstration uniquement** dans cette bêta |
| **Appareils** | le parc : ajouter, nommer, regrouper, retirer |
| **Réglages** | langue, thème, sauvegarde, stockage, mise à jour |

`⌘K` (macOS) ou `Ctrl+K` (Windows) ouvre la **palette de commandes** : tapez le
nom d'un écran ou d'une action pour y aller directement.

---

## 2. Ajouter votre premier appareil

Branchez le LFC Tube sur le même réseau que votre ordinateur, puis :

1. Onglet **Appareils** → **Ajouter un appareil** → **LFC Tube**.
2. Le Studio cherche seul sur le réseau. **Vous n'avez aucune adresse IP à
   saisir.**
3. Choisissez l'appareil trouvé. Sa taille, sa résolution et son numéro de
   série sont lus directement sur le matériel.
4. Donnez-lui un nom parlant — c'est celui que vous verrez dans le planning
   (« Vitrine », « Entrée », « Scène jardin »).

### Si l'appareil n'apparaît pas

- Vérifiez que l'ordinateur et l'appareil sont sur **le même réseau**. Un
  réseau « invité » ou une isolation entre clients Wi-Fi les sépare.
- Vérifiez que vous avez autorisé le **réseau local** (macOS) ou le
  **pare-feu en réseau privé** (Windows) — voir les guides d'installation.
- Premier branchement, appareil jamais configuré : il diffuse son propre réseau
  de configuration. Rejoignez-le avec le mot de passe usine `88888888`.
  L'absence d'Internet sur ce réseau est normale, le Studio vérifie
  automatiquement l'adresse `192.168.43.1`.

### Protéger l'appareil

Le Studio propose un **code d'accès de 4 à 8 chiffres**. Il est demandé
uniquement pour ajouter ce même appareil à un **autre** Studio. Il est conservé
dans le trousseau macOS ou le gestionnaire d'identifiants Windows — jamais dans
un projet exporté, jamais dans une sauvegarde.

### Ranger le parc

**Groupes d'appareils** : rangez par lieu ou par installation (« Vitrine »,
« Étage 1 », « Client Dupont ») pour les retrouver et les piloter ensemble.

**Allumer en bleu** identifie physiquement un appareil dans une installation où
plusieurs se ressemblent.

---

## 3. Importer des contenus

Onglet **Contenus** → **Importer**, ou glissez vos fichiers directement dans la
fenêtre.

**Images** : png, jpg, jpeg, webp, gif, bmp, tiff, heic.
**Vidéos** : mp4, mov, m4v, webm, avi, mkv.

### Dossiers suivis

**Ajouter un dossier** déclare un dossier de votre disque comme source. Le
Studio le relit à chaque ouverture de la bibliothèque et propose les nouveaux
médias. Pratique quand un tiers dépose ses visuels dans un dossier partagé.

Cesser de suivre un dossier ne supprime rien : les contenus déjà importés
restent dans la bibliothèque.

### Ranger et filtrer

- **Dossiers** : classez vos contenus, filtrez la galerie par dossier.
- **Filtrer par appareil** : n'affiche que les contenus au format d'un appareil
  donné.
- Un contenu peut porter la mention *format sans appareil compatible* : aucun
  appareil du parc ne correspond exactement à ses dimensions.

---

## 4. Composer

Une **composition** assemble des calques (images, vidéos, textes, formes) et
les répartit sur un ou plusieurs **écrans de sortie**.

**Contenus** → **Nouvelle composition**, ou sélectionnez un média et créez une
composition à partir de lui. Le média d'origine **reste dans la galerie** : les
modifications ne concernent que la composition.

### Les écrans de sortie (frames)

C'est la notion centrale. Une frame = un écran physique.

1. Panneau **Écrans de sortie** → ajoutez une frame par appareil.
2. **Appareil associé** : le Studio reprend automatiquement sa résolution, son
   orientation et son nombre de modules. La frame se déplace et pivote, elle ne
   se redimensionne pas.
3. Placez vos calques sur le plan de travail. Un calque n'est rendu que dans
   les frames cochées dans **Frames de sortie**.

Une frame affiche son état : **Valide**, **Avertissement**, ou **Incomplète**
(par exemple si aucun appareil ne lui est associé).

Ce mécanisme permet une image continue répartie sur plusieurs tubes : vous
composez une seule fois, chaque appareil reçoit sa découpe.

### Calques et outils

Barre du haut : **Image**, **Vidéo**, **Texte** (`T`), **Rectangle** (`R`),
**Ellipse** (`O`).

Raccourcis dans l'éditeur :

| Raccourci | Effet |
| --- | --- |
| `⌘Z` / `⇧⌘Z` | annuler / rétablir |
| `⌘A` | tout sélectionner |
| `⌘]` / `⌘[` | avancer / reculer d'un rang |
| `⇧⌘]` / `⇧⌘[` | mettre au premier / dernier plan |
| `⌘0` | zoom 100 % |
| `⌘1` | ajuster à la fenêtre |
| Flèches | déplacer de 1 px (`⇧` : 10 px) |
| `Alt` + `←` / `→` | décaler dans le temps de 0,1 s (`⇧` : 1 s) |
| `Espace` | lecture / pause |
| `Retour arrière` | supprimer la sélection |
| `Échap` | désélectionner |

Sur Windows, remplacez `⌘` par `Ctrl`.

### Timeline

Chaque calque a sa place dans le temps. La coupe est **non destructive** :
raccourcir un clip ne touche pas le fichier source.

Une composition ne peut pas dépasser **1 heure**. Au-delà de la borne *Fin*,
les calques sont coupés à la lecture et à l'export, sans être supprimés.

### Aperçu

Deux aperçus : **Tube 3D** (le rendu sur le luminaire) et **LED** (la matrice à
plat, pour vérifier la lisibilité pixel par pixel).

### Dupliquer avant de modifier

**Dupliquer et modifier** conserve la version actuelle et ouvre une copie. Les
médias ne sont pas recopiés : le duplicata réutilise les mêmes fichiers
sources, sans coûter d'espace disque.

L'historique annuler/rétablir est propre à la composition ouverte : passer
d'une composition à l'autre le remet à zéro.

### Polices

**Noto Sans** est la seule police portable. Les projets historiques conservent
leur police FT Polar : l'aperçu utilise Noto Sans et affiche un avertissement,
et l'export portable comme la préparation de diffusion **refusent** ces calques.
Choisissez explicitement Noto Sans dans l'éditeur pour les convertir.

---

## 5. Diffuser maintenant

Bouton **Diffuser**, depuis l'Accueil ou depuis un contenu. Trois étapes :

1. **Appareils** — un ou plusieurs. Un écran éteint mais joignable sera rallumé
   automatiquement. Cochez **Synchroniser la lecture** pour que les contenus
   démarrent ensemble ; un seul groupe synchronisé est actif à la fois sur le
   réseau.
2. **Playlist** — cliquez les contenus dans l'ordre voulu. La liste entière est
   répétée en boucle.
3. **Durée** — sans limite, jusqu'au prochain événement du planning, ou
   jusqu'à la prochaine veille.

Puis **Diffuser maintenant**.

Toute vidéo est **convertie avant l'envoi** au format que le contrôleur
accepte : H.264, 30 images/s, sans B-frames. Cette conversion prend un moment
sur les fichiers longs. Si les outils vidéo embarqués sont absents ou
invérifiables, l'envoi est **bloqué** plutôt que tenté à l'aveugle.

Le Studio ne déclare jamais une diffusion réussie sans confirmation de
l'appareil. Une diffusion partielle est annoncée comme partielle, avec la liste
des appareils sans confirmation.

---

## 6. Programmer

Onglet **Planning** : une grille hebdomadaire, un appareil ou plusieurs.

- **Programmation** : une playlist, des jours, une plage horaire. Les heures
  sont celles de votre fuseau, en heure civile locale.
- **Veille** : l'écran s'éteint, les contenus restent en mémoire dans
  l'appareil. Un contenu programmé sur ces heures **passe devant** la veille.
  L'extinction et le rallumage doivent être à deux heures différentes.

Les modifications sont enregistrées dans le Studio même si un appareil est
hors ligne. L'Accueil affiche alors *« n appareils à synchroniser »* et
**Appliquer maintenant** les pousse dès qu'ils sont joignables.

---

## 7. Live — démonstration

L'onglet **Live** prépare des scénographies : des scènes préchargées sur
plusieurs appareils, déclenchées le jour J.

**Dans cette bêta, le Live est une démonstration.** Le déclenchement est
coordonné au mieux par le réseau local ; aucune précision matérielle n'est
garantie tant que le firmware n'est pas qualifié. Ne l'utilisez pas comme régie
d'un événement réel.

Un appareil réservé au Live refuse les diffusions manuelles et les
modifications de planning tant que vous n'avez pas restauré son planning depuis
l'onglet Live. C'est volontaire : cela évite d'écraser une scène préparée.

---

## 8. Projets et sauvegardes

Deux formats, deux usages différents :

**`.lfcproject` — partager une création.** Contient les médias, les dossiers,
le planning, les frames et le profil de police. Il ne contient **ni adresse IP,
ni numéro de série, ni identité du parc source** : vous pouvez l'envoyer à un
tiers sans exposer votre installation.

**`.lfcstudio` — sauvegarder votre configuration.** Réglages → **Sauvegarder la
configuration**. Exporte le parc, les créations, les scènes et les plannings.
Les médias restent à leur emplacement sur le disque ; la sauvegarde les
référence, elle ne les recopie pas.

Limites d'un projet : 4 096 médias, 16 Gio par média, 64 Gio au total,
5 000 contenus, 2 000 programmations, 500 éléments par playlist et 500 calques
par contenu. Les projets des versions précédentes restent importables.

---

## 9. Réglages

- **Langue** : français ou anglais. **Thème** : clair, sombre ou système.
- **Stockage du Studio** : ce que prennent les données et les fichiers
  temporaires, avec la possibilité de vider le cache.
- **Mise à jour du logiciel** : affiche *Canal de mise à jour non configuré*.
  C'est exact — aucun flux signé n'est publié pour cette bêta, et rien n'est
  simulé. Les mises à jour se font en réinstallant la version suivante.
- **Assistance à distance** : affiche *Service non configuré*. Aucune
  infrastructure n'y est reliée, aucun port ni tunnel n'est ouvert.
- **Effacer les données locales** : supprime le parc, la bibliothèque et le
  planning de cet ordinateur. Les programmes déjà stockés **dans les appareils**
  ne sont pas modifiés.

---

## 10. Retirer un appareil

Onglet **Appareils** → **Retirer du parc**. Deux choix, aux conséquences
différentes :

- **Retirer seulement de ce parc** — le contenu, le Wi-Fi et le code d'accès
  restent sur l'appareil. Il continue de diffuser ce qu'il a en mémoire et
  reste détectable sur le réseau.
- **Préparer pour une autre personne** — efface le code d'accès et le réseau
  Wi-Fi enregistré, et conserve le point d'accès de configuration pour le
  prochain propriétaire. Les médias déjà présents dans l'appareil ne sont pas
  présentés comme effacés : il ne s'agit pas d'une remise à zéro usine.

---

## Limites de cette préversion

À garder en tête avant tout usage en production :

- l'onglet **Live** est une démonstration, non qualifiée sur firmware ;
- **aucune mise à jour automatique** : ni sur macOS ni sur Windows ;
- **aucune assistance à distance** : le service n'est relié à rien ;
- les paquets ne sont **pas signés** (ni Developer ID Apple, ni Authenticode) ;
- le **LFC Tube C16H** est le seul appareil piloté ; les autres géométries sont
  décrites mais n'ont pas de pilote qualifié ;
- la recette matérielle complète reste à faire avant une version stable.

---

## En cas de problème

Ouvrir une [issue](https://github.com/WITH-BY/lfc-studio-releases/issues) en
indiquant votre système, la version du Studio, ce que vous attendiez et ce qui
s'est passé. Le message d'erreur exact affiché par le Studio est l'information
la plus utile.
