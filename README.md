# ipsw-skill

A Claude Code skill for Apple firmware and binary reverse engineering using the [ipsw](https://github.com/blacktop/ipsw) CLI tool.

## What This Skill Provides

This skill empowers Claude to assist with:

- **Disassembling functions** in dyld_shared_cache and Mach-O binaries
- **Dumping Objective-C headers** from private frameworks
- **Downloading IPSWs/OTAs** and extracting kernelcaches
- **Analyzing entitlements** across iOS/macOS binaries
- **KEXT extraction and analysis** from kernelcaches
- **Tracking changes** between iOS/macOS versions

## Installation

### Prerequisites

Install the `ipsw` CLI tool:

```bash
brew install blacktop/tap/ipsw
```

### Claude Code

Install via the Claude Code marketplace:

```bash
claude /marketplace install blacktop/ipsw-skill
```

Or install directly from GitHub:

```bash
claude /install-skill https://github.com/blacktop/ipsw-skill
```

### Codex CLI

Install via the Codex marketplace:

```bash
codex /marketplace install blacktop/ipsw-skill
```

Or install directly:

```bash
codex /install-skill https://github.com/blacktop/ipsw-skill
```

## Usage Examples

Once installed, Claude will automatically use this skill when you ask about Apple reverse engineering tasks:

> "Disassemble the _malloc function from the system dyld_shared_cache"

> "Dump the Objective-C headers for SpringBoardServices"

> "Download the latest IPSW for iPhone 15 Pro and extract the kernel"

> "Find all binaries with the platform-application entitlement in iOS 18"

> "Extract the sandbox KEXT from this kernelcache"

> "What classes in Security.framework handle keychain operations?"

## Skill Contents

```
ipsw/
├── SKILL.md                    # Core workflows and quick reference
└── references/
    ├── dyld.md                 # dyld_shared_cache analysis commands
    ├── macho.md                # Mach-O binary analysis commands
    ├── kernel.md               # Kernel & KEXT analysis commands
    ├── download.md             # Firmware download & extraction
    ├── class-dump.md           # ObjC header dumping
    └── entitlements.md         # Entitlements database & queries
```

## Resources

- [ipsw Documentation](https://blacktop.github.io/ipsw)
- [ipsw GitHub](https://github.com/blacktop/ipsw)
- [Discord Community](https://discord.gg/BEamsHAWAh)

## License

MIT
