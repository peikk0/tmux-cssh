# tmux-cssh

Spawns multiple synchronized SSH sessions inside a tmux session.

Think [Cluster SSH](https://github.com/duncs/clusterssh) except with only one terminal window and without the ugly Tk GUI.

# Requirements

- [tmux](https://tmux.github.io/) >=1.1

# Installation

Just copy `tmux-cssh` somewhere in your `$PATH`.

You might want to add a keybinding in your `.tmux.conf` for toggling panes synchronization:
```
bind-key = set-window-option synchronize-panes
```

# Usage

```
% tmux-cssh -h
Usage: tmux-cssh [options] host [host ...]

Spawns multiple synchronized SSH sessions inside a tmux session.

Options:
  -h                  Show help
  -n <name>           Name of the tmux session (default: cssh)
  -o <ssh args>       Additional SSH arguments

% tmux-cssh web{1..4}

% tmux-cssh -o '-p 2222 -l my_user' web{1..4}
```

# License

[MIT](LICENSE.md)

Handmade with love in Wellington, New Zealand.
