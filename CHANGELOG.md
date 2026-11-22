# Changelog

All notable changes to Shell'Naga, newest first. Downloads and checksums: [Releases](https://github.com/shellnaga/shellnaga/releases) or <https://shellnaga.sh/#download>.

## 0.2.8 — 2026-11-21

- What's new also shows the notes of the versions you skipped when you update from 0.2.6 or earlier.

## 0.2.7 — 2026-11-21

- Tabs: Settings › Window › Tabs › Style chooses the look of the tab bar: Mac, the rounded bar with the tabs inside, as before; or Windows, tabs with rounded tops up in the title bar, the active one joined to the terminal, as in Windows Terminal.
- Tabs: the × that closes a tab is two thin strokes, quiet until the pointer is on it.
- Tabs: the title of a tab under the pointer is easier to read in the light theme.
- Tabs: in the light theme, the ring around the active tab of the Mac style is easier to see.
- Ctrl+Shift+B shows the profile sidebar faster, and the sidebar now slides open and shut.
- What's new after an update shows the notes of every version you skipped, newest first, each under its version.
- Statistics: at All statistics, the daily count also says, in ranges, on how many of the 7 days before you opened the app, how much memory the PC has and who makes its graphics card (never the model); the days of use stay on your PC and go away when you turn the statistics off. Errors only and Off send none of it.

## 0.2.6 — 2026-11-21

- The terminal is no longer announced as "read only", so NVDA speaks the letters and words you type, as it does in Windows Terminal.

## 0.2.5 — 2026-11-21

