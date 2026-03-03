# Frank's VS Code

Personal VS Code / VSCodium setup — themes, settings, and extensions.

## Themes

### Frank's Tomorrow Night Minimal

Muted, minimal dark theme based on the Tomorrow Night palette. Dark gray backgrounds (`#1f1f1f` editor, `#1a1a1a` chrome) with soft syntax colors.

### Frank's Tomorrow Midnight Minimal

Near-black variant of Tomorrow Night Minimal. Same syntax palette pushed onto a much darker canvas (`#111111` editor, `#0c0c0c` chrome).

### Frank's Gruvbox Dark

Warm, high-contrast Gruvbox theme with a deep teal-black background (`#031417`). Rich syntax colors — green strings, red keywords, yellow types, aqua functions.

## Setup

### 1. Clone the repo

```bash
git clone git@github.com:frank-besson/franks-vs-code.git ~/Developer/franks-vs-code
```

### 2. Install the themes

Symlink into the extensions directory:

```bash
# VS Code
ln -s ~/Developer/franks-vs-code ~/.vscode/extensions/franks-vs-code

# VSCodium
ln -s ~/Developer/franks-vs-code ~/.vscode-oss/extensions/franks-vs-code
```

Restart the editor, then select a theme via `Cmd+K Cmd+T` (or `Ctrl+K Ctrl+T`).

### 3. Apply settings (optional)

Copy the editor settings:

```bash
# VS Code (macOS)
cp settings/settings.json ~/Library/Application\ Support/Code/User/settings.json

# VSCodium (macOS)
cp settings/settings.json ~/Library/Application\ Support/VSCodium/User/settings.json
```

### 4. Install extensions (optional)

```bash
# VS Code
cat settings/extensions.txt | xargs -L 1 code --install-extension

# VSCodium
cat settings/extensions.txt | xargs -L 1 codium --install-extension
```

## VSCodium

[VSCodium](https://vscodium.com) is the open-source build of VS Code without Microsoft telemetry. It runs alongside VS Code as a separate app with its own config at `~/.vscode-oss/`.

Install on macOS:

```bash
brew install --cask vscodium
```

Extensions are sourced from [Open VSX](https://open-vsx.org) instead of the Microsoft marketplace. Most extensions are available on both, but some Microsoft-exclusive ones (e.g. `simonsiefke.svg-preview`) are not.

## License

MIT
