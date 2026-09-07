# Guide d'utilisation

LIGHTFORMCOLOR Studio prépare vos images et vos vidéos, les met au format de vos
écrans LFC, puis les envoie et les programme.

Installation : [macOS](INSTALLATION-MACOS.md), [Windows](INSTALLATION-WINDOWS.md).

---

Commencez par **[Votre première utilisation](PREMIERS-PAS.md)** pour configurer le Wi-Fi de secours et découvrir le tutoriel. Ce guide décrit la candidate **1.0.0-beta.13** ; les versions précédentes peuvent différer.

## Organisation de l'application

Vous composez dans le Studio, vous indiquez quel écran reçoit quoi, le Studio
effectue le redimensionnement, la conversion vidéo, l'envoi et la lecture.

| Onglet | Contenu |
| --- | --- |
| Accueil | État des appareils, allumage et extinction, application des changements en attente |
| Contenus | Import des images et vidéos, création des compositions, classement |
| Planning | Programmation par jour et par horaire, plages d'extinction |
| Live | Démonstration de séquences préparées ; pilotage réel désactivé |
| Appareils | Ajout, dénomination, regroupement |
| Réglages | Langue, thème, sauvegarde |

`⌘K` sur Mac, `Ctrl+K` sur Windows, ouvre une recherche : saisissez le nom d'un
écran ou d'une action pour y accéder directement.

---

## Ajouter un appareil

Raccordez le LFC Tube au même réseau que votre ordinateur.

1. Onglet **Appareils**, **Ajouter un appareil**, **LFC Tube**.
2. Le Studio recherche les appareils présents. Aucune adresse n'est à saisir.
3. Sélectionnez l'appareil. Sa taille, sa résolution et son numéro de série sont
   lus sur le matériel.
4. Attribuez-lui un nom, qui apparaîtra dans le planning.

### L'appareil n'apparaît pas

Vérifiez que l'ordinateur et l'appareil sont sur le même réseau. Un réseau
invité, ou un réseau isolant ses clients, les sépare.

Vérifiez l'autorisation d'accès au réseau local, décrite dans les guides
d'installation. C'est la cause la plus fréquente.

S'il s'agit d'un premier démarrage, l'appareil n'est raccordé à aucun réseau et
diffuse le sien. Son nom et son mot de passe s'affichent sur l'appareil au
premier allumage, et à ce moment seulement. Notez-les. Rejoignez ce réseau
depuis les réglages Wi-Fi de votre ordinateur, puis revenez dans le Studio.
L'absence d'accès Internet sur ce réseau est normale.

### Code d'accès

Le Studio propose un code de 4 à 8 chiffres. Il n'est demandé que pour ajouter
l'appareil à un autre ordinateur. Il est conservé dans le trousseau de votre
système et n'est jamais inclus dans un projet exporté.

### Accès de secours

Pendant la première installation, le nom choisi pour le Tube devient son nom Wi-Fi : **Salon → LFC-Salon**. Vous créez un nouveau mot de passe et vérifiez la connexion avant de poursuivre. Le Studio maintient le point d’accès actif quand le Tube rejoint ou oublie son réseau habituel.

Dans **Appareils → Accès de secours**, retrouvez le nom et le mot de passe mémorisés, **même hors ligne**. L’œil révèle la clé. Les identifiants restent dans le coffre sécurisé du compte utilisateur de cet ordinateur ; ils ne sont pas exportés dans les projets ni les sauvegardes.

