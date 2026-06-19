# Homebrew Tap for virtuallytd

This is a [Homebrew](https://brew.sh/) tap for tools by virtuallytd.

## Available Formulae

### ccs - Claude Code Switcher

A CLI tool for running Claude Code in isolated Podman containers with separate profiles for different authentication methods (Vertex AI, API key) and MCP server configurations.

**Installation:**
```bash
brew install virtuallytd/tap/claude-code-switcher
```

**Prerequisites:**
- [Podman](https://podman.io/) (`brew install podman`)
- A running Podman machine (`podman machine init && podman machine start`)

**Quick Start:**
```bash
# Build the container image
ccs build

# Create a profile
ccs init work

# Launch Claude Code with a profile
ccs work ~/Projects/my-repo
```

**Usage:**
```bash
ccs <profile> [path]              # Launch Claude Code with the given profile
ccs init <name>                   # Create a new profile interactively
ccs build                         # Build/rebuild the container image
ccs profiles                      # List available profiles
ccs status                        # Show running containers
ccs stop [profile]                # Stop running container(s)
ccs --version                     # Show version
```

**Documentation:** https://github.com/virtuallytd/claude-code-switcher

## Using This Tap

### One-Time Install

```bash
brew install virtuallytd/tap/claude-code-switcher
```

### Tap First, Then Install

```bash
brew tap virtuallytd/tap
brew install claude-code-switcher
```

### Upgrade

```bash
brew upgrade claude-code-switcher
```

## Formula List

| Formula | Description | Homepage |
|---------|-------------|----------|
| `claude-code-switcher` | CLI tool for running Claude Code with isolated Podman profiles | [GitHub](https://github.com/virtuallytd/claude-code-switcher) |

## About

This tap is maintained by [virtuallytd](https://github.com/virtuallytd) and contains formulae for personal tools and utilities.

Formulae are automatically updated when new releases are created using [GoReleaser](https://goreleaser.com/).
