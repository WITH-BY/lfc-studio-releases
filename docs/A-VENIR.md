# Feuille de route

Ce document décrit ce que nous développons. Il ne décrit pas les fonctions
disponibles aujourd'hui, qui sont couvertes par le
[guide d'utilisation](GUIDE-UTILISATEUR.md).

Les fonctions sont annoncées ici sans date. Nous les publions lorsqu'elles ont
été vérifiées sur le matériel.

---

## Gamme

Le LFC Tube est le premier produit de la gamme. Un écran plat et un boîtier
HDMI sont en développement.

Tous se pilotent depuis les mêmes outils. Ajouter un produit conserve vos noms,
vos droits d'accès et votre bibliothèque de contenus.

## Mise en service

Trois méthodes, selon l'équipement disponible.

| Méthode | Usage |
| --- | --- |
| Téléphone | Scanner le code affiché par l'appareil |
| Ordinateur | Rejoindre le réseau temporaire de l'appareil, puis ouvrir le Studio |
| Code d'association | Saisir dans le Studio le code affiché par un appareil déjà connecté à Internet |

L'interface distingue trois états : réseau rejoint, Internet disponible,
appareil associé. Aucune opération n'est proposée avant que ses conditions
soient réunies.

## Gestion d'un parc

Nommer les emplacements. Constituer des groupes d'appareils. Enregistrer une
configuration d'affichage et la rappeler depuis n'importe quel poste.

Un appareil hors ligne est signalé comme tel sans bloquer les autres. Le
remplacement d'une unité restaure ses réglages.

## Catalogue d'applications

Installation d'applications sur un appareil : horloge, galerie, tableau
d'informations, affichage de données.

Chaque application indique les données et les connexions qu'elle utilise. Un
aperçu au format de votre écran est disponible avant installation. La
désinstallation est sans effet sur le reste de la configuration. Une
application défaillante laisse place au dernier affichage valide.

Le catalogue ne propose que les applications compatibles avec le modèle et la
version de l'appareil.

Sont également prévus un kit de développement et la possibilité, pour une
organisation, de publier un catalogue interne.

## Gestion des contenus

**Fonctionnement autonome.** L'appareil poursuit son dernier programme valide
en l'absence de connexion. Une donnée périmée est signalée plutôt qu'affichée.

**Publication programmée**, avec retour à la version précédente.

**Bibliothèque partagée** entre utilisateurs autorisés, avec validation avant
diffusion lorsque l'organisation le requiert.

**Rapport de diffusion** indiquant les contenus effectivement affichés et leurs
horaires.

## Intégrations

**Entrée HDMI** au format exact de l'écran, avec comportement défini en cas de
perte puis de retour du signal.

**Protocoles professionnels :** NDI, Art-Net, sACN, OSC, MIDI, et affichage
d'une page web. Chaque intégration est publiée avec ses prérequis, ses limites
et son comportement en cas de perte de source. Certaines s'exécutent sur
l'appareil, d'autres nécessitent le Studio.

## Exploitation multi-sites

Vue d'ensemble du parc limitée aux éléments demandant une action.

Déploiement des mises à jour par lots, sur des plages de maintenance définies
par l'exploitant.

Session d'assistance ouverte et révocable par le propriétaire.

## Maîtrise du matériel

L'identité de l'appareil reste sur l'appareil. La réinitialisation complète, la
préparation à la revente et la location temporaire sont prises en charge, avec
suppression vérifiée des données de la session précédente.

Une mise à jour interrompue reprend. Un appareil qui ne démarre plus est
récupérable.

---

## État d'avancement

Le LFC Tube est fonctionnel et pilotable depuis le Studio. La qualification
matérielle est en cours : rendu sur les dalles, mise en service, reprise après
coupure, mise à jour.

Suivent la production des premières unités, puis les groupes et configurations
d'affichage de gamme, puis les premières applications.

## Nous transmettre une demande

Les priorités de développement tiennent compte des retours reçus. Écrivez-nous
depuis les
[questions et retours](https://github.com/WITH-BY/lfc-studio-releases/issues).
