# Installation sur Windows

## Configuration requise

Windows 10 version 1809 ou ultérieure, 64 bits. 400 Mo d'espace disque.

Pour vérifier : **Paramètres**, **Système**, **Informations système**. La ligne
« Type du système » doit indiquer un système 64 bits avec processeur x64.

## Téléchargement

Ouvrez la [page des versions](https://github.com/WITH-BY/lfc-studio-releases/releases)
et sélectionnez la version la plus récente proposant un fichier Windows.

Le navigateur peut signaler un fichier rarement téléchargé. Choisissez
**Conserver**.

## Installation

Ouvrez le fichier téléchargé.

Windows affiche **« Windows a protégé votre ordinateur »**, l'application n'étant
pas encore enregistrée auprès de Microsoft. Cliquez **Informations
complémentaires**, puis **Exécuter quand même**.

Sélectionnez la langue d'installation et suivez l'assistant. L'installation
s'effectue pour votre compte utilisateur et ne requiert pas de droits
administrateur.

Si Microsoft Edge WebView2 est absent, l'installateur le télécharge. Cette étape
nécessite une connexion Internet.

## Autorisation réseau

Au premier démarrage, le pare-feu Windows demande une autorisation. Cochez au
moins **Réseaux privés**, puis **Autoriser l'accès**. Cette autorisation est
nécessaire : sans elle, le Studio ne détecte aucun écran.

Pour la rétablir : **Paramètres**, **Confidentialité et sécurité**, **Sécurité
Windows**, **Pare-feu et protection du réseau**, **Autoriser une application via
le pare-feu**. Activez LIGHTFORMCOLOR Studio en réseau privé et relancez
l'application.

## Mises à jour

Téléchargez la nouvelle version et exécutez l'installateur. Les contenus,
appareils et plannings sont conservés.

La mise à jour automatique est disponible sur macOS. Elle est en cours de
développement pour Windows.

## Désinstallation

**Paramètres**, **Applications**, **Applications installées**,
**LIGHTFORMCOLOR Studio**, **Désinstaller**.

Les projets et réglages ne sont pas supprimés. Pour les effacer, utilisez
**Effacer les données locales** dans les Réglages du Studio avant
désinstallation.

## Assistance

[Questions et retours](https://github.com/WITH-BY/lfc-studio-releases/issues).
Indiquez votre version de Windows et le message affiché.
