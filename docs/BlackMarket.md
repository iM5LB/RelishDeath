# Black Market (Premium)

When a grave expires, it can be listed on the black market for other players to purchase.

## Configuration

```yaml
graves:
  on-expire: black-market

economy:
  enabled: true
  marketplace-enabled: true
  black-market:
    enabled: true
    # Use -1 to keep listings until purchased
    expiration-hours: -1
```

## Buying

- Buyers receive the full contents of the grave.
- If the buyer’s inventory is full, overflow items are sent to stash (premium recovery system).

