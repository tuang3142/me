---
layout: post
title: "Good design get things done faster"
tags: ["ruby on rails", "design", "vim"]
---

## WHAT

I recently learn software design by reading the book [Practical Object-Oriented Design in Ruby](https://www.poodr.com).
It's a good read. I find the first two chapters (which can be summed up as "Designing classes with single
responsibility") helpful to my work. However, I still find my development slow.
I recently implement a feature: show user's portfolio in email. It sounds easy on paper, but it still took me 2-3 days more than I intended.

## WHY

In retrospect, I wrote too much. To be precise, I rewrote too often. Usually, I found myself deleting the whole class
as I tried to apply the principle I just learned. By doing so, I had to refactor the tests as well.
Had I came up with a good design first, I would have rewritten less, thus completed the task faster.

I also created a pretty fat PR (around 500 LOC). It made the reviewing process take longer and it was harder to see code change in a large PR. Small factors like this might slow down the feedback loop.

## HOW (to get things done faster)?

- Gentlemen! Pens and papers are your friends. Draw your design first before click-clacking. Spending some time afk is good for your wrist too.

- Keep a PR around 200 LOC. Split a large PR into smaller ones.

- I'm going to try a syntax that wraps a logic block into a function which is a pretty common Ruby practice (credit goes to [Ben Orenstein](https://github.com/r00k)).

## Closing thoughts

This might only apply to my situation, but to generalize some tips, I'd say: draw your design first, then keep your head down below 200 LOC.
