PHP
===

## Environment
- We host all our websites in a LAMP (Linux, Apache, MySQL, Linux) environment.
- Please optimize for `PHP 5.4`.

## Views

- Always use `HTML` with inline `PHP`.
- Never use blocks of `PHP`.
- Always escape all variables prior to outputting. Use the built-in shortcut `$e()`.
- Always use short tags `<?`, `<?=` and `?>`.
- Never use the standard `<?php` tag.
- Always use the [alternative syntax for control structures](http://php.net/manual/en/control-structures.alternative-syntax.php).
- Never use PHP curley brackets.
- Always have only one statement in a tag each.
- Never use the `use` operator.
- Never access the database layer.
- Always use the `if` and `foreach` control structures.
- Never use the `for`, `while` or `switch` control structures.
- Always avoid assigning variables.