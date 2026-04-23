<div align="center">
  <img src="attachments/voidwalker-screenshot.png" alt="VoidWalker UI" width="800"/>

  # V O I D W A L K E R
  **ELITE PENETRATION TESTING ARSENAL BUILDER & WORKSPACE MANAGER**

  [![Version](https://img.shields.io/badge/version-4.2.0-ff2d95?style=for-the-badge&logo=python)](https://github.com/voidwalker)
  [![Platform](https://img.shields.io/badge/platform-macOS%20%7C%20Linux-00ff9f?style=for-the-badge&logo=apple)](https://github.com/voidwalker)
  [![Tools](https://img.shields.io/badge/arsenal-400%2B-ffd166?style=for-the-badge&logo=powershell)](https://github.com/voidwalker)
  [![C#](https://img.shields.io/badge/compiler-C%23%20%7C%20.NET-8a2be2?style=for-the-badge&logo=csharp)](https://github.com/voidwalker)
</div>

---

<br>

## ⚡ What is VoidWalker?
VoidWalker is an advanced, automated toolkit built for Red Teamers, Penetration Testers, and HTB Pro Lab players. It transforms a barebones macOS or Linux system into a fully equipped offensive workstation in minutes.

With **version 4.2.0**, VoidWalker has evolved beyond a simple downloader into a comprehensive engagement framework.

### 🔥 Key Features
- 🚀 **Blazing Fast Engine**: Multi-threaded, parallel downloads utilizing Python's `ThreadPoolExecutor`. Skips existing files and automatically retries failed connections with exponential backoff.
- 🔨 **Automated C# Build Pipeline**: Clones and compiles custom C# offensive tools from source via `dotnet build -c Release`. Bypasses basic signature detection by generating fresh binaries.
- 📓 **Obsidian Vault Scaffolding**: Instantly generates a structured, professional-grade engagement vault equipped with Dataview dashboards, templates (Hosts, Credentials, Findings), and dynamic attack cheatsheets.
- 🍏 **Cross-Platform Support**: Seamlessly installs dependencies via `apt-get` (Linux) or `brew` (macOS), configuring tools seamlessly across operating systems.
- 🕷️ **Massive AD Arsenal**: 100% coverage of the 2026 SharpCollection nightly roster, packed with the latest Active Directory exploitation and enumeration tools.
- 🗄️ **Integrated References**: Access a curated repository of Maldev learning resources, anonymous VPS providers, commercial C2 frameworks, and offensive guides directly from the CLI.

<br>

## 🛠️ The Arsenal
VoidWalker curates over 400 specialized tools across the following domains:

| Category | Description | Key Tools |
| :--- | :--- | :--- |
| **Windows Binaries** | Compiled C# AD recon, credential extraction, and lateral movement. | `Rubeus`, `Seatbelt`, `SharpHound`, `Certify`, `HandleKatz` |
| **C# Build Targets** | Automated source-to-binary compilation for OPSEC. | `ADCSPwn`, `SharpSCCM`, `GhostlyHollowing`, `SauronEye` |
| **Maldev & Evasion** | Custom loaders, sleep obfuscators, and shellcode runners. | `Freeze.rs`, `NimPlant`, `Ekko`, `CallStackMasker` |
| **C2 Frameworks** | Command and Control servers for post-exploitation. | `Havoc`, `Mythic`, `Sliver`, `Empire`, `Covenant` |
| **PowerShell** | Memory-resident scripts and AMSI bypasses. | `PowerSploit`, `Nishang`, `PowerView`, `Chimera` |
| **Cross-Platform** | Tunnels, proxies, and relays across OS boundaries. | `Chisel`, `Ligolo-ng`, `Kerbrute`, `Fscan` |

<br>

## ⚙️ Installation & Requirements

### Dependencies
- Python 3.8+
- `git`
- `.NET SDK 8.0+` (Required for the C# compilation pipeline)
- `brew` (macOS) or `apt` (Linux)

### Quick Start
```bash
# Clone the repository
git clone https://github.com/your-username/voidwalker.git
cd voidwalker

# Launch the interactive console
python3 voidwalker.py
```

<br>

## 🖥️ Usage & Commands

Launch the **interactive cyberpunk TUI** directly by running `python3 voidwalker.py` to access the main menu:
```text
[1] 🚀 Install Full Arsenal (400+ tools)
[2] ⚙️  Select Categories
[3] ⭐ View All Tools
[4] ✓  System Packages (apt/brew)
[5] 💎 Windows Binaries Only
[6] ⚡ Build C# Tools from Source
[7] 🛡️  Setup Pentest Obsidian Vault
[8] 🛡️  View Sources & Guides
[9] ❌ Exit
```

### CLI Search Helpers
VoidWalker includes built-in offline search modules:
```bash
python3 voidwalker.py poc CVE-2021-44228   # Search local PoC-in-GitHub databases
python3 voidwalker.py nse http             # Search Nmap scripts
python3 voidwalker.py shodan apache        # Shodan terminal query (needs SHODAN_API_KEY)
python3 voidwalker.py exploitdb wordpress  # Search Exploit-DB
python3 voidwalker.py dork                 # Interactive Google Dork generator
```

<br>

## 📓 Obsidian Vault Structure
Running the `[7] Setup Pentest Obsidian Vault` option scaffolds the following engagement template directly into your `~/voidwalker/Vault` directory:

```text
~/voidwalker/Vault/
├── 01_Admin/          (Rules of Engagement, Scope, Configs)
├── 02_Recon/          (OSINT, Nmap Scans, AD enumeration)
├── 03_Hosts/          (Individual Host templates via Dataview)
├── 04_Credentials/    (Hashes, Kerberos tickets, cleartext)
├── 05_Findings/       (Vulnerabilities mapped to CVSS)
├── 06_Payloads/       (Compiled binaries, webshells, scripts)
├── Cheatsheets/       (AD Attacks, File Transfers, Reverse Shells, etc.)
└── Dashboard.md       (Live Dataview engagement tracking)
```

<br>

## ⚠️ Disclaimer
**AUTHORIZED USE ONLY.** VoidWalker is designed strictly for educational purposes, authorized security testing, and Red Team operations. 

- **DO** use on authorized targets only.
- **DO NOT** run on production systems without explicit consent.
- **DO NOT** commit the downloaded tool cache into Git.

The authors are not responsible for any misuse, damage, or illegal activities caused by this tool.
