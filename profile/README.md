# airgap-devkit

**Air-gapped developer toolkit — install, manage, and distribute developer tools in network-restricted environments. Runs entirely offline. Zero CDN dependencies.**

[![CI](https://github.com/airgap-devkit/devkit/actions/workflows/ci.yml/badge.svg)](https://github.com/airgap-devkit/devkit/actions/workflows/ci.yml)
[![Latest Release](https://img.shields.io/github/v/release/airgap-devkit/devkit?label=release)](https://github.com/airgap-devkit/devkit/releases/latest)
[![License: AGPL-3.0-or-later](https://img.shields.io/badge/license-AGPL--3.0--or--later-blue.svg)](https://github.com/airgap-devkit/devkit/blob/main/LICENSE)

---

## What is airgap-devkit?

airgap-devkit is a self-contained toolkit for provisioning developer environments on machines that have no internet access. It ships as a single static Go binary with an embedded web UI — no Python runtime, no Node, no external package manager needed at deploy time.

Engineers on air-gapped networks get a dashboard to install, update, and health-check their tools. Admins get batch install profiles, custom manifests, and first-class CI/CD integration — all without ever touching a CDN.

| Capability | Details |
|---|---|
| **Tools** | 17+ managed tools — CMake, Conan, Python, GDB, gRPC, .NET 10, VS Code extensions, and more |
| **Interfaces** | CLI installer / localhost web UI / embedded dashboard |
| **Install profiles** | Minimal / C++ Developer / DevOps / Full — or define your own |
| **CI/CD** | GitHub Actions / GitLab CI / Jenkins / Jira / Confluence |
| **Auth** | Session token auth, HTTPS support |
| **Platforms** | Windows 11 / RHEL 8 Linux |

---

## Why airgap-devkit?

- **Truly offline.** No CDN calls at install time. Every artifact is bundled or fetched once and served locally.
- **Single static binary.** The DevKit Manager is a compiled Go binary — drop it on any supported machine and run it.
- **Web UI included.** A built-in dashboard shows tool status, health checks, and one-click installs without touching the terminal.
- **Profile-based installs.** Ship a `Minimal`, `C++ Developer`, `DevOps`, or `Full` profile — or define a custom manifest for your team.
- **CI-native.** Structured output, exit codes, and pipeline configs for Jenkins, GitLab CI, and GitHub Actions ship out of the box.
- **AGPL-licensed.** Free to use, study, and modify. Enterprise dual-licensing available.

---

## Quick start

**Download a release binary:**

→ [Latest release](https://github.com/airgap-devkit/devkit/releases/latest)

**Build from source (requires Go):**

```bash
git clone https://github.com/airgap-devkit/devkit.git
cd devkit
bash launch.sh          # starts the web UI at http://127.0.0.1:8080
```

**CLI one-liners:**

```bash
# Install with the default profile
bash install-cli.sh

# Install a specific profile
bash install-cli.sh --profile "C++ Developer"

# Uninstall
bash uninstall.sh
```

---

## Repositories

| Repo | Description |
|---|---|
| [airgap-devkit/devkit](https://github.com/airgap-devkit/devkit) | Engine — Go binary, web UI, install profiles, CI configs |
| [airgap-devkit/tools](https://github.com/airgap-devkit/tools) | Default tool manifests and install scripts |
| [airgap-devkit/teams](https://github.com/airgap-devkit/teams) | Forkable template for team-specific tool images |
| [airgap-devkit/prebuilt](https://github.com/airgap-devkit/prebuilt) | Optional prebuilt binary archives |

---

## Links

- [Releases](https://github.com/airgap-devkit/devkit/releases)
- [Changelog](https://github.com/airgap-devkit/devkit/blob/main/CHANGELOG.md)
- [Tool catalog](https://github.com/airgap-devkit/devkit/blob/main/TOOLS.md)
- [Contributing guide](https://github.com/airgap-devkit/devkit/blob/main/CONTRIBUTING.md)
- [Security policy](https://github.com/airgap-devkit/devkit/security)
- [License: AGPL-3.0-or-later](https://github.com/airgap-devkit/devkit/blob/main/LICENSE)
