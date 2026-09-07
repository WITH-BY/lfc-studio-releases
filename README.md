# LIGHTFORMCOLOR Studio

Application de bureau **macOS Apple Silicon et Windows x64** pour préparer,
programmer et diffuser des contenus sur les écrans **LFC Tube** de WITH‑BY.

Ce dépôt public ne contient **que les artefacts publiés et le feed historique**.
Le code source privé vit dans `WITH-BY/lfc-studio`.

---

## Documentation

Ces trois guides sont joints à chaque release, et lisibles directement ici :

- **[Guide d'utilisation](docs/GUIDE-UTILISATEUR.md)** — ajouter un appareil,
  importer, composer sur plusieurs écrans de sortie, diffuser, programmer,
  sauvegarder.
- **[Installer sur macOS](docs/INSTALLATION-MACOS.md)** — Apple Silicon,
  macOS 11 ou ultérieur.
- **[Installer sur Windows](docs/INSTALLATION-WINDOWS.md)** — x64,
  Windows 10 1809 ou ultérieur.

---

## Installation

La dernière préversion publiée est **`1.0.0-beta.10`**. Elle empêche de perdre
la main sur un appareil : adresse réseau suivie automatiquement, point d'accès
de secours qui ne s'éteint jamais, et sa clé d'usine enfin changeable.

1. Ouvrir **[Releases](../../releases)** et choisir la plus récente.
2. Vérifier l'artefact téléchargé avec `SHA256SUMS.txt`.
3. macOS : ouvrir `…-aarch64.dmg`, glisser l'application dans **Applications**.
4. Windows : la `beta.9` ne fournit qu'un **zip portable**, compilé en croisé et
   jamais exécuté sur Windows — décompresser le dossier entier et garder
   `media-tools/` à côté de l'exécutable. Pour un véritable installateur, rester
   sur l'`…-x64-setup.exe` de la [`beta.8`](../../releases/tag/v1.0.0-beta.8) :
   le défaut corrigé ici ne touchait pas Windows.

### ⚠️ Premier lancement

Cette bêta n'est signée **ni Developer ID Apple, ni Authenticode**. Les deux
systèmes affichent donc un refus au premier lancement. C'est attendu, et la
marche à suivre diffère selon le système :

- **macOS** — Réglages Système → Confidentialité et sécurité → **Ouvrir quand
  même**. Le clic droit → Ouvrir ne suffit plus depuis macOS 15.
  Détail : [Installer sur macOS](docs/INSTALLATION-MACOS.md).
- **Windows** — SmartScreen → Informations complémentaires → **Exécuter quand
  même**, après vérification de l'empreinte publiée.
  Détail : [Installer sur Windows](docs/INSTALLATION-WINDOWS.md).

Les deux systèmes demandent aussi l'autorisation du **réseau local** au premier
démarrage : sans elle, aucun LFC Tube n'est découvert.

Si macOS annonce que l'application « est endommagée », ne forcez pas son
ouverture : retéléchargez l'artefact depuis la release exacte, revérifiez son
SHA-256 puis signalez l'écart si le message persiste.

---

## Mises à jour

**Le canal est actif depuis `beta.10`, sur macOS Apple Silicon seulement.**
`latest.json` porte l'archive signée de cette version et pointe sur le tag
exact. Les installations `beta.10` et suivantes se verront proposer les mises à
jour macOS ; une installation antérieure, elle, ne connaît pas ce canal et doit
être remplacée à la main une dernière fois.

Windows n'a pas de canal : la `beta.10` ne fournit aucun paquet Windows, et
`latest.json` ne déclare donc aucune plateforme Windows plutôt que d'annoncer
une mise à jour qui n'existe pas.

---

## Compatibilité

- macOS 11 ou ultérieur, **Apple Silicon** (`aarch64`)
- Windows 10 1809 ou ultérieur, x64
- pas de paquet macOS Intel ni Windows ARM64 publié

---

## Statut

Version **bêta publique manuelle**, sans garantie de production ni exploitation
sans surveillance. Les tests de code, une compilation, un installateur et une
recette avec un appareil sont des preuves différentes. Les retours sont les
bienvenus dans les [issues](../../issues).

© WITH‑BY
