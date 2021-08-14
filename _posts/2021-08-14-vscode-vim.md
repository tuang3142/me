---
layout: post
title: "Transition from VSCode to Vim"
tags: vim hjkl

---

## Why

VSCode is a good editor. However, since the day I switched to Vim, I would never go back. Vim's design philosophy and the extendability in terms of key mapping are far more superior. I wouldn't think my keyboard would be this efficient with any other editors (my eyes are kept open for Emacs tho). With that being said, and if you're a VSCode user feeling adventurous, this post would help you get into Vim somewhat smoothly and cope with its notorious learning curve.

## How
### vimtutor

`vimtutor` is an interactive tutorial that comes with Vim. It has all the basic lessons for you to use Vim right away: jumping around, exiting Vim (every JS programmers' worst nightmare), Vim modes, etc. It only takes around 15 mins to finish the tutorial, so consider it as a warm-up exercise. I recommend participating with it once a day for a week then tries writing stuff in Vim before sending it anywhere.

### VSCodeVim

[VSCodeVim](https://marketplace.visualstudio.com/items?itemName=VSCodeVim.Vim) is a Vim emulator for VSCode. It helps you maintain your long-time customized, feature-rich extensions while only apply Vim in what matters: editing. You can still use your mouse once in a while at this stage

### vanila Vim

It is recommended to first use Vim naked, that is without any plugins (synonym with VSCode extensions), but you should learn to do some basic settings to make it fit your eye's tolerance (let's be honest, Vim vanilla is ugly af). The config files for Vim is `Vimrc`, usually located at `~/.Vimrc`, `~/config/.Vimrc`, or `~/.Vim/Vimrc`. Find it and type in some code following this [totorial](https://dougblack.io/words/a-good-Vimrc.html). For starter, I only would configure the following:

- Add a color scheme (gruvbox, tomorrow, and jellybeans are my favorites)
- Turn on syntax highlighting
- Set up spaces and tabs
- Set up auto-indentation
- Turn on line numbers

to get me coding comfortably without using my mouse.

### the Vim language

Looking back, this was the defining moment when I felt my-blown, leveled up, awaken, whatever you call it. I [wrote]({% post_url 2021-07-05-vim-text-object %}) about this topic separately and [this](https://youtu.be/wlR5gYd6um0) is a great video to get you started. Mastering the Vim language is an essential part to help you appreciate the beauty of Vim.

## Moving forward

At this point, you should feel all those years of coding with VSCode are completely wasted. Vim is a vast mystical land that requires years to explore and be truly efficient. I would recommend the following topic for your question: "Where to go next?" but you are now on your own journey:

- plugins
- marcos
- Vim on Tmux (the final knot that put VSCode into scramble)
- vimscript (yes it is a language)

Happy hjkl!
