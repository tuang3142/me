---
layout: post
title: "Understand the language of Vim with text object"
tags: vim
---

## WHY

Say the cursor is in the middle of a word and we want to delete it. We can either:
- type `bde` (go to the beginning then delete) like a peasant
- or use `diw` (delete inside a word) like an absolute chad.

## HOW

`diw` is the combination of Vim command `d` and the text object `ir`.
It can be roughly translated as `delete inside word`.
Commonly, text objects start with `i` or `r` which stands for `inside` or `around` respectively.
Some relevant text objects are:

|text object| meaning|
--- | ---
|`iw`|inside word|
|`aw`|around word|
|`im`|inside method|
|`am`|around method|
|`i]`|inside square bracket ] |
|`a]`|round square bracket ] |
|`it`|inside html tag|
|`at`|around html tag|

When combining with Vim command `d`, `c`, or `y`, we have the powerful Vim language. For examples:
- `dim` delete inside method
- `ci'` change inside single quote
- `yi]` yank inside square bracket
- `cit` change inside html tag


Try doing the above examples the normal way to appreciate how bad-ass and efficient text objects are
(change i to a and we have around method, around single quote, etc.).  
To practice, I found this [free course](https://thoughtbot.com/upcase/navigating-ruby-files-with-vim) from thoughtbot really
helpful.

## But seriously, WHY?

A few reasons to use text objects:
- easy to remember and apply because they feel really close to  the human language.
- repeatable with the dot `.` command.
- we can define our own text object.
There is a [plugin](https://github.com/nelstrom/Vim-textobj-rubyblock) for Ruby block to be
selected as text objects with `ir`/`ar` (which, you guess it, means `inside ruby block `/`around ruby block`).


## Conclusion

Just try these tips for a few days to see if they really improve your productivity as they did to me.
You've got to get your hand dirty to appreciate the beauty of the Vim language (or Vim in general).
