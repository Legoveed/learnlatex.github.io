---
layout: "lesson"
lang: "ru"
title: "Специфика русского языка"
description: "Этот урок показывает подробности, специфичные для работы в LaTeX на русском."
next: "extra-01"
toc-anchor-text: "Специфика русского языка"
toc-description: "Использовани LaTeX на русском."
---

# Специфика русского языка

<span
  class="summary">Этот урок показывает подробности, специфичные для работы в LaTeX на русском.</span>

## Использование русского языка в тексте

LaTeX был создан для написания текстов на английском, но
добавление русского языка несложно и осуществляется
с помощью добавления его из пакета `babel`.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage[russian]{babel}
\begin{document}
Some text and какой-то текст
\end{document}
```
