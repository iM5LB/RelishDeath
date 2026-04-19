# Commands

Main command: `/relishdeath`

Aliases: `/rd`, `/rdeath`, `/rl`

Notes:
- Most commands accept an optional grave number `[#]`.
- If you omit `[#]`, RelishDeath targets your newest grave.

## Player Commands

| Command | Description |
|---|---|
| `/rd help` | Show help |
| `/rd list` | List your active graves |
| `/rd locate [#]` | Show graves and start guidance to the selected grave |
| `/rd unlock [#]` | Make your grave public (anyone can claim it) |
| `/rd restore [#]` | Restore items from a grave remotely (permission-based) |
| `/rd info` | Plugin info and status |

## Premium Commands

| Command | Description |
|---|---|
| `/rd stash` | Open your stash packages |
| `/rd blackmarket` | Open black market |
| `/rd trust <player>` | Add a trusted player |
| `/rd untrust <player>` | Remove a trusted player |

## Admin Commands

| Command | Description |
|---|---|
| `/rd reload` | Reload config/lang and refresh visuals |
| `/rd saves` | Open admin death backups GUI |
| `/rd license` | View license status and premium feature availability |

## Permission Nodes (plugin.yml)

| Permission | Description | Default |
|-----------|-------------|---------|
| `relishdeath.use` | Basic plugin usage (graves on death) | `true` |
| `relishdeath.restore` | Remote item restoration | `false` |
| `relishdeath.teleport` | Teleport to your grave | `false` |
| `relishdeath.trust` | Trust system commands | `true` |
| `relishdeath.marketplace.buy` | Use black market | `true` |
| `relishdeath.admin.reload` | Reload command | `op` |
| `relishdeath.admin.backups` | Admin backups GUI | `op` |
| `relishdeath.admin.license` | License status command | `op` |
| `relishdeath.timer.vip` | Timer group `vip` | `false` |
| `relishdeath.timer.premium` | Timer group `premium` | `false` |
| `relishdeath.timer.admin` | Timer group `admin` | `op` |
| `relishdeath.timer.permanent` | Timer group `permanent` | `false` |
