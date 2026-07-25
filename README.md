# LIGHTFORMCOLOR Studio

Application de bureau **macOS** pour préparer, programmer et diffuser des
contenus sur les écrans **LFC Tube** de WITH‑BY.

Ce dépôt ne contient **que les binaires publiés**. Le code source n'y est pas.

---

## Installation

1. Télécharger le `.dmg` de la dernière version dans **[Releases](../../releases)**.
2. Ouvrir le DMG et glisser **LIGHTFORMCOLOR Studio** dans **Applications**.

### ⚠️ Premier lancement

Cette bêta n'est pas signée par Apple. macOS refusera donc de l'ouvrir au
premier double‑clic (« développeur non identifié »). C'est le comportement
normal de Gatekeeper pour un logiciel non signé, pas un défaut de l'application.

**Pour l'ouvrir la première fois :**

1. Dans **Applications**, faire un **clic droit** sur l'app → **Ouvrir**.
2. Confirmer **Ouvrir** dans la fenêtre d'avertissement.

Une seule fois : les lancements suivants sont normaux.

Si macOS annonce que l'application « est endommagée », c'est la mise en
quarantaine du téléchargement. Pour la retirer :

```bash
xattr -dr com.apple.quarantine "/Applications/LIGHTFORMCOLOR Studio.app"
```

---

## Mises à jour

Le Studio se met à jour seul : **Réglages → Mise à jour**.

Chaque archive est **signée**, et l'application vérifie cette signature avec une
clé publique compilée dans son binaire **avant** d'installer quoi que ce soit.
Une archive modifiée est refusée, même servie depuis ce dépôt.

---

## Compatibilité

- macOS 11 ou ultérieur
- **Apple Silicon** (`aarch64`) — pas de version Intel ni Windows pour l'instant

---

## Statut

Version **bêta publique**. Les retours sont les bienvenus dans les
[issues](../../issues).

© WITH‑BY
