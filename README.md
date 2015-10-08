# edebug

Purpose
-------

This is a repo and workflow for a simple Elixir scratchpad for Vim.

Installation
------------

1. Create a file in the root of this directory named `edebug.exs`. This is your scratchpad.
2. Use Vim.
3. Install [sjl](https://github.com/sjl/)'s [Clam.vim](https://github.com/sjl/clam.vim). Thanks, Steve!
4. Stick this (or something like it) in your [`.vimrc`](https://github.com/nicksergeant/dotfiles/blob/57a3fb24c16debff14fa5b5fcaffb989a670bda9/vimrc#L108):

`au BufWritePost edebug.exs execute "normal! :Clam elixir edebug.exs\<cr>"`

Usage
-----

I map `e` in my [Fish config](https://github.com/nicksergeant/dotfiles/blob/395f67d628f72850fad1d21ef020ec6d5846f4ba/config.fish#L152-L154),
and whenever I save the scratchpad (`edebug.exs`), a buffer updates with the result of running through Elixir. The
buffer remains until I close it, and it'll update each time I save the scratchpad, without losing focus of the
scratchpad buffer:

![http://i.nick.sg/image/0U3E051T3v2V/gif.gif](http://i.nick.sg/image/0U3E051T3v2V/gif.gif)
