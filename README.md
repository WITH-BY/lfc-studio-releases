# LIGHTFORMCOLOR Studio

Application de bureau **macOS Apple Silicon et Windows x64** pour préparer,
programmer et diffuser des contenus sur les écrans **LFC Tube** de WITH‑BY.

Ce dépôt public ne contient **que les artefacts publiés et le feed historique**.
Le code source privé vit dans `WITH-BY/lfc-studio`.

---

## Installation

La dernière préversion réellement publiée est **`1.0.0-beta.3`**.

1. Ouvrir **[Releases](../../releases)** et choisir `v1.0.0-beta.3`.
2. Vérifier l'artefact avec `SHA256SUMS.txt`.
3. macOS : ouvrir le DMG puis glisser l'application dans **Applications**.
4. Windows : lancer l'installateur `x64-setup.exe` pour l'utilisateur courant.

### ⚠️ Premier lancement

La bêta macOS n'est pas signée **Developer ID** ni notarisée. Gatekeeper peut
donc refuser le premier double-clic (« développeur non identifié »). Le paquet
Windows n'est pas signé Authenticode et peut déclencher SmartScreen.

**Pour l'ouvrir la première fois :**

1. Dans **Applications**, faire un **clic droit** sur l'app → **Ouvrir**.
2. Confirmer **Ouvrir** dans la fenêtre d'avertissement.

Sous Windows : **Informations complémentaires → Exécuter quand même** uniquement
après vérification de l'empreinte publiée.

Si macOS annonce que l'application « est endommagée », ne forcez pas son
ouverture : retéléchargez l'artefact depuis la release exacte, revérifiez son
SHA-256 puis signalez l'écart si le message persiste.

---

## Mises à jour

La mise à jour automatique n'est **pas** le canal courant. `latest.json` reste
un feed historique de `beta.1`; les releases `beta.2` et `beta.3` ne publient
pas l'ensemble cohérent archive updater + signature + feed pour les deux OS.
Installer donc les préversions manuellement depuis leur release exacte.

Une future activation exigera publication atomique de l'archive et de sa
signature, feed publié en dernier, vérification par le client et rollback. Une
présence de `latest.json` seule ne prouve pas un canal actif.

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
