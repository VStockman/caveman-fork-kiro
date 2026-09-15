# Caveman — fork Kiro Power

Ce dépôt est un **fork de [caveman](https://github.com/JuliusBrussee/caveman)** de Julius Brussee.

Caveman met les agents de code en mode « caveman » : prose ultra-compressée, mais code, commandes et messages d'erreur restent intacts. L'agent écrit moins, donc coûte moins de tokens.

**Ce que ce fork ajoute :** un `plugin.json` à la racine du dépôt pour le rendre installable comme **Power dans l'IDE Kiro**. Tout le reste (skills, engine, hooks, proxy) vient de l'amont — voir le [README d'origine](https://github.com/JuliusBrussee/caveman#readme) pour les détails, les chiffres et les autres agents.

---

## 🪨 Ajouter ce dépôt comme Power Kiro

Kiro lit ce dépôt comme un Power. Le `plugin.json` à la racine rend le dépôt reconnaissable, et chaque `skills/*/SKILL.md` est embarqué automatiquement. Pas de config en plus.

### Depuis l'IDE

1. Ouvre Kiro. Panneau latéral → onglet **Powers**.
2. Clique sur **Add Custom Power**.
3. Choisis la source :
   - **Import from GitHub** — colle l'URL du dépôt : `https://github.com/VStockman/caveman-fork-kiro`
   - **Import power from a folder** — pointe un clone local de ce dépôt (le dossier qui contient `plugin.json`).
4. Installe. Kiro trouve le `plugin.json` à la racine et charge les skills du dossier `skills/` (`caveman`, `caveman-commit`, `caveman-review`, `cavecrew`, et les skills de discipline de tokens).

### Utilisation

Les skills s'activent par mot-clé. Dis `/caveman`, « talk like caveman » ou « be brief ». Dis `stop caveman` pour revenir en prose normale.

### Dépannage

Si l'import affiche :

```
Unable to install power: Nothing to install from the repository root:
expected plugin.json, POWER.md, mcp.json or a steering directory
```

C'est que Kiro a été pointé vers un dossier sans `plugin.json`. Pointe la **racine du dépôt** (le dossier qui contient `plugin.json`), pas un sous-dossier.

---

## Licence

Fork sous les mêmes licences que l'amont : MIT pour les skills, BSL-1.1 pour le runtime engine. Voir [LICENSE](./LICENSE), [LICENSE.BSL](./LICENSE.BSL) et [LICENSING.md](./LICENSING.md).
