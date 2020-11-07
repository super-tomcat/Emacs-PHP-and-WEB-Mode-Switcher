# Emacs-PHP-and-WEB-Mode-Switcher
Quickly switch the emacs buffer from PHP mode and WEB modes

Useful for anyone working with PHP files in Emacs

Add this snippet of code to your emacs init.el file and set up what ever keybindings you want, the default
keybindings are Ctrl-Meta m, in both PHP and Web modes

```
;
(require 'php-mode)
(require 'web-mode)
(defun neils-switch-php-web-mode ()
  "Switches modes between PHP mode and Web mode"
        (interactive)
        (if (derived-mode-p 'php-mode)
         (web-mode)
            (php-mode)))
;
; keybindings to the above
(define-key php-mode-map (kbd "C-M-m") 'neils-switch-php-web-mode)
(define-key web-mode-map (kbd "C-M-m") 'neils-switch-php-web-mode)
;
```

