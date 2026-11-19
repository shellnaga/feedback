# Changelog

All notable changes to Shell'Naga, newest first. Downloads and checksums: [Releases](https://github.com/shellnaga/shellnaga/releases) or <https://shellnaga.sh/#download>.

## 0.2.2 — 2026-11-19

- Connect… (Ctrl+Shift+O): one box for saved connections, recent ones and ~/.ssh/config hosts; type user@host to connect.
- Command line: `shellnaga --quick-connect [destination]` and a `ssh://` or `telnet://` link given as an argument open Connect… with the text filled in; nothing connects until you press Enter.
- Connect…: “Save this connection” (on by default) in the password question saves a destination you typed as a profile, with its password in the vault, once the server accepts it; or choose “Save…” on the strip after connecting. The tab keeps its connection.
- Connect…: Ctrl+Enter splits right and connects, Ctrl+Shift+Enter splits below, Alt+Enter replaces the pane (asking first if something runs); Tab completes the box with the row.
- Connect…: the row's menu (Menu key) offers Edit… (Ctrl+E), Duplicate, Copy ssh command, Delete… (Del; its saved password leaves the vault too) and Remove from recent; Ctrl+S saves a recent connection. Hosts of ~/.ssh/config can only be opened or copied.
- Connect…: each connection shows a badge: connected (and in how many tabs), connecting, or failed last time; the empty box has Recent, Saved and ~/.ssh/config sections, says when the config is being read or cannot be read, and points to the importers.
- Connect…: a pasted `ssh -p 2222 user@host` is read (only -p and -l); a screen reader hears each connection's state, the reason a connection failed and how many results the text leaves.
- Ctrl+Shift+E now also finds a connection by its host or user and connects to a typed `user@host`; the sidebar has a "＋ Connect…" row and "New connection in this group…"; the short Save connection sheet can create a new group.
- SSH: Quick connect and new profiles now refuse user and host names with shell characters (`$ ; | \` & ...`); saved profiles keep opening.
- SSH: a login with an @ can be the user (like name@company.com, from Entra ID or Active Directory): in the profile sheet and group defaults, in Connect… (name@company.com@host) and in Copy ssh command.
- SSH: Hosts in importers and `~/.ssh/config` must be ASCII or punycode (`xn--`); a `~/.ssh/config` on a network drive is not read (see Diagnostics).
- SSH: the app now asks the server for UTF-8 (LC_CTYPE=C.UTF-8), so accents and symbols show right. Older servers (RHEL/CentOS 7, Amazon Linux 2, SLES 12) may print a locale warning at every login: turn off Settings › SSH › Ask the server for UTF-8 and nothing is sent, as in 0.2.1.
- ZMODEM: cancelling a download no longer shows any of the file in the terminal, even on a slow connection or if you type meanwhile. The server's prompt may go missing with it (a blank line shows instead); press Enter to get it back.
- ZMODEM: if the server's rz stops in the middle of an upload, the pane says so instead of going silent, and the rest of the file is kept from running in the server's shell. Press Enter to get the prompt back; if the shell stays busy, reconnect.
- ZMODEM: uploads now escape every control byte and keep at most 64 KiB in flight, so binary files send about 20% more data and uploads to distant servers are slower (about 0.5 MB/s with 100 ms of latency).
- The AI card shows each answer's cost in US$ and how much of the day's limit is used.
- Optional daily AI limit in US$, a warning at 80% of the limit, and the last 30 days in Settings › AI.
- AI token counts are written the same way everywhere: the review says ≈ 3,200 tokens, no longer ≈ 3.2k.
- Panes: Ctrl+Shift+Enter zooms a pane and Alt+Shift+arrows move the divider, in a split tab. Balance panes and Rotate split are in the terminal menu and the palette, and a zoomed tab says how many panes are hidden.
- In a split tab, Alt+Shift+arrows now belong to Shell'Naga (Emacs org-mode and micro lose those keys there). To get them back, set "alt+shift+up", "alt+shift+down", "alt+shift+left" and "alt+shift+right" to "none" under [keybindings] in config.toml.
- Restore tab contents: closing the app no longer waits for the tab contents to be saved, and a pane whose saved contents were not shown keeps them and this run's output together at the next start.
- Vault: Restore the .bak copy no longer replaces the vault while it is being unlocked or its protection is being changed, and a profile's Save that waited for the vault no longer saves changes made after it was pressed: press Save again.
- Vault: Delete vault no longer deletes a vault that changed after the question.
- A frame that fails to draw is drawn once more right away instead of waiting for the next key or mouse move.
- Deleting a group now moves its layouts and serial and Telnet profiles into the parent group, like its other profiles, instead of to the top.
- If the new version can't start after an update, the previous one is put back and the app stays open.
- Closing the last window while an update is being installed no longer interrupts it: Shell'Naga finishes, or puts the previous version back, before it exits.
- Other stability fixes.

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
