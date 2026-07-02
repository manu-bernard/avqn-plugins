# avqn-plugins (dépôt archivé)

> **Déprécié.** Ce contenu est remplacé par la marketplace `manu-bernard/avqn-dev`
> (`/plugin marketplace add manu-bernard/avqn-dev`) ; les connecteurs MCP (`os.avqn.ch/mcp`,
> `infra.avqn.ch/mcp`) s'ajoutent désormais par URL directe, sans plugin.

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
