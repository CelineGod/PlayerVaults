# PlayerVaults 📦

A lightweight, high-performance, and reliable Player Vaults plugin built for **Paper / Spigot (1.20+)**. 

Designed with data integrity as a top priority, PlayerVaults prevents item duplication and item loss through slot-by-slot YAML persistence and silent event-driven auto-saving.

---

## ✨ Features

- **Slot-by-Slot Persistence:** Guarantees data stability and completely prevents item loss or wipe issues upon restart.
- **Silent Auto-Saving:** Automatically saves inventory state when a player closes their vault GUI (`InventoryCloseEvent`), with zero chat spam.
- **LuckPerms Integration:** Fully customizable vault access limits managed dynamically via permissions.
- **Configurable Messages & Settings:** Full control over vault limits and user notifications via `config.yml`.

---

## 🛠️ Commands & Permissions

### Commands
| Command | Aliases | Description |
| :--- | :--- | :--- |
| `/vault <number>` | `/pv <number>` | Opens the specified vault number. |

### Permissions
| Permission | Description |
| :--- | :--- |
| `playervaults.use` | Grants basic permission to access vaults. |
| `playervaults.amount.<number>` | Sets the maximum number of vaults accessible (e.g., `playervaults.amount.5`). |
| `playervaults.admin` | Grants unlimited access to all vaults, bypassing limit checks. |

---

## ⚙️ Configuration (`config.yml`)

```yaml
# PlayerVaults Configuration

# Maximum default vaults for players who have no specific limit permission
default-max-vaults: 1

# Custom messages (Color codes supported with &)
messages:
  no-permission: "&cYou do not have permission to use player vaults."
  max-vaults-exceeded: "&cYou only have access to &e{max} &cvault(s)!"
