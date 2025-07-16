---
type: zettel
---

```meta-bind-button
label: Set next review
hidden: false
id: review
style: primary
actions:
  - type: command
    command: review-obsidian:future-review
  - type: input
    str: "next 7 days"
```

# Tmux

- Install
	- `dnf install tmux`
	- `Ctrl+b ?` - list all shortcuts
	- `Ctrl+b :` - command mode
	- Session > Window > Panel
- Session
	- `tmux ls` - list current sessions
	- `Ctrl+b s` - list sessions with a preview
	- `Ctrl+b $` - change session name
	- `Ctrl+b (` - previous session
	- `Ctrl+b (` - next session
	- `Ctrl+b D` - detach, session remains active after you logout
	- `tmux a -t <id>|<name>` - attach to a session
- Panel
	- `Ctrl+b "` - horizontal split
	- `Ctrl+b %` - vertical split
	- `Ctrl+b arrows` - move between panels
	- `Ctrl+b x` - delete panel
	- `Ctrl+b q` - display panel indexes
	- `Ctrl+b q <id>` - move to panel with specified IDID
	- `Ctrl+b !` - convert panel into window
	- `Ctrl+b z` - temporary panel zoom
- Window
	- `Ctrl+b c` - new window
	- `Ctrl+b n` - next window
	- `Ctrl+b p` - previous window
	- `Ctrl+b <id>` - move to window with specified ID
	- `Ctrl+b &` - delete window (IDs remain unchanged)
	- `Ctrl+b ,` - change window name
	- `Ctrl+b w` - list windows and panels
- Config
	- `~/.tmux.conf`
