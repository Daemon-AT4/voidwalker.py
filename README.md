![VoidWalker UI](attachments/voidwalker-screenshot.png)

```text
+====================================================================+
|  V O I D W A L K E R                                               |
|  ELITE PENETRATION TESTING ARSENAL BUILDER                         |
|  250+ TOOLS :: UBUNTU/DEBIAN :: CYBERPUNK TUI                       |
+====================================================================+
|  [][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][]    |
+====================================================================+
```

# VoidWalker
![Version](https://img.shields.io/badge/version-3.9.2-ff2d95?style=for-the-badge)
![Python](https://img.shields.io/badge/python-3.x-00e5ff?style=for-the-badge)
![Platform](https://img.shields.io/badge/platform-Ubuntu%2FDebian-00ff9f?style=for-the-badge)
![Tools](https://img.shields.io/badge/arsenal-250%2B-ffd166?style=for-the-badge)
![License](https://img.shields.io/badge/license-Not%20specified-ff5555?style=for-the-badge)

```
+--------------------------------------------------------------------+
| VOIDWALKER :: ELITE PENETRATION TESTING ARSENAL BUILDER             |
| Animated TUI installer for Ubuntu/Debian with 250+ security tools   |
+--------------------------------------------------------------------+
```

```
+--------------------------------------------------------------------+
| WARNING: Authorized use only. For legal, ethical security testing. |
+--------------------------------------------------------------------+
```

## What It Does
- Launches an animated cyberpunk TUI with banners, progress bars, and live status
- Builds a full workspace at `~/voidwalker` with engagement templates and tool vaults
- Installs system packages via `apt-get` (Ubuntu/Debian)
- Installs Python tools via `pipx`
- Installs Go tools via `go install` (and select .deb packages)
- **Installs Ruby gems** (wpscan, evil-winrm)
- **Installs special tools** (kerbrute, ligolo-ng, chisel)
- Downloads Windows binaries, ZIPs, and Git repos into the Windows toolkit
- Clones tool repos and downloads files across curated categories
- **Auto-extracts rockyou.txt** wordlist
- **Creates bash aliases** for common pentesting commands
- Provides an installation preview plus success/fail summary stats
- Includes CLI search helpers for PoCs, NSE scripts, Exploit-DB, Shodan, and dorks
- **HTB Dante ProLab Ready** - Includes all tools mentioned in HTB Dante walkthroughs

## Arsenal Map
```
[ Windows Binaries ] [ PowerShell Scripts ] [ Linux Tools ]
[ Pivoting Tools ]   [ C2 Frameworks ]     [ Maldev Tools ]
[ Web Tools ]        [ Cloud Tools ]       [ Container Tools ]
[ Phishing Tools ]   [ Wireless Tools ]    [ Webshells & Payloads ]
[ Exploit Frameworks ] [ Wordlists ]
```

## Setup
```
1) Ubuntu/Debian host with sudo access
2) Python 3
3) git, pipx, and Go installed (for full tool coverage)
4) Reliable internet (downloads are large)
```

Quick start:
```
python3 voidwalker.py
```

Optional env var:
```
export SHODAN_API_KEY="your-api-key"
```

## Usage
Interactive menu:
```
python3 voidwalker.py
```

Search commands:
```
python3 voidwalker.py poc CVE-2021-44228
python3 voidwalker.py nse http
python3 voidwalker.py shodan apache
python3 voidwalker.py exploitdb wordpress
python3 voidwalker.py dork
```

## Workspace Layout
```
~/voidwalker/
|-- engagements/
|   `-- _template/ (notes, scans, loot, exploits, reports)
|-- tools/
|   |-- windows/     |-- powershell/ |-- linux/   |-- pivoting/
|   |-- c2/          |-- maldev/     |-- web/     |-- cloud/
|   |-- container/   |-- phishing/   |-- wireless/
|-- payloads/ (webshells, reverse-shells, shellcode)
|-- wordlists/ (passwords, usernames, directories, subdomains, kerberos)
|-- notes/ (cheatsheets, methodology)
|-- scans/
|-- reports/
```

## HTB Dante ProLab Support
VoidWalker now includes comprehensive support for HTB Dante ProLab with all tools from the official walkthroughs:

**Included Features:**
- ✓ All essential Ubuntu/Debian packages (fping, nmap, enum4linux, patator, etc.)
- ✓ Ruby gems (wpscan, evil-winrm)
- ✓ Special tools (kerbrute, ligolo-ng, chisel) - auto-downloaded and installed
- ✓ Impacket suite (via pipx)
- ✓ CrackMapExec (via pipx)
- ✓ LinPEAS, WinPEAS, pspy
- ✓ BloodHound + SharpHound
- ✓ Metasploit Framework
- ✓ Wordlists: SecLists, Trickest wordlists collection
- ✓ rockyou.txt auto-extraction
- ✓ Bash aliases for common commands

**Bash Aliases Added:**
```bash
# Server aliases
www              # Python HTTP server on port 80
wwwphp           # PHP server on port 80
smbserve         # Impacket SMB server

# Nmap shortcuts
nmap-quick       # Fast port scan
nmap-full        # Full service scan
nmap-vuln        # Vulnerability scan

# Enumeration
enum-smb         # enum4linux full scan
enum-ldap        # LDAP enumeration
ffuf-dir         # Directory fuzzing with SecLists
```

To activate aliases after installation:
```bash
source ~/.bash_aliases
```

## Do / Don't
DO
- Use on authorized targets only
- Run inside a dedicated VM or lab where possible
- Review tool licenses and intended use
- Expect large downloads and storage usage
- Keep your tool cache updated by re-running the installer

DON'T
- Run on production systems without approval
- Assume every downloaded binary is safe or signed
- Commit the downloaded tool cache into Git
- Use without understanding local laws and scope
- Share outputs that contain sensitive data

## Search Helpers (Details)
- PoC search: uses local `PoC-in-GitHub` repo when available, falls back to GitHub API
- NSE search: scans local Nmap scripts or suggests common scripts if Nmap is missing
- Exploit-DB search: greps local `exploitdb` if present, otherwise points to online search
- Shodan search: uses `SHODAN_API_KEY` if set, otherwise prints example dorks
- Dork generator: interactive builder with prebuilt dork sets and optional browser open

## Notes
- Designed for Ubuntu/Debian. Other distros are not supported by the installer flow.
- The installer uses `apt-get`, `pipx`, `go`, `git`, and direct downloads.
- Tools and repos are installed under `~/voidwalker`.

## License
Not specified in this repository.
