---
title: Vim
---

This page contains a bunch of vim related stuff.

Here is an article I wrote about my mistake when first learning vim:  [Don't get bad typing habits](/blog/completed/2020-10-10-touch-typing-and-vim.md)

## cool vim things i like to use

- ``gf`` to go to open file under cursor and ``C-O`` to return back to last open file
- ``g;`` to go to the line where you last made an edit
- ``ci(`` to change the text inside the parenthesis that the cursor is within (also works for other bracket types as well as closing brackets ``{,},[,],)``)
- ``f`` and ``t`` to move the cursor to next occurrence of a character on the current line (capital ``F`` and ``T`` move to previous)
- ``V`` to select the current line
- searching for a word with ``/`` and then using ``n`` to go to next occurrence and ``N`` to go to previous occurrence
- scrolling by a full page with forward (``<c-f>``) back (``<c-b>``)
- centering line at cursor in the view with ``zz``
- I also like to use vim substitutions using the ``:s`` command.

## plugins i use

I currently use [vim-plug](https://github.com/junegunn/vim-plug) to manage plugins but I do want to give the native vim8 plugin manager a try.
Plugins:

- [goyo](https://github.com/junegunn/goyo.vim) is a "zen mode" plugin that centers the content and removes extra ui elements. I like to use it when I am taking notes or writing in english but not really for writing code
- [vim-easy-align](https://github.com/junegunn/vim-easy-align), I only use this to format markdown tables.
- [vim-polyglot](https://github.com/sheerun/vim-polyglot) improves the syntax highlighting for a lot of languages.
- [VimCompletesMe](https://github.com/ackyshake/VimCompletesMe) sets up tab completion using native vim completion like omnicomplete based on the context.

Themes:

- [vim dim](https://github.com/jeffkreeftmeijer/vim-dim) uses ansi color codes so that vim uses your terminal colors.

## useful stuff in my vimrc

Below is some of the stuff that took me some time to figure out.
I have left out the simpler stuff like displaying whitespace, setting up clipboard and mouse, and my autocmds and macros.

### remove trailing whitespaces on save

```vim
autocmd BufWritePre *.py :%s/\s\+$//e
```

[source](https://vim.fandom.com/wiki/Remove_unwanted_spaces)

### nicer shortcuts to switch between splits

```vim
" swithing panes
nnoremap <c-j> <c-w>j
nnoremap <c-k> <c-w>k
nnoremap <c-h> <c-w>h
nnoremap <c-l> <c-w>l
```

### save markdown files on insert leave

You can use this for any file type but i only want it to happen for markdown.

```vim
autocmd InsertLeave *.md silent! execute ":w"
```

### spellchecking for text documents

You can navigate to the next, ``]s`` and previous ``[s`` spelling mistake in normal mode and then bring up a list of corrections with ``z=`` when your cursor is over the word.
I also remove the highlighting and opted to make the errors bold and underlined to be slightly less obnoxious

```vim
autocmd filetype markdown,tex,latex,groff set spell
hi clear SpellBad
hi SpellBad cterm=underline,bold
```

### my own vim statusline

I didn't want to use a plugin for my status line but wanted a few more things added.

```vim
"statusline
set laststatus=2
set statusline=
set statusline+=%#PmenuSel#
set statusline+=%#LineNr#
set statusline+=\ %f
set statusline+=%m
set statusline+=%=
set statusline+=%#LineNr#
set statusline+=\ %y
set statusline+=\ %{&fileencoding?&fileencoding:&encoding}
set statusline+=\[%{&fileformat}\]
set statusline+=\ %p%%
set statusline+=\ %l:%c
```

### type emojis and unicode characters with digraphs

Using ``<Ctr>+k`` in insert mode will allow you to insert unicode characters using two character shorthand.
You can see all the digraphs by entering ``:digraphs`` or ``:help digraph-table`` in normal mode

Some installs of vim contain some emojis by default but my vim install did not have emojis so I added the following to my ``.vimrc``.

> note: when you search online for [emoji codes](https://unicode.org/emoji/charts/full-emoji-list.html) the codes are given in hexadecimal (base 16) and vim wants them in decimal (base 10). You can use [an online tool](https://www.binaryhexconverter.com/hex-to-decimal-converter) to convert hex to dec.

```vim
dig <3 129293 " 🤍
dig :) 128578 " 🙂
dig :( 128577 " 🙁
dig ;) 128521 " 😉
dig :P 128523 " 😋
dig xD 128514 " 😂
dig B) 128526 " 😎
dig :/ 128528 " 😐
dig (: 128579 " 🙃
dig 3) 128522 " 😊
dig 3( 128532 " 😔
dig :L 128530 " 😒
dig ;P 128540 " 😜
dig >: 128545 " 😡
dig :; 128546 " 😢
dig :< 128548 " 😤
dig :I 128556 " 😬
dig := 128557 " 😭
dig :o 128558 " 😮
dig :O 128561 " 😱
dig 8/ 128563 " 😳
dig z: 128564 " 😴
dig xo 128565 " 😵
dig </ 128580 " 🙄
dig hn 128588 " 🙌
dig tx 128591 " 🙏
dig ok 128076 " 👌
dig mm 129292 " 🤌
```

> note: you could also use abbreviations with ``ab`` if you want vim to always replace that text in insert mode and don't want to enter a new mode.

[source](https://lual.dev/blog/how-to-use-emojis-with-vim/)

## useful links

- [nvm language server](https://github.com/neovim/nvim-lspconfig)
- [collection of good vim plugins](https://www.vi-improved.org/plugins/)
- [some funny](https://blog.samwhited.com/2015/04/the-dharma-of-vi/) [vim koans](https://blog.sanctum.geek.nz/vim-koans/) on the 'zen' of vim.[^1]
- [using the native vim8 package manager](https://shapeshed.com/vim-packages/)

[^1]: [What is a koan?](https://en.wikipedia.org/wiki/Koan)
