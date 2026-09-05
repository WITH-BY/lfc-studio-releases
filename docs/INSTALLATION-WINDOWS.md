# Installer LIGHTFORMCOLOR Studio sur Windows

**Préversion `1.0.0-beta.9`.** Cette bêta n'est pas signée Authenticode :
Windows SmartScreen affiche un avertissement au lancement de l'installateur.
Les étapes ci-dessous sont la marche à suivre normale pour une bêta, pas un
contournement de sécurité.

## Ce qu'il vous faut

- **Windows 10 version 1809** ou plus récent, **64 bits** ;
- environ **400 Mo** d'espace disque ;
- le même réseau Wi-Fi ou Ethernet que vos LFC Tube ;
- une connexion Internet au premier lancement de l'installateur, si
  **Microsoft Edge WebView2** n'est pas déjà présent (il l'est sur toute
  installation de Windows 11 et sur la plupart des Windows 10 à jour).

Il n'existe **pas** de paquet Windows ARM64.

Pour vérifier votre PC : **Paramètres** → **Système** → **Informations
système**. « Type du système » doit indiquer *Système d'exploitation 64 bits,
processeur x64*.

## 1. Télécharger

1. Ouvrir la [page des releases](https://github.com/WITH-BY/lfc-studio-releases/releases).
2. Choisir **`v1.0.0-beta.9`**.
3. Télécharger `LIGHTFORMCOLOR-Studio-1.0.0-beta.9-x64-setup.exe`.

Le navigateur peut lui-même signaler un exécutable « rarement téléchargé ».
Choisir **Conserver** pour terminer le téléchargement.

## 2. Vérifier l'empreinte (recommandé)

Le fichier `SHA256SUMS.txt` de la release contient l'empreinte de chaque
artefact. Dans PowerShell :

```powershell
Get-FileHash "$env:USERPROFILE\Downloads\LIGHTFORMCOLOR-Studio-1.0.0-beta.9-x64-setup.exe" -Algorithm SHA256
```

La valeur affichée doit être identique à celle publiée. Si elle diffère,
n'installez pas : retéléchargez, puis signalez l'écart.

## 3. Installer — l'étape qui bloque

1. Double-cliquer l'installateur.
2. SmartScreen affiche **« Windows a protégé votre ordinateur »**.
3. Cliquer **Informations complémentaires**.
4. Vérifier que l'éditeur affiché est bien le fichier attendu, puis cliquer
   **Exécuter quand même**.
5. Choisir la langue de l'installateur (français ou anglais).
6. Suivre l'assistant jusqu'au bout.

L'installation se fait **pour l'utilisateur courant uniquement** : elle ne
demande pas de droits administrateur et n'écrit rien dans `Program Files`.
L'application est installée sous :

```
%LOCALAPPDATA%\LIGHTFORMCOLOR Studio
```

Si WebView2 est absent, l'installateur le télécharge et l'installe
silencieusement. Cette étape demande Internet et peut durer une minute.

## 4. Autoriser le réseau local

Au premier démarrage, Windows affiche l'alerte du pare-feu **« Voulez-vous
autoriser les communications… »**.

**Cochez au moins « Réseaux privés »**, puis **Autoriser l'accès**. Sans cette
autorisation, le Studio ne découvre aucun LFC Tube et la page Appareils reste
vide.

Si vous avez refusé par erreur : **Paramètres** → **Confidentialité et
sécurité** → **Sécurité Windows** → **Pare-feu et protection du réseau** →
**Autoriser une application via le pare-feu**, puis cochez LIGHTFORMCOLOR Studio
en réseau privé et relancez l'application.

## Désinstaller

**Paramètres** → **Applications** → **Applications installées** →
**LIGHTFORMCOLOR Studio** → **Désinstaller**.

Les projets et réglages restent dans ces deux dossiers, à supprimer séparément
si vous voulez repartir de zéro :

```
%APPDATA%\com.withby.lightformcolor.studio
%LOCALAPPDATA%\LIGHTFORMCOLOR Studio\cache
```

Les codes d'accès des appareils sont conservés dans le gestionnaire
d'identifiants Windows, jamais dans ces dossiers ni dans un projet exporté.

## Mise à jour

La mise à jour automatique **n'est pas active** dans cette bêta : aucun canal
signé n'est publié, et l'écran Réglages l'indique explicitement. Pour passer à
une bêta suivante, téléchargez son installateur et relancez-le par-dessus.
Vos contenus, appareils et plannings sont conservés.

## Limites connues de cette bêta

- installateur non signé Authenticode : l'avertissement SmartScreen est attendu
  et se reproduira à chaque nouvelle bêta ;
- x64 uniquement, pas de paquet ARM64 ;
- aucune mise à jour automatique ;
- l'onglet **Live** est une démonstration tant que le firmware n'est pas
  qualifié ;
- l'assistance à distance des Réglages n'est reliée à aucune infrastructure.

## En cas de problème

Ouvrir une [issue](https://github.com/WITH-BY/lfc-studio-releases/issues) en
indiquant la version de Windows, la version du Studio et le message exact
affiché.
