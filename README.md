# dotfiles
My dotfiles managed by [chezmoi](https://www.chezmoi.io/).

## Get started

### 1. Install chezmoi

```
brew install chezmoi
```

### 2. Clone dotfiles

```
chezmoi init https://github.com/gurutaka/dotfiles.git
```

### 3. Apply dotfiles

```
chezmoi apply
```

### 4. Set a Zsh configuration by copying/linking the Zsh configuration files provided:

```bash
setopt EXTENDED_GLOB
for rcfile in "${ZDOTDIR:-$HOME}"/.zprezto/runcoms/^README.md(.N); do
  ln -s "$rcfile" "${ZDOTDIR:-$HOME}/.${rcfile:t}"
done
```
ref: [sorin-ionescu/prezto: The configuration framework for Zsh](https://github.com/sorin-ionescu/prezto#installation)

