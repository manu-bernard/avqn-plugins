# avqn-plugins

Marketplace des plugins publics **AVQN** pour Claude Code / claude.ai.

## Ajouter la marketplace

```
/plugin marketplace add manu-bernard/avqn-plugins
/plugin install avqn-os@avqn
/plugin install avqn-infra@avqn
/plugin install avqn-dev@avqn
```

Puis, pour rester à jour automatiquement : `/plugin` → onglet **Marketplaces** →
`avqn` → **Enable auto-update**.

## Plugins

| Plugin | Contenu |
| --- | --- |
| **avqn-os** | Le connecteur MCP `https://os.avqn.ch/mcp` (CRM, temps, agenda, mémoire, carnet, pilotage…) + le skill `grill-me`. |
| **avqn-infra** | Le connecteur MCP `https://infra.avqn.ch/mcp` (Coolify, Hetzner, DNS, R2, SSH, backup, monitoring, release, dépôts). |
| **avqn-dev** | La méthodo de dev continu AVQN (skills `brainstorm-issue` / `dev` / `apercu` + superpowers). Scope user. |

> Le connecteur MCP exige une authentification (OTP, allowlist) : installer le plugin
> donne les skills et le connecteur, mais l'accès aux données reste gardé côté serveur.
