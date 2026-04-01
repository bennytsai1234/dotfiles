# dotfiles

My dotfiles managed by [chezmoi](https://www.chezmoi.io/).

## Quick Setup on New Machine

```bash
sh -c "$(curl -fsLS get.chezmoi.io)" -- init --apply bennytsai1234
```

## What This Manages

- `~/.bashrc` — Bash configuration, aliases, and prompt
- `~/.gitconfig` — Git config with machine-specific user info (via template)
- `~/.zshrc` — Zsh configuration
- `~/.profile` — Login shell setup
- `~/.config/starship.toml` — Starship prompt theme
- `~/.config/atuin/config.toml` — Atuin shell history config
- `~/.inputrc` — Readline/keyboard configuration
- `~/.blerc` — BluOS CLI config

## Machine-Specific Configuration

Edit `~/.local/share/chezmoi/chezmoi.toml` to set machine-specific values:

```toml
[data]
    name = "Your Name"
    email = "your@email.com"
```

## Updating

```bash
chezmoi update        # Pull latest from repo and apply
chezmoi add ~/.newrc  # Add a new file
chezmoi apply         # Apply changes to home directory
```

## Notes

- Sensitive files (credentials, tokens) are managed separately and NOT committed to this repo
- See chezmoi docs for templates, encryption, and advanced usage
