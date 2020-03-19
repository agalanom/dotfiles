# dotfiles
🔧 .files

### Using the bootstrap script

To update, `cd` into your local `dotfiles` repository and then:

```bash
source bootstrap.sh
```

Alternatively, to update while avoiding the confirmation prompt:

```bash
set -- -f; source bootstrap.sh
```

### Specify the `$PATH`

If `~/.path` exists, it will be sourced along with the other files.

### Add custom commands without creating a new fork

If `~/.extra` exists, it will be sourced along with the other files. You can use this to add commands you don’t want to commit to a public repository.

### Install Homebrew formulae

You can easily install all of the dependencies in the Brewfile with:

```bash
brew bundle
```
