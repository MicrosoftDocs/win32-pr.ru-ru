---
title: Элемент TextPath VML
description: Элемент TextPath VML
ms.assetid: dcc3b723-4c5c-4069-93c7-c41737292109
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08707ae79bf297e6094228b26ae118c57a03c736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672289"
---
# <a name="vml-textpath-element"></a>Элемент TextPath VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет текстовый путь для фигуры.

Следующие атрибуты изменяют текстовый путь.



| attribute                                                                    | Описание                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [фитпас](msdn-online-vml-fitpath-attribute.md)                             | Определяет, соответствует ли текст контуру фигуры.                             |
| [фитшапе](msdn-online-vml-fitshape-attribute.md)                           | Определяет, соответствует ли текст границам фигур.                            |
| [Семейство шрифтов](msdn-online-vml-font-family-attribute.md)                     | Задает семейство шрифтов для текста.                                             |
| [Размер шрифта](msdn-online-vml-font-size-attribute.md)                         | Задает размер шрифта текста.                                               |
| [Стиль шрифта](msdn-online-vml-font-style-attribute.md)                       | Задает начертание текста.                                              |
| [Font-Variant](msdn-online-vml-font-variant-attribute.md)                   | Задает шрифтовый вариант текста.                                            |
| [Шрифт — вес](msdn-online-vml-font-weight-attribute.md)                     | Задает шрифт текста.                                             |
| [Шрифт](msdn-online-vml-font-attribute.md)                                   | Задает значение составного шрифта Text.                                     |
| [MSO-text-shadow](msdn-online-vml-mso-text-shadow-attribute.md)             | Определяет, применяется ли к тексту тень.                               |
| [On](on-attribute--textpath--vml.md) (Вкл.)                                        | Определяет, отображается ли текст.                                         |
| [String](msdn-online-vml-string-attribute.md)                               | Определяет текстовую строку.                                                       |
| [Оформление текста](msdn-online-vml-text-decoration-attribute.md)             | Определяет Оформление текста в тексте.                                       |
| [Trim](msdn-online-vml-trim-attribute.md) (Усечь)                                   | Определяет, удаляется ли дополнительное пространство выше и ниже текста.               |
| [V-вращение-буквы](msdn-online-vml-v-rotate-letters-attribute.md)           | Определяет, поворачиваются ли буквы текста.                        |
| [V-та же высота по буквам](msdn-online-vml-v-same-letter-heights-attribute.md) | Определяет, будут ли все буквы иметь одинаковую высоту.                      |
| [V-Text-выровняйте](msdn-online-vml-v-text-align-attribute.md)                   | Определяет выравнивание текста.                                             |
| [V-Text-кернинг](msdn-online-vml-v-text-kern-attribute.md)                     | Определяет, включен ли кернинг.                                       |
| [V-Text-Reverse](msdn-online-vml-v-text-reverse-attribute.md)               | Определяет, изменяется ли порядок макета строк на обратный.                       |
| [V-текстовые пробельные режимы](msdn-online-vml-v-text-spacing-mode-attribute.md)     | Определяет режим для леттерспаЦинг.                                            |
| [V-текстовые отступы](msdn-online-vml-v-text-spacing-attribute.md)               | Определяет величину интервала для текста.                                        |
| [®](msdn-online-vml-xscale-attribute.md)                               | Определяет, будет ли использоваться прямой текстпас вместо пути к фигуре. |



 

**Замечания**

Этот элемент должен быть определен внутри элемента [Shape](shape-element--vml.md) .

Помимо обычных атрибутов заливки, строки и стиля, атрибуту [Текстпасок](msdn-online-vml-textpathok-attribute.md) [пути](msdn-online-vml-path-element.md) должно быть присвоено значение **true** , а атрибуту [On](on-attribute--textpath--vml.md) текстпас должно быть присвоено значение **true** для вывода текста на текстовый путь.

Ниже приведен минимальный код, необходимый для вывода текста на путь.


```HTML
   <v:line from="50 200" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



**Примеры**

-   [Пример простого Текстпас](/previous-versions/bb264038(v=vs.85))
-   [Пример динамического Текстпас гарнитуры](/previous-versions/bb264042(v=vs.85))
-   [Пример динамической Текстпас кривой](/previous-versions/bb264041(v=vs.85))

 

 