### 0.3.0

- rewrite [`license` module][] to cache HTTP responses
- hide the current buffer's name in license headers when `g:cpywrite#hide_filename` is set to a non-zero value
- provide a `:CPYwriteToggleFilename` command
- identify licenses by full name when there's no standard header

**Note.** To keep longer names like (e.g.) the `LGPLvXX` from running off the screen, enable line wrapping in your `vimrc` or `init.vim`:

```vim
set lbr
set tw=500 "break after 500 characters
set wrap "wrap lines
```

- detect `.vimrc`, `.gvim`, `.ideavim` and `.exrc` as Vim files
- add support for these file types:
  - D
  - Edn (.edn)
  - Fennel
  - Markdown
  - ReactJS (.jsx) and ES Module (.mjs)
  - Scala
  - Swift

### 0.2.1

- add support for these file types:
  - Ada
  - Assembler
  - Coffescript
  - Elixir
  - Elm
  - Erlang
  - Kotlin
  - Lua
  - Objective-C
  - Pascal

- recognize `.vimrc` as VimL
- prevent copyright notice for appearing on public domain (i.e. copyright-free) licenses, in both modes
- fix regex that was inserting authorship at random places in full license text
- leave one blank line after header
- improve load time of `autoload/cpywrite.vim`

### 0.2.0

- extract feature tests and core functions to `autoload` directory to improve startup time ([#2][pr2])
- suggest [`set wildmenu`](README.md#highlights) for faster completions when not using neovim

### 0.1.1

- convenience commands for getting/setting global options:
    - `:CPYwriteDefaultLicense` -- supports `<tab>` completion
    - `:CPYwriteToggleMode` -- switches `g:cpywrite#verbatim_mode` on/off

- relaxed file naming rules to accept full paths

- recognize *CMakeLists* files with the `.txt` extension

- apply line wrapping to keep standard headers within 80 chars (still in progress; expect mixed results)

- brief notices are now fully capitalized

- better-looking standard headers for the older GPL and GFDL licenses families

### 0.1.0

- initial release


[pr2]: https://github.com/rdipardo/vim-cpywrite/pull/2
[`license` module]: https://github.com/rdipardo/vim-cpywrite/blob/master/rplugin/pythonx/cpywrite/spdx/license.py
