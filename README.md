# spell-under

<!-- vim: set sw=2 sts=2 et tw=78 ft=markdown: -->

This `spell-under` is a simple vim plugin to change highlight scheme of
spelling checker to use "UNDERLINE" instead of default "REVERSE" for color
terminals when `:colorscheme` is set.

This enables you to use both `:syntax on` and `:set spell` by avoiding
unreadable text situation due to matched reversed background color and syntax
highlighted foreground text color.

# Installation

The latest version of `spell-under` is available on github. [1]

This plugin follows the vim standard runtime path structure, and as such it
can be installed with a variety of plugin managers:

| Plugin Manager  | Install with... |
| --------------- | ------------- |
| [Pathogen][2]   | `cd ~/.vim/bundle/vim-spell-under && git clone https://github.com/osamuaoki/vim-spell-under`<br/>Remember to run `:Helptags` to generate help tags |
| [Vundle][3]     | `Plugin 'osamuaoki/vim-spell-under'` |
| [Plug][4]       | `Plug 'osamuaoki/vim-spell-under'` |
| [VAM][5]        | `call vam#ActivateAddons([ 'vim-spell-under' ])` |
| [Dein][6]       | `call dein#add('osamuaoki/vim-spell-under')` |
| [minpac][7]     | `call minpac#add('osamuaoki/vim-spell-under')` |
| manual          | copy all of the files into your `~/.vim` directory |
| manual (vim>=8) | `cd ~/.vim/pack/somepath/start && git clone https://github.com/osamuaoki/vim-spell-under` <br/>Remember to run `:Helptags` to generate help tags |

The author of this script uses an extended installation approach based on
"manual (vim>8)" with a shell script based menu system. See
[osamuaoki/dot-vim][8].

# How it works

Once `spell-under` is installed, Vim behaves as follows:

* If `g:spell_under` is unset in `.vimrc`, `spell-under` defaults to using
  `colorscheme` (via `g:colors_name`), or `"NONE"` if both are undefined.
* If `.vimrc` has `let g:spell_under='<scheme>'`, `spell-under` executes
  `:colorscheme <scheme>` and fixes up spell checker to use "UNDERLINE".
* If `.vimrc` has `let g:spell_under='NONE'`, `spell-under` doesn't executes
  `:colorscheme <scheme>`.
* When you execute `colorscheme <scheme>` from any script after parsing this
  plugin or from the vim command prompt, vim sets colorscheme accordingly and
  fixes up spell checker to use "UNDERLINE".
* If `g:loaded_spell_under` is set to 1, `spell-under` plugin has been
  loaded.


# License

MIT License. Copyright (c) 2019 Osamu Aoki


[1]: https://github.com/osamuaoki/vim-spell-under
[2]: https://github.com/tpope/vim-pathogen
[3]: https://github.com/VundleVim/Vundle.vim
[4]: https://github.com/junegunn/vim-plug
[5]: https://github.com/MarcWeber/vim-addon-manager
[6]: https://github.com/Shougo/dein.vim
[7]: https://github.com/k-takata/minpac
[8]: https://github.com/osamuaoki/dot-vim

