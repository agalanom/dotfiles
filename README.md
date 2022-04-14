# dotfiles
🔧 .files

### Using the bootstrap script

To update, `cd` into your local `dotfiles` repository and then:

```bash
bash
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

My `~/.extra` looks something like this:

```bash
# Git credentials
# Not in the repository
GIT_AUTHOR_NAME="Author Name"
GIT_COMMITTER_NAME="$GIT_AUTHOR_NAME"
git config --global user.name "$GIT_AUTHOR_NAME"
GIT_AUTHOR_EMAIL="author@email.com"
GIT_COMMITTER_EMAIL="$GIT_AUTHOR_EMAIL"
git config --global user.email "$GIT_AUTHOR_EMAIL"
```

## Install Homebrew formulae

You can easily install all of the dependencies in the Brewfile with:

```bash
brew bundle
```

## Oh My ZSH
First install [Oh My ZSH](https://github.com/ohmyzsh/ohmyzsh)

Currently using the [agnoster](https://github.com/agnoster/agnoster-zsh-theme) theme.

Alternative [Powerlevel10k](https://github.com/romkatv/powerlevel10k) theme that is extremely configurable.

### Fonts
Many themes require installing the [Powerline Fonts](https://github.com/powerline/fonts) in order to render properly.

Set this font in iTerm2 (iTerm → Preferences → Profiles → Text → Font), in the dropdown select the desired Font. You will see it change on the fly.

### Enable word jumps and word deletion, aka natural text selection

By default, word jumps (option + → or ←) and word deletions (option + backspace) do not work. To enable these, go to "iTerm → Preferences → Profiles → Keys → Presets... → Natural Text Editing"

### Visual Studio Code config

Installing a patched font will mess up the integrated terminal in VS Code unless you use the proper settings. You'll need to go to settings (CMD + ,) and add or edit the following values:

- for Source Code Pro + Font Awesome: `"terminal.integrated.fontFamily": "'SourceCodePro+Powerline+Awesome Regular'"`. The single quotes are important! Restart VS Code after the config change.
- for Source Code Pro: `"terminal.integrated.fontFamily": "Source Code Pro for Powerline"`
- for Meslo: `"terminal.integrated.fontFamily": "Meslo LG M for Powerline"`
- for other fonts you'll need to check the font name in Font Book. You can right click on them on select "Show in Finder" to get the exact name.

You can also set the fontsize e.g.: `"terminal.integrated.fontSize": 14`

### Acknowledgments
Set up guide notes taken from [
kevin-smets/iterm2-solarized.md](https://gist.github.com/kevin-smets/8568070)

Lots of inspiration from the legendary [mathiasbynens/dotfiles](https://github.com/mathiasbynens/dotfiles) repo.
