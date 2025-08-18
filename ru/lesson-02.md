---
layout: "lesson"
lang: "ru"
title: "Работа в LaTeX"
description: "Этот урок объясняет, что такое система TeX и какие системы наиболее распространены, так же приведён список текстовых редакторов, чаще всего используемых для LaTeX и онлайн-систем, которые имеют встроенные редакторы."
toc-anchor-text: "Работа в LaTeX"
toc-description: "Системы TeX и текстовые редакторы LaTeX."
---

# Работа в LaTeX

<span
  class="summary">Этот урок объясняет, что такое система TeX и какие системы наиболее распространены, так же приведён список текстовых редакторов, чаще всего используемых для LaTeX и онлайн-систем, которые имеют встроенные редакторы.</span>


В отличие от многих компьютерных программ, LaTeX - не единое приложение, содержащее
'всё' в одном. Наоборот, существуют различные программы, которые работают вместе.
Мы можем выделить из них на две вещи, которые вам сейчас понадобятся:

- _Система TeX_
- Текстовый редактор (обычно специально для LaTeX)

## Системы LaTeX

Ядро работы с LaTeX содержит систему TeX. Система TeX - набор
программ, работающих 'за кулисами', необходимых для работы LaTeX, которые
в большинстве случаев вам не нужно непосредственно 'запускать'.

На текущий момент, доступны две главные системы TeX,
[MiKTeX](https://miktex.org/) и [TeX Live](https://tug.org/texlive). Обе
доступны под Windows, macOS и Linux.
MiKTeX строго заточен под Windows;
для macOS, TeX Live включён в большой сборник под названием [MacTeX](http://www.tug.org/mactex/).
У каждой системы есть [преимущества](https://tex.stackexchange.com/questions/20036), 
и вы можете прочитать [советы от LaTeX
Project](https://www.latex-project.org/get/).

Так как TeX Live доступен на большинстве платформ и так как у него есть преимущества
в производительности, если вы не уверены, какую систему устанавливать, мы рекомендуем вам
выбрать TeX Live.

## Редакторы

LaTeX files are simply plain text, so they can be edited with any text editor.
However, it's most convenient to have an editor that is designed to work with
LaTeX, as they provide features like one-click compilation of your files,
built-in PDF viewers, and syntax highlighting. A really useful feature in all
modern LaTeX editors is SyncTeX: the ability to click on your source and go
straight to your PDF, or back the other way.

There are many more LaTeX editors than we can hope to list here: there is a
[comprehensive list on
StackExchange](https://tex.stackexchange.com/questions/339/latex-editors-ides).
A basic editor, [TeXworks](https://tug.org/texworks), is included in TeX Live
and MiKTeX on Windows and Linux, and [TeXShop](https://pages.uoregon.edu/koch/texshop/)
is included in MacTeX.

<p 
  class="hint">Whichever editor you pick, we recommend you install it <i>after</i> your TeX system, so that the editor can 'find' the TeX system and set itself up correctly.</p>

## Working online

There are several powerful online sites that allow you to avoid
the need to install a TeX system and LaTeX editor at all. These websites
work by letting you edit your files in the webpage, then they run LaTeX
behind the scenes, and display the PDF that is produced.

Some of these sites combine LaTeX with features similar to a word processor,
whereas others are more focused on letting you see the LaTeX code and
so are closer to having a local installation.

There are systems that let you run LaTeX without needing to be logged in, and we
are using one of those,
[TeXLive.net](https://texlive.net), to let you
edit and test the examples we give. For more complete work, the best online
systems require that you register before you use them. That lets you save your
work but also helps the sites not get overloaded. We have set up links so you
can edit our examples using [Overleaf](https://www.overleaf.com), one of the
major websites for LaTeX online. There are of course others:
[Papeeria](https://papeeria.com/) is an example.

## Working with others

If you are planning to send your LaTeX sources to destinations which process
them, such as publishers, conference organisers or pre-print servers
(e.g. arXiv), you should check what restrictions they impose.

## Exercise

Get yourself set up with a local LaTeX installation _or_ an account with
an online LaTeX service. If you are using a local installation, you'll need
to pick an editor too: we recommend starting with either TeXworks or TeX Shop
(see above), then looking at other editors later once you know how _you_
work best with LaTeX.

You'll be able to [run all of our other exercises in your browser](help.md), but we want
to help you get working with real documents, so now is a great time to get
yourself ready.
