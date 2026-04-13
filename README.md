# Homebrew Tap for virtuallytd

This is a [Homebrew](https://brew.sh/) tap for tools by virtuallytd.

## Available Formulae

### ccs - Claude Code Switcher

A CLI tool for quickly switching between Claude Code profiles with different MCP server configurations and authentication methods.

**Installation:**
```bash
brew install virtuallytd/tap/claude-code-switcher
```

**Setup Shell Integration:**

After installing, add this function to your `~/.zshrc` or `~/.bashrc`:

```bash
ccs() {
  if [[ $# -eq 0 ]] || [[ "$1" == "switch" ]] || [[ "$1" == "reload" ]]; then
    eval "$(command ccs "$@")"
  else
    command ccs "$@"
  fi
}
```

Then reload your shell:
```bash
source ~/.zshrc  # or source ~/.bashrc
```

**Verify Installation:**
```bash
ccs version
```

**Usage:**
```bash
ccs              # Interactive profile switcher
ccs reload       # Reload current profile
ccs current      # Show active profile
ccs save <name>  # Save session token for profile
ccs help         # Show help
```

**Documentation:** https://github.com/virtuallytd/claude-code-switcher

## Using This Tap

### One-Time Install

To install a formula from this tap:
```bash
brew install virtuallytd/tap/<formula>
```

### Tap First, Then Install

Alternatively, you can add the tap first and then install as if the formulae were in the main repository:
```bash
brew tap virtuallytd/tap
brew install claude-code-switcher
```

### Upgrade

To upgrade a formula:
```bash
brew upgrade virtuallytd/tap/claude-code-switcher
```

Or if you've tapped the repository:
```bash
brew upgrade claude-code-switcher
```

## Formula List

| Formula | Description | Homepage |
|---------|-------------|----------|
| `claude-code-switcher` | CLI tool for switching between Claude Code profiles | [GitHub](https://github.com/virtuallytd/claude-code-switcher) |

## About

This tap is maintained by [virtuallytd](https://github.com/virtuallytd) and contains formulae for personal tools and utilities.

Formulae are automatically updated when new releases are created using [GoReleaser](https://goreleaser.com/).
