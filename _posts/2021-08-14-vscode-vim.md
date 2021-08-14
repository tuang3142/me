---
layout: post
title: "Transition from VSCode to Vim"
tags: vim hjkl

---

## Why

VSCode is a good editor. However, since the day I switched to Vim, I would never go back. Vim's design philosophy and the extendability in terms of key mapping are far more superior. I wouldn't think my keyboard could be this efficient with any other editors (my eyes are kept open for Emacs tho). With that being said, and if you're a VSCode user feeling adventurous, this post would help you get into Vim somewhat smoothly and cope with its notorious learning curve.

## How

### vimtutor

`vimtutor` is an interactive tutorial that comes with Vim. It has all the basic lessons for you to use Vim right away: jumping around, exiting Vim (every JS programmers' worst nightmare), Vim modes, etc. It only takes around 15 mins to finish the tutorial, so consider it as a warm-up exercise. I recommend playing with it once a day for a week then try writing stuff in Vim before sending anywhere.

### VSCodeVim

[VSCodeVim](https://marketplace.visualstudio.com/items?itemName=VSCodeVim.Vim) is a Vim emulator for VSCode. It helps you keep using your long-time customized, feature-rich extensions while only apply Vim in what matters: editing. You can still use your mouse once in a while at this stage, but ultimately the goal is to get rid of it (and VSCode) completely.

### vanila Vim

It is recommended to first use Vim naked, that is without any plugins (synonym with VSCode extensions), but you should do some basic settings to make it fit your eye's tolerance (let's be honest, the creators of Vim didn't think of user experience AT ALL). The config files for Vim is usually `~/.vimrc`, `~/config/.vimrc`, or `~/.vim/vimrc`. Find it and type in some code following this [tutorial](https://dougblack.io/words/a-good-Vimrc.html). For starter, I only would configure:

- Color scheme (gruvbox, base16, and jellybeans are my favorites)
- Syntax highlighting
- Set up spaces and tabs
- Set up auto-indentation
- Turn on line numbers

to get me coding comfortably.

### the Vim language

Looking back, this was the defining moment when I felt my-blown, leveled up, awaken, whatever you call it. I [wrote]({% post_url 2021-07-05-vim-text-object %}) about this topic separately and [this](https://youtu.be/wlR5gYd6um0) is a great video to get you start. Mastering the Vim language is an essential part to appreciate the beauty of Vim.

## Moving forward

At this point, you should feel all those years of using VSCode were completely wasted. Now you're on your own journey into the vast and mystical land of Vim. The road is long and hard but full of exitement. I would recommend the following topics for your question: "Where should I go next?":

- plugins
- marcos
- Vim on Tmux (the final knot that put VSCode into shame)
- vimscript (yes it is a language)

Happy hjkl!
