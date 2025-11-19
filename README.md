# tmux_settings

My personal tmux configuration files for easy computer switching. This repository contains my tmux dotfiles, designed to be portable and simple to deploy across multiple machines.

## What is this?

This repository stores my tmux configuration, making it easy to maintain consistent tmux settings across different computers. By keeping these dotfiles in version control, I can quickly set up my preferred tmux environment on any new machine or keep existing setups synchronized.

## Installation

### Quick Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/wvmitchell/tmux_settings.git ~/.tmux_settings
   ```

2. Create a symlink to your tmux configuration:
   ```bash
   ln -s ~/.tmux_settings/.tmux.conf ~/.tmux.conf
   ```

3. Reload tmux configuration (if tmux is already running):
   ```bash
   tmux source-file ~/.tmux.conf
   ```

### Alternative: Direct Configuration

You can also copy the configuration file directly:
```bash
cp ~/.tmux_settings/.tmux.conf ~/.tmux.conf
```

## Usage

After installation, your tmux sessions will automatically use the configuration from this repository. Any updates to the configuration can be pulled down and reloaded:

```bash
cd ~/.tmux_settings
git pull
tmux source-file ~/.tmux.conf
```

## Updating Configuration

When you make changes to your tmux configuration:

1. Edit the configuration file in this repository
2. Test your changes by reloading tmux: `tmux source-file ~/.tmux.conf`
3. Commit and push your changes:
   ```bash
   git add .tmux.conf
   git commit -m "Update tmux configuration"
   git push
   ```

## Related Repositories

- [nvim_settings](https://github.com/wvmitchell/nvim_settings) - My Neovim configuration files

Together, these repositories provide a complete terminal development environment that can be quickly deployed on any machine.

## About tmux

tmux is a terminal multiplexer that allows you to run multiple terminal sessions within a single window. It's particularly useful for:
- Managing multiple terminal panes and windows
- Keeping sessions alive when disconnecting from remote servers
- Organizing your workspace efficiently

For more information about tmux, visit the [official tmux wiki](https://github.com/tmux/tmux/wiki).
