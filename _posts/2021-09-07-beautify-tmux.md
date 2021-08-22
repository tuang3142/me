---
layout: post
title: Beautify your tmux
date: 2021-09-07 20:19 +0700
tag: tmux
---

### WHY

- Make the tmux experience more enjoyable, therefore more encouraging
- Why not? It is as easy to do as changing vim colorscheme
- And let's be honest, you spend hours to find the perfect theme and the dankest font for your
vim, but you leave your tmux as it is cuz you dont know how.

### HOW

#### Pre-built theme

- Download & install [tmux plugin manager](https://github.cbm/tmux-plugins/tpm)

```
$ git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

put this at the END of your `tmux.conf`, then reload config (`prefix + I`)

```
# List of plugins
set -g @plugin 'tmux-plugins/tpm'

# Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
run '~/.tmux/plugins/tpm/tpm'
```

- Add a theme (my personal favorites are `nord` and `gruvbox`), then `prefix + I`

```
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin "arcticicestudio/nord-tmux"
# set -g @plugin 'egel/tmux-gruvbox'
# set -g @tmux-gruvbox 'dark'

run '~/.tmux/plugins/tpm/tpm'
```

#### Using tmuxline

Add the plug-in to your vimrc: [tmuxline.vim](https://github.com/edkolev/tmuxline.vim). Also don't forget to give the author some love and star.
Follow the instruction to create your own color scheme base on your statusline (lightline, airline, tabline, etc.). Alternatively, you can copy my color configuration:

```
# scheme: gruvbox
set -g status-justify "left"
set -g status "on"
set -g status-left-style "none"
set -g message-command-style "fg=#1d2021,bg=#7c6f64"
set -g status-right-style "none"
set -g pane-active-border-style "fg=#fe8019"
set -g status-style "none,bg=#3c3836"
set -g message-style "fg=#1d2021,bg=#7c6f64"
set -g pane-border-style "fg=#7c6f64"
set -g status-right-length "100"
set -g status-left-length "100"
setw -g window-status-activity-style "none"
setw -g window-status-separator ""
setw -g window-status-style "none,fg=#a89984,bg=#3c3836"
set -g status-left "#[fg=#1d2021,bg=#fe8019,bold] #S #[fg=#fe8019,bg=#3c3836,nobold,nounderscore,noitalics]"
set -g status-right "#[fg=#7c6f64,bg=#3c3836,nobold,nounderscore,noitalics]#[fg=#1d2021,bg=#7c6f64] %Y-%m-%d  %H:%M #[fg=#fe8019,bg=#7c6f64,nobold,nounderscore,noitalics]#[fg=#1d2021,bg=#fe8019] #h "
setw -g window-status-format "#[fg=#a89984,bg=#3c3836] #I #[fg=#a89984,bg=#3c3836] #W#{?window_zoomed_flag,>=,} "
setw -g window-status-current-format "#[fg=#3c3836,bg=#7c6f64,nobold,nounderscore,noitalics]#[fg=#1d2021,bg=#7c6f64] #I #[fg=#1d2021,bg=#7c6f64] #W#{?window_zoomed_flag,>=,} #[fg=#7c6f64,bg=#3c3836,nobold,nounderscore,noitalics]"
```

It takes some time to configure, but the effect is nevertherless satisfying.

![tmux_gruvbox](/assets/images/gruvbox.png)

### Further reading

- https://www.nordtheme.com/ports/tmux
- https://github.com/egel/tmux-gruvbox
