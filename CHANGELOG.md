# Changelog

All notable changes to Shell'Naga, newest first. Downloads and checksums: [Releases](https://github.com/shellnaga/shellnaga/releases) or <https://shellnaga.sh/#download>.

## 0.2.1 — 2026-11-17

- Optional AI assistant, off by default: explains a failed command or writes one for you.
- The AI uses a local model or your own key, and never runs a command on its own.
- Drag a pane by its handle to another spot, to the tab bar or out into a new window.
- Split menus show where the new pane goes, and panes can swap places.
- "Update now" looks for the newest version first, so it no longer installs an older one.
- Settings › Appearance › Window colors › Match the scheme: the bar, tabs, menus, dialogs and Settings take your color scheme's own accent instead of Shell'Naga's cyan.
- Window colors › Shell'Naga: the bar and menus follow the light or dark mode you chose in Shell'Naga.
- The default font now has every weight from 100 to 800, and the weight lists show only the weights your font has.
- Bold in bright colors shows again in Grass, Ocean and Red Sands.
- The Appearance preview now shows ligatures, symbols from the fallback font, bold in bright colors and the inner margin.
- Open in WinSCP: keys that only came from the synced folder aren't trusted; WinSCP asks.
- Vault: a vault that can't be read right now (say, in use by another program) offers Try again and can no longer be deleted until it reads again.
- Sync: if this PC's record of the vault's version is damaged, new versions from the folder wait for Push now or Pull now instead of coming in on their own.
- Vault: when a change can't be saved, it is no longer kept as if it were: a removed entry comes back and an updated password goes back to the saved one.
- The splash screen's loading bar is now amber, in Shell'Naga's gold.
- Keyboard focus rings are easier to see on every background.
- shellnaga --version prints the version without opening a window.
- Other stability fixes.

## 0.2.0 — 2026-11-14

- 15 free coding fonts to install from Settings › Appearance, no admin needed.
- What's new now shows in your language, as an easy-to-read list.
- Anonymous statistics have three levels: All statistics, Errors only and Off.
- Unexpected closes and failed updates are now counted, so we can fix them sooner.
- How long you use the app is counted only in broad ranges, and only with All statistics.
- Closing a tab no longer asks about system programs that aren't running in it.
- Commands typed while the PC is busy are no longer marked as finished before they end.
- tmux: if the connection drops while opening a session, the tab no longer gets stuck.
- Plugins: removing a plugin no longer fails with an "Access denied" error.
- Other stability fixes.

## 0.1.2 — 2026-11-12

- Settings: the "Modified" filter now also works on the page you are on.
- Settings work with screen readers (Narrator, NVDA).
- Settings keep your place after "Reset to default" or a change made outside the app.
- Settings reload on their own when another program had the file locked.
- Vault: a vault from a newer version asks you to update instead of saying it is damaged.
- Symbols such as ✳ ✔ ☂ show as text in the text color; real emoji stay in color.
- Warnings in Settings show in the warning color.

## 0.1.1 — 2026-11-12

- Settings: modified options are marked, each one has "Reset to default", and the search has a "Modified" filter.
- Settings: labels fit in every language, and options that only apply to new tabs or connections say so.
- Appearance: "Reset appearance…" brings back the default look in one step.
- Color schemes: a new editor with search and a live preview; editing a built-in scheme saves a copy.
- Color schemes changed outside the app reload right away.
- Panes: "Move pane to new tab", "New tab with profile" in the menu, and a clearer focus ring.
- Installer: in English, with a desktop shortcut and a "Launch Shell'Naga" option at the end.
- Anonymous usage statistics: no banner inside the app anymore; the installer and the website explain them.
- Closing a tab with a program still running in it asks first more reliably.

## 0.1.0 — 2026-11-11

- First public release.
- Native Windows terminal: WSL, PowerShell, Git Bash and cmd in one window, with tabs and split panes.
- SSH, SFTP, Serial and Telnet, with passwords in an encrypted vault.
- Images in the terminal (Sixel and Kitty) and tmux -CC integration.
- Color schemes, keyword highlighting, snippets and a command palette.
- Settings, profiles and snippets sync through a folder you choose.
- Interface in English, Portuguese (Brazil) and Spanish.
- Signed updates with one-click roll back.
