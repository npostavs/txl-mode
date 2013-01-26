Emacs Major Mode for TXL

Contributed by Markus Stoy, mstoy@gmx.de, Rostock (Germany), November/December 2003
Updated for Emacs/X-Emacs compatibility, Ivan N. Veselov, veselov@gmail.com, October 2008
A few updates and enhancements, Noam Postavsky, see https://github.com/npostavs/txl-mode

Installation
------------

1. Copy the file txl-mode.el to a directory where Emacs can find it
   (somewhere within load-path).  To install for yourself only, 
   this can often be in a directory called ".elisp" in your home directory.
   To install for everyone on your system, it should be in the Emacs 
   site-lisp directory, often "/usr/local/share/emacs/site-lisp".

2. Add the following two lines to the Emacs init file (normally ".emacs"
   or "init.el") in your home directory.

    (require 'txl-mode)
    (add-to-list 'auto-mode-alist '("\\.\\([tT]xl\\|[gG]rm\\|[gG]rammar\\|[rR]ul\\(es\\)?\\|[mM]od\\(ule\\)?\\)$" . txl-mode))

3. Test by editing a TXL source file.

Features
--------
   - syntax highlighting (with font-lock-mode)
   - automatic indentation according to TXL style guide (perhaps stil buggy...)
   - compile/debug/run TXL program from within Emacs
   - comment/uncomment regions
   - insert skeletion rules/functions/defines, find and insert matching end's
   - abbreviations for keywords (with abbrev-mode; scroll down to see a list)
   - TXL submenu which contains all new functions and their keyboard shortcuts

Wish list
---------
   - navigation (jump to nonterminal/function/rule under cursor, 
     next/previous nonterminal/function/rule, ...)
   - use comint for run/debug/compile instead of simple shell-command? 
     (which looks ugly under Windows)

Known bugs
----------
   - 'x% is highlighted as comment
   - compile and debug don't work under Windows
