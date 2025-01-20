# keyshield

A simple utility to protect your game inputs from GNOME keyboard shortcuts.

## Overview

When gaming on GNOME, especially with WINE/Proton, system-level keyboard shortcuts can interfere with game controls. Keyshield temporarily disables these shortcuts while you play, and restores them when you're done.

## Installation

```bash
# Clone the repository
git clone https://github.com/popey/keyshield
cd keyshield

# Make the script executable
chmod +x keyshield

# Optional: Copy to your path
sudo cp keyshield /usr/local/bin/
```

## Usage

```bash
keyshield up     # Disable GNOME shortcuts (raise the shield)
keyshield down   # Re-enable GNOME shortcuts (lower the shield)
keyshield status # Check if the shield is raised or lowered
```

Your original keyboard shortcuts are automatically backed up to `~/.config/keyshield/keybindings.conf` before any changes are made.

## How It Works

Keyshield modifies several GNOME settings using `gsettings`, including:
- Mutter overlay key
- Shell overview toggles
- Window management shortcuts

When the shield is raised, these shortcuts are disabled, preventing them from interfering with your game inputs.

## License

MIT License - See LICENSE file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Authors

- Alan Pope ([@popey](https://github.com/popey))
