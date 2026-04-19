<div align="center">

## ⚰️ Advanced Death Inventory Protection • Graves • Holograms • Particle Trails

![RelishDeath-Logo](https://github.com/iM5LB/RelishDeath/blob/master/docs/assets/RelishDeathBanner.png?raw=true)[![M5LBStoreBanner](https://github.com/iM5LB/RelishDeath/blob/master/docs/assets/M5LBStore.png?raw=true)](https://m5lb.run.place/)
[![Discord](https://img.shields.io/badge/Discord-Support-7289da?style=for-the-badge&logo=discord)](https://discord.gg/hjKcHavRjT)
[![Documentation](https://img.shields.io/badge/Docs-Read-blue?style=for-the-badge&logo=gitbook)](https://im5lb.github.io/relishdeath)
[![Issues](https://img.shields.io/badge/🐛%20Issues-Report-orange?style=for-the-badge)](https://github.com/iM5LB/relishdeath/issues)
[![Store](https://img.shields.io/badge/Store-License%20Keys-gold?style=for-the-badge)](https://m5lb.run.place/)
[![Donate](https://img.shields.io/badge/💖%20Donate-Love-ff69b4?style=for-the-badge)](https://creators.sa/m5lb)

</div>

---

## 🌟 **Why Choose RelishDeath?**

RelishDeath provides the most advanced death inventory protection system with real server-side entities, particle guidance, and comprehensive backup systems. Built for modern Minecraft servers with performance and reliability in mind.

### ✨ **Key Highlights**

⚰️ **Real Server-Side Entities** - Uses ItemDisplay, TextDisplay, and Interaction entities (Geyser compatible)  
🎯 **Particle Path Guidance** - Visual trails leading players to their graves  
📦 **Perfect Item Serialization** - NBT-API ensures 100% accurate item restoration  
🔄 **Async Operations** - Non-blocking database operations for optimal performance  
🌍 **Multi-World Support** - Works across all dimensions and custom worlds  

---

## 📋 **Requirements**

| Component | Requirement |
|-----------|-------------|
| **Minecraft** | 1.21+ |
| **Server** | Paper, Purpur, or Paper-based forks |
| **Java** | 21+ |
| **Dependencies** | PacketEvents (required) |
| **Soft Dependencies** | Vault (recommended), SellGUI (optional), RelishCurrencies (optional) |

---

## 🚀 **Features Overview**

### 🆓 **Free Version**
- ✅ **Basic grave system** with real server-side entities and holograms
- ✅ **Advanced holograms** - Enhanced hologram features and customization
- ✅ **Particle navigation** - Dynamic particle trails that guide players to graves
- ✅ **Remote restoration** - Restore items from graves without visiting them (permission-based)
- ✅ **Void death protection** with smart safe location placement
- ✅ **Keep inventory integration** - respects vanilla and plugin keep settings
- ✅ **XP protection** with configurable keep percentages
- ✅ **Multi-grave support** - players can have multiple active graves
- ✅ **Auto-respawn** with configurable delay
- ✅ **Safe teleportation** - prevents teleporting into walls or lava
- ✅ **Basic commands** - list, locate, teleport to graves
- ✅ **Multi-world support** - works across all dimensions and custom worlds
- ✅ **Performance optimized** - spatial partitioning for 500+ players

### ⭐ **Premium Version**
- ⭐ **Admin Recovery System** - Death backup system with SQLite-backed backups and admin GUI
- ⭐ **Stash** - Overflow storage when inventory is full (per-grave packages)
- ⭐ **Black Market** - Expired graves become purchasable with economy integration
- ⭐ **Trust System** - Share grave access with friends
- ⭐ **Economy Integration** - Vault support for grave costs and marketplace

---

## 📦 **Installation**

1. **Download** the plugin JAR file
2. **Place** it in your server's `plugins` folder
3. **Start/Restart** your server
4. **(Optional)** For premium features, buy a license key from [M5LB Store](https://m5lb.run.place/)
5. **Place license key** in `config.yml`
6. **Reload** the plugin

```bash
# Quick setup commands
/rd help          # View all commands
/rd info          # Check plugin status
/rd reload        # Reload configuration
```

---

## 🎮 **Commands & Usage**

### 👤 **Player Commands**

| Command | Description | Example |
|---------|-------------|---------|
| `/rd list` | Show your active graves | `/rd list` |
| `/rd locate [#]` | Track route to grave with particles | `/rd locate 1` |
| `/rd restore [#]` | Restore items from grave remotely | `/rd restore 2` |
| `/rd stash` ⭐ | Open your stash | `/rd stash` |
| `/rd trust <player>` ⭐ | Add player to trusted list | `/rd trust Steve` |
| `/rd untrust <player>` ⭐ | Remove player from trusted list | `/rd untrust Steve` |
| `/rd unlock [#]` | Make grave public | `/rd unlock 1` |
| `/rd blackmarket` ⭐ | Browse black market | `/rd blackmarket` |
| `/rd info` | Plugin statistics | `/rd info` |

### 👑 **Admin Commands**

| Command | Description | Example |
|---------|-------------|---------|
| `/rd tp\|teleport [#]` | Teleport to your grave | `/rd tp 1` |
| `/rd reload` | Reload configuration | `/rd reload` |
| `/rd saves` ⭐ | Open admin death backups GUI | `/rd saves` |
| `/rd license` | View license status and premium feature availability | `/rd license` |

---

## 🔧 **Configuration**

### **Core Setup**
```yaml
# plugins/RelishDeath/config.yml
language: en
license-key: "INSERT_KEY_HERE"
```

### ⏱️ **Timers**
```yaml
timers:
  groups:
    default: 5
    vip: 30
    premium: 60
    admin: 120
    permanent: -1

# Continue timer countdown when player is offline
  continue-offline: true
```

### ⚰️ **Grave Expiration**
```yaml
graves:
  # Options: black-market, stash, drop
  on-expire: black-market
```

### ⚡ **Timer Permissions**
- `relishdeath.timer.vip`
- `relishdeath.timer.premium`
- `relishdeath.timer.admin`
- `relishdeath.timer.permanent`

### 🎯 **Particle Navigation**
```yaml
particles:
  activation-distance: 50.0
  types:
    far: FLAME
    close: SOUL_FIRE_FLAME
    very-close: END_ROD
```

### 🧭 **Teleport Mode**
```yaml
teleport:
  # Options: far, close, very-close
  mode: close
```

### 🔔 **Notifications**
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

### 🎒 **Stash (Premium)**
```yaml
stash:
  expiration-hours: 24
```

### 🛒 **Black Market (Premium)**
```yaml
economy:
  enabled: true
  marketplace-enabled: true
  black-market:
    enabled: true
    # Use -1 to keep listings until purchased
    expiration-hours: -1
```
---

## ⚰️ **Grave System**

### 🗿 **Real Server-Side Entities**
RelishDeath creates **real server-side entities** for graves with full Geyser compatibility:
<div align="center">

![Grave](https://github.com/iM5LB/RelishDeath/blob/master/docs/assets/Grave.png)

</div>

**Entity Components:**
- **ItemDisplay** entities show the player's helmet/head
- **TextDisplay** entities show countdown and item count  
- **Interaction** entities handle right-click grave opening
- **Fully compatible** with Geyser (Bedrock players)

### 🕳️ **Void Death Protection**
Smart grave placement system for void deaths:

**Protection Features:**
- **Automatic detection** when players die below world minimum height + threshold
- **Area search** in configurable radius for safe locations using Minecraft's height maps
- **Performance optimized** with O(1) operations (no loops)
- **Safe placement** ensures graves spawn on solid ground with air space above

### 🎯 **Particle Navigation System**
Dynamic particle trails guide players to their graves:

**Navigation Features:**
- **Automatic activation** when near graves (configurable distance)
- **Ground-following paths** that navigate around obstacles
- **Distance indicators** show remaining distance to grave
- **Multiple trail types** with customizable particle effects
- **Performance optimized** with smart rendering limits

<div align="center">

![particle-trail](https://github.com/iM5LB/RelishDeath/blob/master/docs/assets/particle-trail.gif?raw=true)

</div>

---

## 🎒 **Stash System** ⭐

RelishDeath can safely stash overflow items **without overwriting your inventory**.

**Stash Features:**
- **Per-grave packages** - overflow items stay tied to the grave they came from
- **Click-to-claim items** - take items one-by-one without losing slots
- **Expiration** - stash packages are kept for a limited time (configurable)

Command: `/rd stash` ⭐

---

## 🛒 **Black Market System** ⭐

When graves expire, they can be listed on the black market for other players to purchase.

<div align="center">

![BlackMarket
](https://github.com/iM5LB/RelishDeath/blob/master/docs/assets/BlackMarket.png?raw=true)
</div>

**Market Features:**
- **Automatic listing** when graves expire naturally
- **Economy integration** with Vault-compatible plugins
- **Configurable pricing** based on grave contents value
- **Optional listing expiration** (`expiration-hours`, use `-1` to keep until purchased)
- **Full content transfer** - buyer receives all grave items

### 💪 **Market Configuration**
```yaml
economy:
  enabled: true
  marketplace-enabled: true
  black-market:
    enabled: true
    expiration-hours: -1

graves:
  on-expire: black-market

stash:
  expiration-hours: 24
```

---

## 💾 **Death Backup System** ⭐

### 🔄 **Admin Recovery Tools**
Comprehensive backup and recovery system for server administrators:
<div align="center">

![DeathBackups](https://github.com/iM5LB/RelishDeath/blob/master/docs/assets/DeathBackups.png?raw=true)

</div>

**Backup Features:**
- **Automatic backups** of every death event (stored in SQLite)
- **Admin GUI interface** for browsing all player deaths
- **Inventory restoration** with overflow protection system
- **Detailed death information** including cause, location, time, and XP

### 📊 **Death Information Tracking**
Death backups are stored in `plugins/RelishDeath/relishdeath.db` (SQLite) and include inventory, XP, cause, time, and location.

---

## 🤝 **Trust System** ⭐

### 👥 **Player Trust Management**
Players can share grave access with friends:

**Trust Features:**
- **Individual trust** - Add specific players to your trusted list
- **Configurable limits** - Trust limits per permission group
- **Easy management** - Simple commands for adding/removing trusted players

### 🔒 **Security Options**
```yaml
trust:
  enabled: true
  max-trusted-players: 10
```


## 🌍 **Multi-Language Support**

### 🗣️ **Built-in Languages**
- `en` (English)
- `ar` (Arabic)

### 🌐 **Custom Languages**
1. Create a new file: `plugins/RelishDeath/lang/es.yml`
2. Set the language in `config.yml`:

```yaml
language: es
```

RelishDeath uses MiniMessage in its language files (`<red>`, `<gold>`, `<bold>`, etc.).

---

## 🎨 **GUI Features** ⭐

RelishDeath premium GUIs are fully MiniMessage-based and include page navigation arrows:
- **Black Market GUI** - browse listings and purchase full graves
- **Stash GUI** - open a package and take items by clicking them
- **Admin Backups GUI** - browse and restore death backups

---

## 📈 **Performance & Scalability**

### ⚡ **Optimization Features**
- **Spatial Partitioning** - Efficient hologram rendering for 500+ players
- **Async Database Operations** - Non-blocking SQLite operations  
- **Height Map Usage** - O(1) void protection using Minecraft's cached data
- **Entity Culling** - Holograms only render when players are nearby
- **Particle Optimization** - Smart trail rendering with distance limits

### 📊 **Scalability Options**
- **SQLite** for small-medium servers (0-200 players)
- **Configurable render distances** for performance tuning
- **Memory-efficient caching** with automatic cleanup

---

## 📄 **License**

**RelishDeath is proprietary software. All rights reserved.**

### License Types

#### 🆓 Free Version
- Available without license key
- Includes basic grave system, advanced holograms, particle navigation, remote restoration, void protection, auto-respawn, and core commands
- May be used on unlimited servers
- **NOT open source** - modification and redistribution prohibited

#### ⭐ Premium Version
- Requires valid license key from M5LB
- Includes premium-only features such as Admin Recovery System, Black Market, Trust System, and Economy Integration
- License key tied to purchaser and server count
- **NOT open source** - modification and redistribution prohibited

For full license terms, see [LICENSE](https://github.com/iM5LB/relishdeath?tab=License-1-ov-file) file.

### Obtain Premium License

To get a premium license key:
- 🛒 **Buy a key from [M5LB Store](https://m5lb.run.place/)**

---

<div align="center">

**Made with ❤️ by M5LB**

</div>
