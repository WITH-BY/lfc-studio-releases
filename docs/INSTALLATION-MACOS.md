# Installer LIGHTFORMCOLOR Studio sur Mac

## Choisir le bon téléchargement

Dans **Pomme → À propos de ce Mac**, regardez la ligne **Puce** ou **Processeur**. [Aide Apple](https://support.apple.com/fr-fr/116943).

| Votre Mac | Fichier à choisir |
| --- | --- |
| Puce Apple M1, M2, M3, M4 ou suivante | **Mac-Apple-Silicon.dmg**, ou un nom contenant **aarch64** |
| Processeur Intel | **Mac-Intel.dmg**, ou un nom contenant **x64** et se terminant par **.dmg** |

La candidate beta.13 prévoit les deux paquets séparés. Un paquet Intel n’est disponible qu’après son build sur Mac et son ajout à la page des versions ; les beta.8 à beta.12 n’en proposent pas.

La configuration de l’application demande macOS 11 ou ultérieur. Prévoyez au moins 400 Mo pour l’application, plus de l’espace pour vos vidéos et leurs rendus. La compatibilité du paquet exact est indiquée dans ses notes de version.

## Télécharger sans connaître GitHub

1. Ouvrez la [page de téléchargement](https://github.com/WITH-BY/lfc-studio-releases#telecharger).
2. Choisissez votre type de Mac. Dans la [liste des versions](https://github.com/WITH-BY/lfc-studio-releases/releases), ouvrez une version qui propose votre architecture.
3. Sous **Assets**, cliquez sur le fichier **.dmg** correspondant. Assets signifie simplement « fichiers à télécharger ».
4. Retrouvez-le dans le dossier **Téléchargements** de votre Mac.

Vous n’avez pas besoin d’un compte GitHub pour télécharger les fichiers publics. Les fichiers **Source code**, **.app.tar.gz**, **.sig** et **SHA256SUMS** ne sont pas l’installateur à ouvrir.

## Installer et ouvrir

Double-cliquez sur le **.dmg**. Glissez **LIGHTFORMCOLOR Studio** vers **Applications**. Éjectez ensuite le disque LIGHTFORMCOLOR Studio et ouvrez l’application depuis **Applications**.

Les préversions signées ad hoc peuvent déclencher l’avertissement de macOS sur le développeur. Si vous avez téléchargé le paquet depuis la page WITH-BY ci-dessus :

1. Essayez d’ouvrir l’application une première fois.
2. Ouvrez **Réglages Système → Confidentialité et sécurité**.
3. Repérez LIGHTFORMCOLOR Studio et choisissez **Ouvrir quand même**, puis confirmez.

Les intitulés varient selon macOS. Suivez la [procédure Apple](https://support.apple.com/fr-fr/guide/mac-help/mh40616/mac) si l’option n’apparaît pas. Une alerte indiquant un logiciel malveillant ou un fichier endommagé demande un nouveau téléchargement et un contact avec l’assistance.

## Connecter votre premier appareil

Autorisez l’accès au **réseau local** quand macOS le demande. Sur les versions qui proposent ce réglage, il se retrouve dans **Réglages Système → Confidentialité et sécurité → Réseau local**.

Suivez ensuite **[Votre première utilisation](PREMIERS-PAS.md)** : connexion directe au Tube, nom, nouveau mot de passe de secours, réseau habituel et visite guidée.

## Mettre à jour ou désinstaller

Pour une mise à jour manuelle, quittez le Studio, téléchargez le nouveau DMG de votre architecture et remplacez l’application dans **Applications**. Les données de travail restent sur votre ordinateur. Une mise à jour depuis les Réglages n’est proposée que lorsqu’une version signée est disponible pour votre architecture.

Pour désinstaller, placez l’application dans la corbeille. Vos médias et données ne sont pas supprimés. Les identifiants de secours conservés dans le Trousseau ne sont pas transférés vers un autre Mac.

**Étape suivante : [première connexion et première image](PREMIERS-PAS.md).**
