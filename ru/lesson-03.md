---
layout: "lesson"
lang: "ru"
title: "Основная структура LaTeX-документа"
description: "Этот урок показывает основную структуру LaTeX-документа, то, как собирать его в файл PDF, и основные символы, ипользуемые в LaTeX."
toc-anchor-text: "Структура документа"
toc-description: "Основная структура документа."
---

# Структура документа в LaTeX

<span
  class="summary">Этот урок показывает основную структуру LaTeX-документа, то, как собирать его в файл PDF, и основные символы, ипользуемые в LaTeX.</span>

Ваш первый документ LaTeX будет очень простым: идея в том, чтобы показать
как документ выглядит и как успешно его записать. Кроме того, это ваш первый шанс
увидеть [как использовать примеры](help) на `learnlatex.org`.

Если вы используете локально установленную систему LaTeX, создайте в редакторе новый файл
с названием `first.tex` и просто скопируйте или перепечатайте приведённый ниже текст.

Если вы используете онлайн-систему, просто кликните на кнопку ‘Запустить на TeXLive.net’
или ‘Открыть в Overleaf’ в примере, чтобы попробовать!

<p
  class="hint">Предлагаем попробовать онлайн-способ, даже если вы установили LaTeX локально; это хорошая возможность увидеть, как по-разному они работают.</p>

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage[russian]{babel}

\begin{document}
Привет, мир! 

Это первый документ.
\end{document}
```

Сохраните файл и сконвертируйте его в документ PDF; если вы используете локальную
установку LaTeX, то нужная кнопка зависит от редакторы, который вы выбрали.
Вы должны получить на выходе файл PDF, содержащий текст _плюс_ номер
страницы; LaTeX автоматически его добавляет.

Посмотрите вывод в `first.pdf` в любой программе для просмотра PDF.
Выглядит круто, поздравляем!

Если вы хотите получить вывод в формате HTML, а не PDF, загляните в
[help](./help), чтобы узнать, как это сделать.

## Обработка ошибок

Ошибки случаются.
Проверьте, что вы ввели каждую строку текста в файл точно так же, как написано выше.
Иногда кажущиеся небольшими изменения ввода дают огромные изменения в
результате, включая невозможность создать документ.
Если вы застряли, попробуйти стереть весь текст и заново скопировать строки выше.

Если запуск вашего ввода в LaTeX заканчивается знаком вопроса, вы можете выйти
нажав `x` или `<Enter>`.

Сообщения об ошибках в LaTeX стараются быть полезными, но они не похожи на сообщения
в текстовых редакторах. Кроме того, некоторые редакторы не дают возможности увидеть 'полный' текст
ошибки, что может скрыть ключевые детали. LaTeX всегда создаёт лог с тем, что
он делает; это текстовый файл, оканчивающийся на `.log`. Вы всегда можете посмотреть там полное
сообщение оби ошибке, и, если у вас есть проблема, опытные пользователи LaTeX всегда попросят
у вас копию файла логов.

<p
  class="hint">Мы расскажем больше о том, как бороться с ошибками, в <a href="./lesson-15">уроке 15</a>.</p>

## Что вы получили

Первый документ показывает основы.
Документы LaTeX - это смесь текста и команд.
Команды начинаются с обратного слэша
и иногда принимают аргумент в фигурных скобках
(или, иногда, необязательные аргументы в квадратных скобках).
Затем вы получаете вывод в PDF, сообщив LaTeX о необходимости вывести файл.

Каждый документ LaTeX содержит `\begin{document}` и соответствующее
`\end{document}`.
Между ними находится *тело документа*, где находится содержимое.
Здесь тело содержит два параграфа (в LaTeX вы отделяете параграфы
с помощью одной или нескольких пустых строк).
Перед `\begin{document}` находится *преамбула документа*,
содержащая настройки макета документа.
Команда `\usepackage` описана в более [позднем уроке](lesson-06).
Она используется в большинстве примеров на этом сайте, чтобы установить кодировку
шрифта и возможность вывода текста на русском.

LaTeX включает другие пары `\begin{...}` и `\end{...}`; они
называются *среды*.
Вы должны сопоставлять их так, чтобы на каждое `\begin{x}` приходилось по одному `\end{x}`.
Если вы вкладываете их друг в друга, то вам надо будет иметь `\end{y} ... \end{x}`, чтобы
сопоставить с `\begin{x} ... \begin{y}`, т.е. команды `\begin` и `\end` сопоставляются в 
соответственном порядке.

Мы можем добавлять комментарии в файл LaTeX, начав с `%`; давайте используем
их, чтобы показать структуру:

```latex
\documentclass[a4paper,12pt]{article} % Класс документа с аргументами
% Выбирайте кодировку шрифта T1: подходит для латинского и кириллического алфавитов
\usepackage[T1]{fontenc}
\usepackage[russian]{babel}
% Комментарий в преамбуле
\begin{document}
% Это комментарий
Это простой
документ\footnote{со сноской}.

Это новый параграф.
\end{document}
```

You can see above that we've got two paragraphs: notice the use of a blank  line
to do that. Also notice that multiple spaces are treated as a single space.

You might also sometimes want a 'hard' space that does not break over lines: in
LaTeX we can create that using `~`, 'tying' two pieces of text together. That's
particularly useful when we start creating cross-references later in the course.

## Special characters

You've probably spotted that ``\``, `{` and `}` have a special meaning to LaTeX.
A ``\`` starts an instruction to LaTeX: a 'command'. The curly brace characters
 `{` and `}` are used to show _mandatory arguments_: information that commands
 require.

There are some other characters with special meaning; we've just seen that `~`
is a 'hard' space, for example. Almost all of these characters  are _very_
uncommon in normal text, which is why they were chosen for special meanings.
If you do need to show one of these special characters, we've put some
[information in the further details page](more-03).

## Exercise

Experiment with the online editing and typesetting system; click the
button to typeset the content, then edit it in the webpage and re-typeset it.

Try adding text to your first document, typesetting and seeing the changes in
your PDF. Make some different paragraphs and add variable spaces. Explore how
your editor works; click on your source and find how to go to the same line  in
your PDF. Try adding some hard spaces and see how they influence line-breaking.
