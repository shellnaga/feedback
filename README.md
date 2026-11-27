<p align="center"><img src="logo.svg" width="96" height="96" alt="Shell'Naga logo"></p>

# Shell'Naga

A native terminal and SSH client for Windows 11 and Linux, written in Rust. Tabs and split panes, WSL, PowerShell,
Git Bash and cmd in one window on Windows, a native SSH client with jump hosts, SFTP, mosh and tmux, drawn on the GPU.
Free, no account.

**The source code is not in this repository.** Shell'Naga is closed-source software distributed under its
[license agreement](https://shellnaga.sh/eula). This repository is where we publish release notes and installers
and where you report bugs and share ideas.

## Download

- **[shellnaga.sh/#download](https://shellnaga.sh/#download)** is the official download page.
- **[Releases](https://github.com/shellnaga/feedback/releases)** carry the same files as the site: for Windows 11
  (64-bit) the installer (`.msi`), the `.exe` and the portable `.zip` with `SHA256SUMS.txt`; for Linux (x86_64,
  Wayland or X11) the AppImage, which runs on any distribution, with `SHA256SUMS-linux.txt`. The in-app update check
  uses shellnaga.sh. The `.deb`, the apt repository and Flathub come later.
- **Scoop** (Windows): `scoop bucket add shellnaga https://github.com/shellnaga/scoop-shellnaga`, then
  `scoop install shellnaga/shellnaga`.
- Verify a download: on Windows, `Get-FileHash .\shellnaga-<version>-x64-setup.msi` and compare it with
  `SHA256SUMS.txt`; on Linux, `sha256sum -c --ignore-missing SHA256SUMS-linux.txt` in the folder of the AppImage.

## Verify the apt key

The apt repository for Debian and Ubuntu (`https://repo.shellnaga.sh/apt`) is signed. The key is served by the same
host as the packages, so check its fingerprint against this page, which is published somewhere else, before you trust it.

The fingerprint of the primary key is:

```
4FBF 86E4 1563 1D0A 3EBD FE0D 362B E2A7 E491 2BD8
```

1. Download the key and print its fingerprint:
   ```
   curl -fsSL https://repo.shellnaga.sh/shellnaga.asc -o shellnaga.asc
   gpg --show-keys --with-fingerprint shellnaga.asc
   ```
2. Compare it with the fingerprint above (`gpg` prints it with an extra space in the middle; the characters are the same).
3. Stop if it differs. Do not install the key, and write to [support@shellnaga.sh](mailto:support@shellnaga.sh).

The key is Ed25519, the user ID is `Shell'Naga apt <apt@shellnaga.sh>`, and it has two signing subkeys that expire on
2028-11-21: `7BE7 6D70 7DDF CA66 7B12 7AB4 2FB2 A633 6987 63C9` signs the repository, and
`E073 8F9E 7E76 A0A8 1A12 1CE8 7CD5 ACE6 F1C1 0E08` is the manual fallback. Both are trusted by the same key, so either
one can sign without any change on your machine. The primary key stays offline and never signs the repository.
The install commands are on the [download page](https://shellnaga.sh/#download). We change this fingerprint only with a
notice on the site and in this repository.

## What's new

See the [CHANGELOG](CHANGELOG.md) or the [Releases](https://github.com/shellnaga/feedback/releases) page.

## Report a bug

[Open a bug report](https://github.com/shellnaga/feedback/issues/new/choose). The form asks for the app version,
your operating system (Windows 11 or Linux) and its version, the shell you were using and the steps to reproduce.
Please do not include passwords, host names, keys or other personal data in logs and screenshots.

## Ideas and questions

Use [Discussions](https://github.com/shellnaga/feedback/discussions): feature ideas, how-to questions and
general feedback. Please search before posting; a bug belongs in [Issues](https://github.com/shellnaga/feedback/issues).

## More

- [Privacy policy](https://shellnaga.sh/privacy)
- [License agreement (EULA)](https://shellnaga.sh/eula)
- [Security policy](SECURITY.md)
- Contact: [support@shellnaga.sh](mailto:support@shellnaga.sh)
