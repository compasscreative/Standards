PHP
===

## Environment
- We host all our websites in a LAMP (Linux, Apache, MySQL, Linux) environment.
- Please optimize for `PHP 5.4`.

## Coding Standards

We follow the [PHP-FIG](http://www.php-fig.org/) (PHP Framework Interop Group) coding standards, in particular the [PSR-1](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md) and [PSR-2](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md) recommendations. The only exception is for views, which have their own set of standards (see below).

## Views

### Introduction

Our projects use the [Reveal](https://github.com/reinink/Reveal) library for views. Please see that project for full documentation. Reveal is not templating engine, rather is simply makes working with PHP based views easier. We've created the following rules for how our views should be programmed:

### Rules

- Always use the extension `.tpl` for views.
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

### Example

```php
<?
$this->title = $e($this->gallery->title);
$this->insert('partials/header');
?>

<h1><?=$e($this->gallery->title)?></h1>

<ul>
    <? foreach ($this->photos as $photo): ?>
        <li>
            <a href="<?=$e($photo->xlarge_url)?>" title="<?=$e($photo->caption)?>">
                <img src="<?=$e($photo->small_url)?>" alt="<?=$e($photo->caption)?>" />
            </a>
        </li>
    <? endforeach ?>
</ul>

<div class="description"><?=$this->gallery->description?></div>

<h2>Other Galleries</h2>
<ul>
    <? foreach($this->other_galleries as $gallery): ?>
        <li>
            <a href="<?=$e($gallery->url)?>">
                <img src="<?=$e($gallery->photo_url)?>" alt="<?=$e($gallery->photo_caption)?>">
                <h3><?=$e($gallery->title)?></h3>
            </a>
        </li>
    <? endforeach ?>
</ul>

<? $this->insert('partials/footer'); ?>
```