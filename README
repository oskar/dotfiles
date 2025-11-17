# 1. Install Homebrew
```bash
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
```

# 2. Install oh-my-zsh
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

# 3. Create chezmoi config

Create file `~/.config/chezmoi/chezmoi.toml` with substituted values in data section
```
[git]
    autoCommit = true
    autoPush = true
[edit]
    command = "code"
    args = ["--wait"]
[merge]
    command = "bash"
    args = [
        "-c",
        "cp {{ .Target }} {{ .Target }}.base && code --new-window --wait --merge {{ .Destination }} {{ .Target }} {{ .Target }}.base {{ .Source }}",
    ]
[data]
    email = "<email-address>"
```

# 4. Install chezmoi
```bash
brew install chezmoi
```

# 5. Init chezmoi and apply dotfiles
```bash
chezmoi init --apply https://github.com/oskar/dotfiles.git
```