- SSH: the passphrase of an encrypted key is asked only after the server accepts that key; a key the server refuses asks nothing, and the login goes on to the next way in (the saved password, for example). An old PEM key with no .pub beside it still asks first, as in OpenSSH.
- The passphrase sheet says it unlocks the key file on this computer and is not the server's password; "Skip this key" (or Esc) goes on to the next way in, a passphrase you chose to save goes to the vault only once the key has logged in, and the question closes by itself if the connection drops.
- Hosts of ~/.ssh/config can be edited: Edit… (Settings › Profiles, F2 in the sidebar, Ctrl+E in Connect…) opens the SSH sheet filled with the host, and saving makes a profile in profiles.toml in its place, with the host's saved password, favorite and recent entry; ~/.ssh/config is never changed.
- A profile's color (or its group's) now colors the tabs it opens and its initials in the narrow sidebar; a color picked from the tab's menu still comes first.
- The sidebar has a + beside its search with New SSH connection…, New profile… and Connect…; a destination typed in the search (user@host, host:port, ssh://…) puts "Connect to …" on top, and Enter connects.
- The sidebar's footer shows its keys as keycaps in two aligned columns: Enter open, Ctrl+Enter split, F2 edit, Ctrl+. pin, with the pin key as your keyboard layout types it.
- A double click on a profile in the sidebar opens one tab and the list stays still under the pointer; after Ctrl+Shift+B, what you type goes to the sidebar's search, never to the shell.
- Each window has its own sidebar: Ctrl+Shift+B shows or hides it in that window only, and the setting is how the next window opens.
- Favorites can be put in order with Alt+↑ and Alt+↓, Move up and Move down in the row's menu, or by dragging; the menu also has Pin to Favorites and Unpin from Favorites.
- In "Open now", a tab whose profile was deleted only goes to its tab, its other buttons dimmed with the reason in the tooltip; a deleted profile also leaves Favorites and the recent list.
- In the sidebar's search, the first Esc clears it and the second goes back to the terminal, "No profile matches" says when nothing is found, and screen readers stay in the field while you type and hear how many results there are.
- Ctrl+Shift+B (profile sidebar), Ctrl+Shift+L (save output) and Ctrl+Shift+/ (keyboard shortcuts) are the window's, so a program in the terminal does not get them; if you need one there (a tmux prefix typed with Shift held), give it back with "none" in Settings › Key bindings.
- Focus rings show only when you use the keyboard: a click hides them in that window until the next key, a text field keeps its ring, and moving with a screen reader shows them again.
- Checkboxes have a smooth check mark and an outline that stays visible in every color scheme and at every display scale.
- Agent usage: the panel is now a card with the context as a meter, the 5-hour and 7-day quotas and when they reset (or Connect to Claude Code), the session's estimated cost at API prices and how long it has run, and today's tokens of each agent; Esc or a click outside closes it.
- The agent chip shows the context ("claude · ctx 26%") and its dot says working (green) or idle (grey); the click that brings the window back, or one on the chip of a tab behind, only selects the tab instead of opening the panel.
- Agent usage history (Open history on the card, the command palette or Settings › Agent usage) opens a tab with this computer's usage: tokens, estimated cost, sessions and active hours against the period before, by day, project, model, kind of token and hour of the week, each session in detail, and Export CSV. It reads only the session files on this computer, and nothing leaves it.
- Importing from MobaXterm 26.6 brings its serial sessions with their port and speed (they were skipped as "invalid port"); data bits, parity and flow control stay at 8N1 without flow control.
- Screen readers say the window and the terminal when you come back with Alt+Tab, switch tabs, or split or close a pane, also in a window that opened behind another.
- An SSH key file that exists but cannot be read is named in the login error with the reason ("access denied"), and the login goes on to the next way in.
- A profile in profiles.toml with an invalid id shows a warning on Settings › Profiles instead of disappearing silently; the other profiles still load.
- Tab titles show a composed emoji (a family, a skin tone) as one, cut it whole when the title is too long, and show Hebrew or Arabic in reading order; so do the sidebar's names.

## 0.2.4 — 2026-11-20

- The profile sidebar has a search field on top: type to filter by name, user, host or group, with the part found in bold; ↑ ↓ move, Enter opens, Ctrl+Enter opens in a pane to the right, F2 edits.
- Ctrl+Shift+B now puts the keyboard in the sidebar's search, opening the sidebar if it is closed, and closes it when the keyboard is already there; Esc goes back to the terminal and leaves the sidebar open.
- "Open now", at the top of the sidebar, lists the profiles that have a tab in this window: a connection with a green dot (connected) or a red one (dropped) and for how long, a local shell with a grey one; Enter there goes to the open tab instead of opening another.
- Ctrl+. in the sidebar pins a profile to "Favorites ★", under the open tabs, or takes it off (a ★ marks it in its group too); the sidebar also remembers which groups were folded.
- The sidebar's row under the pointer, or selected, has buttons to open in a new tab, open in a pane to the right and edit, each with its key in the tooltip; the keys are also in the sidebar's footer.
- The right-click menu of a connection in the sidebar has "Copy ssh command", as in Connect….
- Drag the sidebar's edge to change its width; below 120 px it becomes a narrow column of initials with the state dot, the full name in the tooltip and for screen readers.
- Screen readers find the sidebar's search and its rows, with each connection's state in words.
- New shortcuts: Ctrl+Shift+S opens or closes the SFTP panel (SSH tabs only; elsewhere the key goes to the program), Ctrl+Shift+L starts or stops saving the output, Ctrl+Alt+Shift+B turns broadcasting to all panes on or off. With Tabby's shortcuts imported, Ctrl+Shift+S stays split right, and any of them can be given back with "none" in Settings › Key bindings.
- Ctrl+Shift+/ opens "Keyboard shortcuts": every shortcut in use, yours included, by area, with a search; the same key closes it.
- The key that opens a panel or sheet also closes it (Ctrl+Shift+L with the Save output sheet, the palettes), and the keys of symbols are shown as your keyboard layout types them.
- The terminal menu shows the keys of Open SFTP, Save output to file and the broadcasts.
- Agent usage (Settings › Agent usage, off by default): a tab running Claude Code or Codex shows a chip with the 5-hour quota (or the context), and a click on it or Ctrl+Shift+M opens a panel with the context, the 5-hour and 7-day quotas, a warning when a quota runs out at the current pace before it resets, the session's estimated cost and today's tokens of each agent. A bar at the bottom of the window with the whole line is an option.
- Agent usage reads the session files of Claude Code and Codex on this computer only: numbers, model, time and folder, never the conversation, and nothing leaves the computer. A file in a form the app does not know hides the numbers instead of showing wrong ones.
- Agent usage: Claude Code tells its quotas only to its status line. "Connect to Claude Code…" adds Shell'Naga's command beside your status line in ~/.claude/settings.json, after showing it; your line stays the same and keeps working even if Shell'Naga is removed, a copy of the file is kept, and "Disconnect…" puts it back. On Windows without Git Bash (PowerShell) it connects only when you have no status line of your own. Codex's quotas need nothing.
- The installer opens on one screen with the brand: "Install for me" (no administrator rights) or "Options…" for all users, the PATH and the shortcuts; at the end, "Launch Shell'Naga".
- When Shell'Naga is already installed for all users, the installer offers "Update for all users" first, instead of a second copy for you.
- "Launch Shell'Naga" at the end of the installer opens the first tab in your user folder, not in C:\Windows\system32.
- From the update after 0.2.4 on, updating from the app shows Shell'Naga's splash screen where the window was until the new version opens, instead of the Windows Installer box (an install for all users still asks for administrator rights).
- The Roll back option is gone; a failed update still restores the previous version by itself.

## 0.2.3 — 2026-11-20

- Ctrl+Shift+B now shows or hides the profile sidebar, and a button for it sits at the end of the tab bar; to give the key back to a program (nvim, helix), set `"ctrl+shift+b" = "none"` in Settings › Key bindings.
- The ~/.ssh/config section is now called "SSH config" in Connect…, the sidebar and Settings › Profiles, with the path beside it.
- Settings: an option that has a key of its own shows it beside its name (Profiles sidebar, Ctrl+Shift+B) and follows Key bindings when you change it.
- The broadcast indicator no longer disappears in a narrow window: with no room left it becomes a small ● mark that shows the full text when you point at it.
- Screen readers (Narrator, NVDA) now find the buttons of the tab bar and the title bar (New tab, Profiles, Settings, the sidebar button, Minimize, Maximize, Close) in a "Window controls" group, each named with its key, and can press them.
- Snippets from a plugin or the synced folder that are not yet confirmed here are typed only while the pane's shell waits at its prompt, checked when you are asked and again when you confirm, and never go to the other panes by broadcast.
- When a program keeps a snippet from outside out, the message names it ("pwsh runs in this pane…"); on Windows any program the shell started counts, a Start-Job too.
- MCP: when a client asks to type, the question names the program in front of the shell ("python3 is running in front of the shell."), and Type checks the pane again: if the shell or that program changed, nothing is typed and the client gets an error.
- SFTP: the progress bars and the state of transfers can now be read in every color scheme.
- The splash screen's loading bar is blue again.
- Updating is faster: Windows no longer creates a restore point for each update.
- Tabs opened with `--profile` or from the jump list no longer say "restored": they show "[SSH session · Enter to connect]" (or the serial, Telnet or raw socket version) and wait for Enter; only a session brought back from the last run says "restored".
- Correction to the 0.2.2 notes: in Connect…, “Save this connection” is on for a destination typed in the box and off when the destination comes from a link or `--quick-connect`.

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
