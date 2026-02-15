# zsh configuration

My personal [zsh](http://www.zsh.org/) configuration, built up over years of daily use.

## What's Included

This repository contains a modular zsh configuration with:
- Custom aliases and functions
- Shell options and environment setup
- Plugin management and integrations

## Local Configuration

This configuration supports local overrides through two mechanisms, allowing you to extend or customize the configuration without modifying the repository files.

### `.zshrc.local`

Create a `~/.zshrc.local` file to add additional configuration that will be sourced after all standard configuration files are loaded.

```bash
# Example ~/.zshrc.local
export MY_CUSTOM_VAR="value"
alias myalias="my custom command"
```

### `.zsh.local/` Directory

Create a `~/.zsh.local/` directory with files matching the names of the standard configuration files to extend or override specific modules:

```bash
# Example ~/.zsh.local/aliases.zsh
alias ll="ls -lah"
alias gs="git status"

# Example ~/.zsh.local/functions.zsh
function my_custom_function() {
    echo "Hello from my local function"
}
```

The `load_file` function automatically sources files from `~/.zsh.local/` after loading the corresponding files from `~/.zsh/`, allowing you to add to or override the standard configuration on a per-file basis.

## Installation

This configuration can be installed using homeshick. Once installed, the zsh configuration will be placed in `~/.zsh`.
