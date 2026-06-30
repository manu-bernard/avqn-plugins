# avqn-plugins

Marketplace des plugins publics **AVQN** pour Claude Code / claude.ai.

## Ajouter la marketplace

```
/plugin marketplace add manu-bernard/avqn-plugins
/plugin install avqn-os@avqn
```

Puis, pour rester à jour automatiquement : `/plugin` → onglet **Marketplaces** →
`avqn` → **Enable auto-update**.

## Plugins

| Plugin | Contenu |
| --- | --- |
| **avqn-os** | Le connecteur MCP `https://os.avqn.ch/mcp` (CRM, temps, agenda, mémoire, carnet, pilotage…) + le skill `grill-me`. |

> Le connecteur MCP exige une authentification (OTP, allowlist) : installer le plugin
> donne les skills et le connecteur, mais l'accès aux données reste gardé côté serveur.
