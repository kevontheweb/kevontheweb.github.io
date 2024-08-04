---
title: Vim
author: {{site.author}}
last_modified_at: 2023-07-16
categories: [tech]
---

This page contains a bunch of vim related stuff.

## cool vim things i like to use

- ``gf`` to go to open file under cursor and ``C-O`` to return back to last open file
- ``g;`` to go to the line where you last made an edit
- ``ci(`` to change the text inside the parenthesis that the cursor is within (also works for other bracket types as well as closing brackets `{`,`}`,`[`,`]`,`)`, quotations `"`,`'`). `ca(` will change *around* the brackets also deleting the brackets.
- ``f`` and ``t`` to move the cursor to next occurrence of a character on the current line (capital ``F`` and ``T`` move to previous). You can repeat this movement by using `;` to repeat forward and `,` to repeat backwards.
- ``V`` to select the current line
- searching for a word with ``/`` and then using ``n`` to go to next occurrence and ``N`` to go to previous occurrence
- scrolling by a full page with forward (``<c-f>``) back (``<c-b>``)
- centering line at cursor in the view with ``zz``
- I also like to use vim substitutions using the ``:s`` command.
- ``gx`` to open the file under curse with system default application, **this also works for URLS**
- ``K`` to open information from diagnostics and documentation for the word under the cursor.

## plugins i use

> note: my config is often changing, you can see what I've got going on at [my configs repo](https://github.com/kevin-nel/linux-configs)

I currently use [lazy.nvim](https://github.com/folke/lazy.nvim) to manage plugins.

Plugins:

- [which key](https://github.com/folke/which-key.nvim) shows a nice popup with commands available after you type the first letter of a command. I love this because I often forget custom bindings and this helps me to remember they exist and even learn about some new ones.
Themes:
- [gitsigns](https://github.com/lewis6991/gitsigns.nvim) this shows some git information in the gutter. I usually just use regular `git` commands on the cli or vscode for diffs of bigger changes.
- [codeium](https://github.com/Exafunction/codeium.vim), Whether I like it or not AI is coming and it's at the very least trying to make our jobs easier. I've found this free alternative to co-pilot works quite well. But I often have it disabled as it slows down the editor and I also like to not have so much help when learning.
- [Telescope](https://github.com/nvim-telescope/telescope.nvim) this is just an all round super useful plugin. It basically adds a command pallette style interface to neovim and lots of other third party plugins support it as well. It's great for fuzzy finding, jumping to symbols and easy control of other neovim parameters.
- [lualine](https://github.com/nvim-lualine/lualine.nvim), it's a statusline that requires minimal setup.

Themes:

- [tokyo night](https://github.com/folke/tokyonight.nvim)

### LSP stuff

I used [kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim) as a jumping off point for my LSP setup so I am using [nvim-cmp](https://github.com/hrsh7th/nvim-cmp) for completions, [nvim-lspconfig](https://github.com/neovim/nvim-lspconfig) and [mason](https://github.com/williamboman/mason.nvim) for lsp configuration.
I also use [null-ls](https://github.com/jose-elias-alvarez/null-ls.nvim) to run code formatters that aren't supported by the LSPs.

## useful stuff in my vimrc

### remove trailing whitespaces on save

```vim
autocmd BufWritePre *.py :%s/\s\+$//e
```

[source](https://vim.fandom.com/wiki/Remove_unwanted_spaces)

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

> edit: I now use [lualine](https://github.com/nvim-lualine/lualine.nvim)

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
dig :| 128528 " 😐
dig (: 128579 " 🙃
dig >: 128545 " 😡
dig :I 128556 " 😬
dig := 128557 " 😭
dig :o 128558 " 😮
dig :O 128561 " 😱
dig 8| 128563 " 😳
dig z: 128564 " 😴
dig xo 128565 " 😵
dig tx 128591 " 🙏
dig ok 128076 " 👌
dig mm 129292 " 🤌
```

> note: you could also use abbreviations with ``ab`` if you want vim to always replace that text in insert mode and don't want to enter a new mode.

[source](https://lual.dev/blog/how-to-use-emojis-with-vim/)

## useful links

- [nvim language server](https://github.com/neovim/nvim-lspconfig)
- [collection of good vim plugins](https://www.vi-improved.org/plugins/)
- [some funny](https://blog.samwhited.com/2015/04/the-dharma-of-vi/) [vim koans](https://blog.sanctum.geek.nz/vim-koans/) on the 'zen' of vim.[^1]

[^1]: [What is a koan?](https://en.wikipedia.org/wiki/Koan)
