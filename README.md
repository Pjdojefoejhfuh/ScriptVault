# ScriptVault Roblox

Dashboard noir/violet pour comptes, hébergement de scripts Lua et génération de loaders.

## Lancer localement

Node.js 18+ recommandé.

```bash
npm install
npm start
```

Puis ouvre http://localhost:3000

## Loader

Chaque script actif possède un endpoint raw : `/raw/ID` et un loader de la forme :

```lua
loadstring(game:HttpGet("https://TON-DOMAINE/raw/ID"))()
```

`localhost` n'est pas accessible depuis Roblox. Pour un usage distant, déploie le projet sur un hébergeur Node.js avec HTTPS et un stockage persistant pour `scriptvault.db`.

Définis `JWT_SECRET` en production.
