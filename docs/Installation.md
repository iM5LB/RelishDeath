# Installation

## Requirements

- Minecraft: 1.21+ (Paper or Paper-based forks)
- Java: 21+
- Dependency: PacketEvents (required)
- Optional: Vault (economy features)

## Install Steps

1. Install PacketEvents (required).
2. Put `RelishDeath-*.jar` in your server `plugins/` folder.
3. Restart the server (recommended) to generate:
   - `plugins/RelishDeath/config.yml`
   - `plugins/RelishDeath/lang/en.yml`
4. (Premium) Set your key in `plugins/RelishDeath/config.yml`:

```yaml
license-key: "YOUR_KEY_HERE"
```

5. Reload with `/rd reload` (requires `relishdeath.admin.reload`) or restart the server.
6. Verify license status (optional): `/rd license`

## Files Created

- Config: `plugins/RelishDeath/config.yml`
- Language: `plugins/RelishDeath/lang/en.yml`
- Database (SQLite): `plugins/RelishDeath/relishdeath.db`

## Troubleshooting

### PacketEvents Not Found

- Make sure PacketEvents is installed and loaded before RelishDeath.

### Wrong Java Version

- Paper 1.21 requires Java 21. If the plugin fails to load, confirm `java -version` is 21+.

### Enable Debug Logs

```yaml
debug:
  enabled: true
```
