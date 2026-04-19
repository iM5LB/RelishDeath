# Stash (Premium)

RelishDeath stashes overflow items when a player claims a grave but their inventory is full.

## How It Works

- Items are never overwritten in your inventory.
- Overflow items are stored as **packages** tied to the source grave.
- Players claim items by clicking them in the stash GUI (`/rd stash`).

## Expiration

Stash packages expire after a configured time:

```yaml
stash:
  expiration-hours: 24
```

