# Installer LIGHTFORMCOLOR Studio sur Windows

## Vérifier votre ordinateur

La version Windows vise un **processeur x64** et Windows 10 version 1809 ou ultérieure, dont Windows 11. Dans **Paramètres → Système → Informations système**, vérifiez le **Type du système**. Aucun paquet Windows ARM64 natif n’est fourni.

Prévoyez au moins **400 Mo** pour l’application, plus de l’espace pour vos médias et leurs rendus. Une connexion Internet peut être nécessaire pendant l’installation de Microsoft Edge WebView2.

## Télécharger sans connaître GitHub

1. Ouvrez la [page de téléchargement](https://github.com/WITH-BY/lfc-studio-releases#telecharger).
2. Cliquez sur le téléchargement **Windows x64**.
3. Retrouvez dans **Téléchargements** un fichier ressemblant à **LIGHTFORMCOLOR-Studio-1.0.0-beta.14-x64-setup.exe**. Le numéro peut différer selon la version publiée.

Vous n’avez pas besoin d’un compte GitHub pour télécharger les fichiers publics. Si vous parcourez la [liste des versions](https://github.com/WITH-BY/lfc-studio-releases/releases), choisissez la plus récente qui propose un installateur Windows, puis ouvrez **Assets** pour afficher les fichiers. Certaines versions ne proposent qu’un paquet Mac.

Choisissez **x64-setup.exe**. Les fichiers **Source code**, **.zip**, **.sig** et **SHA256SUMS** ne sont pas l’installateur à ouvrir.

## Installer

Double-cliquez sur **x64-setup.exe**. Choisissez la langue et suivez l’assistant. L’application s’installe pour votre compte utilisateur.

Les préversions sans certificat Authenticode peuvent être signalées comme peu connues. Si vous avez téléchargé le fichier depuis la page WITH-BY ci-dessus, le navigateur peut demander **Conserver**. Dans l’écran **Windows a protégé votre ordinateur**, l’option **Informations complémentaires → Exécuter quand même** permet de poursuivre. Un poste géré par votre organisation peut demander l’intervention de son administrateur.

Si **Microsoft Edge WebView2** manque, l’installateur le télécharge : gardez l’accès à Internet pendant cette étape. Ouvrez ensuite **LIGHTFORMCOLOR Studio** depuis le menu Démarrer.

## Connecter votre premier appareil

Si le pare-feu le demande, autorisez LIGHTFORMCOLOR Studio sur votre **réseau privé de confiance**. Le Studio doit pouvoir communiquer avec les appareils du même réseau.

Suivez ensuite **[Votre première utilisation](PREMIERS-PAS.md)**. La connexion directe au Tube peut afficher **« Pas d’Internet »** : c’est normal après l’installation.

Si le Tube n’est pas trouvé, vérifiez le réseau sélectionné et les autorisations dans **Sécurité Windows → Pare-feu et protection du réseau → Autoriser une application via le pare-feu**.

## Mettre à jour ou désinstaller

Pour une mise à jour manuelle, quittez le Studio et exécutez le nouvel installateur. Les appareils, créations et plannings restent sur cet ordinateur. Les Réglages proposent une mise à jour intégrée uniquement lorsqu’un paquet signé correspondant est disponible.

Pour désinstaller : **Paramètres → Applications → Applications installées → LIGHTFORMCOLOR Studio → Désinstaller**. Vos médias et données de travail sont conservés. Les identifiants de secours du Gestionnaire d’identification ne sont pas transférés vers un autre ordinateur.

**Étape suivante : [première connexion et première image](PREMIERS-PAS.md).**