Vous pouvez modifier ces réglages lorsque le Tube est joignable. Si le changement coupe la connexion avant sa confirmation, le Studio conserve le dernier accès vérifié et la nouvelle proposition. Rejoignez le réseau indiqué depuis le menu Wi-Fi de l’ordinateur, puis relisez l’appareil pour confirmer. Le [parcours illustré par les étapes](PREMIERS-PAS.md#2-choisir-son-nom-et-son-accès-de-secours) détaille cette reprise.

Si l’adresse de l’appareil change, le Studio vérifie sa nouvelle adresse. Un appareil protégé peut demander une confirmation avant de réutiliser un accès mémorisé.

### Groupes

Les groupes rassemblent les appareils par emplacement ou par installation. Vous
les retrouvez et les pilotez ensemble.

**Allumer en bleu** identifie physiquement un appareil parmi plusieurs.

---

## Importer des contenus

Onglet **Contenus**, bouton **Importer**, ou glissement des fichiers dans la
fenêtre.

Images : png, jpg, webp, gif, bmp, tiff, heic.
Vidéos : mp4, mov, m4v, webm, avi, mkv.

### Dossiers suivis

**Ajouter un dossier** déclare un dossier de votre disque comme source. Le Studio
le relit à chaque ouverture des Contenus et propose les nouveaux fichiers.

Cesser de suivre un dossier ne supprime pas les contenus déjà importés.

### Classement

Classez les contenus dans des dossiers et filtrez la galerie. Le filtre par
appareil n'affiche que les contenus au format correspondant.

La mention « format sans appareil compatible » indique qu'aucun appareil du parc
ne correspond aux dimensions du contenu.

---

## Composer

Une composition assemble images, vidéos, textes et formes, et les répartit sur
un ou plusieurs écrans.

Depuis **Contenus**, **Nouvelle composition**. Le Studio demande l'appareil de
destination et applique son format et son orientation. Une composition peut
également être créée à partir d'un contenu existant, qui reste inchangé dans la
galerie.

### Écrans de sortie

Un écran de sortie représente un écran physique.

Dans le panneau **Écrans de sortie**, ajoutez-en un par appareil. Le Studio
reprend sa résolution et son orientation. Chaque élément placé sur le plan de
travail n'est affiché que sur les écrans sélectionnés.

Ce mécanisme permet de répartir une image continue sur plusieurs appareils.
Chaque écran de sortie peut être positionné et orienté librement.

### Outils et raccourcis

Barre supérieure : Image, Vidéo, Texte, Rectangle, Ellipse.

| Raccourci | Action |
| --- | --- |
| `⌘Z`, `⇧⌘Z` | Annuler, rétablir |
| `⌘A` | Tout sélectionner |
| `⌘]`, `⌘[` | Avancer, reculer d'un rang |
| `⌘0` | Zoom 100 % |
| `⌘1` | Ajuster à la fenêtre |
| Flèches | Déplacer d'un pixel, de dix pixels avec `⇧` |
| `Espace` | Lecture, pause |
| `Retour arrière` | Supprimer la sélection |

Sur Windows, `Ctrl` remplace `⌘`.

Les trois panneaux de l'éditeur se redimensionnent par leur bord et se replient
depuis la barre d'outils.

### Durée

Chaque élément occupe une plage dans la durée de la composition. Raccourcir une
vidéo n'affecte pas le fichier source. La durée maximale d'une composition est
d'une heure.

### Aperçu

**Tube 3D** présente le rendu sur le luminaire. **LED** présente la matrice à
plat, pour vérifier la lisibilité.

### Vidéos à 60 images/s

Une vidéo à 60 images/s reste à 60 images/s pendant la conversion et dans une composition, y compris avec un texte ou une image superposés. La cadence 59,94 est également conservée. Une composition mêlant plusieurs cadences utilise la plus élevée de ses vidéos ; les sources dépassant 60 images/s sont refusées explicitement.

L’aperçu de l’éditeur peut atteindre 60 images/s selon l’écran et les performances de l’ordinateur. Les petites vignettes de navigation peuvent être moins fluides. La cadence du fichier vidéo et le rafraîchissement électrique des LED sont deux mesures différentes ; le rendu sur l’appareil reste à contrôler.

### Versions

**Dupliquer et modifier** conserve la version en cours et ouvre une copie. Les
fichiers ne sont pas dupliqués sur le disque.

---

## Diffuser

Le bouton **Diffuser** est accessible depuis l'Accueil et depuis un contenu.

1. **Appareils.** Un écran éteint mais joignable est rallumé.
   **Synchroniser la lecture** coordonne le démarrage des appareils
   sélectionnés ; une synchronisation visuelle précise dépend aussi du matériel.
2. **Playlist.** Sélectionnez les contenus dans l'ordre voulu. La liste est lue
   en boucle.
3. **Durée.** Sans limite, jusqu'au prochain événement du planning, ou jusqu'à
   la prochaine extinction programmée.

Les vidéos sont converties avant l'envoi au format lisible par l'écran. Cette
opération prend un temps proportionnel à la durée du fichier.

Une diffusion n'est déclarée effectuée qu'après confirmation par l'appareil. En
cas de succès partiel, les appareils concernés sont nommés.

---

## Programmer

Onglet **Planning**, vue hebdomadaire, un ou plusieurs appareils.

Une **programmation** associe une playlist, des jours et une plage horaire, à
l'heure de votre fuseau.

Une **mise en veille** éteint l'écran sur une plage donnée. Les contenus restent
en mémoire dans l'appareil. Une programmation couvrant ces heures est
prioritaire sur la veille.

Les modifications sont enregistrées même lorsqu'un appareil est éteint.
L'Accueil indique le nombre d'appareils à synchroniser, et **Appliquer
maintenant** les met à jour dès qu'ils répondent.

---

## Live

Le Live est disponible **uniquement en mode démonstration** pendant la qualification du pilotage réel. Il permet d’explorer l’organisation de séquences ; il ne commande aucun appareil réel.

---

## Projets et sauvegardes

Un **projet `.lfcproject`** contient une création et ses fichiers. Il ne contient
aucune information sur votre réseau ni sur vos appareils, et peut être transmis
à un tiers.

Une **sauvegarde `.lfcstudio`**, depuis les Réglages, conserve les appareils, les
créations et le planning. Les fichiers médias restent à leur emplacement sur le
disque.

---

## Réglages

Langue française ou anglaise. Thème clair, sombre ou selon le système.

**Découvrir le Studio** relance la visite guidée en démo. Vous retrouvez votre espace réel à sa fermeture.

**Stockage** indique l'espace occupé par les données et les fichiers temporaires,
et permet de supprimer ces derniers.

**Effacer les données locales** supprime les appareils, la bibliothèque et le
planning de cet ordinateur. Les programmes enregistrés dans les appareils ne
sont pas affectés.

---

## Retirer un appareil

Onglet **Appareils**, **Retirer du parc**.

**Retirer de cet ordinateur uniquement.** L'appareil conserve son contenu, son
réseau et son code d'accès. Il continue de diffuser et reste détectable.

**Préparer pour un autre utilisateur.** Le code d'accès et le réseau Wi-Fi
enregistré sont effacés. Le réseau de secours de l'appareil reste actif.

---

## Assistance

[Questions et retours](https://github.com/WITH-BY/lfc-studio-releases/issues).

Indiquez votre système d'exploitation, l'action effectuée et le résultat obtenu.
Le message affiché par le Studio est l'information la plus utile.
