# Installer LIGHTFORMCOLOR Studio sur macOS

**Préversion `1.0.0-beta.8`.** Cette bêta n'est pas signée Developer ID ni
notarisée par Apple : macOS refuse volontairement de l'ouvrir au premier
double-clic. Les étapes ci-dessous sont la marche à suivre normale pour une
bêta, pas un contournement de sécurité.

## Ce qu'il vous faut

- un Mac **Apple Silicon** (puce M1 ou ultérieure) ;
- **macOS 11 Big Sur** ou plus récent ;
- environ **300 Mo** d'espace disque ;
- le même réseau Wi-Fi ou Ethernet que vos LFC Tube.

Il n'existe **pas** de paquet pour Mac Intel. Sur un Mac Intel, l'application ne
s'installe pas : les outils vidéo embarqués sont compilés pour Apple Silicon.

Pour vérifier votre Mac : menu  → **À propos de ce Mac**. La ligne « Puce »
doit indiquer Apple M1, M2, M3, M4 ou ultérieur.

## 1. Télécharger

1. Ouvrir la [page des releases](https://github.com/WITH-BY/lfc-studio-releases/releases).
2. Choisir **`v1.0.0-beta.8`**.
3. Télécharger `LIGHTFORMCOLOR-Studio_1.0.0-beta.8_aarch64.dmg`.

## 2. Vérifier l'empreinte (recommandé)

Le fichier `SHA256SUMS.txt` de la release contient l'empreinte de chaque
artefact. Dans le Terminal :

```bash
shasum -a 256 ~/Downloads/LIGHTFORMCOLOR-Studio_1.0.0-beta.8_aarch64.dmg
```

La valeur affichée doit être identique à celle publiée. Si elle diffère,
n'installez pas : retéléchargez, puis signalez l'écart.

## 3. Installer

1. Double-cliquer le DMG.
2. Glisser **LIGHTFORMCOLOR Studio** sur le raccourci **Applications**.
3. Éjecter le disque monté (clic droit sur son icône → **Éjecter**).

## 4. Premier lancement — l'étape qui bloque

Au premier double-clic, macOS affiche un refus. Le message dépend de la version
du système : « développeur non identifié », « impossible de vérifier
l'absence de logiciel malveillant », ou « l'application est endommagée ».

**Marche à suivre :**

1. Double-cliquer **LIGHTFORMCOLOR Studio** dans **Applications**. Le refus
   s'affiche : cliquer **OK** ou **Terminé**.
2. Ouvrir **Réglages Système** → **Confidentialité et sécurité**.
3. Descendre jusqu'à la section **Sécurité**. Une ligne mentionne
   « LIGHTFORMCOLOR Studio a été bloqué ».
4. Cliquer **Ouvrir quand même**, puis confirmer avec Touch ID ou le mot de
   passe de votre session.
5. L'application s'ouvre. Les lancements suivants sont directs.

Le clic droit → **Ouvrir** fonctionne encore sur les anciennes versions de
macOS ; à partir de macOS 15 Sequoia, il faut passer par Réglages Système.

Si le message persiste après cette manipulation, l'attribut de quarantaine peut
être retiré explicitement :

```bash
xattr -d com.apple.quarantine "/Applications/LIGHTFORMCOLOR Studio.app"
```

Ne lancez cette commande qu'après avoir vérifié l'empreinte SHA-256 de l'étape 2.
Elle désactive un contrôle de sécurité : elle n'a de sens que si vous savez que
le fichier est bien celui publié.

## 5. Autoriser le réseau local

Au premier démarrage, macOS demande l'autorisation d'accéder aux appareils du
réseau local. **Répondez Autoriser** : sans elle, le Studio ne découvre aucun
LFC Tube et la page Appareils reste vide.

Si vous avez refusé par erreur : **Réglages Système** → **Confidentialité et
sécurité** → **Réseau local**, puis activez l'interrupteur en face de
LIGHTFORMCOLOR Studio et relancez l'application.

## Désinstaller

Glisser **LIGHTFORMCOLOR Studio** de **Applications** vers la corbeille.

Les projets et réglages restent dans ces deux dossiers, à supprimer séparément
si vous voulez repartir de zéro :

```
~/Library/Application Support/com.withby.lightformcolor.studio
~/Library/Caches/LIGHTFORMCOLOR Studio
```

Les codes d'accès des appareils sont conservés dans le trousseau macOS, jamais
dans ces dossiers ni dans un projet exporté.

## Mise à jour

La mise à jour automatique **n'est pas active** dans cette bêta : aucun canal
signé n'est publié, et l'écran Réglages l'indique explicitement. Pour passer à
une bêta suivante, téléchargez son DMG et remplacez l'application. Vos contenus,
appareils et plannings sont conservés.

## Limites connues de cette bêta

- signature ad hoc, sans notarisation Apple : le refus au premier lancement est
  attendu et se reproduira à chaque nouvelle bêta ;
- Apple Silicon uniquement ;
- aucune mise à jour automatique ;
- l'onglet **Live** est une démonstration tant que le firmware n'est pas
  qualifié ;
- l'assistance à distance des Réglages n'est reliée à aucune infrastructure.

## En cas de problème

Ouvrir une [issue](https://github.com/WITH-BY/lfc-studio-releases/issues) en
indiquant la version de macOS, le modèle de Mac, la version du Studio et le
message exact affiché.
