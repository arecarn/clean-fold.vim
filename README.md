clean-fold
==========

clean-fold provides alternatives to the default foldtext cleans up the
appearance of folds. This plugin also provides a new fold expression that is
an alternative to the built-in indent method of folding, that includes the
line before the indent as well as the following indented lines.

Fold Text Style
----------------
Alternatives to the default foldtext and a new foldmethod

* `clean_fold#fold_text(foldchar)`
    * cleaner alternative to default fold text, still including number of folded lines
    ```vim
    set foldtext=clean_fold#fold_text('_')
    ```

* `clean_fold#fold_text_minimal()`
    * just include the text on the line except fold markers
     ```vim
     set foldtext=clean_fold#fold_text_minimal()
     ```

Fold Expression
---------------
A new foldexpr set up so  lines that are at the same indented level are
folded along with the first line above them one indent level up.

* `clean_fold#fold_expr(lnum)`
    * like indent folding but also include first line that is one indent level lower
     ```vim
     set foldmethod=expr
     set foldexpr=clean_fold#fold_expr(v:lnum)
      ```
