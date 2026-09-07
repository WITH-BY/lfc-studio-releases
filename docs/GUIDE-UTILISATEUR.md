# Guide d'utilisation

LIGHTFORMCOLOR Studio prépare vos images et vos vidéos, les met au format exact
de vos écrans LFC, puis les envoie et les programme.

Pour installer le logiciel : [macOS](INSTALLATION-MACOS.md) ou
[Windows](INSTALLATION-WINDOWS.md).

---

## Le principe

Vous composez une fois dans le Studio. Vous indiquez quel écran reçoit quoi. Le
Studio se charge du reste : redimensionnement, conversion vidéo, envoi, lecture.

Six onglets, dans la colonne de gauche.

| Onglet | À quoi il sert |
| --- | --- |
| **Accueil** | l'état de vos appareils, allumer et éteindre, appliquer les changements en attente |
| **Contenus** | importer vos images et vidéos, créer des compositions, les ranger |
| **Planning** | ce qui passe, quel jour, à quelle heure, et les plages où l'écran s'éteint |
| **Live** | déclencher des séquences préparées, pour un événement |
| **Appareils** | ajouter, nommer, regrouper vos écrans |
| **Réglages** | langue, thème, sauvegarde |

Le raccourci `⌘K` sur Mac, `Ctrl+K` sur Windows, ouvre une barre de recherche :
tapez le nom d'un écran ou d'une action pour y aller directement.

---

## Ajouter votre premier appareil

Branchez le LFC Tube sur le même réseau que votre ordinateur, puis :

1. Onglet **Appareils**, bouton **Ajouter un appareil**, choisissez **LFC Tube**.
2. Le Studio cherche seul sur le réseau. Vous n'avez aucune adresse à saisir.
3. Choisissez l'appareil trouvé. Sa taille, sa résolution et son numéro de série
   sont lus directement sur le matériel.
4. Donnez-lui un nom que vous reconnaîtrez dans le planning : « Vitrine »,
   « Entrée », « Scène jardin ».

### Si l'appareil n'apparaît pas

Vérifiez d'abord que l'ordinateur et l'appareil sont sur **le même réseau**. Un
réseau invité, ou un Wi-Fi qui isole ses appareils entre eux, les sépare.

Vérifiez ensuite que vous avez bien autorisé l'accès au réseau local (macOS) ou
au pare-feu en réseau privé (Windows). Les guides d'installation détaillent où
le faire.

S'il s'agit d'un premier branchement, l'appareil n'est encore relié à aucun
réseau : il diffuse le sien. Son nom et son mot de passe sont écrits sur
l'appareil, à côté l'un de l'autre. Rejoignez ce réseau depuis les réglages
Wi-Fi de votre ordinateur, puis revenez dans le Studio. L'absence d'Internet
sur ce réseau est normale.

### Protéger un appareil

Le Studio vous propose un code de 4 à 8 chiffres. Il ne sera demandé que pour
ajouter ce même appareil à un **autre** ordinateur. Il est conservé dans le
trousseau de votre système, jamais dans un projet que vous envoyez à quelqu'un.

### Garder la main sur un appareil

Chaque appareil diffuse son propre réseau de secours, en permanence, même une
fois connecté au vôtre. C'est par lui que vous le retrouvez si votre box change
ou si son mot de passe Wi-Fi est modifié.

Dans **Appareils**, la section **Accès de secours** vous permet de renommer ce
réseau et de changer son mot de passe. Faites-le : celui d'usine est écrit sur
le boîtier et il est le même sur tous les appareils. Notez le nouveau, il n'est
pas relisible ensuite.

Si votre appareil change d'adresse sur le réseau, par exemple après un
redémarrage de votre box, le Studio le retrouve tout seul. Vous n'avez rien à
refaire.

### Ranger vos appareils

Les **groupes** rassemblent vos écrans par lieu ou par installation : « Vitrine »,
« Étage 1 », « Client Dupont ». Vous les retrouvez et vous les pilotez ensemble.

**Allumer en bleu** fait clignoter un appareil en bleu. Pratique pour savoir
lequel est lequel quand plusieurs se ressemblent.

---

## Importer vos contenus

Onglet **Contenus**, bouton **Importer**. Vous pouvez aussi glisser vos fichiers
directement dans la fenêtre.

**Images** : png, jpg, webp, gif, bmp, tiff, heic.
**Vidéos** : mp4, mov, m4v, webm, avi, mkv.

### Dossiers suivis

**Ajouter un dossier** déclare un dossier de votre disque comme source. Le Studio
le relit à chaque ouverture des Contenus et vous propose les nouveaux fichiers.
Pratique quand un graphiste dépose ses visuels dans un dossier partagé.

Cesser de suivre un dossier ne supprime rien : ce qui a déjà été importé reste
dans votre bibliothèque.

### Retrouver un contenu

Classez vos contenus dans des **dossiers**, puis filtrez la galerie. Vous pouvez
aussi filtrer par appareil, pour ne voir que ce qui est au bon format.

Un contenu peut porter la mention « format sans appareil compatible » : aucun de
vos écrans ne correspond exactement à ses dimensions.

---

## Composer

Une **composition** assemble des images, des vidéos, du texte et des formes, puis
les répartit sur un ou plusieurs écrans.

Depuis **Contenus**, cliquez **Nouvelle composition**. Le Studio vous demande
pour quel appareil : la composition démarre alors au bon format et à la bonne
orientation. Vous pouvez aussi partir d'une image ou d'une vidéo existante : le
fichier d'origine reste dans votre galerie, seule la composition est modifiée.

### Les écrans de sortie

