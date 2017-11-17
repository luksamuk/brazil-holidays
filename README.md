# brazil-holidays
Emacs helper file for defining org-mode Brazillian holidays.

## Installation

Create a path to drop your custom elisp files, if you don't have one already. In this example, I'll use `~/.emacs.d/lisp`.
Add this line to your `.emacs`:

```el
(add-to-list 'load-path (expand-file-name "~/.emacs.d/lisp"))
```

Then copy the file `brazil-holidays.el` to the folder you just added.

Now, require the holidays package:

```el
(require 'brazil-holidays)
```

## Configuration

If you wish to replace all your holidays with the ones in this package, add this to your `.emacs`, somewhere under the lines above:

```el
(setq calendar-holidays holiday-brazil-holidays)
```

However, if you wish to only append the brazillian holidays to your calendar:

```el
(setq calendar-holidays (append calendar-holidays holiday-brazil-holidays))
```

## TODO
Some resources for more holidays:
- https://www.calendarr.com/brasil/feriados-2017/

Actual TODO list:
- Add non-blocking, extra holidays (Dia Internacional da Mulher, etc): 'holiday-brazil-extra
- Add nontrivial holidays (Dia do Profissional de Informática, etc): 'holiday-brazil-nontrivial
- Add nontrivial lesser holidays (Dia do Programador, Dia da Toalha, etc): 'holiday-brazil-nerdy
