# 🍎 AppMacOS — Mac Software Repository

> The most trusted, curated, and verified Mac software download repository.  
> Every app is manually reviewed, Apple-notarized, and malware-scanned before publishing.

[![Verified Publisher](https://img.shields.io/badge/Verified-Publisher-green?style=flat-square&logo=apple)](https://appmacos.com)
[![Apps](https://img.shields.io/badge/Apps-462%2B-blue?style=flat-square)](https://appmacos.com/apps)
[![License](https://img.shields.io/badge/License-MIT-gray?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/appmacos/software-repository?style=flat-square&color=yellow)](https://github.com/appmacos/software-repository/stargazers)
[![Last Updated](https://img.shields.io/badge/Updated-Daily-brightgreen?style=flat-square)]()

---

## 🌐 Website

**Visit us at → [appmacos.com](https://appmacos.com)**

Browse, search, and download Mac apps directly from our website — no terminal required.  
The website is the easiest way to explore the full AppMacOS collection.

---

## 📖 What is AppMacOS?

**AppMacOS** is a community-driven repository of the best Mac software available — free, freemium, and premium. We curate, verify, and publish apps so Mac users never have to worry about downloading something unsafe or outdated.

- 462+ apps across 8 categories
- Updated daily with new releases and version bumps
- Every app passes a 4-step security verification process
- Optimized for both Apple Silicon (M1/M2/M3/M4) and Intel Macs

---

## 🔒 Security & Verification

We take security seriously. Every single app in this repository goes through:

| Step | Check | Tool |
|------|-------|------|
| 1 | Source & developer identity verified | Manual review |
| 2 | Code signing validated | `codesign --verify` |
| 3 | Apple notarization confirmed | `spctl --assess --verbose` |
| 4 | Malware scan | VirusTotal + custom scanner |

You can verify any app yourself:

```bash
# Check code signing
codesign --verify --deep --strict /Applications/YourApp.app

# Verify Apple notarization
spctl --assess --verbose /Applications/YourApp.app
```

> 🛡️ If an app fails any of these checks, it is immediately removed from the repository and users are notified via the [issue tracker](https://github.com/appmacos/issue-tracker).

---

## 🚀 Install via Homebrew

The fastest way to install any AppMacOS app is through our official Homebrew tap.

```bash
# Step 1 — Add the AppMacOS tap (one time only)
brew tap appmacos/tap

# Step 2 — Install any app
brew install --cask appmacos/tap/alfred
brew install --cask appmacos/tap/istat-menus
brew install --cask appmacos/tap/cleanmymac-x

# Step 3 — Keep all apps up to date
brew upgrade --greedy
```

Browse all available casks → [appmacos/homebrew-tap](https://github.com/appmacos/homebrew-tap)

---

## 📦 App Categories

| Category | Apps | Description |
|----------|------|-------------|
| 🛠 Utilities | 148 | System tools, cleaners, monitors |
| 💻 Developer | 121 | IDEs, terminals, API tools, git clients |
| 📝 Productivity | 92 | Note-taking, task managers, launchers |
| 🎨 Creative | 64 | Design, video, photo, audio tools |
| 🔒 Security | 37 | VPNs, password managers, firewalls |
| 🌐 Internet | 29 | Browsers, download managers, email |
| 🎮 Entertainment | 21 | Media players, games, streaming |
| 🤖 AI Tools | 18 | Local AI, writing, code assistants |

---

## 🗂️ Repository Structure

```
software-repository/
├── apps/
│   ├── utilities/
│   ├── developer/
│   ├── productivity/
│   ├── creative/
│   ├── security/
│   ├── internet/
│   ├── entertainment/
│   └── ai-tools/
├── scripts/
│   ├── verify.sh         # Run security checks on an app
│   ├── scan.sh           # Malware scan script
│   └── update-index.sh   # Rebuild app index
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md
│   │   ├── app_submission.md
│   │   └── security_disclosure.md
│   └── workflows/
│       ├── verify-pr.yml  # Auto-verify app PRs
│       └── daily-scan.yml # Nightly malware scan
├── CONTRIBUTING.md
├── SECURITY.md
├── CODE_OF_CONDUCT.md
└── README.md
```

---

## ➕ Submit an App

Want to add an app to AppMacOS? We welcome contributions.

**Requirements before submitting:**

- [ ] App has an active developer / official source
- [ ] App is code-signed with an Apple Developer certificate
- [ ] App is notarized by Apple
- [ ] App is compatible with macOS 13 Ventura or later
- [ ] App has a clear, publicly available privacy policy

**How to submit:**

1. Fork this repository
2. Copy `apps/_template.yml` to the correct category folder
3. Fill in all required fields
4. Open a Pull Request — use the `app_submission` template
5. Our team will review within 48 hours

```yaml
# apps/_template.yml
name: "App Name"
developer: "Developer or Company Name"
version: "1.0.0"
category: "utilities"
website: "https://example.com"
download_url: "https://example.com/download"
homebrew_cask: "app-name"
license: "free | freemium | paid"
price: "$0 | $X.XX"
apple_silicon: true
intel: true
min_macos: "13.0"
description: "One-line description of what the app does."
tags:
  - tag1
  - tag2
```

---

## 🗳️ Request an App

Don't see an app you need? Head over to our [App Requests board](https://github.com/appmacos/app-requests) and open a request. The community votes, and the top 10 most-voted apps are added every month.

---

## 🐛 Report a Problem

Found a broken download, a security issue, or wrong information?

- **Bug / wrong info** → [Open an issue](https://github.com/appmacos/issue-tracker/issues/new?template=bug_report.md)
- **Security concern** → [Security disclosure](https://github.com/appmacos/issue-tracker/issues/new?template=security_disclosure.md) or email `security@appmacos.com`
- **App outdated** → Comment on the app's issue or open a PR with the updated version

---

## 🤝 Contributing

We welcome contributions of all kinds — new apps, version updates, documentation improvements, and bug fixes.

Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.  
All contributors must follow our [Code of Conduct](CODE_OF_CONDUCT.md).

---

## 📊 Stats

| Metric | Value |
|--------|-------|
| Total apps | 462 |
| Monthly installs | 94,000+ |
| Contributors | 12 |
| GitHub stars | 4,200+ |
| Avg PR review time | 48 hours |
| Security scan | Daily (automated) |

---

## 📜 License

This repository is licensed under the [MIT License](LICENSE).  
App names, logos, and trademarks belong to their respective developers.

---

## 🔗 Related Repositories

| Repository | Description |
|------------|-------------|
| [appmacos/homebrew-tap](https://github.com/appmacos/homebrew-tap) | Official Homebrew tap — install apps via terminal |
| [appmacos/issue-tracker](https://github.com/appmacos/issue-tracker) | Bug reports, feature requests, security disclosures |
| [appmacos/app-requests](https://github.com/appmacos/app-requests) | Community voting board for new app submissions |

---

<div align="center">

Made with ❤️ for the Mac community · [appmacos.com](https://appmacos.com) · [@appmacos](https://twitter.com/appmacos)

</div>

