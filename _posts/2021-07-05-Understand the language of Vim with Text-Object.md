---
layout: post
title: "Some articles are just so short that we have to make the footer stick"
categories: vim
---

# Understand the language of Vim with Text-Object

# why

Say the cursor is in the middle of a word and we want to delete it. We can either:
- type `bde` (go to the beginning then delete) like a peasant
- or use `diw` (delete inside a word) like an absolute chad.

# how

`diw` is the combination of vim command `d` and text object `ir` (inside a word).  
some ruby relevant text objects are:

when combining with vim command `d`, `c`, or `y`, we have the powerful vim language.  
for examples:
- `dim`: delete inside method
- `ci'`: change inside single quote
- `yi]`: yank inside square bracket  
- `cit`: delete inside html tag  
(change i to a and we have around method, around single quote, etc.)

try doing the above examples the normal way to appreciate how bad-ass and efficient text objects are.

a few more reasons/benefits to use text objects:
- easy to remember and apply because they feel as nature as the human language.
- repeatable with the dot '.' command.
- the potential is limitless when we can define our own text object. this guys wrote a [plugin](https://github.com/nelstrom/vim-textobj-rubyblock) for ruby block which can be selected as `ir`/`ar` (which, you guess it, means `inside ruby block ` / `around ruby block`).


# conclude

I am neither the creator nor a master convincer but merely a vim enthusiastic. Just try these tips for a few days to see if they really improve your productivity as they did to me.
