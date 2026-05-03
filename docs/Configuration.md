# Configuration

RelishDeath loads configuration from:
- `plugins/RelishDeath/config.yml`
- `plugins/RelishDeath/lang/en.yml` (or your selected language)

Database (SQLite):
- `plugins/RelishDeath/relishdeath.db`

RelishDeath includes a config updater/validator that restores missing bundled files, merges missing keys, and creates timestamped backups before rewriting.

## Core Setup

```yaml
language: en
license-key: ""
```

## Timers

```yaml
timers:
  groups:
    default: 5
    vip: 30
    premium: 60
    admin: 120
    permanent: -1
  continue-offline: true
```

## Grave Expiration

```yaml
graves:
  # Options: black-market, stash, drop
  on-expire: black-market
```

Notes:
- `stash` and `black-market` require a premium license.

## Particles

```yaml
particles:
  activation-distance: 50.0
  types:
    far: FLAME
    close: SOUL_FIRE_FLAME
    very-close: END_ROD
```

## Teleport

```yaml
teleport:
  # Options: far, close, very-close
  mode: close
```

## Notifications and Reminders

```yaml
notifications:
  periodic-reminders: true
  reminder-intervals: [180, 120, 60]

  reminders:
    display:
      chat: true
      actionbar: false
      title: false
      bossbar: false
    bossbar-seconds: 5
```

## Stash (Premium)

```yaml
stash:
  expiration-hours: 24
```

## Black Market (Premium)

```yaml
economy:
  enabled: true
  marketplace-enabled: true
  black-market:
    enabled: true
    expiration-hours: -1
```

## Language Files

All messages use MiniMessage formatting (`<red>`, `<gold>`, `<bold>`, click actions, hover text, etc.).

