<p align="center"><img src="logo.svg" width="96" height="96" alt="Shell'Naga logo"></p>

# Shell'Naga

A native terminal and SSH client for Windows 11, written in Rust. Tabs and split panes, WSL, PowerShell, Git Bash
and cmd in one window, a native SSH client with jump hosts, SFTP, mosh and tmux, drawn on the GPU. Free, no
account.

**The source code is not in this repository.** Shell'Naga is closed-source software distributed under its
[license agreement](https://shellnaga.sh/eula). This repository is where we publish release notes and installers
and where you report bugs and share ideas.

## Download

- **[shellnaga.sh/#download](https://shellnaga.sh/#download)** is the official download page.
- **[Releases](https://github.com/shellnaga/feedback/releases)** carry the same installers (`.msi`, `.exe`,
  portable `.zip`) and the same `SHA256SUMS.txt` as the site. The in-app update check uses shellnaga.sh.
- Verify a download with `Get-FileHash .\shellnaga-<version>-x64-setup.msi` and compare it with `SHA256SUMS.txt`.

## What's new

See the [CHANGELOG](CHANGELOG.md) or the [Releases](https://github.com/shellnaga/feedback/releases) page.

## Report a bug

[Open a bug report](https://github.com/shellnaga/feedback/issues/new/choose). The form asks for the app version,
your Windows version, the shell you were using and the steps to reproduce. Please do not include passwords,
host names, keys or other personal data in logs and screenshots.

## Ideas and questions

Use [Discussions](https://github.com/shellnaga/feedback/discussions): feature ideas, how-to questions and
general feedback. Please search before posting; a bug belongs in [Issues](https://github.com/shellnaga/feedback/issues).

## More

- [Privacy policy](https://shellnaga.sh/privacy)
- [License agreement (EULA)](https://shellnaga.sh/eula)
- [Security policy](SECURITY.md)
- Contact: [support@shellnaga.sh](mailto:support@shellnaga.sh)
