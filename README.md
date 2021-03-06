# evil-space

[vim-space](https://github.com/linktohack/vim-space) for `evil-mode`

`evil-space` is intend to be a ported version of `vim-space` for `evil-mode`
with some enhanced features such as remember count motions, e.g.

    9j SPC SPC SPC

## Install

The easiest way to install `evil-space` is by `package.el` through melpa
[melpa](http://melpa.milkbox.net/#/getting-started) then try it with

```lisp
M-x evil-space-default-setup
```

To enable `evil-space` permanently, add

```lisp
(evil-space-default-setup)
```

to your `init.el`.

Or manually by clone `evil-space` to your `load-path`, then add those
lines to the `init.el`.

```lisp
(add-to-list 'load-path "/path/to/evil-space")
(require 'evil-space)
(evil-space-default-setup)
```

## Default setups

The default setups `(evil-space-default-setup)` will
enable repeat for these motions:

```
/?nN (search)
tTfF (next character in line)
}{ (paragraph)
]] and [[ (function)
```

If you don't like the default behavior for `evil-space` you can
enable the key motion you want manually:

```lisp
(add-to-list 'load-path "/path/to/evil-space")
(require 'evil-space)
(evil-space-setup "t" ";" ",")
(evil-space-setup "f" ";" ",")
(evil-space-setup "T" "," ";")
(evil-space-setup "F" "," ";")
```

## Key triggers

The default key triggers are `<SPC>` and `<S-SPC>` but you can
customize them to your like by:

```lisp
M-x customize-group RET evil-space RET
```

## Further information

Pull requests are very welcome, for further information, make an issue
or contact me at linktohack@gmail.com.
