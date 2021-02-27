---
title: "Avoid Learning Bad Typing Habits Formed From Vim"
author: Kevin Nel
last_modified_at: 2020-10-10
categories: [tech]
---

Recently Ive been trying to teach myself touch typing and a really bad habit that I have formed has been brought to light.
When I first learned vim I couldn't really touch type and and I developed the habit of placing my right index finger on ``h`` instead of ``j``.
I thought that I would make this post to encourage new users of vim to not learn this habit.
Rather place your fingers as you would for touch typing and then move your right index from ``j`` to ``h`` when it is needed.

You don't typically move left and right a character nearly as often as you move up and down (at least for programming, writing may be a different situation) so it's actually a bit more helpful to have your index on ``j`` and middle finger on ``k``.

### some tips for left/right movement

- when moving to the left/right it is most often more helpful to use ``b``/``w`` to travel by words.
- use ``f``/``t`` commands to move to cursor to the location of a specific character on a line, [this stack overflow answer explains it well](https://stackoverflow.com/questions/12495442/what-do-the-f-and-t-commands-do-in-vim)
- use ``shift`` + ``a`` to go to the end of the line and change to insert mode (the mnemonic I use to remember this is *Append*)
- use ``shift`` + ``i`` to go to the beginning of the line and change to insert mode (the mnemonic I use to remember this is *Insert*)