C'est la notion centrale. Un écran de sortie représente un écran physique.

Dans le panneau **Écrans de sortie**, ajoutez-en un par appareil. Le Studio
reprend automatiquement sa résolution et son orientation. Placez ensuite vos
éléments sur le plan de travail : chacun n'est affiché que sur les écrans que
vous cochez.

C'est ce qui permet une image continue répartie sur plusieurs tubes. Vous
composez une seule fois, chaque appareil reçoit sa part.

Un écran de sortie peut être posé n'importe où sur le plan de travail, et
orienté comme vous le souhaitez.

### Outils et raccourcis

La barre du haut propose **Image**, **Vidéo**, **Texte**, **Rectangle** et
**Ellipse**.

| Raccourci | Effet |
| --- | --- |
| `⌘Z` et `⇧⌘Z` | annuler et rétablir |
| `⌘A` | tout sélectionner |
| `⌘]` et `⌘[` | avancer et reculer d'un rang |
| `⌘0` | zoom 100 % |
| `⌘1` | ajuster à la fenêtre |
| Flèches | déplacer d'un pixel, avec `⇧` de dix pixels |
| `Espace` | lecture et pause |
| `Retour arrière` | supprimer la sélection |

Sur Windows, remplacez `⌘` par `Ctrl`.

Les trois panneaux de l'éditeur se redimensionnent en tirant leur bord. Vous
pouvez aussi les refermer depuis la barre d'outils pour laisser toute la place
au plan de travail.

### Le temps

Chaque élément a sa place dans la durée de la composition. Raccourcir une vidéo
ne touche pas au fichier d'origine.

Une composition ne peut pas dépasser une heure.

### Voir le résultat

Deux aperçus. **Tube 3D** montre le rendu sur le luminaire. **LED** montre la
matrice à plat, pour vérifier la lisibilité de près.

### Travailler sans perdre une version

**Dupliquer et modifier** conserve la version actuelle et ouvre une copie. Vos
fichiers ne sont pas recopiés, cela ne prend pas de place sur le disque.

---

## Diffuser tout de suite

Le bouton **Diffuser** est disponible depuis l'Accueil et depuis un contenu.
Trois étapes.

**Les appareils.** Un ou plusieurs. Un écran éteint mais joignable sera rallumé.
Cochez **Synchroniser la lecture** pour que tout démarre en même temps.

**La playlist.** Cliquez les contenus dans l'ordre voulu. La liste tourne en
boucle.

**La durée.** Sans limite, jusqu'au prochain événement du planning, ou jusqu'à
la prochaine extinction programmée.

Puis **Diffuser maintenant**.

Vos vidéos sont converties avant l'envoi, au format que l'écran sait lire. Sur
un fichier long, comptez un moment.

Le Studio n'annonce jamais une diffusion réussie sans que l'appareil l'ait
confirmée. Si un écran sur trois n'a pas répondu, il vous le dit et vous nomme
lequel.

---

## Programmer

Onglet **Planning** : une semaine, un ou plusieurs appareils.

Une **programmation** associe une playlist, des jours et une plage horaire. Les
heures sont celles de votre fuseau.

Une **mise en veille** éteint l'écran sur une plage donnée. Vos contenus restent
en mémoire dans l'appareil. Une programmation posée sur ces heures passe devant
la veille.

Vos modifications sont enregistrées même si un appareil est éteint. L'Accueil
affiche alors le nombre d'appareils à synchroniser, et **Appliquer maintenant**
les met à jour dès qu'ils répondent.

---

## Live

L'onglet **Live** prépare des séquences pour un événement : des scènes chargées
à l'avance sur plusieurs appareils, déclenchées le jour venu.

Cette fonction est en cours de mise au point. Le déclenchement est coordonné au
mieux par le réseau, sans garantie de simultanéité au centième de seconde. Ne
l'utilisez pas encore comme régie d'un événement où cela compte.

Un appareil réservé au Live refuse les diffusions manuelles tant que vous
n'avez pas restauré son planning depuis cet onglet. C'est volontaire : cela
évite d'écraser une scène préparée.

---

## Partager et sauvegarder

**Un projet `.lfcproject`** contient votre création et ses fichiers. Vous pouvez
l'envoyer à quelqu'un : il ne contient aucune information sur votre réseau ni
sur vos appareils.

**Une sauvegarde `.lfcstudio`**, depuis les Réglages, conserve vos appareils, vos
créations et votre planning. Vos fichiers médias restent où ils sont sur votre
disque.

---

## Réglages

Vous y choisissez la **langue**, français ou anglais, et le **thème**, clair,
sombre ou selon votre système.

**Stockage** indique ce que prennent vos données et les fichiers temporaires, et
permet de vider ces derniers.

**Effacer les données locales** supprime vos appareils, votre bibliothèque et
votre planning de cet ordinateur. Ce qui est déjà enregistré dans les appareils
n'est pas touché.

---

## Retirer un appareil

Onglet **Appareils**, bouton **Retirer du parc**. Deux choix.

**Retirer seulement de cet ordinateur.** L'appareil garde son contenu, son Wi-Fi
et son code. Il continue de diffuser et reste détectable.

**Préparer pour une autre personne.** Le code d'accès et le réseau Wi-Fi
enregistré sont effacés. Le réseau de secours de l'appareil reste actif pour son
prochain propriétaire.

---

## Une question, un problème

Écrivez-nous depuis les
[questions et retours](https://github.com/WITH-BY/lfc-studio-releases/issues).

Indiquez votre système, ce que vous attendiez et ce qui s'est passé. Le message
exact affiché par le Studio est l'information la plus utile.
